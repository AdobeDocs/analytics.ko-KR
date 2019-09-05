---
title: 내부 트래픽
description: 내부 트래픽 플러그인은 내부 네트워크에서 온 방문자를 동적으로 식별합니다.
seo-description: Internal Traffic Plugin
seo-title: Internal Traffic Plugin
translation-type: tm+mt
source-git-commit: 8c2b28ee1ca2e9448b9dec99a0505d0fae525e94

---


# 내부 트래픽

내부 트래픽 플러그인은 내부 네트워크에서 온 방문자를 동적으로 식별합니다.

수집 중인 데이터를 필터링하는 메커니즘을 제공함으로써 내외부 트래픽은 모든 유형의 보고에서 더 정확하게 정확도를 높입니다. 올바르게 구현되면 이러한 트래픽을 식별하는 일반적인 접근 방식인 VISTA 규칙 또는 처리 규칙의 필요성을 없앨 수 있습니다.

## 내부 트래픽 플러그인은 어떻게 작동합니까?

플러그인은 내부 네트워크/인트라넷에서만 사용할 수 있는 파일 (예: 1 x 1 투명 픽셀) 를 로드하려고 시도합니다. 성공적으로 로드되면 해당 방문자에 대한 트래픽이 내부 트래픽으로 식별됩니다. 다른 것은 외부 트래픽입니다.

## 고려 사항

* 이 방법의 유일한 단점은 방문의 첫 번째 페이지에서 외부 방문자를 위해 브라우저 콘솔에 404 오류가 표시된다는 것입니다. 이는 사용자 경험에 영향을 주지 않습니다.
* 내부적으로 호스팅되는 픽셀을 로드하기 전에 네트워크 또는 인포섹 팀의 승인을 받을 것을 적극 권장합니다.
* 플러그인은 트래픽을 다른 보고서 세트로 이동시키지 않고 보고에서 제외하지 않지만 (VISTA 규칙 사용 가능), 사용자 지정 논리를 구현에 포함할 수 있으므로 이 기능은 클라이언트측에서 실행될 수 있습니다.

## 구현

1. 인트라넷 픽셀 추가: 인트라넷에 액세스하려는 파일 유형을 추가할 수 있습니다. 1 x 1 투명 픽셀이 권장됩니다. 내부 네트워크에서 광범위하게 액세스할 수 있는 인트라넷 위치에 배치해야 합니다.
1. Evar 구성: Evar를 대상 보고서 세트 내에 추가해야 합니다. " 방문 "과" 원래 값 (처음) "의 할당이 있어야 합니다.
1. 내부 URL 정의: Appmeasurement 구성 변수 내에서 doplugins가 인스턴스화되는 전 픽셀 또는 다른 파일에 대한 내부 URL 변수 (s. inturl) 를 트래픽 확인에 사용할 수 있습니다. 예: `s.intURL = "https://www.yourdomainhere.com/trafficCheck.gif"`
1. Doplugins를 수정하고 evar를 설정합니다. 그런 다음 1 단계에서 정의된 Evar를 사용하여 appmeasurement 라이브러리 코드의 doplugins 섹션 내에 이 코드 행을 포함시켜 플러그인을 초기화할 수 있습니다. `s.eVarXX = s.intCheck();`
변수 값은 «내부» 또는 «외부» 로 설정됩니다.
1. 플러그인 소스 코드를 추가합니다. Appmeasurement 파일의 doplugins 섹션 아래에 플러그인 코드를 포함시킵니다.

## 플러그인 소스 코드

Appmeasurement 라이브러리의 doplugins 섹션 아래에 이 코드를 추가합니다.

```JavaScript
s.intCheck=new Function("",""
+"var s=this;if(document.cookie.indexOf('intChk=')==-1){try{document."
+"cookie='intChk=1';var x=new XMLHttpRequest(),y;x.open('GET',s.intUr"
+"l,false);x.send();if(x.status===200&&x.statusText==='OK'){y='intern"
+"al';}}catch(e){y='external'}finally{return y}}");
```

## 기타 참고 사항

* 프로덕션 환경에 배포하기 전에 항상 플러그인 설치를 테스트하여 데이터 수집이 예상대로 이루어지도록 하십시오.
* 구현에서 기본 Adobe Analytics "s" 개체 이외의 다른 개체 이름을 사용할 수 있습니다. 그런 경우 개체 이름을 적절하게 업데이트하십시오.
* 태그 관리 시스템을 사용하는 경우 해당 단계에 따라 Doplugins 및 기타 사용자 정의 플러그인을 업데이트하십시오.
