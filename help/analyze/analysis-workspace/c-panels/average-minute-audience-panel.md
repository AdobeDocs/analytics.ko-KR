---
title: 미디어 대상 평균 시간 패널
description: Analysis Workspace에서 미디어 분당 평균 시청 시간 패널을 사용하고 해석하는 방법에 대해 알아봅니다.
feature: Panels
role: User, Admin
exl-id: be8371ee-8bc6-4a99-8527-dd94eab8a7f9
source-git-commit: 978bd8642011dd2c8e43564c90303f194689a64e
workflow-type: tm+mt
source-wordcount: '1815'
ht-degree: 98%

---

# 미디어 평균 분당 시청 대상자 패널 {#media-average-minute-audience-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaminuteaverageaudience_button"
>title="미디어 평균 분당 시청 대상자"
>abstract="특정 콘텐츠나 특정 기간 동안의 미디어 평균 분당 시청 대상자를 분석하는 패널을 만듭니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_mediaaverageminuteaudience_panel"
>title="미디어 평균 분당 시청 대상자"
>abstract="특정 미디어 콘텐츠나 사용자 정의 기간 동안의 성과를 보여 줍니다.<br/><br/>**일반 매개변수&#x200B;**<br/>**다음에 대한 지표 계산**: 지표 계산: 패널에 사용할 지표를 선택합니다. **특정 콘텐츠**&#x200B;를 선택하여 콘텐츠 길이를 기준으로 특정 콘텐츠나 이벤트에 대한 평균 분당 시청 대상자를 분석합니다. **사용자 정의 기간을 선택하여** 선택한 사용자 정의 기간 동안 평균 분당 시청 대상자가 어떻게 변하는지 분석합니다.<br/>**보고 차원**: **콘텐츠 ID** 차원의 **비디오 이름**&#x200B;별로 보고할지 선택합니다. 특정 콘텐츠를 지표로 선택한 경우에만 사용할 수 있습니다.<br/>**세부 기간**: 보고할 세부 기간을 선택합니다. 사용자 정의 기간을 지표로 선택한 경우에만 사용할 수 있습니다.<br/>**콘텐츠 필터링 기준(선택 사항)**: 특정 프로그램, 시즌, 에피소드를 선택하거나 사용자 정의 차원을 선택하여 콘텐츠를 필터링합니다.<br/><br/>**고급 설정&#x200B;**<br/>**테이블 설정**: 테이블에 계산 값을 표시할 수 있는지 여부를 선택합니다.<br/>**체류 시간 지표**: 특정 콘텐츠 계산에 사용할 체류 시간 지표를 선택합니다. 특정 콘텐츠를 지표로 선택한 경우에만 사용할 수 있습니다."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_이 문서에서는 **Customer Journey Analytics**&#x200B;의 미디어 평균 분당 시청 대상자 패널에 대해 설명합니다.<br/>이 문서의 **Adobe Analytics** 버전은 [미디어 평균 분당 시청 대상자 패널](https://experienceleague.adobe.com/ko/docs/analytics/analyze/analysis-workspace/panels/average-minute-audience-panel)을 참조하십시오.*

>[!ENDSHADEBOX]

>[!NOTE]
>
>**[!UICONTROL 미디어 평균 분당 시청 대상자 패널]**&#x200B;은 Adobe Analytics용 스트리밍 미디어 컬렉션을 구매한 고객에게만 제공됩니다.
>
>자세한 내용은 Adobe 판매 팀 담당자나 Adobe 계정 팀에 문의하십시오.
>

Analysis Workspace에서 평균 분당 시청 대상자는 다음에 대한 정보를 제공할 수 있습니다.

* 특정 미디어 스트림을 시청하는 데 소요된 시간을 콘텐츠의 지속 시간으로 나눈 값 또는
* 선택된 세부 기간에 따라 사용자 정의 기간 동안의 시청 시간.

