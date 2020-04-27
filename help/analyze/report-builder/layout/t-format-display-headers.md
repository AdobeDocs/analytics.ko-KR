---
description: 보고서의 이름을 지정하고 행 및 열 머리글이 표시되는 방식을 구성할 수 있습니다. 피벗 및 사용자 지정 레이아웃 유형에 [서식 선택 사항] 링크를 사용할 수 있습니다.
title: 머리글 표시 형식 지정
topic: Report builder
uuid: cd0e167b-9463-43fd-87b2-724d1c79de68
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 머리글 표시 형식 지정

보고서의 이름을 지정하고 행 및 열 머리글이 표시되는 방식을 구성할 수 있습니다. 피벗 및 사용자 지정 레이아웃 유형에 [서식 선택 사항] 링크를 사용할 수 있습니다.

1. 에서 요청을 만듭니다 [!UICONTROL Request Wizard: Step 1].
1. 클릭 **[!UICONTROL Next]**.
1. On the [!UICONTROL Request Wizard: Step 2] form, add dimensions and metrics data to the request, as desired.
1. 클릭 **[!UICONTROL Format Options]**.
1. Configure the [!UICONTROL Display] options:

   | 요소 | 설명 |
   |--- |--- |
   | 보고서 이름 | 요청 마법사: 1단계의 트리에서 선택한 요청 유형의 이름(예: [!DNL Traffic Report])이나 [!DNL Name this Request]에 입력하는 이름이 표시됩니다. |
   | 필터 매개 변수 | 검색 필터와 같은 차원 필터를 표시합니다. |
   | 세그먼트 | 세그먼트 매개 변수를 표시합니다. |
   | 최근 데이터 | 최근 데이터 매개 변수를 표시합니다. 예:    데이터 최신성: 페이지 보기 수(1.5시간 전), 종료 횟수(30분 전) 현재 데이터 처리에 대한 자세한 내용은 [선택 사항](/help/analyze/report-builder/options.md)을 참조하십시오. |

   Regarding display order, if the [!UICONTROL Row Label] grid (on Step 2) contains an item, it is displayed first in the request. If not, the system uses the first item present in the [!UICONTROL Column Label] grid. If no row or column items exist, the first item in the [!UICONTROL Metrics] grid is displayed.

   **행 및 열 머리글 표시:** 행 및 열을 추가하여 이 항목을 표시합니다.

   버전 3.11에서는 각 항목에 대해 머리글을 표시할 수도 있습니다. 버전 4에는 세 항목 모두 표시되거나 아무 것도 표시되지 않습니다. 버전 3.11에서 요청을 만들어 4.x에서 열면, Report Builder가 2단계에서 머리글이 누락된 항목에 대한 셀 하나로 범위를 업데이트하라는 메시지를 표시합니다.

   **머리글을 Excel 자동 필터로 변경:** 행 및 열 머리글이 표시되는 경우에만 사용할 수 있습니다. 이 설정은 Excel 자동 필터링 기능을 만들어 Report Builder가 이 요청에 대해 반환하는 데이터에 추가합니다.

   >[!NOTE]
   >
   >Excel에서는 한 워크시트에 대해 하나의 자동 필터만 지원합니다. 자동 필터가 이미 있는 워크시트에서 새 자동 필터를 만들면 Excel은 기존 자동 필터가 대체될 것이라는 경고를 표시하지 않습니다.

   **자동 윤곽 수행:** Report Builder가 반환한 날짜를 목록 보기에서 트리 보기로 변환합니다.

   **이 요청의 이름:** 요청에 대해 사용자 정의 이름을 입력하거나 1단계에서 선택한 기본 이름을 사용할 수 있도록 해줍니다. 이 이름은 에서 [!UICONTROL Report] 이름으로 표시됩니다 [!UICONTROL Request Manager]. See [Name a Request](/help/analyze/report-builder/layout/name-a-request.md).

1. 클릭 **[!UICONTROL OK]**.
