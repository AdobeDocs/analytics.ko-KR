---
title: offlineHitLimit
description: 오프라인 추적을 위해 큐에 추가할 최대 히트 수를 결정합니다.
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 84%

---

# offlineHitLimit

오프라인 추적은 Adobe Analytics에서 데이터를 수집할 때 선택할 수 있는 방법입니다. 방문자가 인터넷 연결이 끊겼지만 사이트를 계속 탐색하는 경우 장치가 인터넷에 다시 연결되기 전까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대개 모바일 애플리케이션에 사용됩니다.

`offlineHitLimit` 변수는 장치가 로컬로 저장하는 히트의 수에 제한을 둡니다. 이 변수는 [`trackOffline`](trackoffline.md)이 활성화된 경우에만 작동합니다.

## Adobe Experience Platform에서 태그를 사용한 오프라인 히트 제한

데이터 수집 UI에 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 사용자 지정 코드 편집기의 s.offlineHitLimit

`s.offlineHitLimit` 변수는 장치가 오프라인일 때 저장하는 최대 히트 수를 나타내는 정수입니다. 이 변수가 정의되지 않으면 오프라인 중에 장치가 저장하는 히트 수에 제한이 없습니다.

```js
s.offlineHitLimit = 100;
```
