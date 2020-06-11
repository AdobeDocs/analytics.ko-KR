---
title: 히트 유형
description: 히트가 전경 또는 배경 히트인지 확인합니다.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# 히트 유형

&#39;히트 유형&#39; 차원은 히트를 Adobe 데이터 수집 서버로 보낼 때 모바일 앱이 전경 또는 배경에 있는지 여부를 결정합니다. 이 차원은 모바일 응용 프로그램용 데이터가 포함된 보고서 세트에만 관련이 있습니다. AppMeasurement를 통해 수집된 브라우저 데이터는 항상 히트를 &quot;전경&quot;으로 보고합니다.

## 데이터로 이 차원 채우기

이 차원은 버전 4.13.6 이상에서 모든 모바일 SDK 구현에 적합합니다. 모바일 SDK를 사용하지 않는 경우 &quot;전경&quot; 차원 값 아래의 모든 히트 목록이 표시됩니다. If &quot;Disable Legacy Reporting and Attribution for Background Hits&quot; is checked, then background hits will show up only in [Virtual report suites](../vrs/vrs-mobile-visit-processing.md).

## 차원 값

차원 값은 `"Foreground"` 및 `"Background"`를 포함합니다. 모바일 응용 프로그램 백그라운드에서 전송되지 않은 모든 히트는 `"Foreground"` 차원 값에 속합니다. 모바일 애플리케이션이 백그라운드에 있었던 곳에서 전송된 모든 히트는 `"Background"` 차원 값에 속합니다.
