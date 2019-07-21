---
description: 행 레이블 그리드에 추가할 차원을 필터링할 수 있습니다. 필터는 요청으로 반환된 데이터의 범위를 좁히며, 피벗 또는 사용자 지정 레이아웃에서 적용할 수 있습니다. 피벗 레이아웃에서 차원 필터링을 구성할 때 셀의 항목 수를 추가로 지정할 수 있습니다.
seo-description: 행 레이블 그리드에 추가할 차원을 필터링할 수 있습니다. 필터는 요청으로 반환된 데이터의 범위를 좁히며, 피벗 또는 사용자 지정 레이아웃에서 적용할 수 있습니다. 피벗 레이아웃에서 차원 필터링을 구성할 때 셀의 항목 수를 추가로 지정할 수 있습니다.
seo-title: 차원 필터링 개요
solution: Analytics
title: 차원 필터링 개요
topic: Report Builder
uuid: c 54 d 5 add-f 278-476 d -8 f 14-73 f 1 c 2 e 37671
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 차원 필터링 개요

행 레이블 그리드에 추가할 차원을 필터링할 수 있습니다. 필터는 요청으로 반환된 데이터의 범위를 좁히며, 피벗 또는 사용자 지정 레이아웃에서 적용할 수 있습니다. 피벗 레이아웃에서 차원 필터링을 구성할 때 셀의 항목 수를 추가로 지정할 수 있습니다.

선택한 필터 양식이 Report Builder 요청에서 선택한 요소 및 지표를 기반으로 채워집니다.

## Define filter - values and special characters {#section_15840216A4044C40974945FAA435AD93}

Information about filters in the **[!UICONTROL Most Popular Filter]** &gt; **[!UICONTROL Define Filter]** panel.

![](assets/define_filter.png)

다음 표에는 필터에 대한 예제와 정보가 나와 있습니다.

<table id="table_8AC3A26FF02143DBA949B30F2A46CF11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필터 </th> 
   <th colname="col02" class="entry"> 설명 </th> 
   <th colname="col2" class="entry"> 필터 예 </th> 
   <th colname="col3" class="entry"> 일치 결과 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>다음 검색어 포함 </p> </td> 
   <td colname="col02"> <p>모든 순서의 공백으로 구분된 모든 값을 포함합니다. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p>matches <span class="term"> A B CAND</span><span class="term"> B A C</span>등. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색어를 하나라도 포함 </p> </td> 
   <td colname="col02"> <p>필터 중 하나 이상(공백으로 구분)을 포함합니다. </p> </td> 
   <td colname="col2"> <p>A B C </p> </td> 
   <td colname="col3"> <p>matches <span class="term"> a 1</span>, <span class="term"> b 2</span>, <span class="term"> c 3</span>이지만 <span class="term"> d 4</span>는 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구문 포함 </p> </td> 
   <td colname="col02"> <p>검색 필터를 포함하며 다른 검색어도 포함할 수 있습니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>matches <span class="term"> ABC</span> 및 <span class="term"> ABC def</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색어 포함 안 함 </p> </td> 
   <td colname="col02"> <p>입력하는 값이 포함되지 않은 경우 모든 검색을 반환합니다. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p>matches <span class="term"> D E F</span> 이지만 <span class="term"> C D E F</span>는 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음 구문 포함 안 함 </p> </td> 
   <td colname="col02"> <p>해당 구문을 포함하지 않는 모든 검색을 반환합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>excludes <span class="term"> ABC</span>, <span class="term"> ABC DEF</span> 및 일치 <span class="term"> DEF</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>같음 </p> </td> 
   <td colname="col02"> <p>완전 일치 검색을 반환합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p> <span class="term"> abc</span> 가 반환되고 다른 항목이 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>같지 않음 </p> </td> 
   <td colname="col02"> <p>해당 항목과 정확히 일치하지 않는 모든 검색을 반환합니다. </p> </td> 
   <td colname="col2"> <p>a </p> </td> 
   <td colname="col3"> <p>일치하지 않음 <span class="term"> a</span>. </p> <p>Matches <span class="term"> a b c</span>. </p> <p>Matches <span class="term"> abc</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음으로 시작 </p> </td> 
   <td colname="col02"> <p>특정 값으로 시작하는 결과를 반환합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>matches <span class="term"> abcd</span> but not <span class="term"> 1 abc</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음으로 끝남  </p> </td> 
   <td colname="col02"> <p>특정 값으로 끝나는 결과를 반환합니다. </p> </td> 
   <td colname="col2"> <p>xyz </p> </td> 
   <td colname="col3"> <p>matches <span class="term"> wxyz</span> 하지만 <span class="term"> wxyz 0는 아님</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>고급(특수 문자)  </p> </td> 
   <td colname="col02"> <p>정규 표현식 문자를 사용할 수 있습니다. </p> <p> <code> "", ^, -, *, $, | </code> </p> </td> 
   <td colname="col2"> <p>"^Home*Page$" | sports </p> </td> 
   <td colname="col3"> <p> 여기서는 <span class="term"> Home</span>, 그런 다음 0 개 이상의 문자를 찾은 다음 <span class="term"> 페이지로 끝납니다</span>. </p> <p><span class="term"> 또한 스포츠가 포함된</span> 모든 페이지 </p> <p>몇 가지 일치하는 예는 다음과 같습니다. </p> 
    <ul id="ul_72D76C5AFEAF405E8A0E4E3C604D10AE"> 
     <li id="li_4D490059B667450DA8A0103167C7B391">HomePage </li> 
     <li id="li_1351619156274092AEB2771D882AD357">Home 및 (다른 문자) Page </li> 
     <li id="li_940EAA99A8CF49308E8471065EB317B1">Home sports </li> 
     <li id="li_50A895F14A454BE9BF06EE0F07F99B3B">sports Page </li> 
     <li id="li_F3CE0D07941D4C2485D2DE0B73E00677">sports </li> 
     <li id="li_E84C15C061824A5D922D9900392F2996">xyz sports abc </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_8BBB06C8860745DEA41B39673699DC0F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 특수 문자 </th> 
   <th colname="col2" class="entry"> 용도 </th> 
   <th colname="col3" class="entry"> 내용 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> " " </td> 
   <td colname="col2"> 같음 </td> 
   <td colname="col3"> <p>다른 따옴표와 짝이 맞지 않는 한 이스케이프되지 않습니다. 예를 들어 <span class="term"> 17 "표시는</span> 구문이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> * </td> 
   <td colname="col2"> 와일드카드 </td> 
   <td colname="col3"> <p>정규 표현식에서 사용되는 별표와 동일합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ^ </td> 
   <td colname="col2"> 다음으로 시작 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> $ </td> 
   <td colname="col2"> 다음으로 끝남 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> - </td> 
   <td colname="col2"> 아님 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> | </td> 
   <td colname="col2"> 또는 </td> 
   <td colname="col3"> <p>지원되는 경우에만 <span class="term"> 고급 (특수 문자)</span> 필터를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>