미디어 평균 분당 시청 대상자 패널을 사용하면 모든 길이나 장르의 프로그램을 비교하여 콘텐츠의 평균 소비량을 파악할 수 있습니다. 예를 들어 30분짜리 시트콤과 3시간짜리 스포츠 경기를 비교하여 평균 소비량을 이해할 수 있습니다.

또한 미디어 평균 분당 시청 대상자 패널을 사용하여 이 디지털 평균 분당 시청 대상자를 선형 TV 평균 분당 시청 대상자 지표와 비교하거나 추가할 수 있습니다.

미디어 평균 분당 시청 대상자 패널은 평균 분당 시청 대상자 지표에 비해 다음과 같은 이점이 있습니다.

* 사용자 정의 기간 지원

* 시청 횟수가 처리된 후 기간 분류를 업데이트할 수 있습니다(기간 분류가 없거나 수정이 필요한 경우)

  지표를 사용할 때 이 업데이트를 수행하면 기간 분류가 없습니다(해당 분류가 없는 경우). 또는 기간 분류가 만료됩니다(분류가 있었지만 잘못된 경우).

## 사용

**[!UICONTROL 미디어 평균 분당 시청 대상자]** 패널을 사용하는 방법:

1. **[!UICONTROL 미디어 평균 분당 시청 대상자]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 스트리밍 미디어 컬렉션에서 구성 요소가 구성된 패널의 데이터 보기를 선택해야 합니다.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.

### 패널 입력

이 섹션에 설명된 입력 설정을 사용하여 미디어 평균 시청 대상자 패널을 구성합니다.

