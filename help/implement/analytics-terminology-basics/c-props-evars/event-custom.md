---
description: 사용자 지정 이벤트는 추적하려는 성공 유형을 정의할 수 있도록 해줍니다.
keywords: Analytics 구현; 사용자 지정 이벤트
seo-description: 사용자 지정 이벤트는 추적하려는 성공 유형을 정의할 수 있도록 해줍니다.
seo-title: 사용자 지정 이벤트란 무엇입니까?
solution: Analytics
title: 사용자 지정 이벤트란 무엇입니까?
topic: 개발자 및 구현
uuid: 8 e 78 BA 04-9 B 4 C -4566-980 C-C 24 DD 9 D 82236
translation-type: tm+mt
source-git-commit: d7056c233e784a073c75c55f396ff43c9e0d1c71

---


# 사용자 지정 이벤트란 무엇입니까?

사용자 지정 이벤트는 추적하려는 성공 유형을 정의할 수 있도록 해줍니다.

[!UICONTROL 사용자 지정] 이벤트는 [!UICONTROL 사전 정의된] 이벤트와 유사하긴 하지만, 독자적인 성공 지표를 정의할 수 있도록 해줍니다. For example, if you have a newsletter, your success event could be _Registration_. _등록은_ [!UICONTROL 사전 정의된] 이벤트의 일부가 아닙니다. [!UICONTROL 사용자 지정] 이벤트를 사용하면, 뉴스레터를 등록하는 방문자의 수를 추적할 수 있습니다. [!UICONTROL 사용자 지정] 이벤트는 아래와 같은 표준 구문을 따릅니다.

```js
s.events="event3"
```

위의 코드는 이벤트를 _이벤트_ 변수를 참조하십시오. If you do not modify the event name in the interface, _event3_ would display in the interface.

기본적으로, 성공 이벤트는 _카운터_ 이벤트로 구성됩니다. 카운터 이벤트는 성공 이벤트가 설정되는 횟수를 카운트합니다. 일부 성공 이벤트 사용에서는 이벤트가 사용자 지정 금액만큼 증가해야 합니다. These events can be set either as _numeric_ events or _currency_ events. 관리 콘솔에서 이벤트 유형을 변경할 수 있습니다.
