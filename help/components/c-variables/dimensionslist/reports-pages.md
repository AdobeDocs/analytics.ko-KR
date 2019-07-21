---
description: 트래픽이 가장 많은 사이트 페이지를 기준으로 페이지 등급을 매깁니다. 비즈니스 질문이 페이지의 수량적 데이터에 대한 것인 경우 이 보고서에 올바른 지표를 추가하여 이 질문에 응답할 수 있습니다.
seo-description: 트래픽이 가장 많은 사이트 페이지를 기준으로 페이지 등급을 매깁니다. 비즈니스 질문이 페이지의 수량적 데이터에 대한 것인 경우 이 보고서에 올바른 지표를 추가하여 이 질문에 응답할 수 있습니다.
seo-title: Pages
solution: Analytics
title: Pages
topic: 보고서
uuid: 6435 E 262-E 734-4 C 15-AF 5 B -173799 D 5 CC 43
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pages

트래픽이 가장 많은 사이트 페이지를 기준으로 페이지 등급을 매깁니다. 비즈니스 질문이 페이지의 수량적 데이터에 대한 것인 경우 이 보고서에 올바른 지표를 추가하여 이 질문에 응답할 수 있습니다.

## 할당, 만료 및 특수 값 {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

Reports &amp; Analytics에서 페이지 보고서의 지표는 선형 할당을 사용합니다. 예를 들어, 매출액은 구매 이벤트 전에 본 모든 페이지 간에 분할됩니다. 이것은 장바구니 추가와 같이, 한 페이지에서만 발생할 것으로 예상할 수 있는 일부 지표에 대해 혼란을 초래할 수 있습니다.

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry">보고서 &amp; <p>Analytics </p> </th> 
   <th colname="col3" class="entry"> Ad Hoc Analysis </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
   <th colname="col5" class="entry"> Analysis Workspace </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 지표 할당 </td> 
   <td colname="col2"> 선형 </td> 
   <td colname="col3"> 할당은 각 측정기준에만 적용됩니다. 기본값은 마지막 터치 할당이지만, '페이지 이름' 측정기준은 예외입니다. 사용자 지정 이벤트를 '페이지 이름'에 적용하는 경우 정확한 히트 할당이 됩니다. </td> 
   <td colname="col4"> <p>동일한 페이지 보기에서 설정된 값 </p> </td> 
   <td colname="col5"> <p>동일한 페이지 보기에서 설정된 값 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 값이 다음 시기 이후에 만료 </td> 
   <td colname="col2"> 페이지 보기 </td> 
   <td colname="col3"> 페이지 보기 </td> 
   <td colname="col4"> 페이지 보기 </td> 
   <td colname="col5"> 페이지 보기 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 값 제한 </td> 
   <td colname="col2"> <p>월당 최초 500k 고유 + 트래픽 관련 새 값 </p> </td> 
   <td colname="col3"> <p>월당 최초 500k 고유 + 트래픽 관련 새 값 </p> </td> 
   <td colname="col4"> 없음 </td> 
   <td colname="col5"> <p>월당 최초 500k 고유 + 트래픽 관련 새 값 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 특수 값 </td> 
   <td colname="col2"> <p>(낮은 트래픽) 보고할 만큼 충분한 트래픽을 받지 못한 처음 500k를 넘는 값을 나타냅니다. </p> </td> 
   <td colname="col3"> <p>(낮은 트래픽) 보고할 만큼 충분한 트래픽을 받지 못한 처음 500k를 넘는 값을 나타냅니다. </p> </td> 
   <td colname="col4"> none </td> 
   <td colname="col5"> <p>(낮은 트래픽) 보고할 만큼 충분한 트래픽을 받지 못한 처음 500k를 넘는 값을 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

Reports &amp; Analytics에서 사용자 지정 이벤트를 페이지 보고서의 지표로 적용하는 경우 선형 할당이 적용됩니다.

즉, 이벤트가 s.tl() 호출과 함께 전송된 경우 이전 s.t() 호출의 선형 할당을 얻습니다. 예:

| 페이지 이름 | Page_event | 이벤트 |
|---|---|---|
| 페이지 1 | **s.t()** |  |
| 페이지 1 | s.tl() | 이벤트 1 |
| 페이지 1 | s.tl() | 이벤트 1 |
| 페이지 1 | s.tl() | 이벤트 1 |
| 페이지 2 | **s.t()** |  |
| 페이지 2 | **s.t()** |  |
| 페이지 2 | s.tl() | 이벤트 1 |

이 시나리오의 경우 페이지 보고서에서 다음 할당을 얻습니다.

| Pages | 페이지 보기 횟수 | 이벤트 1 |
|---|---|---|
| 페이지 1 | 1 | 1+1+1+1/3 = 3.33 |
| 페이지 2 | 2 | 2/3 = 0.67 |

s.tl 호출 시 이벤트가 전송되더라도 전송된(s.t() 호출) 이벤트 이전에 본 페이지는 부분 크레딧을 얻습니다.

## 참고 {#section_47B0F4746D4847AC9E8697127063F4D0}

* 페이지 이름이 없으면 URL이 사용됩니다.
* 페이지 이름, 페이지 URL 또는 이벤트 목록(전자 상거래 이벤트 없음)이 없는 히트가 있는 경우 이 히트는 제외됩니다.
* 페이지의 분류에는 지속되는 값이 있었던 모든 페이지가 표시됩니다.

