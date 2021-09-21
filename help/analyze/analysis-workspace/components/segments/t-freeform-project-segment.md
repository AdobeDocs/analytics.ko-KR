---
description: Analysis Workspace에서 세그먼트를 사용합니다.
title: 세그먼트
uuid: 677f6030-5b3e-4dfa-bb79-9f27f3382fb1
feature: Workspace Basics
role: User, Admin
exl-id: 67112e13-4d0a-4d77-be50-496c3d28779c
source-git-commit: 65c955e25714591b8c4b2359969717d13626b322
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 57%

---

# 세그먼트 {#topic_DC2917A2E8FD4B62816572F3F6EDA58A}

세그먼트가 얼마나 복잡해야 하는지, 이 프로젝트에만 적용되어야 하는지에 따라 Workspace에서 다양한 유형의 세그먼트를 만들 수 있습니다. 다음은 세그먼트 유형의 요약입니다.

| 세그먼트 유형 | 어디에서 만들었습니까? | 적용 가능한 위치? | 사용 시기 |
| --- | --- | --- | --- |
| 구성 요소 목록 세그먼트 | [세그먼트 빌더](/help/components/segmentation/segmentation-workflow/seg-build.md) | 전역/공용 | 복잡한 세그먼트의 경우 순차적 세그먼트 |
| 빠른 세그먼트 | [빠른 세그먼트 빌더](/help/analyze/analysis-workspace/components/segments/quick-segments.md) | 프로젝트 수준이지만 공개할 수 있습니다. | 규칙, 이름 및 여러 규칙을 추가/편집할 수 있는 유연성과 제어 |
| 애드혹 세그먼트: |  |  |  |
| - Ad hoc Workspace 프로젝트 세그먼트 | [프로젝트의 세그먼트 드롭 영역으로 끌어다 놓습니다](/help/analyze/analysis-workspace/components/segments/ad-hoc-segments.md) | 프로젝트 수준이지만 공개할 수 있습니다. | 기본적으로 단일 규칙 세그먼트의 경우 |
| - 계산된 지표 기반 세그먼트 | [계산된 지표 빌더](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/metrics-with-segments.html) | 개별 계산된 지표로 | 지표 정의 내에 세그먼트/초 적용 |
| - VRS 기반 세그먼트 | [가상 보고서 세트 빌더](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) | 개별 가상 보고서 세트로 | VRS 정의 내에 세그먼트/초 적용 |

Adobe Analytics의 세그멘테이션에 대해 자세히 알아보려면 [여기](/help/components/segmentation/seg-overview.md)로 이동하십시오.

## 세그먼트 만들기 {#section_693CFADA668B4542B982446C2B4CF0F5}

Analysis Workspace에서 다양한 유형의 세그먼트를 만들 수 있습니다.

* [빠른 세그먼트](/help/analyze/analysis-workspace/components/segments/quick-segments.md)
* [임시 세그먼트](/help/analyze/analysis-workspace/components/segments/ad-hoc-segments.md)
* 세그먼트 라이브러리에 끝나는 일반 구성 요소 목록 세그먼트(아래 참조)

### 구성 요소 목록 세그먼트 만들기 {#section_3B07D458C43E42FDAF242BB3ACAF3E90}

구성 요소 메뉴 아래의 세그먼트 레일은 다음 아이콘으로 세그먼트 템플릿과 세그먼트를 표시합니다.

![](assets/segment_icons.png)

[Analysis Workspace에서 세그먼트 사용](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/using-segments-in-analysis-workspace.html?lang=ko-KR) (6:46)

### 세그먼트를 적용하는 다른 방법 {#section_10FF2E309BA84618990EA5B473015894}

>[!VIDEO](https://video.tv.adobe.com/v/30994/?quality=12)

자유 형식 프로젝트에 세그먼트를 적용하는 몇 가지 다른 방법이 있습니다.

| 작업 | 설명 |
|--- |--- |
| 선택 항목에서 세그먼트 만들기 | 인라인 세그먼트를 만듭니다. 이 세그먼트는 열려 있는 프로젝트에만 적용되며, Analytics 세그먼트로 저장되지는 않습니다. 1. 행을 선택합니다.  2. 선택 항목을 마우스 오른쪽 버튼으로 클릭합니다.  3. *선택 항목으로 세그먼트 만들기*&#x200B;를 클릭합니다. |
| 구성 요소 > 새 세그먼트 | 세그먼트 빌더를 표시합니다. 세그먼테이션에 대한 자세한 내용은 [세그먼트 빌더](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=ko-KR)를 참조하십시오. |
| 공유 > 프로젝트 공유 또는 공유 > 프로젝트 데이터 조정 | [조정 및 공유](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=ko-KR#concept_4A9726927E7C44AFA260E2BB2721AFC6)에서, 수신자를 위한 공유 분석에서 프로젝트에 적용하는 세그먼트를 어떻게 사용할 수 있는지 알아봅니다. |
| 세그먼트를 차원으로 사용 | 비디오: [Analysis Workspace에서 세그먼트를 차원으로 사용](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/using-segments-as-dimensions-in-analysis-workspace.html?lang=en) |

## 세그먼트 IQ

세그먼트 IQ는 다음 기능으로 구성됩니다.

* [세그먼트 비교 패널:](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md) 세그먼트 IQ의 핵심 기능. 두 세그먼트를 패널에 드래그하고 통계적으로 중요한 차이점과 두 대상 간의 겹침을 보여주는 포괄적인 보고서를 보십시오.
* [폴아웃의 세그먼트 비교:](/help/analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.md) 폴아웃 시각화의 컨텍스트에서 서로 다른 대상이 어떻게 서로 비교되는지 확인하십시오.
