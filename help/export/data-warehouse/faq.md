---
title: Data Warehouse FAQ
description: Data Warehouse에 대한 FAQ
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---


# Data Warehouse FAQ

Data Warehouse에 대한 FAQ

## 요청을 만드는 동안 세부기간 드롭다운을 사용할 때 날짜는 어떤 형식으로 제공됩니까?

Data Warehouse 요청에서 세부기간을 적용할 때 &#39;날짜&#39; 열이 보고서에 추가됩니다. 선택한 세부기간에 따라 날짜 형식이 변경됩니다.

| 세부기간 | 형식 | 예 |
| --- | --- | --- |
| 시간별 | `mmmm d, yyyy` 시간 `H` | 1월 1일, 20XX, 시간 0 |
| 일별 | `mmmm d, yyyy` | 1월 1일 20XX |
| 주별 | 주 `w, yyyy` | 1주차, 20XX |
| 월별 | `mmmm yyyy` | 1월 20일 XX |
| 분기별 | `q` 분기 `yyyy` | 1분기 20XX |
| 연간 | `yyyy` | 20XX |

## 차원으로서의 세그먼트는 Data Warehouse에서 어떻게 작동합니까?

Data Warehouse에서 세그먼트를 차원으로 사용할 경우 보고서는 `"0"` 또는 다음을 포함하는 열을 반환합니다 `"1"`.

* **`"0"`**:차원 항목이 세그먼트의 기준을 충족하지 않았습니다.
* **`"1"`**:차원 항목이 세그먼트의 기준을 충족했습니다.
