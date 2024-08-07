---
title: 히트 유형
description: 히트가 전경 히트인지 배경 히트인지 확인합니다.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 84%

---

# 히트 유형

&#39;히트 유형&#39; [차원](overview.md)은(는) 히트가 Adobe 데이터 수집 서버로 전송될 때 모바일 앱이 전경에 있는지 배경에 있는지 여부를 결정합니다. 이 차원은 모바일 애플리케이션용 데이터가 포함된 보고서 세트에만 관련이 있습니다. AppMeasurement를 통해 수집된 브라우저 데이터는 항상 히트를 &quot;전경&quot;으로 보고합니다.

## 이 차원을 데이터로 채우기

이 차원은 버전 4.13.6 이상에서 모든 Mobile SDK 구현에 대해 즉시 작동합니다. Mobile SDK를 사용하지 않는 경우 모든 히트가 &quot;전경&quot; 차원 항목 아래에 표시됩니다. 백그라운드 히트에 대해 이전 보고 및 속성 비활성화를 선택하면 배경 히트 수는 [가상 보고서 세트](../vrs/vrs-mobile-visit-processing.md)에만 표시됩니다.

## 차원 항목

차원 항목은 `"Foreground"` 및 `"Background"`를 포함합니다. 모바일 애플리케이션 배경에서 전송되지 않은 모든 히트는 `"Foreground"` 차원 항목에 속합니다. 모바일 애플리케이션이 배경에 있었던 곳에서 전송된 모든 히트는 `"Background"` 차원 항목에 속합니다.
