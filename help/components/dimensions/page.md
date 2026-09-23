---
title: 페이지
description: 페이지 이름.
feature: Dimensions
exl-id: 579963c8-8460-425f-b716-3b30d7a259af
TQID: https://experienceleague.adobe.com/npKfFB-zOPzNGJJ6YZvtz0oA3NDWuQiHYBraH09lc58
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
    internal-label: Attribution
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
source-wordcount: '226'
ht-degree: 54%
---
# 페이지

&#39;페이지&#39; [차원](overview.md)은(는) 사이트의 페이지 이름을 나열합니다. 사이트의 어느 페이지가 가장 성과가 좋은지 알 수 있도록 해주므로, Adobe Analytics에서 사용되는 가장 일반적인 차원 중 하나입니다.

이 차원은 [사이트 섹션](site-section.md) 및 [서버](server.md) 차원과 관련되어 있습니다. 페이지는 가장 세분화된 차원이고, 서버는 가장 덜 세분화된 차원이며, 사이트 섹션은 그 둘의 사이에 있습니다.

## 이 차원을 데이터로 채우기

[페이지 보기 호출(`t()`)](/help/implement/vars/functions/t-method.md)에서 [`pageName`](/help/implement/vars/page-vars/pagename.md) 변수를 설정합니다. `pageName` 변수가 설정되지 않은 경우 이 차원은 [`pageURL`](/help/implement/vars/page-vars/pageurl.md) 변수를 사용하는 것으로 돌아갑니다. [링크 추적 호출(`tl()`)](/help/implement/vars/functions/tl-method.md)은(는) `pageName` 값이 있는 경우에도 항상 이 차원을 제거합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`pageName`](/help/implement/vars/page-vars/pagename.md) |
| **웹 SDK/XDM 필드** | [`web.webPageDetails.name`](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/data-types/webpage-details) |
| **쿼리 매개 변수** | [`pageName`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<pageName>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 100바이트 |
| **지속성** | 히트 |

## 차원 항목

차원 항목에는 사이트의 페이지 이름이 포함됩니다. 조직은 사용자가 사용하려는 특정 차원 항목을 결정합니다. 일부 조직에서는 `document.title`을 바로 사용하는 반면, 다른 조직에서는 사용자 지정 탐색 표시를 만듭니다. 어떤 방법을 사용하든 일관된 방법을 사용하고 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 기록하도록 하십시오.

>[!NOTE]
>
>Analysis Workspace는 기본적으로 마지막 기여도를 사용하며, 모든 기여도 모델을 사용할 수도 있습니다.
