---
title: 집중 검토 (각 웹 사이트 릴리스 이후)
description: 다음 단계에 따라 구현 오류를 방지하고 KPI를 관리하십시오.
exl-id: e38f92b6-bd6e-4835-a8e5-0f29ac962066
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '514'
ht-degree: 100%

---

# 집중 검토 (각 웹 사이트 릴리스 이후)

몇 개월마다 구현을 검토해야 하는 이유는 무엇입니까? 문제가 커지기 전에 데이터 품질 문제를 해결할 수 있습니다. 각 웹 사이트 릴리스 후에 이 집중 검토를 정기적으로 수행하면, 2년 마다 수행되는 [전체 검토](/help/implement/review/full-review.md)가 훨씬 더 수월해집니다. 또한 사소한 문제가 이해 관계자의 신뢰를 손상시킬 수 있는 대규모 데이터 문제로 번지지 않도록 방지할 수 있습니다.

## 1. 상위 5개의 KPI로 시작합니다.

상위 5개의 주요 성과 지표 (KPI)를 파악하면 검토해야 하는 관련 지표와 차원을 결정하는 데 도움이 됩니다. 지난 6개월 동안 KPI를 새로 고치지 않았거나 아직 회사의 KPI를 만들지 않은 경우에는 [다음 지침](/help/implement/review/define-kpis.md)을 따릅니다.

## 2. KPI 지표와 변수가 계속 제대로 작동하는지 확인합니다.

시간의 경과에 따라 코드를 업데이트하면 의도하지 않은 결과를 초래할 수 있습니다. [상위 5개의 KPI](/help/implement/review/define-kpis.md)에 연결된 모든 지표 및 차원이 계속 제대로 작동하는지 확인해야 합니다. 가장 좋은 방법은 웹 사이트 릴리스 직후 수행하는 것입니다. 지난 몇 달 동안 작업을 수행하지 않았다면 *지금*&#x200B;하십시오. 다음을 수행하십시오.

* 대시보드를 만들어서 이러한 중요한 지표 및 변수의 시간별 트렌드 보기를 보거나 각 지표에 대한 [지능형 경고](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html#analysis-workspace)를 설정합니다. 하루나 이틀 동안 모니터링하여 원하는 데이터를 얻을 수 있는지 데이터가 정확한지 확인합니다. 변곡점을 찾습니다. 중요한 문제를 즉시 해결할 준비를 하십시오. 불일치가 발견되면 데이터 레이어, 태그 관리자 규칙 및 처리 규칙을 검색하여 그 이유를 확인하십시오.
* [Analytics 상태 대시보드](https://assets.adobe.com/public/9549dbe7-765a-4899-77b8-85cbba1a4252)를 다시 실행하여 광범위한 KPI 지표 및 변수 트렌드를 모니터링합니다.

*지표와 변수가 제대로 작동하는지 확인하는 방법에 대한 자세한 내용은 Adobe Analytics 챔피언 사라 오웬의 [팁을 참조](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608)하십시오.*

## 3. 사이트의 업데이트된 섹션에서 데이터를 철저히 검사합니다.

가장 최근의 사이트 릴리스가 사이트의 해당 섹션에 대한 데이터 수집에 부정적인 영향을 주지 않는지 확인합니다. 해당 섹션에 해당하는 모든 코드와 변수를 검토하여 새 추적이 설계된 대로 작동하는지 확인합니다.

## 4. 설명서를 업데이트합니다.

최근 지표나 변수를 추가하거나 변경한 경우 BRD (Business Requirements Document) 및 SDR (Solution Design Reference)을 업데이트해야 합니다.

구현 설명서가 없는 경우 변수 목록을 내보내고 [이 템플릿](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=ko-KR#implementation)을 사용하여 BRD 또는 SDR을 만듭니다.

## 5. 데이터 품질에서 발견되는 차이를 즉시 해결합니다.

상황을 평가하고 데이터를 수정할 계획을 세웁니다. 필요한 사항을 변경하고 설명서를 업데이트한 다음 이해 당사자에게 변경 내용을 알립니다.

*바쁜 일정에 맞게 구현을 검토할 수 있는 자연스러운 시간에 관하여 Adobe Analytics 챔피언 사라 오웬이 제공한 2분 비디오를 감상하십시오.*

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
