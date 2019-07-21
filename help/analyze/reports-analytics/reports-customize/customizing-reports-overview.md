---
description: 보고서 실행 후, 보고서를 사용자 지정하여 필요에 따라 데이터를 보고 분석할 수 있습니다. 보고서 데이터를 필터링하고, 데이터가 그래픽으로 표시되는 방식을 변경하고 날짜 세부기간을 변경하는 등의 작업을 할 수 있습니다.
seo-description: 보고서 실행 후, 보고서를 사용자 지정하여 필요에 따라 데이터를 보고 분석할 수 있습니다. 보고서 데이터를 필터링하고, 데이터가 그래픽으로 표시되는 방식을 변경하고 날짜 세부기간을 변경하는 등의 작업을 할 수 있습니다.
seo-title: 보고서 개요 사용자 지정
solution: Analytics
title: 보고서 개요 사용자 지정
topic: Reports & Analytics
uuid: 37 D 221 B 7-50 FD -4425-B 2 BA-F 40911 B 72 A 2 F
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 보고서 개요 사용자 지정

보고서 실행 후, 보고서를 사용자 지정하여 필요에 따라 데이터를 보고 분석할 수 있습니다. 보고서 데이터를 필터링하고, 데이터가 그래픽으로 표시되는 방식을 변경하고 날짜 세부기간을 변경하는 등의 작업을 할 수 있습니다.

## 사용자 지정 보고서 만들기 {#task_BA6EACA3039C40AEA5605E1D8C76E646}

모든 사용자가 볼 수 있는 새 사용자 지정 보고서로 보고서의 현재 구성을 저장하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_custom.xml

 -->

사용자 지정 보고서는 관리자만 만들 수 있습니다. 사용자 지정 보고서를 만들면 기준 보고서 옆에 있는 주 보고 메뉴에 해당 보고서가 추가됩니다.

**사용자 지정 보고서를 만들려면**

1. 보고서를 실행하고 필요에 따라 구성합니다.
1. **[!UICONTROL 자세히]** &gt; 사용자 지정 보고서 **[!UICONTROL 만들기를]**&#x200B;클릭합니다.
1. 보고서 이름을 지정한 다음 **[!UICONTROL 저장을 클릭합니다.]**

     기존 보고서 이름과 동일하지 않도록 확인합니다.

>[!MORE_LIKE_THIS]
>
>* [메뉴 사용자 지정](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=customize_menus)


## 날짜 또는 날짜 범위 선택 {#task_9BEF7D4D839A4748B76E8500D1406C34}

보고서 데이터에 대한 기간을 선택하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_select_date.xml

 -->

특정 일, 주, 월 또는 연도를 선택할 수 있습니다. 비교 보고서를 실행할 수도 있습니다.

날짜 범위가 다른 reportlet을 사용하여 대시보드를 열 때 달력에서 새 날짜 범위를 선택할 수 있습니다. 변경 사항이 대시보드의 모든 reportlet에 적용됩니다.

**날짜 범위를 선택하려면**

1. 보고서 실행.
1. 오른쪽 상단에 있는 달력 아이콘을 클릭합니다.
1. 날짜를 선택합니다.

   다음을 수행할 수 있습니다.

   * 일, 월 또는 년과 같은 기간을 최대 세 개까지 봅니다.
   * 날짜에서 커서를 드래그하여 범위를 선택합니다.
   * 날짜를 수동으로 입력합니다.
   * 달 이름을 클릭하여 달을 선택합니다.
   * **[!UICONTROL 사전 설정 선택]을 선택하여 미리 정한 날짜를 선택합니다.**
   * 날짜 비교.

1. Click **[!UICONTROL Run Report]**.

## 날짜 비교 {#task_95155C3700774B709F5FB81AE96B0824}

달력을 사용하여 등급 보고서 간의 날짜 비교를 실행하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_comparing_dates.xml

 -->

트렌드 보고서들 간에는 날짜를 비교할 수 없습니다.

