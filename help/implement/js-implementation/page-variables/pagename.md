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


# pageName

 변수에는 사이트에 있는 각 페이지의 이름이 들어 있습니다.

<!-- 

pageName.xml

 -->

<table id="table_0D09BAEC2FFD43F7905ED3649B3F8E05"> 
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
   <td> pageName </td> 
   <td> <p>페이지 </p> <p>경로 </p> </td> 
   <td> 페이지 URL </td> 
  </tr> 
 </tbody> 
</table>

The *`pageName`*&#x200B;변수는 비즈니스 사용자가 인식하는 값으로 채워야 합니다. 대부분의 경우 *`pageName`* 값은 URL 또는 파일 경로가 아닙니다. 일반적으로 *`pageName`* 값에는 "홈 페이지", "체크아웃", "구매 감사" 또는 "등록"과 같은 이름이 포함되어 있습니다.

줄바꿈, -em이나 -en 대시 또는 모든 HTML 문자가 페이지 이름과 다른 변수에 나타나지 않도록 주의하십시오. 일부 브라우저에서는 다른 브라우저에서 보내지 않는 줄바꿈 문자를 보내 보기에는 동일한 두 개의 페이지 이름 사이에서 Analytics의 데이터가 분리되기도 합니다. 많은 워드 프로세서 및 이메일 클라이언트는 하이픈을 입력하면 자동으로 -en이나 -em 대시로 변환합니다. -en 및 -em 대시는 Analytics 변수에 사용할 수 없는 문자(127개가 넘는 코드의 ASCII 문자)이므로, Analytics는 잘못된 문자가 들어 있는 페이지 이름을 기록하지 않고 대신 URL을 보여 줍니다.

*`pageName`*&#x200B;을 비워 두면 페이지 이름을 나타내는 데 URL이 사용됩니다. *`pageName`*&#x200B;을 비워 두면 종종 문제가 발생할 수 있습니다. 다른 URL을 사용하는 동일한 페이지 `www.mysite.com` 및 `mysite.com`에 대해 URL이 동일하지 않은 경우도 있을 수 있기 때문입니다.

**구문 및 가능한 값** {#section_7A61EE70F1A84D26B414404998C84BA8}

*`pageName`* 변수에는 Analytics의 비즈니스 사용자에게 유용한 식별자가 들어 있어야 합니다.

```js
s.pageName="page_name"
```

*`pageName`*&#x200B;에는 표준 변수 제한 외에는 제한이 없습니다.

**예** {#section_8BB4F86F84E246A08B72DEC47FFC0765}

```js
s.pageName="Search Results" 
```

```js
s.pageName="Standard Offer List"
```

**구성 설정** {#section_58CBC68C805344A999EB47455FEBA8D5}

관리자는 [!UICONTROL 페이지 명명] 도구로 Analytics에서 표시되는 페이지 이름을 변경할 수 있지만, 이 도구를 사용하는 것은 위험할 수 있으며 보고서에 부정적인 영향을 줄 수 있습니다. 따라서 [!UICONTROL 페이지 명명] 도구를 사용하려면 그 전에 Adobe 고객 지원 센터에 문의하십시오.

**함정, 질문 및 팁** {#section_BB41DC9682C34385B9CAA80D5257C113}

*`pageName`*&#x200B;에 잘못된 문자가 포함되어 있지 않은지 확인하십시오.
