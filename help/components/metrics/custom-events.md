---
title: 사용자 정의 이벤트
description: 사용자 지정 이벤트가 존재하는 히트의 수입니다.
feature: Metrics
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
TQID: https://experienceleague.adobe.com/1D8ONiUuG3T6DqM7HygbBbf0Y4ja5ej1Hfy8-hKo0yg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 91%

---

# 사용자 정의 이벤트

*이 도움말 페이지에서는 사용자 지정 이벤트가 지표로 작동하는 방식을 설명합니다. 사용자 지정 이벤트가 구현 변수로 작동하는 방법에 대한 자세한 내용은 구현 사용자 안내서의 [이벤트 개요](/help/implement/vars/page-vars/events/events-overview.md)를 참조하십시오.*

사용자 지정 이벤트 [메트릭](overview.md)은(는) 이미지 요청에서 주어진 사용자 지정 이벤트가 설정된 히트의 수를 표시합니다. 이 지표는 각 조직 특유의 이벤트에 대한 인사이트를 제공하므로 많은 구현에서 필수적입니다.

## 이 지표의 계산 방법

사용자 지정 이벤트는 유형에 따라 다르게 계산됩니다. 보고서 세트 설정의 [성공 이벤트](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) 아래에서 이벤트 유형을 확인할 수 있습니다.

* **카운터 이벤트**: 기본 이벤트 설정입니다. 대부분의 이벤트는 카운터 이벤트입니다. [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 일치하는 사용자 지정 이벤트 `event1` - `event1000`이 존재하는 히트의 수를 계산합니다.
* **숫자 이벤트**: `events` 변수의 이벤트에 지정된 숫자 값을 합계합니다.
* **통화 이벤트**: 해당 일의 환율에 대해 통화 전환을 적용한 후 `events` 변수의 각 히트에 지정된 숫자 값을 합계합니다.

사용 가능한 이벤트 수는 조직의 Analytics 계약에 따라 다릅니다. 비 레거시 계약에 있는 대부분의 조직에는 사용할 수 있는 사용자 정의 이벤트 1,000개가 있습니다. 사용 가능한 사용자 정의 이벤트의 수를 모를 경우에는 Adobe 계정 팀에 문의하십시오.

조직의 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에서 각 이벤트를 사용하는 방법을 기록하는 것이 좋습니다.
