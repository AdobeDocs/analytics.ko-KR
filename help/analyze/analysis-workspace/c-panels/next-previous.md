---
description: 특정 차원에 대한 다음 또는 이전 차원 항목을 표시하는 패널입니다.
title: 다음 또는 이전 항목 패널
feature: Panels
role: User, Admin
exl-id: 9f2f8134-2a38-42bb-b195-5e5601d33c4e
source-git-commit: 7bac64aed46d9d7a83dc61c3f55d33ad56564efe
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 36%

---

# 다음 또는 이전 항목 패널 {#next-or-previous-item-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_button"
>title="다음 또는 이전 항목"
>abstract="사용자의 이전 차원과 사용자의 다음 차원을 파악할 수 있는 패널을 만듭니다."

<!-- markdownlint-disable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_nextorpreviousitem_panel"
>title="다음 또는 이전 항목"
>abstract="방문자들이 이전에 왔거나 다음으로 이동하는 가장 일반적인 장소를 분석합니다.<br/><br/>**차원**: 차원을 선택합니다. 예: **페이지**.<br/>**차원 항목**: 특정 차원 항목을 선택합니다. 예: **홈 페이지**.<br/>**방향**: **다음**&#x200B;을 선택하여 선택한 차원 항목 바로 다음에 차원 항목을 표시합니다. **이전**&#x200B;을 선택하여 선택한 차원 항목으로 이어지는 차원 항목을 표시합니다.<br/>**컨테이너**: **세션**&#x200B;을 선택하여 동일한 세션 내에서 다음/이전 차원 항목을 표시하거나 **사용자**&#x200B;를 선택하여 동일한 사용자의 다음/이전 차원 항목을 표시합니다."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

*이 문서는&#x200B;**Adobe Analytics**의 다음 또는 이전 항목 패널을 문서화합니다.<br/>이 문서의&#x200B;**Customer Journey Analytics**버전을 보려면 [다음 또는 이전 항목 패널](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/next-previous)을 참조하세요.*

>[!ENDSHADEBOX]

**[!UICONTROL 다음 또는 이전 항목]** 패널에는 특정 차원에 대한 다음 또는 이전 차원 항목을 식별하는 많은 표와 시각화가 포함되어 있습니다. 예를 들어 고객이 홈 페이지를 방문한 후 가장 자주 방문한 페이지를 탐색할 수 있습니다.

## 사용

**[!UICONTROL 다음 또는 이전 항목]** 패널을 사용하려면:

1. **[!UICONTROL 다음 또는 이전 항목]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.

### 패널 입력

다음 입력 설정을 사용하여 [!UICONTROL 다음 또는 이전 항목] 패널을 구성할 수 있습니다.

![다음 또는 이전 항목 패널](assets/next-or-previous-item.png)

| 입력 | 설명 |
| --- | --- |
| **[!UICONTROL 차원]** | 다음 또는 이전 항목을 탐색할 차원을 선택합니다. |
| **[!UICONTROL 차원 항목]** | 다음/이전 조회의 중심에 있는 특정 차원 항목을 선택합니다. |
| **[!UICONTROL 방향]** | [!UICONTROL 다음] 또는 [!UICONTROL 이전] 차원 항목을 찾고 있는지 여부를 지정하십시오. |
| **[!UICONTROL 컨테이너]** | 컨테이너 [!UICONTROL 세션] 또는 [!UICONTROL 개인](기본값)을 선택하여 문의 범위를 결정합니다. |

{style="table-layout:auto"}

패널을 빌드하려면 **[!UICONTROL 빌드]**&#x200B;를 선택하십시오.

### 패널 출력

[!UICONTROL 다음 또는 이전 항목] 패널은 특정 차원 항목의 다음 또는 이전 발생 횟수를 더 잘 이해할 수 있도록 풍부한 데이터 및 시각화를 반환합니다.


![다음/이전 패널 출력](assets/next-or-previous-item-output.png)


