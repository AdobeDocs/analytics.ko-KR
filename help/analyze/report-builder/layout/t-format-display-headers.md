---
description: 보고서의 이름을 지정하고 행 및 열 머리글이 표시되는 방식을 구성할 수 있습니다. 피벗 및 사용자 지정 레이아웃 유형에 [서식 선택 사항] 링크를 사용할 수 있습니다.
seo-description: 보고서의 이름을 지정하고 행 및 열 머리글이 표시되는 방식을 구성할 수 있습니다. 피벗 및 사용자 지정 레이아웃 유형에 [서식 선택 사항] 링크를 사용할 수 있습니다.
seo-title: 머리글 표시 형식 지정
solution: Analytics
title: 머리글 표시 형식 지정
topic: Report Builder
uuid: CD 0 E 167 B -9463-43 FD -87 B 2-724 D 1 C 79 DE 68
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 머리글 표시 형식 지정

보고서의 이름을 지정하고 행 및 열 머리글이 표시되는 방식을 구성할 수 있습니다. 피벗 및 사용자 지정 레이아웃 유형에 [서식 선택 사항] 링크를 사용할 수 있습니다.

1. Create a request on the [!UICONTROL Request Wizard: Step 1].
1. Click **[!UICONTROL Next]**.
1. [!UICONTROL 요청 마법사: 2단계] 양식에서 원하는 대로 차원 및 지표 데이터를 추가합니다.
1. **[!UICONTROL 형식 옵션을]**&#x200B;클릭합니다.
1. [!UICONTROL 표시] 옵션을 구성합니다. 

   | 요소 | 설명 |
   |--- |--- |
   | 보고서 이름 | Displays either the name of the report type you selected from the tree in the  Request Wizard: Step 1 (for example, [!DNL Traffic Report]), or the name you type in the [!DNL Name this Request] field. |
   | 필터 매개 변수 | 검색 필터와 같은 차원 필터를 표시합니다. |
   | 세그먼트 | 세그먼트 매개 변수를 표시합니다. |
   | 최근 데이터 | 최근 데이터 매개 변수를 표시합니다. 예:    Data Recency: Page Views (1.5 hr ago), Exits (30 mins ago)  See [Options](../../../analyze/report-builder/options.md) for information about current data processing. |

   표시 순서의 경우, [!UICONTROL 행 레이블] 그리드(2단계에서)에 항목이 들어 있으면, 요청에서 먼저 표시됩니다. 없으면, 시스템은 [!UICONTROL 열 레이블] 그리드에 표시된 첫 번째 항목을 사용합니다. 열이나 행 항목이 존재하지 않으면 [!UICONTROL 지표] 그리드의 첫 번째 항목이 표시됩니다.

   **행 및 열 머리글 표시:** 행 및 열을 추가하여 이 항목을 표시합니다.

   버전 3.11에서는 각 항목에 대해 머리글을 표시할 수도 있습니다. 버전 4에는 세 항목 모두 표시되거나 아무 것도 표시되지 않습니다. 버전 3.11에서 요청을 만들어 4.x에서 열면, Report Builder가 2단계에서 머리글이 누락된 항목에 대한 셀 하나로 범위를 업데이트하라는 메시지를 표시합니다.

   **머리글을 Excel 자동 필터로 변경:** 행 및 열 머리글이 표시되는 경우에만 사용할 수 있습니다. 이 설정은 Excel 자동 필터링 기능을 만들어 Report Builder가 이 요청에 대해 반환하는 데이터에 추가합니다.

   >[!NOTE]
   >
   >Excel는 워크시트당 하나의 자동 필터만 지원합니다. 자동 필터가 이미 있는 워크시트에서 새 자동 필터를 만들면 Excel은 기존 자동 필터가 대체될 것이라는 경고를 표시하지 않습니다.

   **자동 윤곽 수행:** Report Builder가 반환한 날짜를 목록 보기에서 트리 보기로 변환합니다.

   **이 요청의 이름:** 요청에 대해 사용자 정의 이름을 입력하거나 1단계에서 선택한 기본 이름을 사용할 수 있도록 해줍니다. 이 이름은 [!UICONTROL 요청 관리자]에 [!UICONTROL 보고서] 이름으로 표시됩니다. see [요청 이름 지정](../../../analyze/report-builder/layout/name-a-request.md#concept_37277AFB63EA4541B6FD93A5B713D82D)

1. **[!UICONTROL 확인을 클릭합니다]**.
