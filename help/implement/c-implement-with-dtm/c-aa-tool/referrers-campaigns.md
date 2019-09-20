---
description: Adobe Analytics에서 다이내믹 태그 관리를 배포할 때 레퍼러 및 캠페인 옵션에 대한 다이내믹 태그 관리의 필드 설명입니다.
keywords: 다이내믹 태그 관리;레퍼러;캠페인;레퍼러 재정의;캠페인 변수;쿼리 매개 변수
seo-description: Adobe Analytics에서 다이내믹 태그 관리를 배포할 때 레퍼러 및 캠페인 옵션에 대한 다이내믹 태그 관리의 필드 설명입니다.
seo-title: 레퍼러 및 캠페인
solution: Experience Cloud,Analytics,다이내믹 태그 관리
title: 레퍼러 및 캠페인
uuid: 56580206-a382-4993-9bba-a488da65cf89
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# 레퍼러 및 캠페인

Field descriptions in [!UICONTROL Dynamic Tag Management] for referrers and campaign options when deploying [!UICONTROL Dynamic Tag Management] in Adobe [!DNL Analytics].

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png) 편집 **[!UICONTROL 도구]** &gt; **[!UICONTROL 레퍼러 및 캠페인]**

<table id="table_09AE3BFF0F12442F9C19CD96451F93E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 레퍼러 무시 </td> 
   <td colname="col2"> <p>Overrides the value set in the <span class="varname"> s.referrer</span> variable, which is typically populated by the referrer set in the browser. </p> <p>[페이지 변수](/help/implement/js-implementation/c-variables/page-variables.md)을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 캠페인 </td> 
   <td colname="col2"> <p>사이트로 방문자를 유도하는 데 사용된 마케팅 캠페인을 식별하는 변수입니다. campaign의 값은 대개 쿼리 문자열 매개 변수에서 가져옵니다. </p> <p>[페이지 변수](/help/implement/js-implementation/c-variables/page-variables.md)을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

DTM 인터페이스에서 쿼리 문자열을 사용할지 아니면 값(데이터 요소에서 끌어올 수 있음)을 사용할지 선택합니다.

![](assets/dtm-queryparam.png)

인터페이스에서 직접 쿼리 문자열을 입력하거나 캠페인을 추적할 다른 방법이 있는 경우 별도의 데이터 요소를 참조할 수 있습니다.