| 시각화 | 설명 |
| --- | --- |
| **[!UICONTROL 가로 막대형]** | 선택한 차원 항목을 기반으로 다음(또는 이전) 항목을 나열합니다. 개별 막대에 마우스를 가져다 대면 자유 형식 테이블에서 해당 항목이 강조 표시됩니다. |
| **[!UICONTROL 요약 번호]** | 현재 월에 대한 모든 다음 또는 이전 차원 항목 발생의 높은 수준 요약 번호(현재까지)입니다. |
| **[!UICONTROL 자유 형식 테이블]** | 선택한 차원 항목을 기반으로 다음(또는 이전) 항목을 테이블 형식으로 나열합니다. 예를 들어, 사람들이 홈 페이지 또는 작업 영역 페이지 뒤(또는 이전)로 이동한 가장 방문 빈도가 높은 페이지(발생 횟수별)입니다. |

{style="table-layout:auto"}


>[!MORELIKETHIS]
>
>[Create a panel](/help//analyze/analysis-workspace/c-panels/panels.md#create-a-panel)
>

<!--
# Next or previous item panel

This panel contains a number of tables and visualizations to easily identify the next or previous dimension item for a specific dimension. For example, you might want to explore which pages customers went to most often after they visited the Home page.

## Access the panel

You can access the panel from within [!UICONTROL Reports] or within [!UICONTROL Workspace].

| Access point | Description |
| --- | --- |
| [!UICONTROL Reports] | <ul><li>The panel is already dropped into a project.</li><li>The left rail is collapsed.</li><li>If you selected [!UICONTROL Next page], default settings have already been applied, such as [!UICONTROL Page] for [!UICONTROL Dimension], and the top page as the [!UICONTROL Dimension Item], [!UICONTROL Next] for [!UICONTROL Direction] and [!UICONTROL Visit] for [!UICONTROL Container]. You can modify all these settings.</li></ul>![Next/Previous panel](assets/next-previous.png)|
| Workspace | Create a new project and select the Panel icon in the left rail. Then drag the [!UICONTROL Next or previous item] panel above the Freeform table. Notice that the [!UICONTROL Dimension] and [!UICONTROL Dimension Item] fields are left blank. Select a dimension from the drop-down list. [!UICONTROL Dimension items] are populated based on the [!UICONTROL dimension] you chose. The top dimension item gets added, but you can select a different item. The defaults are Next and Visitor. Again, you can modify these as well.<p>![Next/Previous panel](assets/next-previous2.png) |

{style="table-layout:auto"}

## Panel Inputs {#Input}

You can configure the [!UICONTROL Next or previous item] panel panel using these input settings:

| Setting | Description |
| --- | --- |
| Segment (or other component) drop zone | You can drag and drop segments or other components to further filter your panel results. |
| Dimension | The dimension for which you want to explore next or previous items. |
| Dimension Item | The specific item at the center of your next/previous inquiry. |
| Direction | Specify whether you are looking for the [!UICONTROL Next] or the [!UICONTROL Previous] dimension item. |
| Container | [!UICONTROL Visit] or [!UICONTROL Visitor] (default) determine the scope of your inquiry. |

{style="table-layout:auto"}

Click **[!UICONTROL Build]** to build the panel.

## Panel output {#output}

The [!UICONTROL Next or previous item] panel returns a rich set of data and visualizations to help you better understand what occurrences follow or precede specific dimension items.

![Next/Previous panel output](assets/next-previous-output.png)

![Next/Previous panel output](assets/next-previous-output2.png)

| Visualization | Description |
| --- | --- |
| Horizontal bar | Lists the next (or previous) items based on the dimension item you chose. Hovering over an individual bar highlights the corresponding item in the Freeform table. |
| Summary number | High-level summary number of all next or previous dimension item occurrences for the current month (so far.) |
| Freeform table | Lists the next (or previous) items based on the dimension item you chose, in a table format. For example, which were the most popular pages (by occurrences) that people went to after (or before) the home page or the workspace page. |

{style="table-layout:auto"}

-->