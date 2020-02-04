---
title: offlineThrottleDelay
description: 장치가 다시 온라인으로 돌아올 때 히트 빈도를 설정합니다.
translation-type: tm+mt
source-git-commit: f313fd0c9ffda054a18ad1d457a74602b08e51fa

---


# offlineThrottleDelay

오프라인 추적은 Adobe Analytics에서 데이터를 수집하는 선택적 방법입니다. 방문자가 인터넷에서 연결이 끊겼지만 사이트를 계속 탐색하는 경우 장치가 인터넷에 다시 연결될 때까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대부분 모바일 애플리케이션에 사용됩니다.

장치가 다시 온라인으로 돌아오면 장치에 저장된 모든 히트가 Adobe 데이터 수집 서버로 전송됩니다. 대기 중인 히트 수가 많으면 이전 장치의 성능에 영향을 줄 수 있습니다. 이 `offlineThrottleDelay` 변수를 사용하여 대기 중인 히트가 Adobe로 전송되는 빈도를 설정합니다.

## Adobe Experience Platform 실행의 오프라인 스로틀 지연

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.offlineThrottleDelay in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.offlineThrottleDelay` 변수는 대기 중인 히트 전송 사이에 AppMeasurement 대기 시간(밀리초)을 나타내는 정수입니다. 기본값은 `0`입니다. 즉, 큐에 있는 모든 히트가 한 번에 전송됩니다. 이 `trackOffline` 경우 이 `false`변수는 아무 작업도 하지 않습니다.

```js
s.offlineThrottleDelay = 500;
```
