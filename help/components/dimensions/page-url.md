---
title: 페이지 URL
description: 페이지의 URL입니다.
feature: Dimensions
exl-id: 7c0ec494-d79b-4b65-9161-bdc48485af84
TQID: https://experienceleague.adobe.com/Qek7BUR15HjFpK-XaYQ-J9fkJQiBfNi-ZoqXqaACP0A
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 52%
---
# 페이지 URL

&#39;페이지 URL&#39; [차원](overview.md)은(는) 사이트의 URL을 나열합니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다. 다른 Analytics 솔루션에서 URL 차원을 사용하려면 모든 히트에서 값을 [eVar](evar.md)에 복사하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

AppMeasurement은 각 [페이지 보기 호출(`t()`)](/help/implement/vars/functions/t-method.md)에서 페이지 URL을 자동으로 수집합니다. [`pageURL`](/help/implement/vars/page-vars/pageurl.md) 변수를 사용하여 수집된 값을 재정의할 수 있습니다. URL이 255바이트보다 긴 경우 오버플로는 `-g` 쿼리 문자열 매개 변수에 저장됩니다. URL의 프로토콜 및 쿼리 문자열이 포함됩니다. [링크 추적 호출(`tl()`)](/help/implement/vars/functions/tl-method.md)은(는) URL 값이 있어도 항상 이 차원을 제거합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`pageURL`](/help/implement/vars/page-vars/pageurl.md) |
| **웹 SDK/XDM 필드** | [`web.webPageDetails.URL`](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/data-types/webpage-details) |
| **쿼리 매개 변수** | [`g`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<pageUrl>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 255바이트(오버플로가 있는 고정 제한 없음) |
| **지속성** | 히트 |

## eVar를 URL로 채우기

연결된 문자열 `window.location.hostname + window.location.pathname`으로 eVar를 설정하는 것이 좋습니다. 이 문자열은 일반적으로 프로토콜, 쿼리 문자열 및 앵커 태그를 생략하므로 `window.location.href`보다 잘 작동합니다.

eVar가 Data Warehouse의 “페이지 URL” 차원과 정확히 일치하도록 하려면 [동적 변수](/help/implement/vars/page-vars/dynamic-variables.md)를 사용하고 각 히트에서 eVar를 `D=g`로 설정할 수 있습니다.

## 차원 항목

차원 항목에는 사이트의 페이지 URL이 포함됩니다.
