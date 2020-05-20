---
title: Analytics 구현에 대한 FAQ
description: 구현에 대한 자주 묻는 질문 및 추가 정보 링크.
keywords: Analytics Implementation;faq;frequently asked questions;evar expiration;custom event visibility;timestamp;visitor id grace period;visitor id;Experience Cloud visitor id;analytics visitor id;dtm;heartbeat;cookies;tracking server;performance;javascript;data collection;s_code version;s_code debug;track link types;track video;track mobile app;first party cookie;ssl certificate;certification expiration;certificate expiration;plugins;data insertion api;500 error;500;Manage user;manage group;users;groups
translation-type: ht
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Analytics 구현에 대한 FAQ

구현에 대한 자주 묻는 질문 및 추가 정보 링크.

**변수 할당과 만료 간의 차이는 무엇입니까?**

할당과 만료는 모두 사용자 지정 변수에 적용할 수 있는 설정입니다. *할당*&#x200B;은 지속되는 변수 값과 새 변수 값이 있을 때 실행되며 이전 값이 유지되는지 아니면 새 값이 유지되는지를 결정합니다. *만료*&#x200B;은 변수 값이 계속 지속되지 않도록 하려 할 때 실행됩니다.

**Experience Cloud 방문자 ID와 Analytics 방문자 ID의 차이점은 무엇입니까?**

ID 서비스는 Experience Cloud에 있는 다른 솔루션 간에 공유할 수 있는 고유한 영구 식별자를 지정합니다. Analytics 방문자 ID는 Analytics에서만 사용됩니다. 구현에서는 Experience Cloud 방문자 ID 서비스를 사용하는 것이 좋습니다.

**쿠키가 차단된 경우 방문자 ID는 어떻게 설정됩니까?**

표준 `s_vi` 쿠키를 사용할 수 없을 경우, 무작위로 생성된 고유 ID를 사용하는 대체 쿠키가 웹 사이트의 도메인에 만들어집니다. `s_fid`라는 이 쿠키는 2년 동안 사용할 수 있으며 앞으로 식별 대비책으로 사용됩니다.

**하트비트 비디오 추적은 어떻게 구현합니까?**

[Adobe Analytics에서 오디오 및 비디오 측정](https://docs.adobe.com/content/help/ko-KR/media-analytics/using/media-overview.html)을 참조하십시오.

**Adobe의 서비스 중단이 성능에 영향을 줄 수 있습니까?**

아니요. JavaScript 파일은 Adobe 서버에서 호스팅되지 않으므로 Adobe 중단은 AppMeasurement 라이브러리에 영향을 주지 않습니다. Adobe Experience Platform Launch를 사용하는 경우, JavaScript 파일은 Akamai에 의해 호스팅되거나, 조직이 결정한 서버 위치에서 호스팅됩니다.

**데이터를 브라우저에서 Adobe 서비스로 보내면 성능이 저하될 수 있습니까?**

AppMeasurement는 HTML 페이지 내에 이미지 개체를 만들며, 그렇게 되면 브라우저가 Adobe 데이터 수집 서버의 이미지 개체를 요청합니다. 데이터 수집 서버가 느려지거나 응답을 하지 않으면, 이미지가 반환되거나, 시간 초과가 발생할 때까지 해당 요청을 처리하는 스레드가 지연됩니다. 브라우저는 여러 스레드로 이미지를 처리하고, Adobe 중단이 페이지 로드 시간에 미치는 영향은 매우 작으므로, 다른 스레드가 계속 작동하는 동안 한 스레드를 연결 중입니다.

**모바일 앱을 어떻게 추적합니까?**

Adobe Experience Platform SDK를 사용할 수 있습니다. 자세한 내용은 [Adobe Experience Platform SDK 개요](https://aep-sdks.gitbook.io/docs/)를 참조하십시오.

**플러그인이란?**

플러그인은 고급 기능을 수행하는 코드 조각으로서, AppMeasurement의 기능을 확장하여 구현에 더 많은 기능을 제공합니다.
