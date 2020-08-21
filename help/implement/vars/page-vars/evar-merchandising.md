---
title: eVar(머천다이징)
description: 개별 제품에 연결된 사용자 지정 변수입니다.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '355'
ht-degree: 100%

---


# eVar(머천다이징)

*이 도움말 페이지에서는 머천다이징 eVar를 구현하는 방법에 대해 설명합니다. 머천다이징 eVar가 차원으로 작동하는 방법에 대한 자세한 내용은 구성 요소 사용 안내서의[eVar(머천다이징)](/help/components/dimensions/evar-merchandising.md)를 참조하십시오.*

## 보고서 세트 설정에서 eVar 설정

구현에서 eVar를 사용하기 전에 보고서 세트 설정에서 eVar를 원하는 구문으로 구성해야 합니다. 관리 안내서에서 [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.

>[!IMPORTANT]
>
>머천다이징 eVar를 올바로 구성하지 않으면 이 변수에 대해 예기치 않은 값이나 데이터 손실이 발생합니다. 이 변수를 구현에 맞게 올바로 구성했는지 확인하십시오.

## 제품 구문을 사용한 구현

제품 구문이 활성화된 경우 머천다이징 카테고리가 `products` 변수 내에서 직접 채워지므로 결합 이벤트를 선택하고 설정할 필요가 없습니다. 성공 이벤트가 발생할 때 변수를 `products`에서 사용할 수 없는 경우를 제외하고 이 방법이 권장됩니다.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

`eVar1`에 대한 값이 제품에 지정됩니다. 이 제품과 관련된 이후의 모든 성공 이벤트는 eVar 값에 반영됩니다.

## 전환 변수 구문을 사용한 구현

`products` 변수에서 eVar 값을 설정할 수 없을 때 전환 변수 구문이 사용됩니다. 이 시나리오는 일반적으로 페이지에 머천다이징 채널 또는 검색 방법 컨텍스트가 없음을 의미합니다. 이 경우 제품 페이지에 도착하기 전에 머천다이징 변수를 설정하고 값은 결합 이벤트가 발생할 때까지 지속됩니다.

구성 중에 선택한 결합 이벤트가 발생하면 eVar의 지속된 값이 제품과 연결됩니다. 예를 들어 `prodView`가 결합 이벤트로 지정된 경우 머천다이징 카테고리가 이벤트가 발생하는 시점에만 현재 제품 목록과 연결됩니다. 후속 결합 이벤트만이 이미 제품에 지정된 머천다이징 eVar를 업데이트할 수 있습니다.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = "Birds;Canary";
```

`eVar1`에 대한 값 `"Aviary"`가 제품 `"Canary"`에 지정됩니다. 이 제품과 관련된 이후의 모든 성공 이벤트는 `"Canary"`에 반영됩니다. 또한 다음 조건 중 하나가 만족될 때까지 머천다이징 변수의 현재 값이 모든 후속 제품에 연결됩니다.

* eVar 만료(&#39;다음 시기 이후에 만료&#39; 설정에 따름)
* 머천다이징 eVar가 새로운 값으로 덮어쓰기됨.
