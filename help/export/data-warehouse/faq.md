---
title: Data Warehouse FAQ
description: Data Warehouse에 대해 자주 묻는 질문.
feature: Data Warehouse
exl-id: 51c3ba17-a8b2-4030-9521-355ebbbfcd0d
source-git-commit: 78cfb1f3c4d45fc983982a8da11b66f2b2c9ecbc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 84%

---

# Data Warehouse FAQ

Data Warehouse에 대해 자주 묻는 질문.

## 요청을 생성하는 동안 세부 기간 드롭다운 목록을 사용할 때 날짜는 어떤 형식이어야 합니까?

Data Warehouse 요청에 세부 기간을 적용하면 “날짜” 열이 보고서에 추가됩니다. 선택한 세부 기간에 따라 날짜 형식이 변경됩니다.

| 세부기간 | 형식 | 예 |
| --- | --- | --- |
| 시간별 | `mmmm d, yyyy` 시간 `H` | 20XX년 1월 1일, 시간 0 |
| 일별 | `mmmm d, yyyy` | 20XX년 1월 1일 |
| 주별 | 주 `w, yyyy` | 20XX년 1주차 |
| 월별 | `mmmm yyyy` | 20XX년 1월 |
| 분기별 | `q` 분기 `yyyy` | 20XX년 1분기 |
| 연간 | `yyyy` | 20XX |

## Data Warehouse에서 차원으로서의 세그먼트는 어떻게 작동합니까?

Data Warehouse에서 세그먼트를 차원으로 사용하면 보고서는 `"0"` 또는 `"1"`가 포함된 열을 반환합니다.

* **`"0"`**: 차원 항목이 세그먼트의 기준을 충족하지 않았습니다.
* **`"1"`**: 차원 항목이 세그먼트의 기준을 충족했습니다.
