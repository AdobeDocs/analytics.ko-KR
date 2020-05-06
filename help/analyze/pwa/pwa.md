---
title: Analytics용 PWA
description: Adobe Analytics용 PWA(Progressive Web App)
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 75%

---


# Adobe Analytics용 PWA

이 페이지에서는 PWA(점진적 웹 앱)와 함께 Adobe Analytics를 사용하는 방법에 대해 설명합니다.

## 소개

PWA는 웹 사이트에 기본 앱 환경과 오프라인 기능을 제공할 수 있습니다. 일반적으로 PWA에는 빠른 로드 시간, 쉬운 탐색 및 반응 동작에 모두 도움이 되는 서비스 작업자, 캐싱 프로비전 및 매니페스트 파일이 포함되어 있습니다.

Adobe Analytics는 기존 웹 사이트에서와 마찬가지로 PWA와도 매끄럽게 연동됩니다. PWA에는 점진적으로 스스로 동작하기 위한 몇 가지 추가 요구 사항이 있지만 Analytics가 기존 웹 사이트와 다르게 데이터를 수집하거나 보고하는 방법에 대한 장애 요소나 제한을 만들지 않습니다. 실제로 Analytics에는 오프라인 추적 기능이 이미 포함되어 있으므로 PWA를 사용하면 기존 웹 사이트보다 이러한 내장된 기능을 보다 손쉽게 활용할 수 있습니다.

## PWA Analytics 데이터 가져오기

To collect and analyze your PWA data with [!UICONTROL Analytics], you do not need to  make any configuration changes. [!UICONTROL Analytics는 기존 웹 사이트에서와 동일한 모든 기능과 특징을 자동으로 제공합니다.]

## 오프라인 추적을 추가하여 PWA 효율성 향상

You can increase the effectiveness of your PWA by using Adobe Analytics [offline tracking capabilities](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/offline-tracking.html) with it. 기본적으로 이 기능은 꺼져 있지만 다음 속성을 AppMeasurement.js 파일에 추가하여 켤 수 있습니다. `s.trackOffline=true;`

예를 들어 다음 AppMeasurement.js 파일에서 속성이 `CONFIG SECTION` 끝에 추가됩니다.

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx" 
s.linkInternalFilters="javascript:" //optional: add your internal domain here 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
s.trackOffline=true
*** 
```

AppMeasurement.js 파일 편집에 대한 자세한 내용은 [AppMeasurement.js 파일에코드 삽입](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html)을 참조하십시오.

AppMeasurement.js 파일의 구성 예는 [AppMeasurement.js 파일구성](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7)을 참조하십시오.

AppMeasurement.js 파일의 특징에 대한 자세한 내용은 [Javascript 구현 개요](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html)를 참조하십시오.
