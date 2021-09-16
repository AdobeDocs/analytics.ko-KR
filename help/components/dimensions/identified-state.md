---
title: 확인된 상태
description: Device Graph로 인식을 결정하는 플래그.
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
source-git-commit: 1a58c3e87f5918c91b891faa6027f5ad8b6024b9
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 61%

---

# 확인된 상태

&#39;확인된 상태&#39; 차원은 [교차 장치 분석](../cda/overview.md) 가상 보고서 세트와 관련이 있습니다. 히트가 보고서 실행 시 시스템에 의해 식별(결합됨)되는지 여부를 보고합니다. 이 차원은 CDA에서 데이터를 얼마나 잘 결합하는지 또는 &quot;압축&quot;하는지를 이해하는 데 도움이 됩니다.

## 이 차원을 데이터로 채우기

가상 보고서 세트에 대해 [교차 장치 분석](../cda/overview.md)이 구성되어 있으면 이 차원이 즉시 작동합니다.

## 차원 항목

차원 항목은 `"Identified"` 및 `"Unidentified"`를 포함합니다. 

* **`"Identified"`**: 히트가 사람에게 매핑됩니다.
* **`"Unidentified"`**: 히트가 사람에게 매핑되지 않으므로 속성 방법으로 매핑할 수 없습니다.
