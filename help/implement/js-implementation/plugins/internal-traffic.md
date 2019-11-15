---
title: 내부 트래픽
description: 내부 트래픽 플러그인은 내부 네트워크에서 온 방문자를 동적으로 식별합니다.
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 내부 트래픽

내부 트래픽 플러그인은 내부 네트워크에서 온 방문자를 동적으로 식별합니다.

내부 및 외부 트래픽을 식별하면 수집 중인 데이터를 필터링하고 세그먼트화하는 메커니즘을 제공하여 모든 유형의 보고에서 정확성을 높일 수 있습니다. 올바르게 구현되면 그러한 트래픽을 식별하는 일반적인 방법인 VISTA 규칙 또는 처리 규칙이 필요하지 않습니다.

## 내부 트래픽 플러그인은 어떻게 작동합니까?

이 플러그인은 내부 네트워크/인트라넷(예: 1x1 투명 픽셀)에서만 사용할 수 있는 파일을 로드하려고 합니다. 성공적으로 로드되면 해당 방문자에 대한 트래픽이 내부로 식별됩니다. 그 밖의 트래픽은 외부 트래픽으로 식별됩니다.

## 고려 사항

* 이 방법은 외부 방문자의 브라우저 콘솔에서 방문하는 첫 페이지에 404 오류가 표시되는 유일한 단점이 있습니다. 사용자 경험에는 영향을 주지 않습니다.
* 내부적으로 호스팅된 픽셀을 로드하기 전에 네트워크 또는 InfoSec 팀의 승인을 받는 것이 좋습니다.
* 플러그인이 다른 보고서 세트로 트래픽을 이동하지 않거나 보고서에서 제외하지는 않지만(VISTA 규칙에서 수행되는 것처럼) 사용자 지정 논리를 해당 구현에 포함할 수 있으므로 이 기능이 클라이언트 측에서 수행될 수 있습니다.

## 구현

1. 인트라넷 픽셀 추가: 플러그인이 액세스를 시도하는 모든 유형의 파일을 인트라넷에 추가할 수 있습니다. 1x1 투명 픽셀을 권장합니다. 내부 네트워크에서 광범위하게 액세스할 수 있는 인트라넷의 위치에 배치해야 합니다.
1. eVar 구성: eVar를 대상 보고서 세트 내에 추가해야 합니다. "방문" 만료 및 "원래 값(처음)"의 할당이 있어야 합니다.
1. 내부 URL 정의: AppMeasurement 구성 변수 내에서 doPlugins가 인스턴스화되기 전에 픽셀에 대한 내부 URL 변수(s.intURL)를 정의합니다. 정의하지 않으면 트래픽 검사에 다른 파일이 사용될 수 있습니다. 예: `s.intURL = "https://www.yourdomainhere.com/trafficCheck.gif"`
1. Modify doPlugins and set the eVar: The plugin can then be initialized by including this line of code within the doPlugins section of your AppMeasurement library code, using the eVar defined in step one: `s.eVarXX = s.intCheck();`
The variable value will be set to "internal" or "external".
1. 플러그인 소스 코드 추가: AppMeasurement 파일의 doPlugins 섹션 아래에 플러그인 코드를 추가합니다.

## 플러그인 소스 코드

AppMeasurement 라이브러리의 doPlugins 섹션 아래에 이 코드를 추가합니다.

```JavaScript
s.intCheck=new Function("",""
+"var s=this;if(document.cookie.indexOf('intChk=')==-1){try{document."
+"cookie='intChk=1';var x=new XMLHttpRequest(),y;x.open('GET',s.intUr"
+"l,false);x.send();if(x.status===200&&x.statusText==='OK'){y='intern"
+"al';}}catch(e){y='external'}finally{return y}}");
```

## 기타 참고 사항

* 프로덕션 환경에 배포하기 전에 항상 플러그인 설치를 테스트하여 데이터 수집이 예상대로 수행되는지 확인합니다.
* 구현에서는 기본 Adobe Analytics "s" 개체가 아닌 다른 개체 이름이 사용될 수 있습니다. 그런 경우 개체 이름을 적절하게 업데이트하십시오.
* Tag Management 시스템을 사용하는 경우 해당 단계에 따라 doPlugins 및 기타 사용자 정의 플러그인을 업데이트하십시오.
