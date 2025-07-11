---
description: Analysis Workspace에서 기본 프로젝트를 만드는 방법을 알아봅니다.
title: 프로젝트 만들기
feature: Workspace Basics
role: User, Admin
exl-id: 24193013-1361-43fc-b129-c44f207d9101
source-git-commit: f258a1150a4bee11f5922d058930dc38b1ddfa14
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 93%

---

# 프로젝트 만들기 {#create-projects}


Analysis Workspace의 [프로젝트](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)를 사용하여 비즈니스에 중요한 분석을 만들고 볼 수 있습니다.  이러한 분석은 조직 내부 또는 외부의 관련자와 공유할 수 있습니다.

1. Adobe Analytics에서 **[!UICONTROL Workspace]**&#x200B;를 선택합니다.

1. 왼쪽 패널에서 **[!UICONTROL 프로젝트]**&#x200B;를 선택한 다음 **[!UICONTROL 프로젝트 만들기]**&#x200B;를 선택합니다.

1. **빈 Workspace 프로젝트**&#x200B;를 선택하여 브라우저를 통해 Workspace 프로젝트를 만듭니다.

   모바일 앱을 사용하여 다른 관련자와 공유할 수 있는 모바일 스코어카드 프로젝트를 만드는 방법에 대한 자세한 내용은 [빈 모바일 스코어카드](/help/analyze/mobile-app/curator.md)를 참조하십시오.

1. [!UICONTROL **만들기**]&#x200B;를 선택합니다.


빈 Workspace 프로젝트를 만들고 나면 [Analysis Workspace](/help/analyze/analysis-workspace/home.md) 사용자 인터페이스를 잘 알고 있는지 확인합니다. 확인되면 프로젝트를 빌드할 수 있습니다. 이렇게 하려면 다음 작업을 수행하십시오.

![예제 프로젝트](assets/example-project.png)

* [패널](/help/analyze/analysis-workspace/c-panels/panels.md)를 프로젝트에 추가합니다. (예: **[!DNL Example Panel]** ➊).

* [시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)를 패널에 추가합니다. 예:
   * **[!DNL Line]** [라인](/help/analyze/analysis-workspace/visualizations/line.md) 시각화 ➋
   * **[!DNL US States]** [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) 시각화➌
* [구성 요소](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)를 시각화에 추가합니다. 예:
   * **[!DNL US States]** [차원](/help/components/dimensions/overview.md) ➍
   * **[!DNL Unique Visitors]** [지표](/help/analyze/analysis-workspace/components/apply-create-metrics.md) ➎
   * **[!DNL Average Revenue Per Order]** [계산된 지표](/help/components/c-calcmetrics/cm-overview.md) ➏
   * **[!DNL Visits from Mobile Devices]** [세그먼트](/help/components/segmentation/seg-overview.md) ➐
   * **[!DNL Last Month]** [날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md) ➑
   * **[!DNL Example]** [주석](/help/analyze/analysis-workspace/components/annotations/overview.md) ➒


## 프로젝트 정보 및 설정 {#project-info-settings}

>[!CONTEXTUALHELP]
>id="workspace_project_countrepeatinstances"
>title="반복 인스턴스 계산"
>abstract="보고서에서 반복 인스턴스가 계산되는지 여부를 지정합니다.<br/><br/>참고: 이 설정은 플로우 또는 폴아웃 시각화에 적용되지 않습니다."

>[!CONTEXTUALHELP]
>id="workspace_project_repeatinstances"
>title="반복 인스턴스 계산"
>abstract="보고서에서 반복 인스턴스가 계산되는지 여부를 지정합니다.<br/>참고: 이 설정은 플로우 또는 폴아웃 시각화에 적용되지 않습니다."


>[!CONTEXTUALHELP]
>id="workspace_project_commenting"
>title="댓글 허용"
>abstract="이 기능을 활성화하면 Analysis Workspace의 프로젝트 오른쪽 레일에 댓글 영역이 제공됩니다."


프로젝트 설정에서는 현재 활성 상태인 프로젝트에 대한 프로젝트 수준의 정보를 제공합니다.

![프로젝트 정보 및 설정 창](./assets/projectinfo.png)

설정에는 다음이 포함됩니다.

| 설정 | 설명 |
|---|---|
| 프로젝트 이름 | 프로젝트에 지정된 이름. 이름을 더블 클릭하여 편집할 수 있습니다. |
| 소유자 | 프로젝트 소유자 이름 |
| 마지막 수정 | 프로젝트의 마지막 수정 날짜. |
| 태그 | 더 쉬운 분류를 위해 프로젝트에 적용된 모든 태그를 나열합니다. |
| 설명 | 설명은 프로젝트의 목적을 명확히 하는 데 유용합니다. 설명을 더블 클릭하여 편집할 수 있습니다. |
| 반복 인스턴스 계산 | 보고서에서 반복 인스턴스가 계산되는지 여부를 지정합니다. 참고: 이 설정은 흐름 또는 폴아웃 시각화에 적용되지 않습니다. |
| 주석 표시 | 이 프로젝트의 주석을 표시할지 여부를 지정합니다. |
| [프로젝트 색상 팔레트](/help/analyze/analysis-workspace/build-workspace-project/color-palettes.md) | 색맹 사용자에 최적화된 비맞춤형 팔레트에서 선택하거나 맞춤형 팔레트를 지정하여 Workspace에서 사용되는 카테고리별 색상 팔레트를 변경할 수 있습니다. 이 기능은 대부분의 시각화를 포함하여 작업 영역의 많은 사항에 영향을 줍니다. |
| [보기 밀도](/help/analyze/analysis-workspace/build-workspace-project/view-density.md) | 자유 형식 테이블 및 코호트 테이블에서 왼쪽 패널의 수직 안쪽 여백을 줄여 화면에서 더 많은 데이터를 볼 수 있습니다. |



