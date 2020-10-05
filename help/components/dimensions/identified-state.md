---
title: 식별된 상태
description: 장치 그래프에 의한 인식을 결정하는 플래그.
translation-type: tm+mt
source-git-commit: 60fe85adaebee8ca390e59727dda949c12c1ee26
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---


# 식별된 상태

&#39;식별된 상태&#39; 차원은 [장치 간 분석](../cda/overview.md) 가상 보고서 세트에만 적용됩니다. 보고서 실행 시 장치 그래프에서 Experience Cloud ID가 인식되는지 보고합니다. 이 차원은 CDA 스티치 또는 &quot;압축&quot; 데이터의 품질을 이해하는 데 도움이 됩니다.

## 이 차원을 데이터로 채우기

가상 보고서 세트에 대해 [장치 간](../cda/overview.md) 분석을 구성한 경우 이 차원은 기본적으로 작동합니다.

## Dimension 항목

Dimension 항목에는 `"Identified"` and가 포함됩니다 `"Unidentified"`.

* **`"Identified"`**:장치 그래프는 히트에 연결된 Experience Cloud ID를 인식합니다.
* **`"Unidentified"`**:장치 그래프가 Experience Cloud ID를 인식하지 못하거나 히트에 Experience Cloud ID가 없습니다.
