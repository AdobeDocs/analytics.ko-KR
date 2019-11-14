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


# pageType

 변수는 404 [페이지가 없습니다] 오류 페이지를 지정하는 데만 사용됩니다.

<!-- 

pageType.xml

 -->

<table id="table_0492B136E9D14070A6CA49ED534BCA4C"> 
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
   <td> 20바이트 </td> 
   <td> pageType </td> 
   <td> 경로 &gt; 페이지 &gt; 페이지 <p>발견되지 않음 </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

The *`pageType`* variable captures the errant URL when a 404 Error page is displayed, which allows you to quickly find broken links and paths that are no longer valid on the custom site. 아래와 같이 오류 페이지에서 *`pageType`* 변수를 설정합니다.

404 오류 페이지에 페이지 이름 변수를 사용하지 마십시오. 404 오류 페이지에는 *`pageType`* 변수만 사용됩니다.

대부분의 경우 404 오류 페이지는 하드 코딩된 정적 페이지입니다. 이러한 경우 .JS 파일 참조를 적절한 글로벌 또는 상대적 경로/디렉토리로 설정하는 것이 중요합니다.

**구문 및 가능한 값** {#section_C1C59968226446559B05F6EE7374D525}

허용되는 *`pageType`* 값은 아래 표시된 대로 "errorPage" 뿐입니다.

```js
s.pageType="errorPage"
```

**예** {#section_6CE22FCB835B4A19B633B7F67E73A115}

```js
s.pageType="errorPage"
```

**구성 설정** {#section_3B304A6D3A6C48F2BE90B4DA92A39DDB}

없음

**함정, 질문 및 팁** {#section_943681AB01FE47BEAC72E93CB60C53C8}

다른 서버측 오류(예: 500 오류)를 캡처하려면 prop을 사용하여 오류 메시지를 캡처하고 `<URL>`이 요청한 URL인 "`500 Error: <URL>`"를 *`pageName`* 변수에 지정합니다. 이 방법을 따르면 [!UICONTROL 경로 지정] 보고서를 사용하여 사용자가 500 오류를 생성하는 경로를 알 수 있습니다. prop는 서버에 의해 지정되는 오류 메시지에 대해 설명합니다.

