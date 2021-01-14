---
title: 전체 검토
description: 6개월마다 구현을 검토하여 비즈니스 요구 사항과 KPI에 맞게 계속 조정할 수 있습니다.
translation-type: tm+mt
source-git-commit: ad7274dbed3b85ca24cd92bf3a0d36d1f2e3597b
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 89%

---


# 전체 검토(2년마다 구현 검토)

6개월마다 구현을 검토해야 하는 이유는 무엇입니까? 비즈니스 요구 사항에 맞게 구현하고 있는지 확인해야 하기 때문입니다. 이해 관계자의 신뢰도를 손상시킬 수 있는 주요 데이터 문제로 확대되기 전에 규모가 작은 데이터 품질 문제를 해결하려는 경우도 있습니다. 6개월마다 수행하는 전체 검토 외에도 각 웹 사이트 릴리스 이후 [집중 검토](/help/implement/review/focused-review.md)도 수행해야 합니다.

## 1. 구현이 비즈니스 요구 사항에 부합하는지 확인합니다.

변화하는 비즈니스 요구 사항을 검토하려면 비즈니스 소유자 및/또는 분석가와 만나보십시오. 구현에서 현재 충족되지 않는 요구 사항이나 측정 기회에 대해 KPI 및 측정 계획을 업데이트하는 방법을 알아봅니다. [BRD 및 SDR](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=ko-kr#implementation)에 변경 내용을 기록해야 합니다.

## 2. 지표 및 변수가 계속 제대로 작동하는지 확인합니다.

비즈니스에 중요한 순서대로 모든 지표와 변수를 간단히 검토하여 데이터가 올바르게 수집되는지 확인합니다. 가장 중요한 지표 및 변수([상위 5개의 KPI](https://experienceleague.adobe.com/docs/analytics/implementation/review/define-kpis.html?lang=ko-kr#review)와 연관된 지표 및 변수)로 시작합니다. 다음을 수행하십시오.

* 대시보드를 만들어 지표와 변수의 월별 트렌드 보기를 보거나 각 지표와 변수에 대해 [지능형 경고](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html#analysis-workspace)를 설정합니다. 이렇게 하면 원하는 데이터가 올바르게 입력되고 있는지 확인할 수 있습니다. 불일치가 발견되면 데이터 레이어, 태그 관리자 규칙 및 처리 규칙을 검토하여 그 이유를 확인하십시오.
* 지표 및 변수의 광범위한 트렌드를 모니터링하려면 [Analytics 상태 대시보드](https://assets.adobe.com/public/9549dbe7-765a-4899-77b8-85cbba1a4252)를 다시 실행하십시오.

필요하지 않은 지표 및 변수로 구현을 활성화하지 마십시오. 비즈니스에 더 이상 필요하지 않거나 사용하지 않는 지표 또는 변수를 비활성화합니다. 삭제하거나 나중에 재사용할 수 있습니다.

## 3. KPI를 새로 고칩니다.

비즈니스 목표에 대한 보기가 갱신되었으므로 5개의 *가장* 중요한 KPI(Key Performance Indicator)를 실제로 선택했는지 다시 평가합니다. 5개만 사용할 수 있습니다. 이러한 KPI는 매출과 같은 지표나 방문당 매출과 같은 계산된 지표가 될 수 있으며 지표에도 변수가 있을 수 있습니다. 자세한 내용은 [상위 5개 KPI 정의](/help/implement/review/define-kpis.md)를 참조하십시오.
