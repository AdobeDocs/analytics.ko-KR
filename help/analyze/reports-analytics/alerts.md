---
description: 'null'
seo-description: 'null'
seo-title: 경고
solution: Analytics
subtopic: 경고
title: 경고
topic: Reports & Analytics
uuid: e 1333 a 9 b-eba 0-45 b 7-b 7 e 6-46 e 06190 db 64
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 경고

## 경고 {#concept_8AB25AF6FB52478DB98C1BA4577A2E16}

모든 Adobe Analytics에 대한 새로운 경고 시스템인 지능형 경고를 사용하면 경고 미리 보기와 규칙 기여도를 갖춘 경고를 작성하고 관리할 수 있습니다. 개별 게시물의

* 예외 항목을 기반으로 한 경고를 만듭니다(90%, 95% 또는 99% 임계값, % 변경, 초과/미만).
* 경고가 트리거되는 빈도를 미리 봅니다.
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다.
* 하나의 경고에서 여러 지표를 캡처하는 "누적된" 경고를 생성합니다.

You can access this new Alerts system from **[!UICONTROL More]** &gt; **[!UICONTROL Alerts]** in any report in Reports &amp; Analytics.

자세한 내용은 [지능형 경고](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/intellligent_alerts.html)의 Analysis Workspace 문서를 참조하십시오.

## 경고 추가 {#task_51187E8BF19544DDA9EF2057E6F11D35}

Adobe Analytics에서 경고를 추가하는 방법을 설명하는 단계입니다.

<!-- 

t_add_an_alert.xml

 -->

**[!UICONTROL Analytics]** &gt; **[!UICONTROL 구성 요소]** 메뉴에서 새 경고 빌더로 이동합니다. 하지만 Reports &amp; Analytics 내에서 여전히 액세스할 수 있습니다.

1. Reports &amp; Analytics에서 경고를 설정할 보고서를 엽니다.
1. **[!UICONTROL 자세히]** &gt; 경고 **[!UICONTROL 추가를]**&#x200B;클릭합니다.
1. This will take you to the [new Alert Builder](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/alert-builder.html).

## 기존 경고 보기 또는 편집 {#task_2ADF2A05EB784B8BBAFE293AC8243C46}

작업 컨텍스트

1. **[!UICONTROL Analytics]** &gt; **[!UICONTROL 구성 요소]** &gt; **[!UICONTROL 경고로 이동합니다]**. This takes you to the new [Alert Manager](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/alert-manager.html).

## 이전 경고 마이그레이션 {#concept_7E8179F5EF6E4913B0CE5CF4FF186911}

기존 Analytics 경고의 몇 가지 기능이 2016년 가을에 Analysis Workspace의 일부로 발표되는 새 경고 관리자에 포함되지 않습니다. 다음 표는 사용되지 않는 경고 기능과, 다른 양식의 새 경고 관리자로 마이그레이션되는 몇 가지 경고 기능을 나열합니다.

<!-- 

deprecated_alerts.xml

 -->

