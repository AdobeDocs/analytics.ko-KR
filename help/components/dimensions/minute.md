---
title: 분
description: 지표가 발생한 분입니다.
feature: Dimensions
exl-id: 63f13083-321f-4fd8-9352-e413e1ebf168
TQID: https://experienceleague.adobe.com/GRivRprXBteGxRZieSI3uyjHALDJ-0hHbZx3S9ldJW0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 76%

---

# 분

&#39;분&#39; [차원](overview.md)은(는) 주어진 지표가 발생한 분을 보고합니다(내림). 첫 번째 차원 항목은 날짜 범위에서 첫 번째 분이고 마지막 차원 항목은 날짜 범위에서 마지막 분입니다. 이 차원은 시간에 따른 지표를 볼 수 있으므로 트렌드 보고서에 중요합니다. 이 차원이 세분화되어 있는 정도를 고려할 때 보고 날짜 범위를 1일 또는 2일로 제한하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

차원 항목에는 해당 날짜와 함께 보고서의 날짜 범위 내에 지정된 분이 포함됩니다. 형식은 `HH:MM YYYY-MM-DD`를 사용합니다. `00:00`(으)로 시작하는 Dimension 항목은 해당 날짜의 자정과 같고, `23:59`(으)로 시작하는 값은 해당 날짜의 오후 11:59(과)와 같습니다.