<!--
# Create projects in Analysis Workspace

[Projects](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) in Analysis Workspace allow you to view business-critical analyses that can be shared with stakeholders inside or outside your organization. 

For general information about how to get started using Analysis Workspace, see [Analysis Workspace overview](/help/analyze/analysis-workspace/home.md).

The following sections describe how to create a project and start adding the key building blocks for any Analysis Workspace project: panels, visualizations, and components.

## Create a project from a blank project or a report

1. In Adobe Analytics, select [!UICONTROL **Workspace**].

1. Choose whether to create a blank project or to create a project from a report:

   +++Create a blank project

   1. On the [!UICONTROL **Workspace**] tab, select the [!UICONTROL **Projects**] tab on the left side of the page, then select [!UICONTROL **Create project**].

   1. Choose whether to create a blank project or a blank mobile scorecard

      * **Blank project** if you plan to share your analysis from the browser 
      * [**Blank mobile scorecard**](/help/analyze/mobile-app/curator.md) if you plan to share your analysis from the Adobe Analytics dashboards mobile app.

   1. Select [!UICONTROL **Create**].

   +++

   +++Create a project from a report
   
      1. On the [!UICONTROL **Workspace**] tab, select the [!UICONTROL **Reports**] tab on the left side of the page.

      1. Search for or navigate to the report you want to use, then select it when it appears.

          A set of standard reports is available by default. In addition, your organization might have created custom reports for you to choose from.
          
      1. Select [!UICONTROL **Project**] > [!UICONTROL **Save**] to save the report as a new project.

          For more information about reports, see "Navigate the Reports tab" in [Adobe Analytics landing page](/help/analyze/landing.md).

   +++

1. Next, you need to add panels, visualizations, and components to your project. First, add panels to your project in Analysis Workspace, as described in [Add panels to the project](#add-panels-to-the-project). You can then add visualizations to any panels. Finally, you can add components to any panels or visualizations.

## Add panels to the project {#panels}

[Panels](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko) are the foundation to any project in Analysis Workspace. Panels are used to organize the content (visualizations and components) of a project. 

Many of the panels provided in Analysis Workspace generate a full set of analyses based on a few user inputs. 

To add a panel:

1. Select the [!UICONTROL **Panels**] icon in the left rail.

   ![](assets/build-panels.png)

1. Search for the panel you want to add. When it appears in the left rail, drag it into your project.

1. Add visualizations to your panel, as described in [Add visualizations to the project](#add-visualizations-to-the-project). 

   Alternatively, you can add components directly to a panel, as described in [Add components to the project](#add-components-to-the-project).

## Add visualizations to the project

[Visualizations](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=ko) (such as a freeform table, a bar chart, or a line chart) can be used to visually bring data to life. 

>[!TIP]
>
>Freeform tables are the most common type of visualization, and are the foundation for interactive data analysis. For more details about how to work with Freeform tables in Analysis Workspace, see [Freeform table](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md).

To add a visualization:

1. Select the **[!UICONTROL Visualizations]** icon in the left rail.

   ![](assets/build-visualizations.png)

1. Search for the visualization you want to add. When it appears in the left rail, drag it to a panel within your project. 

1. Add components to the visualization, as described in [Add components to the project](#add-components-to-the-project).

## Add components to the project

[Components](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) make up the actual data of any project. You can add components to visualizations or to panels.

>[!TIP]
>
>For information about each component, select the Info icon next to a component's name in the left rail, or see the [Analytics Components Guide](/help/components/home.md).

Following is basic information about how to add a component to a project in Analysis Workspace. For more detailed information about adding the various types of components (dimensions, metrics, segments, and date ranges), see [Use components in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

To add a component to a project in Analysis Workspace:

1. Select the **[!UICONTROL Components]** icon in the left rail.

   ![](assets/build-components.png)

1. Scroll to or search for the component you want to add, then drag it to a panel or visualization within your project. 

   For example, you can drag a segment to the segment drop zone in a panel header.

   ![drop a segment in the drop zone](assets/segment-dropzone.png)

   For more information about adding components to projects, see [Use components in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

1. (Optional) Share the project as described in [Save and share the project](#save-and-share-the-project).

## Save and share the project

As you create an analysis in Analysis Workspace, your work is [automatically saved](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md). 

When you finish building out the project and it's gathering actionable insights, the project is ready to be consumed by others. You can share the project with users and groups in your organization, or even with people outside your organization. For information about sharing a project, see [Share projects](/help/analyze/analysis-workspace/curate-share/share-projects.md).
-->