---
title: 방문당 평균 페이지 조회수
description: 주어진 차원 항목이 방문에서 나타난 평균 횟수입니다.
feature: Metrics
exl-id: fef6e803-e819-4f0f-8cb0-c565328a8bea
TQID: https://experienceleague.adobe.com/sospsPhk77O5qOLcMLmu7gB7rvlxbp8rGqB39LCnQ5g
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 92%

---

# 방문당 평균 페이지 조회수

방문당 평균 페이지 보기 수 차원은 원하는 차원에 대해 평균적으로 발생한 페이지 보기 수를 보여줍니다. 시간 기반 차원의 경우 시간 경과에 따른 방문 트렌드 내 평균 페이지 보기 수를 확인할 수 있습니다. 이 [지표](overview.md)은(는) 방문에서 차원 항목이 표시되는 빈도를 이해하려 할 때 유용합니다.

>[!TIP]
>
>이 지표를 다른 지표 (예 [방문 횟수](visits.md))와 함께 사용하면 더 나은 인사이트를 얻을 수 있습니다. 이 지표를 단독으로 사용하는 경우 일반적으로 중요하지 않은 예외적인 방문당 페이지 보기 수를 포함하는 차원 항목을 얻습니다.

## 이 지표의 계산 방법

이 지표는 공식 [`Page views`](page-views.md)` divided by `[`Visits`](visits.md)을 사용하여 계산됩니다.

## 100%를 넘는 백분율

이 지표에는 100%를 넘는 백분율이 자주 포함됩니다. 분모는 전체 차원의 방문당 평균 페이지 보기 수이고 분자는 차원 항목의 방문당 평균 페이지 보기 수입니다. 전체 차원의 방문당 평균 페이지 보기 수가 주어진 차원 항목의 방문당 평균 페이지 보기 수보다 낮은 경우 백분율이 100%보다 높게 표시됩니다. 이 지표로 등급 보고서를 정렬하면 예외적인 방문당 평균 페이지 보기 수 값이 표시되는데, 이것은 일반적으로 중요하지 않습니다. Adobe에서는 등급 보고서에서 [방문 횟수](visits.md)와 같은 다른 지표로 정렬하는 것을 권장합니다.
