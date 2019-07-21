---
description: 검색 키워드 분류를 표시합니다.
seo-description: 검색 키워드 분류를 표시합니다.
seo-title: 검색 키워드
solution: Analytics
title: 검색 키워드
topic: 보고서
uuid: db 9 d 477 b-b 711-4 b 93-9 c 25-3 aebe 5 f 2 ace 6
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 검색 키워드

검색 키워드 분류를 표시합니다.

**검색 키워드 - 모두**: 사이트를 찾는 데 사용한 각 검색 키워드의 분류를 표시합니다. 목록 위에 있는 열 제목을 클릭하여 페이지 보기 횟수 또는 검색 키워드별로 이 목록을 정렬할 수 있습니다. 사이트에 대한 검색 결과를 보려면 검색 키워드 옆에 있는 확대경을 클릭합니다.

**검색 키워드 - 유료**: 사이트를 찾는 데 사용한 각 유료 검색 키워드의 분류를 표시합니다. 목록 위에 있는 열 제목을 클릭하여 페이지 보기 횟수 또는 검색 키워드별로 이 목록을 정렬할 수 있습니다. 사이트에 대한 검색 결과를 보려면 검색 키워드 옆에 있는 확대경을 클릭합니다.

**검색 키워드 - 자연어**: 사이트를 찾는 데 사용한 각 자연어 검색 키워드의 분류를 표시합니다. 목록 위에 있는 열 제목을 클릭하여 페이지 보기 횟수 또는 검색 키워드별로 이 목록을 정렬할 수 있습니다. 사이트에 대한 검색 결과를 보려면 검색 키워드 옆에 있는 확대경을 클릭합니다.

>[!IMPORTANT]
>
>유료 및 자연어 검색의 경우 검색 엔진이 대부분의 경우 검색 키워드를 레퍼러의 일부로 제공하지 않았습니다. 그 결과, Adobe는 항상 Google(또는 Bing이나 Yahoo!) 도메인을 검색으로 분류합니다. Adobe는 레퍼러의 형식과 컨텐츠(키워드가 없는 경우에도)를 기반으로 도메인을 종종 검색 결과라고 판단할 수 있으므로 이 검색은 사용할 수 없는 키워드로 계산됩니다. [자세히...](https://helpx.adobe.com/analytics/kb/keyword-unavailable.html)

## 할당, 만료 및 특수 값 {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Analysis Workspace </p> <p>Reports &amp; Analytics </p> </th> 
   <th colname="col3" class="entry"> Ad Hoc Analysis </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 지표 할당 </td> 
   <td colname="col2"> <p>원래 값(기본값) </p> <p> [선형]으로 변경될 수 있습니다. </p> </td> 
   <td colname="col3"> 가장 최근(지표의 선형 버전을 사용하여 선형으로 변경할 수 있습니다.) </td> 
   <td colname="col4"> <p>원래 값(기본값) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 값이 다음 시기 이후에 만료 </td> 
   <td colname="col2"> 방문 - 단축할 수 있으나 연장할 수는 없습니다. </td> 
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
   <td colname="col2"> <p>없음: 방문 동안 키워드가 없었던 사이트 전체 합계. </p> "사용할 수 없는 키워드"는 키워드가 검색에서 제거되었고, 데이터 수집으로 전송되지 않는 검색입니다. 이 검색은 일반적으로 고객이 Google 계정에 로그인해 있으면 발생합니다. 유료 및 자연어 검색에 적용됩니다. </td> 
   <td colname="col3"> (낮은 트래픽) 보고할 만큼 충분한 트래픽을 받지 못한 처음 500k를 넘는 값을 나타냅니다. </td> 
   <td colname="col4"> <p> 비어 있음 - "없음"에 해당. 방문 동안 키워드가 없었던 사이트 전체 합계. </p> <p>"사용할 수 없는 키워드"는 키워드가 검색에서 제거되었고, 데이터 수집으로 전송되지 않는 검색입니다. 이 검색은 일반적으로 고객이 Google 계정에 로그인해 있으면 발생합니다. 유료 및 자연어 검색에 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 보고서 내역 {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

| 날짜 | 변경 |
|---|---|
| 2014/1/16 | Data Warehouse를 업데이트하여 Marketing Reports &amp; Analytics에서 사용하는 논리와 일치시켰습니다. 이 날짜 전에는 검색 키워드가 방문 전체에서 지속되지 않았습니다. |

