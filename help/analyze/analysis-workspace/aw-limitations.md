---
description: 'null'
seo-description: 'null'
seo-title: 분석 작업 공간의 알려진 제한 사항
title: 분석 작업 공간의 알려진 제한 사항
translation-type: tm+mt
source-git-commit: 9d6b35c7c6de6fcb49fea3b662ff8bc9044b5e29

---


# 분석 작업 공간의 알려진 제한 사항

다음은 분석 작업 공간 및 관련 구성 요소의 알려진 제한 목록입니다.

## 표

* 날짜 범위 또는 지표가 표의 행으로 사용되는 경우 날짜 비교 열을 추가할 수 없습니다.
* 세그먼트가 테이블의 행으로 사용될 때에는 선택 항목으로 지표를 만듭니다. 또한, 선택 사항에서 지표를 만드는 것은 날짜가 지정된 열에 적용되면 안 됩니다.
* 분류 행에 대한 조건부 서식 지정은 사용자 지정 범위를 사용할 수 없습니다.
* 행 값 설정이 적용되어 (일반적으로 정적 행 항목과 함께 사용) 테이블 합계 행은 트렌드를 계산할 때 트렌드를 계산할 수 없습니다.
* [!UICONTROL 기여도 분석은] [!UICONTROL 일별] 세부기간에서만 _실행할_&#x200B;수 있습니다. [!UICONTROL 시간별], [!UICONTROL 주별]등에 대해 실행할 수 없습니다.

## 시각화

* [!UICONTROL 폴아웃], [!UICONTROL 흐름], [!UICONTROL 집단]및 [!UICONTROL 히스토그램과 같은]세그멘테이션을 활용하는 시각화는 계산된 지표를 입력으로 수락할 수 없습니다.
* [!UICONTROL 흐름]: 시작/종료 차원 (예: [!UICONTROL 시작 페이지]) 는 흐름에 사용할 수 없습니다.
* [!UICONTROL 집단]: 정수가 아닌 정수는 집단 기준으로 사용할 수 없습니다.

## 패널

* Segment Comparison: The [!UICONTROL Everyone Else] segment does not get created if a segment template is used in the initial drop zone.

## 구성 요소 &gt; 세그먼트

* Certain metrics and dimensions are not segmentable, such as [!UICONTROL Occurrences], [!UICONTROL Unique Visitors], etc.
* Certain components and operators are unavailable if a segment is created from Workspace (as opposed to being created from [!UICONTROL Components &gt; Segments]). 예: IP 주소.

## 구성 요소 &gt; 계산된 지표

* 계산된 지표는 특정 시각화에 사용할 수 없습니다. 위의'시각화'를 참조하십시오.
* Calculated metrics cannot be used in the [!UICONTROL Attribution] panel, since calculated metrics themselves can include separate attribution models.
* Certain components and operators are unavailable if a calculated metric is created from Workspace (as opposed to being created from [!UICONTROL Components &gt; Segments]). For example, [!UICONTROL IP Address].

## 구성 요소 &gt; 날짜 범위

* Custom date ranges do not support [!UICONTROL This day last year], [!UICONTROL This day last month], etc.

## 구성 요소 &gt; 가상 보고서 세트

* 보고서 시간 처리가 활성화되면 특정 구성 요소가 지원되지 않습니다. For a full list, see [Report Time Processing](/help/components/vrs/vrs-report-time-processing.md).

## 구성 요소 &gt; 보고서 설정

* Some of the settings on the [!UICONTROL Report Settings] page do not apply. Analysis Workspace uses only the [!UICONTROL Language/Currency/Encoding] settings at the bottom: [!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding], and [!UICONTROL CSV Separator Character].

## 속성 IQ

* A subset of metrics is not supported in [!UICONTROL Attribution IQ]. For a full list, see the [Attribution IQ FAQ](/help/analyze/analysis-workspace/attribution-iq/attribution-faq.md).