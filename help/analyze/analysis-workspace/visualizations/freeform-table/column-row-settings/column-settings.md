---
description: 열 설정을 사용하면 열 서식을 구성할 수 있으며, 열 서식 일부는 조건부일 수 있습니다.
title: 열 설정
uuid: 151d66da-04f7-4d0f-985c-4fdd92bc1308
feature: Freeform Tables
role: User, Admin
exl-id: 82034838-b015-4ca2-adb6-736f20a478d8
source-git-commit: 984406d00e5a5ae966fff60ec9fcfcb000958696
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 100%

---

# [!UICONTROL 열 설정]

[!UICONTROL 열 설정]을 사용하면 열 서식을 구성할 수 있으며, 열 서식 일부는 조건부일 수 있습니다.

## [!UICONTROL 열 설정] 편집 {#edit-column-settings}

개별 열 또는 여러 열에 대한 열 설정을 동시에 편집할 수 있습니다.

1. Analysis Workspace에서 자유 형식 테이블을 프로젝트로 드래그합니다.

1. (조건) 여러 열을 동시에 편집하려면 Shift 키를 누른 상태에서 편집할 각 열을 선택합니다.

1. 편집하려는 열 위로 마우스를 가져간 다음 톱니바퀴 아이콘을 선택합니다.

   열을 여러 개 선택했다면 선택한 열의 톱니바퀴 아이콘을 클릭합니다. 변경 사항은 모든 열에 적용됩니다.

   ![](assets/column_settings.png)

