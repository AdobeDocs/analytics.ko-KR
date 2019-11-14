---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 0c7093518933a88c5057ba95cb3564d6ca0ebcad

---



# s.forcedLinkTrackingTimeout

이 값은 최대 대기 시간을 지정합니다. Specifically, it sets the maximum number of milliseconds to wait for tracking to finish before performing the `doneAction` that was passed into `s.tl`. 이 시간 초과 전에 추적 링크 호출이 완료되면 `doneAction`이 즉시 실행됩니다. 추적 링크 호출이 완료되지 않고 있다는 것을 확인한 경우 이 시간 초과를 늘려야 할 수도 있습니다.

기본값 = 250

예: `s.forcedLinkTrackingTimeout = 500`
