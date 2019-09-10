---
title: PWAS for Analytics
seo-title: PWAS for Analytics
description: Adobe Analytics를 위한 점진적 웹 앱
seo-description: Analytics와 PWAS 사용
translation-type: tm+mt
source-git-commit: f64e5d9977bebd0e9db4af0f7118e9e64978c1c7

---


# PWAS for Analytics

본 가이드에서는 PWAS (Progressive Web Apps) 와 함께 Adobe Analytics를 사용하는 방법을 설명합니다.

## 소개

PWAS는 웹 사이트에 대한 기본 앱 경험과 오프라인 기능을 제공할 수 있습니다. 일반적으로 서비스 워커, 캐싱 프로비저닝 및 매니페스트 파일을 포함할 수 있으며, 이러한 모든 것이 로드 시간, 보다 쉬운 탐색 및 응답형 비헤이비어에 도움이 될 수 있습니다.

Adobe Analytics는 기존 웹 사이트에서처럼 원활하게 작동합니다. PDID는 점진적으로 점점 더 많은 요구 사항을 준수해야 하지만, Analytics는 Analytics에서 기존 웹 사이트와 다른 방식으로 데이터를 수집 또는 보고하는 방법에 대한 장벽이나 제한을 만들지 않습니다. 실제로 Analytics 에는 이미 오프라인 추적 기능이 포함되어 있으므로 PWAS를 사용하면 기존 웹 사이트보다 내장된 기능을 보다 손쉽게 활용할 수 있습니다.

## Pwa 분석 데이터 가져오기

Analytics를 사용하여 PWA 데이터를 수집하고 분석하려면 구성을 변경할 필요가 없습니다. Analytics는 기존의 웹 사이트와 동일한 기능과 기능을 모두 자동으로 제공합니다.

## 오프라인 추적을 추가하여 Pwa 효과 향상

Analytics [Offline Tracking 기능을](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/offline-tracking.html) 사용하여 PWA의 효과를 높일 수 있습니다. 기본적으로 이 기능은 비활성화되어 있지만 Appmeasurement. js 파일에 다음 속성을 추가하여 켤 수 있습니다. `s.trackOffline=true;`.

예를 들어 다음 Appmeasurement. js 파일에서 속성이 `CONFIG SECTION`다음 링크의 끝에 추가됩니다.

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


Appmeasurement. js 파일 편집에 대한 자세한 내용은 appmeasurement. js 파일에 코드 [삽입을 참조하십시오](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html).

Appmeasurement. js 파일의 구성 예는 appmeasurement. js 파일 [구성을 참조하십시오](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7).

Appmeasurement. js 파일의 특성에 대한 자세한 내용은 [Javascript 구현 개요를](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html)참조하십시오.
