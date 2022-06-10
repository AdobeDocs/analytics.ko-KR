---
title: offlineThrottleDelay
description: 디바이스가 다시 온라인으로 돌아올 때의 히트 빈도를 설정합니다.
feature: Variables
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 81%

---

# offlineThrottleDelay

오프라인 추적은 Adobe Analytics에서 데이터를 수집할 때 선택할 수 있는 방법입니다. 방문자가 인터넷 연결이 끊겼지만 사이트를 계속 탐색하는 경우 디바이스가 인터넷에 다시 연결되기 전까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대개 모바일 애플리케이션에 사용됩니다.

디바이스가 다시 온라인으로 돌아오면 디바이스에 저장된 모든 히트는 Adobe 데이터 수집 서버로 전송됩니다. 큐에 있는 히트 수가 많으면 이전 디바이스의 성능에 영향을 줄 수 있습니다. 큐에 있는 히트가 Adobe에 전송되는 빈도를 설정하려면 `offlineThrottleDelay` 변수를 사용하십시오.

## Adobe Analytics 확장을 사용한 오프라인 스로틀 지연

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.offlineThrottleDelay

`s.offlineThrottleDelay` 변수는 전송 큐에 있는 히트와 히트 사이에 AppMeasurement가 대기하는 시간 (밀리초)을 나타내는 정수입니다. 기본값은 `0`입니다. 이것은 큐에 있는 모든 히트가 한 번에 전송됨을 의미합니다. `trackOffline`이 `false`경우 이 변수는 아무 작업도 하지 않습니다.

```js
s.offlineThrottleDelay = 500;
```
