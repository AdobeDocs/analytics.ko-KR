---
description: 머천다이징 변수에서 인스턴스가 카운팅되는 방식을 설명합니다.
keywords: Analytics 구현
seo-description: 머천다이징 변수에서 인스턴스가 카운팅되는 방식을 설명합니다.
seo-title: 머천다이징 변수의 인스턴스
solution: Analytics
title: 머천다이징 변수의 인스턴스
topic: 개발자 및 구현
uuid: 4 cdfd 53 e -88 aa -48 cf-a 135-98 f 7 fc 8 dcece
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 머천다이징 변수의 인스턴스

머천다이징 변수에서 인스턴스가 카운팅되는 방식을 설명합니다.

현재 머천다이징 변수에 대한 인스턴스는 지원되지 않습니다. 머천다이징 변수가 들어 있는 보고서에 인스턴스가 있다면, 그것은 eVar이 제품 문자열의 외부에 있는 일부 위치에 설정되고 있음을 의미하며, 선택한 머천다이징 변수에 대한 인스턴스의 실제 개수로 간주하지 말아야 합니다.

전환 변수 구문을 사용하는 경우 변수가 설정될 때마다 인스턴스가 카운트됩니다. 하지만 변수가 설정될 때마다 다음이 발생하지 않으면 인스턴스 속성은 "None"으로 설정됩니다.

* 결합 이벤트가 설정되었습니다.
* 제품 변수가 설정되었습니다.
* 머천다이징 eVar에 값이 있습니다.

예를 들어 다음 eVar1 인스턴스가 "Outdoors:Ski Goggles"로 할당됩니다.

```js
s.eVar1="Outdoors:Ski Goggles" 
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

하지만 다음 예제에서는 eVar가 설정되었을 때 모든 조건이 충족되지 않았으므로 eVar1 인스턴스가 "None"으로 할당됩니다(결합 이벤트가 없고 제품 변수가 설정되지 않음).

방문 페이지 1:

```js
s.eVar1="Outdoors:Ski Goggles"
```

방문 페이지 2:

```js
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

결합 이벤트가 발생하지 않는 페이지에서 eVar에 대한 값을 설정하는 경우 또는 결합 이벤트가 없는 제품 문자열에서 eVar 값을 설정하는 경우 "None"으로 할당됩니다.

>[!NOTE]
>
>머천다이징 변수의 인스턴스 계산에 대한 현재 기능은 검토 중이며 향후 릴리스에서 변경될 예정입니다.

