---
title: 다시 로드
description: 페이지를 다시 로드한 횟수입니다.
feature: Metrics
exl-id: 9539a733-9e9f-48b3-b8ab-8d969de27f87
TQID: https://experienceleague.adobe.com/Jhm8-usZH-SLOzUvNIC3hdoKDMkm9T5mnCUeeMRga7E
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 21%

---

# 다시 로드

&#39;다시 로드&#39; [지표](overview.md)은(는) 다시 로드 중 차원 항목이 있었던 횟수를 보여줍니다. 방문자가 브라우저를 새로 고치는 것이 다시 로드를 트리거하는 가장 일반적인 방법입니다.

## 이 지표의 계산 방법

이 지표는 [Page](../dimensions/page.md) 차원에 이전 히트와 동일한 값이 있는 히트의 수를 계산합니다.

재로드 개념은 보고에 사용하는 차원에 관계없이 페이지 차원에 적용됩니다. 예를 들어 [eVar1](../dimensions/evar.md)을(를) 차원으로 사용하고 지표로 다시 로드하는 경우 테이블은 다시 로드 중 각 eVar 값이 있었던 횟수를 보여줍니다(연속된 두 페이지 값). 두 개의 연속 eVar1 값이 있었던 횟수를 보여 주지 않습니다.
