---
title: 단일 페이지 방문 횟수
description: 방문에서 '페이지' 차원 항목이 변경되지 않은 횟수입니다.
feature: Metrics
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 100%

---

# 단일 페이지 방문 횟수

*이 도움말 페이지에서는 &#39;단일 페이지 방문 횟수&#39;가 지표로 작동하는 방식을 설명합니다. 자세한 내용은 [단일 페이지 방문 횟수](../dimensions/single-page-visits.md) 차원을 참조하십시오.*

[!UICONTROL 단일 페이지 방문] 지표는 [페이지](../dimensions/page.md) 차원 항목이 전체 방문에 대해 단일의 고유 값만 포함한 방문 수를 표시합니다. 이 지표는 짧은 방문을 보고 싶지만 [[!UICONTROL 바운스]](bounces.md)만큼 엄격한 규칙이 없는 차원의 컨텍스트에서 유용합니다.

## 이 지표의 계산 방법

이 지표는 [!UICONTROL 페이지] 차원 항목이 전체 방문에 대해 단일의 고유 값만 포함한 방문 수를 계산합니다. 방문자가 페이지를 다시 로드하거나 링크 추적 호출을 실행하는 경우에도 여전히 단일 페이지 방문으로 계산됩니다. 페이지 차원이 두 번째 고유 값으로 바뀌자마자 이 방문은 더 이상 단일 페이지 방문으로 분류되지 않습니다.

지표 간의 비교에 대해서는 [단일 액세스](single-access.md)를 참조하십시오.

## 반복 인스턴스 계산

이 설정은 보고서에서 반복 인스턴스가 계산되는지 여부를 지정합니다. 자세한 내용은 [반복 인스턴스 계산](/help/components/metrics/count-repeat-instances.md)을 참조하십시오.