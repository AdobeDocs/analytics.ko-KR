---
description: 히스토그램은 Analysis Workspace의 새로운 시각화 유형입니다.
title: 히스토그램
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
feature: Visualizations
role: User, Admin
exl-id: f3dd7507-db2c-495c-b6b9-6c770c7c7ddc
source-git-commit: b2e91c9981b328aa34e03dcd3b713438732ea6b1
workflow-type: ht
source-wordcount: '338'
ht-degree: 100%

---

# 히스토그램 {#histogram}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_histogram_button"
>title="히스토그램"
>abstract="범위 그룹의 숫자 데이터 분포를 나타내는 히스토그램 시각화를 만듭니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_이 문서에서는_ ![Adobe Analytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**&#x200B;의 히스토그램 시각화에 대해 설명합니다._<br/>_이 문서의_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** 버전은 [히스토그램](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/visualizations/histogram)을 참조하십시오._

>[!ENDSHADEBOX]


![Histogram](/help/assets/icons/Histogram.svg) **[!UICONTROL 히스토그램]** 시각화는 [!UICONTROL 막대] 그래프와 유사하지만 숫자들을 범위로 그룹화합니다(버킷). Analytics는 숫자를 범위로 “버킷팅하는 것”을 자동화하지만 [고급 설정](#advanced-settings)에서 설정을 변경할 수 있습니다.

## 사용

히스토그램을 만드는 방법:

1. ![Histogram](/help/assets/icons/Histogram.svg) **[!UICONTROL 히스토그램]** 시각화를 추가합니다. [패널 내에 시각화 추가](freeform-analysis-visualizations.md#add-visualizations-to-a-panel)를 참조하십시오.
1. **[!UICONTROL 지표]** 구성 요소 목록에서 지표를 드래그하거나, [!UICONTROL *지표 추가*] 드롭다운 메뉴에서 지표를 선택합니다.
1. (옵션) **[!UICONTROL 고급 설정 표시]**&#x200B;를 선택합니다. [고급 설정](#advanced-settings)을 확인합니다.
1. **[!UICONTROL 빌드]**&#x200B;를 선택합니다.

>[!NOTE]
>
>히스토그램은 계산된 지표는 지원하지 않고 표준 지표만 지원합니다.

아래 예에서는 히스토그램을 사용하여 세션을 사람 수에 따라 분류했습니다. 히스토그램에 따르면 대부분의 사람들이 선택한 날짜 범위 동안 16~21회 세션을 가지고 있습니다.

![](assets/histogram.png)

## 고급 설정

시각화의 일부로 특정 히스토그램 설정을 사용할 수 있습니다.

| 히스토그램 설정 | 설명 |
|---|---|
| **[!UICONTROL 버킷 시작]** | 히스토그램이 시작되는 버킷을 결정합니다. 1이 기본값입니다. 시작 숫자를 0부터 무한대까지 설정할 수 있습니다(음수는 안 됨). |
| **[!UICONTROL 지표 버킷]** | 데이터 범위(버킷)의 개수를 늘리거나 줄일 수 있습니다. 버킷의 최대 개수는 50개입니다. |
| **[!UICONTROL 지표 버킷 크기]** | 각 버킷의 크기를 설정할 수 있습니다. 예를 들어 버킷 크기를 페이지 보기 1개에서 페이지 보기 2개로 변경할 수 있습니다. |
| **[!UICONTROL 계산 방법]** | **[!UICONTROL 개인]**, **[!UICONTROL 세션]** 또는 **[!UICONTROL 이벤트]** 중에서 선택합니다. 예를 들면 세션 당 페이지 조회수, 개인별 페이지 보기 수 또는 이벤트 당 페이지 조회수 중에서 선택할 수 있습니다. |

<!--Russ or Meike - Check Hit Type link above. -->

**예**:

| 버킷 시작 | 지표 버킷 | 지표 버킷 크기 | 결과 |
|:----:|:--:|:--:|:--|
| 1 | 5 | 2 | ![히스토그램, 버킷 시작 1, 지표 버킷 5, 지표 버킷 크기 2](assets/histogram-1-5-2.png) |
| 0 | 3 | 5 | ![히스토그램, 버킷 시작 0, 지표 버킷 3, 지표 버킷 크기 5](assets/histogram-0-3-5.png) |

>[!MORELIKETHIS]
>
>[패널 내에 시각화 추가](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[시각화 설정](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[시각화 컨텍스트 메뉴](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>[히스토그램을 사용하여 예상치 못한 데이터 값 식별](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-histograms-to-identify-unexpected-data-values/ba-p/596168)

