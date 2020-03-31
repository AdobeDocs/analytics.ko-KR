---
title: pageType
description: 현재 페이지가 404 오류인지 판단합니다.
translation-type: ht
source-git-commit: 751d19227d74d66f3ce57888132514cf8bd6f7fc

---


# pageType

`pageType` 변수는 404 오류와 같이 사이트에서 오류 페이지를 지정하는 데 사용되는 플래그입니다. 이 변수에 문자열 `errorPage`가 포함되어 있으면 &#39;페이지를 찾을 수 없음&#39; 차원이 채워집니다.

> [!IMPORTANT] 오류가 아닌 페이지에서 이 변수를 설정하지 마십시오.

## Adobe Experience Platform Launch의 페이지 유형

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.pageType

`s.pageType` 변수는 값 `errorPage`가 유일하게 유효한 값인 문자열입니다. 이 변수는 404 페이지처럼 사이트의 어떤 오류 페이지에서든 이 값으로 설정하십시오.

```js
s.pageType = "errorPage";
```

> [!TIP] 방문자가 사이트에서 당면하는 특정 오류에 대한 자세한 정보를 사용자가 알 수 있도록 오류 코드를 수집하려면 eVar를 사용하십시오.
