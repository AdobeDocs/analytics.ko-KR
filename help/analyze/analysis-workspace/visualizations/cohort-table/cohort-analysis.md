---
keywords: Analysis Workspace
title: 집단 분석이란?
topic: Reports and analytics
uuid: 39a83f3a-15d1-41d7-bcdd-50c22aed8f1c
translation-type: tm+mt
source-git-commit: 99232c5bce94cfc55b9f01080555cb8e545442e9

---


# 집단 분석이란?

*`cohort`*&#x200B;은 지정된 기간 동안 공통적인 특성을 공유하는 사람들의 그룹입니다. 집단 분석은 예를 들어 집단이 브랜드에 어떻게 참여하는지를 알려고 할 때 유용합니다. 트렌드 변경 사항을 쉽게 찾아 응답할 수 있습니다. (집단 분석에 대한 설명은 [집단 분석 101](https://en.wikipedia.org/wiki/Cohort_analysis)에서와 같이 웹에서 사용할 수 있습니다.)

집단 보고서를 만들면 그 구성 요소(특정 차원, 지표 및 세그먼트)를 조정한 다음, 모든 사람과 집단 보고서를 공유할 수 있습니다. [큐레이션 및 공유](/help/analyze/analysis-workspace/curate-share/curate.md)를 참조하십시오.

집단 분석으로 수행할 수 있는 작업의 예:

* 원하는 작업에 박차를 가할 수 있도록 설계된 캠페인 시작.
* 고객 라이프사이클에서 적시에 마케팅 예산 전환.
* 평가판이나 오퍼를 종료하여 가치를 극대화할 시점 인식.
* 가격 책정, 업그레이드 경로 등과 같은 분야에서 A/B 테스트를 하기 위한 아이디어 얻기.
* 안내가 있는 분석 보고서 내에서 집단 분석 보고서 보기.

집단 분석은 Analysis Workspace에 대한 액세스 권한이 있는 모든 Analytics 고객에 대해 사용할 수 있습니다.

[집단 분석 - YouTube](https://www.youtube.com/watch?v=kqOIYrvV-co&amp;index=45&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS)(4:36)

>[!IMPORTANT]
>
>집단 분석은 계산된 지표를 지원하지 않습니다.

## 집단 분석 기능

2019년 1월 Adobe는 새롭고 크게 향상된 집단 분석 버전을 발표했습니다. 이 버전은 사용자가 구축하는 집단에 대한 미세한 조정이 가능합니다. 다음과 같은 향상된 기능을 제공합니다.

### 유지 테이블

유지 집단 보고서는 방문자 수를 반환합니다. 각 데이터 셀에는 해당 기간 동안 작업을 수행한 집단에 있는 방문자들의 원시 수와 백분율 보여줍니다. 최대 3개의 지표와 10개의 세그먼트를 포함할 수 있습니다.

![](assets/retention-report.png)

### 이탈 테이블

이탈 집단은 유지 테이블의 역버전이며 시간 경과에 따라 집단에 대한 반환 기준을 충족하지 않은 방문자를 표시합니다. 최대 3개의 지표와 10개의 세그먼트를 포함할 수 있습니다.

![](assets/churn-report.png)

### 순환 계산

포함된 열이 아니라 이전 열에 따라 유지 또는 이탈을 계산할 수 있습니다.

![](assets/cohort-rolling-calculation.png)

### 지연 테이블

포함 이벤트가 발생한 이전 및 이후에 경과한 시간을 측정합니다. 이것은 이전/이후 분석을 위한 훌륭한 도구입니다. &quot;포함&quot; 열은 테이블의 중앙에 있으며 포함 이벤트 전후의 기간이 양쪽에 표시됩니다.

![](assets/cohort-latency.png)

### 사용자 지정 차원 집단

기본값인 시간 기반 집단이 아닌 선택된 차원에 따라 집단을 생성합니다. 마케팅 채널, 캠페인, 제품, 페이지, 영역 또는 Adobe Analytics의 다른 차원과 같은 차원을 사용하여 차원의 다양한 값을 기준으로 유지 변경 방법을 보여 줍니다.

![](assets/cohort-customizable-cohort-row.png)

집단 보고서를 설정하고 실행하는 방법에 대한 지침을 확인하려면 [집단 분석 보고서 구성](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

