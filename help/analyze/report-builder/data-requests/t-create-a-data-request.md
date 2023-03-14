---
description: 기본 Report Builder 데이터 요청을 만드는 절차.
title: 데이터 요청 만들기
feature: Report Builder
role: User, Admin
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
source-git-commit: d2e4a6eed54fa8b3e080b162a5e841fc2f5a0e59
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 100%

---

# Report Builder 데이터 요청 만들기

기본 데이터 요청을 만드는 절차.

1. Excel에서 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.
1. [!UICONTROL 요청 마법사: 1단계] 창의 [보고서 세트](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)를 선택합니다.
1. 세그먼트를 선택하여 요청에 적용합니다(선택 사항). 세그먼트를 한 개 이상 선택하면 선택한 세그먼트가 목록 맨 위로 이동합니다.

   Report Builder는 Adobe Analytics가 세그먼트를 사용하는 방법과 같게 세그먼트를 사용합니다. [Analytics 세그멘테이션 안내서](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html)를 참조하십시오.
1. [보고서 유형](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md)을 선택합니다.
1. [날짜 범위](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)를 및 보고서 [세부기간](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md)을 지정합니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. [레이아웃 - 요청 마법사 2단계](/help/analyze/report-builder/layout/layout.md) 창에서 다음 레이아웃을 지정합니다.

   | 요소 | 설명 |
   |---|---|
   | 피벗 레이아웃 | 표준 Excel 테이블과 유사하게, 레이아웃용 행, 열 및 지표 그리드를 제공합니다. 이 레이아웃을 사용하여 원본 요청 내에 분류 요청을 추가할 수 있습니다. |
   | 사용자 정의 레이아웃 | [!UICONTROL 피벗 레이아웃]이 가지고 있는 대부분의 기능을 사용할 수 있지만 스프레드시트에서 그리드에 있는 각 항목을 찾아야 하는 위치를 선택할 수도 있습니다. 이 레이아웃에서는 이전 릴리스에서 사용할 수 있는 유연성을 제공합니다. |

1. [!UICONTROL 지표] 탭에서 트리의 지표를 더블 클릭하여(또는 드래그하여) [!UICONTROL 지표] 그리드에 추가합니다.
1. [!UICONTROL 차원] 탭에서 차원을 더블 클릭하여(또는 드래그하여) [!UICONTROL 행 레이블] 그리드에 추가합니다.

   보고서 세트의 구성과 1단계에서 선택한 기본 보고서에 따라 2단계에서 [차원](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/layout/filter-dimenson/filter-dimensions.html)을 사용할 수 있습니다. 차원은 상호 관련시키거나 하위 관계로 만들거나 [!UICONTROL 요청 마법사: 1단계] 창에서 선택한 원래 보고서 유형 지표의 분류인 항목입니다. 2단계에서 두 개 이상의 차원을 추가하면 데이터 요청에서 분류가 만들어집니다.

   See [지표 및 차원 추가](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md)를 참조하십시오.
