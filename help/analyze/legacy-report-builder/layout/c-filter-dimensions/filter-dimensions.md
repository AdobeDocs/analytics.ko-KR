---
description: 행 레이블 그리드에 추가하는 차원을 필터링할 수 있습니다. 필터는 요청으로 반환된 데이터의 범위를 좁히며, 피벗 또는 사용자 정의 레이아웃에서 적용할 수 있습니다. 피벗 레이아웃에서 차원 필터링을 구성할 때 셀의 항목 수를 추가로 지정할 수 있습니다.
title: 차원 필터링 개요
uuid: c54d5add-f278-476d-8f14-73f1c2e37671
feature: Report Builder
role: User, Admin
exl-id: eded07d5-3c06-419b-92fd-1a48856ac293
TQID: https://experienceleague.adobe.com/yY1Sl6vEWRb-62SzM5e5qxt5lZPHeg-LU5ZiUNb5z8Q
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 28%

---

# 차원 필터링 개요

{{legacy-arb}}

행 레이블 그리드에 추가하는 차원을 필터링할 수 있습니다. 필터는 요청으로 반환된 데이터의 범위를 좁히며, 피벗 또는 사용자 정의 레이아웃에서 적용할 수 있습니다. 피벗 레이아웃에서 차원 필터링을 구성할 때 셀의 항목 수를 추가로 지정할 수 있습니다.

선택한 필터 양식은 Report Builder 요청에서 선택한 요소 및 지표를 기반으로 채워집니다.

## 필터 정의 - 값 및 특수 문자 {#section_15840216A4044C40974945FAA435AD93}

**[!UICONTROL 가장 자주 사용하는 필터]** > **[!UICONTROL 필터 정의]** 패널의 필터에 대한 정보입니다.

![응용 프로그램, 사용자 및 프로젝트별로 필터링할 수 있는 옵션이 있는 필터 정의 대화 상자를 표시하는 스크린샷입니다.](/help/admin/tools/assets/filter.png)

다음 표는 필터에 대한 예제와 정보를 제공합니다.

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
   <td colname="col02"> <p>모든 공백 구분 값을 임의의 순서로 포함합니다. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p><span class="term"> a b c</span> 및 <span class="term"> b a c</span> 등과 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색어를 하나라도 포함 </p> </td> 
   <td colname="col02"> <p>하나 이상의 필터(공백으로 구분)를 포함합니다. </p> </td> 
   <td colname="col2"> <p>에이 비 씨 </p> </td> 
   <td colname="col3"> <p><span class="term"> A1</span>, <span class="term"> B2</span>, <span class="term"> C3</span>와 일치하지만 <span class="term"> D4</span>은(는) 일치하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구문 포함 </p> </td> 
   <td colname="col02"> <p>검색 필터 및 기타 용어를 포함합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p><span class="term"> abc</span> 및 <span class="term"> abc def</span>와(과) 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색어 포함 안 함 </p> </td> 
   <td colname="col02"> <p>입력한 값이 포함되지 않으면 모두 반환합니다. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p><span class="term"> d e f</span>와(과) 일치하지만 <span class="term"> c d e f</span>과는 일치하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음 구문 포함 안 함 </p> </td> 
   <td colname="col02"> <p>구문이 포함되지 않은 모든 항목을 반환합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p><span class="term"> abc</span>, <span class="term"> abc def</span>을(를) 제외하고 <span class="term"> def</span>과(와) 일치시킵니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>같음 </p> </td> 
   <td colname="col02"> <p>정확히 일치하는 항목을 반환합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p> <span class="term"> abc</span>가 반환되고 다른 항목은 반환되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>같지 않음 </p> </td> 
   <td colname="col02"> <p>항목과 정확히 일치하지 않는 모든 항목을 반환합니다. </p> </td> 
   <td colname="col2"> <p>a </p> </td> 
   <td colname="col3"> <p><span class="term"> a</span>와(과) 일치하지 않습니다. </p> <p><span class="term"> a b c</span>와 일치합니다. </p> <p><span class="term"> abc</span>와 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음으로 시작 </p> </td> 
   <td colname="col02"> <p>특정 값으로 시작하는 결과를 반환합니다. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p><span class="term"> abcd</span>과(와) 일치하지만 <span class="term"> 1abc</span>과는 일치하지 않음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음으로 끝남 </p> </td> 
   <td colname="col02"> <p>특정 값으로 끝나는 결과를 반환합니다. </p> </td> 
   <td colname="col2"> <p>xyz </p> </td> 
   <td colname="col3"> <p><span class="term"> wxyz</span> 일치(<span class="term"> wxyz0</span>은 아님) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>고급 (특수 문자) </p> </td> 
   <td colname="col02"> <p>문자를 재정의할 수 있습니다. </p> <p> <code> "", ^, -, *, $, | </code> </p> </td> 
   <td colname="col2"> <p>"^Home*Page$" | 스포츠 </p> </td> 
   <td colname="col3"> <p> <span class="term"> Home</span>(으)로 시작하여 0개 이상의 문자를 찾은 다음 <span class="term"> Page</span>(으)로 끝나는 필터를 정의합니다. </p> <p>또한 <span class="term"> sports</span>가 포함된 모든 페이지. </p> <p>몇 가지 예는 다음과 일치합니다. </p> 
    <ul id="ul_72D76C5AFEAF405E8A0E4E3C604D10AE"> 
     <li id="li_4D490059B667450DA8A0103167C7B391">홈 페이지 </li> 
     <li id="li_1351619156274092AEB2771D882AD357">홈 및 (기타 문자) 페이지 </li> 
     <li id="li_940EAA99A8CF49308E8471065EB317B1">홈 스포츠 </li> 
     <li id="li_50A895F14A454BE9BF06EE0F07F99B3B">스포츠 페이지 </li> 
     <li id="li_F3CE0D07941D4C2485D2DE0B73E00677">스포츠 </li> 
     <li id="li_E84C15C061824A5D922D9900392F2996">xyz 스포츠 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_8BBB06C8860745DEA41B39673699DC0F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 특수 문자 </th> 
   <th colname="col2" class="entry"> 용도 </th> 
   <th colname="col3" class="entry"> 참고 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> " " </td> 
   <td colname="col2"> 같음 </td> 
   <td colname="col3"> <p>다른 따옴표와 쌍을 이루지 않으면 이스케이프 처리되지 않습니다. 예를 들어 <span class="term"> 17" Display</span>은(는) 구문이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> * </td> 
   <td colname="col2"> 와일드카드 </td> 
   <td colname="col3"> <p>정규 표현식에 사용된 별표와 동일합니다. </p> </td> 
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
   <td colname="col3"> <p><span class="term"> 고급(특수 문자)</span> 필터에서만 지원됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
