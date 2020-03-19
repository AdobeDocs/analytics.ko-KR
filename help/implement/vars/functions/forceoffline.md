---
title: forceOffline
description: AppMeasurement의 온라인 상태를 수동으로 설정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# forceOffline

이 `forceOffline()` 방법을 사용하면 자동으로 감지된 AppMeasurement 상태를 재정의할 수 있습니다.

> [!IMPORTANT] 이 기능이 활성화되어 있을 때만 이 함수를 [`trackOffline`](../config-vars/trackoffline.md) 사용합니다. 오프라인 추적 외부에서 이 함수를 사용하면 데이터 손실이 발생할 수 있습니다.

AppMeasurement는 장치의 온라인 상태를 자동으로 감지합니다. 이 `forceOffline()` 방법을 사용하여 AppMeasurement가 히트를 장치가 오프라인 상태인 것처럼 처리하도록 할 수 있습니다. 이 메서드는 인수를 사용하지 않으며 값을 반환하지 않습니다. AppMeasurement의 유일한 목적은 온라인 상태를 무시하는 것입니다.

## Adobe Experience Platform Launch에서 오프라인 활용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.forceOffline()

Analytics 개체를 인스턴스화한 후 구현의 아무 곳에서나 메서드를 호출할 수 있습니다. `s.forceOffline()`

```js
s.forceOffline();
```
