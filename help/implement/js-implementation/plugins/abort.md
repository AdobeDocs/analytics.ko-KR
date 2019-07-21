---
description: doPlugins 내부에 중단 플래그를 설정하여 현재 추적 호출이 전송되지 않도록 할 수 있습니다.
keywords: Analytics 구현
seo-description: doPlugins 내부에 중단 플래그를 설정하여 현재 추적 호출이 전송되지 않도록 할 수 있습니다.
seo-title: s.abort flag
solution: Analytics
title: s.abort flag
topic: 개발자 및 구현
uuid: 0 C 6 EC 8 C 7-D 136-4851-8 CB 6-6 CB 1 B 7 F 6 F 0 DC
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

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
