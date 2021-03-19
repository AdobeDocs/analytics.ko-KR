---
title: null
description: null
translation-type: tm+mt
source-git-commit: 537b41ee45cfa21bdf2e282fabc43a17fd90e327
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 13%

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

| BDIA, FPDS, 모두 | 미디어 변수 | 전체 처리 열 변수 | 설명 |
| --- | --- | --- | --- |
| BDIA | aamlh | 지원되지 않음 | Adobe Audience Manager 위치 힌트. 아래 AAM 지역 목록 표에서 유효한 ID 값을 참조하십시오. |
| 변수 | browserHeight | browserHeight | 브라우저 높이, 픽셀 단위(예: 768) |
| 변수 | browserWidth | browserWidth | 브라우저 너비, 픽셀 단위(예: 1024) |
| 변수 | campaign | campaign | 전환 캠페인 추적 코드 |
| 변수 | channel | channel | 채널 문자열(예: 스포츠 섹션) |
| 변수 | colorDepth | colorDepth | 모니터 색상 깊이, 비트 단위(예: 24) |
| 변수 | connectionType | connectionType | 방문자의 연결 유형(LAN 또는 모뎀) |
| BDIA | contextData.key | 지원되지 않음 | 키-값 쌍은 헤더 &quot;contextData.product&quot; 또는 &quot;contextData.color&quot;의 이름을 지정하여 지정합니다. |
| 변수 | cookiesEnabled | cookiesEnabled | `Y` 또는 방문자가 자사 세션 쿠키를 지원하는  `N` 경우 |
| 변수 | currencyCode | currencyCode | 매출 통화 코드(예: `USD`) |
| BDIA | customerID.[customerIDType].authState | 지원되지 않음 | 방문자의 인증된 상태입니다. 지원되는 값은 0, 1, 2, UNKNOWN, AUTHENTICATED, LOGGED_OUT 또는 &quot;(대/소문자 구분 안 함)입니다. 연속해서 두 개의 작은 따옴표(&quot;)는 쿼리 문자열에서 값을 생략하여 히트가 만들어질 때 0으로 해석합니다. 지원되는 authState 숫자 값은 0 = UNKNOWN, 1 = AUTHENTICATED, 2 = LOGGED_OUT을 나타냅니다. customerIDType은 임의의 영숫자 문자열일 수 있지만 대/소문자를 구분하도록 간주해야 합니다. |
| BDIA | customerID.[customerIDType].id | 지원되지 않음 | 사용할 고객 ID. customerIDType은 임의의 영숫자 문자열일 수 있지만 대/소문자를 구분하도록 간주해야 합니다. |
| BDIA | customerID.[customerIDType].isMCSeed | 지원되지 않음 | Marketing Cloud 방문자 ID의 초기값인지 여부. 지원되는 값은 0, 1, TRUE, FALSE, &quot;(대/소문자 구분 안 함)입니다. 0, FALSE 또는 연속된 단일 따옴표(&quot;)를 사용하면 쿼리 문자열에서 값이 생략됩니다. customerIDType은 임의의 영숫자 문자열일 수 있지만 대/소문자를 구분하도록 간주해야 합니다. |
