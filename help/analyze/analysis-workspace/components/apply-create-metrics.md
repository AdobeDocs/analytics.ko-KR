---
description: Analysis Workspace에서 지표를 사용하는 두 가지 방법이 있습니다.
title: Analysis Workspace의 지표
feature: Metrics
role: User, Admin
exl-id: 0a5dc709-c4e8-412a-a6cf-37b85d811f65
source-git-commit: e0a10540bdfbd9fa3694ff3c7a8585eeb87eaad8
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 23%

---

# 지표

지표를 사용하면 Analysis Workspace의 데이터 포인트를 수량화할 수 있습니다. 이 프로젝트들은 시각화에서 열로 일반적으로 사용되고 차원에 연결됩니다.

Adobe은 Analysis Workspace에서 사용할 몇 가지 유형의 지표를 제공합니다.

* **표준 지표**: 프로젝트에서 사용하는 대부분의 지표는 표준 지표입니다. 해당 예는 다음과 같습니다 [페이지 보기 수](/help/components/metrics/page-views.md), [매출](/help/components/metrics/revenue.md), 또는 [사용자 지정 이벤트](/help/components/metrics/custom-events.md). 자세한 내용은 [지표 개요](/help/components/metrics/overview.md) 자세한 내용은 구성 요소 사용 안내서에서 를 참조하십시오.

   ![표준 지표](assets/standard-metric.png)

* **계산된 지표**: 표준 지표, 정적 숫자 또는 알고리즘 함수를 기반으로 하는 사용자 정의 지표. 사용자 정의 계산된 지표는 사용 가능한 구성 요소 목록에 계산기 아이콘을 표시합니다. 자세한 내용은 [계산된 지표 개요](/help/components/c-calcmetrics/cm-overview.md) 자세한 내용은 구성 요소 사용 안내서에서 를 참조하십시오.

   ![계산된 지표](assets/calculated-metric.png)

* **계산된 지표 템플릿**: 계산된 지표와 유사하게 동작하는 Adobe 정의 지표. 작업 공간 프로젝트에서 그대로 사용하거나 복사본을 저장하여 해당 논리를 사용자 지정할 수 있습니다. 계산된 지표 템플릿은 사용 가능한 구성 요소 목록에 Adobe 아이콘을 표시합니다.

   ![계산된 지표 템플릿](assets/calculated-metric-template.png)

지표는 Analysis Workspace 내에서 사용할 수 있습니다. 지표를 빈 자유 형식 테이블로 끌어다 놓아 프로젝트의 날짜 기간 동안의 해당 지표 트렌드를 확인합니다. 차원이 있을 때 지표를 드래그하여 각 차원 항목과 비교하여 해당 지표를 확인할 수도 있습니다. 기존 지표 헤더 위로 지표를 드래그하면 지표가 대체되고, 헤더 옆에 지표를 드래그하면 두 지표를 나란히 볼 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/40817/?quality=12)

## 계산된 지표

계산된 지표를 사용하면 간단한 연산자 또는 통계 함수를 사용하여 지표가 어떻게 서로 관련되는지를 쉽게 볼 수 있습니다. 다음 몇 가지 방법으로 계산된 지표를 만들 수 있습니다.

* 왼쪽의 구성 요소 목록 아래에 있는 지표 헤더 옆에 있는 더하기 아이콘을 클릭합니다.
* 다음으로 이동 **[!UICONTROL 구성 요소]** > **[!UICONTROL 계산된 지표]** > **[!UICONTROL 추가]**.
* 열 헤더를 마우스 오른쪽 단추로 클릭 > **[!UICONTROL 선택 항목에서 지표 만들기]** 머리글 열 셀을 하나 이상 선택한 경우 이 옵션은 계산된 지표 규칙 빌더를 사용하지 않아도 자동으로 계산된 지표를 만듭니다.

[계산된 지표: 구현 불가 지표](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-implementationless-metrics.html?lang=ko-KR)  (3:42)

## 다양한 속성 모델과 지표 비교

하나의 속성 모델을 다른 속성 모델과 빠르고 쉽게 비교하려면 지표를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL 속성 모델 비교]**&#x200B;를 선택하십시오.

![속성 비교](assets/compare-attribution.png)

이 단축키를 사용하면 지표를 드래그하여 두 번 구성하지 않고 한 가지 속성 모델을 다른 모델과 신속하고 간편하게 비교할 수 있습니다.

## [!UICONTROL 누적 평균] 함수를 사용하여 메트릭 스무딩 적용

다음은 해당 주제에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/27068/?quality=12)
