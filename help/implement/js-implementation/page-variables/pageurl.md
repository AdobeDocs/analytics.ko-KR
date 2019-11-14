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


# pageUrl

 변수는 페이지의 실제 URL을 무시합니다.

<!-- 

pageURL.xml

 -->

페이지의 URL이 Analytics에 보고할 URL과 다른 경우가 드물게 나타납니다.

<table id="table_D4DC6B476FFD4BEEB36A5C6B2D026255"> 
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
   <td> 제한 없음* </td> 
   <td> <p>G </p> </td> 
   <td> 트래픽 &gt; 세그먼테이션 &gt; 가장 방문 빈도가 높은 페이지 경로 </td> 
   <td> 페이지 URL </td> 
  </tr> 
 </tbody> 
</table>

> [!NOTE]*`pageURL`* 값을 최대 64k까지 허용함에도 불구하고, 일부 브라우저에서는 이미지 요청의 URL에 대한 크기 제한을 시행하고 있습니다. 다른 데이터가 잘리지 않도록 하기 위해 255바이트보다 긴 페이지 URL은 분할되어 처음 255바이트는 `g=` 매개 변수에 나타나고 나머지 바이트는 `-g=` 쿼리 매개 변수의 쿼리 문자열 뒤쪽에 나타납니다.

**구문 및 가능한 값** {#section_22AF3BF7C2F743549967B0C760A095C0}

*`pageURL`* 변수는 유효한 프로토콜이 있는 유효한 URL이어야 합니다. 도메인을 보고서에 채우려면 먼저 강제로 소문자로 표시해야 하며 Analytics 설정에 따라 쿼리 문자열이 제거될 수 있습니다.

```js
s.pageURL="proto://domain/path?query_string"
```

페이지 URL에는 URL 호환 문자만 허용됩니다.

> [!NOTE]*`pageURL`* 변수를 사용자 지정 용도로 사용하기 전에 Adobe 컨설턴트나 고객 지원에 문의하는 것이 좋습니다.

**예** {#section_45158FDA3F8F4574BDEB5CBC9F7E6C97}

```js
s.pageURL="https://mysite.com/home.jsp?id=1224" 
```

```js
s.pageURL="https://www.mysite.com/"
```

**구성 설정** {#section_A8F77DAD88164528ACC5C16C066B47DF}

없음

