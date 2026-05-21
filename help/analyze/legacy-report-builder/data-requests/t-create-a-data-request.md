---
description: 기본 Report Builder 데이터 요청을 만드는 절차.
title: 데이터 요청 만들기
feature: Report Builder
role: User, Admin
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
TQID: https://experienceleague.adobe.com/w-oiIfs1qFMoQbaN8YrNIn1TRNHeN97lQOlkLeXdLb0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 59%

---

# Report Builder 데이터 요청 만들기

{{legacy-arb}}

기본 데이터 요청을 만드는 절차.

1. Excel에서 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.
1. [!UICONTROL 요청 마법사: 1단계] 창의 [보고서 세트](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)를 선택합니다.
1. 세그먼트를 선택하여 요청에 적용합니다(선택 사항). 세그먼트를 한 개 이상 선택하면 선택한 세그먼트가 목록 맨 위로 이동합니다.

   Report Builder는 Adobe Analytics가 세그먼트를 사용하는 방법과 같게 세그먼트를 사용합니다. [Analytics 세그멘테이션 안내서](/help/components/segmentation/seg-home.md)를 참조하십시오.
1. [보고서 유형](/help/analyze/legacy-report-builder/data-requests/c-report-types/select-report-types.md)을 선택합니다.
1. [날짜 범위](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md)를 및 보고서 [세부 기간](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/granularity.md)을 지정합니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. [레이아웃 - 요청 마법사 2단계](/help/analyze/legacy-report-builder/layout/layout.md) 창에서 다음 레이아웃을 지정합니다.

   | 요소 | 설명 |
   |---|---|
   | 피벗 레이아웃 | 레이아웃에 대한 행, 열 및 지표 그리드를 제공합니다(표준 Excel 테이블과 유사). 이 레이아웃을 사용하면 원래 요청 내에 분류 요청을 추가할 수 있습니다. |
   | 사용자 정의 레이아웃 | [!UICONTROL 피벗 레이아웃]이 가지고 있는 대부분의 기능을 사용할 수 있지만 스프레드시트에서 그리드에 있는 각 항목을 찾아야 하는 위치를 선택할 수도 있습니다. 이 레이아웃은 이전 릴리스에서 사용할 수 있는 유연성을 제공합니다. |

1. [!UICONTROL 지표] 탭에서 트리의 지표를 더블 클릭하여(또는 드래그하여) [!UICONTROL 지표] 그리드에 추가합니다.
1. [!UICONTROL 차원] 탭에서 차원을 더블 클릭하여(또는 드래그하여) [!UICONTROL 행 레이블] 그리드에 추가합니다.

   2단계에서 사용할 수 있는 [차원](/help/analyze/report-builder/filter-dimensions.md)은(는) 1단계에서 선택한 기본 보고서와 보고서 세트의 구성에 따라 다릅니다. 이 차원은 상호 연관되거나, 하위 관계를 지정하거나, [!UICONTROL 요청 마법사: 1단계] 창에서 선택한 원래 보고서 유형 지표의 분류입니다. 2단계에서 차원을 두 개 이상 추가하는 것은 데이터 요청에서 분류를 만드는 방법입니다.

   자세한 내용은 [지표 및 차원 추가](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md)를 참조하십시오.
