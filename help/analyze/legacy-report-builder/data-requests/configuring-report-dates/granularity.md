---
description: 요청 마법사 1단계에서는 세부 기간 수준을 데이터 요청에 적용할 수 있습니다. 세부기간은 보고서에 포함된 시간 기반 세부 사항의 수준을 지정합니다.
title: 세부 기간
uuid: 948b3ff2-fcff-45fc-9e8c-8a025ac562b1
feature: Report Builder
role: User, Admin
exl-id: 96c3b93a-9adf-4993-b6fc-9146ee5be4bd
TQID: https://experienceleague.adobe.com/26j4Fernl4bfuYeyuVVzw1K5hZvNSD6pDUVOfEc0J8s
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 14%

---

# 세부 기간

{{legacy-arb}}

요청 마법사: 1단계에서 데이터 요청에 세부 기간 수준을 적용할 수 있습니다. 세부기간은 보고서에 포함된 시간 기반 세부 사항의 수준을 지정합니다.

유효한 값은 Hour, Day, Week, Month, Quarter, Year, Aggregated입니다.

## Report Builder가 세부 기간을 처리하는 방법

[!UICONTROL 월] 세부 기간을 가진 월의 날짜 범위를 선택한다고 가정해 봅시다. 요청은 정확히 1개월의 데이터 값을 기반으로 지표에 대한 합계를 보여줍니다. 요청 날짜 범위가 한 분기에 걸쳐 있는 경우 보고서에는 세 가지 그림, 즉 각 달 단위에 대한 하나 또는 그 분수가 표시됩니다. 오늘이 3월 18일인 경우 마지막 분기를 선택하면 1월 1일 - 1월 31일에 대한 숫자 하나와 2월 1일 - 2월 28일에 대한 숫자 하나와 3월 1일 - 3월 17일에 대한 마지막 숫자가 반환됩니다.
