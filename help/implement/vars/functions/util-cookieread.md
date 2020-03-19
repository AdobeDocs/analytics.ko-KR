---
title: Util.cookieRead
description: 쿠키에 사용할 값을 가져옵니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Util.cookieRead

쿠키는 동일한 도메인의 페이지 간에 정보를 저장하고 검색할 수 있습니다. 쿠키에서 값을 검색하려면 `Util.cookieRead()` 메서드를 사용합니다.

## Adobe Experience Platform Launch에서 쿠키 읽기

데이터 요소의 값을 설정하여 쿠키를 읽을 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 데이터 요소를 클릭합니다(또는 데이터 요소 만들기). [!UICONTROL Data Elements]
4. 드롭다운을 [!UICONTROL Extension] 설정하고 [!UICONTROL Core]을 [!UICONTROL Data Element Type] [!UICONTROL Cookie]설정합니다.
5. 텍스트 필드에 쿠키 이름을 입력합니다.

쿠키 값은 데이터 요소에 저장됩니다. 그런 다음 규칙의 데이터 요소를 참조하여 Analytics 변수를 할당할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.Util.cookieRead()

메서드를 호출하여 원하는 쿠키 값을 읽습니다. `s.Util.cookieRead()` 유일한 인수는 필요한 문자열입니다. 이 메서드는 쿠키 값을 포함하는 문자열을 반환합니다. 쿠키가 없으면 빈 문자열이 반환됩니다.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
