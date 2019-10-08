---
description: 구매 이벤트의 경우, 특정 구매 정보를 캡처하는 데는 Analytics 변수를 사용합니다. s.purchaseID 변수는 이벤트를 정리(중복 제거)하는 데 사용됩니다.
keywords: Analytics 구현
seo-description: 구매 이벤트의 경우, 특정 구매 정보를 캡처하는 데는 Analytics 변수를 사용합니다. s.purchaseID 변수는 이벤트를 정리(중복 제거)하는 데 사용됩니다.
seo-title: 구매 이벤트
solution: Analytics
title: 구매 이벤트
topic: 개발자 및 구현
uuid: d90cdec7-7397-445a-84e5-31014f7ff875
translation-type: tm+mt
source-git-commit: e21bb18dd0d0eb13222c655091c3a87939a0351d

---


# 구매 이벤트

구매 이벤트의 경우, 특정 구매 정보를 캡처하는 데는 Analytics 변수를 사용합니다. `s.purchaseID` 변수는 이벤트를 정리(중복 제거)하는 데 사용됩니다.

구매 이벤트가 `purchaseID` 없이 호출되면 고유한 ID가 `s.products` 및 `s.events` 변수를 기준으로 자동 생성됩니다. 자동으로 생성된 이 구매 ID는 방문자의 브라우저 내에서 쿠키 값으로 로컬에 저장되며 Adobe로 전송되지 않습니다. 수동으로 정의된 구매 ID는 Adobe로 전송됩니다. 방문자가 구매한 마지막 5개(구매 ID 포함 또는 불포함)는 로컬 쿠키에 저장됩니다.

방문자가 구입을 하면 다음 사항이 확인됩니다.

*   구매 ID가 5개의 쿠키 값 중 하나와 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
* 정의된 `s.purchaseID` 경우, 보고서 세트에 이미 수집된 값과 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.

특정 서버측 코드를 사용하여 HTML 소스에 포함된 고유 번호(영숫자 값)를 생성할 수 있습니다. 일반적으로 주문 ID나 유사한 영숫자 값이 이러한 목적으로 사용됩니다. 사용자가 페이지를 새로 고칠 경우에는 이 값을 변경하면 안 됩니다.

## 구문

```js
s.purchaseID="12345678";
```

## 예

```js
s.products="Footwear;Hiking Boots;1;170.00";
s.purchaseID="12345678";
s.events="purchase";
```

## 추가 참고 사항

* JavaScript 무작위 지정 함수를 사용하여 숫자를 생성하지 마십시오. 이 함수는 페이지를 로드할 때마다 고유 번호를 생성합니다. Adobe에서는 데이터 레이어를 사용하여 주어진 구매 ID를 저장하는 것이 좋습니다.
* 고유 식별자는 모든 세션의 모든 사용자에게 적용할 수 있습니다. 모든 구매 ID가 고유한지 확인합니다.
* 유효한 값은 최대 20자의 영숫자 값입니다.
* `s.purchaseID``s.events` 변수는 변수 에서 전달 받은 모든 이벤트를 정리하고, 이벤트에 대한 모든 일련화 값을 무시합니다. 변수가 [!UICONTROL 현재 페이지에서 사용되는 경우 이벤트에 대해 이벤트 정리를] `s.purchaseID` 사용하지 마십시오.
* If the `s.purchaseID` variable is left blank, each instance of the purchase event, even page reloads, is counted.
