---
title: 날짜 (월 기준)
description: 월에 상관없이 그 월의 숫자 일입니다.
feature: Dimensions
exl-id: 6d27aa9f-ce75-4a27-bb92-3acabe3975a1
TQID: https://experienceleague.adobe.com/jSrKlf4a5f-6MTrQwwUcvRJep4chAUyOsj5hFjE1HRg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 87%

---

# 날짜 (월 기준)

일&#39; [차원](overview.md)은(는) 주어진 월의 숫자 일을 차원 항목으로 보고합니다. 예를 들어, 1월 1일 - 3월 31일 범위의 보고서가 있을 경우, 각 달의 1일은 동일한 차원 항목으로 그룹화됩니다. 이 보고서는 일별로 구분된 보고서가 필요하지만 차원 항목으로 정적 날짜를 원하지 않는 경우 유용합니다. 이 차원은 선택한 날짜 범위에 실행되므로 특히나 예약된 보고서에서 차원으로서 중요합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

차원 항목에는 히트가 발생한 월의 일을 나타내는 숫자 `1` - `31`이 포함됩니다.
