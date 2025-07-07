---
description: 세그먼트를 삭제하기 전에 알아야 하는 고려 사항을 이해합니다.
title: 세그먼트 삭제
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '63'
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