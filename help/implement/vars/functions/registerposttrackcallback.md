---
title: registerPostTrackCallback
description: Adobe에 히트를 보낸 후 콜백 함수를 만듭니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# registerPostTrackCallback

이 `registerPostTrackCallback` 변수를 사용하면 히트가 Adobe로 성공적으로 전송된 후 조직에서 JavaScript 함수를 바로 연결할 수 있습니다. 추적 호출이 실패하면 이 함수가 실행되지 않습니다. 이 변수를 사용하여 AppMeasurement에서 수집한 데이터를 파트너 또는 사내 인프라로 보내거나 단일 페이지 애플리케이션에서 변수 값을 정리할 수 있습니다.

> [!IMPORTANT] 변수 [`t()`](t-method.md) 내나 같은 추적 호출을 호출하지 마십시오 [`tl()`](tl-method.md) `registerPostTrackCallback` . 이 변수의 추적 기능을 사용하면 이미지 요청의 무한 루프가 발생합니다.

변수를 호출할 때마다 `registerPostTrackCallback` 이미지 요청이 성공적으로 전송된 후 해당 함수가 실행되도록 합니다. 동일한 페이지 로드에서 동일한 함수를 여러 번 등록하지 마십시오.

> [!NOTE] 두 함수 사이에 발생하는 시기와 순서는 [`registerPreTrackCallback`](registerpretrackcallback.md) 보장되지 `registerPostTrackCallback` 않습니다. 이러한 두 함수 간의 종속성을 방지합니다.

## Adobe Experience Platform Launch에서 게시물 추적 콜백 등록

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.registerPostTrackCallback in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.registerPostTrackCallback` 함수는 함수를 유일한 인수로 사용하는 함수입니다. 중첩 함수는 이미지 요청이 전송되기 직전에 실행됩니다.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

코드에서 이미지 요청 URL을 사용하려면 중첩 함수 내에서 `requestUrl` 문자열 인수를 참조하십시오. 원하는 용도로 변수를 구문 분석할 수 `requestUrl` 있습니다.이 변수를 조정해도 데이터 수집에는 영향을 주지 않습니다.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

함수에 추가 인수를 포함할 수 있으며, 이 인수는 중첩 함수에서 사용할 수 있습니다. `s.registerPostTrackCallback`

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## 사용 사례 예

게시물 추적 콜백에서 함수를 등록하면 단일 페이지 애플리케이션에 유익할 수 있습니다. [`clearVars()`](clearvars.md) Adobe에 히트를 성공적으로 보낼 때마다 `clearVars()` 함수가 실행됩니다. 그런 다음 구현을 통해 값을 잘못 유지하는 것에 대한 걱정 없이 변수를 다시 정의할 수 있습니다.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
