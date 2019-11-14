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



# browserWidth

 변수는 브라우저 창의 너비를 표시합니다.

<!-- 

browserwidth.xml

 -->

이 변수는 페이지 코드의 뒤에, *`doPlugins`*&#x200B;가 실행되기 전에 채워집니다.

> [!NOTE] 이 변수는 읽기 전용이어야 하며 설정할 수 없습니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

**매개 변수**

<table id="table_B70F279A8CD240328520E5BD889806BD"> 
 <tbody> 
  <tr> 
   <td> <p> <b>쿼리 매개 변수</b> </p> </td> 
   <td> <p> <b>값</b> </p> </td> 
   <td> <p> <b>예</b> </p> </td> 
   <td> <p> <b>영향을 받은 보고서</b> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>bw </p> </td> 
   <td> <p>양의 정수 </p> </td> 
   <td> <p>1179 </p> </td> 
   <td> <p>트래픽 &gt; 기술 &gt; 브라우저 너비 </p> </td> 
  </tr> 
 </tbody> 
</table>
