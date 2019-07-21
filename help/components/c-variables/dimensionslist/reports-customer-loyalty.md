---
description: 고객 충성도는 고객의 구매 패턴을 보여줍니다.
seo-description: 고객 충성도는 고객의 구매 패턴을 보여줍니다.
seo-title: 고객 충성도
solution: Analytics
title: 고객 충성도
topic: 보고서
uuid: 7 DC 30 B 57-7 B 18-4228-A 6 AB -6 EB 66 B 3 D 9402
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 고객 충성도

고객 충성도는 고객의 구매 패턴을 보여줍니다.

이 보고서는 네 가지 충성도 카테고리를 기반으로 고객의 구매 패턴을 표시합니다.

* 고객이 아님
* 새 고객
* 재방문 고객
* 단골 고객

이 보고서에서 비구매자 지표를 볼 수 있지만(예: 사용자 지정 이벤트, 장바구니 이벤트 등) 카테고리는 항상 주문 개수를 기반으로 합니다. 예를 들어 방문자가 보고서에 내부 검색이라는 사용자 지정 이벤트를 추가할 수 있습니다. 두 번의 내부 검색을 수행한 방문자 수가 아닌 이전에 두 번 구매한 경험이 있는 방문자가 수행한 내부 검색 수가 [!UICONTROL 재방문 고객] 라인 항목에 표시됩니다.

**고객 충성도 처리**

다음 표는 Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis 및 Data Warehouse에서 현재 고객 충성도를 처리하는 방법을 정의합니다.

<table id="table_E6A5CA96BE5C47F29F09688A4D41BC60"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>2016년 5월 19일 이후 </p> </th> 
   <th colname="col3" class="entry"> <p>2016년 4월 21과 5월 19 사이 </p> <p>(Data Warehouse에 적용할 수 없음) </p> </th> 
   <th colname="col4" class="entry"> <p>2016년 4월 21일 전 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>고객이 아님 </p> </td> 
   <td colname="col2"> <p>전혀 구입하지 않은 방문자 </p> </td> 
   <td colname="col3"> <p>방문 종료 시까지 아무것도 구입하지 않은 방문자입니다. </p> </td> 
   <td colname="col4"> <p>사용할 수 없음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>새 고객 </p> </td> 
   <td colname="col2"> <p>한 번 구입한 방문자 </p> </td> 
   <td colname="col3"> <p>방문 종료 시까지 한 번 구입하지 않은 방문자입니다. </p> <p>(구입이 발생하면 고객 상태가 해당 구입 이후 다음 방문 시 업데이트되었습니다.) </p> </td> 
   <td colname="col4"> <p>해당 방문 종료 시까지 아무것도 구입하지 않은 방문자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>재방문 고객 </p> </td> 
   <td colname="col2"> <p>두 번 구입한 방문자 </p> </td> 
   <td colname="col3"> <p>두 번째 구입한 방문을 종료할 때까지 두 번 구입한 방문자입니다. </p> <p>(구입이 발생하면 고객 상태가 해당 구입 이후 다음 방문 시 업데이트되었습니다.) </p> </td> 
   <td colname="col4"> <p>구입한 방문을 종료할 때까지 한 번 구입한 방문자입니다. </p> <p>(구입이 발생하면 고객 상태가 해당 구입 이후 다음 방문 시 업데이트되었습니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>단골 고객 </p> </td> 
   <td colname="col2"> <p>세 번 이상 구입한 방문자 </p> </td> 
   <td colname="col3"> <p>가장 최근에 구입한 방문을 종료할 때까지 세 번 이상 구입한 방문자입니다. </p> <p>(구입이 발생하면 고객 상태가 해당 구입 이후 다음 방문 시 업데이트되었습니다.) </p> </td> 
   <td colname="col4"> <p>가장 최근에 구입한 방문을 종료할 때까지 세 번 이상 구입한 방문자입니다. </p> <p>(구입이 발생하면 고객 상태가 해당 구입 이후 다음 방문 시 업데이트되었습니다.) </p> </td> 
  </tr> 
 </tbody> 
</table>

| 버전 14 고객 충성도(현재) |
|---|
| 새 고객 | 1회 방문 및 1회 구입 |
| 재방문 고객 | 2회 이상 방문 및 2회 구입 |
| 단골 고객 | 2회 이상 방문 및 3회 이상 구입 |

충성도 상태는 동일한 방문 내에서 구매 이벤트가 일어나는 즉시 변경됩니다. 예를 들어 새 고객(1회 구입)이 구매한 다음 동일한 방문 내에서 해당 구매 후 뉴스레터에 등록합니다. 구매가 발생한 직후 방문자의 고객 충성도 상태가 변경되므로 뉴스레터 등록 이벤트는 재방문 고객의 상호 작용으로 간주됩니다.
