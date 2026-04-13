---
title: 미디어 재생 소요 시간 패널
description: Analysis Workspace에서 미디어 재생 소요 시간 패널을 사용하고 해석하는 방법에 대해 알아봅니다.
feature: Panels
role: User, Admin
exl-id: 9268baf7-b50b-4c09-a722-7bfcd4172f15
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 90%

---

# 미디어 재생 소요 시간 패널 {#media-playback-time-spent-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaplaybacktimespent_button"
>title="미디어 재생 소요 시간"
>abstract="다양한 수준의 세부 기간과 분류 및 비교 기능을 통해 시간에 따른 비디오 사용량을 분석하는 패널을 만듭니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaplaybacktimespent_panel"
>title="미디어 재생 소요 시간"
>abstract="시간 경과에 따른 비디오 사용량을 분석하고, 다양한 세부 기간을 선택하고 분석 및 비교합니다.<br/><br/>**세부 기간**: 동시 시청자를 확인할 수 있는 기간을 선택합니다.<br/>**패널 요약 숫자(선택 사항)**: 이 옵션은 각 행의 날짜 또는 시간 세부 정보가 포함된 요약 숫자를 표시합니다. 최대값은 최장 재생 체류 시간에 대한 세부 정보를 표시합니다. 최소값은 저점에 대한 세부 정보를 보여 줍니다. 합계는 재생 체류 시간의 총합에 대한 세부 정보를 보여 줍니다.<br/>**시리즈 분류(선택 사항)**: 세그먼트, 차원, 차원 항목 또는 날짜 범위별로 시각화를 분류합니다. 한 번에 최대 10개의 줄을 확인합니다. 분류는 단일 수준으로 제한됩니다.<br/>**시간 형식**: 이 옵션은 시각화에 대한 시간 형식을 시간 또는 분 단위로 표시합니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_이 문서에서는_ ![Adobe Analytics](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**&#x200B;의 미디어 재생 소요 시간 패널에 대해 설명합니다._<br/>_이 문서의 [CustomerJourneyAnalytics](/help/analyze/analysis-workspace/c-panels/media-playback-time-spent.md)Customer Journey Analytics_ ![버전은 &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**미디어 재생 시간 소요 패널**&#x200B;을 참조하십시오._

>[!ENDSHADEBOX]


>[!NOTE]
>
>미디어 분당 평균 시청 시간 패널은 스트리밍 미디어용 Adobe Analytics 추가 기능을 구입한 고객에게만 제공됩니다.
>
>자세한 내용은 Adobe 판매 팀 담당자나 Adobe 계정 팀에 문의하십시오.
>

**[!UICONTROL 미디어 재생 소요 시간]** 패널은 최대 동시 시청과 분류 및 비교 기능에 대한 세부 정보와 함께 시간 경과에 따른 재생을 분석할 수 있습니다.

Analysis Workspace에서 재생 시간이란 특정 시점에서 미디어 스트림을 보는 데 소요된 시간을 말합니다. 여기에는 일시 정지, 버퍼, 시작 시간이 포함됩니다.

스트리밍 미디어용 Adobe Analytics 추가 기능을 구매한 고객은 재생 시간을 분석하여 컨텐츠 및 뷰어 참여의 품질에 귀중한 insight을 활용할 수 있습니다. 그리고 볼륨이나 규모에 대한 문제 해결이나 계획 수립 시 도움이 됩니다.

재생 소요 시간은 다음을 이해하는 데 도움이 될 수 있습니다.

* 최대 동시 시청이 발생한 위치.

* 감소가 발생한 위치.

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [미디어 재생 소요 시간 패널](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/media-analytics/measuring-media-analytics/media-playback-time-spent-panel){target="_blank"}을 확인하십시오.

>[!ENDSHADEBOX]

## 사용

**[!UICONTROL 미디어 재생 소요 시간]** 패널 사용 방법:

1. **[!UICONTROL 미디어 재생 소요 시간]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 스트리밍 미디어용 Adobe Analytics 추가 기능에서 구성 요소를 구성한 패널에 대한 보고서 세트를 선택해야 합니다.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.


### 패널 입력

다음 입력 설정을 사용하여 미디어 재생 소요 시간 패널을 구성할 수 있습니다.

