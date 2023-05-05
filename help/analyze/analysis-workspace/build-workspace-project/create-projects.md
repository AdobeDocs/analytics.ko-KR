---
description: Analysis Workspace에서 프로젝트를 만드는 기본 사항을 알아봅니다
title: 프로젝트 만들기
feature: Workspace Basics
role: User, Admin
source-git-commit: dadda9e105526c05ee763f4502f38524f5ddb1f0
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 5%

---

# 프로젝트 만들기

[프로젝트](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) Analysis Workspace에서 조직 내부 또는 외부의 이해 관계자와 공유할 수 있는 비즈니스 크리티컬 데이터를 표면화할 수 있습니다.

Analysis Workspace 사용을 시작하는 방법에 대한 일반적인 내용은 [Analysis Workspace 개요](/help/analyze/analysis-workspace/home.md).

다음 섹션에서는 프로젝트를 만들고 모든 Analysis Workspace 프로젝트의 주요 빌딩 블록을 추가하는 방법에 대해 설명합니다. 패널, 시각화 및 구성 요소.

## 빈 프로젝트 또는 템플릿에서 프로젝트 만들기

1. Adobe Analytics에서 [!UICONTROL **작업 공간**].

1. 빈 프로젝트를 만들지 아니면 템플릿에서 프로젝트를 생성할지 선택합니다.

   +++빈 프로젝트 만들기

   1. 을(를) 선택합니다 [!UICONTROL **프로젝트**] 탭을 선택하고 [!UICONTROL **프로젝트 만들기**].

   1. 빈 프로젝트를 만드는지 빈 모바일 스코어카드를 만드는지 선택합니다

      * **빈 프로젝트** 브라우저에서 분석을 공유할 계획이라면
      * [**빈 모바일 스코어카드**](/help/analyze/mobile-app/curator.md) Adobe Analytics 대시보드 모바일 앱에서 분석을 공유할 계획인 경우.
   1. Select [!UICONTROL **Create**].

+++

   +++템플릿에서 프로젝트 만들기

   1. 을(를) 선택합니다 [!UICONTROL **보고서**] 탭.

   1. 사용할 템플릿을 검색하거나 해당 템플릿으로 이동한 다음 표시될 때 선택합니다.

      표준 템플릿 세트는 기본적으로 사용할 수 있습니다. 또한, 조직에서 사용자가 선택할 수 있는 사용자 지정 템플릿을 만들 수도 있습니다.

      자세한 내용은 [Reports &amp; Analytics 시작하기](/help/analyze/reports-analytics/getting-started.md).
+++

1. 그런 다음 패널, 시각화 및 구성 요소를 프로젝트에 추가해야 합니다. 먼저 다음에 설명된 대로 Analysis Workspace에서 프로젝트에 패널을 추가합니다 [프로젝트에 패널 추가](#add-panels-to-the-project). 그런 다음 패널에 시각화를 추가할 수 있습니다. 마지막으로, 패널 또는 시각화에 구성 요소를 추가할 수 있습니다.

## 프로젝트에 패널 추가 {#panels}

[패널](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko) 는 Analysis Workspace에 있는 모든 프로젝트의 기반입니다. 패널 은 프로젝트의 컨텐츠(시각화 및 구성 요소)를 구성하는 데 사용됩니다.

Analysis Workspace에서 제공되는 많은 패널은 몇 개의 사용자 입력을 기반으로 전체 분석 집합을 생성합니다.

패널을 추가하려면 다음을 수행하십시오.

1. 을(를) 선택합니다 [!UICONTROL **패널**] 아이콘을 클릭합니다.

   ![](assets/build-panels.png)

1. 추가할 패널을 검색합니다. 왼쪽 레일에 나타나면 프로젝트로 드래그합니다.

1. 에 설명된 대로 시각화를 패널에 추가합니다. [프로젝트에 시각화 추가](#add-visualizations-to-the-project).

   또는, [프로젝트에 구성 요소 추가](#add-components-to-the-project).

## 프로젝트에 시각화 추가

[시각화](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=ko) (자유 형식 테이블, 막대 차트 또는 라인 차트와 같은)를 사용하여 데이터를 시각적으로 생동감 있게 가져올 수 있습니다.

>[!TIP]
>
>자유 형식 테이블은 시각화의 가장 일반적인 유형이며, 대화형 데이터 분석을 위한 기반입니다. Analysis Workspace에서 자유 형식 테이블로 작업하는 방법에 대한 자세한 내용은 [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md).

시각화를 추가하려면:

1. 을(를) 선택합니다 **[!UICONTROL 시각화]** 아이콘을 클릭합니다.

   ![](assets/build-visualizations.png)

1. 추가할 시각화를 검색합니다. 왼쪽 레일에 나타나면 프로젝트 내의 패널로 드래그합니다.

1. 에 설명된 대로 시각화에 구성 요소를 추가합니다. [프로젝트에 구성 요소 추가](#add-components-to-the-project).

## 프로젝트에 구성 요소 추가

[구성 요소](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) 프로젝트의 실제 데이터를 구성합니다. 시각화 또는 패널에 구성 요소를 추가할 수 있습니다.

>[!TIP]
>
>각 구성 요소에 대한 자세한 내용은 왼쪽 레일에서 구성 요소의 이름 옆에 있는 정보 아이콘을 선택하거나 [Analytics 구성 요소 안내서](/help/components/home.md).

구성 요소를 추가하려면

1. 을(를) 선택합니다 **[!UICONTROL 구성 요소]** 아이콘을 클릭합니다.

   ![](assets/build-components.png)

1. 추가할 구성 요소를 검색합니다. 왼쪽 레일에 나타나면 프로젝트 내의 패널 또는 시각화로 드래그합니다.

### 프로젝트를 저장하고 공유

Analysis Workspace에서 분석을 만들면 작업은 다음과 같습니다 [자동 저장](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md).

프로젝트 작성을 완료하고 실행 가능한 통찰력을 수집하면 다른 사용자가 프로젝트를 사용할 수 있습니다. 프로젝트를 조직의 사용자 및 그룹이나 조직 외부의 사용자와 공유할 수 있습니다. 프로젝트 공유에 대한 자세한 내용은 [프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md).

