---
description: 데이터 피드를 사용한 일반 지표 계산 방법을 설명합니다.
keywords: 데이터 피드; 작업; 지표; pre column; 이후 열; 보트; 날짜 필터링; 이벤트 문자열; common; 공식
seo-description: 데이터 피드를 사용한 일반 지표 계산 방법을 설명합니다.
seo-title: 지표 계산
solution: Analytics
title: 지표 계산
topic: Reports & Analytics
uuid: A 45 EA 5 BB -7 C 83-468 F-B 94 A -63 Add 78931 D 7
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 지표 계산

데이터 피드를 사용한 일반 지표 계산 방법을 설명합니다.

<!--Meike, I commented out this heading because it contains no content, and I'm troubleshooting a dita error-Bob
## Pre vs. Post column {#section_19967AF2FD9D44D6A8EC30F77E71F2ED}
-->

## 보트 {#section_06753B95800F47668AAF52E7227F27C8}

보트는 보고서 세트에 대해 정의된 [보트 규칙](https://marketing.adobe.com/resources/help/en_US/reference/?f=bot_rules)에 따라 데이터 피드에서 제외됩니다.

## 날짜 필터링 {#section_3BFF4F7EED1F4FA69EBF12BF98B347E8}

`date_time` 필드를 필터링함으로써 포함시킬 날짜 범위의 행을 포함시키십시오. `date_time` 필드는 사람이 읽을 수 있으며 `YYYY-MM-DD HH:MM:SS`보고서 세트의 시간대로 조정됩니다. For example, `date_time starts with "2013-12"` includes hits from December 2013.

## 이벤트 문자열 {#section_87B686512EFD4A6CA072165CB28A130A}

The event string in `event_list` and `post_event_list` contains a comma-delimited list of events, which may have a value and/or a unique ID. 중복 제거가 되어 있고 이미 같은 ID를 가진 중복 이벤트를 제거하는 로직이 적용된 `post_event_list`에서 모든 처리를 수행할 것을 권장합니다([이벤트 일련화](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=c_event_serialization) 참고).

매핑 명명을 위한 이벤트 ID의 경우 데이터 피드를 통해 제공된 이벤트 조회를 참조하십시오.

이벤트에 대한 자세한 정보는 [이벤트](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_events)에서 참조하십시오.

## 일반 지표를 위한 공식 {#section_E26A01C234484857BF8C74443222AE41}

다음 표는 몇 가지 일반 지표를 계산하는 방법을 설명합니다.

<table id="table_814EA73C01EE4B2CA3CEB2839E19ADF9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 지표 </th> 
   <th colname="col2" class="entry"> 계산 방법 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 페이지 보기 횟수 </td> 
   <td colname="col2"> <p> <code>post_pagename</code> 또는 <code>post_page_url</code>에 값이 있을 때를 카운트하여 페이지 보기 횟수를 계산할 수 있습니다 . </p> 
    <p>비슷한 로직을 사용하여 사용자 지정 링크를 카운트할 수 있습니다. </p> 
    <ul id="ul_8DFBEE3ED30C465D8E55B1F3880D5263"> 
     <li id="li_009F2B7E3F9443889AE95B3358169444"> <code> post_page_event = 100</code>으로 사용자 지정 링크를 카운트합니다. </li> 
     <li id="li_866DA2F5C2404347863CD1417F822FE8"> <code> post_page_event = 101</code>로 다운로드 링크를 카운트합니다. </li> 
     <li id="li_4BC6E62CE8B1474DB22448FA32C9EE01"> <code> post_page_event = 102</code>로 종료 링크를 카운트합니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문 횟수 </td> 
   <td colname="col2"> 
    <ol id="ol_FE1831195A474650B07D7820DCD38728"> 
     <li id="li_274590E937A142D19B204768B1F10325"><code>exclude_hit &gt; 0</code>인 모든 행을 제외합니다 . </li> 
     <li id="li_038B8FF66EA44E138C8A8932DA7B39E5"><code>hit_source = 5,7,8,9</code>가 있는 모든 행을 제외합니다 . 5,8 및 9는 데이터 소스를 사용하여 업로드된 요약 행입니다. 7은 방문 및 방문자 카운트에 포함되지 않아야 하는 거래 ID 데이터 소스 업로드를 나타냅니다. see <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> 히트 출처 조회 </a>. </li> 
     <li id="li_7FCD9BDF4D8547719420B34BA48BFA2D"><code>post_visid_high</code>, <code>post_visid_low</code>, <code>visit_num</code> 및 <code>visit_start_time_gmt</code>*를 결합합니다. 고유한 조합 개수를 카운트합니다. </li> 
    </ol> <p>*드문 경우이긴 하지만 인터넷 불안정, 시스템 불안정 또는 사용자 지정 방문자 ID의 사용으로 인해 같은 방문자 ID에 대해 같은 <code>방문</code>이 아닌 중복된 <a href="https://marketing.adobe.com/resources/help/en_US/reference/?f=metrics_visit" format="http" scope="external">visit_num</a> 값이 있을 수 있습니다 . 결과 문제가 발생하지 않도록 하려면 방문 횟수를 카운트할 때 <code>visit_start_time_gmt</code>도 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 수 </td> 
   <td colname="col2"> 
    <ol id="ol_E2BC9235A3164EF5936EFC5D9E9327D0"> 
     <li id="li_2C145CA54EBF4B358FC7DC78D8DA577D"><code>exclude_hit &gt; 0</code>인 모든 행을 제외합니다 . </li> 
     <li id="li_9EF364652A214A4D9B66552BC6BBE527"><code>hit_source = 5,7,8,9</code>가 있는 모든 행을 제외합니다 . 5,8 및 9는 데이터 소스를 사용하여 업로드된 요약 행입니다. 7은 방문 및 방문자 카운트에 포함되지 않아야 하는 거래 ID 데이터 소스 업로드를 나타냅니다. see <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> 히트 출처 조회 </a> </li> 
     <li id="li_4AB5129315644A29987E8FCB9C9F9C39"><code>post_visid_high</code>와 <code>post_visid_low</code>를 결합합니다 . 고유한 조합 개수를 카운트합니다. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 인스턴스 </td> 
   <td colname="col2"> <p>히트에 대한 이벤트가 설정된 경우 <code>post_event_list</code>에 이벤트가 포함됩니다. <code>post_event_list</code>는 중복 제거되어 있으며 이벤트 인스턴스 결정에 권장됩니다. </p> <p>예: </p> 
    <code>post_ event_ list = 1,200 </code>
  <p><code>purchase</code> 및 <code>event1</code> 인스턴스를 표시합니다 . </p> 
    <ol id="ol_84B529A668A54686957D1EB36D944467"> 
     <li id="li_F953D7668C704C1AB7970123E369472A"><code>exclude_hit &gt; 0</code>인 모든 행을 제외합니다 . </li> 
     <li id="li_65B0B504DB654479844EAE490D9283EB"><code>hit_source = 5,8,9</code>가 있는 모든 행을 제외합니다 . 이것은 데이터 소스를 사용하여 업로드된 요약 행입니다. see <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> 히트 출처 조회 </a>. </li> 
     <li id="li_FB1C31048EC7415088F41E8CDC01AEBD">이벤트 조회 값이 <code>post_event_list</code>에 표시되는 횟수를 카운트합니다 . </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar 인스턴스 </td> 
   <td colname="col2"> <p>히트에 대해 eVar가 설정된 경우 <code>event_list</code>에 이 eVar의 인스턴스가 포함됩니다. </p> <p>예: </p> 
    <code>post_ event_ list &amp; amp; nbsp; = &amp; amp; nbsp; 100,101,106 </code>
  <p><code>eVar1</code>, <code>eVar2</code> 및 <code>eVar7</code> 인스턴스를 표시합니다 . 이 3가지 eVars에 대한 값이 히트에 대해 설정된 것을 의미합니다. </p> <p>eVars에 대한 인스턴스를 계산하려면 위의 <i>Event instances</i>에 설명된 것과 같은 로직을 사용하되 eVar 조회가 <code>post_event_list</code>에 나타나는 횟수를 카운트합니다 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 체류 시간 </td> 
   <td colname="col2"> <p>체류 시간을 계산하려면, 방문별 히트를 그룹화한 다음 해당 방문 내의 히트 번호에 따라 순서를 지정합니다. </p> 
    <ol id="ol_946E7CD6005A42EB9A4B79268BF84066"> 
     <li id="li_D109FAF4686D4935B7A6DCA5D383612F"><code>exclude_hit &gt; 0</code>인 모든 행을 제외합니다 . </li> 
     <li id="li_D88F3691DB6746EBA84AA52841E56803"><code>visid_high</code>, <code>visid_low</code> 및 <code>visit_num</code>을 연결하여 방문에 대한 히트를 그룹화합니다 . </li> 
     <li id="li_08792F3BDFEA4DA29E0983C4BE65D73B"><code>visit_page_num</code>의 각 방문에 대한 히트의 순서를 지정합니다 . </li> 
     <li id="li_4B956734DBB84603B86DDA6A2B0B41A0"><a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-page-event.md#concept_A3AC076C3728445EB4CC572A6EDA5263" format="dita" scope="local"> page_ event </a>를 사용하여 원하는 히트 유형을 필터링합니다. </li> 
     <li id="li_2C5AC0477CFC409B8F169079354C8226">체류 시간을 추적할 값이 설정된 히트를 찾습니다. 예: 
      <code>히트 1: post_ prop 1 = RED 히트 2: post_ prop 1 = blue </code>
  </li> 
     <li id="li_20106B322F7B45CE8D2FBD9B0CB3D60D">히트 2에 대한 <code>post_cust_hit_time</code>에서 히트 1에 대한 <code>post_cust_hit_time</code>을 빼서 두 히트 간의 시간(초)을 결정합니다. 결과는 <code>post_prop1=red</code>에 대한 체류 시간입니다. 결과가 음수이면, 히트를 비순차적으로 받은 것이며 이 계산은 버려야 합니다. </li> 
    </ol> <p>이 논리는 다른 값에 대한 체류 시간을 계산하는 데까지 확장할 수 있습니다. 체류 시간 계산 시, Analytics에서는 체류 시간을 이 값이 <code>track</code>(<code>page_event=0</code>) 또는 <code>trackLink</code>(<code>page_event=10|11|12</code>) 호출에서 설정된 시간에서 다음 페이지 보기(<code>track</code> 호출) 시간까지를 기반으로 계산합니다. </p> <p>특정 기간에 대한 체류 시간 보고 시, Marketing Reports &amp; Analytics과 Ad Hoc Analysis에서는 기간의 시작 및/또는 종료 날짜에 월별 제한이 있을 때를 제외하고 보고 기간을 지난 히트를 평가하여 보고 기간 내 값에 대한 체류 시간을 결정합니다. 이러한 계산의 복잡성으로 인해 체류 시간 지표를 정확히 일치시키기가 어려울 수 있습니다. Data Warehouse에서는 보고 기간 이후의 히트를 평가하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 매출액, 주문, 판매량 </td> 
   <td colname="col2"> <p>통화 변환은 보고서 세트의 설정에 따라 <code>post_product_list</code>에 적용되므로 해당 열을 사용하는 것이 권장됩니다. </p> 
    <ol id="ol_03D62086EDDE42AD82049830D85FDC69"> 
     <li id="li_2A5B8205EA30492986C35DC382B91F16"><code>exclude_hit &gt; 0</code>인 모든 행을 제외합니다 . </li> 
     <li id="li_6417C228AC414B01A30F85BE4842ED3C"><code>hit_source = 5,8,9</code>가 있는 모든 행을 제외합니다 . 5~9는 데이터 소스를 사용하여 업로드한 요약 행을 나타냅니다. see <a href="../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42" format="dita" scope="local"> 히트 출처 조회 </a>. </li> 
     <li id="li_C48F91C74F5E4286B5F0B285E33AF733"><code>duplicate_purchase = 1</code>인 행의 구매 데이터를 무시합니다. 이 플래그는 구매가 중복(동일한 <code>purchaseID</code>의 히트가 이미 기록되었음을 의미)임을 가리킵니다. </li> 
     <li id="li_FA1639FEF516419BA1BFDC37B063B346"> <p><code>post_product_list</code>는 <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=c_products" format="http" scope="external">s.products</a>와 같은 구문을 사용하므로 이 문자열을 분석하여 지표를 계산할 수 있습니다. 예: </p> 
      <code>; 크로스 트레이너1; 69.95; 운동용 Socks; 10; 29.99 </code>
  <p>이 문자열을 분석함으로써 크로스 트레이너 1쌍이 $69.95에 구입되었고 이 구입의 총 매출은 $99.94임을 알 수 있습니다. </p> </li> 
    </ol> <p>참고: 분석을 통해 제품 매출액을 포함한 통화 이벤트가 이벤트 문자열을 따라 전달될 수 있으므로 제품 문자열에 없는 매출을 고려할 필요가 있습니다. <i>s.events</i>에서 <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=c_events" format="http" scope="external">숫자/통화 이벤트</a>를 보십시오 . </p> </td> 
  </tr> 
 </tbody> 
</table>
