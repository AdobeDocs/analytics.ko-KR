---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.registerPreTrackCallback and s.registerPostTrackCallback

이 함수들은 매개 변수로서 콜백(기능)을 사용하고 해당 기능에 대한 매개 변수를 사용합니다. 예:

```
s.registerPreTrackCallback(function(requestUrl,a,b,c) { 
    console.log("pre track callback"); 
    console.dir(requestUrl); // Request URL 
    console.dir(a); // param1 
    console.dir(b); // param2 
    console.dir(c); // param3 
}, "param1", "param2", "param3");
```

콜백은 콜백을 등록할 때 전달되는 모든 매개 변수와 `requestUrl`과 함께 호출됩니다. 이러한 일은 콜백을 등록하는 데 사용되는 메서드에 따라 추적 호출 전 또는 후에 발생합니다.

이러한 콜백이 호출되는 순서는 보장되지 않습니다. 사전 함수에 등록된 콜백은 최종 추적 URL이 생성된 후 호출됩니다. 사후 콜백은 추적 호출 성공 시 호출됩니다(추적 호출이 실패하는 경우에는 이 함수들이 호출되지 않습니다). `registerPreTrackCallback`과 함께 등록된 모든 콜백은 추적 호출에 영향을 주지 않습니다. 또한, 등록된 임의의 콜백에서는 추적 메서드를 호출하지 않는 것이 좋으며, 호출하는 경우 무한 루프가 발생할 수 있습니다.
