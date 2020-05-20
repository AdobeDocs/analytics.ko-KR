---
title: doPlugins
description: 히트가 컴파일되고 Adobe에 전송되기 바로 전에 논리를 구성합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# doPlugins

`doPlugins` 변수는 구현에서 값을 설정하는 &#39;마지막 호출&#39; 역할을 합니다. [`usePlugins`](../config-vars/useplugins.md)가 활성화된 경우 다음을 포함한 모든 유형의 이미지 요청이 컴파일되어 Adobe에 전송되기 바로 전에 자동으로 실행됩니다.

* 모든 페이지 보기([`t()`](t-method.md)) 호출
* 자동 다운로드 링크 및 종료 링크를 포함한 모든 링크 추적([`tl()`](tl-method.md)) 호출

이미지 요청이 컴파일되어 Adobe에 전송되기 바로 전에 `doPlugins` 변수를 사용하여 플러그인 코드를 호출하고 최종 변수 값을 설정하십시오.

## Adobe Experience Platform Launch의 플러그인

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드의 s.doPlugins

`s.doPlugins` 변수를 원하는 코드를 포함하는 함수로 설정하십시오. 추적 호출을 수행하면 함수가 자동으로 실행됩니다.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!NOTE] 함수를 구현에서 한 번만 `doPlugins` 변수로 설정하십시오. `doPlugins` 변수를 두 번 이상 설정하면 가장 최근 코드만 사용됩니다.

## 예

```js
// Set eVar1 to the web page's title
s.doPlugins = function() {
  s.eVar1 = window.document.title;
};

// Use the getPreviousValue plug-in (requires plug-in code outside the function)
s.doPlugins = function() {
  s.eVar1 = s.getPreviousValue(s.pageName,'gpv_pn');
}
```

>[!NOTE] 이전 버전의 AppMeasurement에는 약간 다른 `doPlugins()` 코드가 있었습니다. 위의 형식을 우수 사례로 사용하는 것이 좋습니다.
