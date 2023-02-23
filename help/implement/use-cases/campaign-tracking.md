---
title: 캠페인 추적 워크플로
description: Adobe Analytics를 사용하여 마케팅 활동을 추적하십시오.
feature: Implementation Basics
exl-id: 9f7920e0-471c-46bc-9314-7b0a7c93fdce
source-git-commit: c118d42667c4a1af55929834b87d148a5973bed9
workflow-type: ht
source-wordcount: '581'
ht-degree: 100%

---

# 캠페인 추적 워크플로

조직에서 마케팅 활동의 성과 및 클릭스루 비율을 추적하려는 경우 다음 프로세스를 사용할 수 있습니다. 이러한 각 단계에는 아래에 더 자세한 내용이 포함된 전용 섹션이 있습니다.

1. [추적 코드 생성 프로세스 설정](#establish-a-tracking-code-generation-process)
1. [이메일에 원하는 추적 코드 추가](#add-the-desired-tracking-code-to-the-email)
1. [추적 코드 데이터를 포함하도록 Adobe Analytics 구현 설정 또는 조정](#include-campaign-variables-in-your-implementation)
1. [Analysis Workspace에서 보고서 보기](#view-the-reports-in-analysis-workspace)

[Adobe Campaign](https://business.adobe.com/products/campaign/adobe-campaign.html)은 이러한 각 단계를 단순화하여 마케팅 활동에서 최대한의 가치를 이끌어내는 데 도움이 될 수 있습니다. 자세한 내용은 Adobe 영업 담당자에게 문의하십시오.

## 추적 코드 생성 프로세스 설정

추적 코드에 대한 요구 사항은 조직마다 다릅니다. 수동으로 작성한 추적 코드로도 충분할 경우 일부 조직은 필요한 사항이 최소화될 수 있습니다. 다른 조직에서는 추적에 대한 더 많은 제어를 원하고 원하는 추적 코드를 생성하기 위한 여러 시스템을 갖추고 있을 수 있습니다. 조직에서 Adobe Analytics와 함께 Google Analytics를 사용하는 경우 이미 `utm` 추적 코드 모델을 갖추고 있는 것입니다.

추적 코드를 만들거나 생성하는 방법에 관계없이 일관된 시스템을 갖추면 조직에서 보고용 추적 코드를 훨씬 간편하게 그룹화할 수 있습니다. 일관되게 구성된 추적 코드를 사용하면 [분류 규칙](/help/components/classifications/crb/classification-rule-builder.md)을 만들어 범주별 성능에 대한 통찰력을 얻을 수 있습니다.

## URL에 원하는 추적 코드 추가

광고, 소셜 미디어 또는 이메일과 같이 온라인에 게시하는 모든 링크에 원하는 추적 코드 값을 추가할 수 있습니다. 이러한 추적 코드를 추가하는 작업은 일반적으로 링크의 쿼리 문자열에서 이루어집니다. 사용하는 쿼리 문자열 매개 변수는 조직의 추적 요구 사항에 따라 다릅니다. 일반적인 쿼리 문자열 매개변수는 `cid`입니다(캠페인 ID의 약자). Google Analytics도 함께 사용하는 일부 조직에는 이미 `utm_source`, `utm_medium` 등과 같은 여러 캠페인 쿼리 문자열 매개 변수가 있을 수 있습니다.

이메일의 링크에 쿼리 문자열을 추가한 모습은 다음과 유사합니다.

```text
https://example.com?cid=EM989027
```

## 구현에 캠페인 변수 포함

Adobe Analytics에는 조직 전체의 다양한 마케팅 활동을 측정하는 데 사용할 수 있는 전용 [추적 코드](/help/components/dimensions/tracking-code.md) 차원이 있습니다. 그러나 조직마다 추적 요구 사항이 다를 수 있습니다. 조직의 [솔루션 디자인 문서](../prepare/solution-design.md)를 참조하여 올바른 변수에서 올바른 값을 일관되게 추적하는 것이 중요합니다.

조직에서 아직 캠페인 추적을 설정하지 않은 경우 구현을 조정하여 [`campaign`](/help/implement/vars/page-vars/campaign.md) 변수를 설정할 수 있습니다. [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) 메서드를 참조하여 조직의 구현과 관련된 쿼리 문자열 매개 변수 값을 수집하는 방법에 대해 알아보십시오.

조직에서 `utm` 쿼리 문자열을 수집하는 경우 다음 중 하나를 선택할 수 있습니다.

* 모든 `utm` 쿼리 문자열을 연결된 값으로 추적 코드 차원에 전송합니다. 그런 다음 [분류 규칙](/help/components/classifications/crb/classification-rule-builder.md)을 사용하여 `utm` 매개 변수에 중점을 두는 추가 차원을 만들 수 있습니다. 이 방법은 학습 곡선이 더 복잡하지만 추가 eVar를 사용하지 않습니다.
* 각 `utm` 쿼리 문자열을 별도의 [eVar](/help/components/dimensions/evar.md)로 전송합니다. 이 방법은 전반적으로 구현하기가 더 간단하지만 추가 eVar를 사용해야 합니다.

## Analysis Workspace에서 보고서 보기

추적 코드 데이터를 수집하도록 구현을 올바르게 설정하면 Analysis Workspace에서 보고서를 볼 수 있습니다.

1. [Adobe Experience Cloud](https://experience.adobe.com)에 로그인한 다음 [!UICONTROL Adobe Analytics]를 선택합니다.
1. [작업 영역 프로젝트](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)를 만듭니다.
1. 왼쪽의 구성 요소 목록에서 [추적 코드](/help/components/dimensions/tracking-code.md) 차원을 작업 영역 캔버스로 드래그합니다.
1. [방문 횟수](/help/components/metrics/visits.md) 또는 [주문 수](/help/components/metrics/orders.md) 등 원하는 지표를 작업 영역 캔버스의 오른쪽으로 드래그합니다.

![캠페인 추적 보고서](../assets/campaign-tracking-report.png)
