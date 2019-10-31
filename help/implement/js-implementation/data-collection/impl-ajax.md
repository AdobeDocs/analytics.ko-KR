---
description: AJAX로 구현하는 것은 표준 HTML 페이지에서 코드를 배포하는 것과 똑같습니다.
keywords: Analytics 구현
seo-description: AJAX로 구현하는 것은 표준 HTML 페이지에서 코드를 배포하는 것과 똑같습니다.
seo-title: AJAX를 사용하여 구현
solution: Analytics
title: AJAX를 사용하여 구현
topic: 개발자 및 구현
uuid: 9e3477ef-7dea-4c76-ab61-36a188222be7
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# AJAX를 사용하여 구현

AJAX로 구현하는 것은 표준 HTML 페이지에서 코드를 배포하는 것과 똑같습니다.

비즈니스에 대답이 필요한 질문이 있으면, 필요성을 평가하고 변수를 지정합니다. 그런 다음 디자인을 적용하고 배포합니다. 초기 구현 단계를 거쳤다면 이러한 개념이 익숙할 것입니다.

## 솔루션 디자인 {#section_78F1C7AFBB4E4175A6FE04A962C9C9D0}

[!UICONTROL AJAX]를 혼합할 때의 차이점은 수집해야 하는 세부 사항의 수준을 먼저 이해하는 것입니다. 페이지에서 컨텐츠를 변경(거시적 수준)하거나 애플리케이션의 특성을 추적(미시적 수준)할 가능성은, 설정해야 하는 변수와 데이터를 Adobe로 보내는 가장 좋은 방법을 결정합니다.

## 코드 배포 {#section_F3FC6F07A3E148D89A4C9ABC442920C3}

JavaScript 코드에는 데이터를 보낼 수 있게 해주는 두 가지 함수가 있는데, 이와 같이 데이터를 보내는 데 사용해야 하는 방법을 알기 위해서는 따라야 할 지침이 있습니다.
동일한 페이지에서 이전에 이미지 요청이 수행된 경우, 먼저 이전에 설정한 변수의 값을 지워야 합니다. JavaScript용 [!DNL AppMeasurement]의 `clearVars()` 함수를 사용하거나, H 코드를 사용하는 경우 간단한 JavaScript 함수를 작성하여 변수를 지웁니다. 변경된 콘텐츠에 적절한 값, 즉 *`pageName`* 변수를 설정합니다. 변수가 설정되면 *`t()`* 함수를 호출합니다.

> [!NOTE]`s.t()` 를 호출하기 전에 s 개체에서 지속하지 않으려는 값이 있으면 삭제해야 합니다. JavaScript용 [!DNL AppMeasurement]를 사용 중인 경우 `s.clearVars()`를 호출할 수 있습니다. H 코드를 사용 중인 경우 간단한 루틴을 작성하여 변수를 빈 문자열로 설정하십시오.

```js
s.clearVars(); 
s.pageName="New Page" 
s.prop1="some value" 
void(s.t());
```

다음 예제는 JQuery `done` 함수의 `.ajax` 콜백에서 추적 호출을 보여줍니다.

```
$.ajax({ 
  url: "test.html", 
  dataType: "html" 
}) 
  .done(function( response ) { 
    $( "#content" ).html( response ); 
  s.clearVars(); 
  s.pageName = $( "h1:first" ).text(); 
  s.t(); 
  }); 
```

동일한 페이지에서 이전에 이미지 요청이 수행된 경우, 먼저 이전에 설정한 변수의 값을 지우십시오. 지우는 것은 다음 작업을 통해 수행할 수 있습니다.

* 간단한 JavaScript 함수를 작성하여 Adobe 변수 지우기
* Set the *`linkTrackVars`* 및 *`linkTrackEvents`* 변수를 [!DNL s_code.js] 파일에서 아직 설정하지 않았다면 설정합니다.

* 변경된 콘텐츠에 적절한 값, 즉 *`pageName`* 변수를 설정합니다. 
* 변수가 설정되면 *`tl()`* 함수를 호출합니다.

```js
//set linkTrackVars and linkTrackEvents> (if applicable) 
//set new variables 
s.tl(this,'o','Link Name');
```

```js
s.linkTrackVars="prop1,eVar1,events"; s.linkTrackEvents="event1"; 
s.prop1="some value"; s.eVar1="another value"; s.events="event1"; 
s.tl(this,'o','My Link Name');
```

