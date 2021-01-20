---
title: 식별된 상태
description: 장치 그래프로 인식을 결정하는 플래그.
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 9%

---


# 식별된 상태

&#39;식별된 상태&#39; 차원은 [상호 장치 분석](../cda/overview.md) 가상 보고서 세트와 관련이 있습니다. 보고서 실행 시 장치 그래프에서 Experience Cloud ID가 인식되는지 보고합니다. 이 차원은 CDA 스티치 또는 &quot;압축&quot; 데이터의 품질을 이해하는 데 도움이 됩니다.

## 이 차원을 데이터로 채우기

가상 보고서 세트에 대해 [장치 간 분석](../cda/overview.md)이 구성되어 있으면 이 차원은 즉시 작동합니다.

## 차원 항목

차원 항목은 `"Identified"` 및 `"Unidentified"`를 포함합니다. 

* **`"Identified"`**:장치 그래프는 히트에 연결된 Experience Cloud ID를 인식합니다.
* **`"Unidentified"`**:장치 그래프가 Experience Cloud ID를 인식하지 못하거나 히트에 Experience Cloud ID가 없습니다.
