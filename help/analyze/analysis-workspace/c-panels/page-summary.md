---
description: 페이지 요약 패널을 사용하여 선택한 페이지에 대한 요약 정보를 표시하는 방법에 대해 알아봅니다.
title: 페이지 요약 패널
feature: Panels
role: User, Admin
exl-id: f0b7cd92-17b2-452d-9aab-f78629360ab8
source-git-commit: 19c2c1abd7f1799598597c0e696d0b001c1ef0ea
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 90%

---

# 페이지 요약 패널 {#page-summary}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_button"
>title="페이지 요약"
>abstract="일부 고급 지표와 특정 페이지 간의 이동 상황을 빠르게 검토할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_panel"
>title="페이지 요약 패널"
>abstract="일부 고급 지표와 특정 페이지 간의 이동 상황을 빠르게 검토할 수 있습니다.<br/><br/>**매개변수&#x200B;**<br/>**페이지 차원 항목 추가**: 구성 요소 레일을 열고 페이지 차원을 찾은 다음 당근 모양 아이콘을 클릭하여 확장한 다음 차원 항목을 확인합니다. 그런 다음 자세히 살펴보고자 하는 특정 페이지를 빌더로 드래그 앤 드롭하십시오. 차원 항목을 드래그 앤 드롭하면 해당 페이지에 대한 주요 정보가 보고서에 자동으로 채워집니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_이 문서에서는_ ![Adobe Analytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**&#x200B;의 페이지 요약 패널에 대해 설명합니다._<br/>__![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**&#x200B;에는 동등한 패널이 없습니다._

>[!ENDSHADEBOX]

**[!UICONTROL 페이지 요약]** 패널에서 특정 페이지에 대한 주요 통계를 살펴볼 수 있습니다.

## 사용

**[!UICONTROL 페이지 요약]** 패널 사용 방법:

1. **[!UICONTROL 페이지 요약]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.



[!UICONTROL 보고서] 또는 [!UICONTROL 작업 영역]에서 패널에 액세스할 수 있습니다.

| 액세스 포인트 | 설명 |
| --- | --- |
| [!UICONTROL 보고서] | <ul><li>패널이 이미 프로젝트에 포함되었습니다.</li><li>왼쪽 레일이 축소되어 있습니다.</li><li>페이지 차원만 지원됩니다.</li><li>기본 설정이 이미 적용되었습니다. 이 경우, [!UICONTROL 페이지] 차원에서 가장 많이 방문한 페이지입니다. 이 설정은 수정할 수 있습니다.</li></ul> |
| 작업 영역 | 새로운 프로젝트를 만들고 왼쪽 레일에서 패널 아이콘을 선택합니다. [!UICONTROL 페이지 요약] 패널을 자유 형식 테이블 위로 끌어다 놓습니다. 페이지 [!UICONTROL 차원 항목] 필드가 비어 있습니다. 드롭다운 목록에서 차원 항목을 선택합니다. |

### 패널 입력 {#panel-input}

다음 입력 설정을 사용하여 [!UICONTROL 페이지 요약] 패널을 구성할 수 있습니다.

![페이지 입력 요약](assets/page-summary-input.png)

| 입력 | 설명 |
| --- | --- |
| **[!UICONTROL 페이지]** | 주요 통계를 탐색할 페이지에 대한 페이지 차원을 선택합니다. 예를 들어 **[!UICONTROL home]**&#x200B;을 사용하여 홈 페이지에 대한 통계를 살펴보십시오. 드롭다운 메뉴를 사용하여 페이지를 선택하거나 입력을 시작하여(예: `home`) 페이지를 빠르게 검색합니다. |

{style="table-layout:auto"}


패널을 빌드하려면 **[!UICONTROL 빌드]**&#x200B;를 선택합니다.

### 패널 출력 {#panel-output}

[!UICONTROL 페이지 요약] 패널은 특정 페이지에 대한 통계를 더 잘 이해할 수 있도록 풍부한 지표 데이터와 시각화를 제공합니다.

![페이지 요약 패널](assets/page-summary-output.png)

| 시각화 | 설명 |
| --- | --- |
| **[!UICONTROL 페이지 조회수] - 현재 월(지금까지)** | 현재 한 달 동안 이 페이지의 페이지 조회수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) 시각화. |
| **[!UICONTROL 페이지 조회수] - 4주 전** | 지난 한 달 동안 이 페이지의 페이지 조회수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) 시각화. |
| **[!UICONTROL 페이지 조회수] - 52주 전** | 지난 1년 동안 이 페이지의 페이지 조회수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) 시각화. |
| **[!UICONTROL 트렌드]** | 이번 달, 4주 전, 52주 전의 페이지 조회수에 대한 트렌드 [라인](/help/analyze/analysis-workspace/visualizations/line.md) 시각화. |
| **[!UICONTROL 모든 페이지 조회수의 백분율]** | 모든 페이지 조회수 중 이 페이지로 이동한 비율에 대한 요약 숫자. |
| **[!UICONTROL 페이지에서 보낸 시간]** | [가로 막대](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md)는 이 페이지에서 소요된 시간을 보여 주는 시각화. |
| **[!UICONTROL 단일 페이지 방문 횟수]** | 이 페이지에서 유일하게 방문한 페이지의 조회 수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md). |
| **[!UICONTROL 다시 로드]** | 다시 로드 중 차원 항목이 있었던 횟수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md). 방문자가 브라우저를 새로 고치는 것이 다시 로드를 트리거하는 가장 일반적인 방법입니다. |
| **[!UICONTROL 진입]** | 주어진 차원 항목이 방문에서 첫 번째 값으로 캡처된 횟수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md). |
| **[!UICONTROL 종료]** | 주어진 차원 항목이 방문에서 마지막 값으로 캡처된 횟수를 보여 주는 [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md). |
| **[!UICONTROL 플로우]** | 선택한 페이지에 초점을 맞춘 [플로우](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) 시각화. [Flow](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md) 시각화에서처럼 데이터를 더 자세히 들여다볼 수 있습니다. |

{style="table-layout:auto"}

![편집](/help/assets/icons/Edit.svg)을 사용하여 패널을 재구성하고 재작성합니다.
