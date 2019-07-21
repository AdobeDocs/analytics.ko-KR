---
description: 지표는 표준, 기여도, 최근, 선형 할당 방법 등을 사용하여 계산됩니다. 각 방법은 수식에 기반하여 다르게 값을 계산합니다.
seo-description: 지표는 표준, 기여도, 최근, 선형 할당 방법 등을 사용하여 계산됩니다. 각 방법은 수식에 기반하여 다르게 값을 계산합니다.
seo-title: 지표 계산
solution: Analytics
title: 지표 계산
topic: 지표
uuid: 2 AF 58 F 1 E -12 c 5-4828-AE 39-C 9 AEAEF 6 B 705
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 지표 계산

지표는 표준, 기여도, 최근, 선형 할당 방법 등을 사용하여 계산됩니다. 각 방법은 수식에 기반하여 다르게 값을 계산합니다.

<table id="table_6F81A12174D84124B7FD81FBBEDF18A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 지표 계산 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 최초 </td> 
   <td colname="col2"> <p>전체 크레딧은 성공 이벤트와 관련된 첫 번째 변수 값에 주어집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최근 </td> 
   <td colname="col2"> <p>전체 크레딧은 성공 이벤트와 관련된 마지막 변수 값에 주어집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 선형 </td> 
   <td colname="col2"> <p>선형 할당을 선택하면, 성공 이벤트는 방문에서 보이는 모든 변수에 균등하게 나눠집니다. 숫자 및 통화 이벤트에 <span class="term"> 매출</span>, 금액은 분할됩니다. <span class="term"> 주문과</span>같은 카운터 이벤트의 경우, 이벤트의 일부가 방문의 각 변수 값에 부여됩니다. 보고에 있는 이 부분들은 합해진 후, 보고에서 가장 근사치의 정수로 반올림됩니다. </p> <p>예를 들어 성공 이벤트에 앞서 4개의 페이지를 방문하는 경우 각 페이지가 이벤트의 25%에 대한 크레딧을 받습니다. 동일한 방문에서 <span class="varname"> 캠페인에는</span> 두 개의 값이 있었지만 각 캠페인 값은 이벤트에 대한 크레딧의 50%를 받습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기여도 </td> 
   <td colname="col2"> <p>전체 크레딧을, 방문 내의 성공 이벤트에 기여한 각 변수 값에 지정합니다. 교차 방문 기여도 지표를 사용할 경우 교차 방문자 세션에도 이 계산을 적용할 수 있습니다.  </p> <p>자세한 내용은 <a href="../../../components/c-variables/c-metrics/metrics-participation.md#concept_8E6B39106A244CB49E055150B291B477" format="dita" scope="local"> 기여도</a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 - 지표 계산 {#section_4CE01DA35108418D9909823A7ECC4B45}

사이트에 전환 변수(eVar)를 사용하여 추적되는 내부 검색이 있다고 가정해 보십시오. 방문자는 $100 구매를 하기 전에 몇 가지 내부 검색을 수행합니다.

*`Pet`* &gt; *`Feline`* &gt; *`Cat`* &gt; *`Kitten`* &gt; $ 100 Purchase

보고에서 크레딧 할당은 다음과 같습니다.

<table id="table_91A7244E77854838A8392B49366FB445"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar 변수 </th> 
   <th colname="col2" class="entry"> 첫 번째 날 </th> 
   <th colname="col3" class="entry"> 마지막 날 </th> 
   <th colname="col4" class="entry"> 선형 </th> 
   <th colname="col5" class="entry"> 기여도 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>애완 동물 </p> </td> 
   <td colname="col2"> <p>$100 </p> </td> 
   <td colname="col3"> <p>$0 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>고양이과 </p> </td> 
   <td colname="col2"> <p>$0 </p> </td> 
   <td colname="col3"> <p>$0 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>고양이 </p> </td> 
   <td colname="col2"> <p>$0 </p> </td> 
   <td colname="col3"> <p>$0 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>새끼 고양이 </p> </td> 
   <td colname="col2"> <p>$0 </p> </td> 
   <td colname="col3"> <p>$100 </p> </td> 
   <td colname="col4"> <p>$25 </p> </td> 
   <td colname="col5"> <p>$100 </p> </td> 
  </tr> 
 </tbody> 
</table>

