---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 8c06a54ccd652f3f915af3af040e9cc69f01d0c1

---


# s.useForcedLinkTracking

이 플래그는 일부 브라우저에 대한 강제 링크 추적을 비활성화하는 데 사용됩니다. 강제 링크 추적은 FireFox 20 이상과 WebKit 브라우저에 대해 기본적으로 활성화됩니다.

When `useForcedLinkTracking` is enabled, the AppMeasurement file overrides the default link behavior on some browsers to prevent the track link call from being canceled when the new page opens. AppMeasurement 파일은 기본 브라우저 작업을 사용하는 대신 추적 링크 호출을 실행하고 탐색 이벤트를 수동으로 처리합니다.

JavaScript H.25.4(2013년 2월 발표)에서는, `useForcedLinkTracking`이 활성화되면 추적되는 링크에 다음의 범위 제한을 추가했습니다. 자동 강제 링크 추적은 다음의 경우에만 적용됩니다.

* `<A>` 및 `<AREA>` 태그에서 보냅니다.
* 태그에 `HREF` 특성이 반드시 있어야 함.
* The `HREF` can't start with `#`, `about:`, or `javascript:`.
* The `TARGET` attribute must not be set, or the `TARGET` needs to refer to the current window ( `_self`, `_top`, or the value of `window.name`).

기본값 = true

## 예

`s.useForcedLinkTracking = false`

