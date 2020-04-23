---
description: 링크 보고서는 현재 페이지에 있는 링크에 대해 보고합니다. 이 보고서는 해당 페이지에 대해 수집된 모든 링크에 대해 보고하지 않습니다.
title: 링크 보고서
topic: Activity map
uuid: 1e7ca5d8-d144-4a21-a2f9-e05bd3232c59
translation-type: tm+mt
source-git-commit: 6b27755178d156b1eaf159640d466bd84659983d

---


# 링크 보고서

링크 보고서는 현재 페이지에 있는 링크에 대해 보고합니다. 이 보고서는 해당 페이지에 대해 수집된 모든 링크에 대해 보고하지 않습니다.

페이지에 있는 링크 수 보고서는 링크에 대한 표 형식으로 표시합니다. 때로 단일 보기에서 등급이 지정된 링크 클릭(또는 기타 지표)을 볼 수 있습니다. 이렇게 하면 한 링크를 다른 링크와 더 잘 비교할 수 있습니다. 페이지의 모든 링크(링크 ID별), 클릭 정보(# 및 %) 및 페이지의 영역을 포함한 페이지에 있는 링크 수 보고서를 만듭니다. Activity Map 도구 모음에서 페이지에 있는 링크 수 보고서 단추를 클릭합니다.

The **[!UICONTROL Links On Page]** report opens below the browser frame in the Activity Map dashboard.

## 표준 모드 {#section_C8D2A1C07A2A4E3A8F84AC9240603FA7}

![](assets/links_in_page.png)

표준 모드에서 &quot;페이지에 있는 링크 수&quot; 보고서는 전체 날짜 범위에 대해 집계된 하루 범위에서 여러 날 사이의 링크 데이터를 보여줍니다. 각 링크에 대해 다음 정보가 표시됩니다.

<table id="table_3DE41B2CFA644B70AF802A3123CE51D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 열 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 등급 </td> 
   <td colname="col2"> 페이지의 등급. 표준 모드에서 등급 값은 클릭하는 열에 관계없이 동일하게 유지됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 링크 ID </td> 
   <td colname="col2">The link's primary ID (for more information on how primary ID is defined by the <a href="/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md">New Link Tracking Methodology</a>) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 클릭 수 </td> 
   <td colname="col2"> 지정된 링크에 대한 원시 클릭 수와 해당 페이지의 총 클릭 수 비율입니다. 사용자가 도구 모음에서 다른 지표를 선택하면 링크 보고서가 해당 지표에 대해 보고합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지역 </td> 
   <td colname="col2"> 링크가 있는 페이지의 영역을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 가시성 </td> 
   <td colname="col2">링크의 가시성 상태와 관련이 있습니다. 다음 두 가지 값을 사용할 수 있습니다. 
    <ul id="ul_BABCC0F64145407C9D439150A6898E6D">
     <li id="li_9AF0479BDCEB4A44A37292FAABFA83A5"><b>숨김</b>:링크가 현재 페이지에 있지만 최종 사용자는 볼 수 없습니다(탐색 메뉴의 하위 메뉴처럼 사용자가 상위 메뉴의 맨 위를 마우스로 가리킬 경우에만 표시됨). </li>
     <li id="li_C6FA4EC27EDD4341AB9821E2B4BC9E60"><b>표시</b>:링크가 현재 페이지에 표시됩니다. 그러나 접힌 항목 아래에 표시될 수 있습니다.사용자는 페이지를 스크롤하여 보아야 볼 수 있습니다. </li>
    </ul><p>참고: 링크가 "숨김"으로 설정되어 있다면, 그에 대해 표시되는 오버레이가 없습니다. </p></td> 
  </tr> 
 </tbody> 
</table>

**데이터 필터**

When you want to zero in on a specific link, you can search for a related term in the **[!UICONTROL Filter Data]** field. 검색과 일치하는 링크에만 오버레이가 있습니다. 필터가 없으면 Activity Map 설정에 지정된 [오버레이가](/help/analyze/activity-map/activitymap-overlay-settings.md) 표시됩니다.

## 라이브 모드 {#section_AC1967217B5A4532ACB01D33636F6770}

라이브 모드에서 페이지에 있는 링크 수 보고서에는 몇 분에 걸친 트렌드 데이터가 표시됩니다.

![](assets/links_on_page.png)

<table id="table_61D1FB0F02894055A1AB394DE4FE4742"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 열 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 등급 </td> 
   <td colname="col2"> 페이지의 등급. 그라데이션 또는 버블 오버레이의 경우, 등급 값은 클릭하는 열에 관계없이 동일하게 유지됩니다. 승자/패자 오버레이의 경우, 해당 등급 값은 가장 많이 얻거나 잃은 링크에 따라 변경됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 링크 ID </td> 
   <td colname="col2">링크의 기본 ID입니다. For more information on how the primary ID is defined by the New <a href="/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md"> Link Tracking Methodology</a>. </td>
  </tr> 
  <tr> 
   <td colname="col1"> 링크 클릭 횟수 </td> 
   <td colname="col2"> 선택한 기간에 대한 총 클릭 수. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> % 변경 </td> 
   <td colname="col2"> 현재 기간 링크 지표와 이전 기간 링크 지표 간의 % 변경. 음수 % 변화는 빨간색으로, 양수로 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 트렌드 </td> 
   <td colname="col2"> 수집된 모든 기간에 대한 라인 차트. 현재 선택한 기간은 녹색 마커로 표시됩니다. 현재 마우스로 가리킨 기간은 빨간색 마커로 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지역 </td> 
   <td colname="col2"> 링크가 있는 페이지의 영역을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 가시성 </td> 
   <td colname="col2">링크의 가시성 상태와 관련이 있습니다. 다음 두 가지 값을 사용할 수 있습니다. 
    <ul id="ul_B10C55ED4D3C4CF99506DC467E2E7CFB">
     <li id="li_EA646722A51041CC9E62C56DEF92C81F">숨김:링크는 현재 페이지에 있지만 사용자에게 보이지 않습니다(예: 페이지를 로드한 후 나타나는 링크). </li>
     <li id="li_F9543614C2894003AC9984A7404E2785">표시:링크가 현재 페이지에 표시됩니다. 그러나 접힌 항목 아래에 표시될 수 있습니다.페이지를 스크롤하여 보아야 볼 수 있습니다. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

## 정렬 및 필터링 {#section_4B8E8233C21247CAA70DAEC2156548AD}

경우에 따라 특정 페이지 영역(예: 왼쪽 패널)의 결과만 분석하여 웹 페이지의 특정 영역의 컨텐츠를 구성하는 방법을 결정해야 합니다.

이를 위해 페이지에 있는 링크 수 보고서의 링크에 대한 정렬 및 필터링 기능을 만들었습니다. 필터 필드를 통해 필터링할 수 있으며 검색 용어가 링크 ID 열 및 링크 영역 열에 적용됩니다. 정렬 기능은 통화(등급, 링크 ID, 클릭 수, 시간에 따라 변경, 영역, 가시성)를 클릭하여 사용할 수 있으며 오름차순과 내림차순이 모두 가능합니다. 링크가 페이지에 있는 링크 수 보고서에서 필터링되면 오버레이가 웹 사이트에서 사라집니다.
