---
title: pageType
description: 현재 페이지가 404 오류인지 확인합니다.
translation-type: tm+mt
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# pageType

이 `pageType` 변수는 404 오류와 같이 사이트에서 오류 페이지를 지정하는 데 사용되는 플래그입니다. 이 변수에 문자열이 포함되어 `errorPage`있으면 &#39;페이지를 찾을 수 없음&#39; 차원이 채워집니다.

> [!IMPORTANT] 오류가 아닌 페이지에서 이 변수를 설정하지 마십시오.

## Adobe Experience Platform Launch의 페이지 유형

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.pageType in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.pageType` 변수는 값이 `errorPage` 유일한 유효한 값인 문자열입니다. 404페이지 등 사이트에서 오류 페이지에 이 변수를 이 값으로 설정합니다.

```js
s.pageType = "errorPage";
```

> [!TIP] eVar를 사용하여 오류 코드를 수집하면 방문자가 사이트에서 발생하는 특정 오류에 대한 자세한 내용을 볼 수 있습니다.
