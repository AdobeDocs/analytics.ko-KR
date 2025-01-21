---
description: 페이지 요약 패널에는 선택한 페이지에 대한 요약 정보가 표시됩니다.
title: 페이지 요약 패널
feature: Panels
role: User, Admin
exl-id: f0b7cd92-17b2-452d-9aab-f78629360ab8
source-git-commit: 2aaa8c0d13755b40ec701ca6342ab773103a0422
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 12%

---

# 페이지 요약 패널 {#page-summary}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_button"
>title="페이지 요약"
>abstract="일부 높은 수준의 지표는 물론 특정 페이지로의 이동도 빠르게 검토합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_panel"
>title="페이지 요약 패널"
>abstract="일부 높은 수준의 지표는 물론 특정 페이지로의 이동도 빠르게 검토합니다.<br/><br/>**매개 변수&#x200B;**<br/>**페이지 차원 항목 추가**: 구성 요소 레일을 열고 페이지 차원을 찾은 다음 당근을 클릭하여 확장하여 차원 항목을 봅니다. 그런 다음 학습할 특정 페이지를 빌더로 끌어서 놓습니다. 차원 항목을 끌어다 놓으면 보고서가 페이지에 대한 주요 정보로 자동으로 채워집니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_이 문서는_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**&#x200B;의 페이지 요약 패널에 대한 문서를 제공합니다._<br/>_동등한 패널이_&#x200B;에 없습니다. ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._

>[!ENDSHADEBOX]

**[!UICONTROL 페이지 요약]** 패널을 통해 특정 페이지에 대한 주요 통계를 살펴볼 수 있습니다.

## 사용

**[!UICONTROL 페이지 요약]** 패널을 사용하려면:

1. **[!UICONTROL 페이지 요약]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.



[!UICONTROL 보고서] 또는 [!UICONTROL Workspace] 내에서 패널에 액세스할 수 있습니다.

| 액세스 지점 | 설명 |
| --- | --- |
| [!UICONTROL 보고서] | <ul><li>패널이 이미 프로젝트에 드롭되었습니다.</li><li>왼쪽 레일이 무너졌습니다.</li><li>페이지 차원만 지원됩니다.</li><li>기본 설정이 이미 적용되었습니다. 이 경우 [!UICONTROL 페이지] 차원에 대해 가장 많이 방문한 페이지입니다. 이 설정을 수정할 수 있습니다.</li></ul> |
| 작업 영역 | 새 프로젝트를 만들고 왼쪽 레일에서 패널 아이콘을 선택합니다. [!UICONTROL 페이지 요약] 패널을 자유 형식 테이블 위로 드래그합니다. [!UICONTROL Dimension 항목] 필드가 비어 있습니다. 드롭다운 목록에서 차원 항목을 선택합니다. |

### 패널 입력 {#panel-input}

다음 입력 설정을 사용하여 [!UICONTROL 페이지 요약] 패널을 구성할 수 있습니다.

![페이지 입력 요약](assets/page-summary-input.png)

| 입력 | 설명 |
| --- | --- |
| **[!UICONTROL 페이지]** | 주요 통계를 탐색할 페이지에 대한 페이지 차원을 선택합니다. |

{style="table-layout:auto"}


패널을 빌드하려면 **[!UICONTROL 빌드]**&#x200B;를 선택하십시오.

### 패널 출력 {#panel-output}

[!UICONTROL 페이지 요약] 패널에서는 특정 페이지에 대한 통계를 더 잘 이해할 수 있도록 다양한 지표 데이터 및 시각화를 반환합니다.

![페이지 요약 패널](assets/page-summary-output.png)

| 시각화 | 설명 |
| --- | --- |
| **[!UICONTROL 페이지 보기 수] - 현재 월(현재까지)** | 현재 월의 이 페이지에 대한 페이지 보기 수를 보여 주는 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) 시각화입니다. |
| **[!UICONTROL 페이지 보기 수] - 4주 전** | 지난 달 동안 이 페이지의 페이지 보기 수를 보여 주는 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) 시각화입니다. |
| **[!UICONTROL 페이지 보기 수] - 52주 전** | 지난 1년간 이 페이지의 페이지 보기 수를 보여 주는 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) 시각화입니다. |
| **[!UICONTROL 트렌드]** | 4주 전, 52주 전 이번 달 페이지 보기에 대한 트렌드 [Line](/help/analyze/analysis-workspace/visualizations/line.md) 시각화입니다. |
| **[!UICONTROL 모든 페이지 보기의 백분율]** | 이 페이지로 이동한 모든 페이지 보기 수의 비율에 대한 요약 번호입니다. |
| **[!UICONTROL 페이지에서 보낸 시간]** | 이 페이지에서 보낸 시간을 보여 주는 [가로 막대](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md) 시각화입니다. |
| **[!UICONTROL 단일 페이지 방문 횟수]** | [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)로, 이 페이지가 방문한 유일한 페이지인 페이지 보기 수를 표시합니다. |
| **[!UICONTROL 다시 로드]** | 다시 로드하는 동안 차원 항목이 있었던 횟수를 보여 주는 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)입니다. 방문자가 브라우저를 새로 고치는 것이 다시 로드를 트리거하는 가장 일반적인 방법입니다. |
| **[!UICONTROL 항목]** | 주어진 차원 항목이 방문에서 첫 번째 값으로 캡처된 횟수를 보여 주는 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)입니다. |
| **[!UICONTROL 종료]** | 주어진 차원 항목이 방문에서 마지막 값으로 캡처된 횟수를 보여 주는 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)입니다. |
| **[!UICONTROL 흐름]** | 선택한 페이지를 초점으로 하는 [흐름](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) 시각화입니다. [흐름](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md) 시각화에서와 같이 데이터를 더 자세히 들여다 볼 수 있습니다. |

{style="table-layout:auto"}

![편집](/help/assets/icons/Edit.svg)을 사용하여 패널을 다시 구성하고 다시 빌드합니다.
