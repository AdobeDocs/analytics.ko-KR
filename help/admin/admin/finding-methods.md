---
description: '[검색 방법] 페이지에서는 다양한 검색 방법 보고서가 사용자 사이트에서의 전환 성공 이벤트에 대한 크레딧을 받는 방법을 식별합니다. 예를 들어 검색 엔진이 구매하는 방문자를 해당 사이트로 안내하는 경우, 검색 방법은 검색 엔진이 참조에 대한 크레딧을 받는 방법을 지정합니다.'
seo-description: '[검색 방법] 페이지에서는 다양한 검색 방법 보고서가 사용자 사이트에서의 전환 성공 이벤트에 대한 크레딧을 받는 방법을 식별합니다. 예를 들어 검색 엔진이 구매하는 방문자를 해당 사이트로 안내하는 경우, 검색 방법은 검색 엔진이 참조에 대한 크레딧을 받는 방법을 지정합니다.'
seo-title: 검색 방법
solution: Analytics
title: 검색 방법
topic: 관리 도구
uuid: 1053993 e -7 fc 4-4874-84 fa -367 ecdcd 7 b 45
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 검색 방법

[검색 방법] 페이지에서는 다양한 검색 방법 보고서가 사용자 사이트에서의 전환 성공 이벤트에 대한 크레딧을 받는 방법을 식별합니다. 예를 들어 검색 엔진이 구매하는 방문자를 해당 사이트로 안내하는 경우, 검색 방법은 검색 엔진이 참조에 대한 크레딧을 받는 방법을 지정합니다.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리]** &gt; **[!UICONTROL 보고서 세트]** &gt; **[!UICONTROL 설정]** 편집 &gt; **[!UICONTROL 전환]** &gt; **[!UICONTROL 검색 방법]**.

## 검색 방법 설명 {#section_8B6278DB75224EAB9F49D89A86274E8A}

<table id="table_8ABC1C9BD63F419082E4C4C69E401526"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 수정할 검색 방법 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 할당 </td> 
   <td colname="col2"> 참조에 대한 크레딧을 적용하는 방법을 지정합니다. 지원되는 할당 옵션에는 다음이 포함됩니다. <p> <span class="uicontrol"> 가장 최근 (마지막):</span> 모든 크레딧을 마지막 레퍼러에게 줍니다(기본값). </p> <p> <span class="uicontrol"> 원래 값:</span> 첫 참조에 모든 크레딧을 부여합니다. </p> <p> <span class="uicontrol"> 선형:</span> 모든 참조에 균등하게 크레딧을 배분합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다음 동작이 끝나면 만료 </td> 
   <td colname="col2"> 
    <ul id="ul_95EB224CAD164E9997B148E08AFA5F9B"> 
     <li id="li_C240460C21E14AA498D2EA62B9354710"> <span class="uicontrol">방문:</span> 지정된 활동 중지 시간(일반적으로 약 30분) 이후 </li> 
     <li id="li_A3AE5438919E44B68DF99BEEA60C44EE"> <span class="uicontrol">페이지 보기:</span> 사이트의 페이지가 열리면 즉시 </li> 
     <li id="li_D5E20FEF313E4C5B99E7097CA175761A"> <span class="uicontrol">분:</span> 활동 중지 1분 </li> 
     <li id="li_7315AA3EDDBB47A2BEA3C173881378A1"> <span class="uicontrol">구매:</span> 구매 시점 </li> 
     <li id="li_C0CF07581654472C9C9EC944E6F18164"> <span class="uicontrol">제품 보기:</span> 방문자가 제품 웹 페이지를 볼 때 </li> 
     <li id="li_A1B04065150B407491D2EC78EC0DBDF5"> <span class="uicontrol">장바구니 열기:</span> 방문자가 새로운 온라인 장바구니를 열 때 </li> 
     <li id="li_2AA50C6B9CB14500B67909CDF2AA700C"> <span class="uicontrol">장바구니 체크아웃:</span> 방문자가 온라인 장바구니 사용을 체크아웃할 때 </li> 
     <li id="li_F58CE6FB8DCE4BE4927FFCB35A6D8E31"> <span class="uicontrol">장바구니 추가:</span> 방문자가 온라인 장바구니에 제품을 추가할 때 </li> 
     <li id="li_AD7C846F46604FC48E0919ACB7515E14"> <span class="uicontrol">장바구니 제거:</span> 방문자가 온라인 장바구니에서 제품을 제거할 때 </li> 
     <li id="li_EB66E0563F564C9F985BE922DABD0A56"> <span class="uicontrol">장바구니 열기:</span> 방문자가 온라인 장바구니의 컨텐츠를 볼 때 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>모든 검색 방법은 방문이 종료될 때 만료됩니다. 다른 이벤트(예: 장바구니 체크아웃) 이후에 만료되도록 선택하면 방문 중에 장바구니 체크아웃이 발생할 때 검색 방법이 만료됩니다. 방문 중에 장바구니 체크아웃이 발생하지 않으면 방문이 종료될 때 검색 방법이 만료됩니다.

