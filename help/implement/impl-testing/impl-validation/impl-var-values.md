---
description: 서버 스크립팅이나 코드에서 채워지는 변수는 값을 방해하는 인용 부호를 출력할 수 없습니다.
keywords: Analytics 구현
seo-description: 서버 스크립팅이나 코드에서 채워지는 변수는 값을 방해하는 인용 부호를 출력할 수 없습니다.
seo-title: 변수 및 값
solution: Analytics
title: 변수 및 값
topic: 개발자 및 구현
uuid: 2 FF 4857 A -9451-4794-9146-F 417 ABD 1 D 1 BA
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 변수 및 값

서버 스크립팅이나 코드에서 채워지는 변수는 값을 방해하는 인용 부호를 출력할 수 없습니다.

예:

```js
s.pageName="Article: "Article Name"" 
s.pageName='Company's Information' 
```

변수의 값이 이 문서에 지정된 최대 제한을 초과하지 않도록 하십시오. 제한을 초과하는 문자는 데이터 수집 서버에서 잘립니다. 이러한 추가적인 문자는 전체 길이에 지장을 주고, 대역폭을 불필요하게 증가시키고, 기타 문제를 일으킬 수 있습니다.

products 변수에서는 $, ™, ®, © 또는 쉼표(,)를 사용하지 마십시오. 일반적으로, 이 문자들은 [!DNL Analytics] 변수에서 유용하지 않으며, 필드를 해석하거나 내보내는 기능을 방해할 수 있습니다. 문자를 처음 127자의 ASCII 문자로 제한하는 것이 좋습니다.

Ensure that the events variable is populated with an appropriate value ( [!UICONTROL prodView], [!UICONTROL purchase], [!UICONTROL scAdd], [!UICONTROL scRemove], [!UICONTROL scOpen], or event1-event5) whenever *`products`* is populated. 모든 [!DNL Analytics] 변수와 함수의 대소문자가 아래에서 보듯이 유지되는지 확인하십시오.

```js
s.pageName 
s.server 
s.channel 
s.pageType 
s.prop1 - s.prop20 
s.campaign 
s.state 
s.zip 
s.events 
s.products 
s.purchaseID 
s.eVar1 - s.eVar20 
var s_code=s.t();if(s_code)document.write(s_code)//--> 
```

페이지 이름은 대소문자를 구분하며, 차이가 나면 새로운 페이지 레코드가 생성됩니다. "Home" 및 "home"은 [!DNL Analytics] 내에서 두 개의 서로 다른 페이지입니다.

>[!NOTE]
>
>여러 페이지 레코드는 보고서 내에서 결합할 수 없습니다.

링크가 [!UICONTROL 사용자 지정 링크] 보고서로 보고되는지 확인하십시오. [!UICONTROL tl] 함수에 올바른 매개 변수를 전달했는지 확인하십시오. [!UICONTROL 사용자 지정 링크]에 대한 자세한 내용은 [링크 추적](../../../implement/js-implementation/function-tl.md#concept_EA13689CB8EE4F308FC89A1293046D5E).
