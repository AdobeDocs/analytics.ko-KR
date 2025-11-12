---
title: Analysis Workspace 개요
description: Adobe Analytics의 고급 분석 도구인 Analysis Workspace에 대해 알아봅니다. 프로젝트, 패널, 테이블, 시각화 및 기타 구성 요소를 사용하여 데이터를 생생하게 표현하고 분석을 조정하여 공유할 수 있습니다.
feature: Workspace Basics
role: User, Admin
exl-id: de95551d-09ea-4461-9bb4-b4ef235e9cd2
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 100%

---

# Analysis Workspace 개요 {#analysis-workspace-overview}

Analysis Workspace를 사용하면 분석을 신속하게 빌드하여 인사이트를 수집한 다음 해당 인사이트를 다른 사람과 공유할 수 있습니다. 드래그 앤 드롭 브라우저 인터페이스를 사용하여 분석을 만들고, 시각화를 추가하여 데이터를 생동감 있게 표현하고, 데이터 세트를 조정하며, 원하는 누구와도 [프로젝트](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)를 공유 및 예약할 수 있습니다.

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Analysis Workspace 개요](https://video.tv.adobe.com/v/35560/?captions=kor&quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

## 인터페이스

다음 이미지와 함께 제공되는 테이블은 Analysis Workspace 사용자 인터페이스의 주요 요소를 설명합니다.

![인터페이스의 다양한 섹션을 강조하는 Analysis Workspace 창](assets/analysis-workspace-overview.png)

| 위치 | 이름 및 기능 |
|:---------:|----------|
| A | 프로젝트 이름기능에 액세스하는 메뉴 구조, 프로젝트 목록으로 돌아가는 ![뒤로 버튼](/help/assets/icons/ChevronLeft.svg) 및 [Workspace 프로젝트를 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md)하는 **[!UICONTROL 공유]** 버튼을 포함합니다. <br/>언제든지 프로젝트 이름(예: 새 프로젝트)을 선택하여 이름을 변경합니다. <br/>프로젝트를 자주 사용하는 프로젝트로 표시하려면 ![즐겨찾기에서 추가](/help/assets/icons/Star.svg) 또는![즐겨찾기 취소](/help/assets/icons/StarOutline.svg)를 선택합니다. |
| B | **버튼 패널:** Analysis Workspace의 주요 [기능](#features)에 액세스할 수 있는 버튼이 포함되어 있습니다.<ul><li>![WebPage](/help/assets/icons/WebPage.svg) [[!UICONTROL 패널]](/help/analyze/analysis-workspace/c-panels/panels.md)</li><li>![GraphBarVertical](/help/assets/icons/GraphBarVertical.svg) [[!UICONTROL 시각화]](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</li><li>![Curate](/help/assets/icons/Curate.svg) [[!UICONTROL 구성 요소]](/help/components/home.md)</li><li>![ViewList](/help/assets/icons/ViewList.svg) [[!UICONTROL 목차]](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md)</li><li>![Bookmark](/help/assets/icons/Bookmark.svg) [[!UICONTROL 데이터 사전]](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)</li></ul> |
| C | **왼쪽 패널**: 이 영역에는 개별 패널, 시각화, 구성 요소 또는 목록이 포함됩니다. 콘텐츠는 버튼 패널에서 선택한 버튼에 따라 달라집니다. |
| D | **캔버스**: 왼쪽 패널에서 콘텐츠를 드래그하여 프로젝트를 빌드하는 기본 영역입니다. 패널을 추가하고, 시각화를 패널에 추가하고, 구성 요소를 시각화에 추가하면 프로젝트가 동적으로 업데이트됩니다. 여러 패널을 만들고, 각 패널 내부에서 여러 시각화를 만들 수 있습니다.<br/>각 패널은 선택한 보고서 세트를 기반으로 합니다. 선택한 보고서 세트는 사용할 수 있는 지표와 차원과 같은 구성 요소를 결정합니다. 자세한 내용은 [패널 - 보고서 세트](/help/analyze/analysis-workspace/c-panels/panels.md#report-suite)를 참조하십시오. |

## 기능

버튼 패널을 통해 Analysis Workspace의 주요 기능을 사용할 수 있습니다.

| 아이콘 | 기능 | 설명 |
|:---:|---|---|
| ![WebPage](/help/assets/icons/WebPage.svg) | **[!UICONTROL 패널]** | [패널](/help/analyze/analysis-workspace/c-panels/panels.md)은 프로젝트 내에서 분석을 구성하는 데 사용되며 많은 테이블과 시각화를 포함할 수 있습니다. Analysis Workspace에서 제공되는 많은 패널은 몇 개의 사용자 입력을 기반으로 전체 분석 집합을 생성합니다. |
| ![GraphBarVertical](/help/assets/icons/GraphBarVertical.svg) | **[!UICONTROL 시각화]** | 막대 또는 선 차트와 같은 [시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)를 사용하여 데이터를 시각적으로 생동감 있게 표현할 수 있습니다. 맨 왼쪽 패널에서 가운데 **[!UICONTROL 시각화]** 아이콘을 선택하여 시각화의 전체 목록을 확인합니다. |
| ![Curate](/help/assets/icons/Curate.svg) | **[!UICONTROL 구성 요소]** | [구성 요소](/help/components/home.md)에는 다음 요소가 포함됩니다.<ul><li>![Dimensions](/help/assets/icons/Dimensions.svg) [차원](/help/components/dimensions/overview.md)</li><li>![Event](/help/assets/icons/Event.svg) [지표](/help/analyze/analysis-workspace/components/apply-create-metrics.md)</li><li>![세분화](/help/assets/icons/Segmentation.svg) [세그먼트](/help/components/segmentation/seg-overview.md)</li><li>![Calendar](/help/assets/icons/Calendar.svg) [날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)</li></ul> |
| ![ViewList](/help/assets/icons/ViewList.svg) | **[!UICONTROL 목차]** | [목차](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md)가 프로젝트에 포함된 모든 패널 및 시각화를 축소 가능한 목록으로 구성하면 특정 패널이나 시각화에 빠르게 액세스할 수 있습니다. |
| ![Bookmark](/help/assets/icons/Bookmark.svg) | **데이터 사전** | [데이터 사전](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)은 사용자와 관리자 모두 Analytics 환경의 구성 요소를 계속 파악하고 더 잘 이해할 수 있도록 도와줍니다. |


## 메뉴

Analysis Workspace의 기능 대부분은 드래그 앤 드롭을 통해, 패널, 시각화 및 구성 요소 내 컨텍스트 메뉴를 통해 사용할 수 있습니다.

Workspace 메뉴 및 단축키 또는 핫키를 통해서도 기능을 사용할 수 있습니다. 단축키는 브라우저가 실행 중인 운영 체제에 따라 다릅니다. 개요는 아래 테이블을 참조하십시오.

키보드에서 다음 기호를 사용해야 합니다.

- **[!UICONTROL *Shift *]**의 경우**⇧**
- **⌘****[!UICONTROL *Cmd *]**(명령)의 경우.
- **⌃****[!UICONTROL *Ctrl *]**(제어)의 경우.
- **⌥****[!UICONTROL *Opt *]**(옵션)의 경우.
- **⎇****[!UICONTROL *Alt *]**(대체)의 경우.

사용 가능한 메뉴 개요는 아래 테이블을 참조하십시오.

| **[!UICONTROL 프로젝트]** | 단축키 Mac | 단축키 Windows | 설명 |
|---|---|---|---|
| **[!UICONTROL 프로젝트 만들기]** | **[!UICONTROL *Shift+Cmd+P *]** | **[!UICONTROL *Shift+Ctrl+P *]** | 새 프로젝트를 만듭니다. |
| **[!UICONTROL 모바일 스코어카드 만들기]** | | | [새 모바일 스코어카드 만들기](/help/analyze/mobile-app/create-scorecard.md). |
| **[!UICONTROL 열기...]** | **[!UICONTROL *Cmd+O *]** | **[!UICONTROL *Ctrl+O *]** | [기존 프로젝트 열기](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#open-another-project). |
| **[!UICONTROL 이전 버전 열기...]** | **[!UICONTROL *Opt+Cmd+O *]** | **[!UICONTROL *Alt+Ctrl+O *]** | [이전 버전의 프로젝트 열기](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#open-previous-version). |
| **[!UICONTROL 저장]** | **[!UICONTROL *Cmd+S *]** | **[!UICONTROL *Ctrl+S *]** | [프로젝트 저장](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#save-projects). |
| **[!UICONTROL 메모와 함께 저장...]** | **[!UICONTROL *Opt+Cmd+S *]** | **[!UICONTROL *Alt+Ctrl+S *]** | [저장한 프로젝트 버전에 메모 추가](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#save-project-options). |
| **[!UICONTROL 다른 이름으로 저장...]** | **[!UICONTROL *Shift+Cmd+S *]** | **[!UICONTROL *Shift+Ctrl+S *]** | [다른 이름 및 세부 정보를 사용하여 프로젝트를 저장합니다.](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#save-project-options) |
| **[!UICONTROL 프로젝트 새로 고침]** | **[!UICONTROL *Opt+R *]** | **[!UICONTROL *Alt+R *]** | 프로젝트 새로 고침 |
| **[!UICONTROL CSV 다운로드]** | **[!UICONTROL *Shift+Cmd+V *]** | **[!UICONTROL *Shift+Ctrl+V *]** | 프로젝트를 CSV 파일로 다운로드합니다. |
| **[!UICONTROL PDF 다운로드]** | **[!UICONTROL *Shift+Cmd+B *]** | **[!UICONTROL *Shift+Ctrl+B *]** | 프로젝트를 PDF 문서로 다운로드합니다. |
| **[!UICONTROL 프로젝트 정보 및 설정]** | | | 이름, 태그, 색상 팔레트 등과 같은 프로젝트의 설정을 정의합니다. |
| **[!UICONTROL 사용자 설정]** | | | [Analysis Workspace 사용에 대한 환경 설정을 구성합니다](/help/analyze/analysis-workspace/user-preferences.md). |


| **[!UICONTROL 편집]** | 단축키 Mac | 단축키 Windows | 설명 |
|---|---|---|---|
| **[!UICONTROL 실행 취소]** | **[!UICONTROL *Cmd+Z *]** | **[!UICONTROL *Ctrl+Z *]** | 이전 액션을 실행 취소합니다. |
| **[!UICONTROL 다시 실행]** | **[!UICONTROL *Cmd+Shift+Z *]** | **[!UICONTROL *Ctrl+Shift+Z *]** | 이전 액션을 다시 실행합니다. |
| **[!UICONTROL 모두 지우기]** | **[!UICONTROL *Opt+W *]** | **[!UICONTROL *Alt+W *]** | 현재 프로젝트의 패널을 모두 지웁니다. |

| **[!UICONTROL 삽입]** | 단축키 Mac | 단축키 Windows | 설명 |
|---|---|---|---|
| **[!UICONTROL 빈 패널]** | **[!UICONTROL *Opt+B *]** | **[!UICONTROL *Alt+B *]** | [빈 패널](/help/analyze/analysis-workspace/c-panels/blank-panel.md)을 삽입합니다. |
| **[!UICONTROL 미디어 동시 뷰어]** | **[!UICONTROL *Opt+H *]** | **[!UICONTROL *Alt-H *]** | [미디어 동시 뷰어](/help/analyze/analysis-workspace/c-panels/media-concurrent-viewers.md) 패널을 삽입합니다. |
| **[!UICONTROL 미디어 재생 체류 시간]** | **[!UICONTROL *Opt+I *]** | **[!UICONTROL *Alt+I *]** | [미디어 재생 체류 시간](/help/analyze/analysis-workspace/c-panels/media-playback-time-spent.md) 패널을 삽입합니다. |
| **[!UICONTROL 미디어 평균 분당 시청 대상자]** | **[!UICONTROL *Opt+M *]** | **[!UICONTROL *Alt+M *]** | [미디어 평균 분당 시청 대상자](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md) 패널을 삽입합니다. |
| **[!UICONTROL 속성]** | **[!UICONTROL *Opt+E *]** | **[!UICONTROL *Alt+E *]** | [속성](/help/analyze/analysis-workspace/c-panels/attribution.md) 패널을 삽입합니다. |
| **[!UICONTROL 자유 형식]** | **[!UICONTROL *Opt+A *]** | **[!UICONTROL *Alt+A *]** | [자유 형식](/help/analyze/analysis-workspace/c-panels/freeform-panel.md) 패널을 삽입합니다. |
| **[!UICONTROL 빠른 인사이트]** | **[!UICONTROL *Opt+J *]** | **[!UICONTROL *Alt+J *]** | [빠른 인사이트](/help/analyze/analysis-workspace/c-panels/quickinsight.md) 패널을 삽입합니다. |
| **[!UICONTROL 자유 형식 테이블]** | **[!UICONTROL *Opt+1 *]** | **[!UICONTROL *Alt+1 *]** | [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) 시각화를 삽입합니다. |
| **[!UICONTROL 라인]** | **[!UICONTROL *Opt+2 *]** | **[!UICONTROL *Alt+2 *]** | [라인](/help/analyze/analysis-workspace/visualizations/line.md) 시각화를 삽입합니다. |
| **[!UICONTROL 막대]** | **[!UICONTROL *Opt+3 *]** | **[!UICONTROL *Alt+3 *]** | [막대](/help/analyze/analysis-workspace/visualizations/bar.md) 시각화를 삽입합니다. |
| **[!UICONTROL 콤보]** | **[!UICONTROL *Opt+4 *]** | **[!UICONTROL *Alt+4 *]** | [ 콤보](/help/analyze/analysis-workspace/visualizations/combo-charts.md) 시각화를 삽입하다. |


| **[!UICONTROL 구성 요소]** | 단축키 Mac | 단축키 Windows | 설명 |
|---|---|---|---|
| **[!UICONTROL 세그먼트 만들기...]** | **[!UICONTROL *Shift+Cmd+E *]** | **[!UICONTROL *Shift+Ctrl+E *]** | 새 [세그먼트](/help/components/segmentation/segmentation-workflow/seg-create.md)를 만듭니다. |
| **[!UICONTROL 지표 만들기...]** | **[!UICONTROL *Shift+Cmd+C *]** | **[!UICONTROL *Shift+Ctrl+C *]** | 새 [계산된 지표](/help/components/calculated-metrics/cm-overview.md)를 만듭니다. |
| **[!UICONTROL 날짜 범위 만들기...]** | **[!UICONTROL *Shift+Cmd+D *]** | **[!UICONTROL *Shift+Ctrl+D *]** | 새 [날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)를 만듭니다. |
| **[!UICONTROL 주석 만들기...]** | **[!UICONTROL *Shift+Cmd+O *]** | **[!UICONTROL *Shift+Ctrl+O *]** | 새 [주석](/help/analyze/analysis-workspace/components/annotations/overview.md)을 만듭니다. |
| **[!UICONTROL 구성 요소 새로 고침]** | **[!UICONTROL *Opt+Shift+R *]** | **[!UICONTROL *Alt+Shift+R *]** | 프로젝트의 구성 요소를 새로 고칩니다. |

| **[!UICONTROL 공유]** | 단축키 Mac | 단축키 Windows | 설명 |
|---|---|---|---|
| **[!UICONTROL Workspace 사용자와 공유]** | **[!UICONTROL *Cmd+H *]** | **[!UICONTROL *Ctrl+H *]** | [다른 Workspace 사용자와 프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-with-customer-journey-analytics-users-and-groups-in-your-organization). |
| **[!UICONTROL 모두와 공유]** | **[!UICONTROL *Opt+L *]** | **[!UICONTROL *Alt+L *]** | [모두와 읽기 전용 버전의 프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-a-link-to-a-project). |
| **[!UICONTROL 파일 보내기]** | **[!UICONTROL Opt+S]** | **[!UICONTROL *Alt+S *]** | [프로젝트를 다른 수신자에게 CSV 또는 PDF 파일로 전송](/help/analyze/analysis-workspace/curate-share/send-schedule-files.md). |
| **[!UICONTROL 파일 내보내기 예약]** | **[!UICONTROL *Shift+Opt+S *]** | **[!UICONTROL *Shift+Alt+S *]** | [프로젝트를 다른 수신자에게 일정에 따라 CSV 또는 PDF로 전송](/help/analyze/analysis-workspace/curate-share/send-schedule-files.md). |
| **[!UICONTROL 프로젝트 데이터 조정]** | **[!UICONTROL *Shift+Cmd+G *]** | **[!UICONTROL *Shift+Ctrl+G *]** | [프로젝트 데이터 조정](/help/analyze/analysis-workspace/curate-share/curate.md). |

| 도움말 | 설명 |
|---|---|
| **[!UICONTROL 비디오]** | 새 브라우저 탭에서 Customer Journey Analytics YouTube 채널을 엽니다. |
| **[!UICONTROL 도움말 설명서]** | 새 브라우저 탭에서 설명서(실제로 방금 읽은 문서...)를 엽니다. |
| **[!UICONTROL 도움말 포럼]** | 새 브라우저 탭에서 Adobe Analytics Experience League 커뮤니티 포럼을 엽니다. |
| **[!UICONTROL 핫키]** | Workspace에서 사용할 수 있는 핫키(단축키)에 대한 개요를 표시합니다. |
| **[!UICONTROL 디버거 활성화]** | 디버거를 활성화합니다. 프로젝트가 다시 로드됩니다. |
| **[!UICONTROL 디버거 비활성화]** | 디버거를 비활성화합니다. 프로젝트가 다시 로드됩니다. |
| **[!UICONTROL 성능]** | **[!UICONTROL Analysis Workspace]** 성능의 지표를 보여 주는 대화 상자를 표시합니다. **[!UICONTROL CSV로 다운로드]**&#x200B;를 사용하여 성과 지표의 CSV 파일을 다운로드합니다. |
| **[!UICONTROL Workspace 정보 페이지]** | 버전 정보, 기능 액세스 수준 및 활성 기능 플래그와 함께 **[!UICONTROL Analysis Workspace 정보 페이지]** 대화 상자를 표시합니다. |

## 데이터 소스

시각화를 동기화하여 시각화에 해당하는 데이터 테이블 또는 데이터 소스를 제어합니다. 자세한 내용은 [데이터 소스 관리](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md)를 참조하십시오.

## Analysis Workspace 사용


Analysis Workspace를 시작하는 방법:

1. [Adobe Experience Cloud](https://experience.adobe.com)에 로그인합니다.
1. 인터페이스 오른쪽 상단에 있는 앱 전환기 ![App](/help/assets/icons/Apps.svg)에서 **[!UICONTROL Customer Journey Analytics]**&#x200B;를 선택합니다.
1. Analysis Workspace의 **[!UICONTROL 프로젝트]** 페이지가 기본적으로 표시됩니다. 특정 프로젝트를 선택했거나 최근 작업 중인 경우 해당 프로젝트가 기본적으로 표시됩니다.

### 프로젝트를 만듭니다.

Analysis Workspace에서 분석은 [프로젝트](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)라고 합니다.

[프로젝트 만들기](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)에 설명된 대로 Analysis Workspace에서 프로젝트를 만들 수 있습니다.

[Analysis Workspace의 폴더](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)에 설명된 대로 프로젝트를 폴더와 하위 폴더로 구성할 수 있습니다.

### 프로젝트 저장 및 공유

Analysis Workspace에서 분석을 만들면 작업이 [자동으로 저장됩니다](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md).

프로젝트 빌드를 완료하고 프로젝트에서 실행 가능한 인사이트를 수집하면 다른 사람이 프로젝트를 사용할 수도 있습니다. 조직의 사용자 및 그룹은 물론 조직 외부의 사람들과도 프로젝트를 공유할 수 있습니다. 프로젝트 공유에 대한 내용은 [프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md)를 참조하십시오.

## 추가 리소스 {#resources}

- Adobe는 수백 개의 [Analytics 비디오 교육 튜토리얼](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/overview)을 제공합니다.
- 새 기능을 위한 업데이트에 대해서는 [Adobe Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/ko/docs/release-notes/experience-cloud/current)를 참조하십시오.



<!--
# Analysis Workspace overview {#analysis-workspace-overview}

Analysis Workspace allows you to build analyses quickly to gather insights and then share those insights with others. Using the drag-and-drop browser interface, you can craft your analysis, add visualizations to bring data to life, curate a dataset, and share and schedule [projects](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) with anyone you choose.

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Analysis workspace overview](https://video.tv.adobe.com/v/35560/?captions=kor&quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

## Interface

The following image and accompanying table explain the main elements in the Analysis Workspace user interface:

![Analysis Workspace window highlighting the various sections of the interface](assets/analysis-workspace-overview.png)

| Location | Name and function |
|:---------:|----------|
| A | Contains the name of the project, a menu structure to access functionality, a button ![Back button](/help/assets/icons/ChevronLeft.svg) to return back to your Project list, and a **[!UICONTROL Share]** button to [share your Workspace project](/help/analyze/analysis-workspace/curate-share/share-projects.md). <br/>Select the name of your project (for example: New project) at any time to change the name. <br/>Select ![Unfavor](/help/assets/icons/StarOutline.svg) to mark your project as a favorite project ![Favor](/help/assets/icons/Star.svg). |
| B | **Button panel:** Contains buttons for accessing the key [features](#features) of Analysis Workspace:<ul><li>![WebPage](/help/assets/icons/WebPage.svg) [[!UICONTROL Panels]](/help/analyze/analysis-workspace/c-panels/panels.md)</li><li>![Guided Analysis](/help/assets/icons/GuidedAnalysis.svg) [[!UICONTROL Guided Analysis]](/help/guided-analysis/overview.md)</li><li>![GraphBarVertical](/help/assets/icons/GraphBarVertical.svg) [[!UICONTROL Visualizations]](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</li><li>![Curate](/help/assets/icons/Curate.svg) [[!UICONTROL Components]](/help/components/overview.md)</li><li>![ViewList](/help/assets/icons/ViewList.svg) [[!UICONTROL Table of contents]](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md)</li><li>![Bookmark](/help/assets/icons/Bookmark.svg) [[!UICONTROL Data Dictionary]](/help/components/data-dictionary/data-dictionary-overview.md)</li></ul> |
| C | **Left panel:** This area contains individual panels, visualizations, components, or lists. The content depends on the button selected in the button panel.  |
| D | **Canvas:** The main area where you drag content from the left panel to build your project. The project dynamically updates as you add panels, add visualizations to panels, and add components to visualizations. You can create multiple panels, and within each panel you can create multiple visualizations.<br/>Each panel is based on a selected data view. The selected data view determines available components like metrics and dimensions. See [Panels - Data view](/help/analyze/analysis-workspace/c-panels/panels.md#data-view) for more information. |

## Features

The key features of Analysis Workspace are available through the button panel:

| Icon | Feature | Description |
|:---:|---|---|
| ![WebPage](/help/assets/icons/WebPage.svg) | **[!UICONTROL Panels]** | [Panels](/help/analyze/analysis-workspace/c-panels/panels.md) are used to organize your analysis within a project and can contain many tables & visualizations. Many of the panels provided in Analysis Workspace generate a full set of analyses based on a few user inputs. |
| ![Guided Analysis](/help/assets/icons/GuidedAnalysis.svg) | **[!UICONTROL Guided Analysis]** | [Guided analysis](../guided-analysis/overview.md) allows you to self-serve high quality data and insights about the customer journey through guided workflows. You can create an analysis for inclusion in your Workspace project, or include an existing analysis previously saved. |
| ![GraphBarVertical](/help/assets/icons/GraphBarVertical.svg) | **[!UICONTROL Visualizations]** | [Visualizations](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md), such as a bar or line chart, can be used to bring data visually to life. On the far left panel, select the middle **[!UICONTROL Visualizations]** icon to see the full list of visualizations available. |
| ![Curate](/help/assets/icons/Curate.svg) | **[!UICONTROL Components]** | [Components](/help/components/overview.md) include the following elements:<ul><li>![Dimensions](/help/assets/icons/Dimensions.svg) [Dimensions](/help/components/dimensions/overview.md)</li><li>![Event](/help/assets/icons/Event.svg) [Metrics](/help/components/apply-create-metrics.md)</li><li>![Segmentation](/help/assets/icons/Segmentation.svg) [Segments](/help/components/segments/seg-overview.md)</li><li>![Calendar](/help/assets/icons/Calendar.svg) [Date ranges](/help/components/date-ranges/overview.md)</li></ul> |
| ![ViewList](/help/assets/icons/ViewList.svg) | **[!UICONTROL Table of contents]** | The table of contents organizes all panels and visualizations included in the project into a collapsible list, allowing you to access a specific panel or visualization quickly. |
|![Bookmark](/help/assets/icons/Bookmark.svg) | **Data dictionary** | The [Data dictionary](/help/components/data-dictionary/data-dictionary-overview.md) helps both users and administrators keep track of and better understand the components in their Analytics environment. |


## Menu

Most of the functionality of Analysis Workspace is available through drag and drop, and trough context menus within panels, visualizations and components.

Functionality is also available through the Workspace menu and shortcuts or hotkeys. Shortcut keys differ depending on the operating system that your browser is running on. See the tables below for an overview.  

Note that on your keyboard the following symbols might be used:

- **⇧** for **[!UICONTROL *shift*]**.
- **⌘** for **[!UICONTROL *cmd*]** (command).
- **⌃** for **[!UICONTROL *ctrl*]** (control).
- **⌥** for **[!UICONTROL *opt*]** (option).
- **⎇** for **[!UICONTROL *alt*]** (alternate).

See the tables below for an overview of the available menus.  

| **[!UICONTROL Project]** | Shortcut Mac | Shortcut Windows | Description |
|---|---|---|---|
| **[!UICONTROL Create project]** | **[!UICONTROL *shift+cmd+p*]** | **[!UICONTROL *shift+ctrl+p*]** | Create a new project. |
| **[!UICONTROL Create a mobile scorecard]** | | | [Create a new mobile scorecard](/help/mobile-app/create-scorecard.md). |
| **[!UICONTROL Open...]** | **[!UICONTROL *cmd+o*]** | **[!UICONTROL *ctrl+o*]** | [Open an existing project](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#open-another-project). |
| **[!UICONTROL Open previous version...]** | **[!UICONTROL *opt+cmd+o*]** | **[!UICONTROL *alt+ctrl+o*]** | [Open earlier versions of your project](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#open-previous-version). |
| **[!UICONTROL Save]** | **[!UICONTROL *cmd+s*]** | **[!UICONTROL *ctrl+s*]** | [Save your project](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#save-projects). |
| **[!UICONTROL Save with notes...]** | **[!UICONTROL *opt+cmd+s*]** | **[!UICONTROL *alt+ctrl+s*]** | [Add notes to the project version that you save](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#save-project-options). |
| **[!UICONTROL Save as...]** | **[!UICONTROL *shift+cmd+s*]** | **[!UICONTROL *shift+ctrl+s*]** | [Save the project using a different name and details](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md#save-project-options). |
| **[!UICONTROL Refresh project]** | **[!UICONTROL *opt+r*]** | **[!UICONTROL *alt+r*]** | Refresh the project. |
| **[!UICONTROL Download CSV]** | **[!UICONTROL *shift+cmd+v*]** | **[!UICONTROL *shift+ctrl+v*]** | Download the project as a CSV file. |
| **[!UICONTROL Download PDF]**| **[!UICONTROL *shift+cmd+b*]** | **[!UICONTROL *shift+ctrl+b*]** | Download the project as a PDF document. |
| **[!UICONTROL Project info & settings]** | | | Define settings for your projects, such as name, tags, color palette, and more. |
| **[!UICONTROL User settings]** | | | [Configure preferences for using Analysis Workspace](/help/analyze/analysis-workspace/user-preferences.md). |


| **[!UICONTROL Edit]** | Shortcut Mac | Shortcut Windows | Description |
|---|---|---|---|
| **[!UICONTROL Undo]** | **[!UICONTROL *cmd+z*]** | **[!UICONTROL *ctrl+z*]** | Undo the previous action. |
| **[!UICONTROL Redo]** | **[!UICONTROL *cmd+shift+z*]** | **[!UICONTROL *ctrl+shift+z*]** | Redo the previous action. |
| **[!UICONTROL Clear all]** | **[!UICONTROL *opt+w*]** | **[!UICONTROL *alt+w*]** | Clear all panels in the current project. |

| **[!UICONTROL Insert]** | Shortcut Mac | Shortcut Windows | Description |
|---|---|---|---|
| **[!UICONTROL Blank panel]** | **[!UICONTROL *opt+b*]** | **[!UICONTROL *alt+b*]** |  Insert a [Blank panel](/help/analyze/analysis-workspace/c-panels/blank-panel.md). |
| **[!UICONTROL Media concurrent viewers]** | **[!UICONTROL *opt+h*]** | **[!UICONTROL *alt-h*]** |  Insert a [Media concurrent viewers](/help/analyze/analysis-workspace/c-panels/media-concurrent-viewers.md) panel. |
| **[!UICONTROL Media playback time spent]** | **[!UICONTROL *opt+i*]** | **[!UICONTROL *alt+i*]** |  Insert a [Media playback time spent](/help/analyze/analysis-workspace/c-panels/media-playback-time-spent.md) panel. |
| **[!UICONTROL Media average minute audience]** | **[!UICONTROL *opt+m*]** | **[!UICONTROL *alt+m*]** |  Insert a [Media average minute audience](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md) panel. |
| **[!UICONTROL Attribution]** | **[!UICONTROL *opt+e*]** | **[!UICONTROL *alt+e*]** |  Insert an [Attribution](/help/analyze/analysis-workspace/c-panels/attribution.md) panel. |
| **[!UICONTROL Freeform]** | **[!UICONTROL *opt+a*]** | **[!UICONTROL *alt+a*]** |  Insert a [Freeform](/help/analyze/analysis-workspace/c-panels/freeform-panel.md) panel. |
| **[!UICONTROL Quick insights]** | **[!UICONTROL *opt+j*]** | **[!UICONTROL *alt+j*]** |  Insert a [Quick insights](/help/analyze/analysis-workspace/c-panels/quickinsight.md) panel. |
| **[!UICONTROL Experimentation]** |**[!UICONTROL *opt+x*]** | **[!UICONTROL *alt+x*]** |  Insert an [Experimentation](/help/analyze/analysis-workspace/c-panels/experimentation.md) panel. |
| **[!UICONTROL Freeform table]** | **[!UICONTROL *opt+1*]** | **[!UICONTROL *alt+1*]**|  Insert a [Freeform table](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) visualization. |
| **[!UICONTROL Line]** | **[!UICONTROL *opt+2*]** | **[!UICONTROL *alt+2*]** |  Insert a [Line](/help/analyze/analysis-workspace/visualizations/line.md) visualization. |
| **[!UICONTROL Bar]** | **[!UICONTROL *opt+3*]** | **[!UICONTROL *alt+3*]** |  Insert a [Bar](/help/analyze/analysis-workspace/visualizations/bar.md) visualization. |
| **[!UICONTROL Combo]** | **[!UICONTROL *opt+4*]**| **[!UICONTROL *alt+4*]** |  Insert a [Combo](/help/analyze/analysis-workspace/visualizations/combo-charts.md) visualization. |


| **[!UICONTROL Components]** | Shortcut Mac | Shortcut Windows | Description |
|---|---|---|---|
| **[!UICONTROL Create segment...]** | **[!UICONTROL *shift+cmd+e*]** | **[!UICONTROL *shift+ctrl+e*]** | Create a new [segment](/help/components/segments/seg-create.md). |
| **[!UICONTROL Create metric...]** | **[!UICONTROL *shift+cmd+c*]** | **[!UICONTROL *shift+ctrl+c*]** | Create a new [calculated metric](/help/components/calc-metrics/calc-metr-overview.md). |
| **[!UICONTROL Create date range...]** | **[!UICONTROL *shift+cmd+d*]** | **[!UICONTROL *shift+ctrl+d*]** | Create a new [date range](/help/components/date-ranges/overview.md). |
| **[!UICONTROL Create annotation...]** | **[!UICONTROL *shift+cmd+o*]** | **[!UICONTROL *shift+ctrl+o*]** | Create a new [annotation](/help/components/annotations/overview.md). |
| **[!UICONTROL Create audience...]** | **[!UICONTROL *shift+cmd+u*]** | **[!UICONTROL *shift+ctrl+u*]** | Create a new [audience](/help/components/audiences/audiences-overview.md). |
| **[!UICONTROL Refewsh components]** | **[!UICONTROL *opt+shift+r*]** | **[!UICONTROL *alt+shift+r*]** | Refresh the components in the project. |

| **[!UICONTROL Share]** | Shortcut Mac | Shortcut Windows | Description |
|---|---|---|---|
| **[!UICONTROL Share with Workspace users]** | **[!UICONTROL *cmd+h*]** | **[!UICONTROL *ctrl+h*]** | [Share the project with other Workspace users](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-with-customer-journey-analytics-users-and-groups-in-your-organization). |
| **[!UICONTROL Share with anyone]** | **[!UICONTROL *opt+l*]** | **[!UICONTROL *alt+l*]**| [Share a read-only version of the project with anyone](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-a-link-to-a-project). |
| **[!UICONTROL Send file]** | **[!UICONTROL opt+s]** | **[!UICONTROL *alt+s*]** | [Send the project as a CSV or PDF file to other recipients](/help/analyze/analysis-workspace/curate-share/send-schedule-files.md). |
| **[!UICONTROL Schedule file export]** | **[!UICONTROL *shift+opt+s*]** | **[!UICONTROL *shift+alt+s*]** | [Send the project on a schedule as a CSV or PDF file to other recipients](/help/analyze/analysis-workspace/curate-share/send-schedule-files.md). |
| **[!UICONTROL Curate project data]** | **[!UICONTROL *shift+cmd+g*]** | **[!UICONTROL *shift+ctrl+g*]** | [Curate the project data](/help/analyze/analysis-workspace/curate-share/curate.md). |

| Help | Shortcut Mac | Shortcut Windows | Description |
|---|---|---|---|
| **[!UICONTROL Videos]** | | | Open the Customer Journey Analytics YouTube channel in a new browser tab. |
| **[!UICONTROL Help documentation]** | | | Open the documentation (you are actually reading just now...) in a new browser tab. |
| **[!UICONTROL Help forum]** | | | Open the Adobe Analytics Experience League communities forum in a new browser tab. |
| **[!UICONTROL Hotkeys]** | | | Show an overview of the hotkeys (shortcuts) you can use in Workspace. |
| **[!UICONTROL Enable debugger]** |  | | Enable the debugger. Your project will reload. |
| **[!UICONTROL Disable debugger]** | | | Disable the debugger. Your project will reload. |
| **[!UICONTROL Performance]** | | | Show a dialog displaying metrics on the **[!UICONTROL Analysis Workspace performance]**. Use **[!UICONTROL Download as CSV]** to download a CSV file of the performance metrics. |
| **[!UICONTROL About Workspace]** | | | Show an **[!UICONTROL About Analysis Workspace]** dialog with version information, feature access levels and active feature flags. |

## Data sources

You synchronize visualizations to control which data table or data source corresponds to a visualization. See [manage data sources](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md) for more information.

## Use Analysis Workspace


To start using Analysis Workspace: 

1. Log in to [Adobe Experience Cloud](https://experience.adobe.com).
1. Select **[!UICONTROL Customer Journey Analytics]** from the app switcher ![App](/help/assets/icons/Apps.svg) at the top right of the interface.
1. The **[!UICONTROL Projects]** page of Analysis Workspace is shown by default. If a specific project has been selected for you or you have been working on recently, then that project is shown by default.

### Create a project

An analysis in Analysis Workspace is referred to as a [project](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md). 

You can create a project in Analysis Workspace as described in [Create projects](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md).

Projects can be organized into folders and subfolders, as described in [Folders in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md).

### Save and share a project

As you create an analysis in Analysis Workspace, your work is [automatically saved](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md). 

When you finish building out the project and it's gathering actionable insights, others might want to consume the project. You can share the project with users and groups in your organization, or even with people outside your organization. For information about sharing a project, see [Share projects](/help/analyze/analysis-workspace/curate-share/share-projects.md).

## Additional resources {#resources}

- The [Learning landing](/help/getting-started/landing.md#learning) page in Customer Journey Analytics. This page is  great way to become acquainted with Analysis Workspace. Especially the Learning Workspace Fundamental. This template walks you through common terminology and steps for building your first analysis in Workspace
- Adobe offers hundreds of [Analytics video training tutorials](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/overview).
- See [Adobe Experience Cloud release notes](https://experienceleague.adobe.com/ko/docs/release-notes/experience-cloud/current) for updates about new features.



<!--
# Analysis Workspace overview

Analysis Workspace allows you to quickly build analyses to gather insights and then share those insights with others. Using the drag-and-drop browser interface, you can craft your analysis, add visualizations to bring data to life, curate a dataset, and share and schedule projects with anyone you choose.

The following video provides a brief overview with examples of what is possible.


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Analysis Workspace overview](https://video.tv.adobe.com/v/35560/?captions=kor&quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

## Areas of Analysis Workspace

The following image and accompanying table explain some of the main areas in Analysis Workspace:

![Analysis Workspace overview](assets/analysis-workspace-overvew.png)

| Location in image | Name and function |
|---------|----------|
| A | **Far left rail:** Contains tabs for adding panels, visualizations, and components to Analysis Workspace. Also contains the Data Dictionary icon that is used to open the Data Dictionary. |
| B | **Left rail:** Depending on which tab is selected in the far left rail, this area contains individual panels, visualizations, or components. |
| C | **Canvas:** This is the main area where you drag content from the left rails to build your project. The project dynamically updates as you add panels, visualizations, and components to the canvas. |
| D | **Report suite drop-down menu:** For each panel in Analysis Workspace, the report suite drop-down menu allows you to choose the report suite that you want to use as your data source. |

## Features in Analysis Workspace {#analysis}

Following are some of the key features available in Analysis Workspace: 

### Panels

**Panels** are used to organize your analysis within a project and can contain many tables & visualizations. Many of the panels provided in Analysis Workspace generate a full set of analyses based on a few user inputs. On the far left rail, select the top **[!UICONTROL Panels]** icon to see a full list of panels available.

To learn more about panels, see [Panels overview](/help/analyze/analysis-workspace/c-panels/panels.md).

![](assets/build-panels.png)

### Visualizations

**Visualizations**, such as a bar or line chart, can be used to visually bring data to life. On the far left rail, select the middle **[!UICONTROL Visualizations]** icon to see the full list of visualizations available. 

To learn more about visualizations, see [Visualizations overview](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).

![](assets/build-visualizations.png)

### Components

Components in Analysis Workspace consist of the following:

* Dimensions

* Metrics

* Segments

* Date ranges

To learn more about each of these component types, see [Components overview](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). 

Each of these component types can be added to a visualization (such as a Freeform table) to start answering your business questions. 

After you understand component terminology, you can drag components into visualizations (including Freeform tables) to [build your analysis](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).

![](assets/build-components.png)

### Data Dictionary

The Data Dictionary in Analysis Workspace helps both users and administrators keep track of and better understand the components in their Analytics environment.

To learn more about the Data Dictionary, see [Data Dictionary overview](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md).

### Data Sources

Synchronizing visualizations lets you control which data table or data source corresponds to a visualization. Here is more information on how you can [manage data sources](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md).

## Start using Analysis Workspace

### Log in to Adobe Analytics {#login}

To start using Analysis Workspace, log in to Adobe Analytics by going to [experience.adobe.com/analytics](https://experience.adobe.com/analytics). The Projects page of Analysis Workspace is shown by default. If a specific project has been selected for you, that project is shown by default.

### Create a project {#new-project}

An analysis in Analysis Workspace is referred to as a [project](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).  

You can create a project in Analysis Workspace as described in [Create projects](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md).

Projects can be organized into folders and subfolders, as described in [Folders in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md).

### Save and share a project

As you create an analysis in Analysis Workspace, your work is [automatically saved](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md). 

When you finish building out the project and it's gathering actionable insights, the project is ready to be consumed by others. You can share the project with users and groups in your organization, or even with people outside your organization. For information about sharing a project, see [Share projects](/help/analyze/analysis-workspace/curate-share/share-projects.md).

## Additional resources {#resources}

* Adobe offers hundreds of [Analytics video training tutorials](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/overview.html?lang=ko).
* See [Adobe Experience Cloud release notes](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko#analytics) for updates about new features.
* A great way to become acquainted with Analysis Workspace is through the Analysis Workspace Training Tutorial template. This template walks you through common terminology and steps for building your first analysis in Workspace. To begin the tutorial:
  1. On the [!UICONTROL **Workspace**] tab in Adobe Analytics, select **[!UICONTROL Learning]** on the left.
  1. Select **[!UICONTROL Open Tutorial]**.
     ![](assets/training-tutorial.png)

-->