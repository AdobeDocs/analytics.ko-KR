---
description: s.t() 함수는 해당 페이지에 정의된 모든 변수를 이미지에 컴파일하고 서버로 보내는 역할을 합니다.
keywords: track; Analytics 구현; 페이지 추적; 페이지 추적
seo-description: s.t() 함수는 해당 페이지에 정의된 모든 변수를 이미지에 컴파일하고 서버로 보내는 역할을 합니다.
seo-title: s.t() 함수 - 페이지 추적
solution: Analytics
subtopic: 함수
title: s.t() 함수 - 페이지 추적
topic: 개발자 및 구현
uuid: 67696 E 46-1 E 0 D -4200-BFAD -4217 D 1023948
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# s.t() 함수 - 페이지 추적

s.t() 함수는 해당 페이지에 정의된 모든 변수를 이미지에 컴파일하고 서버로 보내는 역할을 합니다.

## 함수의 속성 {#section_DB1F3E216DCD4E12AE42BBDCD25B9626}

* [!UICONTROL s.t()] 호출을 제거하면 데이터가 [!DNL Analytics]에 도달하지 못합니다. 여러 [!UICONTROL s.t()] 호출은 여러 이미지 요청을 실행합니다(사이트에서 보고된 트래픽을 두 배로 만듬).

* 하나의 페이지 로드에서 두 개 이상의 이미지 요청을 실행하려면, [!UICONTROL s.tl()] 함수를 사용하는 것이 좋습니다.
* 이 함수를 실행하면 항상 [!UICONTROL 페이지 보기]가 증가하고, 항상 [!UICONTROL s.pageName] 변수가 포함됩니다.

## 구현 {#section_F75C7BD4A8954CD5BE066C6B88A4A01C}

[!UICONTROL 코드 관리자]에서 코드를 생성하면, 페이지 코드의 하단에 다음과 내용이 주어집니다.

```js
var s_code=s.t();if(s_code)document.write(s_code)//--></script> 
<script language="JavaScript" type="text/javascript"><!--if(navigator.appVersion.indexOf('MSIE')>=0)document.write(unescape('%3C')+'\!-'+'-')//--></script> 
<noscript><img src="https://yournameserver.112.2o7.net/b/ss/yourreportsuiteid/1/H.23.6--NS/0" height="1" width="1" border="0" alt="" /></noscript> 
```

코드의 각 줄에는 특정 목적이 있습니다.

```js
var s_code=s.t();if(s_code)document.write(s_code)//-->
```

이 코드 줄이 실제로 JavaScript 함수를 실행하는 것입니다. [!UICONTROL s_code] 변수 및 함께 사용되는 document.write 메서드는 이미지 개체를 지원하지 않는 브라우저를 위한 것입니다(버전 3 이전의 Netscape 브라우저와 버전 4 이전의 Internet Explorer. 전 인터넷 사용자의 .5% 미만으로 추산됨).

```js
<script language="JavaScript" type="text/javascript"><!--if(navigator.appVersion.indexOf('MSIE')>=0)document.write(unescape('%3C')+'\!-'+'-')//--></script> 
<noscript><img  
src="https://yournameserver.112.2o7.net/b/ss/yourreportsuiteid/1/H.23.6--NS/0" height="1" width="1" border="0" alt="" />
```

[!UICONTROL s.t()] 함수에 대한 추가 문의 사항은 해당 조직의 계정 관리자에게 문의하십시오. 계정 관리자는 도움을 줄 수 있는 Adobe 구현 컨설턴트와의 만남을 주선할 수 있습니다.
