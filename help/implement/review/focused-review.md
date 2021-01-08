---
title: 집중 검토(각 웹 사이트 릴리스 이후)
description: 다음 단계에 따라 구현 시 오류가 발생하지 않고 KPI에 맞게 유지되도록 하십시오.
translation-type: tm+mt
source-git-commit: a7f1da79bd5a6f78ed1a706ccae01b03a2f5665c
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---


# 집중 검토(각 웹 사이트 릴리스 이후)

왜 몇 개월마다 구현을 검토해야 합니까? 데이터 품질은 작지만 모든 문제를 해결할 수 있습니다. 각 웹 사이트 릴리스 후에 이 집중 검토를 일관되게 수행하는 경우, 2년 과정의 [전체 검토](/help/implement/review/full-review.md)가 훨씬 더 수월합니다. 또한 사소한 문제가 이해 관계자의 신뢰를 손상시킬 수 있는 빅데이터 문제로 번지지 않도록 방지할 수 있습니다.

## 1. 상위 5개의 KPI로 시작합니다.

상위 5개의 주요 성과 지표(KPI)를 파악하면 검토해야 하는 관련 지표와 차원을 결정하는 데 도움이 됩니다. 지난 6개월 동안 KPI를 새로 고치지 않았거나 사업이 아직 KPI를 만들지 않은 경우에는 [다음 지침](/help/implement/review/define-kpis.md)을 따릅니다.

## 2. KPI 지표와 변수가 여전히 제대로 작동하는지 확인합니다.

시간의 경과에 따른 코드 업데이트는 의도하지 않은 결과를 초래할 수 있습니다. 상위 5개의 KPI[에 연결된 모든 지표 및 차원이 여전히 제대로 작동하는지 확인해야 합니다. ](/help/implement/review/define-kpis.md) 가장 좋은 방법은 웹 사이트 릴리스 직후 수행하는 것입니다.지난 몇 달 동안 작업을 수행하지 않았다면 *지금*&#x200B;하십시오. 이렇게 하려면:

* **대시보드** 를 만들어 이러한 중요한 지표 및 변수의 시간별 트렌드 보기를 확인합니다. 각 지표에 대한 지능형 경고를 설정하고 하루 또는 이틀 동안 모니터링하여 예상한 데이터를 얻고 데이터가 올바른지 확인할 수 있습니다. 변곡점을 찾습니다. 모든 중요한 문제를 즉시 해결할 준비를 하세요. 불일치가 발견되면 데이터 레이어, 태그 관리자 규칙 및 처리 규칙을 검색하여 그 이유를 확인하십시오.
* **Analytics 상태 대시보드를** 다시 실행하여 KPI 지표 및 변수의 광범위한 트렌드를 모니터링할 수 있습니다.

지표와 변수가 제대로 작동하는지 확인하는 방법에 대한 자세한 내용은 Adobe Analytics Champion Sarah Owen이 제공하는 [다음 팁](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608)을 참조하십시오.

## 3. 사이트의 업데이트된 섹션에서 데이터를 철저히 검사합니다.

가장 최근의 사이트 릴리스가 사이트의 해당 섹션에 대한 데이터 수집에 부정적인 영향을 주지 않는지 확인합니다.해당 섹션에 해당하는 모든 코드와 변수를 검토하여 새 추적이 설계된 대로 작동하는지 확인합니다.

## 4. 설명서를 업데이트합니다.

최근 지표나 변수를 추가하거나 변경한 경우 BRD(Business Requirements Document) 및 SDR(Solution Design Reference)을 업데이트해야 합니다.

구현 설명서가 없는 경우 변수 목록을 내보내고 [이 템플릿](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=en#implementation)을 사용하여 BRD 또는 SDR을 만듭니다.

## 5. 데이터 품질에서 발견되는 차이를 즉시 해결합니다.

상황을 평가하고 데이터를 수정할 계획을 세우시오. 필요한 사항을 변경하고 설명서를 업데이트한 다음 이해 관계자에게 변경 내용을 알립니다.

*Adobe Analytics 챔피언 사라 오웬이 바쁜 일정에 따른 검토 작업에 시간을 맞출 수 있는 시간을 소개합니다.*

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
