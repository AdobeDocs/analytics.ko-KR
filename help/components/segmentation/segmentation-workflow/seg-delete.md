---
description: 세그먼트를 삭제하기 전에 알아야 하는 고려 사항을 이해합니다.
title: 세그먼트 삭제
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
TQID: https://experienceleague.adobe.com/G1gycXvzM-mMdpElmelyD204Ts-C2uua5X4rJMM3JNQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 3%

---

# 세그먼트 삭제

이 문서에는 세그먼트를 삭제하기 전에 알아야 하는 몇 가지 고려 사항이 나와 있습니다.

세그먼트를 삭제할 때:

* 이 세그먼트가 적용된 예약된 보고서 및 대시보드는 정상적으로 계속 작동합니다.
* 예약된 보고서는 같은 이름의 세그먼트를 편집할 때 업데이트되지 않습니다.

<!--

For example: Assume you have 2 segments with the same name in different report suites:

  | Segment name | Report suite |
  |---|---|
  | Visits from California | mainprod |
  | Visits from California | maindev |

  You have a visualization that references the segment for the **[!UICONTROL mainprod]** report suite. Then you delete that segment because the segment is a duplicate. The bookmark will continue to run, referencing the definition of the deleted segment. If you change the segment definition for the remaining segment to include Catalina Island and Tijuana Mexico, the segment applied to the bookmark will not change. The segment will use the old definition. To fix this, update the bookmark to reference the new definition. If you are unsure whether a bookmark, dashboard or scheduled report is using a deleted segment, you could change the name of the remaining segment to indicate whether the bookmark is using the remaining segment.

-->