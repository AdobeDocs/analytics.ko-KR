---
title: eVar(머천다이징 변수)
description: 개별 제품에 연결된 사용자 정의 변수입니다.
feature: Appmeasurement Implementation
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
mini-toc-levels: 3
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/BdChWcR9AJqLZ0KjOxSvFAjB8-58JmmGahrpvTyFeFI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: ca917b867cd84b09b899ce7b72586f0b15003106
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 29%
---
# eVar (머천다이징)

>[!BEGINSHADEBOX]

*이 도움말 페이지에서는 머천다이징 eVar를 구현하는 방법에 대해 설명합니다. 머천다이징 eVar가 차원으로 작동하는 방법에 대한 자세한 내용은 구성 요소 사용 안내서의 [eVar(머천다이징 차원)](/help/components/dimensions/evar-merchandising.md)을(를) 참조하십시오.*

>[!ENDSHADEBOX]

머천다이징 eVar는 값을 개별 제품에 바인딩하므로 각 제품과 관련된 성공 이벤트는 해당 제품에 바인딩된 값에 반영됩니다. 다음 두 가지 방법 중 하나로 값을 설정할 수 있습니다.

* **[!UICONTROL 제품 구문]**: [`products`](products.md) 변수의 각 제품에 대한 값을 설정합니다.
* **[!UICONTROL 전환 변수 구문]**: eVar 자체에서 값을 설정합니다. 이 값은 바인딩 이벤트가 포함된 히트의 제품에 바인딩됩니다.

바인딩, 할당 및 만료가 작동하는 방법은 [eVar(머천다이징 차원)](/help/components/dimensions/evar-merchandising.md)을(를) 참조하십시오.

## 보고서 세트 설정에서 eVar 설정

