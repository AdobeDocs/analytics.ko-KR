---
title: trackOffline
description: AppMeasurement가 데이터를 수집하는 방법을 변경하는 오프라인 추적을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackOffline

오프라인 추적은 Adobe Analytics에서 데이터를 수집하는 선택적 방법입니다. 방문자가 인터넷에서 연결이 끊겼지만 사이트를 계속 탐색하는 경우 장치가 인터넷에 다시 연결될 때까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대부분 모바일 애플리케이션에 사용됩니다.

이 `trackOffline` 변수는 구현에서 오프라인 추적을 사용할지 여부를 결정합니다.

> [!IMPORTANT] 이 변수를 활성화하기 전에 타임스탬프가 지정된 히트를 허용하도록 보고서 세트를 구성해야 합니다. 보고서 세트에서 타임스탬프가 지정된 히트를 허용하지 않고 이 변수를 활성화하면 데이터가 손실되어 복구할 수 없습니다.

활성화되면 AppMeasurement는 다음 프로세스를 사용하여 데이터를 Adobe로 전송합니다.

* 이미지 요청을 컴파일할 때 타임스탬프 쿼리 문자열 매개 변수가 포함됩니다.
* 장치가 Adobe 데이터 수집 서버에 도달할 수 없는 경우 히트는 장치에 로컬로 저장됩니다.
* 이후 각 히트 동안 AppMeasurement는 이미지 요청을 Adobe에 전송하려고 시도합니다.
   * Adobe 데이터 수집 서버에 연결할 수 없는 경우 히트가 장치의 큐에 추가됩니다.
   * Adobe 데이터 수집 서버에 도달할 수 있는 경우 장치가 오프라인일 때 히트 및 히트 큐가 전송됩니다.

## Adobe Experience Platform Launch에서 오프라인 추적

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.trackOffline in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.trackOffline` 변수는 오프라인 추적을 활성화하거나 비활성화하는 부울입니다. Its default value is `false`. 오프라인 추적을 활성화하려면 이 값을 `true` 설정합니다.

```js
s.trackOffline = true;
```
