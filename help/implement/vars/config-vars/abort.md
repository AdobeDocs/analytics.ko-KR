---
title: 중단
description: abort 변수는 히트가 Adobe 데이터 수집 서버로 전송되지 않도록 하는 부울입니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 중단

이 `abort` 변수는 다음 추적 호출이 Adobe로 전송되지 않도록 하는 부울입니다.

## Adobe Experience Platform Launch에서 중단 변수 사용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## Launch의 AppMeasurement 구문 및 사용자 지정 코드 편집기

이 `abort` 변수는 부울입니다. Its default value is `false`.

* 로 설정된 `true`경우 다음 추적 호출([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))은 데이터를 Adobe로 전송하지 않습니다.
* 로 설정되었거나 정의되지 `false` 않은 경우 이 변수는 아무 작업도 하지 않습니다.

```js
s.abort = true;
```

> [!NOTE] 이 `abort` 변수는 모든 추적 호출 `false` 후 로 재설정됩니다. 동일한 페이지에서 후속 추적 호출을 중지해야 하는 경우 `abort` 로 `true` 다시 설정합니다.

## 예

이 `abort` 변수는 [`doPlugins()`](../functions/doplugins.md) 함수에서 설정할 수 있습니다. 이 함수는 이미지 요청이 Adobe로 전송되기 전에 마지막으로 실행되는 함수입니다.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

사용하는 로직을 중앙에서 관리하여 일부 사용자 지정 링크 또는 디스플레이 광고의 외부 링크와 같이 추적하지 않을 활동을 식별할 수 있습니다.
