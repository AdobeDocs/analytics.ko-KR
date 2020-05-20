---
title: registerPreTrackCallback
description: Adobe에 히트를 보내기 전 콜백 함수를 만듭니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# registerPreTrackCallback

`registerPreTrackCallback` 변수를 사용하면 이미지 요청 URL이 컴파일된 후 전송되기 전에 조직에서 JavaScript 함수를 후크할 수 있습니다. 이 변수를 사용하여 AppMeasurement에서 수집한 데이터를 파트너 또는 사내 인프라에 보낼 수 있습니다.

>[!IMPORTANT] [`t()`](t-method.md) 변수 내에서 [`tl()`](tl-method.md) 또는 [`registerPostTrackCallback`](registerposttrackcallback.md) 같은 추적 호출을 호출하지 마십시오. 이 변수에서 추적 함수를 사용하면 이미지 요청의 무한 루프가 발생합니다.

`registerPreTrackCallback` 변수를 호출할 때마다 이미지 요청 URL이 컴파일될 때 해당 함수를 실행하도록 후크합니다. 동일한 페이지 로드에서 동일한 함수를 여러 번 등록하지 마십시오.

>[!NOTE] `registerPreTrackCallback`과 `registerPostTrackCallback` 사이에 실행된 함수의 타이밍과 순서는 보장되지 않습니다. 이 두 함수 간에 종속성이 생기지 않도록 하십시오.

## Adobe Experience Platform Launch에서 사전 추적 콜백 등록

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.registerPreTrackCallback

`s.registerPreTrackCallback`은 함수를 유일한 인수로 사용하는 함수입니다. 중첩 함수는 이미지 요청이 전송되기 바로 전에 실행됩니다.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

코드에서 이미지 요청 URL을 사용하려면 중첩 함수 내에서 `requestUrl` 문자열 인수를 참조하십시오. 원하는 용도로 `requestUrl` 변수를 구문 분석할 수 있습니다. 이 변수를 조정해도 데이터 수집에는 영향을 주지 않습니다.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

`s.registerPreTrackCallback` 함수에서 추가 인수를 포함할 수 있으며 이 인수는 중첩 함수에서 사용할 수 있습니다.

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

>[!NOTE] 페이지 변수를 설정하거나 이 함수 내에서 `requestUrl` 문자열을 변경해도 이 함수 호출 직후 전송된 이미지 요청에는 영향을 주지 **않습니다**. [`doPlugins()`](doplugins.md) 변수를 대신 사용하십시오.
