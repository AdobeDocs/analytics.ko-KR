---
description: Adobe Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록
title: Analysis Workspace의 알려진 제한 사항
translation-type: tm+mt
source-git-commit: 025ac334f9191b6455eea0530a2a21c01199000a

---


# Analysis Workspace의 알려진 제한 사항

다음은 Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록입니다.

## 표

* 날짜 범위 또는 지표를 테이블의 행으로 사용하는 경우 날짜 비교 열을 추가할 수 없습니다.
* 세그먼트가 테이블의 행으로 사용되는 경우 선택 내용에서 지표 생성이 비활성화됩니다. 또한 선택 내용에서 지표 생성은 날짜 정렬 열에는 적용하지 않아야 합니다.
* 분류 행에 대한 조건부 서식은 사용자 지정 범위를 사용할 수 없습니다.
* 행 값을 합하여 합계 계산 설정이 적용될 때(일반적으로 정적 행 항목과 함께 사용) 테이블 합계 행에는 트렌드를 표시할 수 없습니다.
* [!UICONTROL Contribution Analysis] 는 [!UICONTROL daily] 세부기간에서만 __&#x200B;실행할 수 있습니다. It cannot be run against [!UICONTROL hourly], [!UICONTROL weekly], etc., data.

## 시각화

* Visualizations that leverage segmentation, such as [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort], and [!UICONTROL Histogram], cannot accept calculated metrics as inputs.
* [!UICONTROL Flow]:시작/종료 차원(예:흐름에서 사용할 수 [!UICONTROL Entry page]없습니다.
* [!UICONTROL Cohort]:정수가 아닌 항목은 집단 기준으로 사용할 수 없습니다.

## 패널

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.

## 구성 요소 > 세그먼트

* Certain metrics and dimensions are not segmentable, such as [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], etc.
* Certain components and operators are unavailable if a segment is created from Workspace (as opposed to being created from [!UICONTROL Components > Segments]). 예를 들어 IP 주소가 그렇습니다.

## 구성 요소 > 계산된 지표

* 계산된 지표는 특정 시각화에 사용할 수 없습니다. 위의 &#39;시각화&#39;를 참조하십시오.
* Calculated metrics cannot be used in the [!UICONTROL Attribution] panel, since calculated metrics themselves can include separate attribution models.
* Certain components and operators are unavailable if a calculated metric is created from Workspace (as opposed to being created from [!UICONTROL Components > Segments]). (예: [!UICONTROL IP Address])

## 구성 요소 > 날짜 범위

* 사용자 지정 날짜 범위는 [!UICONTROL This day last year]지원 [!UICONTROL This day last month]등을 하지 않습니다.

## 구성 요소 > 가상 보고서 세트

* 보고서 처리 시간이 활성화되면 특정 구성 요소가 지원되지 않습니다. 전체 목록이 필요하면 [보고서 처리 시간](/help/components/vrs/vrs-report-time-processing.md)을 참조하십시오.

## 구성 요소 > 보고서 설정

* Some of the settings on the [!UICONTROL Report Settings] page do not apply. 분석 작업 공간에서는 아래쪽의 [!UICONTROL Language/Currency/Encoding] 설정만 사용합니다. [!UICONTROL Thousands separator]및 [!UICONTROL Scheduled Report Encoding]를 [!UICONTROL CSV Separator Character]참조하십시오.

## 기여도 분석 IQ

* A subset of metrics is not supported in [!UICONTROL Attribution IQ]. 전체 목록이 필요하면 [기여도 분석 IQ FAQ](/help/analyze/analysis-workspace/c-panels/attribution/attribution-faq.md)를 참조하십시오.
