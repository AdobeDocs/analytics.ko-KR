---
description: 머천다이징 변수에서 인스턴스가 카운팅되는 방식을 설명합니다.
keywords: Analytics Implementation
title: 머천다이징 변수의 인스턴스
topic: Developer and implementation
uuid: 4cdfd53e-88aa-48cf-a135-98f7fc8dcece
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 머천다이징 변수의 인스턴스

머천다이징 변수에서 인스턴스가 카운팅되는 방식을 설명합니다.

머천다이징 변수에는 현재 인스턴스가 지원되지 않습니다. 머천다이징 변수가 포함된 보고서의 인스턴스가 발견되면, eVar가 제품 문자열 외부의 일부 위치에 설정되고 있으며, 선택한 머천다이징 변수에 대한 실제 인스턴스 수로 간주되어서는 안 됩니다.

전환 변수 구문을 사용하는 경우 변수가 설정될 때마다 인스턴스가 카운트됩니다. 그러나 변수가 설정될 때마다 다음이 발생하지 않는 한 인스턴스는 &quot;None&quot;으로 설정됩니다.

* 바인딩 이벤트가 설정되었습니다.
* products 변수가 설정되었습니다.
* 머천다이징 eVar에 값이 있습니다.

예를 들어 다음 eVar1 인스턴스가 &quot;Outdoors:Ski Goggles&quot;에 할당됩니다.

```js
s.eVar1="Outdoors:Ski Goggles" 
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

그러나 다음 예제에서는 eVar가 설정될 때 모든 조건이 충족되지 않으므로 eVar1의 인스턴스가 &quot;없음&quot;으로 할당됩니다(결합 이벤트가 없고 제품 변수가 설정되지 않음).

방문의 페이지 1:

```js
s.eVar1="Outdoors:Ski Goggles"
```

방문의 2페이지:

```js
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

결합 이벤트가 발생하지 않는 페이지에서 eVar에 대한 값을 설정하거나 결합 이벤트가 없는 제품 문자열에서 eVar 값을 설정하는 경우 &quot;없음&quot;으로 할당됩니다.

>[!NOTE] 머천다이징 변수에서의 인스턴스 카운팅을 위한 현재 기능은 검토 중이며 향후 릴리스에서 변경될 예정입니다.

