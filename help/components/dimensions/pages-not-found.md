---
title: 페이지를 찾을 수 없음(차원)
description: 사이트에서 오류를 반환하는 URL입니다.
feature: Dimensions
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
TQID: https://experienceleague.adobe.com/0S2WzNRJrtOa9ZPTg5cmbwxMLJE5tI6Qa3GtZs6GqKc
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
source-wordcount: '276'
ht-degree: 50%
---
# 페이지를 찾을 수 없음

>[!BEGINSHADEBOX]

*이 도움말 페이지에서는 &#39;페이지를 찾을 수 없음&#39;이 [차원](overview.md)(으)로 작동하는 방식을 설명합니다. 지표로 작동하는 방식에 대한 자세한 내용은 [페이지를 찾을 수 없음](../metrics/pages-not-found.md) 지표 페이지를 참조하십시오.*

>[!ENDSHADEBOX]

&quot;페이지를 찾을 수 없음&quot; 차원은 오류가 포함된 URL을 보여 줍니다. 이 차원은 방문자가 사이트에서 받는 오류의 수를 줄이려는 경우에 유용합니다.

* [흐름 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)에서 이 차원을 사용하여 방문자가 어느 페이지를 클릭스루하여 오류에 도달하는지 확인할 수 있습니다. 확인이 되면 조직의 개발 팀과 협력하여 각 페이지에서 링크를 수정할 수 있습니다.
* [레퍼러](referrer.md) 차원과 함께 이 차원을 사용하면 방문자가 외부 링크에서 사이트에 도착하는 위치를 확인할 수 있습니다. 그런 다음 원하는 위치로의 리디렉션을 구현하거나, 서드파티와 협력하여 링크를 수정할 수 있습니다.

>[!NOTE]
>
>Data Warehouse에서 이 차원의 이름은 &#39;[!UICONTROL 페이지 유형 오류]&#39;입니다.

## 이 차원을 데이터로 채우기

AppMeasurement는 [`pageType`](/help/implement/vars/page-vars/pagetype.md) 변수를 사용하여 이 데이터를 수집합니다. `pageType`이(가) `errorPage`(으)로 설정되면 히트의 페이지 URL이 차원 항목으로 기록됩니다. `pageType` 변수가 정의되지 않았거나 다른 값으로 설정되어 있으면 이 차원에 대한 데이터가 수집되지 않습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`pageType`](/help/implement/vars/page-vars/pagetype.md) |
| **웹 SDK/XDM 필드** | [`web.webPageDetails.isErrorPage`](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/data-types/webpage-details) |
| **쿼리 매개 변수** | [`pageType`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<pageType>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 해당 없음 |
| **지속성** | 히트 |

## 차원 항목

차원 항목에는 오류가 발생한 사이트의 페이지 URL이 포함됩니다.