1. [열 설정](#column-settings)으로 계속 진행합니다.

## 열 설정

[열 설정 편집](#edit-uicontrol-column-settings)에 설명된 대로 Analysis Workspace의 개별 테이블에 대한 다음 열 설정을 업데이트할 수 있습니다.

[사용자 환경 설정](/help/analyze/analysis-workspace/user-preferences.md)에 설명된 대로 Analysis Workspace에서 만드는 모든 새 프로젝트에 대해 이러한 동일한 설정 중 일부를 관리할 수도 있습니다.

| 요소 | 설명 |
| --- | --- |
| **합계 셀** |  |
| 합계 표시 | 이 합계는 일반적으로 [!UICONTROL 총 합계]와 같거나 그 하위 집합입니다. [!UICONTROL 포함 내용 없음] 선택 사항을 포함하여 자유 형식 테이블 내에 적용된 테이블 필터를 반영합니다. |
| 합계 표시 | 이 합계는 수집 된 모든 히트 수를 나타내며 “보고서 세트 합계”라고도 합니다. 세그먼트가 패널 수준에서 또는 자유 형식 테이블 내에서 적용되면 이 합계는 세그먼트 기준과 일치하는 모든 히트를 반영하도록 조정됩니다. [정적 행](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md)이 있는 테이블 또는 분류에서는 총 합계가 지원되지 않습니다. |
| **테이블 셀** |   |
| 숫자 | 셀에 지표에 대한 숫자 값을 표시할지 또는 숨길지를 결정합니다. 예를 들어 지표가 페이지 조회수이면 숫자 값은 행 항목에 대한 페이지 조회수입니다. |
| 비율 | 셀에 지표에 대한 퍼센트 값을 표시할지 또는 숨길지를 결정합니다. 예를 들어 지표가 페이지 조회수이면 퍼센트 값은 행 항목에 대한 페이지 조회수를 해당 열에 대한 총 페이지 조회수로 나눈 수입니다.  참고: 정확하게 말하자면 100%보다 큰 백분율을 표시할 수 있습니다. 또한 열의 너비를 크게 늘릴 수 있도록 상한을 1,000%로 옮겼습니다. |
| 예외 항목 | 이 열의 값에 대해 예외 항목 탐지가 실행되는지 여부를 결정합니다. 자세한 내용은 [Analysis Workspace에서 예외 항목 보기](/help/analyze/analysis-workspace/c-anomaly-detection/view-anomalies.md)를 참조하십시오. |
| 머리글 텍스트 줄바꿈 | 자유 형식 테이블의 머리글 텍스트를 줄바꿈하여 머리글을 더 읽기 쉽게 하고 테이블을 더 공유하기 쉽게 할 수 있습니다. 이 기능은 .pdf 렌더링 및 긴 이름을 사용하는 지표에 유용합니다. 기본적으로 사용됩니다. |
| 0을 값없음으로 해석 | 값이 0인 셀에 대해, 0을 표시할지 아니면 빈 셀을 표시할지를 결정합니다. 달의 각 날에 대한 데이터를 보고 일부 날은 아직 일어나지 않은 경우 유용합니다.  차후의 날짜에 대해 0을 표시하는 대신 빈 셀을 표시할 수 있습니다. 차트에 이 설정도 적용됩니다(즉, 이 설정을 선택한 경우 차트에 값이 0인 줄 또는 막대가 표시되지 않습니다). |
| 배경 | 막대 그래프 및 조건부 서식을 포함하여, 셀에 모든 셀 서식을 표시할지 또는 숨길지를 결정합니다. |
| 막대 그래프 | 열에 대한 합계와 상대적인 셀 값을 나타내는 수평 막대 그래프를 표시합니다. |
| 조건부 서식 | 아래 섹션을 참조하십시오. |
| 테이블 셀 미리보기 | 각 셀이 현재 선택된 서식 선택 사항이 적용되면 어떻게 나타나는지 미리보기를 표시합니다. |

## 조건부 서식 {#conditional-formatting}

조건부 서식을 지정하면 정의할 수 있는 상한, 중간점 및 하한에 서식이 적용됩니다. “사용자 정의” 제한을 선택하지 않은 경우 자유 형식 테이블 내의 조건부 서식 지정(예: 색상)이 분류에서도 자동으로 사용됩니다.

![](assets/conditional-formatting.png)

| 요소 | 설명 |
| --- | --- |
| 조건부 서식 | 선택한 사전 구성된 색상 세트를 셀에 적용합니다. 선택한 4개의 색상 구성표에 따라 높은 값, 중간 값, 낮은 값에 다른 색상을 지정합니다. <br> 테이블에서 차원을 바꾸면 조건부 서식 제한이 재설정됩니다. 지표를 바꾸면 해당 열에 대한 제한이 재계산됩니다 (지표는 X축에 있고 차원은 Y축에 있음). |
| 백분율 제한값 사용 | 절댓값이 아니라 백분율에 따라 제한 범위 변경. 개수와 비율 (페이지 조회수 등)이 있는 지표는 물론, 비율만 기반으로 하는 지표 (바운스 비율 등)에도 작동합니다. |
| 자동 생성 | 데이터를 기반으로 상한/중간/하한을 자동으로 계산. 상한은 이 열에서 가장 큰 값입니다. 하한은 가장 낮은 값이며, 중간점은 상한과 하한의 평균입니다. |
| 사용자 정의 | 수동으로 상한/중간/하한 지정. 이렇게 하면 열 값이 양호, 평균 또는 나쁨일 때를 유연하게 확인할 수 있습니다. |
| 조건부 서식 팔레트 | 조건부 서식에 사용 가능한 4개의 색상 구성표 중 하나를 선택합니다. |

## 비기본 속성 모델 사용 {#attribution}

Analysis Workspace는 거의 모든 지표에 대한 [속성](/help/analyze/analysis-workspace/attribution/overview.md)을 지원합니다.

1. 자유 형식 테이블 열 옆의 설정(기어) 아이콘을 클릭합니다.

   ![속성 확인란](assets/attribution-checkbox.png)

1. **[!UICONTROL 데이터 설정]**&#x200B;에서 **[!UICONTROL 기본값이 아닌 속성 모델 사용]**&#x200B;을 선택합니다. 다른 속성 모델에 대한 자세한 내용은 [속성 모델](/help/analyze/analysis-workspace/attribution/models.md)을 참조하십시오.

   ![속성 모델 선택](assets/attribution-select.png)

>[!MORELIKETHIS]
>
>* [데이터 소스 관리](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md)

## 동적 열

다음은 Analysis Workspace의 동적 열을 사용하는 방법에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/23138/?quality=12)
