---
description: '히스토그램은 Analysis Workspace의 새로운 시각화 유형입니다. '
title: 히스토그램
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 히스토그램

히스토그램은 막대 그래프와 유사하지만 숫자들을 범위로 그룹화합니다(버킷). Analytics는 숫자를 범위로 "버킷하는 것"을 자동화하지만, [고급 설정](#section_09D774C584864D4CA6B5672DC2927477)에서 설정을 변경할 수 있습니다. 

## 히스토그램 작성 {#section_74647707CC984A1CB6D3097F43A30B45}

히스토그램을 만드는 방법:

1. 왼쪽 레일에서 **[!UICONTROL 시각화]**&#x200B;를 클릭합니다. 
1. **[!UICONTROL 히스토그램]**&#x200B;을 패널로 드래그합니다. 
1. 히스토그램 시각화로 드래그할 지표를 선택하고 **[!UICONTROL 작성]**&#x200B;을 클릭합니다.

![](assets/histogram.png)

> [!NOTE] 히스토그램은 계산된 지표는 지원하지 않고 표준 지표만 지원합니다. 

여기에서는 고유 방문자 수에 대한 페이지 보기 횟수를 사용했습니다. 첫 번째(왼쪽) 버킷은 고유 방문자에 대한 1개의 페이지 보기에 해당하고 두 번째 버킷은 2개의 페이지 보기 등에 해당합니다. 

![](assets/histogram2.png)

## 고급 설정 {#section_09D774C584864D4CA6B5672DC2927477}

히스토그램 설정을 조정하려면 오른쪽 상단의 설정("톱니바퀴") 아이콘을 클릭하십시오. 수정할 수 있는 설정은 다음과 같습니다. 

| 히스토그램 설정 | 설명 |
|---|---|
| 버킷 시작 | 히스토그램이 시작되는 버킷을 결정합니다. 1이 기본값입니다. 시작 숫자를 0부터 무한대까지 설정할 수 있습니다(음수는 안 됨).  |
| 지표 버킷 | 데이터 범위(버킷)의 수를 늘이거나 줄일 수 있습니다. 최대 버킷 수는 50개입니다. |
| 지표 버킷 크기 | 각 버킷의 크기를 설정할 수 있습니다. 예를 들어 버킷 크기를 페이지 보기 1개에서 페이지 보기 2개로 변경할 수 있습니다.  |
| 계산 방법 | [방문자](https://marketing.adobe.com/resources/help/ko_KR/reference/visitors.html), [방문](https://marketing.adobe.com/resources/help/ko_KR/reference/metrics_visit.html) 또는 [히트](https://marketing.adobe.com/resources/help/ko_KR/reference/hit.html) 중에서 선택할 수 있습니다. 예를 들면 방문 당 페이지 보기 수, 방문자 당 페이지 보기 수 또는 히트 당 페이지 보기 수 중에서 선택할 수 있습니다. 히트의 경우 "발생 횟수"는 자유형 테이블에서 y축 지표로 사용됩니다. |

**예**:

* 버킷 시작: 1; 지표 버킷: 5; 지표 버킷 크기: 2를 설정하면 다음의 히스토그램이 만들어짐: 1-2, 3-4, 5-6, 7-8, 9-10.
* 버킷 시작: 0; 지표 버킷: 3; 지표 버킷 크기: 5를 설정하면 다음의 히스토그램이 만들어짐: 0-4, 5-9, 10-14

## 히스토그램 데이터 보기 및 편집 {#section_B2CD7CDF0F6B432F928103AE7AAA3617}

히스토그램 차트에 대한 데이터 소스를 보거나 변경하려면, 히스토그램 헤더의 옆에 있는 점을 클릭하여 **[!UICONTROL 데이터 소스 설정]** &gt; **[!UICONTROL 데이터 소스 표시]**&#x200B;로 이동합니다.

![](assets/manage-data-source.png)

표에 표시되는 사전에 작성된 세그먼트는 내부 세그먼트이며, 세그먼트 선택기에 나타나지 않습니다. 세그먼트 이름의 옆에 있는 "i" 아이콘을 클릭한 다음, **[!UICONTROL 공개하기]**&#x200B;를 클릭하여 세그먼트를 공개로 만듭니다.

![](assets/prebuilt_segments.png)

데이터 분류 수행과 같이, 자유 형식 데이터 테이블 및 기타 시각화를 관리하는 방법을 더 탐색하려면, [여기](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/freeform-analysis-visualizations.html)로 이동하십시오. 
