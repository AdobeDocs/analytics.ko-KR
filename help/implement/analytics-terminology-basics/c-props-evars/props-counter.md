---
description: 카운터는 특정 이벤트나 프로세스가 발생한 횟수를 저장(및 때로 표시)합니다.
keywords: Analytics Implementation;props;s.prop;custom traffic;counters
solution: Analytics
title: prop을 카운터로 사용
topic: Developer and implementation
uuid: ab83bd7e-10d9-49f9-b9e7-c50397e95c17
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# prop을 카운터로 사용

카운터는 특정 이벤트나 프로세스가 발생한 횟수를 저장(및 때로 표시)합니다.

prop을 사용하여 이벤트가 발생하는 횟수를 셀 수 있습니다. 예를 들어 사이트에서 Real Player와 Windows Media Player의 사용을 추적할 수 있습니다. 각 페이지에는 [!UICONTROL 붙여넣을 코드]가 들어 있으며, 여기에서 [!UICONTROL s.prop] 변수를 볼 수 있습니다. [!UICONTROL s.prop] 1을 사용하여 플레이어를 추적하십시오. 페이지 A의 경우, [!UICONTROL s.prop]1에 값을 입력하여 Real Player를 표시합니다.

```js
s.prop1="RealPlayer"
```

페이지 B의 경우, 아래에서 보듯이 Windows Media Player에 대해 [!UICONTROL s.prop]1에 유사한 값을 입력합니다.

```js
s.prop1="WindowsMP"
```

> [!NOTE] Adobe에서는 사용할 수 있는 [!UICONTROL s.prop] 변수를 최대 75개까지 제공합니다.

방문자가 사이트에 와서 Real Player나 Windows Media Player가 들어 있는 페이지를 방문하면, [!DNL Analytics]는 사용자가 방문한 페이지들을 기반으로 사용자를 세그먼트화할 수 있습니다. 그러면 [!UICONTROL 사용자 지정 트래픽] 보고서에 각 페이지에 대한 방문 횟수가 표시됩니다.

> [!NOTE][!UICONTROL  사용자 지정 트래픽] 보고서의 이름은 사용자 지정할 수 있습니다. 예를 들어 [!UICONTROL 사용자 지정 트래픽] 보고서의 이름은 "플레이어 유형 보고서"로 변경할 수 있습니다.

