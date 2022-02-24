---
title: forceOffline
description: AppMeasurement의 온라인 상태를 수동으로 설정합니다.
feature: Variables
exl-id: 2e48bdf6-7de7-4976-86dd-ef3d558769c7
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '141'
ht-degree: 100%

---

# forceOffline

`forceOffline()` 메서드를 사용하면 자동으로 감지된 AppMeasurement 상태를 무시할 수 있습니다.

>[!IMPORTANT]
>
>[`trackOffline`](../config-vars/trackoffline.md)이 활성화되어 있을 때에만 이 함수를 사용하십시오. 오프라인 추적의 외부에서 이 함수를 사용하면 데이터가 손실될 수 있습니다.

AppMeasurement는 디바이스의 온라인 상태를 자동으로 감지합니다. `forceOffline()` 메서드를 사용하여 AppMeasurement가 히트를 디바이스가 오프라인 상태인 것처럼 처리하도록 할 수 있습니다. 이 메서드는 인수를 사용하지 않으며 값을 반환하지 않습니다. AppMeasurement에서 온라인 상태를 무시하는 것이 이 메서드의 유일한 목적입니다.

## Adobe Experience Platform의 태그를 사용하여 오프라인 강제

데이터 수집 UI에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 사용자 지정 코드 편집기의 s.forceOffline()

Analytics 개체를 인스턴스화한 후에는 구현의 어느 곳에서든 `s.forceOffline()` 메서드를 호출할 수 있습니다.

```js
s.forceOffline();
```
