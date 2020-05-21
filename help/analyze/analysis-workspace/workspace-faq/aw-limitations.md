---
description: Adobe Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록
title: Analysis Workspace의 알려진 제한 사항
translation-type: ht
source-git-commit: 025ac334f9191b6455eea0530a2a21c01199000a

---


# Analysis Workspace의 알려진 제한 사항

다음은 Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록입니다.

## 표

* 날짜 범위 또는 지표를 테이블의 행으로 사용하는 경우 날짜 비교 열을 추가할 수 없습니다.
* 세그먼트가 테이블의 행으로 사용되는 경우 선택 내용에서 지표 생성이 비활성화됩니다. 또한 선택 내용에서 지표 생성은 날짜 정렬 열에는 적용하지 않아야 합니다.
* 분류 행에 대한 조건부 서식은 사용자 지정 범위를 사용할 수 없습니다.
* 행 값을 합하여 합계 계산 설정이 적용될 때(일반적으로 정적 행 항목과 함께 사용) 테이블 합계 행에는 트렌드를 표시할 수 없습니다.
* [!UICONTROL Contribution Analysis]은 [!UICONTROL daily] 세부 기간&#x200B;_에서만_ 실행할 수 있습니다. [!UICONTROL hourly],[!UICONTROL weekly] 등 데이터에 대해서는 실행할 수 없습니다.

## 시각화

* [!UICONTROL Fallout], [!UICONTROL Flow], [!UICONTROL Cohort] 및 [!UICONTROL Histogram]과 같이 세그멘테이션을 활용하는 시각화는 계산된 지표를 입력으로 허용할 수 없습니다.
* [!UICONTROL Flow]: 시작/종료 차원(예: [!UICONTROL Entry page])은 플로우에서 사용할 수 없습니다.
* [!UICONTROL Cohort]: 정수가 아닌 항목은 집단 기준으로 사용할 수 없습니다.

## 패널

* 세그먼트 비교: [!UICONTROL Everyone Else] 세그먼트는 세그먼트 템플릿이 초기 놓기 영역에 사용되는 경우 생성되지 않습니다.

## 구성 요소 > 세그먼트

* 특정 지표 및 차원은 [!UICONTROL Occurrences], [!UICONTROL Unique Visitors] 등과 같이 세그멘테이션할 수 없습니다.
* 세그먼트가 Workspace에서 만들어지는 경우([!UICONTROL Components > Segments]에서 만드는 것이 아니라) 특정 구성 요소 및 연산자를 사용할 수 없습니다. 예를 들어 IP 주소가 그렇습니다.

## 구성 요소 > 계산된 지표

* 계산된 지표는 특정 시각화에 사용할 수 없습니다. 위의 &#39;시각화&#39;를 참조하십시오.
* 계산된 지표 자체가 별도의 기여도 분석 모델을 포함할 수 있으므로 계산된 지표는 [!UICONTROL Attribution] 패널에서 사용할 수 없습니다.
* 계산된 지표가 Workspace에서 만들어지는 경우([!UICONTROL Components > Segments]에서 만드는 것이 아니라) 특정 구성 요소 및 연산자를 사용할 수 없습니다. (예: [!UICONTROL IP Address])

## 구성 요소 > 날짜 범위

* 사용자 지정 날짜 범위는 [!UICONTROL This day last year], [!UICONTROL This day last month] 등을 지원하지 않습니다.

## 구성 요소 > 가상 보고서 세트

* 보고서 처리 시간이 활성화되면 특정 구성 요소가 지원되지 않습니다. 전체 목록이 필요하면 [보고서 처리 시간](/help/components/vrs/vrs-report-time-processing.md)을 참조하십시오.

## 구성 요소 > 보고서 설정

* [!UICONTROL Report Settings] 페이지의 일부 설정은 적용되지 않습니다. Analysis Workspace는 하단에 있는 [!UICONTROL Language/Currency/Encoding] 설정만 사용합니다([!UICONTROL Thousands separator], [!UICONTROL Scheduled Report Encoding] 및 [!UICONTROL CSV Separator Character]).

## 기여도 분석 IQ

* 지표의 하위 세트는 [!UICONTROL Attribution IQ]에서 지원되지 않습니다 . 전체 목록이 필요하면 [기여도 분석 IQ FAQ](/help/analyze/analysis-workspace/c-panels/attribution/attribution-faq.md)를 참조하십시오.
