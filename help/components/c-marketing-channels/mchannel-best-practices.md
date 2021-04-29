---
title: Adobe Analytics 마케팅 채널 구현을 위한 모범 사례
description: Attribution IQ 및 Customer Journey Analytics에서 마케팅 채널 사용에 대한 우수 사례를 업데이트했습니다.
translation-type: tm+mt
source-git-commit: 402546c3110e78240e9379ea28957b070f22e697
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 3%

---


# 마케팅 채널의 Attribution IQ - 우수 사례

[마케팅 ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) 채널은 Adobe Analytics의 귀중하고 강력한 기능입니다. 마케팅 채널 구현에 대한 현재 지침은 [Attribution IQ](https://experienceleague.corp.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=en#analysis-workspace) 및 [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=ko-KR#cja-usecases)이(가) 존재하지 않았을 때 작성되었습니다.

향후 마케팅 채널 구현을 보호하고 Attribution IQ 및 Customer Journey Analytics과 일관성을 보고하기 위해 업데이트된 모범 사례를 제공합니다. 이미 마케팅 채널을 사용하고 있는 경우 이러한 새 지침 중 최상의 옵션을 선택할 수 있습니다. 마케팅 채널을 처음 사용하는 경우 모든 새로운 우수 사례를 준수할 것을 권장합니다.

마케팅 채널이 처음 소개되었을 때 첫 번째 접촉 및 마지막 접촉 차원에서만 제공되었습니다. 현재 버전의 속성을 사용할 경우 명확한 첫 번째/마지막 접촉 차원이 더 이상 필요하지 않습니다. Adobe은 원하는 속성 모델에서 사용할 수 있도록 일반 &#39;마케팅 채널&#39; 및 &#39;마케팅 채널 세부 사항&#39; 차원을 제공합니다. 이러한 일반 차원은 마지막 접촉 채널 크기와 동일하게 동작하지만 다른 속성 모델과 함께 마케팅 채널을 사용할 때 혼동을 방지하기 위해 다르게 레이블이 지정됩니다.

마케팅 채널 차원은 기존 방문 정의(처리 규칙으로 정의됨)에 따라 다르므로 가상 보고서 세트를 사용하여 방문 정의를 변경할 수 없습니다. 이러한 개정된 관행을 통해 Attribution IQ 및 CJA를 통해 명확한 확인 창을 확인할 수 있습니다.

## 모범 사례 #1:제어된 분석을 위한 Attribution IQ 활용

마케팅 채널 분석을 세부적으로 조정하려면 기존 마케팅 채널 속성 대신 [Attribution IQ](https://experienceleague.corp.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=en#analysis-workspace)을 사용하는 것이 좋습니다. 다른 모범 사례를 따라 Attribution IQ을 통해 분석에 대한 일관성과 강력한 제어를 보장합니다.

![](assets/attribution.png)

* 마케팅 채널 및 마케팅 채널 세부 사항의 구성은 각 마케팅 채널 인스턴스에 따라 평가할 터치포인트를 설정합니다.
* 지표 분석을 위해 조직에서 하나 이상의 속성 모델을 기준으로 정렬해야 합니다.이 모델을 사용하여 사용자 지정 지표를 저장하여 재사용할 수 있습니다.
* 기본적으로 데이터는 마지막 터치 및 방문자 참여 기간 설정을 사용하여 할당됩니다. Attribution IQ 지표 모델은 룩백 창과 [algorithmic attribution](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/algorithmic.html?lang=en#analysis-workspace)을(를) 비롯한 다양한 항목을 보다 효과적으로 제어합니다.

## 모범 사례 #2:직접 및 세션 새로 고침 채널 정의 없음

직접 및 내부/세션 새로 고침 채널은 사용자 지정 속성 모델(Attribution IQ)에서 사용하는 경우에는 권장되지 않습니다.

조직에서 직접 및 세션 새로 고침을 이미 구성한 경우 어떻게 합니까? 이 경우 마케팅 채널에 대한 분류를 만들고 이 두 채널을 분류하지 않는 것이 좋습니다. 분류된 차원은 해당 채널이 구성되지 않은 것과 동일한 Attribution IQ 결과를 가져옵니다.

![](assets/direct-session-refresh.png)

## 모범 사례 #3:모든 채널에 대해 마지막 접촉 채널 무시 활성화

Workspace에서 마케팅 채널 차원과 함께 사용되는 사용자 지정 속성 모델은 이 설정이 활성화되면 가장 잘 작동합니다. 이 설정을 활성화하면 마케팅 채널 인스턴스가 새 채널/세부 사항이 발견되면 계산됩니다. 더 이상 사용자 지정 속성 모델(Attribution IQ)에 사용할 것을 권장하지 않는 직접 또는 내부/세션 새로 고침을 제외한 모든 채널에 대해 이 설정을 활성화해야 합니다.

![](assets/override.png)

## 모범 사례 #4:방문자 참여 기간 최소화

방문자 참여 기간을 최소 &quot;1일&quot;로 설정하면 값의 지속 가능성이 최소화됩니다. AIQ(사용자 지정 속성 모델)는 유연한 전환 창을 지원하므로 이 설정의 영향을 최소화하려면 최소 값을 설정하는 것이 좋습니다.

![](assets/expiration.png)

## 모범 사례 #5:마케팅 채널 처리 규칙은 활성화된 채널에만 있어야 합니다.

비활성화된 채널에 대한 마케팅 채널 처리 규칙을 제거해야 합니다. 규칙은 활성화됨으로 선택된 마케팅 채널에 대해서만 존재해야 합니다.
