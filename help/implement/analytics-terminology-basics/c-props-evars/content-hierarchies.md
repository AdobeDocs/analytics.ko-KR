---
description: 컨텐츠 계층의 일반적인 용도는 방문자가 특정 페이지, 수준 등에서 택한 다양한 경로를 보여주는 것입니다.
keywords: Analytics 구현; 컨텐트 계층 구조; hier
seo-description: 컨텐츠 계층의 일반적인 용도는 방문자가 특정 페이지, 수준 등에서 택한 다양한 경로를 보여주는 것입니다.
seo-title: 컨텐츠 계층 계산
solution: Analytics
title: 컨텐츠 계층 계산
topic: 개발자 및 구현
uuid: d 41 df 92 d -65 fb -44 de-bf 46-8 fac 24303 dad
translation-type: tm+mt
source-git-commit: 1bc1c7a1e00d7b59cd39f368ac9afb745bea9e47

---


# 컨텐츠 계층 계산

컨텐츠 계층의 일반적인 용도는 방문자가 특정 페이지, 수준 등에서 택한 다양한 경로를 보여주는 것입니다.

**내[!UICONTROL 컨텐츠 계층]은 어떻게 추적해야 합니까?** 

먼저 [!UICONTROL 컨텐츠 계층] 추적을 위한 보고 요구 사항을 이해해야 합니다. 계층 추적 요구 사항이 매우 자세한 경우 종종 계층( *`hier`*) 변수를 사용하는 것이 좋습니다. 일반적으로 계층은 동일한 하위 노드가 여러 상위 노드 아래에 거의 없는, 엄격하고 사전에 정의된 분류법을 필요로 합니다. 다음 예를 생각해 보십시오.

[!UICONTROL 글로벌 계층]

모든 사이트 &gt; 지역 &gt; 국가 &gt; 언어 &gt; 카테고리

이 예에서, 계층은 언어 수준에서 분류를 시작할 수 있습니다. 요구 사항이 전체 "영어" 트래픽에 대해 보고하는 것일 경우, 영어가 미국, 영국, 호주 등에 나타나는 문제가 발생할 수 있습니다. 계층을 사용하면 드릴다운만 할 수 있습니다. 여러 계층에 걸쳐 수평적으로 자세히 분할하는 좋은 방법은 [!UICONTROL 사용자 지정 트래픽 변수](prop)를 사용하는 것입니다.

사용자가 사이트를 통해 드릴다운(사용자가 사이트를 탐색하는 방법과 유사)하고 각 계층 수준에서 [!UICONTROL 고유 방문자]에 대해 보고할 수 있도록 하려면, 계층 변수를 사용하는 것이 좋습니다.

props와 *`hier`* 변수를 모두 사용하는 경우도 있습니다. 다음은 각 변수 유형에 대해 지원되는 prop입니다.

<table id="table_E960D100DA0F433A94A4B246D6EF0D0A"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> Prop </th> 
   <th class="entry"> 계층 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 상관 관계 </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_2832E346D220429DA643B908EC10260D" /> </p> </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_2A70A61A78024204B6CEE4FFF9A0851E" /> </p> </td> 
  </tr> 
  <tr> 
   <td> 경로 지정 </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_EE5ED36AC75F4D648F54858D796F82BD" /> </p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 페이지 보기 </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_5BB82776D41642E78C2ECFD71DD33164" /> </p> </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_18F34EE8957946AF9D6C2C9B492CEDB7" /> </p> </td> 
  </tr> 
  <tr> 
   <td> 고유 방문자 수 </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_A475267547B94DB4A1EEFD903B2CA1EB" /> </p> </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_1E9E302D999146128CDBCE13E52BC38C" /> </p> </td> 
  </tr> 
  <tr> 
   <td> 분류 </td> 
   <td> <p><img  src="assets/check-mark.png" id="image_FC5FEFE7BA8C4475BA4F31D57302BE6B" /> </p> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

