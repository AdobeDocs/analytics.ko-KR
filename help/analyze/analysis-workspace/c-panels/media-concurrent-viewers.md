---
title: 미디어 동시 뷰어 패널
description: Analysis Workspace에서 미디어 동시 뷰어 패널을 사용하고 해석하는 방법을 알아봅니다.
feature: Panels
role: User, Admin
exl-id: 29575b51-e319-4156-9834-aa0b671afb31
source-git-commit: 978bd8642011dd2c8e43564c90303f194689a64e
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 98%

---


# 미디어 동시 뷰어 패널 {#media-concurrent-viewers-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaconcurrentviewers_button"
>title="미디어 동시 시청자"
>abstract="특정 콘텐츠나 특정 기간 동안의 미디어 평균 분당 시청 대상자를 분석하는 패널을 만듭니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaconcurrentviewers_panel"
>title="미디어 동시 시청자"
>abstract="시간 경과에 따른 동시 시청자를 분석하고, 최대 동시 시청을 확인하거나 분류 및 비교합니다.<br/><br>**세부 기간**: 동시 시청자를 확인할 수 있는 기간을 선택합니다.<br/>**패널 요약 숫자**:<br/>이 옵션은 각 행의 날짜 또는 시간 세부 정보가 포함된 요약 숫자를 표시합니다. 최대값은 최대 동시 시청에 대한 세부 정보를 표시합니다. 최소값은 저점에 대한 세부 정보를 보여 줍니다.<br/>**시리즈 분류(선택 사항)**: 세그먼트, 차원, 차원 항목 또는 날짜 범위별로 시각화를 분류합니다. 한 번에 최대 10개의 줄을 확인합니다. 분류는 단일 수준으로 제한됩니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_이 문서에서는_ ![Adobe Analytics](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**&#x200B;의 미디어 동시 뷰어 패널에 대해 설명합니다._<br/>_이 문서의 [CustomerJourneyAnalytics](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/panels/media-concurrent-viewers)Customer Journey Analytics_ ![버전은 ](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**미디어 동시 뷰어 패널**&#x200B;을 참조하십시오._

>[!ENDSHADEBOX]


>[!NOTE]
>
>미디어 평균 분당 시청 대상자 패널은 Adobe Analytics용 스트리밍 미디어 컬렉션 추가 기능을 구매한 고객에게만 제공됩니다.
>
>자세한 내용은 Adobe 판매 팀 담당자나 Adobe 계정 팀에 문의하십시오.
>

**[!UICONTROL 미디어 동시 뷰어]** 패널을 사용하면 최대 동시 시청에 대한 세부 정보와 분류 및 비교 기능을 통해 시간에 따른 동시 시청자를 분석할 수 있습니다.

동시 시청자 분석을 통해 최대 동시 시청 시간 발생 위치 또는 드롭오프가 발생한 위치를 파악하여 콘텐츠 및 시청자 참여의 품질에 대한 중요한 인사이트를 제공합니다. 그리고 볼륨이나 규모에 대한 문제 해결이나 계획 수립 시 도움이 됩니다.

