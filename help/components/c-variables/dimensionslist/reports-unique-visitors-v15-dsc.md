---
description: 사이트에 액세스한 고유 방문자 수를 표시합니다. 각 방문자는 웹 사이트 방문 횟수에 관계 없이 한 번만 카운트됩니다.
seo-description: 사이트에 액세스한 고유 방문자 수를 표시합니다. 각 방문자는 웹 사이트 방문 횟수에 관계 없이 한 번만 카운트됩니다.
seo-title: 고유 방문자 수
solution: Analytics
title: 고유 방문자 수
topic: 보고서
uuid: e70e1a14-b3b9-4d1a-a8a5-a247a443c752
translation-type: tm+mt
source-git-commit: 646d6e01d0f0201c78117ee9bf9ff64fda9a026a

---


# 고유 방문자 수

사이트에 액세스한 고유 방문자 수를 표시합니다. 각 방문자는 웹 사이트 방문 횟수에 관계 없이 한 번만 카운트됩니다.

**샘플 데이터**

이 페이지의 예는 다음 표를 참조하십시오. 같은 방문자가 여기에 표시되어 있습니다.

<table id="table_4F54873A4ED8451494E466C2BDB15B00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 2017/1/1 </th> 
   <th colname="col3" class="entry"> 2017/1/1 </th> 
   <th colname="col4" class="entry"> 2017/1/2 </th> 
   <th colname="col5" class="entry"> 2017/1/2 </th> 
   <th colname="col6" class="entry"> 2017/1/2 </th> 
   <th colname="col7" class="entry"> 2017/1/3 </th> 
   <th colname="col8" class="entry"> 2017/1/4 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>페이지 </p> </td> 
   <td colname="col2"> <p>A </p> </td> 
   <td colname="col3"> <p>C </p> </td> 
   <td colname="col4"> <p>A </p> </td> 
   <td colname="col5"> <p>B </p> </td> 
   <td colname="col6"> <p>C </p> </td> 
   <td colname="col7"> <p>D </p> </td> 
   <td colname="col8"> <p>E </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eVar </p> </td> 
   <td colname="col2"> <p>T, U </p> </td> 
   <td colname="col3"> <p>V </p> </td> 
   <td colname="col4"> <p>W </p> </td> 
   <td colname="col5"> <p> </p> </td> 
   <td colname="col6"> <p>X, Y </p> </td> 
   <td colname="col7"> <p>Z </p> </td> 
   <td colname="col8"> <p>Z </p> </td> 
  </tr> 
 </tbody> 
</table>

## 고유 방문자 보고서 - 트렌드 지표 {#section_372C08A881D34BBF811C1DE0A1460617}

[!UICONTROL 고유 방문자] 보고서는 애드혹 분석에서 비슷하게 동작합니다. 방문이 발생한 각 히트에 대해 해당 히트에서 방문자가 계산됩니다. 각 페이지는 페이지의 방문자에 대한 크레딧을 받습니다.

<table id="table_7D9119045E8243698B6BB2E8C93F6B97"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 페이지 </th> 
   <th colname="col2" class="entry"> 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

또한 각 날짜는 그 날짜의 방문자에 대한 크레딧을 받습니다.

<table id="table_E0D06D9434444947BDA818F61A580B65"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

**[!UICONTROL 고유 방문자 보고서]분류 기준&#x200B;*`Page`*.**

[!UICONTROL 고유 방문자 보고서]에 대해 페이지를 선택할 수 있습니다. 다음 보고서에서는 방문자가 아래와 같은 날짜에 페이지 A를 방문합니다.

<table id="table_2ABA17B19E0D4F92AAB003BE784DA9E0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 기간 기반 고유 방문자(트렌드) {#section_B3502EBF1ACB487AA8E0EFBA9A0561FD}

시간별, 일일, 주별, 월별, 분기별 및 연간 [!UICONTROL 고유 방문자 보고서](트렌드)를 실행할 수 있습니다.

기간 기반 고유 방문자는 지정한 기간의 첫 번째 방문에서만 계산됩니다. 예를 들어, 시간대별 고유 방문자는 지정된 시간의 첫 방문만 계산합니다. 일일 고유 방문자는 지정한 날의 첫 번째 방문만 계산합니다.

<table id="table_FF14F05CDFDA4F2E92A62D9D751A1CAA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 주간 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

일일 고유 방문자에 대해 다음 보고서가 표시됩니다.

<table id="table_4E44BC4722064501A5B648BE80ED8E60"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 일일 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>4 </p> </td> 
  </tr> 
 </tbody> 
</table>

보고서의 날짜 범위에 따라 지표 합계가 변경될 수 있습니다. 마케팅 보고서는 날짜 범위가 시작될 때부터 시간 기반 고유 방문자를 계산하기 시작합니다. 예를 들어, 날짜 범위가 1월 2일에서 1월 3일까지인 경우는 주간 고유 방문자에 대해 다음 결과가 표시됩니다.

<table id="table_B695708BB22949E7BA293FE492D2EEA0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 주간 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

**세그멘테이션**

