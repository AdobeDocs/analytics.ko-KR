---
title: 사용자 지정 이벤트
description: 사용자 지정 이벤트가 존재하는 히트의 수입니다.
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '221'
ht-degree: 100%

---

# 사용자 지정 이벤트

*이 도움말 페이지에서는 사용자 지정 이벤트가 지표로 작동하는 방식을 설명합니다. 사용자 지정 이벤트가 구현 변수로 작동하는 방법에 대한 자세한 내용은 구현 사용자 안내서의 [이벤트 개요](/help/implement/vars/page-vars/events/events-overview.md)를 참조하십시오.*

사용자 지정 이벤트 지표는 이미지 요청에서 주어진 사용자 지정 이벤트가 설정된 히트의 수를 보여줍니다. 이 지표는 각 조직 특유의 이벤트에 대한 통찰력을 제공하므로 많은 구현에서 필수적입니다.

## 이 지표의 계산 방법

사용자 지정 이벤트는 유형에 따라 다르게 계산됩니다. 보고서 세트 설정의 [성공 이벤트](../../admin/admin/c-success-events/success-event.md) 아래에서 이벤트 유형을 확인할 수 있습니다.

* **카운터 이벤트**: 기본 이벤트 설정입니다. 대부분의 이벤트는 카운터 이벤트입니다. [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 일치하는 사용자 지정 이벤트 `event1` - `event1000`이 존재하는 히트의 수를 계산합니다.
* **숫자 이벤트**: `events` 변수의 이벤트에 지정된 숫자 값을 합계합니다.
* **통화 이벤트**: 해당 일의 환율에 대해 통화 전환을 적용한 후 `events` 변수의 각 히트에 지정된 숫자 값을 합계합니다.

사용 가능한 이벤트 수는 조직의 Analytics 계약에 따라 다릅니다. 비 레거시 계약에 있는 대부분의 조직에는 사용할 수 있는 사용자 지정 이벤트 1,000개가 있습니다. 사용 가능한 사용자 지정 이벤트의 수를 모를 경우에는 조직의 계정 관리자에게 문의하십시오.

조직의 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에서 각 이벤트를 사용하는 방법을 기록하는 것이 좋습니다.
