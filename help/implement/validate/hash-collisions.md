---
title: 해시 충돌
description: 해시 충돌의 정의와 해시 충돌이 어떻게 발현될 수 있는지에 대해 설명합니다.
feature: Implementation Basics
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/yjYX-h-8jJA7k-jzRMOJ0l2BxN5-no2kCfySkGYss8w'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2: id: e992d880-33bc-4949-a648-aa7d410276cd
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 539
ht-degree: 5%

---

# 해시 충돌

Adobe Analytics의 차원은 문자열 값을 수집합니다. 때로는 이러한 문자열의 길이가 수백 자인 반면 때로는 짧습니다. 성능을 향상시키기 위해 이 문자열 값은 보고서 처리 시간에 직접 사용되지 않습니다. 대신 각 값에 대해 해시가 계산되어 균일 크기의 식별자를 생성합니다. 대부분의 필드의 경우 해시 전에 값이 소문자로 변환되므로 총 고유 값 수가 줄어듭니다. 모든 보고서는 이러한 해시된 값에서 실행되므로 성능이 크게 향상됩니다.

Adobe Analytics은 각 변수에 대해 별도의 해시 테이블을 유지 관리하며 각 테이블은 매월 다시 작성됩니다. 이러한 테이블 중 하나에서 서로 다른 두 소스 값이 가끔 동일한 해시를 생성할 수 있습니다. 이를 *해시 충돌*&#x200B;이라고 합니다.

해시 충돌은 다음과 같이 보고서에서 나타날 수 있습니다.

* 시간이 지남에 따라 보고서를 보고 예상치 못한 스파이크가 표시되면 해당 변수에 대한 여러 고유 값이 동일한 해시를 사용할 수 있습니다.
* 세그먼트를 사용하고 예기치 않은 값이 표시되면 예기치 않은 차원 항목이 세그먼트와 일치하는 다른 차원 항목과 동일한 해시를 사용할 수 있습니다.

## 해시 충돌 가능성

Adobe Analytics은 대부분의 차원에 32비트 해시를 사용하므로 가능한 해시 조합이 2<sup>32</sup>개(약 43억)입니다. 고유 값의 수에 따라 해시 충돌이 발생할 대략적인 확률은 다음과 같다. 이러한 승산은 단일 달의 단일 차원을 기반으로 합니다.

| 고유 값 | 확률 |
| --- | --- |
| 1,000 | 0.01% |
| 10,000 | 1% |
| 50,000 | 26% |
| 100,000 | 71% |

[생일 역설](https://en.wikipedia.org/wiki/Birthday_problem)과 마찬가지로 고유한 값의 수가 증가하면 해시 충돌 가능성이 크게 증가합니다. 100만 개의 고유 값에서 해당 차원에 대해 최소 100개의 해시 충돌이 있을 수 있습니다.

## 해시 충돌 완화

해시 충돌을 완전히 제거할 수는 없지만 보고서에 미치는 영향을 완화할 수 있습니다. 대부분의 해시 충돌은 두 개의 흔하지 않은 값에서 발생하며, 이는 보고서에 의미 있는 영향을 미치지 않습니다. 해시가 공통적이고 흔하지 않은 값과 충돌하더라도 결과는 무시해도 된다. 그러나 두 개의 인기 있는 값이 해시 충돌을 경험하는 드문 경우, 그 효과를 명확하게 볼 수 있습니다. Adobe은 보고서에서 그 효과를 줄이려면 다음을 권장합니다.

* **날짜 범위를 변경합니다**: 해시 테이블이 매월 변경됩니다. 날짜 범위를 다른 달에 걸쳐 변경하면 각 값에 충돌하지 않는 서로 다른 해시가 제공될 수 있습니다. 일반적으로 특정 보고서에서 표시되는 예외 항목을 지우는 가장 빠른 방법입니다.
* **고유 값의 수를 줄입니다**: 구현을 조정하거나 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)을 사용하여 차원에서 수집하는 고유 값의 수를 줄일 수 있습니다. 예를 들어 차원에서 URL을 수집하는 경우 쿼리 문자열 또는 프로토콜을 제거할 수 있습니다.
* **[Data Warehouse](/help/export/data-warehouse/data-warehouse.md) 또는 [데이터 피드 사용](/help/export/analytics-data-feed/data-feed-overview.md)**: 이 도구는 해시 테이블에 의존하지 않습니다.
* **[Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=ko-KR)**(으)로 이동: Customer Journey Analytics에는 해시 레이어가 없으며 [차원에 대한 카디널리티 제한 없음](https://experienceleague.adobe.com/docs/analytics-platform/using/components/dimensions/high-cardinality.html). 해시 충돌 또는 [[!UICONTROL 낮은 트래픽]](/help/technotes/low-traffic.md)이 보고서에 자주 영향을 주는 경우 이 제품으로 이동하는 것이 좋습니다.

>[!MORELIKETHIS]
>
>* Adobe Analytics의 [[!UICONTROL 낮은 트래픽] 값](/help/technotes/low-traffic.md)
>* [처리 규칙 개요](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)

<!-- https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=OmniArch&title=Uniques -->