Analysis Workspace에서 동시 시청자 지표는 세션 수에 관계없이 특정 시점에 미디어 스트림을 시청하는 고유 사용자 수로 정의됩니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [미디어 동시 뷰어 패널](https://video.tv.adobe.com/v/342839?quality=12&learn=on&captions=kor){target="_blank"}을 확인하십시오.

>[!ENDSHADEBOX]



## 사용

**[!UICONTROL 미디어 동시 뷰어]** 패널을 사용하는 방법:

1. **[!UICONTROL 미디어 동시 뷰어]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 스트리밍 미디어 컬렉션에서 구성 요소가 구성된 패널의 데이터 보기를 선택해야 합니다.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.

### 패널 입력

다음 입력 설정을 사용하여 미디어 동시 뷰어 패널을 구성할 수 있습니다.

| 설정 | 설명 |
|---|---|
| **[!UICONTROL 패널 날짜 범위]** | 패널 날짜 범위 기본값은 오늘입니다. 단 하루 또는 여러 달이 보이도록 편집할 수 있습니다. <br> <br>이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다. |
| **[!UICONTROL 세부 기간]** | 세부 기간 기본값은 분입니다.<br>이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다. |
| **[!UICONTROL 패널 요약 숫자]** | 동시 시청자의 날짜 또는 시간 세부 정보를 보려면 요약 숫자를 사용할 수 있습니다. 최대값은 최대 동시 시청에 대한 세부 정보를 표시합니다. **[!UICONTROL 최소값]**&#x200B;은 저점에 대한 세부 정보를 보여 줍니다. 패널 기본값은 최대값만 표시하지만 최소값 또는 최대값과 최소값을 모두 표시하도록 변경할 수 있습니다.<br><br>분류를 사용하는 경우 각각에 대한 요약 숫자가 표시됩니다. |
| **[!UICONTROL 시리즈 분류]** | 필요에 따라 필터, 차원, 차원 항목 또는 날짜 범위별로 시각화를 분류할 수 있습니다.<br>한 번에 최대 10개의 줄을 볼 수 있습니다. 분류는 단일 수준으로 제한됩니다.<br>차원을 끌어오면 선택한 패널 날짜 범위를 기반으로 최상위 차원 항목이 자동으로 선택됩니다.<br>날짜 범위를 비교하려면 2개 이상의 날짜 범위를 시리즈 분류 필터로 끌어옵니다. |

다음은 **[!UICONTROL 분]** 단위 세부 기간을 위해 구성된 패널의 예시로, **[!UICONTROL 최대]** 요약 숫자만 표시합니다. **[!UICONTROL 기타]**, **[!UICONTROL 테이블]**, **[!UICONTROL 휴대전화]**, **[!UICONTROL 게임 콘솔]**, **[!UICONTROL 미디어 플레이어]**, **[!UICONTROL 셋톱박스]**, **[!UICONTROL 텔레비전]**&#x200B;으로 분류되어 있습니다.

![미디어 동시 뷰어 시리즈 분류 보기에서는 10개 차원, 세그먼트 또는 날짜 범위 중 7개를 보여 줍니다.](assets/concurrent-viewers-series-breakdown.png)

### 패널 출력

미디어 동시 뷰어 패널은 최대 및/또는 최소 동시 시청자에 대한 세부 정보를 포함하는 꺾은선형 차트 및 요약 숫자를 반환합니다. 패널 맨 위에는 선택한 패널 설정을 알려 주는 요약 줄이 제공됩니다.

언제든지 ![동시 시청자 패널 편집](/help/assets/icons/Edit.svg)을 선택하여 패널을 편집하고 다시 구성할 수 있습니다.

시리즈 분류를 선택한 경우 꺾은선형 차트에 선과 요약 숫자가 각각 표시됩니다.

![미디어 동시 뷰어 출력.](assets/concurrent-viewers-output.png)

### 데이터 소스

이 패널에서 사용할 수 있는 유일한 지표는 **[!UICONTROL 동시 시청자]**&#x200B;입니다.

| 지표 | 설명 |
|---|---|
| **[!UICONTROL 동시 시청자]** | 세션 수에 관계없이 특정 시점에 미디어 스트림을 시청하는 고유 사용자의 수. |

이 보기에서는 자유 형식 테이블을 사용할 수 없습니다. 데이터 소스를 보려면 라인 차트 시각화 컨텍스트 메뉴에서 데이터 소스를 다운로드하고 **[!UICONTROL 데이터를 CSV로 다운로드]**&#x200B;를 선택하면 됩니다. 시리즈 분류가 포함됩니다.

![“데이터를 CSV로 다운로드”가 강조 표시된 동시 시청자 출력 옵션.](assets/concurrent-viewers-download-csv.png)

## FAQ

| 질문 | 답변 |
|---|---|
| 자유 형식 테이블은 어디에 있습니까? 데이터 소스는 어떻게 볼 수 있습니까? | 이 보기에서는 자유 형식 테이블을 사용할 수 없습니다. 라인 차트 컨텍스트 메뉴에서 데이터 소스를 다운로드하고 **[!UICONTROL 데이터를 CSV로 다운로드]**&#x200B;를 선택할 수 있습니다. |
| 세부 기간이 변경된 이유는 무엇입니까? | 이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다.<br><br>큰 날짜 범위에서 작은 날짜 범위로 변경하는 경우 날짜 범위가 변경되면 세부 기간이 허용되는 가장 낮은 세부 항목으로 업데이트됩니다. 더 높은 수준의 세부 기간으로 보려면 패널을 편집하고 다시 빌드하십시오. |
| 비디오 이름, 필터, 콘텐츠 유형 등을 비교하려면 어떻게 해야 합니까? | 단일 시각화에서 이 항목들을 비교하려면 시리즈 분석 필터에서 필터, 차원 또는 특정 차원 항목을 끌어옵니다.<br><br>보기는 10개의 분류로 제한됩니다. 10개 이상을 보려면 여러 패널을 사용해야 합니다. |
| 날짜 범위는 어떻게 비교합니까? | 단일 시각화에서 날짜 범위를 비교하려면 2개 이상의 날짜 범위를 끌어서 시리즈 분류를 사용합니다. 날짜 범위는 패널 날짜 범위보다 우선 적용됩니다. |
| 시각화 유형은 어떻게 변경합니까? | 이 패널은 시계열에 대한 라인 시각화만 허용합니다. |
| 예외 항목 탐지를 실행할 수 있습니까? | 아니요. 이 패널에서는 예외 항목 탐지를 사용할 수 없습니다. |
| 활성 세션 대신 고유 사용자를 사용하는 이유는 무엇입니까? | 고유 사용자를 사용하면 표시 경계(세션이 종료되고 동시에 시작되는 위치)에서 원하지 않는 급등을 제거할 수 있습니다. |
| 분 단위보다 세부 기간 수준이 높은 동시 뷰어가 있다는 것은 무엇을 의미합니까? | 세부 기간이 1분보다 큰 경우, 동시 시청자는 해당 시간 범위 내의 모든 분에 대한 고유 동시 시청자의 합계입니다. 예를 들어 시간 수준 세부 기간에서 동시 시청자 수는 시간 내의 모든 분에 대한 고유 동시 시청자의 합계입니다. |
| Workspace 패널에 동시 시청자 보고서와 동일한 정보가 표시됩니까? | 아니요. Analysis Workspace에서 동시 시청자 지표는 특정 시점에 미디어 스트림을 시청하는 고유 사용자 수로 정의됩니다. 세션 수와 관계가 없습니다.<br><br>이 지표는 동시 활성 세션을 사용하는 보고서 섹션의 동시 시청자 보고와 다릅니다. 고유 사용자 계정을 사용하면 표시 경계(세션이 종료되고 동시에 시작되는 위치)에서 원하지 않는 급등을 제거할 수 있습니다. |

<!-- For more information about Media Concurrent Viewers, visit [MA doc page]( https://url). -->


>[!MORELIKETHIS]
>
>[패널 만들기](/help/analyze/analysis-workspace/c-panels/panels.md#create-a-panel)
>&#x200B;>[미디어 재생 소요 시간 패널](media-playback-time-spent.md)
>&#x200B;>[미디어 평균 분당 시청 대상자 패널](average-minute-audience-panel.md)
>
<!--
# Media Concurrent Viewers panel

Customers who have purchased the Streaming Media Collection Add-on can analyze concurrent viewers to understand where peak concurrency occurred or where drop-offs happened to provide valuable insight into the quality of content and viewer engagement, and to help with troubleshooting or planning for volume or scale.

In Analysis Workspace, Concurrent Viewers is the number of unique visitors viewing your media stream(s) at a specific point in time, regardless of the number of sessions.

The Media Concurrent Viewers panel enables analysis of concurrent viewers over time, with details on peak concurrency and the ability to break down and compare.  To access the Media Concurrent Viewers panel, navigate to a report suite with streaming media components enabled. Then, click the panel icon on the far-left and drag the panel into your Analysis Workspace project.

Here is a video overview of this panel:

>[!VIDEO](https://video.tv.adobe.com/v/342839/?quality=12&captions=kor)

## Panel Inputs {#Input}

You can configure the Media Concurrent Viewers panel using these input settings:

|Setting|Description|
|---|---|
|Panel date range|The panel date range default is Today.  You may edit it to view a single day or many months at a time. <br> <br>This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity).  If a date range and granularity combination results in more than 1440 rows, the granularity is automatically updated to accommodate the full date range.|
|Granularity|The granularity default is Minute. <br> <br>This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity).  If a date range and granularity combination results in more than 1440 rows, the granularity is automatically updated to accommodate the full date range.|
|Panel summary numbers| To see date or time details for concurrent viewers, a summary number is available. The Maximum shows details for peak concurrency. The Minimum shows details for the trough.  The panel default shows Maximum only, but you can change it to show Minimum or both Maximum and Minimum.<br><br>If you are using breakdowns, a summary number is displayed for each.|
|Series breakdown| Optionally, you can break down your visualization by segments, dimensions, dimension items, or date ranges. <br><br>- You may view up to 10 lines at a time. Breakdowns are limited to a single level.<br><br>- When dragging a dimension, the top dimension items will be automatically selected based on the selected panel date range.<br><br>- To compare date ranges, drag 2 or more date ranges into the series breakdown filter.|

### Default view

![Default view](assets/concurrent-viewers-default.png)


### Series breakdown view

![series breakdown view](assets/concurrent-viewers-series-breakdown.png)

## Panel Output {#Output}

The Media Concurrent Viewers panel returns a line chart and summary numbers to include details for the maximum and/or minimum concurrent viewers.  At the top of the panel, a summary line is provided to remind you of the panel settings you selected.

At any time, you can edit and rebuild the panel by clicking the edit pencil on the top right.

If you selected series breakdown, a line on the line chart and a summary number is displayed for each:

![concurrent viewers output](assets/concurrent-viewers-output.png)

### Data Source

The only metric that can be used in this panel is Concurrent Viewers:

|Metric|Description|
|---|---|
|Concurrent Viewers| Number of unique visitors viewing your media stream(s) at a specific point in time, regardless of the number of sessions.<br><br>This is different than Concurrent Viewer reporting in the Reports section, which uses Concurrent Active Sessions.  Using unique visitors accounts for removal of unwanted 'spikes' at show boundaries (where sessions are ending and starting at the same time).|

A Freeform table is not available in this view.  In order to view the data source, you may right-click on the line chart and download as a .csv file.  Series breakdowns will be included.


![concurrent viewers output](assets/concurrent-viewers-download-csv.png)

## FAQs {#FAQ}

|Question|Answer|
|---|---|
|Where is the Freeform table? How can I see the data source?| The Freeform table is not available in this view.  You can download the data source by right-clicking on the line chart and downloading the CSV file.|
|Why did my granularity change?|This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity).  If a date range and granularity combination results in more than 1440 rows, the granularity will be automatically updated to accommodate the full date range.<br><br>When changing from a larger date range to a smaller one, the granularity will be updated to the lowest detail allowable once the date range is changed. To view a higher granularity, edit the panel and rebuild.|
|How do I compare video names, segments, content types, etc?|To compare these in a single visualization, drag segments, dimensions, or specific dimension items in the series breakdown filter.<br><br>The view is limited to 10 breakdowns.  To view more than 10, you must use multiple panels.|
|How do I compare date ranges?|To compare date ranges in a single visualization, use the series breakdowns by dragging 2 or more date ranges.  These date ranges will override the panel date range.|
|How do I change the visualization type?|This panel only allows for the line visualization for the time series.|
|Can I run anomaly detection?|No.  Anomaly detection is not available for this panel.|
|Why use unique visitors instead of active sessions?|Using unique visitors enables removal of unwanted spikes at show boundaries (where sessions are ending and starting at the same time).|
|What does it mean to have concurrent viewers at higher granularity than minute?|With a granularity larger than a minute, concurrent viewers is the sum of unique concurrent viewers for all minutes within that time range.  For example, at hour-level granularity concurrent viewers is the sum of unique concurrent viewers for all minutes within the hour.|
|Does the workspace panel show the same information as the Concurrent Viewers Report?|No.  In Analysis Workspace, Concurrent viewers is defined as the number of unique visitors viewing your media stream at a specific point in time, regardless of the number of sessions.<br><br>This is different than Concurrent Viewer reporting in the Reports section, which uses Concurrent Active Sessions.  Using unique visitors accounts for removal of unwanted spikes at show boundaries—where sessions are ending and starting at the same time.|

-->