1. 다음 입력 설정을 구성합니다.

   | 설정 | 설명 |
   |---------|------------|
   | **패널 날짜 범위** | 패널 날짜 범위 기본값은 [!UICONTROL **이번 달**]&#x200B;입니다. 단 하루 또는 여러 달이 보이도록 편집할 수 있습니다. <br></br> 이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다. |
   | [!UICONTROL **세그먼트(또는 다른 구성 요소)를 여기에 놓습니다.**] | 다른 패널과 마찬가지로 이 설정은 사용자가 만든 세그먼트를 기반으로 선택 항목을 필터링합니다. 이 설정은 특정 플랫폼, 라이브 스트림 또는 기타 일반적인 미디어 세그먼트를 볼 수 있는 좋은 방법입니다. |
   | [!UICONTROL **다음에 대한 지표 계산**] | [**[!UICONTROL 특정 콘텐츠]**](#specific-content)에 대한 평균 분당 시청 대상자 수를 확인할지 여부를 선택합니다. 또는 [**[!UICONTROL 사용자 정의 기간]**](#custom-time-period)의 평균 분당 시청 대상자 수를 확인할 수 있습니다.<br/><br/>[!UICONTROL **사용자 정의 기간**]&#x200B;을 선택하는 방법: <ul><li>기간을 알 수 없는 경우 또는 </li><li>여러 콘텐츠가 포함된 시계열에 대한 평균 분당 시청 대상자 수를 보고 싶은 경우 또는</li><li>특정 기간이 지정되지 않은 콘텐츠(예: 라이브 스트리밍 또는 이벤트 중)의 경우</li></ul></li></li></ul> <p>이 설정은 워크플로 및 보고서 출력을 변경합니다.</p> |

1. [다음에 대한 지표 계산](#specific-content) 드롭다운 목록에서 선택한 옵션에 따라 [특정 콘텐츠](#custom-time-period) 또는 [!UICONTROL **사용자 정의 기간**]&#x200B;을 계속 진행합니다.

#### 특정 콘텐츠

1. [패널 입력 구성](#panel-inputs) 시 [!UICONTROL **다음에 대한 지표 계산**] 드롭다운 메뉴에서 [!UICONTROL **특정 콘텐츠**]&#x200B;를 선택한 경우 다음 구성 옵션을 지정합니다.

   | 설정 | 설명 |
   |---------|------------|
   | [!UICONTROL **보고 차원**] | 특정 콘텐츠를 선택하는 경우, 콘텐츠 및 연관된 분당 평균 시청 대상자를 표시하기 위해 비디오 이름 또는 콘텐츠 ID 필드를 사용하도록 보고서 출력을 선택할 수 있습니다. |
   | [!UICONTROL **콘텐츠 필터링 기준(선택 사항)**] | 원하는 보기 또는 데이터 구조화 방식에 따라 특정 콘텐츠를 필터링할 방법을 선택합니다. <ul>[!UICONTROL **쇼, 시즌, 에피소드**]: 검색을 사용해(또는 왼쪽 열에서 쇼 이름을 끌어다 놓아) 필터링할 수 있는 사용 가능한 쇼가 드롭다운에 표시됩니다. 여기에서 선택을 끝내면 쇼의 모든 시즌을 볼 수 있습니다. 또는 개별 시즌별로 필터링한 다음 개별 에피소드별로 필터링할 수 있습니다. 이 설정은 선택한 기간의 해당 쇼, 시즌 또는 에피소드에 대한 데이터를 표시합니다.</li><li>[!UICONTROL **사용자 정의 차원**]: 쇼 이름이 사용자 정의 차원에 있는 경우 차원(선택 사항) 드롭다운에서 검색하거나 왼쪽 열 검색을 사용하여 찾을 수 있습니다. 차원 항목은 해당 선택에 따라 자동으로 채워지고 에피소드로 처리됩니다.</li><li>[!UICONTROL **없음**]: 선택한 항목에 대한 분당 평균 대상자 시청 시간 데이터가 있는 모든 비디오 이름을 표시할 수 있습니다. (기본적으로 이 옵션은 선택되어 있습니다.)</li></ul> |

1. [특정 콘텐츠 고급 설정](#specific-content-advanced-settings)으로 고급 설정을 구성합니다.

#### 특정 콘텐츠 고급 설정

1. [!UICONTROL **다음에 대한 지표 계산**] 드롭다운 메뉴에서 [!UICONTROL **특정 콘텐츠**]&#x200B;를 선택하고 [!UICONTROL **고급 설정 표시**]&#x200B;를 선택한 후 다음 구성 옵션을 지정합니다.

   | 옵션 | 설명 |
   |---------|------------|
   | **[!UICONTROL 테이블 설정]** | 기본 옵션은 분당 평균 시청 대상자의 분자와 분모를 테이블의 선행 열로 표시하는 **[!UICONTROL 테이블에 계산 값 표시]**&#x200B;입니다. 이 옵션의 선택을 해제하면 두 열이 제거됩니다. 평균 분당 시청 대상자 열은 비디오 이름이나 콘텐츠 ID 옆 표에 표시됩니다. |
   | **[!UICONTROL 체류 시간 지표]** | 콘텐츠 시간만 포함하는 기본 **[!UICONTROL 체류 시간 지표]** 옵션을 선택할 수 있습니다. 또는 평균 분당 시청 대상자의 분자로 콘텐츠와 광고 시간을 함께 포함하는 **[!UICONTROL 미디어 사용 시간]**&#x200B;을 사용할 수 있습니다. |

1. [!UICONTROL **빌드**]&#x200B;를 선택하여 미디어 평균 시청 대상자 패널 만들기를 완료합니다.

1. 미디어 평균 시청 대상자자 패널 사용 방법에 대한 정보는 [패널 출력](#panel-output)을 계속 참조하십시오.

#### 사용자 정의 기간

1. [패널 입력 구성](#panel-inputs) 시 [!UICONTROL **다음에 대한 지표 계산**] 드롭다운 메뉴에서 [!UICONTROL **사용자 정의 기간**]&#x200B;을 선택한 경우 다음 구성 옵션을 지정합니다.

   | 옵션 | 설명 |
   |---------|------------|
   | **[!UICONTROL 세부 기간]** | 기본 세부 기간은 [!UICONTROL **5분**]&#x200B;이지만 선택한 기간 내에서 시계열의 분모로 사용되는 세부 기간을 선택할 수 있습니다. 예를 들어 5분 세부 기간을 사용하여 오후 12시에서 12시 30분을 선택하면 전체 30분 동안의 평균 분당 시청 대상자와 각 5분 기간에 대한 평균 분당 시청 대상자가 있는 6개의 행이 반환됩니다. 이 행은 시계열 차트에 대한 데이터 포인트로 사용됩니다. |
   | [!UICONTROL **콘텐츠 필터링 기준(선택 사항)**] | 원하는 보기 또는 데이터 구조화 방식에 따라 특정 콘텐츠를 필터링할 방법을 선택합니다. <ul>[!UICONTROL **쇼, 시즌, 에피소드**]: 검색을 사용해(또는 왼쪽 열에서 쇼 이름을 끌어다 놓아) 필터링할 수 있는 사용 가능한 쇼가 드롭다운에 표시됩니다. 여기에서 선택을 끝내면 쇼의 모든 시즌을 볼 수 있습니다. 또는 개별 시즌별로 필터링한 다음 개별 에피소드별로 필터링할 수 있습니다. 이 설정은 선택한 기간의 해당 쇼, 시즌 또는 에피소드에 대한 데이터를 표시합니다.</li><li>[!UICONTROL **사용자 정의 차원**]: 쇼 이름이 사용자 정의 차원에 있는 경우 차원(선택 사항) 드롭다운에서 검색하거나 왼쪽 열 검색을 사용하여 찾을 수 있습니다. 차원 항목은 해당 선택에 따라 자동으로 채워지고 에피소드로 처리됩니다.</li><li>[!UICONTROL **없음**]: 선택한 항목에 대한 분당 평균 대상자 시청 시간 데이터가 있는 모든 비디오 이름을 표시할 수 있습니다. (기본적으로 이 옵션은 선택되어 있습니다.)</li></ul> |

1. 고급 설정을 구성하려면 [사용자 정의 기간 고급 설정](#custom-time-period-advanced-settings)으로 계속 진행합니다.

#### 사용자 정의 기간 고급 설정

1. [!UICONTROL **다음에 대한 지표 계산**] 드롭다운 메뉴에서 [!UICONTROL **사용자 정의 기간**]&#x200B;을 선택하고 [!UICONTROL **고급 설정 표시**]&#x200B;를 선택한 후 다음 구성 옵션을 지정합니다.

   | 옵션 | 설명 |
   |---------|------------|
   | **[!UICONTROL 테이블 설정]** | 기본 설정은 평균 분당 시청 대상자의 분자와 분모를 테이블의 선행 열로 표시하는 테이블에 계산 값을 표시합니다. 이 옵션을 선택 해제하면 기간 옆에 평균 분당 시청 대상자만 남겨두고 해당 두 열이 제거됩니다. |

1. [!UICONTROL **빌드**]&#x200B;를 선택하여 미디어 평균 시청 대상자 패널 만들기를 완료합니다.

1. 미디어 평균 시청 대상자자 패널 사용 방법에 대한 정보는 [패널 출력](#panel-output)을 계속 참조하십시오.

### 패널 출력

[패널 입력 구성](#panel-inputs) 시 [!UICONTROL **다음에 대한 지표 계산**] 드롭다운 메뉴에서 [!UICONTROL **특정 콘텐츠**] 또는 [!UICONTROL **사용자 정의 기간**]&#x200B;을 선택했는지에 따라 패널 출력이 달라집니다.

#### 특정 콘텐츠

미디어 평균 분당 시청 대상자 패널은 다음을 반환합니다.

* 전체 선택 항목에 대한 총 평균 분당 시청 대상자
* 테이블에 표시되는 개별 비디오에 대한 필터 및 평균 분당 시청 대상자
* 고급 설정을 선택한 경우 콘텐츠 체류 시간 및 비디오 길이(지속 시간)

언제든지 오른쪽 상단의 ![편집](/help/assets/icons/Edit.svg)을 선택하여 패널을 편집하고 다시 작성할 수 있습니다.

![기본 보기](assets/specific-content-panel-output.png)

#### 특정 콘텐츠 데이터 소스

미디어 평균 분당 시청 대상자 패널은 평균 분당 시청 대상자 지표만 사용하여 데이터를 수집합니다. 패널에서는 분류나 기타 지표를 사용할 수 없습니다.

| 지표 | 설명 |
|--------|-------------|
| **[!UICONTROL 평균 분당 시청 대상자]** | 미디어 스트림을 보는 데 소요된 시간을 분류를 통해 제공된 비디오 길이(지속 시간)로 나눈 값입니다. |

#### 사용자 정의 기간 {#custom-time-period-output}

미디어 평균 분당 시청 대상자 패널은 다음을 반환합니다.

* 전체 선택 항목에 대한 총 평균 분당 시청 대상자

* 최대 및 최소 평균 분당 시청 대상자 수

* 전체 선택 항목에 대한 평균 분당 시청 대상자 수를 보여 주는 라인 시리즈 그래프.

* 세부 기간에 대한 필터 및 평균 분당 시청 대상자 뿐만 아니라 각 기간에 대한 콘텐츠 체류 시간 및 세부 기간을 보여 주는 테이블

  이 테이블은 고급 설정에서 [!UICONTROL **테이블에 계산 값 표시**]&#x200B;라는 옵션이 선택된 경우에만 표시됩니다.

언제든지 패널을 편집하고 다시 작성하려면 오른쪽 상단에 있는 ![미디어 평균 분당 시청 대상자 패널 편집](/help/assets/icons/Edit.svg)을 선택합니다.


#### 사용자 정의 기간 데이터 소스

미디어 평균 분당 시청 대상자 패널은 평균 분당 시청 대상자 지표만 사용하여 데이터를 수집합니다. 패널에서는 분류나 기타 지표를 사용할 수 없습니다.

| 지표 | 설명 |
|---|---|
| **[!UICONTROL 평균 분당 시청 대상자]** | 미디어 스트림을 보는 데 소요된 시간을 전체 선택 기간 또는 선택한 세부 기간(분)으로 나눈 값입니다. |


>[!MORELIKETHIS]
>
> [패널 만들기](/help/analyze/analysis-workspace/c-panels/panels.md#create-a-panel)
> > [미디어 동시 뷰어 패널](media-concurrent-viewers.md)
> > [미디어 재생 소요 시간 패널](media-playback-time-spent.md)
>


<!--

# Media average minute audience panel

>[!NOTE]
>
>The Media average minute audience panel is available only to customers who have purchased the Streaming Media Collection Add-on. 
>
>Contact your Adobe Sales Representative or Adobe Account Team to purchase the Streaming Media Collection Add-on. 

In Analysis Workspace, average minute audience is the time spent viewing your media stream divided by the duration of the content or the total selection of the period and selected granularity.

The Media average minute audience panel enables you to better understand average consumption of your content by comparing programs of any length or genre. For example, you can understand average consumption when comparing a 30-minute sitcom with a 3-hour sporting event.

In addition, you can use the Media average minute audience panel to compare or append this digital average minute audience to linear TV average minute metrics. 

The Media average minute audience panel provides the following benefits over the Average Minute Audience metric:

* Supports custom time periods

* Allows for updating the duration classification after views are processed (if it was not present or if it needs to be corrected)

  If you did this when using the metric, it either won't exist (if the classification wasn't present) or it will be out of date (if the classification was present but incorrect).

## Access the Media average minute audience panel

1. In Analysis Workspace, go to a report suite that has streaming media components enabled. 

1. In the left nav, select the **Panels** icon.

   ![Panels icon in left nav](assets/panels-icon.png)

1. Drag the [!UICONTROL **Media average minute audience**] panel onto the canvas in Analysis Workspace.

1. To configure the panel, continue with [Panel inputs](#panel-inputs).

## Panel inputs {#Input}

Use the input settings described in this section to configure the Media average minute audience panel.

1. Begin creating a Media average minute audience panel, as described in [Access the Media average minute audience panel](#access-the-media-average-minute-audience-panel).

1. Configure the following input settings:

   | Setting | Description |
   |---------|------------|
   | **Panel date range** | The panel date range default is [!UICONTROL **This month**]. You can edit it to view a single day or many months at a time. <br></br> This visualization is limited to 1440 rows of data (for example, 24-hours at minute-level granularity). If a date range and granularity combination results in more than 1440 rows, the granularity is automatically updated to accommodate the full date range. |
   | [!UICONTROL **Drop a segment here (or any other component)**] | Like other panels, this setting filters your selections based on segments you've created. This is a great way to look at specific platforms, live streams, or other common media segments. |
   | [!UICONTROL **Calculate metric for**] | Choose whether you want to see the average minute audience for a specific piece of content, or if you want to see the average minute audience for a custom period of time:<ul><li>**Specific content:** This is available only if the duration has been updated using Classifications. If the duration is unavailable, or if you want to view the average minute audience for a time series with multiple pieces of content or content without a specific assigned duration (like during a live stream or event), then you should select [!UICONTROL **Custom time period**]. (Durations can be set using Classifications either before or after processing time.)</li><li>**Custom time period:** This is available regardless of whether the durations is made available using Classifications.</li></ul> <p>This setting changes the workflow and report output.</p>  |

1. Continue with [Specific content](#specific-content) or [Custom time period](#custom-time-period), depending on the option you chose in the [!UICONTROL **Calculate metric for**] drop-down menu.

### Specific content

1. If you selected [!UICONTROL **Specific content**] in the [!UICONTROL **Calculate metric for**] drop-down menu when [configuring panel inputs](#panel-inputs), specify the following configuration options:

   | Setting | Description |
   |---------|------------|
   | [!UICONTROL **Reporting dimension**] | When you choose specific content, you can select the report output to use either the video name or content ID fields to show the content and its associated average minute audience for the time period selected. |
   | [!UICONTROL **Filter content by (optional)**] | Choose how to filter the specific content, depending on the view you want or the way your data is structured. <ul>[!UICONTROL **Show, season, episode**]: Displays your available shows in the drop-down, which you can filter using a search (or by dragging and dropping the show name from the left column). You can end your selection there to see all the seasons of your show, or you can filter by individual seasons and then by individual episodes. This setting shows the data for those shows, seasons, or episodes for the selected time period.</li><li>[!UICONTROL **Custom dimension**]: If your show name is under a custom dimension, you can find it either by searching in the dimension (optional) drop down or by using the left column search. The dimension item automatically populates based on that selection and is treated as an episode.</li><li>[!UICONTROL **None**]: Shows all the video names that have average minute audience data for the selection you've chosen. (This options is selected by default.)</li></ul>  |

1. Continue with [Specific content advanced settings](#specific-content-advanced-settings) to configure advanced settings. 

### Specific content advanced settings

1. With [!UICONTROL **Specific content**] selected in the [!UICONTROL **Calculate metric for**] drop-down menu, select [!UICONTROL **Show advanced settings**], then specify the following configuration options:

   | Setting | Description |
   |---------|------------|
   | Table settings | The default setting shows the calculation values in the table, which shows the numerator and denominator of the average minute audience as the preceding columns in the table. Deselecting this option removes those two columns, leaving only the average minute audience next to the video name or content ID. |
   | Time spent metric | You can choose the default content time spent, which includes only content time, or you can choose to use the media time spent, which includes content and ad time together as the numerator calculation for the average minute audience. |

1. Select [!UICONTROL **Build**] to finish creating the Media average minute audience panel.

1. Continue with [Panel output](#panel-output) for information about how to use the Media average minute audience panel.

### Custom time period

1. If you selected [!UICONTROL **Custom time period**] in the [!UICONTROL **Calculate metric for**] drop-down menu when [configuring panel inputs](#panel-inputs), specify the following configuration options:

   | Setting | Description |
   |---------|------------|
   | Granularity | The default granularity is [!UICONTROL **5-Minute**], but you can choose any of the granularities that are used as the denominator for the time series within your overall time period selection made in the calendar selection. For example, selecting 12:00 pm to 12:30 pm with a 5-minute granularity returns the average minute audience over the full half hour as well as six rows with the average minute audience for each 5-minute period. These rows are used as the datapoints for the time series chart. |
   | [!UICONTROL **Filter content by (optional)**] | Choose how to filter the specific content, depending on the view you want or the way your data is structured. <ul>[!UICONTROL **Show, season, episode**]: Displays your available shows in the drop-down, which you can filter using a search (or by dragging and dropping the show name from the left column). You can end your selection there to see all the seasons of your show, or you can filter by individual seasons and then by individual episodes. This setting shows the data for those shows, seasons, or episodes for the selected time period.</li><li>[!UICONTROL **Custom dimension**]: If your show name is under a custom dimension, you can find it either by searching in the dimension (optional) drop down or by using the left column search. The dimension item automatically populates based on that selection and is treated as an episode.</li><li>[!UICONTROL **None**]: Shows all the video names that have average minute audience data for the selection you've chosen. (This options is selected by default.)</li></ul>  |

1. Continue with [Custom time period advanced settings](#custom-time-period-advanced-settings) to configure advanced settings. 

### Custom time period advanced settings

1. With [!UICONTROL **Custom time period**] selected in the [!UICONTROL **Calculate metric for**] drop-down menu, select [!UICONTROL **Show advanced settings**], then specify the following configuration option:

   | Setting | Description |
   |---------|------------|
   | Table settings | The default setting displays the calculation values in the table, which displays the numerator and denominator of the average minute audience as the preceding columns in the table. Deselecting this option removes those two columns leaving only the average minute audience next to the time period. |

1. Select [!UICONTROL **Build**] to finish creating the Media average minute audience panel.

1. Continue with [Panel output](#panel-output) for information about how to use the Media average minute audience panel.

## Panel output

The panel output differs depending on whether you chose [!UICONTROL **Specific content**] or [!UICONTROL **Custom time period**] in the [!UICONTROL **Calculate metric for**] drop-down menu when [configuring panel inputs](#panel-inputs).

### Specific content

The Media average minute audience panel returns the following:

* Total average minute audience for your entire selection
* Filters and average minute audience for the individual videos displayed in a table 
* Content time spent and video length (duration) if that advanced setting was selected

To edit and rebuild the panel at any time, select the Edit (pencil) icon in the top right.

![Default view](assets/specific-content-panel-output.png)

### Specific content data source

The Media average minute audience panel uses only the Average Minute Audience metric to gather data. Breakdowns or other metrics cannot be used in the panel.

| Metric | Description |
|--------|-------------|
| Average Minute Audience | The time spent viewing your media stream divided by the video length (duration) supplied via Classifications. |

### Custom time period {#custom-time-period-output}

The Media average minute audience panel returns the following:

* The total average minute audience for your entire selection

* The maximum and minimum average minute audience

* The line series graph showing the average minute audience over the entire selection.

* A table that shows the filters and average minute audience for the granularities, as well as the content time spent and granularity for each time period 

  This table displays only if the option under advanced settings called [!UICONTROL **Show calculation values in table**] is selected.

To edit and rebuild the panel at any time, select the Edit (pencil) icon in the top right.

![concurrent viewers output](assets/custom-time-period-panel-output.png)

### Custom time period data source

The Media average minute audience panel uses only the Average Minute Audience metric to gather data. Breakdowns or other metrics cannot be used in the panel.

|Metric|Description|
|---|---|
|Average Minute Audience| The time spent viewing your media stream divided by the total selection or selected granularity in minutes.|

-->