---
title: abort
description: abort 변수는 히트가 Adobe 데이터 수집 서버에 전송되지 않도록 하는 부울입니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# abort

`abort` 변수는 그 다음 추적 호출이 Adobe에 전송되지 않도록 하는 부울입니다.

## Adobe Experience Platform Launch에서 abort 변수 사용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 구문 및 Launch의 사용자 지정 코드 편집기

`abort` 변수는 부울입니다. 기본값은 `false`입니다.

* `true`로 설정하면 그 다음 추적 호출([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))이 데이터를 Adobe에 전송하지 않습니다.
* `false`로 설정하거나 정의하지 않을 경우 이 변수는 아무 작업도 하지 않습니다.

```js
s.abort = true;
```

>[!NOTE] `abort` 변수는 모든 추적 호출 후 `false`로 재설정됩니다. 동일한 페이지에서 후속 추적 호출을 중지해야 하는 경우에는 `abort`을 다시 `true`로 설정하십시오.

## 예

`abort` 변수는 [`doPlugins()`](../functions/doplugins.md) 함수에서 설정할 수 있습니다. 이 함수는 이미지 요청이 Adobe에 전송되기 전에 마지막으로 실행되는 함수입니다.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

일부 사용자 지정 링크 또는 디스플레이 광고의 외부 링크와 같이 추적하지 않으려는 활동을 식별하는 데 사용하는 논리에 집중할 수 있습니다.
