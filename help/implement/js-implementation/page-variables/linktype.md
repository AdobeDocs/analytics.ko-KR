---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---



# linkType

 변수는 링크 이름 또는 URL이 표시되는 보고서(사용자 지정, 다운로드 또는 종료 링크)를 결정하는 링크 추적에 사용되는 선택 변수입니다.

<!-- 

linkType.xml

 -->

*`linkType`* 변수는 *`tl()`* 함수에서 두 번째 매개 변수가 대체하므로 보통은 필요가 없습니다.

<table id="table_3D1A2FC1CECD4709BE2F9E32AC2DC730"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 1자 </td> 
   <td> pe=[lnk_o|lnk_d|lnk_e] </td> 
   <td> <p>파일 다운로드 </p> <p>사용자 지정 링크 </p> <p>종료 링크  </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

사용자 지정 링크는 데이터를 Analytics로 보냅니다. *`linkType`* 변수(또는 *`tl()`* 함수의 두 번째 매개 변수)는 링크 이름 또는 URL이 나타나는 보고서를 식별하는 데 사용됩니다([!UICONTROL 사용자 지정], [!UICONTROL 다운로드] 또는 [!UICONTROL 종료 링크] 보고서).

종료 및 다운로드 링크의 경우 클릭한 링크가 종료 링크인지 아니면 다운로드 링크인지에 따라 *`linkType`* 변수가 자동으로 채워집니다. 사용자 지정 링크는 이 변수나 *`tl()`* 함수의 두 번째 매개 변수가 있는 세 개의 보고서 중 하나에 데이터를 보내도록 구성할 수 있습니다. *`linkType`*&#x200B;을 'o', 'e' 또는 'd'로 설정하거나 *`linkName`* 또는 링크 URL이 각각 [!UICONTROL 사용자 지정 링크], [!UICONTROL 종료 링크] 또는 [!UICONTROL 파일 다운로드] 보고서에 각각 전송됩니다.

**구문 및 가능한 값** {#section_18DB3A8083FB4F75B970055ED336DA4E}

*`linkType`* 변수 구문은 XML 또는 쿼리 문자열 사용 여부에 따라 다릅니다.

XML을 사용하는 경우 변수에는 단일 문자, 즉, 'o,' 'e' 또는 'd'만 포함될 수 있습니다.

```js
s.tl(this,'o','Link Name');
```

쿼리 문자열 `pe`를 사용하는 경우 `lnk_d`, `lnk_e` 또는 `lnk_o`를 사용해야 합니다.

**예** {#section_242B5DFFD1C9462A9A8EB1556B2E3160}

```js
<a href="index.html" onClick=" 
 var s=s_gi('rsid'); **see note below on the rsid** 
 s.tl(this,'o','Link Name'); 
 ">My Page</a> 
```

**구성 설정** {#section_59738AD1B5E94294B8D36F4E772DEDB3}

없음

**함정, 질문 및 팁** {#section_F0D01DDE3FDA486C987162DA50A79C45}

* *`linkType`*&#x200B;을 지정하지 않으면 사용자 지정 링크('o')로 간주됩니다.
