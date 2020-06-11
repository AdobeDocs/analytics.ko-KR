---
title: eVar(머천다이징)
description: 제품 차원에 연결된 사용자 지정 변수.
translation-type: tm+mt
source-git-commit: 1968162d856b6a74bc61f22f2e5a6b1599d04c79
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 25%

---


# eVar(머천다이징)

*이 도움말 페이지에서는 머천다이징 eVar가 차원으로 작동하는 방식을 설명합니다. For information on how to implement merchandising eVars, see[eVars](/help/implement/vars/page-vars/evar.md)in the Implement user guide.*

일반적으로 외부 캠페인 또는 외부 검색 용어의 성공을 측정할 때는 하나의 값이 성공 이벤트 발생 요인으로 인정되기를 원할 것입니다. 예를 들어 고객이 이메일 캠페인의 링크를 클릭하여 웹 사이트를 방문하면 그에 따라 이루어진 모든 구매가 해당 캠페인 덕분인 것으로 됩니다.

내부 검색이나 고객이 여러 항목을 찾을 때 카테고리 탐색에 의해 발생하는 이벤트는 어떻습니까? For example, a customer searches your site for `"goggles"`, then adds a pair to their cart:

![고글 예제](assets/merch-example-goggles.png)

Before checkout, the customer searches for `"winter coat"`, then adds a down jacket to the to their cart:

![코트의 예](assets/merch-example-coat.png)

방문자가 이 구매를 완료하면, 고글 한 쌍의 구매에 대한 내부 검색이 `"winter coat"` 이루어집니다(eVar가 &#39;가장 최근&#39;의 기본 할당을 사용한다고 가정). Good for `"winter coat"`, but bad for marketing decisions:

| 내부 검색어 | 수입  |
|---|---|
| 겨울 코트 | $157 |

## 머천다이징 변수로 이 문제를 해결하는 방법

머천다이징 eVar를 사용하면 성공 이벤트가 발생할 때 eVar의 현재 값을 제품에 할당할 수 있습니다. 이 값은 나중에 특정 eVar에 대해 새로운 값이 하나 이상 설정되어도 제품과의 연결을 유지합니다.

If merchandising is enabled for the eVar in the previous example, the search term `"goggles"` is tied to the snow goggles, and the search term `"winter coat"` is tied to the down jacket. 머천다이징 eVar는 제품 수준에서 매출을 할당하므로, 각 용어는 용어가 연관된 제품에 대한 매출액에 대한 크레딧을 받습니다.

| 내부 검색어 | 수입  |
|---|---|
| 겨울 코트 | $119 |
| 고글 | $38 |

구현 [지침은 머천다이징](/help/implement/vars/page-vars/evar-merchandising.md) eVar를 참조하십시오.

## 머천다이징 변수의 인스턴스

인스턴스 [지표는 머천다이징](../metrics/instances.md) 변수에서 사용하지 않는 것이 좋습니다.

* 제품 구문을 사용하는 머천다이징 변수의 경우 인스턴스가 전혀 증가하지 않습니다.
* 전환 변수 구문을 사용하는 머천다이징 변수의 경우 eVar가 설정될 때마다 인스턴스가 카운트됩니다. 하지만 동일한 히트에서 다음 사항이 모두 발생하지 `"None"` 않는 한 차원 값에 속성이 적용됩니다.
   * 머천다이징 eVar는 값으로 설정됩니다.
   * 이 `products` 변수는 값으로 정의됩니다.
   * 결합 이벤트가 설정되었습니다.

```js
// This merchandising eVar uses conversion variable syntax, and counts an instance.
// However, if the binding event and products variable are not both set, the instance attributes to "None".
s.eVar1 = "Tower defense";

// This merchandising eVar uses product syntax, and does not count an instance.
s.products = "Games;Wizard tower;;;;eVar2=Tower defense";
```

전환 변수 구문에 대한 대부분의 사용 사례는 서로 다른 히트에서 eVar 및 products 변수가 필요하므로 &#39;인스턴스&#39; 지표를 사용하는 것은 현실적이지 않습니다.
