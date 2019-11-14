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



# linkName

이 변수는 사용자 지정, 다운로드 또는 종료 링크의 이름을 결정하는 [!UICONTROL 링크 추적]에 사용되는 선택 변수입니다. 

<!-- 

linkName.xml

 -->

*`linkName`* 변수는 *`tl()`* 함수에서 세 번째 매개 변수가 대체하므로 보통은 필요가 없습니다.

<table id="table_4B0D1C9AADA542A59B626E077D5FC568"> 
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
   <td> 100바이트 </td> 
   <td> pev2 </td> 
   <td> <p>파일 다운로드 </p> <p>사용자 지정 링크 </p> <p>종료 링크  </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL 사용자 지정 링크]는 추적 데이터를 보내는 링크를 말합니다. The *`linkName`* 변수(또는 *`tl()`* 함수의 세 번째 매개 변수)는 [!UICONTROL 사용자 지정], [!UICONTROL 다운로드] 또는 [!UICONTROL 종료 링크] 보고서에 나타나는 값을 식별하는 데 사용됩니다. *`linkName`*&#x200B;을 채우지 않으면 링크의 URL이 보고서에 나타납니다.

**구문 및 가능한 값** {#section_C8D89834C98B4C7A858C947293C4148E}

```js
s.linkName="Link Name"
```

*`linkName`*&#x200B;에는 표준 변수 제한 외에는 제한이 없습니다.

**예** {#section_5F68766210184E82A23D2A6ECD80BA0B}

```js
s.linkName="Nav Bar Home Link"
```

```js
s.linkName="Partner Link to A.com"
```

**구성 설정** {#section_F15FF429FC274F708D50DF79D4668EA3}

없음

**함정, 질문 및 팁** {#section_170A78452A7340B5B229713AC1FB71FA}

* *`linkName`* 변수는 *`tl()`* 함수의 세 번째 매개 변수로 교체되었습니다.

* *`linkName`* 변수와 *`tl()`* 함수의 세 번째 매개 변수가 비어 있는 경우 링크가 상대 링크이더라도 링크의 전체 URL(쿼리 문자열은 예외)이 보고서에 표시됩니다.