구현에서 eVar를 사용하기 전에 보고서 세트 설정에서 eVar를 원하는 구문으로 구성해야 합니다. 관리 안내서에서 [전환 변수](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.

>[!WARNING]
>
>머천다이징 eVar를 올바로 구성하지 않으면 이 변수에 대해 예기치 않은 값이나 데이터 손실이 발생합니다. 이 변수를 구현에 맞게 올바로 구성했는지 확인하십시오.

## 구문 선택

`products` 변수를 설정할 때 머천다이징 값을 사용할 수 있거나 동일한 히트에 있는 제품에 다른 값이 필요한 경우에는 [!UICONTROL 제품 구문]을 사용하십시오. 방문자를 제품으로 이끈 검색어나 내부 캠페인과 같이 제품 앞에 값을 알고 있는 경우 [!UICONTROL 전환 변수 구문]을 사용하십시오. 전체 비교는 [바인딩 및 할당이 작동하는 방법](/help/components/dimensions/evar-merchandising.md#how-binding-and-allocation-work)을 참조하십시오.

## 제품 구문을 사용한 구현

[!UICONTROL 제품 구문]을 사용하도록 설정하면 머천다이징 값이 `products` 변수 내에서 직접 설정되므로 바인딩 이벤트가 사용되지 않습니다. 머천다이징 eVar는 각 제품의 마지막 세그먼트로 이동합니다.

```js
s.products = "[category];[name];[quantity];[revenue];[events];[eVars]";
```

동일한 제품에 대해 여러 머천다이징 eVar를 파이프(`|`)를 사용하여 구분하십시오. 수량, 수익 및 이벤트에 대한 빈 자리 표시자는 사용하지 않더라도 필수입니다. 이러한 변수가 없으면 eVar 값이 무시됩니다.

값은 해당 히트의 제품에 바인딩됩니다. 이후 값이 기존 바인딩을 대체하는지 여부는 [!UICONTROL 할당] 설정에 따라 다릅니다. [바인딩 및 할당 작동 방식](/help/components/dimensions/evar-merchandising.md#how-binding-and-allocation-work)을 참조하세요.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

### 웹 SDK를 사용한 제품 구문

[**XDM 개체**](/help/implement/aep-edge/xdm-var-mapping.md)&#x200B;를 사용하는 경우 제품 구문 머천다이징 변수는 다음 XDM 필드를 사용합니다.

* 제품 구문 머천다이징 eVar는 `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar1` 아래에서 `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar250`에 매핑됩니다.
* 제품 구문 머천다이징 이벤트는 `xdm.productListItems[]._experience.analytics.event1to100.event1.value` 아래에서 `xdm.productListItems[]._experience.analytics.event901to1000.event1000.value`에 매핑됩니다. [이벤트 일련화](events/event-serialization.md) XDM 필드는 `xdm.productListItems[]._experience.analytics.event1to100.event1.id` 아래에서 `xdm.productListItems[]._experience.analytics.event901to1000.event1000.id`에 매핑됩니다.

>[!NOTE]
>
>`productListItems` 아래에서 이벤트를 설정할 때 이벤트 문자열에서 설정할 필요가 없습니다. 두 위치에 모두 설정된 경우 이벤트 문자열의 값이 우선합니다.

다음 예는 여러 상품화 eVar 및 이벤트를 사용하는 단일 [제품](products.md)을 보여 줍니다.

```json
"productListItems": [
  {
    "name": "Bahama Shirt",
    "priceTotal": "12.99",
    "quantity": 3,
    "_experience": {
      "analytics": {
        "customDimensions" : {
          "eVars" : {
            "eVar10" : "green",
            "eVar33" : "large"
          }
        },
        "event1to100" : {
          "event4" : {
            "value" : 1
          },
          "event10" : {
            "value" : 2,
            "id" : "abcd"
          }
        }
      }
    }
  }
]
```

위의 예 오브젝트는 `";Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large"`로 Adobe Analytics에 전송됩니다.

[**데이터 개체**](/help/implement/aep-edge/data-var-mapping.md)&#x200B;를 사용하는 경우 AppMeasurement `products` 변수와 동일한 구문을 사용하여 제품 구문 머천다이징 eVar가 `data.__adobe.analytics.products`에 설정됩니다. 위의 XDM 예제와 동등한 데이터 개체:

```json
"data": {
  "__adobe": {
    "analytics": {
      "products": ";Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large"
    }
  }
}
```

## 전환 변수 구문을 사용한 구현

`products` 변수에서 eVar 값을 설정할 수 없을 때 [!UICONTROL 전환 변수 구문]을 사용하십시오. 이 시나리오는 일반적으로 제품 페이지에 머천다이징 채널 또는 검색 방법 컨텍스트가 없음을 의미합니다. 이러한 경우 바인딩 이벤트가 발생하는 페이지에서 또는 그 이전에 머천다이징 eVar을 설정합니다. 이 값은 만료되거나 새 값으로 덮어쓰여질 때까지 지속됩니다.

히트에 `products` 변수와 선택한 [!UICONTROL 머천다이징 바인딩 이벤트]가 모두 포함되어 있으면 eVar의 현재 값이 해당 히트의 모든 제품에 바인딩됩니다. 바인딩 이벤트 없이 제품과 함께 eVar을 설정하면 값이 바인딩되지 않습니다. 이후 바인딩이 기존 바인딩을 대체할지 여부는 [!UICONTROL 할당] 설정에 따라 다릅니다. [바인딩 및 할당 작동 방식](/help/components/dimensions/evar-merchandising.md#how-binding-and-allocation-work)을 참조하세요.

여러 제품 검색 방법 eVar를 한 번에 설정하는 예제는 [모범 사례: 제품 검색 방법](/help/components/dimensions/evar-merchandising.md#best-practice-product-finding-methods)을 참조하십시오.

다음 예제에서는 바인딩 이벤트 앞에 머천다이징 eVar을 설정합니다.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = ";Canary";
```

[!UICONTROL 제품 보기 이벤트]이(가) 바인딩 이벤트인 경우 `eVar1`의 값 `"Aviary"`이(가) 제품 `"Canary"`에 바인딩됩니다. 이 제품과 관련된 후속 성공 이벤트는 `"Aviary"`에 반영됩니다. 다음 조건 중 하나가 충족될 때까지 값 `"Aviary"`은(는) 바인딩 이벤트가 포함된 이후 히트의 제품에도 바인딩됩니다.

* eVar 만료([!UICONTROL 다음 시기 이후에 만료] 설정에 따름)
* 머천다이징 eVar가 새 값으로 덮어써집니다.

### 웹 SDK를 사용한 전환 변수 구문

[**XDM 개체**](/help/implement/aep-edge/xdm-var-mapping.md)&#x200B;를 사용하는 경우 구문은 다른 [eVars](evar.md) 및 [events](events/events-overview.md) 구현과 유사하게 작동합니다. [**데이터 개체**](/help/implement/aep-edge/data-var-mapping.md)&#x200B;를 사용하는 경우 구문은 AppMeasurement 다음에 나옵니다.

위의 AppMeasurement 예를 미러링하는 XDM은 다음과 같습니다.

동일한 이벤트 호출 또는 이전 이벤트 호출에서 eVar를 설정합니다.

```json
"_experience": {
  "analytics": {
    "customDimensions": {
      "eVars": {
        "eVar1" : "Aviary"
      }
    }
  }
}
```

제품 문자열에 대한 바인딩 이벤트 및 값을 설정합니다.

```json
"commerce": {
  "productViews" : {
    "value" : 1
  }
},
"productListItems": [
  {
    "name": "Canary"
  }
]
```

위의 AppMeasurement 예제를 미러링하는 데이터 개체는 다음과 같습니다.

동일한 이벤트 호출 또는 이전 이벤트 호출에서 eVar를 설정합니다.

```json
"data": {
  "__adobe": {
    "analytics": {
      "eVar1": "Aviary"
    }
  }
}
```

제품 문자열에 대한 바인딩 이벤트 및 값을 설정합니다.

```json
"data": {
  "__adobe": {
    "analytics": {
      "events": "prodView",
      "products": ";Canary"
    }
  }
}
```

