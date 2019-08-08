---
description: DFA용 Genesis 통합은 DFA Floodlight 구성 ID(dfa_SPOTID)를 활용하여 DFA와 Adobe 데이터 수집 시스템 간에 보고서 일관성을 향상시킵니다.
keywords: DFA
seo-description: DFA용 Genesis 통합은 DFA Floodlight 구성 ID(dfa_SPOTID)를 활용하여 DFA와 Adobe 데이터 수집 시스템 간에 보고서 일관성을 향상시킵니다.
seo-title: 웹 사이트의 데이터 수집 코드 업데이트
solution: Analytics
title: 웹 사이트의 데이터 수집 코드 업데이트
topic: Data connectors
uuid: A 97 D 1 B 62-F 883-48 B 1-9516-4 F 889 E 701901
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# 웹 사이트의 데이터 수집 코드 업데이트{#update-your-web-site-s-data-collection-code}

DFA용 Genesis 통합은 DFA Floodlight 구성 ID(dfa_SPOTID)를 활용하여 DFA와 Adobe 데이터 수집 시스템 간에 보고서 일관성을 향상시킵니다.

>[!NOTE]
>
>Google DFA의 최근 릴리스에서 용어 스포트라이트가 Floodlight로 변경되었습니다. JavaScript 매개 변수 `dfa_SPOTID`는 Spotlight 용어를 기반으로 명명되었지만 두 버전에 모두 사용됩니다.

웹 사이트에서 DFA 통합을 활성화하려면 다음을 추가하여 JavaScript 데이터 수집 코드를 업데이트해야 합니다.

* DFA에 대한 통합 모듈
* 수집 코드에 추가

## DFA에 대한 통합 모듈 {#section-fa00e42a732a4e27a4ab3dfcfeae1a5b}