| 설정 | 설명 |
|---|---|
| 패널 날짜 범위 | 패널 날짜 범위 기본값은 오늘입니다. 단 하루 또는 여러 달이 보이도록 편집할 수 있습니다.<br>이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다. |
| 세부 기간 | 세부 기간 기본값은 분입니다.<br>이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다. |
| 패널 요약 숫자 | 재생 소요 시간의 날짜 또는 시간 세부 정보를 보려면 요약 숫자를 사용할 수 있습니다. 최대값은 최대 동시 시청에 대한 세부 정보를 표시합니다. 최소값은 저점에 대한 세부 정보를 보여 줍니다. 합계는 선택에 소요된 총 재생 시간을 합산합니다. 패널 기본값은 최대값만 표시하지만 최소값, 합계 또는 세 가지 조합을 표시하도록 변경할 수 있습니다.<br>분류를 사용하는 경우 각각에 대한 요약 숫자가 표시됩니다. |
| 시리즈 분류 | 필요에 따라 필터, 차원, 차원 항목 또는 날짜 범위별로 시각화를 분류할 수 있습니다.<p>- 한 번에 최대 10개의 줄을 볼 수 있습니다. 분류는 단일 수준으로 제한됩니다.</p><p>- 차원을 끌어오면 선택한 패널 날짜 범위를 기반으로 최상위 차원 항목이 자동으로 선택됩니다.</p>- 날짜 범위를 비교하려면 2개 이상의 날짜 범위를 시리즈 분류 필터로 끌어옵니다. |
| 시간 형식 | `Hours:Minutes:Seconds`(기본값) 또는 `Minutes`(0.5로 반올림된 정수로 표시됨)으로 소요된 재생 시간을 볼 수 있습니다. |
| 날짜 시퀀스 표시 | 두 개 이상의 날짜 범위 필터를 시리즈 분류로 배치한 경우 오버레이(기본값) 또는 순차적 중에서 선택하는 옵션이 표시됩니다. 오버레이는 공통 x축으로 시작하는 선을 표시하여 병렬로 실행되는 반면, 순차적 옵션은 특정 x축으로 시작하는 선을 표시합니다. 데이터가 정렬되면(예: 필터 1이 오후 8:44에 끝나고 필터 2가 오후 8:45에 시작됨) 선이 순차적으로 표시됩니다. |


![미디어 플레이북 소요 시간 기본 보기.](assets/mpts_default_view.png)

### 패널 출력

미디어 재생 소요 시간 패널은 최대, 최소 및/또는 소요 재생 시간 합계에 대한 세부 정보를 포함하는 라인 차트와 요약 숫자를 반환합니다. 패널 맨 위에는 선택한 패널 설정을 알려 주는 요약 줄이 제공됩니다.

언제든지 ![미디어 재생 소요 시간 패널 편집](/help/assets/icons/Edit.svg)을 선택하여 패널을 편집하고 다시 빌드할 수 있습니다.

시리즈 분류를 선택한 경우 꺾은선형 차트에 선과 요약 숫자가 각각 표시됩니다.

![선형 차트와 요약으로 표시한 미디어 재생 소요 시간.](assets/mpts_outputs1.png)

### 데이터 소스

이 패널에서 사용할 수 있는 유일한 지표는 재생 시간입니다.

| 지표 | 설명 |
|---|---|
| 재생 소요 시간 | 일시 중지, 버퍼 및 시작 시간을 포함하여 선택한 세부 기간 동안 시청한 콘텐츠의 총 `hours:minutes:seconds`(또는 `minutes`). |

## FAQ

| 질문 | 답변 |
|---|---|
| 자유 형식 테이블은 어디에 있습니까? 데이터 소스는 어떻게 볼 수 있습니까? | <p></p><p>이 보기에서는 자유 형식 테이블을 사용할 수 없습니다. 데이터 소스를 다운로드하려면 선형 차트의 컨텍스트 메뉴에서 CSV 파일을 다운로드하는 옵션을 선택합니다.</p> |
| <p>세부 기간이 변경된 이유는 무엇입니까?</p> | <p>이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다.</p><p></p><p>큰 날짜 범위에서 작은 날짜 범위로 변경하는 경우 날짜 범위가 변경되면 세부 기간이 허용되는 가장 낮은 세부 항목으로 업데이트됩니다. 더 높은 수준의 세부 기간으로 보려면 패널을 편집하고 다시 빌드하십시오.</p> |
| <p></p><p>비디오 이름, 필터, 콘텐츠 유형 등을 비교하려면 어떻게 해야 합니까?</p> | <p>단일 시각화에서 이들을 비교하려면 시리즈 분석 필터에서 필터, 차원 또는 특정 차원 항목을 끌어옵니다.</p><p></p><p>보기는 10개의 분류로 제한됩니다. 10개 이상을 보려면 여러 패널을 사용해야 합니다.</p> |
| 날짜 범위는 어떻게 비교합니까? | 단일 시각화에서 날짜 범위를 비교하려면 2개 이상의 날짜 범위를 끌어서 시리즈 분류를 사용합니다. 이러한 날짜 범위는 패널 날짜 범위보다 우선 적용됩니다. |
| 시각화 유형은 어떻게 변경합니까? | <p></p><p>이 패널은 시계열에 대한 라인 시각화만 허용합니다.</p> |
| 예외 항목 탐지를 실행할 수 있습니까? | <p></p><p>아니요. 이 패널에서는 예외 항목 탐지를 사용할 수 없습니다.</p> |


