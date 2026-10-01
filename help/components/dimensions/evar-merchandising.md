---
title: eVar (머천다이징 차원)
description: 제품 차원에 연결된 사용자 지정 변수입니다.
feature: Dimensions
exl-id: a7e224c4-e8ae-4b53-8051-8b5dd43ff380
TQID: 'https://experienceleague.adobe.com/No-Va3JzN6Qz9hBu73A5ZzKudEB1Tqa4sNPKVKAASGI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
    internal-label: Dimensions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: ca917b867cd84b09b899ce7b72586f0b15003106
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 4%
---
# eVar (머천다이징)

>[!BEGINSHADEBOX]

*이 도움말 페이지에서는 머천다이징 eVar가 [차원](overview.md)(으)로 작동하는 방식을 설명합니다. 머천다이징 eVar 구현 방법에 대한 자세한 내용은 구현 사용 안내서의 [eVar(머천다이징 변수)](/help/implement/vars/page-vars/evar-merchandising.md)을(를) 참조하십시오.*

>[!ENDSHADEBOX]

머천다이징 eVar은 각 제품에 자체 사본이 있다는 점을 제외하면 표준 eVar과 유사하게 작동합니다. 지속성, 할당 및 만료는 모두 동일한 방식으로 작동하지만 각 제품마다 별도로 작동합니다. 표준 eVar은 모든 성공 이벤트에 대한 크레딧을 받는 방문자당 하나의 지속적인 값을 보유합니다. 머천다이징 eVar은 제품당 하나의 지속적인 값을 보유하며 해당 값은 해당 제품의 성공 이벤트에 대한 크레딧을 받습니다.

* 제품 A → `eVar1` = `value A`
* 제품 B → `eVar1` = `value B`

각 제품의 값은 해당 제품을 포함하는 히트에서만 설정하거나 변경할 수 있습니다. 설정되면 값은 만료될 때까지 지속되며 해당 제품의 성공 이벤트에 대한 크레딧만 받습니다. 제품 A의 값을 변경해도 제품 B에는 영향을 미치지 않습니다.

머천다이징 eVar는 [`products`](/help/implement/vars/page-vars/products.md) 변수에서만 작동합니다. 제품에 바인딩되지 않은 머천다이징 eVar 값은 크레딧을 받지 않습니다. 제품이 없는 히트에 대한 성공 이벤트는 모든 머천다이징 eVar의 `"None"`에 연결됩니다.

