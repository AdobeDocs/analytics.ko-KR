---
title: forceOnline
description: AppMeasurement의 온라인 상태를 수동으로 설정합니다.
feature: Appmeasurement Implementation
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/qPSlGDmNTccOtGRvlu-xr-wf1hV18OA-yyiuScnZr7g'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 80%

---

# forceOnline

`forceOnline()` 메서드를 사용하면 자동으로 감지된 AppMeasurement 상태를 무시할 수 있습니다.

>[!WARNING]
>
>[`trackOffline`](../config-vars/trackoffline.md)이 활성화되어 있을 때에만 이 메서드를 사용하십시오. 오프라인 추적의 외부에서 이 함수를 사용하면 데이터가 손실될 수 있습니다.

AppMeasurement는 디바이스의 온라인 상태를 자동으로 감지합니다. `forceOnline()` 메서드를 사용하여 AppMeasurement가 히트를 디바이스가 온라인 상태인 것처럼 처리하도록 할 수 있습니다. 이 메서드는 인수를 사용하지 않으며 값을 반환하지 않습니다. AppMeasurement에서 온라인 상태를 무시하는 것이 이 메서드의 유일한 목적입니다.

## 웹 SDK을 사용하여 온라인 강제 실행

웹 SDK은 오프라인 추적을 지원하지 않습니다.

## Adobe Analytics 확장을 사용하여 온라인 강제 실행

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.forceOnline()

Analytics 개체를 인스턴스화한 후에는 구현의 어느 곳에서든 `s.forceOnline()` 메서드를 호출할 수 있습니다.

```js
s.forceOnline();
```
