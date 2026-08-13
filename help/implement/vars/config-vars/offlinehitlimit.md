---
title: offlineHitLimit
description: 오프라인 추적을 위해 큐에 추가할 최대 히트 수를 결정합니다.
feature: Appmeasurement Implementation
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/YaAPaPRLQ7YYxARVRBuxB1J25qeS8JTPbIO1Bj725YM'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 39%

---

# offlineHitLimit

오프라인 추적은 Adobe Analytics에서 데이터를 수집할 때 선택할 수 있는 방법입니다. 방문자가 인터넷 연결이 끊겼지만 사이트를 계속 탐색하는 경우 장치가 인터넷에 다시 연결될 때까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대개 모바일 애플리케이션에 사용됩니다.

`offlineHitLimit` 변수는 디바이스가 로컬로 저장하는 히트의 수에 제한을 둡니다. 이 변수는 [`trackOffline`](trackoffline.md)이 활성화된 경우에만 작동합니다.

## 웹 SDK을 사용한 오프라인 히트 제한

웹 SDK은 오프라인 추적을 지원하지 않습니다.

## Adobe Analytics 확장을 사용한 오프라인 히트 제한

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.offlineHitLimit

`s.offlineHitLimit` 변수는 장치가 오프라인일 때 저장하는 최대 히트 수를 나타내는 정수입니다. 이 변수가 정의되지 않으면 기본값은 `10`입니다. 어떤 정수 값으로든 설정할 수 있습니다. 높은 값을 설정할 때는 방문자 브라우저의 로컬 저장소 상한을 고려해야 합니다. 이 제한은 일반적으로 5~10MB입니다.

```js
s.offlineHitLimit = 100;
```
