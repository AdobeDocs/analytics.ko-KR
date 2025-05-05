---
description: Workspace 프로젝트 작업의 기초 배우기.
keywords: Analysis Workspace
title: 프로젝트 개요
feature: Workspace Basics
role: User, Admin
exl-id: 75c551de-297e-4c45-95e6-77472be6628a
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 43%

---

# 프로젝트 개요

Workspace 프로젝트를 사용하면 데이터 구성 요소, 테이블 및 시각화를 결합하여 분석을 작성하고 조직의 모든 사람과 공유할 수 있습니다. 첫 번째 프로젝트를 시작하기 전에 프로젝트에 액세스, 탐색 및 관리하는 방법에 대해 살펴보십시오.

다음은 Workspace 프로젝트 빌드 방법에 대한 비디오입니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Workspace 프로젝트 빌드](https://video.tv.adobe.com/v/3415640?quality=12&learn=on&captions=kor){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]


## 프로젝트 목록 {#project-list}

처음 **[!UICONTROL Analytics]** > **[!UICONTROL Workspace]**&#x200B;로 이동하면 페이지에 사용자가 보유하거나 사용자와 공유된 모든 프로젝트가 나열됩니다. 이전에 사용자 지정 랜딩 페이지를 설정한 경우가 아니라면 이 페이지는 Adobe Analytics의 랜딩 페이지이기도 합니다.

프로젝트 페이지에는 다음 정보가 포함되어 있습니다.

| 요소 | 설명 |
|---|---|
| [환경 설정 편집](/help/analyze/analysis-workspace/user-preferences.md) | 사용자가 만드는 모든 새 프로젝트 또는 패널에 대한 Analysis Workspace 및 관련 구성 요소의 설정을 관리합니다. |
| [폴더 만들기](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/create-folders.md) | 프로젝트 및 폴더 목록에 새 폴더 또는 하위 폴더를 추가합니다. |
| [프로젝트 제작](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md) | 처음부터 또는 보고서에서 새 프로젝트를 시작합니다. |
| 자세히 보기 | 이 옵션을 선택하면 빈 프로젝트 또는 모바일 스코어카드를 만들거나 [교육 튜토리얼을 보거나](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/analysis-workspace-basics/analysis-workspace-introduction) 또는 [릴리스 정보를 보는](/help/release-notes/latest.md)에 대한 옵션이 표시됩니다. |
| ![필터 표시](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg) | 필터를 표시하거나 숨깁니다. 태그, 보고서 세트, 소유자, 유형(프로젝트, 폴더, 모바일 스코어카드) 및 기타 필터를 필터링할 수 있습니다. |
| ![Search](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) | 검색 필드를 사용하여 폴더, Workspace 프로젝트 또는 모바일 스코어카드를 검색합니다. |
| 폴더 및 프로젝트 표시 | 프로젝트의 폴더 구조를 표시할지 여부를 선택합니다. 자세한 내용은 [Analytics의 폴더 정보](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)를 참조하십시오. |
| ![표 사용자 지정](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg) | 이 아이콘을 사용하면 프로젝트 목록의 각 프로젝트에 대해 표시되는 열을 사용자 지정할 수 있습니다. |

프로젝트 목록에는 다음 열이 표시될 수 있습니다.

| 열 | 설명 |
|---|---|
| [!UICONTROL 이름] | Workspace 프로젝트의 이름입니다. 프로젝트 또는 폴더에 대한 자세한 정보가 있는 팝업을 표시하려면 ![정보](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg)를 선택하세요. 사용 가능한 작업을 표시하려면 ![자세히](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg)를 선택하십시오. 자세한 내용은 [프로젝트 관리](#manage-projects)를 참조하십시오. |
| [!UICONTROL Type] | 이 항목이 Workspace 프로젝트, 폴더 또는 [모바일 스코어카드](https://experienceleague.adobe.com/ko/docs/analytics/analyze/mobapp/home)인지 여부를 나타냅니다. |
| [!UICONTROL 태그] | 프로젝트에 적용된 태그. |
| [!UICONTROL 예약됨] | 프로젝트를 수신자에게 이메일로 보내도록 예약할지 여부를 나타냅니다. [프로젝트 예약](/help/analyze/analysis-workspace/curate-share/t-schedule-report.md)을 참조하세요. |
| 공유 링크 (누구나) | 프로젝트는 Analysis Workspace에 액세스할 수 없는 사용자와도 누구와도 공유할 수 있습니다. 이 열은 프로젝트가 이러한 방식으로 공유되었는지 여부를 보여 줍니다. 자세한 내용은 [프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md)에서 [누구와도 프로젝트 공유(로그인 필요 없음)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link)를 참조하십시오. |
| [프로젝트 역할](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/curate-share/share-projects) | 프로젝트에 대한 역할(소유자, 편집, 복제, 보기)을 나타냅니다. |
| [!UICONTROL 보고서 세트] | 프로젝트가 연결된 보고서 세트입니다. |
| [!UICONTROL 소유자] | 이 프로젝트를 만든 사람 (귀하 또는 프로젝트를 귀하와 공유한 사용자) |
| [!UICONTROL 다음 사용자와 공유] | 프로젝트가 공유된 사용자입니다. |
| [!UICONTROL 마지막 수정일] | 프로젝트가 마지막으로 수정된 날짜와 시간. |
| [!UICONTROL 마지막으로 연 날짜] | 프로젝트를 마지막으로 연 날짜 및 시간입니다. |
| [!UICONTROL 마지막 사용] | 프로젝트를 마지막으로 사용한 날짜 및 시간입니다. |
| [!UICONTROL 프로젝트 ID] | 프로젝트의 ID입니다. |
|  | 프로젝트의 가장 긴 날짜 범위입니다. |
| [!UICONTROL 쿼리 개수] | 프로젝트에 포함된 총 쿼리 수입니다. |
| [!UICONTROL 위치] | 프로젝트가 있는 폴더입니다. |

### 프로젝트 관리

프로젝트를 관리하려면 프로젝트 목록에서 하나 이상의 프로젝트를 선택합니다.

파란색 작업 표시줄에서 다음 작업을 선택할 수 있습니다.

| 액션 | 설명 |
|---|---|
| ![삭제](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) 삭제 | 선택하면 Workspace 프로젝트 또는 모바일 스코어카드의 삭제를 확인하는 확인 대화 상자가 표시됩니다. **[!UICONTROL 확인]**&#x200B;을(를) 선택하여 확인합니다. |
| ![공유](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Share_18_N.svg) 공유 | 이 작업을 통해 프로젝트를 공유할 수 있습니다. [프로젝트 공유](../curate-share/share-projects.md)를 참조하십시오. |
| ![이름 바꾸기](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) 이름 바꾸기 | 프로젝트 이름을 바꾸기 위한 **[!UICONTROL 이름 바꾸기: *이름&#x200B;*]**&#x200B;대화 상자를 엽니다.**[!UICONTROL 저장&#x200B;]**&#x200B;을 선택하여 프로젝트의 새 이름을 저장합니다. |
| ![복사](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Copy_18_N.svg) 복사 | 선택한 프로젝트를 *원래 이름*(으)로 새 프로젝트에 즉시 복사합니다(복사). |
| ![고정](https://spectrum.adobe.com/static/icons/workflow_18/Smock_PinOff_18_N.svg) 고정 | 즉시 프로젝트를 목록의 맨 위에 고정합니다. ![핀](https://spectrum.adobe.com/static/icons/workflow_18/Smock_PinOff_18_N.svg) 표시기를 추가합니다. |
| ![태그](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Label_18_N.svg) 태그 | **[!UICONTROL 태그 프로젝트]** 대화 상자를 엽니다. 기존 태그를 선택하거나 새 태그를 추가할 수 있습니다. **[!UICONTROL 저장]**&#x200B;을 선택하여 프로젝트에 대한 태그를 저장합니다. |
| ![(비승인)승인](https://spectrum.adobe.com/static/icons/workflow_18/Smock_CheckmarkCircle_18_N.svg) 승인 또는 비승인 | 프로젝트를 승인하거나 승인하지 않습니다. |
| ![CSV 내보내기](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FileCSV_18_N.svg) CSV 내보내기 | 프로젝트의 쉼표로 구분된 값 목록이 포함된 파일을 즉시 다운로드합니다. |
| ![이동](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FolderAddTo_18_N.svg) 이동 | 이 작업을 사용하면 프로젝트를 폴더로 이동할 수 있습니다. **[!UICONTROL 폴더 선택]** 대화 상자의 **[!UICONTROL 폴더]** 목록에서 폴더를 선택한 다음 **[!UICONTROL 이동]**&#x200B;을 선택합니다. |


## 메뉴 바 {#menu-bar}

프로젝트 내에서 메뉴는 프로젝트 관리, 구성 요소 추가, 도움말 찾기 등의 옵션을 제공합니다. 키보드로 각 메뉴 옵션에 액세스할 수도 있습니다. [바로 가기](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys).


| 메뉴 항목 | 설명 |
|---|---|
| 프로젝트 | 이 메뉴에는 새로 만들기, 열기, 저장, 다른 이름으로 저장, [회사 보고서로 저장](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md) 등 프로젝트 관리를 위한 일반적인 작업이 포함되어 있습니다. 프로젝트 새로 고침을 클릭하여 전체 프로젝트를 새로 고쳐 최신 데이터 및 정의를 검색할 수도 있습니다. [CSV 및 PDF 다운로드](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/curate-share/download-send) 옵션을 사용하면 Workspace에서 데이터를 내보낼 수 있습니다. [프로젝트 정보 및 설정](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/build-workspace-project/freeform-overview)은 프로젝트 관리를 위한 다양한 옵션을 제공합니다. |
| 편집 | 마지막 작업을 실행 취소하거나 다시 실행합니다. 모두 지우기는 프로젝트를 빈 시작 지점으로 재설정합니다. |
| 삽입 | 이 메뉴에서 새 패널 또는 시각화를 삽입합니다. 왼쪽 레일에서 새 패널과 시각화를 삽입할 수도 있습니다. |
| [구성 요소](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/components/analysis-workspace-components) | 프로젝트에서 새 세그먼트, 계산된 지표, 날짜 범위 또는 경고 구성 요소를 만듭니다. 왼쪽 레일에서 새 구성 요소를 만들 수도 있습니다. 구성 요소 정의가 최근에 변경된 경우 구성 요소 새로 고침은 최신 정의를 검색합니다. |
| [Share](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/curate-share/send-schedule-files) | 조직의 수신자에게 PDF/CSV 프로젝트를 조정, 공유 및 예약합니다. |
| 도움말 | 도움말 문서, 비디오 및 Analytics [Experience League 커뮤니티](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=ko)에 액세스합니다. [디버거](https://developer.adobe.com/analytics-apis/docs/2.0/) 외에도 Workspace 팁의 가시성을 관리합니다. 프로젝트 [성능](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)에 영향을 미치는 Workspace 및 요인에 대한 세부 정보를 확인할 수 있습니다. |
| 공유 버튼 또는 소유자 | 프로젝트를 소유 또는 편집 중인 경우 오른쪽 상단의 공유 버튼을 클릭하면 프로젝트 수신자를 관리할 수 있습니다. 프로젝트에 대한 중복 또는 보기 역할이 있는 경우 프로젝트 소유자의 이름이 표시됩니다. |

### 프로젝트 정보 및 설정 {#info-settings}

**[!UICONTROL Workspace]** > **[!UICONTROL 프로젝트]** > **[!UICONTROL 프로젝트 정보 및 설정]**&#x200B;에서는 현재 활성 상태인 프로젝트에 대한 프로젝트 수준 정보를 제공합니다.

![프로젝트 정보](assets/projectinfo.png)

설정에는 다음이 포함됩니다.

| 설정 | 설명 |
|---|---|
| 프로젝트 이름 | 프로젝트에 지정된 이름. 이름을 더블 클릭하여 편집할 수 있습니다. |
| 소유자 | 프로젝트 소유자 이름 |
| 마지막 수정일 | 프로젝트의 마지막 수정 날짜. |
| 태그 | 더 쉬운 분류를 위해 프로젝트에 적용된 모든 태그를 나열합니다. |
| 설명 | 설명은 프로젝트의 목적을 명확히 하는 데 유용합니다. 설명을 더블 클릭하여 편집할 수 있습니다. |
| 반복 인스턴스 계산 | 보고서에서 반복 인스턴스가 카운트되는지 여부를 지정합니다. 예를 들어 이 설정(활성화된 경우)은 동일한 페이지에 대한 여러 개의 연속 페이지 조회수를 여러 페이지 조회수로 처리합니다. 이 설정을 끄면 단일 페이지 조회수로 계산됩니다(이 설정은 단일 페이지 방문과 같은 특정 지표에만 영향을 줌). **참고**: 이 설정은 플로우 또는 폴아웃 시각화에 적용되지 않습니다. |
| [주석 표시](/help/analyze/analysis-workspace/components/annotations/overview.md) | 프로젝트에 주석을 표시할지 여부를 지정합니다. |
| [프로젝트 색상 팔레트](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes) | 색맹 사용자에 최적화된 비맞춤형 팔레트에서 선택하거나 맞춤형 팔레트를 지정하여 Workspace에서 사용되는 범주별 색상 팔레트를 변경할 수 있습니다. 이 기능은 대부분의 시각화를 포함하여 작업 영역의 많은 사항에 영향을 줍니다. |
| [보기 밀도](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density) | 자유 형식 테이블 및 집단 테이블에서 왼쪽 레일의 수직 안쪽 여백을 줄여 화면에서 더 많은 데이터를 볼 수 있습니다. |

## 왼쪽 레일 {#left-rail}

프로젝트 내에서 왼쪽 레일에서 다양한 아이콘을 사용할 수 있으며, 각 아이콘은 프로젝트를 빌드하는 데 중요한 도구를 나타냅니다.

| 아이콘 | 기능 |
|---|---|
| ![패널 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_WebPage_18_N.svg) | [패널](/help/analyze/analysis-workspace/c-panels/panels.md) |
| ![시각화 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_GraphBarVertical_18_N.svg) | [시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) |
| ![구성 요소 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) | [구성 요소](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) |
| ![데이터 사전 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Bookmark_18_N.svg) | [데이터 사전](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) |
| ![목차 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ViewList_18_N.svg) | [목차](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md) |

왼쪽 레일의 구성 요소(차원, 지표, 세그먼트, 날짜 범위)는 활성 패널 데이터 보기와 관련되어 있습니다. 파란색 테두리가 활성 패널을 식별하고 활성 보고서 세트가 구성 요소 레일의 맨 위에 나열됩니다.


## 마우스 오른쪽 버튼 클릭 메뉴

다음은 Analysis Workspace에서 마우스 오른쪽 클릭 메뉴 사용에 대한 비디오입니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [상황에 맞는 메뉴 사용](https://video.tv.adobe.com/v/30915?quality=12&learn=on&captions=kor){target="_blank"}을 참조하세요.

>[!ENDSHADEBOX]

## 프로젝트 캔버스 {#canvas}

프로젝트 캔버스에서는 패널, 테이블, 시각화, 구성 요소를 결합하여 분석을 작성합니다. 프로젝트에는 여러 패널이 포함될 수 있으며 각 패널에는 여러 테이블과 시각화가 포함될 수 있습니다

패널은 기간, 보고서 세트 또는 분석 사용 사례에 따라 프로젝트를 구성하려는 경우 유용합니다. 활성 패널 주위에 색상이 있는 테두리가 있으며 왼쪽 레일에서 사용할 수 있는 구성 요소를 결정합니다.

프로젝트를 위해 선택한 시작 지점에 따라 캔버스에 [자유 형식 테이블](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/freeform-table) 또는 [빈 패널](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/panels/blank-panel)이 있습니다. 분석을 시작하는 가장 빠른 방법은 하나 이상의 구성 요소를 선택하여 프로젝트 캔버스로 끌어서 놓는 것입니다. 데이터 테이블이 자동으로 렌더링됩니다. [&#128279;](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/freeform-table)표를 만드는 다양한 옵션에 대해 자세히 알아보거나[교육 튜토리얼](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/home)을 활용하여 첫 번째 프로젝트를 만드는 방법에 대한 자세한 지침을 확인하십시오.

![](assets/canvas.png)
