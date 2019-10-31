---
description: Adobe Analytics에서 Dynamic Tag Management를 배포할 때 레퍼러 및 캠페인 옵션에 대한 Dynamic Tag Management의 필드 설명입니다.
keywords: Dynamic Tag Management;레퍼러;캠페인;레퍼러 재정의;캠페인 변수;쿼리 매개 변수
seo-description: Adobe Analytics에서 Dynamic Tag Management를 배포할 때 레퍼러 및 캠페인 옵션에 대한 Dynamic Tag Management의 필드 설명입니다.
seo-title: 레퍼러 및 캠페인
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: 레퍼러 및 캠페인
uuid: 56580206-a382-4993-9bba-a488da65cf89
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 레퍼러 및 캠페인

Adobe [!DNL Analytics]에서 [!UICONTROL Dynamic Tag Management]를 배포할 때 레퍼러 및 캠페인 옵션에 대한 [!UICONTROL Dynamic Tag Management]의 필드 설명입니다.

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png) **[!UICONTROL 편집 도구]** &gt; **[!UICONTROL 레퍼러 및 캠페인]**

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
   <td colname="col2"> <p>Overrides the value set in the <span class="varname"> s.referrer</span> 변수에 설정된 값을 무시합니다. 이 값은 일반적으로 브라우저에서 설정된 레퍼러로 채워집니다. </p> <p>See <a href="/help/implement/js-implementation/c-variables/page-variables.md">Page Variables</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 캠페인 </td> 
   <td colname="col2"> <p>사이트로 방문자를 유도하는 데 사용된 마케팅 캠페인을 식별하는 변수입니다. campaign의 값은 대개 쿼리 문자열 매개 변수에서 가져옵니다. </p> <p>See [<a href="/help/implement/js-implementation/c-variables/page-variables.md">Page Variables</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

DTM 인터페이스에서 쿼리 문자열을 사용할지 아니면 값(데이터 요소에서 끌어올 수 있음)을 사용할지 선택합니다.

![](assets/dtm-queryparam.png)

인터페이스에서 직접 쿼리 문자열을 입력하거나 캠페인을 추적할 다른 방법이 있는 경우 별도의 데이터 요소를 참조할 수 있습니다.
