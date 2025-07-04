---
description: 세그먼트를 삭제하기 전에 알아야 하는 몇 가지 고려 사항을 표시합니다.
title: 세그먼트 삭제
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 39%

---

# 세그먼트 삭제

이 문서에는 세그먼트를 삭제하기 전에 알아야 하는 몇 가지 고려 사항이 나와 있습니다.

세그먼트를 삭제할 때:

* 이 세그먼트가 적용된 예약된 보고서 및 대시보드는 정상적으로 계속 작동합니다. 예를 들어 세그먼트 또는 대시보드는 삭제된 세그먼트를 계속 사용합니다.
* 예약된 보고서는 같은 이름의 세그먼트를 편집해도 업데이트되지 않습니다. 다음은 예제입니다. 서로 다른 보고서 세트에 이름이 같은 세그먼트가 2개 있다고 가정해 보겠습니다.

  | 세그먼트 이름 | 보고서 세트 |
  |---|---|
  | 캘리포니아 방문 횟수 | mainprod |
  | 캘리포니아 방문 횟수 | maindev |

  [!UICONTROL mainprod] 보고서 세트에 대한 세그먼트를 참조하는 책갈피가 있습니다. 그런 다음 세그먼트가 중복되어 있으므로 해당 세그먼트를 삭제합니다. 책갈피는 계속 실행되며 삭제된 세그먼트의 정의를 참조합니다. 남은 세그먼트에 대한 세그먼트 정의를 Catalina Island 및 Tijuana Mexico를 포함하도록 변경해도 해당 책갈피에 적용된 세그먼트는 변경되지 않습니다. 세그먼트는 이전 정의를 사용합니다. 이 문제를 해결하려면 새 정의를 참조하도록 책갈피를 업데이트합니다. 책갈피, 대시보드 또는 예약된 보고서가 삭제된 세그먼트를 사용하는지 확실하지 않은 경우 나머지 세그먼트의 이름을 변경하여 책갈피에 나머지 세그먼트가 사용되고 있는지 여부를 나타낼 수 있습니다.
