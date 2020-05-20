---
title: forceOnline
description: AppMeasurement의 온라인 상태를 수동으로 설정합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# forceOnline

`forceOnline()` 메서드를 사용하면 자동으로 감지된 AppMeasurement 상태를 무시할 수 있습니다.

>[!IMPORTANT] [`trackOffline`](../config-vars/trackoffline.md)이 활성화되어 있을 때에만 이 메서드를 사용하십시오. 오프라인 추적의 외부에서 이 함수를 사용하면 데이터가 손실될 수 있습니다.

AppMeasurement는 장치의 온라인 상태를 자동으로 감지합니다. `forceOnline()` 메서드를 사용하여 AppMeasurement가 히트를 장치가 온라인 상태인 것처럼 처리하도록 할 수 있습니다. 이 메서드는 인수를 사용하지 않으며 값을 반환하지 않습니다. AppMeasurement에서 온라인 상태를 무시하는 것이 이 메서드의 유일한 목적입니다.

## Adobe Experience Platform Launch에서 온라인 적용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.forceOnline()

Analytics 개체를 인스턴스화한 후에는 구현의 어느 곳에서든 `s.forceOnline()` 메서드를 호출할 수 있습니다.

```js
s.forceOnline();
```
