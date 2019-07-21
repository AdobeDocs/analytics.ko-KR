---
description: 사용자 유형별 경로 세그먼트화는 얼마나 구체적인 사용자 유형이 사이트에서 경로를 이동하는지를 이해하기 위한 일반적인 요청입니다.
keywords: Analytics 구현
seo-description: 사용자 유형별 경로 세그먼트화는 얼마나 구체적인 사용자 유형이 사이트에서 경로를 이동하는지를 이해하기 위한 일반적인 요청입니다.
seo-title: 사용자 유형별 세그먼트 경로
solution: Analytics
title: 사용자 유형별 세그먼트 경로
topic: 개발자 및 구현
uuid: 5 C 298 F 39-381 D -453 B-A 608-109 E 3276 B 361
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 사용자 유형별 세그먼트 경로

사용자 유형별 경로 세그먼트화는 얼마나 구체적인 사용자 유형이 사이트에서 경로를 이동하는지를 이해하기 위한 일반적인 요청입니다.

사용자 유형 및 페이지 이름을 [!UICONTROL sprop]에 연결하고 [!UICONTROL sprop]에서 경로 지정을 활성화할 수 있습니다.

For example, let's say you have two user types: _Registered_ users and _Non-Registered_ users. 각 페이지에서 이 두 사용자 유형을 구별하고 이 값을 지정된 [!UICONTROL sprop]에 삽입해야 합니다. prop을 채우면 아래와 같이 표시됩니다.

```js
 s.prop1=”Registered : “ + s.pageName;
```

사용자가 등록된 사용자이고 홈 페이지를 방문했다면, prop에 있는 값은 다음과 같이 표시됩니다.

```js
 “Registered : Home Page”
```

"Page 2"라는 다른 페이지로 클릭하면, 해당 페이지에 대한 값이 다음과 같이 표시됩니다.

```js
 “Registered : Page 2”
```

[!UICONTROL 경로 지정] 기능이 켜져 있으면, 이 두 값이 연속적으로 표시됩니다. 등록된 사용자가 어떻게 홈 페이지로부터 이동하는지를 알려면, 경로 보고서들 중 하나에서 값 "Registered : Home Page"를 찾고 방문자가 방문한 다음 페이지를 확인합니다. 이 경우 다음으로 이동한 곳은 "Page 2"입니다.
