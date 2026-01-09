---
title: 확인된 상태
description: 결합에 대한 인식을 결정하는 플래그.
feature: Dimensions
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
source-git-commit: f75a1f6d9f08f422595c24760796abf0f8332ddb
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 83%

---

# 확인된 상태

&#39;확인된 상태&#39; [차원](overview.md)은(는) [크로스 디바이스 분석](../cda/overview.md)가상 보고서 세트와 관련이 있습니다. 보고서 실행 시 시스템에 의해 히트가 확인(결합)되거나 확인되지 않는 경우 이를 보고합니다. 이 차원은 CDA에서 데이터를 얼마나 잘 결합하는지 또는 &quot;압축&quot;하는지를 이해하는 데 도움이 됩니다.

## 이 차원을 데이터로 채우기

가상 보고서 세트에 대해 [크로스 디바이스 분석](../cda/overview.md)이 구성되어 있으면 이 차원이 즉시 작동합니다.

## 차원 항목

차원 항목은 `"Identified"` 및 `"Unidentified"`를 포함합니다.

* **`"Identified"`**: 히트는 사용자에게 매핑됩니다.
* **`"Unidentified"`**: 히트는 사용자에게 매핑되지 않고 모든 기여도 방법에도 매핑될 수 없습니다.
