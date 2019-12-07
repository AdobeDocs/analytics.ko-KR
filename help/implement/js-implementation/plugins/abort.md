---
description: doPlugins 내부에 중단 플래그를 설정하여 현재 추적 호출이 전송되지 않도록 할 수 있습니다.
keywords: Analytics Implementation
title: s.abort flag
topic: Developer and implementation
uuid: 0c6ec8c7-d136-4851-8cb6-6cb1b7f6f0dc
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# s.abort flag

doPlugins 내부에 중단 플래그를 설정하여 현재 추적 호출이 전송되지 않도록 할 수 있습니다.

abort 플래그가 모든 추적 호출로 재설정되므로, 추적 호출 또한 무시해야 할 경우 우 플래그를 doPlugins 내에서 다시 설정해야 합니다.

```js
s.doPlugins = function(s) { 
     s.campaign = s.getQueryParam("cid"); 
     if ((!s.campaign) && (!s.events)) { 
          s.abort = true; 
     } 
};
```

이는 사용하는 로직에 집중할 수 있게 하여 일부 사용자 지정 링크 또는 디스플레이 광고의 외부 링크와 같이 추적하지 않으려는 활동을 식별할 수 있습니다.