세그멘테이션을 사용하여 이전 날짜 대신 나중 날짜가 포함되도록 날짜 범위를 변경할 수 있습니다. 예를 들어, 날짜 범위가 여전히 1월 2일에서 1월 3일까지라고 가정합니다(위 표에 표시). 페이지 = C인 세그먼트를 적용하면 1월 2일은 세그먼트에 들어가지 않으며 주간 고유 방문자의 첫 번째 히트는 1월 3일이 됩니다. 대신 페이지 = D인 세그먼트를 적용하면 1월 2일과 1월 3일이 모두 제외됩니다. 결과가 주별 고유 보고서에 표시되지 않으며 합계에서 제외됩니다.

**기간 기반 고유 방문자 보고서 **

이러한 보고서는 특정 페이지, prop 및 특성(예: 페이지 = A)을 사용합니다.

[!UICONTROL 페이지 보고서]에 기간 기반 고유 방문자 지표로 트렌드를 표시하는 경우를 가정합니다. 기간 기반 고유 방문자 보고서에 대해 선택된 분류 또는 변수가 있으면 마케팅 보고서는 방문자 및 특성 쌍의 모든 고유 인스턴스를 계산합니다. 방문자의 첫 번째 히트에 대해서는 이 경우가 전의 예들과 다르지 않습니다. 그 뒤의 히트에 대해, 이 보고서는 페이지가 다른 경우 위 보고서에 포함되지 않은 히트를 포함합니다.

페이지 = A인 주간 고유 방문자의 경우, 마케팅 보고서는 1월 2일을 합계에서 제외합니다. 이러한 제외는 마케팅 보고서가 이미 1월 1일에 주간 고유 방문자를 계산했기 때문에 발생합니다. 다음은 페이지 = A인 주간 고유 방문자 보고서입니다.

<table id="table_9C5E00029C7340B28D76696E84F66511"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 주간 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

페이지 = B인 주간 고유 방문자의 경우는 다음과 같이 발생이 1월 2일에만 있습니다.

<table id="table_262150BECCB74120B58F506F4BC6F629"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 방문 - 주간 고유 방문자 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 비트렌드 보고서의 기간 기반 고유 방문자 지표 {#section_90B784F4E49F4930B3F0923B95958BA2}

[!UICONTROL 페이지 보고서]의 주간 고유 방문자 지표와 같이, 비트렌드 보고서에 기간 기반 고유 방문자를 추가할 수 있습니다.

<table id="table_8651A42696B0404CAEAE0FC5522CC1C9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 페이지 </th> 
   <th colname="col02" class="entry"> 방문 날짜 </th> 
   <th colname="col2" class="entry"> 방문 - 주간 고유 방문자 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col02"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B </p> </td> 
   <td colname="col02"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C </p> </td> 
   <td colname="col02"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D </p> </td> 
   <td colname="col02"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E </p> </td> 
   <td colname="col02"> <p>1월 5일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col02"> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL 페이지 보고서]의 일일 고유 방문자 지표에는 다음이 표시됩니다.

<table id="table_04C7C305C2B945D6A79A6B80F48A4BF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 페이지 </th> 
   <th colname="col02" class="entry"> 방문 날짜 </th> 
   <th colname="col2" class="entry"> 방문 횟수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col02"> <p>1월 1일 </p> </td> 
   <td colname="col2"> <p>2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B </p> </td> 
   <td colname="col02"> <p>1월 2일 </p> </td> 
   <td colname="col2"> <p>2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C </p> </td> 
   <td colname="col02"> <p>1월 3일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D </p> </td> 
   <td colname="col02"> <p>1월 4일 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col02"> <p> </p> </td> 
   <td colname="col2"> <p>일일 고유 방문자 4명 </p> </td> 
  </tr> 
 </tbody> 
</table>

한 특성을 다른 특성으로 분류하는 경우(예: *`page`* by *`eVar`*), Analytics allocates a period-based Unique Visitor for each unique instance of the period and page (or the attribute being correlated).

페이지 A를 eVar T, U로 분류하면, 페이지 A를 1월 1일에 봤기 때문에 1월 2일이 제외됩니다. 주간 고유 방문자에 대해 다음 보고서가 표시됩니다.

<table id="table_328A6F2E920A44B3B55A6E6A630F6DBD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar </th> 
   <th colname="col2" class="entry"> 주간 고유 방문자 수 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>합계 </p> </td> 
   <td colname="col2"> <p>1 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 영구적 쿠키 {#section_81E139F08AEB4E30A06472856975EA1E}

영구적 쿠키는 Adobe가 후속 방문에서 방문자를 식별할 수 있도록 방문 사이에 방문자의 컴퓨터에 보존됩니다. To see the percentage of users who do and do not accept persistent cookies, select **[!UICONTROL Filter]** &gt; **[!UICONTROL Persistent Cookies]**.

아래의 세부 정보와 그래프에서는 영구적 쿠키와 비영구적 쿠키 방문자를 모두 보여 줍니다. 대개 비영구적 쿠키 방문자의 수는 무시해도 될 정도입니다.
