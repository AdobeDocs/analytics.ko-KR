---
title: Analytics용 PWA
seo-title: Analytics용 PWA
description: Adobe Analytics용 점진적 웹 앱
seo-description: Analytics와 함께 PWA 사용
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Analytics용 PWA

이 안내서에서는 Adobe Analytics를 점진적 웹 앱(PWA)과 함께 사용하는 방법에 대해 설명합니다.

## 소개

PWA 파섹 일반적으로 PWA에는 서비스 작업자, 캐싱 규정 및 매니페스트 파일이 포함되어 있으며 이러한 모든 것이 빠른 로드 시간, 간편한 탐색 및 응답형 비헤이비어에 도움이 됩니다.

Adobe Analytics는 기존 웹 사이트에서와 마찬가지로 PWA와도 매끄럽게 연동됩니다. PWA에는 점진적 행동을 위한 몇 가지 요구 사항이 더 있지만 Analytics가 기존 웹 사이트와 다른 방식으로 데이터를 수집하거나 보고하는 방식에 대한 장벽이나 제한 사항을 만들지 않습니다. 실제로 Analytics에는 이미 오프라인 추적 기능이 포함되어 있으므로 PWA는 기존의 웹 사이트보다 이러한 내장된 기능을 보다 손쉽게 활용할 수 있도록 지원합니다.

## PWA Analytics 데이터 가져오기

Analytics를 사용하여 PWA 데이터를 수집하고 분석하려면 구성을 변경할 필요가 없습니다. Analytics는 기존 웹 사이트와 동일한 모든 기능과 기능을 자동으로 제공합니다.

## 오프라인 추적을 추가하여 PWA 효과 향상

Analytics [오프라인 추적 기능을](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/offline-tracking.html) 사용하여 PWA의 효과를 높일 수 있습니다. 기본적으로 이 기능은 꺼져 있지만 AppMeasurement.js 파일에 다음 속성을 추가하여 활성화할 수 있습니다. `s.trackOffline=true;`Adobe

예를 들어 다음 AppMeasurement.js 파일에서 속성은 `CONFIG SECTION`

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


AppMeasurement.js 파일 편집에 대한 자세한 내용은 [AppMeasurement.js 파일에](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html)코드 삽입을 참조하십시오.

AppMeasurement.js 파일의 구성 예는 [AppMeasurement.js 파일](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7)구성을 참조하십시오.

AppMeasurement.js 파일의 특성에 대한 자세한 내용은 Javascript [구현 개요를](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html)참조하십시오.
