---
title: 평균 페이지 깊이
description: 차원이 존재하는 곳에 들어가는 평균 페이지 수입니다.
feature: Metrics
exl-id: 6625405a-bda5-4723-8d22-4bc5b7e44d4e
TQID: https://experienceleague.adobe.com/Pm2WxRPqn9M-7IdrFQ2Tkj9t-L8ug3nZGr6ncpZg7lg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 365
ht-degree: 55%

---

# 평균 페이지 깊이

&#39;평균 페이지 깊이&#39; [지표](overview.md)은(는) 차원 항목이 평균적으로 주어진 방문으로 확장되는 정도를 보여줍니다. 예를 들어, 홈 페이지(페이지 차원에 대한 차원 항목)는 일반적으로 구매 확인 페이지보다 작은 평균 페이지 깊이를 보여주며, 이는 방문으로 더 확장될 수 있습니다. 평균 페이지 깊이가 낮은 경우 이 정보를 사용하여 특정 페이지를 신규 방문자에게 최적화할 수 있습니다.

>[!TIP]
>
>이 지표를 [방문 횟수](visits.md)와 같은 다른 지표와 함께 사용하면 더 나은 통찰력을 얻을 수 있습니다. 이 지표를 단독으로 사용하는 경우 일반적으로 귀중한 insight이 아닌 이례적인 페이지 깊이를 포함하는 차원 항목을 가져올 수 있습니다.

## 이 지표의 계산 방법

방문의 첫 번째 페이지에 대한 페이지 깊이는 `0`입니다. 다음 페이지는 페이지 깊이가 1이며, 방문이 끝날 때까지 각 페이지 보기를 증가시킵니다. 이 지표는 페이지 보기([`t()`](/help/implement/vars/functions/t-method.md)) 호출에서만 증가하고 링크 추적([`tl()`](/help/implement/vars/functions/tl-method.md)) 호출에서는 증가하지 않습니다.

주어진 차원 항목에 대해 해당 차원 항목에 대한 모든 페이지 깊이를 추가하고 방문 수로 나눕니다. 결과 숫자는 가장 가까운 정수로 반올림된 평균 페이지 깊이입니다. 평균 페이지 깊이가 `0`인 차원 항목은 해당 차원이 흔히 방문의 첫 페이지에 있었음을 의미합니다.

예를 들어 다음 방문 예를 고려해 보십시오.

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

차원 항목 `Page2`에 대한 평균 페이지 깊이가 필요한 경우 다음과 같이 계산됩니다.

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

이 지표에는 100%를 넘는 백분율이 자주 포함됩니다. 분모는 전체 차원의 평균 페이지 깊이이고 분자는 차원 항목의 평균 페이지 깊이입니다.

전체 차원의 평균 페이지 깊이가 주어진 차원 항목의 평균 페이지 깊이보다 낮은 경우 백분율이 100%를 넘게 됩니다. 이 지표로 등급 보고서를 정렬하면 일반적으로 중요하지 않은 예외적인 평균 페이지 깊이 값이 표시됩니다. Adobe에서는 등급 보고서에서 [방문 횟수](visits.md)와 같은 다른 지표로 정렬하는 것을 권장합니다.
