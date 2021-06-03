---
title: 마케팅 채널 분석
description: Workspace에서 마케팅 채널 차원을 사용하는 방법을 알아봅니다.
exl-id: 7030e41a-4e92-45c7-9725-66a3ef019313
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 95%

---

# 마케팅 채널 분석

>[!NOTE]
>
>Attribution IQ 및 Customer Journey Analytics에 대한 마케팅 채널의 효과를 극대화하기 위해 [수정된 모범 사례](/help/components/c-marketing-channels/mchannel-best-practices.md)를 게시했습니다.

어느 마케팅 채널이 가장 효과적인지 알고 싶을 것입니다. 그러한 채널을 이용하여 노력을 향상시키고 최적의 마케팅 효과를 얻을 수 있습니다. Adobe Analytics에서는 Workspace의 마케팅 채널 차원 및 지표가 주문, 매출 등에 대한 다양한 채널의 영향을 추적하는 데 도움이 되는 도구 중 하나이며, 유용한 채널 인사이트를 제공합니다. 마케팅 채널과 관련하여 사용할 수 있는 차원 및 지표는 다음과 같습니다.

![](assets/mc-dims.png)

| 차원/지표 | 정의 |
| --- | --- |
| 마케팅 채널 | 권장 마케팅 채널 차원입니다. 런타임 시 속성 IQ 모델을 적용할 수 있습니다. 이 차원은 마지막 터치 채널 차원과 동일하게 동작하지만 다른 속성 모델과 함께 이 차원을 사용할 때 혼동을 방지하기 위해 레이블이 다르게 지정됩니다. |
| 마지막 터치 채널 | 마지막 터치 속성 모델이 사전 적용되어 변경할 수 없는 기존 차원입니다. |
| 첫 번째 터치 채널 | 첫 번째 터치 속성 모델이 사전 적용되어 변경할 수 없는 기존 차원입니다. |
| 마케팅 채널 인스턴스 | 이 지표는 표준 페이지 보기 수 및 사용자 지정 링크 호출을 포함하여 마케팅 채널이 이미지 요청에 정의된 횟수를 측정합니다. 지속되는 값을 포함하지 않습니다. |
| 새 참여 횟수 | 이 지표는 인스턴스와 유사하지만 첫 번째 접점 마케팅 채널이 이미지 요청에 정의될 때만 증가합니다. |

## 기본 분석

이 자유 형식 테이블은 각 마케팅 채널에 대한 온라인 주문, 온라인 매출 및 전환율 지표를 보여 줍니다.

![](assets/mc-viz1.png)

여기서는 도넛형 차트에 나와 있는 각 마케팅 채널의 온라인 주문 및 온라인 매출을 확인할 수 있습니다.

![](assets/mc-viz2.png)

이 선 차트는 시간에 따른 다양한 채널에 대한 온라인 주문 트렌드를 보여 줍니다.

![](assets/mc-viz3.png)

## 고급 분석

마케팅 채널 세부 정보는 각 채널을 더 깊이 있게 분석하여 특정 캠페인, 배치 등을 보여 줍니다. 각 마케팅 채널을 다음과 같이 세부적으로 분류할 수 있습니다.

![](assets/mc-viz4.png)

## 속성 모델 적용

[속성 IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution/use-attribution.html)를 사용하여 다른 속성 모델을 즉시 적용할 수 있습니다.

![](assets/mc-viz5.png)

서로 다른 속성 모델을 적용할 때 동일한 지표 (온라인 주문)가 다른 결과를 어떻게 생성하는지 확인하십시오.

## 교차 탭 마케팅 분석

기존의 첫 번째 접점 채널과 마지막 접점 채널을 사용하면 채널 상호 작용에 도움이 되는 보기를 얻을 수 있습니다.

![](assets/mc-viz6.png)

이 비디오에서 교차 탭 마케팅 분석에 대해 자세히 알아보십시오. [교차 탭 분석을 사용하여 Analysis Workspace에서의 기본 마케팅 기여도 살펴보기](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/attribution-iq/using-cross-tab-analysis-to-explore-basic-marketing-attribution-in-analysis-workspace.html).
