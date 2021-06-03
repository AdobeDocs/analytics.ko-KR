---
title: 코호트 분석이란 무엇이며 어떻게 작동합니까?
description: 코호트 분석을 통해 잠재고객에 대한 데이터를 더 깊이 파고들고 관련 집단으로 나눕니다. Analysis Workspace의 집단 분석에 대한 자세한 내용.
feature: 시각화
role: Business Practitioner, Administrator
exl-id: 6a46e76f-671e-4b1b-933a-6c2776c72d09
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 98%

---

# Adobe Analytics의 [!UICONTROL 코호트 분석]에 대해 알아보기

*`cohort`*&#x200B;는 지정된 기간 동안 공통적인 특성을 공유하는 사람들의 그룹입니다. [!UICONTROL 집단 분석은 예를 들어 집단이 브랜드에 어떻게 참여하는지를 알려고 할 때 유용합니다.] 트렌드 변경 사항을 쉽게 찾아 응답할 수 있습니다.  ([!UICONTROL 집단 분석]에 대한 설명은 [집단 분석 101](https://ko.wikipedia.org/wiki/Cohort_analysis)에서와 같이 웹에서 사용할 수 있습니다.)

집단 보고서를 만들면 그 구성 요소 (특정 차원, 지표 및 세그먼트)를 조정한 다음, 모든 사람과 집단 보고서를 공유할 수 있습니다. [큐레이션 및 공유](/help/analyze/analysis-workspace/curate-share/curate.md)를 참조하십시오.

[!UICONTROL 집단 분석]으로 수행할 수 있는 작업의 예:

* 원하는 작업에 박차를 가할 수 있도록 설계된 캠페인 시작.
* 고객 라이프사이클에서 적시에 마케팅 예산 전환.
* 평가판이나 오퍼를 종료하여 가치를 극대화할 시점 인식.
* 가격 책정, 업그레이드 경로 등과 같은 분야에서 A/B 테스트를 하기 위한 아이디어 얻기.
* 안내가 있는 분석 보고서 내에서 [!UICONTROL 집단 분석] 보고서 보기.

[!UICONTROL 집단 분석]은 [!UICONTROL Analysis Workspace]에 대한 액세스 권한이 있는 모든 Adobe Analytics 고객에 대해 사용할 수 있습니다.

[코호트 분석 비디오 튜토리얼](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/cohort-analysis-workspace.html)  (4:36)

>[!IMPORTANT]
>
>[!UICONTROL 집단 분석]
>
>세그먼트화할 수 없는 지표 (계산된 지표 포함), 정수가 아닌 지표 (매출액 등) 또는 발생을 지원하지 않습니다. 세그먼트에서 사용할 수 있는 지표만
>[!UICONTROL 집단 분석], 한 번에 1씩만 증분할 수 있습니다.

## 집단 분석 기능

다음 기능을 통해 생성 중인 집단에 대해 세밀하게 제어할 수 있습니다.

### [!UICONTROL 유지 테이블]

[!UICONTROL 유지 ]집단 보고서는 방문자 수를 반환합니다. 각 데이터 셀에는 해당 기간 동안 작업을 수행한 집단에 있는 방문자들의 원시 수와 백분율 보여 줍니다. 최대 3개의 지표와 10개의 세그먼트를 포함할 수 있습니다.

![](assets/retention-report.png)

### [!UICONTROL 이탈 테이블]

[!UICONTROL 이탈 ]집단은 유지 테이블의 역버전이며 시간 경과에 따라 집단에 대한 반환 기준을 충족하지 않은 방문자를 표시합니다. 최대 3개의 지표와 10개의 세그먼트를 포함할 수 있습니다.

![](assets/churn-report.png)

### [!UICONTROL 순환 계산]

포함된 열이 아니라 이전 열에 따라 유지 또는 이탈을 계산할 수 있습니다.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL 지연 테이블]

포함 이벤트가 발생한 이전 및 이후에 경과한 시간을 측정합니다. 이것은 이전/이후 분석을 위한 훌륭한 도구입니다. **[!UICONTROL 포함]** 열은 테이블의 중앙에 있으며 포함 이벤트 전후의 기간이 양쪽에 표시됩니다.

![](assets/cohort-latency.png)

### [!UICONTROL 사용자 지정 차원 집단]

기본값인 시간 기반 집단이 아닌 선택된 차원에 따라 집단을 생성합니다. [!UICONTROL 마케팅·채널],·[!UICONTROL 캠페인],·[!UICONTROL 제품],·[!UICONTROL 페이지],·[!UICONTROL 영역]·또는·Adobe·Analytics의·다른·차원과·같은·차원을·사용하여·차원의·다양한·값을·기준으로·유지·변경·방법을·보여·줍니다.￼

![](assets/cohort-customizable-cohort-row.png)

집단 보고서를 설정하고 실행하는 방법에 대한 지침은 [집단 분석 보고서 구성](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md)에서 확인할 수 있습니다.