>[!MORELIKETHIS]
>
>[패널 만들기](/help//analyze/analysis-workspace/c-panels/panels.md#create-a-panel)
>[미디어 평균 분당 시청 대상자 패널](average-minute-audience-panel.md)
>[미디어 동시 뷰어 패널](media-concurrent-viewers.md)
>

<!--
# Media Playback Time Spent panel

In Analysis Workspace, Playback Time Spent is the amount of time spent viewing your media streams at a specific point in time. It includes pause, buffer, and time to start.

The Media Playback Time Spent panel enables analysis of playback over time, with details on peak concurrency and the ability to break down and compare. 

Customers who have purchased the Streaming Media Collection Add-on can analyze playback time spent to gain valuable insight into the quality of content and viewer engagement, and to help when troubleshooting or planning for volume or scale.

Playback Time Spent can help you understand:

* Where peak concurrency occurred

* Where drop-offs occurred 

Following is a video overview of this panel:

>[!VIDEO](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/media-analytics/measuring-media-analytics/media-playback-time-spent-panel)

## Use the Media Playback Time Spent panel

1. Go to a report suite with streaming media components enabled. 
1. Select the panel icon on the far-left, then drag the panel into your Analysis Workspace project.
1. Continue with the following sections to customize the Media Playback Time Spent panel

   * [Panel Inputs](#panel-inputs)
   * [Panel Output](#panel-output)

## Panel Inputs {#Input}

You can configure the Media Playback Time Spent panel using these input settings:

|Setting|Description|
|---|---|
|Panel date range|The panel date range default is Today. You may edit it to view a single day or many months at a time.<br>This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity). If a date range and granularity combination results in more than 1440 rows, the granularity is automatically updated to accommodate the full date range.|
|Granularity|The granularity default is Minute.<br>This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity). If a date range and granularity combination results in more than 1440 rows, the granularity is automatically updated to accommodate the full date range.|
|Panel summary numbers|To see date or time details for playback time spent, a summary number is available. The Maximum shows details for peak concurrency. The Minimum shows details for the trough. Sum adds up the total playback time spent for the selection. The panel default shows Maximum only, but you can change it to show Minimum, Sum, or any combination of the three.<br>If you are using breakdowns, a summary number is displayed for each.|
|Series breakdown|Optionally, you can break down your visualization by segments, dimensions, dimension items, or date ranges.<p>- You may view up to 10 lines at a time. Breakdowns are limited to a single level.</p><p>- When dragging a dimension, the top dimension items will be automatically selected based on the selected panel date range.</p>- To compare date ranges, drag 2 or more date ranges into the series breakdown filter.|
|Time format|You can view the playback time spent in either `Hours:Minutes:Seconds` (default) or in `Minutes` (which is displayed in whole numbers, rounded up at .5). |
|Date sequence display|If you've placed at least two date range segments as series breakdowns you'll see the option to select either overlay (default) or sequential. Overlay will display the lines with a common x-axis start so that they run in parallel, while sequential will display the lines with their specific x-axis start. If the data lines up (for example, segment 1 ends at 8:44 pm and segment 2 starts at 8:45 pm), then the lines will show in sequence. |

## Default view

![Default view](assets/mpts_default_view.png)

## Panel Output {#Output}

The Media Playback Time Spent panel returns a line chart and summary numbers to include details for the maximum, minimum, and/or sum of playback time spent. At the top of the panel, a summary line is provided to remind you of the panel settings you selected.

At any time, you can edit and rebuild the panel by clicking the edit pencil on the top right.

If you selected series breakdown, a line on the line chart and a summary number is displayed for each:

![media playback time spent output](assets/mpts_outputs1.png)

### Data Source

The only metric that can be used in this panel is Playback Time Spent.

|Metric|Description|
|---|---|
|Playback Time Spent|Total `hours:minutes:seconds` (or `minutes`) of content viewed during the selected granularity including pause, buffer, and time to start.|

## FAQs

|Question|Answer|
|---|---|
|Where is the Freeform table? How can I see the data source?|The Freeform table is not available in this view. You can download the data source by right-clicking on the line chart and downloading the CSV ﬁle.|
|Why did my granularity change?|This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity). If a date range and granularity combination results in more than 1440 rows, the granularity will be automatically updated to accommodate the full date range. <p>When changing from a larger date range to a smaller one, the granularity will be updated to the lowest detail allowable once the date range is changed. To view a higher granularity, edit the panel and rebuild.</p>|
| How do I compare video names, segments, content types, etc?| To compare these in a single visualization, drag segments, dimensions, or speciﬁc dimension items in the series breakdown ﬁlter.The view is limited to 10 breakdowns. To view more than 10, you must use multiple panels.|
|How do I compare date ranges?|To compare date ranges in a single visualization, use the series breakdowns by dragging 2 or more date ranges. These date ranges will override the panel date range.|
|How do I change the visualization type?|This panel only allows for the line visualization for the time series.|
|Can I run anomaly detection?|No. Anomaly detection is not available for this panel.|

-->
