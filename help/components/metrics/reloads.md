---
title: 다시 로드
description: 페이지를 다시 로드한 횟수입니다.
feature: Metrics
exl-id: 9539a733-9e9f-48b3-b8ab-8d969de27f87
source-git-commit: c9b7c32adfb44a04ab792d12ca049106b3009710
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 21%

---

# 다시 로드

&#39;다시 로드&#39; [지표](overview.md)은(는) 다시 로드 중 차원 항목이 있었던 횟수를 보여줍니다. 방문자가 브라우저를 새로 고치는 것이 다시 로드를 트리거하는 가장 일반적인 방법입니다.

## 이 지표의 계산 방법

이 지표는 [Page](../dimensions/page.md) 차원에 이전 히트와 동일한 값이 있는 히트의 수를 계산합니다.

재로드 개념은 보고에 사용하는 차원에 관계없이 페이지 차원에 적용됩니다. 예를 들어 [eVar1](../dimensions/evar.md)을(를) 차원으로 사용하고 지표로 다시 로드하는 경우 테이블은 다시 로드 중 각 eVar 값이 있었던 횟수를 보여줍니다(연속된 두 페이지 값). 두 개의 연속 eVar1 값이 있었던 횟수를 보여 주지 않습니다.
