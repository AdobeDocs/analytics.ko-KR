---
title: registerPostTrackCallback
description: Adobe에 히트를 보낸 후 콜백 함수를 만듭니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# registerPostTrackCallback

`registerPostTrackCallback` 변수를 사용하면 히트가 성공적으로 Adobe에 전송된 직후 조직에서 JavaScript 함수를 후크할 수 있습니다. 추적 호출이 실패하면 이 함수는 실행되지 않습니다. 이 변수를 사용하여 AppMeasurement에서 수집한 데이터를 파트너 또는 사내 인프라에 보내거나 단일 페이지 애플리케이션에서 변수 값을 정리할 수 있습니다.

>[!IMPORTANT] [`t()`](t-method.md) 변수 내에서 [`tl()`](tl-method.md) 또는 `registerPostTrackCallback` 같은 추적 호출을 호출하지 마십시오. 이 변수에서 추적 함수를 사용하면 이미지 요청의 무한 루프가 발생합니다.

`registerPostTrackCallback` 변수를 호출할 때마다 이미지 요청이 성공적으로 전송된 직후 해당 함수를 실행하도록 후크합니다. 동일한 페이지 로드에서 동일한 함수를 여러 번 등록하지 마십시오.

>[!NOTE] [`registerPreTrackCallback`](registerpretrackcallback.md)과 `registerPostTrackCallback` 사이에 실행된 함수의 타이밍과 순서는 보장되지 않습니다. 이 두 함수 간에 종속성이 생기지 않도록 하십시오.

## Adobe Experience Platform Launch에서 사후 추적 콜백 등록

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.registerPostTrackCallback

`s.registerPostTrackCallback`은 함수를 유일한 인수로 사용하는 함수입니다. 중첩 함수는 이미지 요청이 전송되기 바로 전에 실행됩니다.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

코드에서 이미지 요청 URL을 사용하려면 중첩 함수 내에서 `requestUrl` 문자열 인수를 참조하십시오. 원하는 용도로 `requestUrl` 변수를 구문 분석할 수 있습니다. 이 변수를 조정해도 데이터 수집에는 영향을 주지 않습니다.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

추가적인 인수는 `s.registerPostTrackCallback` 함수에 포함할 수 있으며, 중첩 함수에서 사용할 수 있습니다.

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## 사용 사례 예

사후 추적 콜백의 [`clearVars()`](clearvars.md) 함수를 등록하는 것은 단일 페이지 애플리케이션에 유익할 수 있습니다. 히트를 Adobe에 성공적으로 보낼 때마다 `clearVars()` 함수가 실행됩니다. 그러면 구현 시 값이 잘못 유지될 염려없이 변수를 다시 정의할 수 있습니다.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
