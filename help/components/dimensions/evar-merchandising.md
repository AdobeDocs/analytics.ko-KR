---
title: eVar (머천다이징 차원)
description: 제품 차원에 연결된 사용자 지정 변수입니다.
feature: Dimensions
exl-id: a7e224c4-e8ae-4b53-8051-8b5dd43ff380
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 92%

---

# eVar (머천다이징)

*이 도움말 페이지에서는 머천다이징 eVar가 [차원](overview.md)(으)로 작동하는 방식을 설명합니다. 머천다이징 eVar 구현 방법에 대한 자세한 내용은 구현 사용 안내서의 [eVar(머천다이징 변수)](/help/implement/vars/page-vars/evar-merchandising.md)을(를) 참조하십시오.*

머천다이징 eVars의 작동 원리에 대한 자세한 내용은 [머천다이징 eVar 및 제품 검색 방법](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/merchandising-evars.md)을 참조하십시오.

일반적으로 외부 캠페인 또는 외부 검색 용어의 성공을 측정할 때는 하나의 값이 성공 이벤트 발생 요인으로 인정되기를 원할 것입니다. 예를 들어 고객이 이메일 캠페인의 링크를 클릭하여 웹 사이트를 방문하면 그에 따라 이루어진 모든 구매가 해당 캠페인 덕분인 것으로 됩니다.

내부 검색 또는 고객이 여러 항목을 찾을 때 카테고리 탐색으로 인해 발생한 이벤트의 경우 어떻습니까? 예를 들어 고객이 귀하의 사이트에서 `"goggles"`를 검색하여 찾은 후 장바구니에 추가합니다.

![고글 예](assets/merch-example-goggles.png)

이 고객은 결제에 앞서 `"winter coat"`를 검색하고 장바구니에 다운 재킷을 추가합니다.

![코트 예](assets/merch-example-coat.png)

방문자가 이 구매를 완료하면 고글 구매가 반영된 `"winter coat"`에 대한 내부 검색이 이루어집니다(eVar가 &#39;가장 최근 항목&#39;의 기본 할당을 사용한다고 가정). 이는 `"winter coat"`에는 좋지만 마케팅 의사 결정에는 적합하지 않습니다.

| 내부 검색어 | 수입 |
|---|---|
| 겨울 코트 | 157달러 |

## 머천다이징 변수로 이 문제를 해결하는 방법

머천다이징 evar를 통해 성공 이벤트가 발생하는 시점에 eVar의 현재 값을 제품에 할당할 수 있습니다. 이 값은 나중에 특정 eVar에 대해 새로운 값이 하나 이상 설정되어도 제품과의 연결을 유지합니다.

이전 예에서 eVar에 대해 머천다이징이 활성화되었다면 `"goggles"`라는 검색어가 스키용 고글에 연결되고 `"winter coat"`라는 검색어가 다운 재킷에 연결됩니다. 머천다이징 eVar는 제품 수준에서 매출을 할당하므로 각 용어가 이와 연결된 제품 수익 금액에 대한 요인으로 인정됩니다.

| 내부 검색어 | 수입 |
|---|---|
| 겨울 코트 | 119달러 |
| 고글 | $38 |

구현 지침이 필요하면 [머천다이징 eVar](/help/implement/vars/page-vars/evar-merchandising.md)를 참조하십시오.

## 머천다이징 변수의 인스턴스

[인스턴스](../metrics/instances.md) 지표는 머천다이징 변수에서 사용하지 않는 것이 좋습니다.

* 제품 구문을 사용하는 머천다이징 변수의 경우 인스턴스가 전혀 증가하지 않습니다.
* 전환 변수 구문을 사용하는 머천다이징 변수의 경우 eVar가 설정될 때마다 인스턴스가 계산됩니다. 하지만 이는 동일한 히트에서 다음 경우가 모두 발생하지 않는 한 차원 항목 `"None"`에 기여합니다.
   * 머천다이징 eVar가 값으로 설정되어 있습니다.
   * `products` 변수가 값으로 정의되어 있습니다.
   * 결합 이벤트가 설정되었습니다.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

전환 변수 구문에 대한 대부분의 사용 사례에서는 서로 다른 히트에서 eVar 및 products 변수가 필요하므로 &#39;인스턴스&#39; 지표를 사용하는 것은 현실적이지 않습니다.