>[!NOTE]
>
>If you want to perform a date comparison on key metrics in a dashboard, you can pull the data into [Report Builder](https://marketing.adobe.com/resources/help/en_US/arb/) using two separate requests. 그런 다음 Excel에서 사용자 지정 공식을 사용하여 둘 사이의 차이를 분석합니다.

Reports &amp; Analytics에서 등급 보고서 간 날짜 비교:

1. 보고서 실행.
1. 오른쪽 상단에 있는 달력을 클릭합니다.
1. Click **[!UICONTROL Compare Dates]**.
1. 사용할 날짜를 선택합니다.
1. Click **[!UICONTROL Run Report]**.

## 비율을 그래프로 표시 {#task_BC28CA19A4834AF6BFE68B5B5AEFE75D}

보고서 테이블에서 비율을 그래프로 표시할지 여부를 지정하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_graph_percent.xml

 -->

시각화 옵션은 대시보드 reportlet에서도 사용할 수 있습니다.

1. Run a report that supports percentages, such as a [!UICONTROL Pages Report].
1. Click **[!UICONTROL Percent Shown As: Graph]**.

## 보고서 데이터 정규화 {#task_8005B55E59BD479DA67BC618FF8BC94A}

보고서 데이터를 정규화하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_normalize.xml

 -->

비교 날짜로 보고서를 실행한 후 또는 A/B 비교의 경우 데이터를 정규화하여 보고서 간 변화율을 나타낼 수 있습니다. 보조 데이터 세트는 선택한 일수의 차이 또는 다른 트래픽 볼륨을 보상하여 조정됩니다.

**보고서 데이터를 정규화하려면**

1. 날짜 비교를 지원하는 보고서를 실행합니다
1. Click **[!UICONTROL Compare Dates]**, then specify your date comparison.
1. Click **[!UICONTROL Run Report]**.
1. Click **[!UICONTROL Normalize Data: Yes]**.

## 보고서 페이지 선택 {#task_5CAC3B76BD4C4208B8D53DD972D4771F}

보고서에 대한 웹 사이트 페이지에서 특정 페이지를 선택하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_select_page.xml

 -->

1. [!UICONTROL 페이지 보기 보고서] ( **[!UICONTROL 보고서]** &gt; **[!UICONTROL 사이트 지표]** &gt; **[!UICONTROL 페이지 보기]**) 와 같은 보고서를 생성합니다.
1. **선택한 페이지** 링크를 클릭합니다.
1. [!UICONTROL 페이지 선택]에서 표시할 페이지를 선택합니다.
1. 페이지를 찾습니다.
1. **[!UICONTROL 확인을 클릭합니다.]**

## 보고서 세트 비교 {#task_6BEBEB2D4F36497C9DA5B18ADAD35546}

같은 보고서에 있는 두 개의 보고서 세트에서 보고서를 표시하는 방법을 설명하는 단계입니다.

<!-- 

t_reports_compare_suites.xml

 -->

그래픽 표시 외에 보고서 표는 백분율 비교를 제공합니다. 다음 보고서는 비교하며 실행할 수 있습니다.

* 사이트 컨텐츠
* 모바일
* 트래픽 소스
* 캠페인
* 제품
* 방문자 유지
* 방문자 프로필
* 사용자 지정 전환
* 사용자 지정 트래픽
* 목표
* 설문 조사

**보고서 세트를 비교하려면**

1. 보고서를 비교할 수 있도록 해주는 보고서를 생성합니다.
1. **사이트에 비교** 링크를 클릭합니다.
1. 보고서 세트를 찾습니다.
1. **[!UICONTROL 확인을 클릭합니다.]**

## 보고서 세부기간 지정 {#task_7ED3EEC9E1704A918B25D06ADA3412E0}

시간대별, 일일, 주간, 월간, 분기별 또는 연간 기준으로 보고서 총계를 보는 방법을 설명하는 단계입니다.

<!-- 

t_reports_granularity.xml

 -->

보고서의 기간은 사용 가능한 세부기간 옵션을 결정합니다. 예를 들어 1 또는 2일 시간대를 선택한 경우에만 **[!UICONTROL 시간별]옵션을 선택할 수 있습니다.** 2년 이상의 연도를 선택한 경우에만 **[!UICONTROL 연간]세부기간을 선택할 수 있습니다.**

**보고서 세부기간을 지정하려면**

1. **[!UICONTROL 사이트 컨텐츠]** &gt; **[!UICONTROL 페이지와 같은 트렌드 보고서를 생성합니다.]**
1. **보기 방법** 링크를 클릭한 다음 세부기간을 클릭합니다.

## 요일 보고서 실행 {#task_67CC818ACC3749839B69BDB2ED9AE6B8}

특정 요일에 보고서를 실행하는 방법을 설명하는 단계입니다(예: 지정된 날짜 범위에서 매주 월요일).

<!-- 

t_reports_day_of_week.xml

 -->

이 기능은 날짜 범위가 주 또는 일인 트렌드 보고서에만 적용됩니다.

1. 지정된 날짜 범위에서 추세 보고서를 실행합니다.
1. **요일** 링크를 클릭한 다음 요일을 클릭합니다.

## '작업 공간에서 시도' 버튼 {#concept_DA41E22460B94BD9ADF63B1CEE2714A7}

보고서 상단의 **[!UICONTROL 작업 공간에서 시도]버튼을 클릭하면 Analysis Workspace에서 동일한 보고서가 로드됩니다.**

<!-- 

try_in_workspace.xml

 -->

Reports &amp; Analytics의 대부분의 보고서에는 이후의 사용자 지정을 위해 Analysis Workspace에서 현재 보기를 재현할 수 있는 "작업 공간에서 시도" 버튼이 포함되어 있습니다.

현재 이 버튼은 사용자가 Analysis Workspace에 대한 모든 권한을 보유하는 경우에만 사용할 수 있습니다.

보고서를 사용자 지정할 수 있는 모든 방법에 대한 자세한 내용은 [Analysis Workspace](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/) 가이드를 참조하십시오.
