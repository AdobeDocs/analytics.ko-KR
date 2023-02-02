---
title: Analysis Workspace에서 사용자 및 회사 환경 설정을 지정하는 방법
description: 사용자를 위한 일반 및 프로젝트 환경은 물론 어두운 테마 환경을 설정할 수 있습니다.
feature: Workspace Basics
role: User, Admin
exl-id: f32e3061-f396-4730-96e1-d251b00e32f0
source-git-commit: 58abc4a8410441a3c76c6737ace8e2c5ab5c1374
workflow-type: tm+mt
source-wordcount: '2556'
ht-degree: 95%

---

# 환경 설정

생성한 모든 새 프로젝트 또는 패널에 대해 Analysis Workspace 및 관련 구성 요소의 설정을 관리할 수 있습니다. 기존 프로젝트 및 패널은 영향을 받지 않습니다.

기본 설정에 대한 간단한 개요를 보려면 이 비디오를 보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/332600/?quality=12)

## 환경 설정 업데이트

1. Adobe Analytics에서 [!UICONTROL **프로젝트**] 랜딩 페이지를 선택한 다음 [!UICONTROL **기본 설정**].

   ![사용자 환경 설정](assets/user-preferences.png)

1. 각 탭에서 사용 가능한 환경 설정에 대한 자세한 내용을 보려면 이 문서의 다음 섹션을 계속 진행합니다.

   * [일반 환경 설정](#general-preferences)

   * [프로젝트 환경 설정](#project-preferences)

   * [자유 형식 테이블 환경 설정](#freeform-table-preferences)

   * [시각화 환경 설정](#visualizations-preferences)

## 일반 환경 설정

Analysis Workspace에서 만드는 모든 새 프로젝트에 대한 일반 환경 설정을 사용자 지정할 수 있습니다. 이러한 환경 설정에 액세스하는 방법에 대한 자세한 내용은 [환경 설정 업데이트](#update-preferences)를 참조하십시오.

| 환경 설정 | 옵션 |
| --- | --- |
| 랜딩 페이지 | Adobe Analytics에 액세스할 때 기본 페이지로 표시되는 페이지를 선택합니다. <ul><li>프로젝트 목록 (기본값)</li><li>빈 프로젝트</li><li>특정 프로젝트 목록에서 선택</li></ul> |
| 팁 표시 | Analysis Workspace 오른쪽 아래 영역의 파란색 상자에 팁을 표시합니다. <p>이 옵션은 기본적으로 활성화되어 있습니다.</p> |
| 왼쪽 레일 그룹에 표시되는 구성 요소 | 왼쪽 레일의 구성 요소 메뉴에 표시할 각 구성 요소의 수를 선택합니다. <p>0을 선택하는 경우 작업 영역의 왼쪽 레일에서 구성 요소에 더 이상 액세스할 수 없습니다.</p><p>기본적으로 다음 각 항목에 대해 5개의 구성 요소가 표시됩니다.</p> <ul><li>차원</li><li>지표</li><li>필터</li><li>날짜 범위</li></ul> <p>Analysis Workspace의 구성 요소에 대한 자세한 내용은 [구성 요소 개요](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)를 참조하십시오.</p> |

## 프로젝트 환경 설정

Analysis Workspace에서 만든 모든 새 프로젝트의 프로젝트 환경 설정을 사용자 정의할 수 있습니다. 이러한 환경 설정에 액세스하는 방법에 대한 자세한 내용은 [환경 설정 업데이트](#update-preferences)를 참조하십시오.

[프로젝트 개요](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)의 설명에 따라 개별 프로젝트에 맞게 동일한 환경 설정 중 일부를 사용자 정의할 수도 있습니다.

각 환경 설정에 대한 자세한 내용과 컨텍스트를 보려면 링크된 환경 설정 제목을 클릭합니다.

| 섹션 | 환경 설정 | 옵션 |
| --- | --- | --- |
| **표시** |  |  |
|  | [보기 밀도](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=ko-KR) | 자유 형식 테이블 및 집단 테이블에서 왼쪽 레일의 수직 안쪽 여백을 줄여 화면에 표시해야 할 콘텐츠 양을 선택합니다. <ul><li>콤팩트</li><li>편안함</li><li>확장됨 (기본값)</li></ul> |
|  | [색상 팔레트](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html?lang=ko-KR) | Analysis Workspace에 사용되는 시각화 색상 팔레트를 선택합니다. <ul><li>Adobe 제공 팔레트 (기본값)</li><li>조건부 서식 팔레트 </li><li>위/아래 팔레트 (분기)<li>사용자 정의 팔레트</li></ul> |
| **데이터** |  |  |
|  | [보고서 세트](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko-KR?#report-suite) | 테이블 및 시각화가 데이터를 도출하는 위치에서 선택합니다. <ul><li>가장 최근 (기본값)</li><li>목록에서 선택한 특정 보고서 세트</li></ul> |
|  | [달력](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko-KR?#calendar) | 다음 목록에서 선택: <ul><li>Adobe 제공 범위 (기본값은 이번 달)</li><li>사용자 정의 범위</li></ul> |
|  | [패널 유형](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko-KR) | <ul><li>자유형 (기본값)</li><li>빈</li><li>빠른 인사이트</li></ul> |
|  | 반복 인스턴스 계산 | 보고서에서 반복 인스턴스가 카운트되는지 여부를 지정합니다. 예를 들어 이 설정(활성화된 경우)은 동일한 페이지에 대한 여러 개의 연속 페이지 조회수를 여러 페이지 조회수로 처리합니다. 이 설정을 끄면 단일 페이지 조회수로 카운트됩니다. <p>**참고:** 이 설정은 특정 지표(예: 단일 페이지 방문)에만 영향을 주고 흐름 또는 폴아웃 시각화에 적용되지 않습니다.</p> |
|  | 번호 형식 | <ul><li>1,000.00 (기본값)</li><li>1.000,00</li><li>1 000,00</li></ul> |
|  | CSV 구분 기호 문자 | <ul><li>쉼표 (기본값)</li><li>세미콜론</li><li>콜론</li><li>파이프</li><li>기간</li><li>공백</li><li>탭</li></ul> |
|  | 주석 표시 | 프로젝트에 주석을 표시할지 여부를 선택합니다. 주석에 대한 자세한 내용은 [주석 개요](/help/analyze/analysis-workspace/components/annotations/overview.md)를 참조하십시오. |

## 자유 형식 테이블 환경 설정

Analysis Workspace에서 만든 모든 새 프로젝트의 자유 형식 테이블 환경 설정을 사용자 정의할 수 있습니다. 이러한 환경 설정에 액세스하는 방법에 대한 자세한 내용은 [환경 설정 업데이트](#update-preferences)를 참조하십시오.

개별 프로젝트에 맞게 동일한 환경 설정 중 일부를 사용자 정의할 수도 있습니다.

사용 가능한 환경 설정에 대한 자세한 내용과 컨텍스트를 보려면 링크된 섹션 제목을 클릭합니다.

| 섹션 | 환경 설정 | 옵션 |
| --- | --- | --- |
| **표** |  |  |
|  | 테이블 유형 | <ul><li>자유 형식</li><li>테이블 빌더</li></ul> |
|  | 기본 테이블 지표 | <ul><li>발생 횟수</li><li>고유 방문자 수</li><li>방문 횟수</li></ul> |
|  | 기본 테이블 차원 | 분, 시간, 일, 주, 월, 분기 또는 연도 중에서 선택합니다. |
|  | 날짜 정렬 | 이 옵션을 선택하여 각 열의 날짜가 같은 행에서 시작하도록 맞춥니다. |
| **[열](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** |  |  |
|  | 머리글 텍스트 줄바꿈 | 자유 형식 테이블의 머리글 텍스트를 줄바꿈하여 머리글을 더 읽기 쉽게 하고 테이블을 더 공유하기 쉽게 할 수 있습니다. 이 기능은 .pdf 렌더링 및 긴 이름을 사용하는 지표에 유용합니다. 기본적으로 사용됩니다. |
|  | 합계 표시 | 이 합계는 일반적으로 [!UICONTROL 총 합계]와 같거나 그 하위 집합입니다. [!UICONTROL 포함 내용 없음] 선택 사항을 포함하여 자유 형식 테이블 내에 적용된 테이블 필터를 반영합니다. |
|  | 총계 표시 | 이 합계는 수집 된 모든 히트 수를 나타내며 “보고서 세트 합계”라고도 합니다. 세그먼트가 패널 수준에서 또는 자유 형식 테이블 내에서 적용되면 이 합계는 세그먼트 기준과 일치하는 모든 히트를 반영하도록 조정됩니다. [정적 행](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md)이 있는 테이블 또는 분류에서는 총 합계가 지원되지 않습니다. |
|  | 스파크라인 표시 | 차트 하단에 라인 차트를 표시하거나 숨깁니다. 범례가 숨겨져 있으면 더 이상 시각적으로 선을 참조하지 않습니다. |
|  | 숫자 | 셀에 지표에 대한 숫자 값을 표시할지 또는 숨길지를 결정합니다. 예를 들어 지표가 페이지 조회수이면 숫자 값은 행 항목에 대한 페이지 조회수입니다. |
|  | 비율 | 셀에 지표에 대한 퍼센트 값을 표시할지 또는 숨길지를 결정합니다. 예를 들어 지표가 페이지 조회수이면 퍼센트 값은 행 항목에 대한 페이지 조회수를 해당 열에 대한 총 페이지 조회수로 나눈 수입니다.  참고: 정확하게 말하자면 100%보다 큰 백분율을 표시할 수 있습니다. 또한 열의 너비를 크게 늘릴 수 있도록 상한을 1,000%로 옮겼습니다. |
|  | 예외 항목 표시 <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | 이 열의 값에 대해 예외 항목 탐지가 실행되는지 여부를 결정합니다. |
|  | 0을 값없음으로 해석 | 값이 0인 셀에 대해, 0을 표시할지 아니면 빈 셀을 표시할지를 결정합니다. 달의 각 날에 대한 데이터를 보고 일부 날은 아직 일어나지 않은 경우 유용합니다.  차후의 날짜에 대해 0을 표시하는 대신 빈 셀을 표시할 수 있습니다. 차트에 이 설정도 적용됩니다(즉, 이 설정을 선택한 경우 차트에 값이 0인 줄 또는 막대가 표시되지 않습니다). |
|  | 배경 | 막대 그래프 및 조건부 서식을 포함하여, 셀에 모든 셀 서식을 표시할지 또는 숨길지를 결정합니다 <ul><li>막대 그래프</li> 열에 대한 합계와 상대적인 셀 값을 나타내는 수평 막대 그래프를 표시합니다. <li>조건부 서식</li>조건부 서식에 대한 자세한 내용은 [열 설정](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)의 “조건부 서식”을 참조하십시오.</ul> |
|  | 셀 미리보기 | 각 셀이 현재 선택된 서식 선택 사항이 적용되면 어떻게 나타나는지 미리보기를 표시합니다. |
| **[행](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** |  |  |
|  | 위치별 분류 | 분류를 항목 자체가 아닌 항목 위치로 유지하려면 이 옵션을 선택합니다. 분류에 대한 자세한 내용은 [차원 분류](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)를 참조하십시오. |
|  | 백분율 계산 | <ul><li>열</li><li>행</li></ul> |

## 시각화 환경 설정

Analysis Workspace에서 만든 모든 새 프로젝트의 시각화 환경 설정을 업데이트할 수 있습니다. 이러한 환경 설정에 액세스하는 방법에 대한 자세한 내용은 [환경 설정 업데이트](#update-preferences)를 참조하십시오.

개별 시각화에 맞게 동일한 환경 설정 중 일부를 사용자 정의할 수도 있습니다.

사용 가능한 환경 설정에 대한 자세한 내용과 컨텍스트를 보려면 링크된 섹션 제목을 클릭합니다.

| 섹션 | 환경 설정 | 옵션 |
| --- | --- | --- |
| **일반 기본값** |  |  |
|  | 백분율 | 모든 시각화 값을 백분율로 표시합니다. |
|  | 범례 표시 | 모든 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
|  | 최대 항목 수 제한 | 모든 시각화에 대한 X축의 항목 수를 줄입니다. 대규모 데이터 세트가 있는 경우 유용할 수 있습니다. |
|  | 이중 축 표시 (해당되는 경우) | 지표가 두 개일 경우에만 적용됩니다. 왼쪽(한 지표에 대해)과 오른쪽(다른 지표에 대해)에 y축을 놓을 수 있습니다. 그려진 지표의 크기가 매우 다른 경우에 유용합니다. |
|  | 표준화 (해당되는 경우) | 지표를 등분 비례에 강제 적용합니다. 그려진 지표의 크기가 매우 다른 경우에 유용합니다. |
|  | Y축을 0에 고정 | 차트에 표시된 모든 값이 0보다 매우 큰 경우, 차트 기본값에 따라 y축의 하단이 0이 아닌 값으로 지정됩니다. 이 상자를 선택하면 y축이 0이 됩니다(그리고 차트가 다시 그려짐). |
|  | 예외 항목으로 Y축의 크기 조절 | 차트에 여러 개의 지표가 있을 경우에는 사용자는 마우스를 각 예외 항목의 위에 놓아 해당 지표에 대한 신뢰 대역을 확인해야 합니다. 예외 항목 탐지 신뢰 구간은 시각화를 읽기 쉽게 만들기 위해 Y축 크기를 자동으로 조절하지 않습니다. 이 옵션을 통해 신뢰 구간에서 시각화 크기를 조절할 수 있습니다. <p>자세한 내용은 [Analysis Workspace에서 예외 항목 보기](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/view-anomalies.md)를 참조하십시오.</p> |
| **[라인](/help/analyze/analysis-workspace/visualizations/line.md)** |  |  |
|  | 백분율 | 라인 시각화 값을 백분율로 표시합니다. |
|  | 범례 표시 | 라인 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
|  | 최대 항목 수 제한 | 라인 시각화에서 X축의 항목 수를 줄입니다. 대규모 데이터 세트가 있는 경우 유용할 수 있습니다. |
|  | 이중 축 표시 (해당되는 경우) | 지표가 두 개일 경우에만 적용됩니다. 왼쪽(한 지표에 대해)과 오른쪽(다른 지표에 대해)에 y축을 놓을 수 있습니다. 그려진 지표의 크기가 매우 다른 경우에 유용합니다. |
|  | 표준화 (해당되는 경우) | 지표를 등분 비례에 강제 적용합니다. 그려진 지표의 크기가 매우 다른 경우에 유용합니다. |
|  | X축 표시 | 라인 차트에 X축을 표시합니다. |
|  | Y축 표시 | 라인 차트에 Y축을 표시합니다. |
|  | Y축 고정 | 차트에 표시된 모든 값이 0보다 매우 큰 경우, 차트 기본값에 따라 y축의 하단이 0이 아닌 값으로 지정됩니다. 이 상자를 선택하면 y축이 0이 됩니다(그리고 차트가 다시 그려짐). |
|  | 최소 표시 | 최소값 레이블을 오버레이하여 지표의 최저점을 빠르게 강조 표시합니다. 참고: 최소값은 차원 내의 전체 값 집합이 아니라 시각화에 표시되는 데이터 포인트에서 파생됩니다. |
|  | 최대 표시 | 최대값 레이블을 오버레이하여 지표의 최고점을 빠르게 강조 표시합니다. 참고: 최대값은 차원 내의 전체 값 집합이 아니라 시각화에 표시되는 데이터 포인트에서 파생됩니다. |
|  | 트렌드 라인 표시 | 라인 시리즈에 회귀 또는 이동 평균 추세선을 표시합니다. 트렌드 라인은 데이터의 명확한 패턴을 표현하는 데 도움이 됩니다. |
| **[집단](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md)** |  |  |
|  | 세부 기간 | 트렌드 시각화의 경우 시간 단위(일, 주, 월, 분기 또는 연도)를 변경할 수 있습니다. 이 변경 사항은 데이터 소스 테이블에도 적용됩니다. |
|  | 백분율만 표시 | 숫자 값을 제거하고 백분율만 표시합니다. |
|  | 백분율 반올림 | 백분율 값을 소수 값으로 표시하지 않고 가장 가까운 정수로 반올림합니다. |
|  | 평균 백분율 행 표시 | 테이블의 맨 위에 새 행을 삽입한 다음 각 열 내의 값에 대한 평균을 추가합니다. |
|  | 집단 미리보기 | 색상 팔레트가 집단 시각화에 어떻게 표시되는지 미리보기. |
|  | 코호트 팔레트 | 집단 시각화에 사용되는 색상 팔레트. |
| **[콤보 차트](/help/analyze/analysis-workspace/visualizations/combo-charts.md)** |  |  |
|  | X축 표시 | 콤보 차트에 X축을 표시합니다. |
|  | Y축 표시 | 콤보 차트에 Y축을 표시합니다. |
|  | 선에 바벨 표시 | 콤보 차트의 라인에 바벨을 표시합니다. |
| **[주요 지표 요약](/help/analyze/analysis-workspace/visualizations/key-metric.md)** |  |  |
|  | 요약 표시 유형 | <ul><li>백분율 변경 강조</li><li>숫자 값 강조</li></ul> |
|  | 스파크라인 표시 | 차트 하단에 라인 차트를 표시하거나 숨기는 방법. 범례가 숨겨져 있으면 더 이상 시각적으로 선을 참조하지 않습니다. |
|  | 스파크라인에서 최대 및 최소 표시 | 기본 및 비교 라인 차트에서 최소값 및 최대값 표시 또는 숨기기. |
|  | 비교 보기 | 비교 데이터 표시. 숨겨진 경우 보기에서 비교 라인 차트와 요약 변경 오브젝트가 모두 표시되지 않습니다. |
|  | 숫자 값 옵션 | [!UICONTROL **주요 지표 요약**] 섹션에서 <ul><li>백분율 변경 표시</li><li>원시 차이 표시</li>기본 날짜 범위와 보조 날짜 범위의 총 지표 값 간의 원시 차이</ul> |
| **[폴아웃](/help/analyze/analysis-workspace/visualizations/fallout/configuring-fallout.md)** |  |  |
|  | 컨테이너 | 방문과 방문자 간을 변환하여 방문자 이동 경로를 분석할 수 있도록 합니다. 기본값은 방문자입니다. 이 설정은 방문들에 대해 방문자 수준에서 방문자 참여를 이해하거나 분석을 단일 방문으로 제한하는 데 도움이 됩니다. <p>다음 옵션을 사용할 수 있습니다.</p> <ul><li>방문</li><li>방문자</li></ul> |
| **[플로우](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md)** |  |  |
|  | 컨테이너 | [!UICONTROL **흐름**] 섹션에서 <ul><li>방문</li><li>방문자</li></ul> |
|  | 줄 바꿈 레이블 | 대개 흐름 요소의 레이블은 화면 공간을 절약하기 위해 잘리지만 이 상자를 선택하여 전체 레이블을 표시할 수 있습니다. 기본값 = 선택 해제. |
|  | 반복 인스턴스 포함 | 플로우 시각화는 차원의 인스턴스를 기반으로 합니다. 이 설정은 반복된 인스턴스 (예: 페이지 다시 로드)를 포함하거나 제외하는 옵션을 제공합니다. 하지만 listVars, listProp, s.product, 머천다이징 eVar 등과 같이 여러 값을 갖는 차원을 포함하는 플로우 시각화에서는 반복을 제거할 수 없습니다. 기본값 = 선택 해제. |
|  | 툴팁 표시 | 흐름 시각화에서 마우스로 개별 노드를 가리킬 때 노드 데이터를 포함하는 도구 설명이 표시되는지 여부를 결정합니다. |
|  | 열 수 | 플로우 다이어그램에 사용할 열 수를 결정합니다. |
|  | 열당 항목 확장됨 | 각 열에 원하는 항목 수입니다. |
| **스택형 차트** |  |  |
|  | 100% 누적 | 스택 영역, 막대 스택 또는 가로 막대형 스택 시각화에 대한 이 설정은 차트를 “100% 스택”시각화로 전환합니다. <p>자세한 내용은 [막대 및 스택 막대](/help/analyze/analysis-workspace/visualizations/bar.md)를 참조하십시오.</p> |
| **[히스토그램](/help/analyze/analysis-workspace/visualizations/histogram.md)** |  |  |
|  | 버킷 수 | 시각화에서 데이터 범위(버킷) 수를 선택합니다. 최대 버킷 수는 50개입니다. <p>자세한 내용은 [히스토그램](/help/analyze/analysis-workspace/visualizations/histogram.md)을 참조하십시오.</p> |
|  | 계산 방법 | 다음 선택 사항 중 하나를 선택합니다. <ul><li>히트</li><li>방문</li><li>방문자</li></ul> <p>예를 들어 페이지 조회수와 함께 사용될 때 방문자당 페이지 조회수, 방문 페이지 조회수 또는 히트당 페이지 조회수를 선택할 수 있습니다. 히트의 경우 “발생 횟수”는 자유형 테이블에서 Y축 지표로 사용됩니다.</p> |
| **[맵](/help/analyze/analysis-workspace/visualizations/map-visualization.md)** |  |  |
|  | 플로팅 차원 | <ul><li>모바일 위도/경도</li><li>지리적 차원</li></ul> |
|  | 맵 유형 | <ul><li>버블</li><li>히트맵</li></ul> |
|  | 색상 테마 | Coral, Reds, Greens, Blues, Heatmap 및 Positive/Negative 중에서 선택할 수 있습니다. |
|  | 맵 스타일 | Basic, Street, Bright, Light, Dark 및 Satellite 중에서 선택할 수 있습니다. |
| **[요약 변경](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** |  |  |
|  | 값 | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>백분율 변경</li><li>원시 차이</li></ul> |
|  | 백분율 | 요약 변경 시각화 값을 백분율로 표시합니다. |
|  | 범례 표시 | 요약 변경 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
| **[요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** |  |  |
|  | 백분율 | 요약 번호 시각화 값을 백분율로 표시합니다. |
|  | 범례 표시 | 요약 번호 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
|  | 기준별 요약 값 | 최대, 최소, 평균, 중앙값 및 합계 중에서 선택합니다. |
|  | 값 생략 | [!UICONTROL **요약 번호**] 섹션에서 |
| **[트리맵](/help/analyze/analysis-workspace/visualizations/treemap.md)** |  |  |
|  | 백분율 | 트리맵 시각화 값을 백분율로 표시합니다. |
|  | 최대 항목 수 제한 | 트리맵 시각화에서 X축의 항목 수를 줄입니다. 대규모 데이터 세트가 있는 경우 유용할 수 있습니다. |
| **[벤](/help/analyze/analysis-workspace/visualizations/venn.md)** |  |  |
|  | 범례 표시 | 벤 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
| **[분산](/help/analyze/analysis-workspace/visualizations/scatterplot.md)** |  |  |
|  | 백분율 | 분산 시각화 값을 백분율로 표시합니다. |
|  | 범례 표시 | 분산 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
|  | 최대 항목 수 제한 | 분산 시각화에서 X축의 항목 수를 줄입니다. 대규모 데이터 세트가 있는 경우 유용할 수 있습니다. |
|  | Y축을 0에 고정 | 차트에 표시된 모든 값이 0보다 매우 큰 경우, 차트 기본값에 따라 y축의 하단이 0이 아닌 값으로 지정됩니다. 이 상자를 선택하면 y축이 0이 됩니다(그리고 차트가 다시 그려짐).  |

## 회사 환경 설정

조직 내의 모든 사용자 및 프로젝트에 적용되는 회사 환경 설정을 업데이트할 수 있습니다. 이러한 환경 설정에 액세스하는 방법에 대한 자세한 내용은 [환경 설정 업데이트](#update-preferences)를 참조하십시오.

| 섹션 | 환경 설정 | 옵션 |
| --- | --- | --- |
| **보고서 탭** |  |  |
|  | 보고서 탭 숨기기 | 조직의 모든 사용자에 대한 보고서 탭을 숨깁니다. |

{style=&quot;table-layout:auto&quot;}

## 기본 환경 설정 복원

모든 사용자 환경 설정을 시스템 기본값으로 복원할 수 있습니다. 이는 회사 탭 아래의 관리자 환경 설정에 영향을 주지 않습니다.

이 작업은 실행 취소할 수 없습니다.

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] **>** [!UICONTROL **환경 설정**]&#x200B;을 선택합니다.

   ![사용자 환경 설정](assets/user-preferences.png)

1. 오른쪽 상단에서 **[!UICONTROL 기본값 복원]**&#x200B;을 선택합니다.

1. 메시지가 표시되면 **[!UICONTROL 기본값 복원]**&#x200B;을 선택합니다.

## [!UICONTROL 어두운 테마]

Adobe Analytics 사용자 인터페이스에 어두운 배경을 사용하려는 경우 [!UICONTROL 어두운 테마]로 전환할 수 있습니다.

1. 오른쪽 상단에서 Experience Cloud 사용자 아이콘을 클릭합니다.

   ![dark-theme](assets/dark-theme.png)

1. **[!UICONTROL 어두운 테마]** 토글을 오른쪽으로 이동합니다.

