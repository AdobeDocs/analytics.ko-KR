---
title: 전체 처리 데이터 소스의 수명 종료
description: 벌크 데이터 삽입 API와 전체 처리 데이터 소스 간의 비교 및 실행이 종료되는 이유.
translation-type: tm+mt
source-git-commit: 97e60e4c3a593405f92f47e5aa79ece70e0b3d60
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 31%

---


# 전체 처리 데이터 소스의 수명 종료

몇 년 동안 전체 처리 데이터 소스를 통해 히트 수준 데이터를 Adobe Analytics에 제출할 수 있습니다. 이 데이터는 JavaScript 라이브러리 및 모바일 앱 SDK를 통해 수집한 데이터와 같은 방식으로 처리되었습니다. 2020년, Adobe은 전체 처리 데이터 소스와 동일한 기능을 하지만 추가 기능을 제공하는 [벌크 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)를 출시했습니다. 이 항목에서는 벌크 데이터 삽입 API에서 제공하는 추가 기능에 대한 세부 사항을 제공하며 파일 형식 차이에 대한 개요를 설명합니다.

2021년 3월 25일부터 Adobe은 새로운 전체 처리 데이터 소스 연결을 만들지 못하게 됩니다. 기존 연결은 서비스를 완전히 사용하지 않을 때까지 계속 지원됩니다. 세부 사용 날짜는 아직 결정되지 않았지만 2021년에 있을 것이다.

## 이 기능을 종료하는 이유는 무엇입니까?

BDIA(Bulk Data Insertion API)는 전체 처리에서 지원되는 모든 사용 사례에 대해 추가 기능을 제공합니다. 대량 데이터 삽입 API를 사용하면 보다 향상된 기능을 경험할 수 있습니다.

## 전체 처리 데이터 소스와 벌크 데이터 삽입 API의 주요 차이점

