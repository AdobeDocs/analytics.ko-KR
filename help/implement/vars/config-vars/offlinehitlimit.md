---
title: offlineHitLimit
description: 오프라인 추적을 위해 대기열에 추가할 최대 히트 수를 결정합니다.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# offlineHitLimit

오프라인 추적은 Adobe Analytics에서 데이터를 수집하는 선택적 방법입니다. 방문자가 인터넷에서 연결이 끊겼지만 사이트를 계속 탐색하는 경우 장치가 인터넷에 다시 연결될 때까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대부분 모바일 애플리케이션에 사용됩니다.

이 `offlineHitLimit` 변수는 장치가 로컬로 저장하는 히트 수에 제한을 둡니다. 이 변수는 `trackOffline` 인 경우에만 작동합니다 `true`.

## Adobe Experience Platform 실행의 오프라인 히트 제한

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.offlineHitLimit

이 `s.offlineHitLimit` 변수는 장치가 오프라인일 때 저장하는 최대 히트 수를 나타내는 정수입니다. 이 변수가 정의되지 않은 경우, 오프라인 중에 장치가 저장하는 히트 수에 제한이 없습니다.

```js
s.offlineHitLimit = 100;
```
