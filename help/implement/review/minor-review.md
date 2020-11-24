---
title: 간단한 구현 검토(각 웹 사이트 릴리스 이후)
description: 다음 단계에 따라 구현 시 오류가 발생하지 않고 KPI와 일치하는지 확인합니다.
translation-type: tm+mt
source-git-commit: 82064e267729b6995402bd122c6f71b3d38967a3
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# 간단한 구현 검토(각 웹 사이트 릴리스 이후)

각 웹 사이트 릴리스 이후 구현을 검토해야 하는 이유는 무엇입니까? 따라서 코드 업데이트가 의도하지 않은 영향을 미치지 않도록 해야 하며 데이터 품질 관련 문제를 해결해야 합니다. 각 웹 사이트 릴리스 이후 이 마이너 리뷰를 일관성 있게 수행하면 [주요 리뷰](/help/implement/review/major-review.md) (6개월마다)가 훨씬 수월합니다. 또한 작은 문제가 이해 관계자의 신뢰를 손상시킬 수 있는 빅데이터 문제로 번지는 것을 방지할 수 있습니다.

## 1. 릴리스는 사이트의 해당 섹션에 대한 데이터에 어떤 영향을 줍니까?

철저한 단위 테스트:방금 업데이트한 사이트의 섹션에 해당하는 모든 코드와 변수를 검토하여 새 추적이 설계된 대로 작동하는지 확인합니다.

## 2. 설명서를 업데이트합니다.

론치를 수용하기 위해 추가/변경한 변수로 BRD(Business Requirements Document) 및 SDR(Solution Design Reference)을 업데이트합니다.

구현에 대한 문서가 없는 경우 변수 목록을 내보내고 [이 템플릿을 사용하여 BRD 또는 SDR을 만듭니다](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=en#implementation).

## 3. 상위 5개의 KPI로 시작

상위 5개의 주요 성과 지표(KPI)를 파악하면 검토해야 하는 관련 지표와 차원을 결정하는 데 도움이 됩니다. 지난 6개월 동안 KPI를 새로 고치지 않았거나 비즈니스에 KPI가 아직 만들어지지 않았으면 [다음 지침을 따르십시오](/help/implement/review/define-kpis.md).

## 4. 모든 KPI 지표와 변수가 릴리스 후에도 제대로 작동합니까?

모든 코드 업데이트는 의도하지 않은 결과를 초래할 수 있습니다. 상위 5개의 KPI와 연관된 모든 지표 및 차원 [이](/help/implement/review/define-kpis.md) 여전히 제대로 작동하는지 확인하려고 합니다. 이렇게 하려면:

* **이러한 중요한 지표 및 변수의 시간별 트렌드 보기를 표시하는 대시보드** 만들기각 지표에 대한 지능형 경고를 설정하고 하루 또는 2일 후 릴리스 후 동안 모니터링하여 예상한 데이터를 얻고 데이터가 올바른지 확인할 수 있습니다. 변곡점을 찾습니다. 모든 중요한 문제를 즉시 해결할 준비를 하세요. 올바르게 보이지 않는 불일치가 있는 경우 데이터 레이어, 태그 관리자 규칙 및 처리 규칙을 확인하여 그 이유를 확인하십시오.
* **Analytics 상태 대시보드를** 다시 실행하여 KPI 지표 및 변수의 광범위한 트렌드를 모니터링합니다.
지표와 변수가 제대로 작동하는지 확인하는 방법에 대한 자세한 내용은 Adobe Analytics 챔피언 사라 오언의 팁을 참조하십시오.

## 5. 데이터 품질에 차이가 있습니까?

상황을 평가하고 데이터를 수정할 계획을 세우세요. 그런 다음 필요한 사항을 변경하고 설명서를 업데이트하여 이해 관계자에게 변경 내용을 알립니다.

Adobe Analytics 챔피언 사라 오웬이 제작한 이 비디오를 통해 자신의 업무 일정에 대한 검토 작업을 맞출 수 있는 시간을 자연스러운 타이밍에 대해 살펴볼 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
