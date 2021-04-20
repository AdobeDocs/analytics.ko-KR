---
title: Analytics용 PWA
description: Adobe Analytics용 PWA(Progressive Web App)
role: Business Practitioner, Administrator
exl-id: f28e0bfc-0e3e-4f28-9533-6788a36d37fe
translation-type: tm+mt
source-git-commit: 3f3a9b7f81ce671a94b7fe71c3ef7e4ae206b875
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 78%

---

# Adobe Analytics용 PWA

이 페이지는 PWA(Progressive Web App)에서 Adobe Analytics를 사용하는 방법을 설명합니다.

## 소개

PWA는 웹 사이트에 기본 앱 환경과 오프라인 기능을 제공할 수 있습니다. 일반적으로 PWA에는 빠른 로드 시간, 쉬운 탐색 및 반응 동작에 모두 도움이 되는 서비스 작업자, 캐싱 프로비전 및 매니페스트 파일이 포함되어 있습니다.

Adobe Analytics은 기존 웹 사이트와 마찬가지로 PWA과 매끄럽게 연동됩니다. PWA에는 점진적으로 스스로 동작하기 위한 몇 가지 추가 요구 사항이 있지만 Analytics가 기존 웹 사이트와 다르게 데이터를 수집하거나 보고하는 방법에 대한 장애 요소나 제한을 만들지 않습니다. 실제로 Analytics에는 이미 오프라인 추적 기능이 포함되어 있으므로 PWA는 기존의 웹 사이트보다 빌드된 이러한 기능을 보다 쉽게 활용하는 데 도움을 줄 수 있습니다.

## PWA Analytics 데이터 가져오기

[!UICONTROL Analytics]를 사용하여 PWA 데이터를 수집하고 분석하기 위해 구성을 변경할 필요가 없습니다. [!UICONTROL Analytics는 기존 웹 사이트에서와 동일한 모든 기능과 특징을 자동으로 제공합니다.]

## 오프라인 추적을 추가하여 PWA 효율성 향상

Adobe Analytics [오프라인 추적 기능](/help/implement/vars/config-vars/trackoffline.md)을 사용하여 PWA의 효율성을 높일 수 있습니다. 기본적으로 이 기능은 꺼져 있지만 다음 속성을 AppMeasurement.js 파일에 추가하여 켤 수 있습니다. `s.trackOffline=true;`

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

AppMeasurement.js 파일 편집에 대한 자세한 내용은 [핵심 AppMeasurement 코드 삽입](/help/implement/other/dtm/c-aa-tool/t-appmeasurement-code.md)을(를) 참조하십시오.

AppMeasurement.js 파일 구성에 대한 자세한 내용은 같은 하위 장의 [구성 변수 개요](/help/implement/vars/config-vars/configuration-variables.md) 및 개별 변수 관련 페이지를 참조하십시오.

AppMeasurement.js 파일의 특성에 대한 자세한 내용은 [JavaScript 구현 개요](/help/implement/js/overview.md)를 참조하십시오.
