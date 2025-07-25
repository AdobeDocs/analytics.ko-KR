---
title: Util.cookieRead
description: 쿠키에 사용할 값을 가져옵니다.
feature: Appmeasurement Implementation
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 72%

---

# Util.cookieRead

쿠키는 동일한 도메인에 있는 페이지 간에 정보를 저장하고 검색할 수 있습니다. 쿠키에서 값을 검색하려면 `Util.cookieRead()` 메서드를 사용하십시오.

## Adobe Analytics 확장 및 Web SDK 확장을 사용하여 쿠키를 읽습니다.

데이터 요소의 값을 설정하여 쿠키를 읽을 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 데이터 요소] 탭으로 이동한 다음, 원하는 데이터 요소를 클릭하거나 데이터 요소를 만듭니다.
4. [!UICONTROL 확장] 드롭다운 목록을 **[!UICONTROL 코어]**(으)로 설정하고 [!UICONTROL 데이터 요소 유형]을(를) **[!UICONTROL 쿠키]**(으)로 설정합니다.
5. 텍스트 필드에 쿠키 이름을 입력합니다.

쿠키 값은 데이터 요소에 저장됩니다. 그런 다음 규칙의 데이터 요소를 참조하여 원하는 변수를 할당할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.Util.cookieRead()

원하는 쿠키 값을 읽으려면 `s.Util.cookieRead()` 메서드를 호출하십시오. 이 메서드의 유일한 인수는 문자열로서, 필수입니다. 이 메서드는 쿠키 값을 포함하는 문자열을 반환합니다. 쿠키가 존재하지 않으면 빈 문자열이 반환됩니다.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
