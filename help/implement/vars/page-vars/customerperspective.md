---
title: customerPerspective
description: 앱이 전경에 있는 동안 모바일 앱 히트가 발생했는지 배경에 있는 동안 발생했는지 여부를 지정합니다.
feature: Appmeasurement Implementation
role: Admin, Developer
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 199
ht-degree: 0%

---

# customerPerspective

`customerPerspective` 변수는 모바일 앱 히트가 앱이 전경과 배경 중 발생했는지 여부를 지정합니다. `cp` 쿼리 매개 변수로 Adobe 데이터 수집으로 전송되고 [히트 유형](/help/components/dimensions/hit-type.md) 차원을 채웁니다.

## 유효한 값

`customerPerspective`은(는) 다음 문자열 값을 허용합니다.

* `foreground`: 앱을 활성 상태로 사용하는 동안 히트가 발생했습니다.
* `background`: 위치 업데이트 또는 푸시 알림으로 트리거된 히트와 같이 앱이 백그라운드에서 실행되는 동안 히트가 발생했습니다.

## 이 변수 설정 방법

Adobe Mobile SDK(버전 4.13.6 이상)는 `customerPerspective`을(를) 자동으로 설정합니다. 일반적으로 수동으로 설정하지 않습니다. 브라우저에서 AppMeasurement을 통해 보낸 히트는 항상 `foreground`(으)로 보고됩니다. 변수가 히트에 없으면 해당 히트가 전경 히트로 처리됩니다.

## 보고에 미치는 영향

전경/배경 구분은 방문 처리 방식에 영향을 줍니다.

* 방문은 하나 이상의 전경 히트가 포함된 경우에만 카운트됩니다.
* 배경 히트는 여전히 전환 이벤트로 인한 것일 수 있으며 가상 보고서 세트의 [컨텍스트 인식 세션](/help/components/vrs/vrs-mobile-visit-processing.md)을 통해 분석할 수 있습니다. 이 동작은 푸시 알림의 효과를 측정할 때 유용합니다.
