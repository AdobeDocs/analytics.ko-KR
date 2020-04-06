---
description: 다른 보고서 유형을 실행하는 단계.
title: 다른 보고서 유형 실행
topic: Reports,Reports and analytics
uuid: f59ab2a1-e916-46e8-bb5b-e6361ba00dda
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 다른 보고서 유형 실행

다른 보고서 유형을 실행하는 단계.


## 등급 보고서 실행 {#task_C570BA4A213F4F2EB7B30E012934BE7D}

등급 보고서의 표는 숫자나 비율에 따라 지표와 관련된 보고서 페이지의 등급을 보여줍니다. 등급 보고서는 한 보고서에 여러 지표를 표시할 수 있습니다.

<!-- 

t_reports_ranked.xml

 -->

1. 보고서(예: a [!UICONTROL Pages Report] ( **[!UICONTROL Reports]** > **[!UICONTROL Site Content]** > **[!UICONTROL Pages]**)를 생성합니다.
1. In the report header, click **[!UICONTROL Ranked.]**
1. 보고서의 등급을 지정하려면 테이블의 열 제목을 클릭합니다.

   등급 보고서의 테이블에는 최대 200개의 항목(예: 제품, 카테고리, 웹 페이지 등)과 10개의 지표(매출액, 주문, 보기 등)를 표시할 수 있습니다.

## 트렌드 보고서 실행 {#task_F03B4E760B9E4EA29FC3F654E6316887}

트렌드 보고서는 시간에 따른 지표를 표시합니다. 한 기간에서 다음 기간까지 세그먼트가 수행되는 방식을 보려는 경우 이 보고서 유형을 사용합니다.

<!-- 

t_reports_trended.xml

 -->

대부분의 전환 및 트래픽 보고서에는 트렌드 보기를 사용할 수 있습니다. 을 [!UICONTROL Calendar]사용하면 매달 지정된 일, 연중 주간, 분기별 주간, 연중 월간 등을 비롯한 모든 기간 분류에 대한 개선 사항을 표시할 수 있습니다. 트렌드 보고서는 최대 5개 항목(예: 제품, 카테고리, 웹 페이지 등)에 대한 단일 지표(매출액, 주문, 보기 등)의 트렌드를 보여줍니다.

**트렌드 보고서를 실행하려면**

1. 전환 또는 트래픽 보고서(예: **[!UICONTROL Reports]** > **[!UICONTROL Site Content]** > **[!UICONTROL Pages]**)를 실행합니다.
1. Under **[!UICONTROL Report Type]**, click **[!UICONTROL Trended.]**

## 전환 단계 보고서 실행 {#task_B926A74AA6A641138C2986C1635120CB}

전환 단계 보고서는 원하는 작업을 수행하기 위해 일련의 이벤트를 거친 방문자의 비율을 표시합니다. 예를 들어 웹 페이지 방문, 장바구니에 항목 추가, 항목 구입을 통해 경과된 방문자 수를 확인할 수 있습니다. 이 보고서는 도중에 폴아웃된 사람도 보여줍니다.

<!-- 

t_reports_conversion_funnel.xml

 -->

이 보고서를 실행하려면 보고서(예: 페이지 보고서)를 선택합니다( **[!UICONTROL Reports]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Tracking Code]** > **[!UICONTROL Campaign Conversion Funnel]**).

