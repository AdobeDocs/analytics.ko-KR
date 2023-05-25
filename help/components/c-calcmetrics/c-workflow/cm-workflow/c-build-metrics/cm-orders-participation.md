---
description: 주문을 지원하는 마케팅 채널을 보여 주는 지표를 작성하는 방법에 대해 설명합니다. 이는 원하는 모든 차원 또는 성공 이벤트에 적용할 수 있습니다.
title: 지원 지표 주문
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: 4bf8397ee979614539baf21b36363eb03357567a
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 57%

---

# 지원 주문 지표 작성

다음 정보는 주문 유도 활동에 도움이 되는 마케팅 채널을 보여 주는 지표를 만드는 방법을 설명합니다. 이는 원하는 모든 차원 또는 성공 이벤트에 적용할 수 있습니다.

1. 에 설명된 대로 계산된 지표 만들기를 시작합니다. [지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).

1. 계산된 지표 빌더에서 지표의 이름을 &quot;지원 주문&quot;으로 지정합니다.

1. 정의 캔버스에서 주문 지표를 드래그합니다. 그런 다음 **[!UICONTROL 기본이 아닌 기여도 분석 모델]** 확인란을 선택하여 설정 기어를 통해 기여도 분석 모델을 조정합니다.

   ![](assets/attr-model.png)

1. **[!UICONTROL 사용자 지정]**&#x200B;을 기여도 분석 모델로 선택합니다. 가중치를 0 (시작), 100 (중간), 0 (종료)으로 변경합니다.

   ![](assets/custom-attr-model.png)

1. 선택 [!UICONTROL **적용**] > [!UICONTROL **저장**].

1. Analysis Workspace에서 마케팅 채널 차원, 주문 및 새로운 지원 주문 지표를 사용하여 자유 형식 테이블을 만듭니다.

   ![](assets/mktg-channel-assists.png)

   이는 마케팅 채널에서 주문을 지원하는 방법을 쉽게 구분하는 방법입니다. 또는 자유 형식 테이블에서 임의의 지표를 마우스 오른쪽 단추로 클릭하고 테이블에서 직접 속성 모델을 조정할 수 있습니다.

1. (선택 사항) 의 설명에 따라 조직의 다른 사용자와 지표를 공유합니다 [계산된 지표 공유](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md).
