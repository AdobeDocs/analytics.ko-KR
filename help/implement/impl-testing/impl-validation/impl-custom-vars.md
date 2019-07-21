---
description: Analytics에서 사용된 사용자 지정 변수 목록
keywords: Analytics 구현
seo-description: Analytics에서 사용된 사용자 지정 변수 목록
seo-title: '사용자 지정 변수 입니다. '
solution: Analytics
title: '사용자 지정 변수 입니다. '
topic: 개발자 및 구현
uuid: 54 ADF 622-7 F 05-49 C 0-B 7 E 6-702 BB 2 F 17 B 1 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 사용자 지정 변수 입니다. 

Analytics에서 사용된 사용자 지정 변수 목록

<table id="table_E8C7871F63F648A59644638FB56BD0E1"> 
 <thead> 
  <tr> 
   <th class="entry"> 변수 </th> 
   <th class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 트래픽 변수 </td> 
   <td> prop1 - 75의 값을 확인합니다. 다음은 수행할 확인 목록입니다. 
    <ul id="ul_0EE2D50BA90F4F21BD63268A5082F980"> 
     <li id="li_A6E4D66E8A03400491A26A08E4945908">대/소문자를 올바로 사용하는가? "ValueA"는 "valueA"와 다른 레코드입니다. 적은 수의 브라우저 하위 세트가 모든 변수를 소문자로 전환하므로 모든 소문자를 사용할 수 있습니다. </li> 
     <li id="li_65CBFB908E7B4ED5AF9518FE5B58D4E2">값의 길이가 100자 미만인가? 아닐 경우, 값의 일부가 잘릴 수 있습니다. </li> 
     <li id="li_CC506D114AFE44699D89AB84BBCCEBFC"> 하나의 속성 변수에 있는 모든 값이 관련되어 있는가, 아니면 일부 값이 적절하지 않아 보이는가? </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> 전환 변수 </td> 
   <td> <span class="wintitle">Econversion</span> 변수에는 eVar 1 - 75가 포함됩니다. 다음은 확인할 문제 목록입니다. 
    <ul id="ul_CA10C5B9F24B4C49A64CA84A9DCE8E63"> 
     <li id="li_8CCD92F3AD5E49EBA91C9B008DA47016">대/소문자를 올바로 사용하는가? "ValueA"는 "valueA"와 다른 레코드입니다. 적은 수의 브라우저 하위 세트가 모든 변수를 소문자로 전환하므로 모든 소문자를 사용할 수 있습니다. </li> 
     <li id="li_5B6FDEDB2C32409AA59D6BB0DF2346CB">값의 길이가 255자 미만인가? 아닐 경우, 값의 일부가 잘릴 수 있습니다. </li> 
     <li id="li_C31AFBAC99D84E96A1244E795CE7765D">하나의 eVar에 있는 모든 값이 관련되어 있는가, 아니면 일부 값이 적절하지 않아 보이는가? </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> 사용자 지정 이벤트 </td> 
   <td> 이벤트에는 event1부터 event100에 이르는 사용자 지정 이벤트는 물론, 표준 값(<span class="wintitle">prodView</span>, <span class="wintitle">scOpen</span>, <span class="wintitle">scAdd</span>, <span class="wintitle">scCheckout</span>, <span class="wintitle">purchase</span>)도 모두 포함되어 있습니다. 모든 이벤트는 이벤트 변수에서 전송됩니다. 같은 페이지에 여러 이벤트가 있으면 쉼표로 구분해야 합니다(공백 없이). 
    <ul id="ul_2213CC9DE892433FAF6FC1F5A2B841B4"> 
     <li id="li_15E31A9FF1654DFA93C158F422B9EAE3">모든 표준 전환 이벤트의 경우 제품은 적용 가능한 제품으로 채워져야 합니다. 구매를 제외한 모든 이벤트의 경우, 수량 및 가격 요소는 선택 사항입니다. </li> 
     <li id="li_03ED9AAC45DA47A58AB482E2CEBF5108"><span class="wintitle">구매</span> 이벤트는 구매를 완료하고 확인한 후, 세션에서 한 번만 설정해야 합니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