DFA 통합은 핵심 JavaScript 데이터 수집 코드(`s_code.js`)에 기능을 추가하는 Adobe Marketing Cloud 통합 모듈을 사용합니다. 통합 모듈은 [코드 관리자에서 Javascript 용 appmeasurement 코드를 다운로드할 때.zip 파일의 일부로 제공됩니다](https://marketing.adobe.com/resources/help/en_US/reference/code_manager_admin.html). 추가 도움이 필요한 경우 Adobe 컨설턴트에게 문의하십시오.

Insert the Integrate Module code in the `Modules` section of your website's `s_code.js` file.

## 수집 코드에 추가 {#section-8f98c727f1ba414fb8b4f02d696b8791}

통합 마법사에서 DFA 통합을 활성화할 때 선택한 항목에 따라 Data Connectors가 JavaScript 데이터 수집 코드에 대한 사용자 정의된 추가 항목을 이메일로 보냅니다. `s_code.js` 함수 또는 다른 함수가 아닌 `doPlugins` 파일의 기본 섹션에 이 코드를 삽입합니다.

아래 표시된 샘플 코드는 단순한 예시용입니다. Data Connectors 통합 마법사를 완료한 후에 이메일로 전송된 코드를 사용하십시오.

수집 코드는 다음 구성 요소로 구성됩니다.

* DFA 통합 설정
* 통합해야 하는 플러그인

**DFA 통합 설정**

```
/************************** DFA VARIABLES **************************/ 
var dfaConfig = { 
   CSID:              "1234567", 
   SPOTID:            "29876543", 
   tEvar:             "eVar17", 
   errorEvar:         "eVar59", 
   timeoutEvent:      "event76", 
   requestURL:         "http://fls.doubleclick.net/ 
json?spot=[SPOTID]&src=[CSID]&var=[VAR]&host=integrate.112.2o7.net%2 
Fdfa_echo%3Fvar%3D[VAR]%26AQE%3D1%26A2S%3D1&ord=[RAND]", 
 
   maxDelay:          "1500", 
   visitCookie:       "s_dfa", 
   clickThroughParam: "CID", 
   searchCenterParam: "s_kwcid", 
   newRsidsProp:      undefined 
}; 
/************************ END DFA Variables ************************/ 
```

DFA 통합 설정 블록은 DFA 통합에 필요한 변수를 설정합니다. 이러한 각 변수에 대한 값은 다음 소스에서 제공됩니다.

**CSID**: 클라이언트측 ID. 통합 마법사를 완료하면 DFA에서 생성합니다. Data Connectors는 이 변수를 DFA CS ID로 먼저 채우고, 사용자가 통합 마법사를 완료하면 사용자에게 설정 이메일로도 이 값을 보냅니다. 이 변수는 계정에 [고급 광고 제공 기능]이 활성화된 경우 필요하지 않습니다.

**SPOTID**: Floodlight 구성(이전에 Spotlight ID라고 함). Data Connectors는 사용자가 통합 마법사에 지정한 DFA 계정 정보에 따라 이 변수를 DFA Floodlight 구성 ID로 미리 채웁니다.

**tEvar**: 전송 변수. Data Connectors는 통합 마법사에 뷰스루 변수에 대해 지정한 Analytics 변수 이름으로 이 변수를 미리 채웁니다. 이 값은 반드시 Adobe 엔지니어링 또는 엔지니어링 서비스를 통해 신중하게 조정하여 변경해야 합니다.

**errorEvar**: 오류 변수. Data Connectors는 통합 마법사에 DFA 쿼리 오류 변수에 대해 지정한 Analytics 변수 이름으로 이 변수를 미리 채웁니다.

**timeoutEvent**: 시간 초과 이벤트. Data Connectors는 통합 마법사에 시간 초과 이벤트 변수에 대해 지정한 Analytics 변수 이름으로 이 변수를 미리 채웁니다.

**requestURL**: 광고 정보를 쿼리할 원격 DFA 호스트. Adobe의 지시 없이는 이 값을 변경하지 마십시오.

**maxDelay**: JavaScript 데이터 수집 코드가 DFA Floodlight 서버로부터 응답을 기다리는 시간(밀리초)을 지정합니다. Adobe는 이 값으로 테스트하여 사이트 트래픽에 따라 최적의 값을 찾을 것을 권장합니다. 예를 들어 이 값을 늘리면 일반적으로 더 많은 DFA 데이터가 수집되지만, 방문자가 지연 기간 동안 사이트를 나가는 경우 기본 방문자 데이터가 손실될 위험이 높아집니다. 이 값을 줄이면 히트 데이터 손실 위험은 줄어들지만 Adobe 히트 데이터로 전송된 DFA 데이터 양이 줄어들 수 있습니다.

**visitCookie**: DFA 호출 횟수를 방문당 한 번으로 제한하는 데 사용되는 쿠키의 이름입니다.

**clickThroughParam**: 클릭이 방금 발생했음을 통합 모듈에 알리는 쿼리 문자열로 일반적으로 모든 광고에 포함됩니다. 쿼리 문자열에 이 매개 변수가 있으면 방문자가 이미 30분 전에 쿼리했는지 여부에 상관없이 요청이 DFA Floodlight 서버로 전달됩니다.

**newRsidsProp**: (선택 사항) 사용되지 않은 트래픽 속성 변수에 매핑됩니다. DFA 통합은 이 값을 수집하고 방문 쿠키에 저장하여 특정 방문자에 대한 데이터를 수집한 보고서 세트를 식별합니다. 이 속성은 Adobe 엔지니어링 서비스에서 사용자 지정 구현에만 필요합니다.

**통합해야 하는 플러그인**

수집 코드 추가 기능은 DFA 통합 작업을 향상시키는 추가 플러그인을 통합합니다.

* DFA 쿼리를 방문당 한 번으로 제한합니다.
* 유연한 쿠키 이름을 제공합니다. 대부분의 조직에서 s_dfa를 사용하지만 DFA 통합에 유효한 쿠키 이름을 사용할 수 있습니다.
* 불필요한 리디렉션을 제거합니다. 뷰스루 데이터는 실시간으로 수집되므로 Adobe 수집 서버 및 DFA에서 모든 페이지 보기의 데이터를 잠재적으로 교환할 수 있습니다. 플러그인은 정보가 필요하지 않은 경우 이러한 데이터 교환을 차단합니다.

>[!CAUTION]
>
>불필요한 DFA 쿼리를 제거하기 위해 플러그인이 사용하는 메커니즘 중 하나는 도메인 기반 방문 쿠키입니다. 여러 도메인을 포괄하는 통합 보고서 세트는 방문자가 DFA의 영향을 받는 뷰스루 또는 클릭스루 이후 도메인을 교차하면 클릭스루 및 뷰스루 데이터를 늘립니다.

