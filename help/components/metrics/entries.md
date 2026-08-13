---
title: 항목
description: 방문에서 첫 번째 값의 인스턴스입니다.
feature: Metrics
exl-id: f5d359ce-e6ac-4f80-a30b-ff78cc5fc8dc
TQID: https://experienceleague.adobe.com/H3LE0wm2uDL3-pILbvOXvccAJQdo5o9X3uHJ4xZe7UU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 89%

---

# 항목

*이 도움말 페이지에서는 시작이 지표로서 작동하는 방식을 설명합니다. 시작이 차원으로 작동하는 방법에 대한 자세한 내용은 [시작 차원](../dimensions/entry-dimensions.md)을 참조하십시오.*

시작 [지표](overview.md)은(는) 주어진 차원 항목이 방문에서 첫 번째 값으로 캡처된 횟수를 보여줍니다. 이 지표는 방문자가 사이트에 대해 갖는 첫 번째 노출에 대해 더 알려고 할 때 유용합니다. 차원의 첫 번째 값을 확인하는 것은 새 방문자가 느끼는 경험을 이해하고 최적화하는 데 도움이 될 수 있습니다.

## 이 지표의 계산 방법

주어진 차원에 대해 방문에서 보이는 첫 번째 차원 항목을 시작으로 기록합니다. 방문당 차원당 하나의 시작만 존재합니다. 차원이 처음에 설정되어 있지 않다면 반드시 방문의 첫 번째 히트일 필요는 없습니다. 방문 기반 지표이므로 차원 항목에 연결되면 방문의 나머지 시간 동안 지속됩니다.

>[!TIP]
>
>모든 방문에서 항상 설정되지는 않는 차원에 대해 이 지표를 보는 경우 Analysis Workspace에서 &#39;지정되지 않음&#39; 차원 항목을 숨길 수 있습니다. 필터 아이콘을 클릭한 후, [!UICONTROL 지정되지 않음 (없음) 포함]의 선택을 취소합니다.