설명은 [전환 보고서](https://marketing.adobe.com/resources/help/ko_KR/reference/reports_conversion.html)를 참조하십시오.

## 폴아웃 보고서 실행 {#task_8FD97C8260464F9DA731A93DB8F80184}

이 [!UICONTROL Fallout Report] 보고서는 미리 지정된 페이지 시퀀스를 방문한 방문자 수를 보여줍니다. 또한 각 단계 간의 전환율과 폴아웃 비율을 표시합니다.

<!-- 

t_reports_fallout.xml

 -->

분석 작업 공간에서 새로운 [폴아웃](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/fallout_flow.html) 분석 패널을 확인하십시오.

1. 에서 [!UICONTROL Adobe Analytics]> **[!UICONTROL Reports]** > **[!UICONTROL Paths]** > **[!UICONTROL Pages]** 를 클릭합니다 **[!UICONTROL Fallout]**.
1. 페이지에서 [!UICONTROL Fallout Report] 을 클릭합니다 **[!UICONTROL Launch the Fallout Report Builder]**.

   ![단계 결과](assets/fallout_add_items.png)

1. On the [!UICONTROL Define Checkpoints] page, specify the checkpoints that you want to use for the report.
1. 클릭 **[!UICONTROL Run Report]**.

   ![단계 결과](assets/fallout_report.png)

>[!MORELIKETHIS]
>
>* [폴아웃 보고서 설명](https://marketing.adobe.com/resources/help/ko_KR/reference/reports_fallout.html)


## 페이지 흐름 보고서 실행 {#task_133E8B87C3F04DA0A42D10CBA499305B}

페이지 흐름 보고서는 방문자가 페이지에 액세스하고 사이트를 탐색하는 순서를 보여줍니다. 이 보고서를 통해 답변

분석 작업 공간에서 새로운 [흐름 시각화를](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/flow.html) 확인하십시오!

경로 [보고서를](https://marketing.adobe.com/resources/help/ko_KR/reference/reports_paths.html) 실행합니다.

예를 들어 > **[!UICONTROL Reports]** > **[!UICONTROL Paths]** > **[!UICONTROL Pages]** > **[!UICONTROL Next Page Flow]**&#x200B;를 클릭합니다.

![](assets/page_flow.png)

선택한 페이지에서 시작하여 이 보고서를 왼쪽에서 오른쪽으로 읽습니다. 선택한 페이지 이후에 본 페이지는 오른쪽으로 확장되는 분기로 표시됩니다.

각 후속 페이지를 본 비율은 페이지 이름 옆에 표시됩니다. 다음 각 페이지에 연결된 선의 너비는 이 상대적 백분율을 나타냅니다.

**[!UICONTROL Path Views]**:표시된 경로로 제한될 때 페이지를 본 횟수를 나타냅니다.

예를 들어 개인정보 보호정책 페이지에는 총 10,000개의 페이지 보기가 있을 수 있지만, 이 페이지 중 500개만 홈 페이지 바로 다음에 발생했습니다. 따라서 경로 보기라는 용어가 사용됩니다.

상대 백분율은 선의 상대적 너비로 표시됩니다. 기본적으로 이 보고서에는 5개의 2차 수준 분기와 5개의 3차 수준 분기가 표시됩니다.분기 수를 확장하여 최대 10개의 2차 수준 분기와 5개의 3차 수준 분기를 볼 수 있습니다. 이렇게 하면 보고서 높이가 높아지며 전체 그래프를 보려면 스크롤이 필요할 수 있습니다.

## 단계 보고서 실행 {#task_2BBF6FACD48F479E8B2EE458919941CB}

성공 이벤트를 선택하고 [!UICONTROL Purchase Conversion Funnel] 보고서나 [!UICONTROL Product Conversion Funnel] 보고서에 추가할 수 있습니다.

<!-- 

t_reports_funnel.xml

 -->

1. > **[!UICONTROL Reports]** > **[!UICONTROL Products]** > [제품 전환 단계를 클릭합니다](https://marketing.adobe.com/resources/help/ko_KR/reference/reports_conversion_funnel.html).

## 마케팅 채널 보고서 실행 {#task_64ADED5CC75248319E06E3E029B47F78}

마케팅 채널 보고는 매출, 주문 및 비용과 같은 표준 보고 지표와 함께 첫 번째 및 마지막 접촉 채널 할당에 대한 개요 보고서를 제공합니다. 이러한 보고서를 사용하면 각 채널이 생성하는 매출액을 분석할 수 있습니다.

<!-- 

t_reports_marketing_channel.xml

 -->

See the [Marketing Channel](https://marketing.adobe.com/resources/help/ko_KR/mchannel/index.html) help system for more information.

## 예외 항목 탐지 보고서 실행 {#task_4808C96327354D789C075823F5C3A049}

예외 항목 탐지에 있는 개별 지표 차트와 요약을 해석하는 방법에 대해 설명합니다.

<!-- 

t_anomaly_view.xml

 -->

Analysis Workspace에서 새[ 예외 항목 탐지 및 기여도 분석](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/anomaly_detection.html) 기능을 확인하십시오!

**[!UICONTROL Reports]** > **[!UICONTROL Site Metrics]** > **[!UICONTROL Anomaly Detection]** .

>[!NOTE] Analysis Workspace 프로젝트 내에서 예외 항목 탐지도 실행할 수 있습니다. [자세히...](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/anomaly_detection.html)

예외 항목 탐지 설정에 대한 자세한 내용은 참조 [가이드를 참조하십시오](https://marketing.adobe.com/resources/help/ko_KR/sc/user/index.html#Setting_up_Anomaly_Detection).

예외 항목 탐지는 두 가지 유형의 차트를 보여줍니다.요약 차트 및 개별 지표 차트 개별 지표 차트는 해당 지표에 대해 하나 이상의 예외 항목이 검색된 경우에만 표시됩니다.

<table id="table_88163CD8FC164342855D90D01F9C581A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>차트 유형 </p> </th> 
   <th colname="col2" class="entry"> <p>어떤 것이 있습니까 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>요약 차트 </p> <p><img placement="break"  src="assets/ad_summary_chart.png" width="570px" id="image_1CD4C4770BAA43C4AD7CBB824AD41338" /> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_D26DA3024CD7468291369F549557B28A"> 
      <li id="li_1C22B6E02FFB479FB71EFAD89EB37A4E">각 상자는 아래 지표에 해당하는 일별 추적된 하나의 예외 항목을 나타냅니다. </li> 
      <li id="li_8FC587D3FF4E452D83263CC7A10B6675">녹색은 트렌드 라인 위의 예외 항목을, 파란색은 꺾은 선형 아래의 예외 항목을 나타냅니다. </li> 
      <li id="li_25135AB691BF443599AF2A3A60E2E71A">예외 항목의 강도를 나타냅니다.예외 항목이 클수록 데이터 포인트의 색상이 어두워지고 트렌드 라인에서 멀어집니다. </li> 
      <li id="li_0C42AFA8897D420D8AB1A5D0F65B3B3A">개별 예외 항목을 클릭하면 예외 항목의 개별 지표 차트(요약 차트 아래)가 맨 위에 표시됩니다. </li> 
      <li id="li_85C0F426952547B5A75D6BD31DE19CA5">편차 백분율 값(차트의 왼쪽)은 다음과 같이 계산됩니다. 
       <ul id="ul_BEC0A88BFFAC4CF78BC9885FEB749694"> 
        <li id="li_1BAB2F50482745B69937DFAF1E09982E">상한 및 예상 값이 동일하면 편차 비율은 100%입니다. </li> 
        <li id="li_CA48064F5788448C8646CCE196161237">그 외의 경우 편차 비율은 ((실제 값 – 상한 값)/(상한 값 – 예상 값)) * 100입니다. </li> 
        <li id="li_4090357A0D214BC7B1C3DE0615875554">하한과 예상 값이 동일하면 편차 비율은 –100%입니다. </li> 
        <li id="li_EF694E1A4E874ECD94E1E8F7302E494F">그 외의 경우 편차 비율은 ((하한 값 – 실제 값)/(예상 값 – 하한 값)) * -100입니다. </li> 
       </ul> </li> 
      <li id="li_5C05EF7023484CC993E96D63E842B65C"><span class="uicontrol">세그먼트 표시</span>를 클릭하면 세그먼트를 예외 항목 탐지 보고서에 적용할 수 있도록 해주는 세그먼트 레일이 표시됩니다.  세그멘테이션 <a href="https://marketing.adobe.com/resources/help/ko_KR/analytics/segment/"  >추가 정보</a>. </li> 
      <li id="li_1B41CABF13D1407886C68EE3BC201E60"><span class="uicontrol">지표 편집</span>을 클릭하면 예외 항목을 탐지할 지표를 선택하거나 선택 취소할 수 있습니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>개별 지표 차트 </p> <p><img placement="break"  src="assets/metric_report.png" width="570px" id="image_5BBECFD91CF14478AA4761E6256BBCB9" /> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_739C5687013743A29B63089FDA763F45"> 
      <li id="li_456A0BDA4D4E46CE9CC1C3DBAA1E2220">개별 트렌드 지표(계산된 지표 포함)에 대한 예외 데이터 포인트를 점으로 표시합니다. </li> 
      <li id="li_89FD847C65F04F48BCA7CD38D0EC51CD">맨 위에 가장 최근 예외 항목을 표시하고 부차적으로 예외 항목 수별로 순위가 정해집니다. </li> 
      <li id="li_98B97A9706DE4455B8D8850904CBDE03">현재 수집된 실제 데이터를 나타내는 실선을 표시합니다. 이것은 데이터 포인트가 예외적인지 여부를 도출하기 위한 오차 예측 및 여백과 비교됩니다. </li> 
      <li id="li_0EEA38DDDC344BF3879430E67D74EB72">내역 데이터(즉, 교육 기간)를 기반으로 예측을 나타내는 점선을 표시합니다. </li> 
      <li id="li_035BD2725D004AEDB630BF8DFF4DA4F3">상위 및 하위 95% 신뢰 구간/범위를 회색 음영으로 표시합니다. </li> 
      <li id="li_021A3D1F2EDB4319B9B39620EF1C038A">지표 이름 옆에 있는 이중 위쪽 또는 아래쪽 화살표를 클릭하여 개별 보고서를 축소하고 확장할 수 있습니다. </li> 
      <li id="li_722E4B9FC21047AC96D7B143197E293D">개요 보고서의 드릴다운에 응답하여 지표 차트가 표시되는 순서를 변경합니다(위 참조). </li> 
      <li id="li_A2441169B185475AA68A64F81E6E40B8">모든 페이지 관련 지표에 대해 "페이지"와 같은 검색어를 사용하여 차트를 필터링할 수 있습니다. </li> 
      <li id="li_F1BBBFCA8E2A43C29658E4FCAA36C904">정의한 모든 지표나 예외 항목이 있는 지표만 표시할 수 있습니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예외 항목 탐지 설정 {#task_AF347B34F56E44A6AE70E019B6EB2F08}

예외 항목 탐지를 위한 보고서 세트, 지표 및 교육/보기 기간을 선택하는 절차입니다.

<!-- 

t_anomaly_config.xml

 -->

각 보고서 세트에 대해 독립적으로 예외 항목 탐지를 설정합니다.

1. 로 **[!UICONTROL Analytics > Reports > Site Metrics > Anomaly Detection]** 이동합니다.
1. 일일 예외 항목 탐지를 추적할 보고서 세트를 선택합니다. 보고서 세트 목록을 표시하려면, 보고서 세트 선택기 드롭다운 메뉴를 클릭합니다.
1. To select the metrics and/or define filtered metrics, click **[!UICONTROL Edit Metrics]** at the top right of the screen:  ![](assets/metrics_icon.png).

   모든 지표 목록(계산된 지표 포함) 또는 추적된 지표 목록에서 지표를 선택할 수 있습니다. 목록의 범위를 좁히려면 특정 용어로 필터링할 수도 있습니다. 1. Once the report has been generated, define the **[!UICONTROL Training Period]** and the **[!UICONTROL View Period]** for anomaly detection. (훈련 기간을 알고리즘에 대한 &quot;학습 기간&quot;으로 생각합니다.)

   ![](assets/view_training_periods.png)

   주의 사항:

* 교육 기간은 보기 기간이 시작되기 직전에 종료됩니다.
* 두 항목의 기본값은 모두 30일이며, 60일 또는 90일로 연장할 수 있습니다.
* 교육 기간을 연장하면 데이터가 더 큰 컨텍스트에서 표시되고 예외 항목의 크기가 줄어들 수 있습니다.

   예외 항목 탐지 지표 보고서는 매개 변수를 변경할 때마다 새로 고침됩니다.
1. (Optional) Apply segments to the report by clicking **[!UICONTROL Show Segments]** and selecting one or more existing segments or creating a new segment and applying it.

   ![](assets/ad_top_menu.png)

   세그먼트 만들기나 관리에 대한 자세한 내용은 [분석 세그멘테이션 안내서](https://marketing.adobe.com/resources/help/ko_KR/analytics/segment/)를 참조하십시오. 1. (선택 사항) 보고서를 즐겨찾기 또는 책갈피로 추가합니다.
1. (선택 사항) 보기 기간의 종료 날짜를 변경합니다. 기본값은 어제입니다.
1. 이제 보고서 해석을 시작할 수 있습니다. [예외 항목 탐지 차트를 봅니다](/help/analyze/reports-analytics/t-running-report-types.md#task_4808C96327354D789C075823F5C3A049).

## 실시간 보고서 실행 {#task_5D25929C918E40B18965222FA94176B0}

실시간 보고서를 보고 해석하는 방법에 대해 설명합니다.

<!-- 

reports_realtime.xml

 -->

**[!UICONTROL Reports > Site Metrics > Real-Time]** .

실시간 보고에서는 개요 보고서와 세부 사항 보고서 등 두 가지 주요 보고서를 제공합니다. 각 reportlet은 여러 개의 reportlet으로 구성됩니다.

실시간 보고서 구성에 대한 자세한 내용은 분석 [참조 안내서를 참조하십시오](https://marketing.adobe.com/resources/help/ko_KR/reference/index.html#RealTime_Reports_Configuration).

1. Take a look at the **[!UICONTROL Overview]** report and its components:  ![](assets/rtr_overview_report.png)

   <table id="choicetable_8586BECF55E843B2B5CD41205567EA32"> 
   <thead class="chhead sthead"> 
   <th class="choptionhd"> UI 구성 요소 </th> 
   <th class="chdeschd"> 설명 </th> 
   </thead> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>보고서 세트 선택</strong></td> 
   <td class="chdesc stentry"> 이 실시간 보고서가 다루는 보고서 세트를 보여 줍니다. 보고서 세트를 변경하려면, <a href="https://marketing.adobe.com/resources/help/ko_KR/reference/t_realtime_admin.html"  >실시간 보고서 구성</a>을 참조하십시오 . </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>보고서 간 전환</strong></td> 
   <td class="chdesc stentry"> 설정한 보고서(최대 3개) 간을 전환할 수 있습니다. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>시간 범위 선택</strong></td> 
   <td class="chdesc stentry"> 보고서에 있는 모든 reportlet에서 사용할 전체 시간 범위를 선택할 수 있습니다. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>보고서 구성</strong></td> 
   <td class="chdesc stentry"> 이 톱니바퀴 아이콘 링크는 관리자 권한이 있어야 볼 수 있습니다. 이 링크를 클릭하면 <span class="ignoretag"><span class="uicontrol">관리 도구</span> &gt; <span class="uicontrol">보고서 세트</span> &gt; <span class="uicontrol">설정 편집</span> &gt; <span class="uicontrol">실시간</span></span> 아래의 보고서 세트 관리자가 표시됩니다  . </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>전체 화면 보기</strong></td> 
   <td class="chdesc stentry"> 전체 화면 보기 아이콘은 모니터가 특정 종횡비(16:9 또는 16:10)이고, 브라우저가 이 종횡비를 지원하는 경우에만 볼 수 있습니다. 전체 화면 모드(종료하려면 <span class="uicontrol">Esc</span> 키 누름)일 때에는 화면과 상호 작용할 수 없습니다. 전체 화면 모드는 시간 제한이 없습니다. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>사이트 트래픽 Reportlet</strong></td> 
   <td class="chdesc stentry"> 파란색 트렌드 라인 데이터는 전체 사이트의 트래픽 합계를 보여줍니다. X축은 실시간 표현식으로 표시되는 현재 값을 제외한 문자 레이블(15분 전, 10분 전)을 사용합니다. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>사이트 총계 Reportlet</strong></td> 
   <td class="chdesc stentry"> 지난 N분 동안 실시간 보고서에서 선택한 지표에 대한 사이트 합계 수를 표시합니다. "N"은 시간 범위 선택기를 통해 구성할 수 있습니다. <p>화살표 색상 및 방향은 다음 알고리즘을 기반으로 합니다. 
      <ul id="ul_9F40CEA33798467393CB1266BB36D500"> 
      <li id="li_CCD01A44F912487DA5681EA50113643C">중요 게인(위쪽 화살표):&gt; 100% </li> 
      <li id="li_7402491A9A614851B7F2AE0C77BD9A97">게인(오른쪽 위 화살표):5% ~ 100% 사이 </li> 
      <li id="li_BCA79C08B5714D4B9315068112C66107"> 평면(오른쪽 화살표):5% ~ -5% </li> 
      <li id="li_234ECBD7D83A4AE680E4A70BF288681F"> 손실(오른쪽 아래 화살표):-5% ~ -10% </li> 
      <li id="li_10C5EA8803604C1CA714D3DB27478B31"> 중요 손실(아래쪽 화살표):&lt;-100% </li> 
      </ul> </p> <p>사이트 합계가 "인스턴스"로 보고되는 경우 이러한 인스턴스는 기본 reportlet의 차원을 반영합니다. 인스턴스별 이름(예: "페이지 보기")이 있으면 사이트 총계가 해당 이름을 보고합니다. </p> </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>기본 Reportlet</strong></td> 
   <td class="chdesc stentry"> 실시간 보고서의 기본 차원과 해당 지표에 대한 보고서입니다. 선택한 시간 범위의 해당 요소에 대한 꺾은 선형을 표시합니다. 지표 합계는 전체 트렌드 라인의 합계를 나타냅니다. 화살표는 항목이 크게 증가, 증가, 균일, 손실 또는 크게 손실되는지 여부를 나타냅니다. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>검색 대화 상자</strong></td> 
   <td class="chdesc stentry"> 검색은 모든 reportlet에 영향을 줍니다. 검색은 보고서를 볼 때 지속됩니다. </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>정렬 기준... 가장 빈도가 높음/승자/ 패자</strong></td> 
   <td class="chdesc stentry"> <span class="uicontrol">가장 빈도가 높음</span>(기본값), <span class="uicontrol">승자</span>(대부분의 성장을 보여 주는 차원), 및 <span class="uicontrol">패자</span>(하향 궤적에 있는 차원)을 기준으로 정렬하도록 전환할 수 있습니다. <p>승자인지 패자인지를 결정하는 데 사용되는 공식이 있습니다. 실시간 기능은 가장 이른 샘플과 다음으로 최신인 샘플을 보고 간단한 “변경률” 계산을 수행합니다. 따라서 "지난 15분"을 선택하고 n이 현재 분을 나타내는 경우 n-1은 n-15와 비교됩니다. 현재 실시간은 가중치를 적용하지 않습니다. 현재 분은 완료되지 않았으며 잘못된 % 변경을 생성할 수 있으므로 무시됩니다. </p> <p>이 공식은 실시간 보고서에 사용된 모든 지표에서 일관됩니다. </p> </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>보조 1 Reportlet</strong></td> 
   <td class="chdesc stentry"> 프로비저닝된 두 번째 보고서의 차원과 지표에 대한 실시간 보고서를 표시합니다. <p>보조 1 reportlet은 상위 4개 카테고리를 표시합니다.5번째 값은 남아 있는 모든 값의 집합입니다. 각 카테고리에 대해 해당 카테고리의 전체 원시 보기가 제공됩니다. 또한 모든 카테고리의 합계는 가운데에 표시됩니다. </p> <p> 마우스로 섹션을 가리키면 연관된 카테고리가 강조 표시되고 도넛 아래에 카테고리 꺾은 선형이 표시됩니다. </p> <p> 라인 항목을 마우스로 가리키면 라인 항목과 연관된 섹션이 강조 표시되고 도넛 아래에 카테고리 꺾은 선형이 표시됩니다. </p> </td> 
   </tr> 
   <tr class="chrow strow"> 
   <td class="choption"><strong>보조 2 Reportlet</strong></td> 
   <td class="chdesc stentry"> 프로비저닝된 세 번째 보고서의 차원과 지표에 대한 실시간 보고서를 표시합니다. 마우스로 항목 레이블 위에 마우스를 놓으면 레이블이 오른쪽으로 이동하고 마우스로 가리킨 항목의 꺾은 선형이 표시됩니다. </td> 
   </tr> 
   </table>

1. Click a list item in the Primary Reportlet to launch the **[!UICONTROL Details]** view for that list item:  ![](assets/rtr_detail_report.png)

   | **항목 트렌드 Reportlet** | 지난 N분 동안 개요 보고서에서 선택한 항목의 꺾은 선형을 표시합니다. N은 시간 범위 선택기를 통해 구성할 수 있습니다. |
   |---|---|
   | **항목 합계 Reportlet** | 지난 N분 동안 개요 보고서에서 선택한 항목에 대한 총 지표 카운트를 표시합니다. N은 시간 범위 선택기를 통해 구성할 수 있습니다. |
   | **상관 관계가 있는 보조 1 Reportlet** | 이 reportlet은 보조 1 Reportlet과 매우 유사합니다. 유일한 차이는 이 보고서를 채우는 데 사용된 데이터 소스입니다.이 예에서는 특정 페이지(개요 보고서의 기본 reportlet에서 선택한 페이지)와 본 인스턴스 간의 상관 관계(또는 분류)를 보여줍니다. |
   | **상관 관계가 있는 보조 2 Reportlet** | 이 reportlet은 보조 2 Reportlet과 매우 유사합니다. 유일한 차이는 이 보고서를 채우는 데 사용된 데이터 소스입니다.이 예에서는 특정 페이지(개요 보고서의 기본 reportlet에서 선택한 페이지)와 언어 차원 간의 상관 관계(또는 분류)를 보여줍니다. |
