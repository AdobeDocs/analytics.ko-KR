---
description: Adobe Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항에 대해 알아보기
title: 알려진 제한 사항
feature: Workspace Basics
role: User, Admin
exl-id: 520e970b-1387-4f70-985b-bfe397f4a21b
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 100%

---

# 알려진 제한 사항

다음은 Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록입니다.

## 테이블

* 날짜 범위 또는 지표를 테이블의 행으로 사용하는 경우 날짜 비교 열을 추가할 수 없습니다.
* 세그먼트가 테이블의 행으로 사용되는 경우 선택 내용에서 지표 생성이 비활성화됩니다. 또한 선택 내용에서 지표 생성은 날짜 정렬 열에는 적용하지 않아야 합니다.
* 분류 행에 대한 조건부 서식은 사용자 정의 범위를 사용할 수 없습니다.
* 행 값을 합하여 합계 계산 설정이 적용될 때(일반적으로 정적 행 항목과 함께 사용) 테이블 합계 행에는 트렌드를 표시할 수 없습니다.

## 시각화

* [!UICONTROL 폴아웃], [!UICONTROL 흐름], [!UICONTROL 코호트] 및 [!UICONTROL 히스토그램]과 같이 세그먼트를 활용하는 시각화는 계산된 지표를 입력으로 허용할 수 없습니다.
* [!UICONTROL 흐름]: 시작/종료 차원(예: [!UICONTROL 시작 페이지])은 흐름에서 사용할 수 없습니다.
* [!UICONTROL 코호트]: 정수가 아닌 항목은 코호트 기준으로 사용할 수 없습니다.

## 세그먼트

* [!UICONTROL 이벤트], [!UICONTROL 개인] 등과 같은 특정 지표 및 차원은 세그먼트화할 수 없습니다.
* [패널 놓기 영역](/help/analyze/analysis-workspace/c-panels/panels.md)에 만든 애드혹 세그먼트는 일종의 빠른 세그먼트입니다. 공개하지 않으면 Workspace 또는 세그먼트 관리자의 왼쪽 패널에 나타나지 않습니다. 자세한 내용은 [빠른 세그먼트](/help/components/segmentation/segmentation-workflow/seg-quick.md)를 참조하십시오.

## 계산된 지표

* 계산된 지표는 특정 시각화에 사용할 수 없습니다. [시각화](#visualizations)를 참조하십시오.
* 계산된 지표 자체가 별도의 속성 모델을 포함할 수 있으므로 계산된 지표는 [!UICONTROL 속성] 패널에서 사용할 수 없습니다.
* 계산된 지표가 Workspace에서 만들어지는 경우 ([!UICONTROL 구성 요소 > 세그먼트]에서 만드는 것이 아니라) 특정 구성 요소 및 연산자를 사용할 수 없습니다. 예를 들어 [!UICONTROL IP 주소]가 그렇습니다.

## 날짜 범위

* 사용자 정의 날짜 범위는 [!UICONTROL 지난해 이날], [!UICONTROL 지난달 이날] 등을 지원하지 않습니다.


## 보고서 설정

* [!UICONTROL 보고서 설정] 페이지의 일부 설정은 적용되지 않습니다. Analysis Workspace는 맨 아래에 있는 [!UICONTROL 언어/통화/인코딩] 설정인 [!UICONTROL 천 단위 구분자], [!UICONTROL 예약된 보고서 인코딩] 및 [!UICONTROL CSV 구분자]만 사용합니다.



<!--
# Known limitations in Analysis Workspace 

Here is a list of known limitations in Analysis Workspace and its related components:

## Tables

* Date comparison columns cannot be added when either date ranges or metrics are used as rows of a table.
* Create metric from selection is disabled when segments are used as rows of a table. Additionally, Create metric from selection should not be applied to date-aligned columns.
* Conditional formatting for breakdown rows cannot use custom ranges.
* Table total rows cannot be trended when Calculate totals by summing the row values setting is applied (typically used with Static row items).
* [!UICONTROL Contribution Analysis] can be run at the [!UICONTROL daily] granularity _only_. It cannot be run against [!UICONTROL hourly], [!UICONTROL weekly], etc., data.

## Visualizations

* Visualizations that leverage segmentation, such as [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], and [!UICONTROL Histogram], cannot accept calculated metrics as inputs.
* [!UICONTROL Flow]: Entry/Exit dimensions, e.g. [!UICONTROL Entry page], cannot be used in Flow.
* [!UICONTROL Cohort]: Non-integers cannot be used as Cohort criteria.

## Panels

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.

## Components > Segments

* Certain metrics and dimensions are not segmentable, such as [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], etc.
* Adhoc segments created in the [panel dropzone](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html) are a type of quick filter. They do not appear in the left rail of Workspace or the Segment component manager unless they are made public. For more information, see [Quick segments](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

## Components > Calculated Metrics

* Calculated metrics cannot be used in certain visualizations. See 'Visualizations' above.
* Calculated metrics cannot be used in the [!UICONTROL Attribution] panel, since calculated metrics themselves can include separate attribution models.
* Certain components and operators are unavailable if a calculated metric is created from Workspace (as opposed to being created from [!UICONTROL Components > Segments]). For example, [!UICONTROL IP Address].

## Components > Date Ranges

* Custom date ranges do not support [!UICONTROL This day last year], [!UICONTROL This day last month], etc.

## Components > Virtual Reports Suites

* When report time processing is enabled, certain components are not supported. For a full list, see [Report Time Processing](/help/components/vrs/vrs-report-time-processing.md).

## Components > All components > Report settings

* Some of the settings on the [!UICONTROL Report Settings] page do not apply. Analysis Workspace uses only the [!UICONTROL Language/Currency/Encoding] settings at the bottom: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], and [!UICONTROL CSV Separator Character].

## Attribution

* A subset of metrics is not supported in [!UICONTROL Attribution]. For a full list, see the [Attribution FAQ](/help/analyze/analysis-workspace/attribution/faq.md).
-->
