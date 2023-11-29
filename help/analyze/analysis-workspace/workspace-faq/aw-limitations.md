---
description: Adobe Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록
title: Analysis Workspace의 알려진 제한 사항
feature: Workspace Basics
role: User, Admin
exl-id: 520e970b-1387-4f70-985b-bfe397f4a21b
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 90%

---

# Analysis Workspace의 알려진 제한 사항

다음은 Analysis Workspace 및 관련 구성 요소의 알려진 제한 사항 목록입니다.

## 표

* 날짜 범위 또는 지표를 테이블의 행으로 사용하는 경우 날짜 비교 열을 추가할 수 없습니다.
* 세그먼트가 테이블의 행으로 사용되는 경우 선택 내용에서 지표 생성이 비활성화됩니다. 또한 선택 내용에서 지표 생성은 날짜 정렬 열에는 적용하지 않아야 합니다.
* 분류 행에 대한 조건부 서식은 사용자 정의 범위를 사용할 수 없습니다.
* 행 값을 합하여 합계 계산 설정이 적용될 때 (일반적으로 정적 행 항목과 함께 사용) 테이블 합계 행에는 트렌드를 표시할 수 없습니다.
* [!UICONTROL 기여도 분석]은 [!UICONTROL 일별] 세부기간에서&#x200B;_만_ 실행할 수 있습니다. [!UICONTROL 시간별], [!UICONTROL 주별] 등 데이터에 대해서는 실행할 수 없습니다.

## 시각화

* [!UICONTROL 폴아웃], [!UICONTROL 플로우], [!UICONTROL 집단] 및 [!UICONTROL 히스토그램]과 같이 세그먼테이션을 활용하는 시각화는 계산된 지표를 입력으로 허용할 수 없습니다.
* [!UICONTROL 플로우]: 시작/종료 차원(예: [!UICONTROL 시작 페이지])은 플로우에서 사용할 수 없습니다.
* [!UICONTROL 집단]: 정수가 아닌 항목은 집단 기준으로 사용할 수 없습니다.

## 패널

* 세그먼트 비교: [!UICONTROL 기타 사용자] 세그먼트는 세그먼트 템플릿이 초기 놓기 영역에 사용되는 경우 생성되지 않습니다.

## 구성 요소 > 세그먼트

* 특정 지표 및 차원은 [!UICONTROL 발생 횟수], [!UICONTROL 고유 방문자 수] 등과 같이 세그먼테이션할 수 없습니다.
* 에서 생성된 임시 세그먼트 [패널 드롭 영역](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko-KR) 는 빠른 필터의 유형입니다. 이러한 구성 요소는 공개하지 않는 한 작업 영역 또는 세그먼트 구성 요소 관리자의 왼쪽 레일에 표시되지 않습니다. 자세한 내용은 [빠른 세그먼트](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

## 구성 요소 > 계산된 지표

* 계산된 지표는 특정 시각화에 사용할 수 없습니다. 위의 &#39;시각화&#39;를 참조하십시오.
* 계산된 지표 자체가 별도의 속성 모델을 포함할 수 있으므로 계산된 지표는 [!UICONTROL 속성] 패널에서 사용할 수 없습니다.
* 계산된 지표가 Workspace에서 만들어지는 경우 ([!UICONTROL 구성 요소 > 세그먼트]에서 만드는 것이 아니라) 특정 구성 요소 및 연산자를 사용할 수 없습니다. 예를 들어 [!UICONTROL IP 주소]가 그렇습니다.

## 구성 요소 > 날짜 범위

* 사용자 지정 날짜 범위는 [!UICONTROL 지난해 이날], [!UICONTROL 지난달 이날] 등을 지원하지 않습니다.

## 구성 요소 > 가상 보고서 세트

* 보고서 처리 시간이 활성화되면 특정 구성 요소가 지원되지 않습니다. 전체 목록이 필요하면 [보고서 처리 시간](/help/components/vrs/vrs-report-time-processing.md)을 참조하십시오.

## 구성 요소 > 모든 구성 요소 > 보고서 설정

* [!UICONTROL 보고서 설정] 페이지의 일부 설정은 적용되지 않습니다. Analysis Workspace는 맨 아래에 있는 [!UICONTROL 언어/통화/인코딩] 설정인 [!UICONTROL 천 단위 구분 문자], [!UICONTROL 예약된 보고서 인코딩] 및 [!UICONTROL CSV 구분 문자]만 사용합니다.

## 속성

* 지표의 하위 세트는 [!UICONTROL Attribution ]에서 지원되지 않습니다. 전체 목록이 필요하면 [Attribution FAQ](/help/analyze/analysis-workspace/attribution/faq.md)를 참조하십시오.
