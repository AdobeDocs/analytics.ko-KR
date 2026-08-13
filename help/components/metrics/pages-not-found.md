---
title: 페이지를 찾을 수 없음 (지표)
description: 오류가 포함된 히트의 수입니다.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
TQID: https://experienceleague.adobe.com/V5jVT8wh71qMrchQmmM6c4EMofHPUEI388TmAf7Zf6M
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 38%

---

# 페이지를 찾을 수 없음

*이 도움말 페이지에서는 &#39;페이지를 찾을 수 없음&#39;이 지표로 작동하는 방식을 설명합니다. 차원으로 작동하는 방법에 대한 자세한 내용은 [페이지를 찾을 수 없음](../dimensions/pages-not-found.md) 차원 페이지를 참조하십시오.*

&#39;페이지를 찾을 수 없음&#39; [지표](overview.md)은(는) 방문자에게 오류가 발생한 시점에 차원이 설정되었거나 지속된 히트 수를 보여줍니다. 이 지표는 오류 메시지(예: 404)가 포함된 페이지 또는 URL을 확인하려는 경우 유용합니다. 그런 다음 이 정보를 웹 개발 팀에 전달하여 오류의 원인을 파악하고 수정할 수 있습니다.

## 이 지표의 계산 방법

이 지표는 [`pageType`](/help/implement/vars/page-vars/pagetype.md) 변수가 `"errorPage"`의 값과 같은 모든 히트를 계산합니다. [페이지를 찾을 수 없음](../dimensions/pages-not-found.md) 차원에 해당하는 지표입니다.
