---
description: 기본 리포트 빌더 데이터 요청을 만드는 절차.
seo-description: 기본 리포트 빌더 데이터 요청을 만드는 절차.
seo-title: 리포트 빌더 데이터 요청 만들기
solution: Analytics
title: 데이터 요청 만들기
topic: Report Builder
uuid: 5d0151f1-e23d-43eb-84a4-96ae06c3a564
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# 리포트 빌더 데이터 요청 만들기

기본 데이터 요청을 만드는 절차.

1. In Excel, click **[!UICONTROL Create]**.
1. In the [!UICONTROL Request Wizard: Step 1] window, select a [report suite](../../../analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md#task_59444416F6F042D1998217AE91580913).
1. (선택 사항) 세그먼트를 선택하여 요청에 적용합니다. 세그먼트를 한 개 이상 선택하면 선택한 세그먼트가 목록 맨 위로 이동합니다.

   Report Builder는 Adobe Analytics가 세그먼트를 사용하는 방법과 동일하게 세그먼트를 사용합니다. [Analytics 세그멘테이션 안내서](https://marketing.adobe.com/resources/help/en_US/analytics/segment/)를 참조하십시오. 1. (선택 사항) 배포에 사용할 [게시 목록을](../../../analyze/report-builder/data-requests/allow-publishing-list-overrides.md#concept_BCB19A20DC4B4B8D984F9670EE018D8C) 선택합니다.
1. [보고서 유형을](../../../analyze/report-builder/data-requests/c-report-types/select-report-types.md#concept_C711B27E6FB64C18AC564EE142FC7EFC)선택합니다.
1. 날짜 범위 [및 보고서](../../../analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) 세부기간을 지정합니다 [](../../../analyze/report-builder/data-requests/configuring-report-dates/granularity.md#concept_A13CBA2962E24FF882456135431B7ADB).
1. Click **[!UICONTROL Next]**.
1. In the [Layout - Request Wizard Step 2](../../../analyze/report-builder/layout/layout.md#concept_D66E1C2217E24E1F837AC064C61919DB) window, specify a layout:

   | 요소 | 설명 |
   |---|---|
   | 피벗 레이아웃 | 표준 Excel 테이블과 유사하게, 레이아웃용 행, 열 및 지표 그리드를 제공합니다. 이 레이아웃을 사용하여 원본 요청 내에 분류 요청을 추가할 수 있습니다. |
   | 사용자 지정 레이아웃 | [!UICONTROL 피벗 레이아웃]이 가지고 있는 대부분의 기능을 사용할 수 있지만, 스프레드시트에서 그리드에 있는 각 항목을 찾아야 하는 위치를 선택할 수도 있습니다. 이 레이아웃에서는 이전 릴리스에서 사용할 수 있는 유연성을 제공합니다. |

1. [!UICONTROL 지표] 탭에서, 트리의 지표를 두 번 클릭하여(또는 드래그하여) [!UICONTROL 지표] 그리드에 추가합니다.
1. [!UICONTROL 차원] 탭에서 차원을 두 번 클릭하여(또는 드래그하여) [!UICONTROL 행 레이블] 그리드에 추가합니다.

   보고서 세트의 구성과 1단계에서 선택한 기본 보고서에 따라 2단계에서 [차원](https://marketing.adobe.com/resources/help/en_US/reference/dimensions.html)을 사용할 수 있습니다. 차원은 상호 관련시키거나 하위 관계로 만들거나 [!UICONTROL 요청 마법사: 1단계] 창에서 선택한 원래 보고서 유형 지표의 분류인 항목입니다. 2단계에서 두 개 이상의 차원을 추가하면 데이터 요청에서 분류가 만들어집니다.

   자세한 내용은 [지표 및 차원 추가](../../../analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md#task_E3F520C020F64C5A96DC5C96FEF71FC4)를 참조하십시오.