* 벌크 데이터 삽입을 통해 여러 파일을 동시에 처리할 수 있습니다. 방문자 그룹을 사용하여 방문자 연속성 및 eVar 속성을 보장할 수 있습니다.
* 벌크 데이터 삽입에는 데이터 유효성 검사와 오류 처리 기능이 있으므로 히트 데이터를 제출하는 관리 작업 중 일부를 제거합니다.
* 벌크 데이터 삽입은 방문자 ID에 대한 여러 옵션을 지원합니다. 분석 ID와 Marketing Cloud ID를 모두 제출할 수 있습니다(자세한 내용은 [ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html) 참조). 또한 자신의 ID를 ECID](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#customer-id-and-experience-cloud-visitor-id-seeds)를 생성하기 위해 [시드로 사용할 수 있습니다.
* 벌크 데이터 삽입은 목록 및 컨텍스트 데이터 변수를 지원합니다.
* 벌크 데이터 삽입은 Activity Map 데이터를 지원하지 않습니다.

## 파일 형식 및 내용의 주요 차이점

* 벌크 데이터 삽입에는 몇 가지 추가 필수 필드가 있습니다. 자세한 내용은 [설명서](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)를 참조하십시오.
* 방문자의 연속성 및 속성을 보장하기 위해 벌크 데이터 삽입은 파일 내의 행을 시간순으로 정렬해야 합니다. 파일 간의 방문자 활동 순서에 대해 알려면 [방문자 그룹](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md#visitor-groups)을 참조하십시오.
* 벌크 데이터 삽입에는 .gzip 형식으로 압축되는 .csv 파일이 필요합니다.
* BDIA는 &quot;date&quot; 대신 &quot;timestamp&quot;를 사용합니다.

자세한 내용은 대량 데이터 삽입(BDIA) 및 전체 처리 데이터 소스(FPDS)에서 사용할 수 있는 필드 값 비교를 참조하십시오.

## BDIA 및 FPDS에서 사용할 수 있는 필드 값 비교

| 미디어 변수 | 전체 처리 열 변수 | 설명 |
| --- | --- | --- |
| aamlh | 지원되지 않음 | Adobe Audience Manager 위치 힌트. |
| browserHeight | browserHeight | 브라우저 높이, 픽셀 단위(예: 768) |
| browserWidth | browserWidth | 브라우저 너비, 픽셀 단위(예: 1024) |
| campaign | campaign | 전환 캠페인 추적 코드 |
| channel | channel | 채널 문자열(예: 스포츠 섹션) |
| colorDepth | colorDepth | 모니터 색상 깊이, 비트 단위(예: 24) |
| connectionType | connectionType | 방문자의 연결 유형(LAN 또는 모뎀) |
| contextData.key | 지원되지 않음 | 키-값 쌍은 헤더 &quot;contextData.product&quot; 또는 &quot;contextData.color&quot;의 이름을 지정하여 지정합니다. |
| cookiesEnabled | cookiesEnabled | `Y` 또는 방문자가 자사 세션 쿠키를 지원하는  `N` 경우 |
| currencyCode | currencyCode | 매출 통화 코드(예: `USD`) |
| customerID.[customerIDType].authState | 지원되지 않음 | 방문자의 인증된 상태입니다. 지원되는 값은 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT 또는 &quot;(대/소문자 구분 안 함)입니다. 연속해서 두 개의 작은 따옴표(&quot;)는 쿼리 문자열에서 값을 생략하여 히트가 만들어질 때 0으로 해석합니다. 지원되는 authState 숫자 값은 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT을 나타냅니다. customerIDType은 임의의 영숫자 문자열일 수 있지만 대/소문자를 구분하도록 간주해야 합니다. |
| customerID.[customerIDType].id | 지원되지 않음 | 사용할 고객 ID. customerIDType은 임의의 영숫자 문자열일 수 있지만 대/소문자를 구분하도록 간주해야 합니다. |
| customerID.[customerIDType].isMCSeed | 지원되지 않음 | Marketing Cloud 방문자 ID의 초기값인지 여부. 지원되는 값은 0, 1, TRUE, FALSE, &quot;(대/소문자 구분 안 함)입니다. 0, FALSE 또는 연속된 단일 따옴표(&quot;)를 사용하면 쿼리 문자열에서 값이 생략됩니다. customerIDType은 임의의 영숫자 문자열일 수 있지만 대/소문자를 구분하도록 간주해야 합니다. |
| eVarN | eVarN, 즉`<eVar2>`...`<eVar>` | 전환 eVar 이름. 최대 75개의 eVar를 가질 수 있습니다( eVar1 - eVar75 ) eVar 이름(eVar12) 또는 친숙한 이름(광고 캠페인 3)을 지정할 수 있습니다. |
| events | events | [s.events 변수와 동일한 구문을 사용하여 형식이 지정된 이벤트 문자열](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=en#vars). 예:scAdd,event1,event7 |
| hierN | hierN, 즉`<hier2>`..`</hier2>` | 계층 이름. 최대 5개의 계층을 가질 수 있습니다( hier1 - hier5 ). 기본 계층 이름 `hier2` 또는 친숙한 이름(Yankees)을 지정할 수 있습니다. |
| homePage | homePage | Y 또는 N -- 현재 페이지가 방문자의 홈 페이지인지 여부. |
| ipaddress | 지원되지 않음 | 방문자의 IP 주소입니다. |
| javaEnabled | javaEnabled | Y 또는 N -- 방문자의 Java 활성화 여부. |
| javaScriptVersion | javaScriptVersion | JavaScript 버전(예: 1.3). |
| language | 지원되지 않음 | 브라우저에서 지원되는 언어입니다. (예: `en-us`) |
| linkName | linkName | 링크 이름. |
| linkType | linkType | 링크 유형. 지원되는 값은 다음과 같습니다. `d: Download link`, `e: Exit link`, `o: Custom link`. |
| linkURL | linkURL | 링크의 HREF. |
| listn 예: list2. | 지원되지 않음 | 변수로 전달된 후 보고를 위해 개별 라인 항목으로 보고되는 구분 기호로 구분된 값의 목록입니다. |
| marketingCloudVisitorID | 지원되지 않음 | Marketing Cloud ID. [방문자 식별](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en#id-service-api) 및 Marketing Cloud 방문자 ID 서비스를 참조하십시오. |
| 지원되지 않음 | charSet | 웹 사이트에 지원되는 문자 집합입니다. 예를 들어 UTF-8, ISO-8859-1 등입니다.  |
| 지원되지 않음 | clickAction | 방문자 클릭 맵에 대한 개체 식별자(oid) |
| 지원되지 않음 | clickActionType | 방문자 클릭 맵에 대한 개체 식별자 유형(oidt) |
| 지원되지 않음 | clickContext | 방문자 클릭 맵에 대한 페이지 식별자(pid) |
| 지원되지 않음 | clickContextType | 방문자 클릭 맵에 대한 페이지 식별자 유형(pidt) |
| 지원되지 않음 | clickSourceID | 방문자 클릭 맵에 대한 소스 색인(oi) |
| 지원되지 않음 | clickTag | 방문자 클릭 맵에 대한 개체 태그 이름(ot) |
| 지원되지 않음 | scXmlVer | 마케팅 보고서 XML 요청 버전 번호(예: 1.0). |
| 지원되지 않음 | timezone | 방문자의 시간대와 GMT의 시차, 시간 단위(예: -8). |
| pageName | pageName | 페이지의 이름입니다. |
| pageType | pageType | 페이지 유형(예: &quot;오류 페이지&quot;). |
| pageUrl | pageUrl | 페이지 URL(예: https://www.example.com/index.html). |
| plugins | plugins | 세미콜론으로 구분된 브라우저 플러그인 이름 목록. |
| products | products | 페이지의 모든 제품 목록. 쉼표로 제품을 구분합니다. 예:스포츠;볼;1;5.95,장난감;위쪽;1:1.99. |
| prop1 - prop75 | propN, 즉`<prop2>`..`</prop2>` | 속성 번호 문자열(예: 스포츠 섹션). |
| propN | propN | 속성에 대한 속성 값. |
| purchaseID | purchaseID | 구매 ID 번호. |
| referrer | referrer | 페이지 레퍼러의 URL. |
| reportSuiteID | s_account | 데이터 제출을 원하는 보고서 세트를 지정합니다. 여러 보고서 세트 ID를 쉼표로 구분해야 합니다. |
| resolution | resolution | 모니터 해상도(예: 1024x768). |
| server | server | 서버 문자열. |
| state | state | 전환 상태 문자열. |
| timestamp | 날짜 | YYYY-MM-DDThh:mm:ss UTC_offset(예: 2021-09-01T12:00:00-07:00) 또는 Unix 시간 형식(1970년 1월 1일 이후 경과한 초)의 ISO 8601 날짜 형식을 사용합니다. |
| trackingServer | 지원되지 않음 | 열 헤더를 통해서만 제공할 수 있습니다. |
| transactionID | 지원되지 않음 | 보고 목적으로 다중 채널 사용자 활동을 연결하는 데 사용되는 공통된 값입니다. 자세한 내용은 [Data Sources 사용자 안내서](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html?lang=en#data-sources)를 참조하십시오. |
| userAgent | 지원되지 않음 | 사용자 에이전트 문자열 |
| visitorID | visitorID | 방문자의 분석 ID. [방문자 식별](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)을 참조하십시오. |
| zip | zip | 전환 우편번호. |