>[!TIP]
>
>지속된 값을 제품이 아닌 차원에 바인딩하려면 Customer Journey Analytics에서 [[!UICONTROL 바인딩 차원]](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-dataviews/component-settings/persistence#binding-dimension)을 사용하는 것이 좋습니다.

## 머천다이징 eVar를 사용하는 이유

방문자가 구매하는 모든 것에 대해 하나의 값이 크레딧을 받지 않아야 할 때 각 제품에 대해 별도의 값을 유지하는 것이 중요합니다. 표준 eVar은 외부 캠페인 또는 외부 검색어에 잘 작동합니다. 이 경우 발생하는 모든 성공 이벤트에 대한 크레딧을 한 가지 값으로 받아야 합니다. 예를 들어 고객이 이메일 캠페인의 링크를 클릭하여 웹 사이트를 방문하는 경우 그 결과로 이루어진 모든 구매는 해당 캠페인에 대한 크레딧이 있어야 합니다.

방문자는 종종 내부 검색을 사용하여 각각 다른 방식으로 여러 제품을 발견하기 때문에 내부 검색과 범주 탐색이 다릅니다. 예를 들어 고객이 귀하의 사이트에서 `"goggles"`를 검색하여 찾은 후 장바구니에 추가합니다.

![고글 예](assets/merch-example-goggles.png)

결제에 앞서 고객이 `"winter coat"`을(를) 검색한 다음 장바구니에 다운 재킷을 추가합니다.

![코트 예](assets/merch-example-coat.png)

방문자가 이 구매를 완료하면 내부 검색어 `"winter coat"`이(가) eVar의 가장 최근 값([!UICONTROL 가장 최근 값(마지막)]의 기본 할당)이므로 고글을 포함한 전체 주문에 대해 크레딧을 받습니다. 검색어 `"goggles"`이(가) 구매의 일부로 연결되었지만 크레딧을 받지 못했습니다.

| 내부 검색어 | 매출 |
| --- | --- |
| 겨울 외투 | 157달러 |

## 머천다이징 eVar로 이 문제를 해결하는 방법

이전 예에서 eVar에 대해 머천다이징이 활성화된 경우 검색어 `"goggles"`은(는) 스키용 고글에 바인딩되고 검색어 `"winter coat"`은(는) 다운 재킷에 바인딩됩니다. 머천다이징 eVar는 제품 수준에서 매출을 할당하므로 각 용어가 바인딩된 제품에 대한 수익 금액에 대한 크레딧을 받습니다.

| 내부 검색어 | 매출 |
| --- | --- |
| 겨울 외투 | 119달러 |
| 고글 | $38 |

## 바인딩 및 할당 작동 방식

머천다이징 eVar는 다음 세 가지 개념을 사용합니다.

* **바인딩**: 제품과 eVar 값 간의 연결입니다. 각 제품은 각 머천다이징 eVar에 대해 고유한 바인딩을 유지합니다. 표준 eVar 값과 마찬가지로 바인딩은 만료되기 전까지 이후 히트에서 유지됩니다. 예를 들어 제품 페이지에서 제품에 바인딩된 값은 나중에 해당 제품을 구매할 때 값을 다시 설정하지 않고도 계속 크레딧을 받습니다. 값이 제품에 도달하는 방법은 아래에 설명된 eVar 구문에 따라 다릅니다.
* **할당**: [!UICONTROL 할당] 설정은 새 값이 **이미 바인딩된**&#x200B;인 제품에 바인딩하려고 할 때 수행되는 작업을 결정합니다. 할당은 제품마다 별도로 평가되므로 다른 제품에 바인딩된 머천다이징 eVar 값은 서로 경쟁하지 않습니다.
  * **[!UICONTROL 원래 값(첫 번째)]**: 기존 바인딩이 유지됩니다. 바인딩이 만료될 때까지 해당 제품에 대한 새 값이 무시됩니다.
  * **[!UICONTROL 가장 최근(마지막)]**: 제품이 새 값에 다시 바인딩됩니다.
* **만료**: [!UICONTROL 다음 시기 이후에 만료] 설정은 바인딩이 종료되는 시기를 결정합니다. 각 제품의 바인딩에는 해당 제품이 바인딩된 시점부터 계산되는 자체 만료일이 있습니다. 예를 들어, [!UICONTROL 주] 만료인 경우 제품 A가 월요일에 바인딩되고 제품 B가 수요일에 바인딩되면 제품 A의 바인딩이 그 다음 월요일에 만료되고 제품 B의 바인딩이 그 다음 수요일에 만료됩니다. 바인딩이 만료되면 표준 eVar이 만료된 후 값을 가지지 않는 것과 마찬가지로 제품에는 더 이상 해당 eVar에 대한 값이 없습니다. 해당 제품에 대한 성공 이벤트는 제품이 다시 바인딩될 때까지 `"None"`에 연결됩니다.

각 머천다이징 eVar은 [보고서 세트 설정](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md)의 [!UICONTROL 머천다이징] 설정에 설정된 두 구문 중 하나를 사용합니다. 구문은 값이 제품에 도달하는 방법을 결정합니다.

* **[제품 구문](#product-syntax)**: 값이 `products` 변수의 각 제품에 직접 설정되고 해당 히트의 해당 제품에 바인딩됩니다.
* **[전환 변수 구문](#conversion-variable-syntax)**: 값이 eVar 자체에 설정되어 표준 eVar 값처럼 유지됩니다. 바인딩 이벤트가 포함된 동일한 히트 또는 이후 히트의 제품에 바인딩됩니다.

두 구문 모두 위에서 설명한 동일한 바인딩, 할당 및 만료 동작을 사용합니다. 다음과 같은 점에서 차이가 있습니다.

| | 제품 구문 | 전환 변수 구문 |
| --- | --- | --- |
| 값이 설정되는 위치 | 각 제품에서 [`products`](/help/implement/vars/page-vars/products.md) 변수 | 표준 eVar과 동일한 방식으로 [`eVar`](/help/implement/vars/page-vars/evar-merchandising.md) 자체에서 |
| 바인딩 발생 시 | 제품에 값이 설정된 모든 히트에서 | 제품 및 구성된 바인딩 이벤트가 모두 포함된 히트에서 |
| 히트당 값 | 각 제품은 다른 값을 가질 수 있습니다 | 바인딩 히트의 모든 제품은 동일한 값을 받습니다 |
| 구현 노력 | 높음 | Lower |

## 제품 구문

제품 구문을 사용하면 `products` 변수의 각 제품에 eVar 값이 설정됩니다. `products` 문자열에서 제품의 마지막 세미콜론 뒤의 값은 머천다이징 eVar입니다. 전체 구문은 [제품 구문을 사용하여 구현](/help/implement/vars/page-vars/evar-merchandising.md#implement-using-product-syntax)을 참조하십시오.

값은 해당 히트의 해당 제품에 직접 바인딩됩니다. 바인딩 이벤트는 사용되지 않습니다. 장바구니 추가 또는 구매와 같이 제품을 포함하는 이후 히트는 값을 반복할 필요가 없습니다. 각 제품은 고유한 값을 가지고 있으므로 **동일한 히트**&#x200B;에 있는 제품에 **다른** 값이 필요한 경우 제품 구문이 유일한 옵션입니다.

+++예: 동일한 제품이 두 개의 값을 받습니다

| 히트 | `products` | `events` |
| --- | --- | --- |
| 1 | `;12345;;;;eVar1=internal keyword search` | |
| 2 | `;12345;;;;eVar1=internal campaign` | |
| 3 | `;12345;1;50` | `purchase` |

* **[!UICONTROL 원래 값(첫 번째)]**: 제품 `12345`에 대해 히트 2가 무시됩니다. 구매가 `internal keyword search`(으)로 크레딧되었습니다.
* **[!UICONTROL 가장 최근(마지막)]**: 히트 2 제품 `12345`을(를) 리바인딩합니다. 구매가 `internal campaign`(으)로 크레딧되었습니다.

+++

+++예: 두 제품이 서로 다른 값을 받습니다

| 히트 | `products` | `events` |
| --- | --- | --- |
| 1 | `;productA;;;;eVar1=value A` | |
| 2 | `;productB;;;;eVar1=value B` | |
| 3 | `;productA;1;50,;productB;1;30` | `purchase` |

각 제품은 자체 바인딩을 유지하므로 이 예제에서는 할당 설정이 적용되지 않습니다. `value A`은(는) 제품 A의 매출에 대한 크레딧을 받고 `value B`은(는) 제품 B의 매출에 대한 크레딧을 받습니다. 두 값 모두 하나의 주문을 받습니다. 주문에는 각 값에 바인딩된 제품이 포함되어 있기 때문입니다.

+++

+++예: ID가 같고 값이 다른 제품

방문자가 상위 제품 ID가 `tshirt123`인 중간 크기의 파란색 티셔츠와 큰 크기의 빨간색 티셔츠를 구매하면 `eVar10`에서 하위 SKU를 캡처합니다.

```js
s.events = "purchase";
s.products = ";tshirt123;1;20;;eVar10=tshirt123-m-blue,;tshirt123;1;20;;eVar10=tshirt123-l-red";
```

각 하위 SKU는 `tshirt123`의 자체 인스턴스에 대한 크레딧을 받습니다.

+++

제품 구문은 바인딩이 발생할 때마다 각 제품에 대한 전체 값 문자열이 필요합니다. 일반적으로 여러 eVar를 한 번에 사용하는 제품 검색 방법의 경우 문자열은 다음과 같습니다.

```js
s.products = ";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";
```

검색 방법은 방문자가 제품과 상호 작용한 후에만 크레딧을 받아야 하므로 이 문자열은 일반적으로 검색 결과 페이지가 아닌 제품 세부 사항 페이지 또는 장바구니 추가 페이지에서 설정됩니다. 이렇게 하려면 개발자는 다음을 수행해야 합니다.

* 검색 방법 페이지에서 제품 세부 사항 페이지로 검색 방법 세부 사항을 전달하거나 장바구니 추가가 결과 페이지에서 실행될 때 사용할 수 있도록 합니다.
* 구문 오류 없이 전체 `products` 문자열을 어셈블합니다.

전환 변수 구문은 두 요구 사항을 모두 충족합니다.

## 전환 변수 구문

전환 변수 구문을 사용하면 값이 eVar 자체에서 설정됩니다.

```js
s.eVar1 = "internal keyword search";
```

eVar은 *준비 영역* 역할을 합니다. eVar에 설정된 값은 바인딩 이벤트가 히트의 제품에 바인딩될 때까지 유지됩니다. 바인딩은 다음 두 단계로 진행됩니다.

1. **스테이징**: eVar이 설정되면 해당 값은 만료될 때까지 후속 히트에서 유지됩니다. 이 지속된 값은 [데이터 피드](/help/export/analytics-data-feed/data-feed-overview.md)의 `post_evar` 열입니다. 전환 변수 구문을 사용하는 머천다이징 eVar의 경우 [!UICONTROL 할당] 설정에 관계없이 준비된 값 **은(는) 보낸 가장 최근 값**&#x200B;을(를) 항상 반영합니다. 각 새 값은 이전에 준비된 값을 대체합니다.
1. **바인딩**: 히트에 제품과 구성된 [!UICONTROL 머천다이징 바인딩 이벤트]가 모두 포함된 경우 준비된 값은 해당 히트의 모든 제품에 바인딩됩니다. 제품이 이미 바인딩된 경우 [!UICONTROL 할당]은 새 값이 기존 바인딩을 대체하는지 여부를 결정합니다. 이미 바인딩된 제품은 해당 값을 [!UICONTROL 원래 값(첫 번째)]으로 유지하거나 [!UICONTROL 가장 최근 값(마지막)]으로 리바인딩합니다.

eVar, `products` 변수 및 바인딩 이벤트가 모두 동일한 히트에서 설정된 경우 스테이징과 바인딩이 동시에 발생합니다. 새 값은 해당 히트의 제품에 즉시 바인딩됩니다.

바인딩 이벤트 없이 제품과 함께 eVar을 설정하면 값이 해당 제품에 바인딩되지 않습니다. 단계적 값은 제품에 바인딩될 때까지 크레딧을 받지 않습니다.

### 바인딩 이벤트의 기능

바인딩 이벤트는 Adobe에 준비된 값을 히트의 제품에 바인딩하도록 지시하는 트리거입니다.

* 바인딩 이벤트는 표준 또는 사용자 지정 성공 이벤트, 추적 코드([!UICONTROL 캠페인 이벤트]) 또는 eVar일 수 있습니다. Prop은 바인딩에 영향을 주지 않습니다.
* [!UICONTROL 제품 보기 이벤트], [!UICONTROL 장바구니 추가 이벤트], [!UICONTROL 구매 이벤트]와 같은 여러 바인딩 이벤트를 구성할 수 있습니다. 이러한 이벤트 중 하나가 제품이 있는 히트에 있는 경우 스테이징된 값은 해당 히트의 모든 제품에 바인딩됩니다.
* 기본적으로([!UICONTROL 모두]), 다른 이벤트 또는 eVar이 제품과 동일한 히트에 있을 때마다 바인딩이 발생합니다. 바인딩 이벤트가 명시적으로 선택되지 않은 경우 [!UICONTROL 모두]이(가) 사용됩니다. [!UICONTROL 모두]를 사용하여 제품을 포함하는 히트에서 eVar을 설정하면 해당 히트에서 바인딩이 항상 트리거됩니다. 이전 히트에서 준비된 값은 제품 및 기타 모든 이벤트 또는 eVar을 포함하는 다음 히트에 바인딩됩니다.

+++예: 바인딩 이벤트를 사용한 바인딩

다음 히트를 고려하십시오.

```js
// Hit 1
s.eVar1 = "internal keyword search";
s.eVar2 = "sandals";

// Hit 2
s.products = ";sandal123";
s.events = "prodView";
```

`prodView`이(가) 두 eVar에 대한 바인딩 이벤트인 경우, 히트 2는 `internal keyword search`(`eVar1`) 및 `sandals`(`eVar2`)을(를) `sandal123`에 바인딩합니다. eVar에서 `prodView`을(를) 바인딩 이벤트로 나열하지 않으면 해당 eVar에 대한 바인딩이 발생하지 않습니다.

+++

+++예: 할당은 제품별로 평가됩니다

| 히트 | `eVar1` | `products` | `events` |
| --- | --- | --- | --- |
| 1 | `value A` | | |
| 2 | | `;productA,;productB` | 바인딩 이벤트 |
| 3 | `value B` | | |
| 4 | | `;productA` | 바인딩 이벤트 |
| 5 | | `;productA;1;50,;productB;1;30` | `purchase` |

히트 3 후 스테이징된 값(`post_evar1`)은 두 할당 설정이 있는 `value B`입니다.

* **[!UICONTROL 원래 값(첫 번째)]**: 제품 A가 이미 바인딩되었으므로 제품 A에 대한 히트 4가 무시됩니다. 두 제품 모두 모든 구매 크레딧을 받는 `value A`에 연결되어 있습니다.
* **[!UICONTROL 가장 최근(마지막)]**: 히트 4는 제품 A를 `value B`에 다시 바인딩합니다. 제품 B가 히트 4에 있지 않으므로 `value A`에 바인딩된 상태로 유지됩니다. 제품 A의 구매 크레딧은 `value B`이고 제품 B의 구매 크레딧은 `value A`입니다.

히트 1, 2, 5와 같이 단일 바인딩 시도만으로도 두 설정 모두 동일한 결과를 생성합니다. 할당은 이미 바인딩된 제품이 다른 바인딩 시도를 수신하는 경우에만 중요합니다.

+++

## 모범 사례: 제품 검색 방법

대부분의 소매 사이트에서는 각각 머천다이징 eVar과 같은 다음과 같은 제품 검색 방법을 추적할 수 있습니다.

* 내부 검색 키워드(예: `eVar2`)
* 내부 캠페인 추적 코드(예: `eVar3`)
* 머천다이징 또는 범주 찾아보기(예: `eVar4`)
* 크로스셀 링크(예: `eVar5`)
* 제품 페이지에 대한 외부 링크(예: `eVar1`)와 같은 메서드를 포함하여 모든 메서드를 비교하는 전체 제품 검색 방법 eVar

방문자가 한 가지 방법을 사용하는 경우 다른 검색 방법 eVar를 &quot;비&quot; 값으로 설정합니다. 그렇지 않으면 사용되지 않은 방법의 이전 값이 다른 방법을 통해 발견된 제품에 대한 크레딧을 받을 수 있습니다. 예를 들어 결과 페이지에서 &quot;샌들&quot;에 대한 내부 검색을 수행할 수 있습니다.

```js
s.eVar1 = "internal keyword search";
s.eVar2 = "sandals";
s.eVar3 = "non-internal campaign";
s.eVar4 = "non-browse";
s.eVar5 = "non-cross-sell";
```

전환 변수 구문을 사용하면 개발자는 prop의 검색어와 같은 간단한 값만 설정할 수 있으며, 구현의 로직이 머천다이징 eVar를 채울 수 있습니다. 페이지 사이에 전달하거나 `products` 문자열에 빌드할 필요가 없습니다. 바인딩이 발생하는 히트에 `products` 변수가 계속 필요합니다.

Adobe은 제품 검색 방법 eVar에 대해 다음 설정을 권장합니다.

| 설정 | 값 |
| --- | --- |
| [!UICONTROL 할당] | [!UICONTROL 원래 값(첫 번째)] |
| [!UICONTROL 다음 시기 이후에 만료] | [!UICONTROL 사용자 지정]을 사용하여 14일 또는 30일 동안 제품을 자동 제거하기 전까지 장바구니에 보관하는 기간. 장바구니에 제한이 없는 경우 [!UICONTROL 구매]를 사용하십시오. |
| [!UICONTROL Type] | [!UICONTROL 텍스트 문자열] |
| [!UICONTROL 머천다이징 사용] | [!UICONTROL 활성화됨] |
| [!UICONTROL 머천다이징] | [!UICONTROL 전환 변수 구문] |
| [!UICONTROL 머천다이징 바인딩 이벤트] | [!UICONTROL 제품 보기 이벤트], [!UICONTROL 장바구니 추가 이벤트] 및 [!UICONTROL 구매 이벤트] |

각 설정에 대한 설명은 관리 안내서의 [전환 변수](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.

+++가장 최근 값(마지막) 대신 원래 값(첫 번째)인 이유

방문자는 장바구니에서 이미 보거나 추가한 제품을 다시 찾는 경우가 많습니다. 예:

1. 방문자가 &quot;샌들&quot;을 검색하고 결과 페이지에서 `sandal123`을(를) 장바구니에 추가합니다. 제품이 `internal keyword search`에 바인딩됩니다.
1. 3일 후 방문자는 **여성 > 신발 > 샌들**(`eVar1` = `browse`)로 이동한 다음 `sandal123`을(를) 다시 보고 구매합니다.

[!UICONTROL 가장 최근(마지막)]을 사용하면 2단계의 제품 보기가 `sandal123`을(를) `browse`에 다시 바인딩한 다음 구매 크레딧을 받습니다. 원래 제품을 찾은 메서드는 를 받지 않습니다.

[!UICONTROL 원래 값(첫 번째)]을 사용하면 2단계의 바인딩 시도가 무시되고 `internal keyword search`이(가) 크레딧을 유지합니다.

방문자가 제품을 구매하지 않는 경우 만료에서 바인딩이 제거되므로 방문자가 사용하는 다음 검색 방법은 제품에 바인딩될 수 있습니다. [!UICONTROL 다음 시기 이후에 만료]이(가) 제품이 장바구니에 보관되는 기간과 일치해야 하는 이유입니다.

+++

## 머천다이징 eVar의 인스턴스

기본 [인스턴스](../metrics/instances.md) 지표는 머천다이징 변수에서 사용하지 않는 것이 좋습니다.

* 제품 구문을 사용하는 머천다이징 변수의 경우 인스턴스가 전혀 증가하지 않습니다.
* 전환 변수 구문을 사용하는 머천다이징 변수의 경우 eVar가 설정될 때마다 인스턴스가 계산됩니다. 그러나 인스턴스가 차원 항목 `"None"`에 대한 특성을 지정합니다. 단, 동일한 히트에서 다음 경우가 모두 발생하지 않습니다.
  * 머천다이징 eVar가 값으로 설정되어 있습니다.
  * `products` 변수가 값으로 정의되어 있습니다.
  * 바인딩 이벤트가 설정되었습니다.

전환 변수 구문에 대한 대부분의 사용 사례에서는 서로 다른 히트에 eVar 및 제품 변수가 필요하므로 기본 인스턴스 지표는 현실적으로 사용할 수 없습니다.

전환 변수 구문으로 전송된 각 값에 대한 인스턴스를 카운트하려면 **마지막 터치** [속성 모델](/help/analyze/analysis-workspace/attribution/overview.md)을 인스턴스 지표에 적용하십시오. 속성 모델은 스테이징된 값이나 제품 바인딩이 아니라 각 히트에서 전송된 값을 사용합니다. 마지막 터치는 eVar의 할당 설정에 관계없이 히트가 전송된 히트에서 각 값을 크레딧하므로 전환 확인 기간은 문제가 되지 않습니다.

![속성 선택](assets/attribution-select.png)
