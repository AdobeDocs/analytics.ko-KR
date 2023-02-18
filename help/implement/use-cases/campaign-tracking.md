---
title: 캠페인 추적 워크플로우
description: Adobe Analytics을 사용하여 마케팅 활동을 추적합니다.
feature: Implementation Basics
exl-id: 9f7920e0-471c-46bc-9314-7b0a7c93fdce
source-git-commit: c118d42667c4a1af55929834b87d148a5973bed9
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# 캠페인 추적 워크플로우

조직에서 마케팅 활동의 성과 및 클릭스루 비율을 추적하려는 경우 다음 프로세스를 사용할 수 있습니다. 이러한 각 단계에는 아래에 자세히 나와 있는 전용 섹션이 있습니다.

1. [추적 코드 생성 프로세스 설정](#establish-a-tracking-code-generation-process)
1. [원하는 추적 코드를 이메일에 추가합니다](#add-the-desired-tracking-code-to-the-email)
1. [추적 코드 데이터를 포함하도록 Adobe Analytics 구현을 설정 또는 조정합니다](#include-campaign-variables-in-your-implementation)
1. [Analysis Workspace에서 보고서 보기](#view-the-reports-in-analysis-workspace)

[Adobe Campaign](https://business.adobe.com/products/campaign/adobe-campaign.html) 은 이러한 각 단계를 간소화하여 마케팅 활동의 가치를 극대화할 수 있습니다. 자세한 내용은 Adobe 영업 담당자에게 문의하십시오.

## 추적 코드 생성 프로세스 설정

모든 조직에는 추적 코드에 대한 다양한 요구 사항이 있습니다. 일부 조직에는 수동으로 만든 추적 코드가 충분하지 않은 최소 요구 사항이 있을 수 있습니다. 다른 조직에서는 추적을 보다 세밀하게 제어하고 원하는 추적 코드를 만들기 위한 여러 시스템이 제위치에 있을 수 있습니다. 조직에서 Adobe Analytics 외에도 Google Analytics을 사용하는 경우 조직에 이미 `utm` 추적 코드 모델이 설정되었습니다.

추적 코드를 만들거나 생성하는 방법에 관계없이, 일관된 시스템을 통해 추적 코드를 함께 그룹화하여 보고하려는 경우 보다 쉽게 조직에 연결할 수 있습니다. 일관되게 구조화된 추적 코드를 사용하여 다음을 만들 수 있습니다 [분류 규칙](/help/components/classifications/crb/classification-rule-builder.md) 범주 성능에 대한 통찰력을 얻을 수 있습니다.

## 원하는 추적 코드를 URL에 추가합니다

원하는 추적 코드 값이 있으면 광고, 소셜 미디어 또는 이메일과 같이 온라인에서 게시하는 링크에 추가할 수 있습니다. 이러한 추적 코드를 추가하는 작업은 일반적으로 링크의 쿼리 문자열에서 수행됩니다. 사용하는 쿼리 문자열 매개 변수는 조직의 추적 요구 사항에 따라 다릅니다. 일반적인 쿼리 문자열 매개 변수는 `cid` (campaign ID에는 짧습니다.) Google Analytics을 사용하는 일부 조직에는 다음과 같은 여러 캠페인 쿼리 문자열 매개 변수가 이미 있을 수 있습니다. `utm_source`, `utm_medium`, 및 기타.

이메일의 링크에 쿼리 문자열을 추가하는 것은 다음과 비슷합니다.

```text
https://example.com?cid=EM989027
```

## 구현에 캠페인 변수를 포함하십시오

Adobe Analytics에는 전용 기능이 있습니다 [추적 코드](/help/components/dimensions/tracking-code.md) 조직 전체에서 다양한 마케팅 활동을 측정하는 데 사용할 수 있는 차원입니다. 그러나 서로 다른 조직에는 서로 다른 추적 요구 사항이 있을 수 있습니다. 조직의 [솔루션 디자인 문서](../prepare/solution-design.md) 를 입력하여 올바른 변수의 올바른 값을 일관되게 추적할 수 있습니다.

조직에서 아직 캠페인 추적을 설정하지 않은 경우 구현을 조정하여 [`campaign`](/help/implement/vars/page-vars/campaign.md) 변수를 채우는 방법을 설명합니다. 자세한 내용은 [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) 조직의 구현과 관련된 쿼리 문자열 매개 변수 값을 수집하는 방법을 알아봅니다.

조직에서 `utm` 쿼리 문자열에서 다음 중 하나를 선택할 수 있습니다.

* 모두 보내기 `utm` 연결된 값으로 추적 코드 차원에 문자열을 질의합니다. 그런 다음 를 사용할 수 있습니다 [분류 규칙](/help/components/classifications/crb/classification-rule-builder.md) 각 차원에 중점을 두는 추가 차원을 만들려면 `utm` 매개 변수. 이 메서드는 더 복잡한 학습 곡선을 가지지만 추가 eVar는 사용하지 않습니다.
* 각각 보내기 `utm` 쿼리 문자열을 별도의 [eVar](/help/components/dimensions/evar.md). 이 방법은 전체적으로 를 구현하는 것이 더 간단하지만 추가 eVar를 사용해야 합니다.

## Analysis Workspace에서 보고서 보기

추적 코드 데이터를 수집하도록 구현을 제대로 설정했으면 Analysis Workspace에서 보고서를 볼 수 있습니다.

1. 에 로그인합니다. [Adobe Experience Cloud](https://experience.adobe.com) 을(를) 선택합니다. [!UICONTROL Adobe Analytics].
1. 만들기 [작업 공간 프로젝트](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).
1. 왼쪽의 구성 요소 목록에서 [추적 코드](/help/components/dimensions/tracking-code.md) 차원을 작업 공간 캔버스에 추가합니다.
1. 원하는 지표(예: )를 드래그합니다 [방문 횟수](/help/components/metrics/visits.md) 또는 [주문](/help/components/metrics/orders.md) 작업 공간 캔버스 오른쪽의

![캠페인 추적 보고서](../assets/campaign-tracking-report.png)
