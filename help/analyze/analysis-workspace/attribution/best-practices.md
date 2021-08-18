---
title: 속성 모범 사례
description: 속성 모델을 결정하는 것과 관련된 우수 사례는 무엇입니까?
source-git-commit: 3f586a6a183baf5ff388a55105886eb31fd4366a
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 2%

---


# 속성 모범 사례

조직에 대해 올바른 속성 모델을 선택하는 것은 여러 고려 사항에 따라 다릅니다. 이 문서에서는 방법론과 일반적인 모범 사례를 설명합니다.

## 1단계: 예비 분석

>[!NOTE]
>속성 모델을 선택하기 전에 이 분석을 수행해야 합니다.

이 단계는 처음에 고객 행동을 이해하고 전환 지표를 정의하는 것으로 구성됩니다. 전환 지표를 기반으로, [데이터 피드](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=en)(원시 데이터의 경우) 또는 Analysis Workspace과 같은 도구는 를 쉽게 이해할 수 있도록 합니다

* 전환하기 전에 서로 다른 마케팅 채널을 터치하는 고객은 몇 명입니까?
* 이러한 동작의 비율/분배입니다.

예를 들어 고객의 50%가 전환하기 전에 3개의 채널을 터치하는 경우 이러한 3개 채널 간에 상호 작용이 있습니까?
그런 다음 상위 및 하위 단계 분석을 수행하여 이해를 확장할 수 있습니다.

### 상위 단계 분석

상위 단계 분석은 브랜드 또는 제품 인식을 만드는 데 사용되는 채널을 분석합니다. 예를 들어, 대부분의 TV 광고의 목표는 브랜드 인식입니다. 사람들이 시간이 지남에 따라 TV 광고에 대해 잊어버리기 때문에 [&quot;시간 가치 하락&quot; 속성 모델](/help/analyze/analysis-workspace/attribution/models.md)을 사용할 수 있습니다.

### 낮은 단계 분석

이 분석에서 가정은 사람들이 이미 여러분의 브랜드에 대해 알고 있고 여러분이 그들이 전환하기를 원한다는 것입니다. 이메일 또는 푸시 알림 또는 Facebook 광고를 사용합니다.

## 2단계: 규칙 기반 속성

이 단계의 목적은 가설을 검증하는 것입니다.

**예제 1**

여러분의 가설이 &quot;첫 번째 터치 채널이 마지막 터치 채널보다 전환에 더 많은 영향을 줍니다. 그런 다음 [&quot;Inverse J자형&quot; 속성 모델](/help/analyze/analysis-workspace/attribution/models.md)을 사용하여 이 가설을 테스트합니다. 이 모델은 첫 번째 터치 포인트에 크레딧의 60%를 제공합니다.

**예제 2**

당신의 가설은 다음과 같습니다. &quot;우리 업계(예를 들어 여행 산업)에서, 고객들이 제품을 사기 전에 많은 연구를 하기 때문에 속성 기간은 30일이 아니라 60~90일입니다. 그런 다음 [전환 확인 기간](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en#lookback-windows)을 90일로 변경합니다.

## 3단계: 알고리즘 속성 사용

가능한 가설 및 조합의 수가 많기 때문에 [알고리즘 속성](/help/analyze/analysis-workspace/attribution/algorithmic.md)을 사용하여 이 작업을 기본 제공 알고리즘에 남길 수 있습니다. 모든 질문에 답변하고 완벽하게 맞는 완벽한 속성 모델을 이미 찾은 경우 이 단계를 수행할 필요가 없습니다.

## 기타 고려 사항

* Analysis Workspace에만 의존하지 않고 데이터 과학자 서비스를 사용해야 할 수도 있습니다.
* Adobe 데이터 피드에서와 같이 원시 데이터를 사용할 수 있습니다.
* 예를 들어 노출 횟수 데이터를 고려하려는 경우 [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko) 사용을 고려해 보십시오.
