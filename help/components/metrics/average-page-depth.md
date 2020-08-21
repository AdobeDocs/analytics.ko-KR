---
title: 평균 페이지 깊이
description: 차원이 존재하는 곳에 들어가는 평균 페이지 수입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 59%

---


# 평균 페이지 깊이

&#39;평균 페이지 깊이&#39; 지표는 주어진 방문에서 차원 항목의 거리를 보여줍니다. 예를 들어, 일반적으로 홈 페이지는 한 방문에서 일반적으로 더 들어가는 구매 확인 페이지보다 더 작은 평균 페이지 깊이를 보여줍니다. 이 지표는 특정 차원 항목의 평균 페이지 수를 이해하려는 경우 유용합니다. 평균 페이지 깊이가 낮은 경우 이 정보를 사용하여 특정 페이지를 신규 방문자에게 최적화할 수 있습니다.

>[팁] 이 지표를 다른 지표(예: [방문 횟수](visits.md))와 함께 사용하면 더 나은 통찰력을 얻을 수 있습니다. 이 지표를 단독으로 사용하는 경우 일반적으로 가치가 없는 예외 항목 페이지 깊이가 포함된 차원 항목을 가져옵니다.

## 이 지표의 계산 방법

방문의 첫 번째 페이지에 대한 페이지 깊이는 `0`입니다. 다음 페이지는 페이지 깊이가 1이며, 방문이 끝날 때까지 각 페이지 보기를 증가시킵니다. 이 지표는 페이지 보기([`t()`](/help/implement/vars/functions/t-method.md)) 호출만 증가시키고 링크 추적([`tl()`](/help/implement/vars/functions/tl-method.md)) 호출은 증가시키지 않습니다.

특정 차원 항목의 경우 해당 차원 항목에 대한 모든 페이지 깊이를 추가하고 방문 수로 나눕니다. 결과 숫자는 가장 가까운 정수로 반올림된 평균 페이지 깊이입니다. Dimension items with an average page depth of `0` means it was frequently on the first page of the visit.

예를 들어 다음 방문 예를 고려해 보십시오.

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

If we wanted average page depth for the dimension item `Page2`, it would be calculated as follows:

```text
If 'Count repeat instances' is enabled:
(1 + 2 + 5) / 3 = 2.67, rounded up to 3

If 'Count repeat instances' is disabled:
(1 + 4) / 2 = 2.5, rounded up to 3
```

>[!TIP]
>
>소수점이 있는 평균 페이지 깊이를 보려면 이 지표를 공식 내의 유일한 요소로 사용하여 계산된 지표를 만드십시오. 계산된 지표의 소수점 자리를 원하는 소수까지 늘립니다.

## 100%를 넘는 백분율

이 지표에는 100%를 넘는 백분율이 자주 포함됩니다. 분모는 전체 차원의 평균 페이지 깊이이며 분자는 차원 항목의 평균 페이지 깊이입니다. 전체 차원의 평균 페이지 깊이가 지정된 차원 항목의 평균 페이지 깊이보다 낮은 경우 백분율이 100%보다 높은 것으로 표시됩니다. 이 지표로 등급 보고서를 정렬하면 일반적으로 중요하지 않은 예외적인 평균 페이지 깊이 값이 표시됩니다. Adobe에서는 등급 보고서에서 [방문 횟수](visits.md)와 같은 다른 지표로 정렬하는 것을 권장합니다.