<table id="table_9307013B16AC4AC7BFC6F4C440FCFDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이전 경고 기능 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 사용 중단 또는 마이그레이션 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>총계(모든 항목) </p> </td> 
   <td colname="col2"> <p>측정기준 보고서의 모든 항목에 대한 경고를 생성합니다. </p> </td> 
   <td colname="col3"> <p>경우에 따라 측정기준 보고서의 모든 항목에 대한 경고를 생성하든지 또는 집계된 지표 자체에만(측정기준에 적용하지 않음) 경고를 설정하든지 여부에 관계없이 동일한 결과가 발생합니다. 예를 들어, 월별 모든 항목 경고를 "매출" 측정기준에 대해 생성한다고 가정해 보겠습니다. 매출 보고서 실행과 월별 경고 설정으로부터 동일한 결과를 얻는다고 가정합니다. </p> <p>이 상황에서 이전 총계(모든 항목) 경고는 더 이상 사용할 수 없으며 더 간단한 버전인 후자로 마이그레이션됩니다. </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상위 1000개 항목 </p> <p> </p> </td> 
   <td colname="col2"> <p>보고서에서 상위 1000개 항목에 대한 경고를 생성합니다. </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 더 이상 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시간 기반 고유 방문자 수 경고(일일, 주간, 월간 등 고유 방문자 수) </p> <p> </p> </td> 
   <td colname="col2"> <p>시간대별, 일일, 주간, 월간 고유 방문자 수 보고서에 대한 경고를 생성합니다. </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 특정 시간 기반 고유 방문자 수 경고는 더 이상 지원되지 않습니다. 예를 들어, 이전에 일일 고유 방문자 수에 대한 경고를 설정할 수 있었던 위치에서 고유 방문자 수 지표에 대한 일일, 주간 등의 경고를 설정할 수 있게 됩니다. (Analysis Workspace에서 고유 방문자 수 지표를 지원하지만 일일/주간/월간 등의 고유 방문자 수 지표는 지원하지 않습니다.) </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색 </p> </td> 
   <td colname="col2"> <p>검색이 적용된 측정기준 보고서에 대한 경고를 생성합니다. "총계"("모든 항목") 또는 "상위 1000개 항목"에만 적용됩니다. </p> <p> </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 더 이상 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Reports &amp; Analytics에만 해당되는 보고서 </p> </td> 
   <td colname="col2"> <p>다음과 같이 Reports &amp; Analytics에는 있지만 Analysis Workspace 보고서에는 해당하지 않는 몇 가지 보고서에 대한 경고를 생성합니다. 
     <ul id="ul_9A690970A5AE4ED39E664DF23EF3164F"> 
      <li id="li_E2F44EDBA1D945CEBAC4802ED714E7A1">JavaScript </li> 
      <li id="li_B847C6A988854F76824F099681705EC9">경로 길이 </li> 
      <li id="li_4AF656460BC748E8802FAF258D01842F">보트 </li> 
      <li id="li_A300D2803B244774839BEC23D3EB533A">시간대 </li> 
      <li id="li_7A0B4CF92F4D47238B7B329EEC213322">최상위 수준 도메인 </li> 
     </ul> </p> <p> </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 더 이상 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ASI 슬롯이 보고서 세트로 포함된 경고 </p> </td> 
   <td colname="col2"> <p>더 이상 <a href="https://marketing.adobe.com/resources/help/en_US/reference/ASI_slots_admin.html" format="https" scope="external">ASI 슬롯을 생성하거나 편집</a>할 수 없으며 Analysis Workspace에서 사용할 수 없습니다. 따라서 새 경고에서 지원되지 않습니다. </p> <p> </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기여도 지표를 사용하는 경고 </p> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/reference/metrics_participation.html" format="https" scope="external"> 기여도 지표</a>는 Reports &amp; Analytics에서 사용할 수 있지만 현재 Analysis Workspace의 새 경고 시스템에서 사용할 수 없습니다. </p> <p> </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 지정 달력 보고서 세트용 월별 경고 </p> </td> 
   <td colname="col2"> <p>이 기능은 <a href="https://marketing.adobe.com/resources/help/en_US/arb/custom_calendar.html" format="https" scope="external">사용자 지정 월 시작일</a>(전국 소매 연합/NRF 및 사용자 지정 달력 유형)을 가진 보고서 세트용 경고를 설정한 고객에게만 영향을 미칩니다. </p> <p>태양력 또는 수정된 태양력 보고서 세트의 경고에는 영향을 미치지 않습니다. 이전에 이러한 경고는 태양력 달의 첫날(예: 1월 1일, 2월 1일 등)로 전송되었습니다. 이 기능은 예외 항목을 탐지할 때 이전 달의 데이터를 고려하는 새 경고 예외 항목 탐지 기능에서는 작동하지 않습니다. 차후에 사용자 지정 달력에 예약 시스템 지원을 추가하여 경고 및 예약된 프로젝트 모두에서 태양력 달의 첫날에만 보내는 대신 사용자 지정 달력의 첫날에도 보내기를 예약할 수 있도록 합니다. </p> <p> </p> </td> 
   <td colname="col3"> <p>새 경고 관리자에서 아직 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2015년 9월 이후 실행되지 않는 경고 </p> </td> 
   <td colname="col2"> <p>경고가 2015년 9월 이후 실행되지 않는 이유에는 다음 몇 가지가 있습니다. </p> 
    <ul id="ul_15812938A2454537AF6ADDB039DE16BC"> 
     <li id="li_D079A819CEE04F609AF18C09EEE83F0D">경고 관리자의 경고에서 "비활성화"를 클릭했습니다. </li> 
     <li id="li_E23D01FA0B1341AD8BC1DDD16FB1366F">경고에 오류가 발생하여 성공적으로 완료되지 않습니다. </li> 
    </ul> <p> </p> </td> 
   <td colname="col3"> 이러한 경고는 새 시스템으로 마이그레이션되지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> "비활성화"로 표시된 경고 </td> 
   <td colname="col2"> 이 기능을 추가할 계획은 있지만 현재 새 사용자 인터페이스에서 경고를 비활성화 또는 다시 활성화할 수 있는 방법은 없습니다. <p> </p> </td> 
   <td colname="col3"> 이러한 경고는 새 시스템으로 마이그레이션되지 않습니다. </td> 
  </tr> 
 </tbody> 
</table>

