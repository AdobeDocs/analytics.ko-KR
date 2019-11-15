---
description: 사용자 유형별 경로 세그먼트화는 얼마나 구체적인 사용자 유형이 사이트에서 경로를 이동하는지를 이해하기 위한 일반적인 요청입니다.
keywords: Analytics Implementation
solution: Analytics
title: 사용자 유형별 경로 세그먼트화
topic: Developer and implementation
uuid: 5c298f39-381d-453b-a608-109e3276b361
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 사용자 유형별 경로 세그먼트화

사용자 유형별 경로 세그먼트화는 얼마나 구체적인 사용자 유형이 사이트에서 경로를 이동하는지를 이해하기 위한 일반적인 요청입니다.

사용자 유형 및 페이지 이름을 [!UICONTROL sprop]에 연결하고 [!UICONTROL sprop]에서 경로 지정을 활성화할 수 있습니다.

예를 들어 _등록된_ 사용자와 _등록되지 않은_ 사용자, 이렇게 두 가지 사용자 유형이 있다고 할 경우, 각 페이지에서 이 두 사용자 유형을 구별하고 이 값을 지정된 [!UICONTROL sprop]에 삽입해야 합니다. prop을 채우면 아래와 같이 표시됩니다.

```js
 s.prop1="Registered : " + s.pageName;
```

사용자가 등록된 사용자이고 홈 페이지를 방문했다면, prop에 있는 값은 다음과 같이 표시됩니다.

```js
 "Registered : Home Page"
```

"Page 2"라는 다른 페이지로 클릭하면, 해당 페이지에 대한 값이 다음과 같이 표시됩니다.

```js
 "Registered : Page 2"
```

[!UICONTROL 경로 지정] 기능이 켜져 있으면, 이 두 값이 연속적으로 표시됩니다. 등록된 사용자가 어떻게 홈 페이지로부터 이동하는지를 알려면, 경로 보고서들 중 하나에서 값 "Registered : Home Page"를 찾고 방문자가 방문한 다음 페이지를 확인합니다. 이 경우 다음으로 이동한 곳은 "Page 2"입니다.
