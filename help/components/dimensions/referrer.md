---
title: 리퍼러
description: 방문자가 사이트로 연결되는 링크를 클릭하기 전에 있었던 URL입니다.
feature: Dimensions
exl-id: 146f0327-c73c-40f5-8cc1-584e31d163a2
TQID: https://experienceleague.adobe.com/VE1bJD2ah1N9t-fHKc5GC0-pC4YmXEDkCwhVmI5rHZQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 76%
---
# 리퍼러

&#39;레퍼러&#39; [차원](overview.md)은(는) 방문자가 사이트에 도달하기 위해 클릭스루할 때 있었던 URL을 보고합니다. 이 차원은 사이트로 들어오는 트래픽이 가장 많은 특정 URL을 이해하는 데 유용합니다. 링크는 외부 URL에 있어야 하며, 방문자가 링크를 클릭하여 차원 항목을 표시해야 합니다.

>[!IMPORTANT]
>
>이 차원을 사용하려면 보고서 세트의 [내부 URL 필터](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 URL이 포함되거나 외부 URL이 표시되지 않을 수 있습니다.

동일한 보고서가 Analysis Workspace와 Data Warehouse 간에 다른 결과를 보여 줄 수 있습니다. Analysis Workspace는 내부 URL 필터와 일치하는 값을 제외하고 각 개별 페이지에 대한 레퍼러를 보고합니다. Data Warehouse는 방문의 첫 번째 레퍼러만 보고하고 내부 URL 필터는 무시합니다.

## 이 차원을 데이터로 채우기

AppMeasurement은 브라우저의 `document.referrer` 값에서 레퍼러를 자동으로 수집합니다. [`referrer`](/help/implement/vars/page-vars/referrer.md) 변수를 사용하여 수집된 값을 재정의할 수 있습니다. 보고서 세트의 [내부 URL 필터](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)도 구성해야 합니다. 구성하지 않으면 내부 URL이 포함되거나 외부 URL이 표시되지 않을 수 있습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`referrer`](/help/implement/vars/page-vars/referrer.md) |
| **웹 SDK/XDM 필드** | [`web.webReferrer.URL`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/data-types/web-information) |
| **쿼리 매개 변수** | [`r`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<referrer>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 255바이트 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 방문자가 사이트를 클릭스루하는 URL이 포함됩니다. 히트에 레퍼러 데이터가 없으면 이 히트는 차원 항목 `"Typed/Bookmarked"` 아래에 그룹화됩니다. 이 차원 항목은 방문자가 수동으로 브라우저 주소를 주소 표시줄에 입력하거나 책갈피를 클릭하는 등의 경우와 같이 레퍼러 값이 없음을 의미합니다. Analytics를 수용하지 않는 리디렉션에 대해서도 `"Typed/Bookmarked"` 차원 항목이 나타납니다. 기술 정보 사용 안내서에서 [리디렉션 및 별칭](/help/technotes/redirects.md)을 참조하십시오.

### `googleusercontent.com`을 포함하는 차원 항목

사용자는 도메인 `googleusercontent.com`이 있는 차원 항목을 볼 수 있습니다.

* **캐시된 페이지**: Google의 스파이더는 오프라인 상태가 될 경우에 대비해 끊임없이 웹을 크롤링하고 페이지 사본을 저장합니다. 이러한 캐시된 페이지는 &quot;캐시됨&quot; 링크를 클릭하여 대부분의 검색 결과 옆에서 사용할 수 있습니다. 사용자가 이 링크를 클릭하고 Google에서 캐시한 콘텐츠를 볼 때에는 `webcache.googleusercontent.com`이 일반적인 차원 항목입니다.
* **번역된 페이지**: Google은 강력하고 편리한 번역 서비스를 제공합니다. 이 서비스를 사용하여 사이트를 보는 경우 `translate.googleusercontent.com`에서 사이트가 전송됩니다. 이 차원 항목은 사용자가 링크를 클릭하여 원래 콘텐츠로 돌아가는 경우 나타납니다.
