---
description: 채널에 비용 및 예산 금액을 할당하는 방법을 살펴볼 수 있습니다.
seo-description: 채널에 비용 및 예산 금액을 할당하는 방법을 살펴볼 수 있습니다.
seo-title: 비용 및 예산
solution: Analytics
subtopic: 마케팅 채널
title: 비용 및 예산
topic: Reports & Analytics
uuid: 7 BA 0 E 968-E 565-4 D 4 C -8 FC 0-39 BF 25 D 3 E 5 B 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 비용 및 예산

채널에 비용 및 예산 금액을 할당하는 방법을 살펴볼 수 있습니다.

## Costs and budgets {#topic_7CCFD3B54440433FBA0E4EE127F58B0C}

채널에 비용 및 예산 금액을 할당하는 방법을 살펴볼 수 있습니다.

비용은 채널에서 지출한 것을 나타냅니다. 예산은 지출 가능한 금액을 나타냅니다.

ROI를 확인하는 유용한 방법은 매출에서 비용을 뺀 값을 보여주는 계산된 지표 또는 새 유도당 비용 분류와 함께 총 비용을 보여주는 계산된 지표를 만드는 것입니다. 예를 들어 새 유도를 보여주는 [!UICONTROL 첫 번째 접촉 채널] 보고서를 실행한 다음 계산된 지표를 만들어 새 유도당 비용을 보여주는 첫 번째 접촉 비용 지표를 추가할 수 있습니다.

자세한 내용은 [계산된 지표는 마케팅 채널 보고서를 사용했습니다](../../components/c-marketing-channels/c-channel-calc-metrics.md#topic_4521D324A79E43EF99E69FCDE1E92F74).

채널에만 비용과 예산을 할당할 수 있습니다. 모든 비용은 보고 시 적용되는 시간대를 기준으로 합니다. 비용이 채널과 직접적인 연관이 있는 경우, 채널 내 캠페인들 간에 비용이 분류되는 방법을 보여주는 할당 지표가 선택됩니다.

비용과 예산 항목을 추가한 후 테이블 데이터를 CSV 파일로 내보낼 수 있습니다. 또한 CSV 파일을 마케팅 채널 비용 페이지로 가져올 수 있습니다.

## 비용 및 예산 항목 추가 {#task_9238A033994440748960DE21593E6388}

마케팅 채널에 비용과 예산 항목을 추가합니다.

1. **[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리]** &gt; **[!UICONTROL 보고서 세트를 클릭합니다]**.
1. [!UICONTROL 보고서 세트 관리자 페이지에서 보고서 세트를 선택합니다.]
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Marketing Channels]** &gt; **[!UICONTROL Marketing Channel Costs]**.
1. [!UICONTROL 마케팅 채널 비용] 페이지에서 비용 항목 **[!UICONTROL 추가]** 또는 예산 항목 **[!UICONTROL 추가를]**&#x200B;클릭합니다.
1. **[!UICONTROL 저장을 클릭합니다.]**

   비용 항목을 계속 추가하려면 **[!UICONTROL 저장 후 다른 항목 추가를 클릭합니다]**.

1. (Optional) To export or import CSV files, access the [!UICONTROL Marketing Channel Costs] page, click **[!UICONTROL Export File]** or **[!UICONTROL Import File]**, then follow the prompts.

## Marketing Channel costs - definitions {#reference_0B193210E10A4B6B84A385A781FD9515}

마케팅 채널 비용 및 예산에 대한 필드 정의.



| 필드 | 정의 |
|--- |--- |
| 이름 | 비용 또는 예산 항목의 이름. 이 값은 SAINT를 사용하는 경우의 키 값입니다. |
| 채널 | 이 금액과 연관시키려는 채널. 비용 또는 예산을 첫 번째 접촉 채널에 적용할지, 마지막 접촉 채널에 적용할지를 지정합니다. 1회 새 유도로 첫 번째 접촉 비용 금액을 고려해 보십시오. 마지막 접촉 비용 금액은 클릭스루용입니다. |
| 날짜 범위 | 이 금액에 대해 사용하고자 하는 기간 |
| 유형 |  비용 또는 예산 유형(요율 또는 1회 비용). 요율은 클릭당 금액 같은 진행 중인 비용을 지정합니다. 1회 비용을 사용하면 배포 기준 금액을 지정할 수 있습니다. 예를 들어 클릭당 비용을 배포할 경우 총 클릭 수의 60%를 갖는 제휴는 총 비용의 60%를 소비하게 됩니다. 배포 기준 값은 숫자 분류를 세부적으로 나눌 때 사용되는 지표입니다. |
| 파일 내보내기 | 테이블 데이터를 CSV 파일로 내보낼 수 있습니다. |
| 파일 가져오기 | CSV 파일을 마케팅 채널 비용 페이지로 가져올 수 있습니다. |
