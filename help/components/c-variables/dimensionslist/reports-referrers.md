---
description: 방문자가 사이트에 오기 전에 있었던 도메인 또는 URL, 방문자가 웹 사이트를 검색하는 데 사용한 방법 및 이러한 참조 위치에서 이루어진 사이트 방문 횟수를 보여줍니다.
seo-description: 방문자가 사이트에 오기 전에 있었던 도메인 또는 URL, 방문자가 웹 사이트를 검색하는 데 사용한 방법 및 이러한 참조 위치에서 이루어진 사이트 방문 횟수를 보여줍니다.
seo-title: 레퍼러
solution: Analytics
title: 레퍼러
topic: 보고서
uuid: E 63 B 47 B 4-49 F 3-43 AF -8409-3272 BEC 0484 E
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 레퍼러

방문자가 사이트에 오기 전에 있었던 도메인 또는 URL, 방문자가 웹 사이트를 검색하는 데 사용한 방법 및 이러한 참조 위치에서 이루어진 사이트 방문 횟수를 보여줍니다.

예를 들어 방문자가 사이트 A에서 링크를 클릭하여 특정 사이트에 도달하는 경우 사이트 A가 도메인의 일부로 정의되어 있지 않으면 사이트 A가 레퍼러입니다.  구현 시 구현 컨설턴트가 웹 사이트의 일부인 도메인과 URL을 정의할 수 있도록 도와줄 수 있습니다. (이러한 변경은 구현 후 수행할 수 있습니다.)

정의된 도메인과 URL의 일부가 아닌 도메인 또는 URL은 레퍼러로 간주됩니다. 예를 들어, 웹 페이지 A와 웹 페이지 B는 내부 URL 필터에 추가되지만 웹 페이지 C는 추가되지 않습니다. 이 경우, 웹 페이지 C는 레퍼러로 간주됩니다.

## 할당, 만료 및 특수 값 {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Marketing Reports &amp; Analytics (SiteCatalyst) </th> 
   <th colname="col3" class="entry"> Ad hoc analytics </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 지표 할당 </td> 
   <td colname="col2"> 최근 </td> 
   <td colname="col3"> 최근 </td> 
   <td colname="col4"> 최근 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 값이 다음 시기 이후에 만료 </td> 
   <td colname="col2"> 방문 </td> 
   <td colname="col3"> 방문 </td> 
   <td colname="col4"> 방문 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 값 제한 </td> 
   <td colname="col2"> 제한 없음(차후 출시 버전에서 변경될 수 있음) </td> 
   <td colname="col3"> 제한 없음(차후 출시 버전에서 변경될 수 있음) </td> 
   <td colname="col4"> 없음 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 특수 값 </td> 
   <td colname="col2"> <p>없음: 방문 동안 레퍼러가 없었던 사이트 전체 합계. </p> </td> 
   <td colname="col3"> <p>없음: 방문 동안 레퍼러가 없었던 사이트 전체 합계. </p> </td> 
   <td colname="col4"> <p> 비어 있음 - "없음"에 해당. 방문 동안 레퍼러가 없었던 사이트 전체 합계. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 내용 {#section_B83A3571D64E4E7792712FAF740D7955}

* 레퍼러, 레퍼러 유형 및 참조 도메인은 방문의 첫 번째 히트에서, 또는 레퍼러가 외부인 방문 동안(예: 방문자가 사이트를 떠나고, 검색 엔진을 사용한 다음 첫 번째 방문이 만료되기 전에 사이트로 돌아오는 경우) 설정됩니다. 이 값들은 동시에 설정되며, 방문 전체에서 지속됩니다.
* 내부 URL은 필터링됩니다. 내부 URL 필터에 대응하지 않는 레퍼러만 이 보고서에 있습니다.
* 해당 지표를 Ad Hoc Analysis에서 레퍼러 인스턴스라고 합니다.
* 입력/책갈피 표시 값은 레퍼러 보고서에 포함되지 않습니다. 이것은 사이트 전체 방문이 이 보고서의 방문과 일치하지 않음을 의미합니다.

## 보고서 내역 {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

<table id="table_9DFA79EC6A5A48648F2FB5418E1752DB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 </th> 
   <th colname="col2" class="entry"> 변경 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 2014/1/16 </td> 
   <td colname="col2"> Data Warehouse를 업데이트하여 Marketing Reports &amp; Analytics에서 사용하는 논리와 일치시켰습니다. 이 날짜 전에는 검색 키워드가 방문 전체에서 지속되지 않았습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2012년 6월 19일 </td> 
   <td colname="col2"> <p> 2012년 7월 이전 "없음"에는 모든 모바일 트래픽, 입력/책갈피 표시 및 [JavaScript 없음]인 방문이 포함됩니다. 2012년 7월 이후 "없음"에는 방문의 첫 번째 페이지에 대한 [JavaScript 없음]인 히트만 포함됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

