---
title: 확인된 상태
description: Device Graph로 인식을 결정하는 플래그.
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '120'
ht-degree: 100%

---

# 확인된 상태

&#39;확인된 상태&#39; 차원은 [교차 장치 분석](../cda/overview.md) 가상 보고서 세트와 관련이 있습니다. 보고서 실행 시 Device Graph에서 Experience Cloud ID가 인식되는지 보고합니다. 이 차원은 CDA에서 데이터를 얼마나 잘 결합하는지 또는 &quot;압축&quot;하는지를 이해하는 데 도움이 됩니다.

## 이 차원을 데이터로 채우기

가상 보고서 세트에 대해 [교차 장치 분석](../cda/overview.md)이 구성되어 있으면 이 차원이 즉시 작동합니다.

## 차원 항목

차원 항목은 `"Identified"` 및 `"Unidentified"`를 포함합니다. 

* **`"Identified"`**: Device Graph에서 히트에 연결된 Experience Cloud ID를 인식합니다.
* **`"Unidentified"`**: Device Graph에서 Experience Cloud ID를 인식하지 못하거나 히트에 Experience Cloud ID가 없습니다.
