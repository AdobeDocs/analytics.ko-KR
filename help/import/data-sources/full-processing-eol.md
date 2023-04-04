---
title: 전체 처리 데이터 소스에 대한 수명 종료
description: 전체 처리 데이터 소스에 대한 수명 종료 발표에 대해 자세히 알아보십시오.
source-git-commit: bb3036380eeec9b7a868f60a4c9076f2b772532b
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 15%

---

# 전체 처리 데이터 소스에 대한 수명 종료

전체 처리 데이터 소스를 통해 조직에서 이전에 Adobe Analytics에 히트 수준 데이터를 제출할 수 있었습니다. 이 데이터는 AppMeasurement와 같은 기존 데이터 수집 수단을 통해 수집된 데이터와 동일한 방식으로 처리되었습니다. 2020년에 Adobe은 [대량 데이터 삽입 API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/)는 전체 처리 데이터 소스와 동일한 기능을 수행하지만 추가 기능을 사용하여 수행합니다. 이 페이지에서는 대량 데이터 삽입 API에서 제공하는 추가 기능에 대한 세부 정보를 제공하며 파일 형식의 차이점을 간략하게 설명합니다.

2021년 3월 25일에 Adobe에서 새로운 전체 처리 데이터 소스 연결이 생성되지 않았습니다. 2022년 1월 31일에 모든 전체 처리 데이터 서비스가 비활성화되었습니다.

## 전체 처리 데이터 소스와 벌크 데이터 삽입 API 간의 주요 차이점

* 대량 데이터 삽입을 사용하면 병렬 처리를 위해 여러 파일을 제출할 수 있습니다. 방문자 그룹을 사용하면 방문자 지속성과 eVar 속성이 보장됩니다.
* 벌크 데이터 삽입에는 데이터 유효성 검사 및 오류 처리 기능이 있어서 히트 데이터 제출이라는 일부 관리 작업이 제거됩니다.
* 대량 데이터 삽입은 여러 방문자 ID 식별 방법을 지원합니다.
* 대량 데이터 삽입에는 몇 가지 추가 필수 필드가 있습니다. 방문자 식별 열, `pageName` (또는 이에 상응하는 링크), `reportSuiteID`, `timestamp`, 및 `userAgent`.
* 방문자 연속성 및 속성을 보장하기 위해 벌크 데이터 삽입에는 파일 내의 행을 시간 순서대로 정렬해야 합니다. 파일 간 방문자 활동 순서에 대해 알아보려면 [방문자 그룹](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/visitor-groups/)을 참조하십시오.
* 대량 데이터 삽입을 위해서는 파일을 .gzip 형식으로 압축해야 합니다.
* BDIA 사용 `timestamp` 대신 `date`.

## BDIA와 전체 처리 데이터 소스 간의 변수 비교

다음 변수는 이전에 전체 처리 데이터 소스에서 사용할 수 없었던 대량 데이터 삽입에 도입되었습니다.

* **`aamlh`**: Adobe Audience Manager 위치 힌트.
* **`contextData.key`**: [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md).
* **`customerID`**: Experience Cloud ID 서비스 변수. `id`, `authState`및 `isMCSeed`를 포함합니다.
* **`hints`**: [클라이언트 힌트](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html?lang=ko-KR) 변수를 채우는 방법을 설명합니다. 포함 `bitness`, `brands`, `mobile`, `model`, `platform`, `platformversion`, 및 `wow64`.
* **`ipaddress`**: 방문자의 IP 주소입니다.
* **`language`**: 다음 [언어](/help/components/dimensions/language.md) 차원.
* **`list1`** - **`list3`**: [목록 변수](/help/implement/vars/page-vars/list.md).
* **`marketingCloudVisitorID`**: 방문자의 Experience Cloud ID.
* **`tnta`**: 에 사용된 Target 데이터 페이로드 [Target 분석](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 통합.
* **`trackingServer`**: .[`trackingServer`](/help/implement/vars/config-vars/trackingserver.md)
* **`transactionID`**: .[`transactionID`](/help/implement/vars/page-vars/transactionid.md)
* **`userAgent`**: 장치의 사용자 에이전트 문자열입니다.

다음 변수는 대량 데이터 삽입을 통해 지원되지 않습니다.

* **`charSet`**: . [`charSet`](/help/implement/vars/config-vars/charset.md) 대량 데이터 삽입은 UTF-8만 지원합니다.
* **`timezone`**: 방문자의 시간대가 GMT에서 시간 단위로 오프셋됩니다.
* **`clickAction`**, **`clickActionType`**, **`clickContext`**, **`clickContextType`**, **`clickSourceID`**, **`clickTag`**: Activity Map 데이터 수집에 사용되는 변수입니다.
