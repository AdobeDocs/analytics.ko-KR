---
title: 전체 처리 데이터 소스의 서비스 종료
description: 전체 처리 데이터 소스의 서비스 종료 공지에 대해 자세히 알아보십시오.
exl-id: 7dd6d518-156f-4bf5-86cb-04d0acc8ff0c
feature: Data Sources
role: Admin
TQID: 'https://experienceleague.adobe.com/3NSbjRWl0GsomjsEXo8XczQ1RWOPGpqW4OM2YeUo3Wk'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: f46a60da-b0b2-4ca3-bd91-271173f4123d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 415
ht-degree: 8%

---

# 전체 처리 데이터 소스의 서비스 종료

전체 처리 데이터 소스는 지금까지 조직에서 히트 수준 데이터를 Adobe Analytics에 제출할 수 있도록 해 주었습니다. 이 데이터는 AppMeasurement과 같은 전통적인 데이터 수집 수단을 통해 수집된 데이터와 동일한 방식으로 처리되었다. 2020년 Adobe은 전체 처리 데이터 소스와 동일한 기능을 수행하지만 추가 기능이 포함된 [Bulk data insertion API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/)를 출시했습니다. 이 페이지에서는 Bulk data insertion API에서 제공하는 추가 기능에 대한 세부 정보를 제공하며 파일 형식의 차이점을 간략하게 설명합니다.

2021년 3월 25일, Adobe에서 새로운 전체 처리 데이터 소스 연결이 생성되지 않았습니다. 2022년 1월 31일에 모든 전체 처리 데이터 서비스가 비활성화되었습니다.

## 전체 처리 데이터 소스와 Bulk data insertion API 간의 주요 차이점

* Bulk data insertion을 사용하면 병렬 처리를 위해 여러 파일을 제출할 수 있습니다. 방문자 그룹은 방문자 연속성과 eVar 속성을 보장합니다.
* Bulk Data Insertion에는 데이터 유효성 검사 및 오류 처리 기능이 있으므로 히트 데이터를 제출하는 관리 작업의 일부를 생략할 수 있습니다.
* 대량 데이터 삽입은 여러 방문자 ID 식별 방법을 지원합니다.
* 대량 데이터 삽입에는 방문자 식별 열, `pageName`(또는 이에 상응하는 링크), `reportSuiteID`, `timestamp` 및 `userAgent`과(와) 같은 일부 추가 필수 필드가 있습니다.
* 방문자 연속성과 속성을 보장하기 위해 Bulk data insertion은 파일 내의 행을 시간순으로 정렬합니다. 파일 간 방문자 활동 순서에 대해 알아보려면 [방문자 그룹](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/visitor-groups/)을 참조하십시오.
* 대량 데이터 삽입을 사용하려면 파일이 .gzip 형식으로 .csv 압축되어야 합니다.
* BDIA는 `date` 대신 `timestamp`을(를) 사용합니다.

## BDIA와 전체 처리 데이터 소스 간의 변수 비교

다음 변수가 Bulk data insertion에 도입되었는데, 이전에는 전체 처리 데이터 소스에서 사용할 수 없었습니다.

* **`aamlh`**: Adobe Audience Manager 위치 힌트입니다.
* **`contextData.key`**: [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md).
* **`customerID`**: Experience Cloud ID 서비스 변수. `id`, `authState`및 `isMCSeed`를 포함합니다.
* **`hints`**: [클라이언트 힌트](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html) 변수. `bitness`, `brands`, `mobile`, `model`, `platform`, `platformversion` 및 `wow64`을(를) 포함합니다.
* **`ipaddress`**: [IP 주소](/help/components/dimensions/ip-address.md) 차원.
* **`language`**: [언어](/help/components/dimensions/language.md) 차원.
* **`list1`** - **`list3`**: [목록 변수](/help/implement/vars/page-vars/list.md).
* **`marketingCloudVisitorID`**: 방문자의 Experience Cloud ID.
* **`tnta`**: [Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 통합에 사용되는 Target 데이터 페이로드입니다.
* **`trackingServer`**: [`trackingServer`](/help/implement/vars/config-vars/configuration-variables.md) 변수입니다.
* **`transactionID`**: [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 변수입니다.
* **`userAgent`**: 장치의 사용자 에이전트 문자열입니다.

다음 변수는 대량 데이터 삽입을 통해 지원되지 않습니다.

* **`charSet`**: [`charSet`](/help/implement/vars/config-vars/charset.md) 변수입니다. 대량 데이터 삽입은 UTF-8만 지원합니다.
* **`timezone`**: 방문자의 표준 시간대 오프셋(시간 단위)입니다.
* **`clickAction`**, **`clickActionType`**, **`clickContext`**, **`clickContextType`**, **`clickSourceID`**, **`clickTag`**: Activity Map 데이터 수집에 사용되는 변수입니다.
