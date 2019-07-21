---
description: 구매 이벤트의 경우, 특정 구매 정보를 캡처하는 데는 Analytics 변수를 사용합니다. s.purchaseID 변수는 이벤트를 정리(중복 제거)하는 데 사용됩니다.
keywords: Analytics 구현
seo-description: 구매 이벤트의 경우, 특정 구매 정보를 캡처하는 데는 Analytics 변수를 사용합니다. s.purchaseID 변수는 이벤트를 정리(중복 제거)하는 데 사용됩니다.
seo-title: 구매 이벤트
solution: Analytics
title: 구매 이벤트
topic: 개발자 및 구현
uuid: D 90 CDEC 7-7397-445 A -84 E 5-31014 F 7 FF 875
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 구매 이벤트

구매 이벤트의 경우, 특정 구매 정보를 캡처하는 데는 Analytics 변수를 사용합니다. s.purchaseID 변수는 이벤트를 정리(중복 제거)하는 데 사용됩니다.

The *`purchaseID`* is limited to 20 characters. *`purchaseID`* 변수는 변수 [!UICONTROL s.events]에서 전달 받은 모든 이벤트를 정리하고, 이벤트에 대한 모든 일련화 값을 무시합니다. If *`purchaseID`* is left blank, each instance of the purchase event, even page reloads, is counted.

구매 이벤트가 *`purchaseID`* 없이 호출되면 고유한 ID가 *`s.products`* 및 *`s.events`변수를 기준으로 자동 생성됩니다.* 이렇게 자동 생성된 *`purchaseID`는 방문자의 브라우저에 쿠키 값으로 로컬 저장되고 보고서 세트 표로 전송됩니다.* Manually defined *`purchaseID`*s on the other hand are sent to a back-end table within the report suite. The last five purchases made by a visitor (with or without *`purchaseID`*) are stored in the local cookie.

방문자가 구입을 하면 다음 사항이 확인됩니다.

*   *`purchaseID`*&#x200B;가 이 5개의 쿠키 값 중 하나와 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
* If *`purchaseID`* is defined, does it match any value in the report suite's back-end table? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
* *`purchaseID`*&#x200B;가 쿠키에 저장된 마지막 5개 값 및 보고서 세트의 *`purchaseID`테이블에 대해 고유한 경우 이미지 요청이 고유한 것으로 보고에 포함됩니다.* 예를 들어, 5개의 구매가 이미 로컬 쿠키에 포함된 경우 가장 오래된 쿠키가 덮어쓰기됩니다.

특정 서버측 코드를 사용하여 HTML 소스에 포함된 고유 번호(영숫자 값)를 생성할 수 있습니다. 일반적으로 주문 ID나 유사한 영숫자 값이 이러한 목적으로 사용됩니다. 사용자가 페이지를 새로 고칠 경우에는 이 값을 변경하면 안 됩니다. 다음은 간단한 예( *`purchaseID`*&#x200B;코드가 굵은 글씨임)입니다.

## 구문 {#section_4FBF138093BD41F59885D2ACC429FF5B}

```js
s.products="Category;ProductName;Qty;total_price [,Category2;ProductName2;Qty;total_price]" 
s.state="XX" 
s.zip="00000" 
 
<b>s.purchaseID="<%=getPurchaseID()%>"</b> 
s.events="purchase" 
```

## 예 {#section_2CBA9B6386A146C0BEF375E1B55687BC}

```js
s.products="Footwear;Hiking Boots (1234);1;170.00" 
s.state="UT" 
s.zip="84097" 
s.purchaseID="12341234" 
s.events="purchase"
```

## 추가 참고 사항 {#section_5A0590B8FD4F40DC89776F55ED9DE668}

* 이벤트에 대한 고유 식별자를 생성할 때는 반드시 서버측 코드를 사용하십시오. JavaScript 무작위 함수를 사용하여 번호를 생성하지 마십시오. 이 함수는 페이지를 로드할 때마다 고유 번호를 생성합니다(각 [!UICONTROL 인스턴스]/[!UICONTROL 페이지 보기] 횟수).

* 고유 식별자는 모든 세션의 모든 사용자에게 적용할 수 있습니다. 따라서 식별자가 사용자 및 세션 간에 고유하도록 하십시오. 예를 들어 주문 ID가 30일 후 반복되는 경우, 주문 날짜를 추가하여 [!UICONTROL 주문 ID]를 충분히 고유하게 만드십시오.
* 일련화 값의 길이는 영숫자로 최대 20자입니다. 이것은 [!UICONTROL s.purchaseID](G 코드의 경우 s.는 s_로 대체됨)의 제한과 동일합니다.
* [!UICONTROL s.purchaseID] 변수는 변수 [!UICONTROL s.events]에서 전달 받은 모든 이벤트를 정리하고, 이벤트에 대한 모든 일련화 값을 무시합니다. 현재 페이지에서 [!UICONTROL s.purchaseID] 변수를 사용하는 경우(G 코드의 경우 s.는 s_로 대체됨), 어떤 이벤트에도 [!UICONTROL 이벤트 정리]를 사용하지 마십시오.

