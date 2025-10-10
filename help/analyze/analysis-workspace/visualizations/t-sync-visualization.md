---
description: 자유 형식 테이블 또는 데이터 소스를 해당 시각화에 동기화하는 방법에 대해 알아봅니다.
keywords: Analysis Workspace;시각화를 데이터 소스와 동기화
title: 데이터 소스 관리
feature: Visualizations
role: User, Admin
exl-id: 0500b27a-032e-4dc8-98b7-58519ef59368
source-git-commit: f258a1150a4bee11f5922d058930dc38b1ddfa14
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 89%

---

# 데이터 소스 관리 {#manage-data-sources}

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_lockselection"
>title="선택 사항 잠금"
>abstract="이 설정을 활성화하여 시각화를 데이터 소스의 선택한 위치 또는 선택한 항목에 잠급니다."

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_lockselection_showtable"
>title="테이블 표시"
>abstract="**[!UICONTROL 테이블 표시]**&#x200B;를 선택하면 현재 시각화에 대한 새 데이터 소스를 생성하여 원래 데이터 소스와 분리시킬 수 있습니다."

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_showtable"
>title="테이블 표시"
>abstract="**[!UICONTROL 테이블 표시]**&#x200B;를 선택하면 현재 시각화에 대한 새 데이터 소스를 생성하여 원래 데이터 소스와 분리시킬 수 있습니다."


시각화를 동기화하면 시각화에 해당하는 자유 형식 테이블 또는 데이터 소스를 제어할 수 있습니다.


>[!TIP]
>
>시각화 제목 옆의 ![StatusOrange](/help/assets/icons/StatusOrange.svg) 색상을 통해 연관된 시각화를 구분할 수 있습니다. 색상이 일치하면 시각화가 동일한 데이터 소스를 기준으로 한다는 것을 의미합니다.
>

데이터 소스를 표시하거나 숨길 수 있습니다. 선택한 위치나 항목에 선택 항목을 잠글 수도 있습니다. 이러한 설정은 새 데이터가 유입될 때 시각화가 변경되는 (또는 변경되지 않는) 방식을 결정합니다.

![다음 섹션에 설명된 옵션을 보여 주는 데이터 소스 옵션 대화 상자.](assets/lock-selection.png)

<!--
**Tip:** You can tell which visualizations are related by the color of the dot next to the title. Matching colors mean that visualizations are based on the same data source.

Managing a data source lets you show the data source or lock the selection. These settings determine how the visualization changes (or doesn't change) when new data comes in.

1. [Create a project](/help/analyze/analysis-workspace/home.md) with a data table and a [visualization](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. In the data table, select the cells (data source) you want to associate with the visualization.
1. In the visualization, click the dot next to the title to bring up the **[!UICONTROL Data Source]** dialog. Select **[!UICONTROL Show Data Source]** or **[!UICONTROL Lock Selection]**.

   ![](assets/manage-data-source.png)

   Synchronizing a visualization to a table cell creates a new (hidden) table and color-codes the synchronized visualization with that table.

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Data source settings](https://video.tv.adobe.com/v/30919?quality=12&learn=on&captions=kor){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

-->

| 옵션 | 설명 |
|--- |--- |
| **[!UICONTROL 데이터 소스]** | 드롭다운 메뉴에서 시각화의 기반이 되는 데이터 소스를 선택합니다. |
| **[!UICONTROL 연결된 시각화]** | 연결된 모든 시각화를 나열합니다. 데이터 소스(자유 형식 테이블)에 적용됩니다. |
| **[!UICONTROL 데이터 소스 표시]** | 시각화에 해당하는 데이터 소스(자유 형식 테이블)를 표시하거나 숨길 수 있습니다. |
| **[!UICONTROL 선택 사항 잠금]** | 이 옵션을 선택하면 해당 데이터 테이블에서 현재 선택된 데이터로 시각화 ![LockClosed](/help/assets/icons/LockClosed.svg)를 잠급니다. 활성화되면 다음 중에서 선택합니다.  <ul><li>**선택한 위치**: 시각화가 해당 데이터 테이블에서 선택한 **위치**&#x200B;에 잠깁니다. 이 위치는 특정 항목이 위치(예: 정렬 또는 필터링)에서 변경되더라도 계속 시각화됩니다. 예를 들어 데이터 소스에 나열된 상위 5개 캠페인 이름을 이 시각화에 항상 표시하려면 이 옵션을 선택합니다. 어떤 캠페인 이름이 표시되는지는 중요하지 않습니다.</li> <li>**선택한 항목**: 시각화가 해당 데이터 테이블에서 현재 선택한 특정 **항목**&#x200B;에 잠깁니다. 이러한 항목은 테이블의 항목 간에 순위가 바뀌는 경우에도 계속 시각화됩니다. 예를 들어 데이터 소스에 나열된 동일한 5개의 특정 캠페인 이름을 이 시각화에 항상 표시하려면 이 옵션을 선택합니다. 캠페인 이름의 순위가 어떻게 되는지는 중요하지 않습니다.</li></ul>연결된 데이터 테이블에 시각화가 더 이상 표시되지 않는 데이터로 잠긴 경우 새 테이블을 생성할 수 있습니다. **[!UICONTROL 테이블 표시]**&#x200B;를 선택하면 현재 시각화에 대한 새 데이터 소스를 생성하여 원래 데이터 소스와 분리시킬 수 있습니다. |
