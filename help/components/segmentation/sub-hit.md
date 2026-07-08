---
title: 하위 히트 분석
description: 하위 히트 분석을 통해 Adobe Analytics의 히트 내에서 개별 제품을 필터링하여 제품 보고서에서 속성 출혈을 제거하는 방법에 대해 알아봅니다.
feature: Segmentation
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: a544b409-2610-410d-a842-474ac1d0d54e
source-git-commit: 0168cf33d647c5edb367094d57ad9ea3ee253844
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 0%

---

# 하위 히트 분석

{{release-limited-testing}}

하위 히트 분석을 사용하면 히트 수준보다 더 세분화된 수준에서 제품 데이터를 분석할 수 있습니다. 전체 히트에 대해 필터링하는 대신 히트 내의 개별 제품에 대해 세그먼트화할 수 있습니다. 예를 들어 동일한 순서로 구매한 다른 모든 제품을 포함하지 않고 특정 제품 카테고리로 세그먼트화할 수 있습니다.

Adobe Analytics 하위 히트 분석에서는 특히 **[!UICONTROL Products]** 변수에 적용됩니다. **[!UICONTROL Products]** 변수는 Adobe Analytics에서 하위 히트 분석을 지원하는 유일한 다중 값 개체입니다.

Adobe Analytics에서 [제품 변수](/help/components/dimensions/product.md)은(는) 하나의 히트에서 여러 제품을 캡처할 수 있습니다. 하위 히트 분석이 없으면 제품 속성에 대해 세그먼트화하면 히트 내의 모든 제품이 제품 속성과 일치하는 모든 히트가 반환됩니다. 그 결과가 잘못된 속성 및 부풀려진 매출 지표입니다. 하위 히트 분석은 필터를 히트 내의 개별 제품 행으로 범위를 지정하고 이러한 문제를 해결합니다.

하위 히트 분석에서 제외 논리는 제품 변수에 대한 표준 히트 수준 제외와 다르게 동작합니다. [!UICONTROL 제품] 컨테이너 내에서 제품 특성을 제외하면 세그먼트는 **제품이 있음**&#x200B;을 반환하지만 제외 기준과 일치하지 않는 히트를 반환합니다. 세그먼트는 제품이 없는 히트를 전혀 반환하지 않습니다.

## 예

남성 범주의 온라인 매출만 측정하려 합니다. 하위 히트 분석이 없으면 Men에 대한 세그먼트를 적용하면 Men 카테고리가 있는 제품이 하나 이상 포함된 주문(히트)에 있는 모든 제품의 수익이 포함됩니다. 하위 히트 분석을 사용하면 필터를 제품 수준으로 확장하고 Men 카테고리의 제품에 대한 매출만 반환합니다.

또한 남성 범주를 제외한 다른 모든 범주의 온라인 매출을 측정하려고 합니다.

>[!BEGINTABS]

>[!TAB 히트 분석]

세그먼테이션 빌더에서 또는 **[!UICONTROL 빠른 세그먼트]**&#x200B;의 일부로 **[!UICONTROL 히트]** 컨테이너에 **[!UICONTROL Dimension]** **[!UICONTROL 소매: 패션 제품 범주]** **[!UICONTROL 같음]** **[!UICONTROL 남성]**&#x200B;을 **[!UICONTROL 포함]**&#x200B;하도록 지정합니다.

![제품 범주 남성에 대한 히트 수준의 세그먼테이션을 보여 주는 패널](./assets/product-category-segmentation-hits.png)

따라서 최소 한 개 이상의 **[!UICONTROL 남성]** **[!UICONTROL 소매: 패션 제품 범주]**&#x200B;가 포함된 모든 주문이 고려되며 이러한 주문의 다른 제품 매출은 **[!UICONTROL 온라인 매출]** 지표에 포함됩니다.카테고리를 보고할 때 **[!UICONTROL Men]** **[!UICONTROL Retail: Fashion Product Category]**&#x200B;와(과) 함께 제품을 포함하는 주문의 일부인 **[!UICONTROL Retail: Fashion Product Category]**&#x200B;에 대한 다른 모든 값이 보고됩니다.

>[!TAB 하위 히트 분석]

세그먼테이션 빌더에서 또는 **[!UICONTROL 빠른 세그먼트]**&#x200B;의 일부로 **[!UICONTROL 제품]** 컨테이너에 **[!UICONTROL Dimension]** **[!UICONTROL 소매: 패션 제품 범주]** **[!UICONTROL 같음]** **[!UICONTROL 남성]**&#x200B;을 **[!UICONTROL 포함]**&#x200B;하도록 지정합니다.

![제품 범주 남성의 하위 히트 수준에 대한 세분화를 보여 주는 패널](./assets/product-category-segmentation-sub-hits.png)

그 결과, 최소 **[!UICONTROL 남성]** **[!UICONTROL 소매: 패션 제품 범주]**&#x200B;을 포함하는 모든 주문이 고려되며 **[!UICONTROL 남성]** **[!UICONTROL 소매: 패션 제품 범주]**&#x200B;에 속하는 제품의 매출만 **[!UICONTROL 온라인 매출]** 지표에 포함됩니다.범주를 보고할 때 **[!UICONTROL 남성]** **[!UICONTROL 소매: 패션 제품 범주]**&#x200B;만 보고됩니다.

>[!TAB 하위 히트 분석(제외)]

세그먼테이션 빌더에서 또는 **[!UICONTROL 빠른 세그먼트]**&#x200B;의 일부로 **[!UICONTROL 제품]** 컨테이너에 **[!UICONTROL Dimension]** **[!UICONTROL 소매: 패션 제품 범주]** **[!UICONTROL 같음]** **[!UICONTROL 남성]**&#x200B;을 **[!UICONTROL 제외]**&#x200B;하도록 지정합니다.

![제품 범주 남성을 제외하기 위한 하위 히트 수준의 세그먼테이션을 보여 주는 패널](./assets/product-category-segmentation-sub-hits-exclude.png)

제품 수준에서 제외하려면 하나 이상의 제품이 포함된 히트가 포함된 다음 하위 히트 수준의 제외가 해당 범위 내에 적용됩니다. 이 제외는 전체 히트를 제외하는 히트 수준 제외와 다릅니다.

>[!ENDTABS]
