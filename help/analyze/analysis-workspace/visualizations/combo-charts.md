---
description: Analysis Workspace에서 지난달, 지난해 등과 비교한 내용과 같은 비교 데이터를 쉽게 시각화할 수 있습니다.
title: 콤보 차트 시각화
feature: Visualizations
role: User, Admin
exl-id: 08e49857-aa58-4527-bdfd-b1663a75a02b
source-git-commit: c0855c6bed6a9762c0440e1a8e004ee11020808e
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 95%

---

# 콤보 차트 {#combo}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_combo_button"
>title="콤보"
>abstract="우선 자유 형식 테이블을 만들지 않고도 콤보 차트 시각화를 빠르게 만듭니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

*이 문서는&#x200B;**Adobe Analytics**의 콤보 시각화에 대해 설명합니다.<br/>이 문서의&#x200B;**Customer Journey Analytics**버전에 대한 [콤보](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/combo-charts)를 참조하세요.*

>[!ENDSHADEBOX]

[!UICONTROL 콤보 차트]를 시각화하면 테이블을 만들지 않고도 비교 시각화를 빠르게 만들 수 있습니다. 데이터의 트렌드를 선/막대 조합으로 쉽게 볼 수 있습니다.

[!UICONTROL 콤보 차트] 사용

* 몇 번의 클릭만으로 이번 주 주문을 지난달과 지난해 같은 시기의 주문과 비교해 보십시오.

* 동일한 차트에서 여러 지표(예: [!UICONTROL 고유 방문자] 및 [!UICONTROL 수익])를 빠르게 분석하고 비교합니다.

* 시간대의 함수(예: [!UICONTROL 누적 평균])에 대해 지표를 분석합니다.

다음 사항을 염두에 두십시오.

* 단일 [!UICONTROL 콤보 차트]에 여러 비교를 추가할 수 있습니다.
* 하나 이상의 비교를 추가하는 경우 [!UICONTROL 시간 비교]와 같이 동일한 유형이어야 합니다.
* 최대 5개의 비교를 추가할 수 있습니다.
* 지표에 최대 3개의 필터(세그먼트)를 적용할 수 있습니다.
* 계산된 지표는 콤보 차트에서 지원되지 않습니다.

## 콤보 차트 빌드

1. 왼쪽 레일의 시각화 드롭다운 목록에서 [!UICONTROL 콤보 차트] 시각화를 빈 패널로 드래그합니다.

   ![](assets/combo-chart-build.png)

1. 드롭다운 목록에서 X축의 차원과 Y축의 지표를 선택합니다.

1. 사용하려는 [!UICONTROL 선 비교] 유형을 선택합니다.

   | 선 비교 유형 | 정의 |
   | --- | --- |
   | **[!UICONTROL 시간 비교]** | 예를 들어 가장 일반적인 비교 유형은 4주 전과 이 기간을 비교하는 것입니다. [!UICONTROL 시간 비교]를 선택한 경우 비교할 기간에 대해 2차 선택을 합니다.<p>![](assets/combo-time-period.png) |
   | **[!UICONTROL 함수]** | [!UICONTROL 평균]과 같은 함수를 비교에 도입할 수 있습니다. 아래에서 지원되는 함수 목록을 참조하십시오.<p>![](assets/combo-functions.png) |
   | **[!UICONTROL 보조 지표]** | 예를 들어 [!UICONTROL 수익]을 다른 지표와 비교할 수 있습니다.<p>![](assets/combo-2metrics.png) |

   {style="table-layout:auto"}

1. **[!UICONTROL 빌드]**&#x200B;를 클릭합니다.

   출력 값은 다음과 유사합니다.

   ![](assets/combo-output.png)

   현재 기간은 막대 그래프로 표시되고 비교 기간은 선 차트로 표시됩니다. 선 차트의 점을 “바벨”이라고 합니다.

## 지원되는 함수

[!UICONTROL 선 비교 유형]으로 **[!UICONTROL 함수]**&#x200B;를 선택하면 선택한 지표의 함수가 반환됩니다.

| 함수 | 정의 |
| --- | --- |
| **[!UICONTROL 열 합계]** | 열 내의 한 지표에 대한 모든 숫자 값을 추가합니다(차원 요소에 대해) |
| **[!UICONTROL 누적 평균]** | 마지막 N개 행의 평균을 반환합니다. |
| **[!UICONTROL 중간값]** | 열에 있는 지표에 대한 중간값을 반환합니다. 중간값은 숫자 세트의 중간에 있는 숫자입니다. 즉, 이 값의 반은 중간값보다 크거나 같은 값이고 다른 반은 중간값보다 작거나 같습니다. |
| **[!UICONTROL 누적]** | N개 행의 누적 합계입니다. |
| **[!UICONTROL 열 최대값]** | 지표 열에 대한 차원 요소 세트에서 가장 큰 값을 반환합니다. |
| **[!UICONTROL 평균]** | 지표에 대한 산술 평균 또는 평균을 반환합니다. |
| **[!UICONTROL 열 최소값]** | 지표 열에 대한 차원 요소 세트에서 가장 작은 값을 반환합니다. |

{style="table-layout:auto"}

다음은 수익 지표에 대한 누적 평균의 예입니다.

![](assets/combo-cumul-avg.png)

다음은 누적 평균 및 평균 함수가 모두 포함된 콤보 차트의 예입니다.

![](assets/combo-two-functions.png)

## 콤보 차트 설정

콤보 차트의 오른쪽 상단에 있는 톱니바퀴 아이콘을 클릭하여 설정을 변경합니다.

![](assets/combo-settings.png)

| 설정 | 정의 |
| --- | --- |
| **[!UICONTROL 시각화 유형]** | 다른 시각화 유형으로 전환할 수 있습니다. |
| **[!UICONTROL 세부 기간]** | 트렌드 시각화의 경우 이 드롭다운 목록에서 시간 세부기간(일, 주, 월 등)을 변경할 수 있습니다. |
| **[!UICONTROL 일반]** |  |
| **[!UICONTROL 백분율]** | 값을 백분율로 표시합니다. |
| **[!UICONTROL 범례 표시]** | 콤보 차트 시각화에 대한 자세한 범례 텍스트를 숨길 수 있습니다. |
| **[!UICONTROL 최대 항목 수 제한]** | X축의 항목 수를 줄입니다. 빅 데이터 세트가 있는 경우 처음 10개 항목(또는 선택한 값)만 표시할 수 있습니다. |
| **[!UICONTROL 오버레이]** | 선에 바벨을 표시하거나 숨깁니다. |
| **[!UICONTROL 축]** | |
| **[!UICONTROL 이중 축 표시]** | 지표가 두 개일 경우에만 적용됩니다. 왼쪽(한 지표에 대해)과 오른쪽(다른 지표에 대해)에 Y축을 놓을 수 있습니다. 그려진 지표의 크기가 매우 다른 경우에 유용합니다. 이중 축 색상은 다중 비교가 없는 한 테이블의 색상과 일치합니다. 이 경우 모든 비교에 대한 색상은 회색입니다. |
| **[!UICONTROL 표준화]** | 지표를 등분 비례에 강제 적용합니다. 그려진 지표의 크기가 매우 다른 경우에 유용합니다. |
| **[!UICONTROL X축 표시]** | X축을 표시하거나 숨깁니다. |
| **[!UICONTROL Y축 표시]** | Y축을 표시하거나 숨깁니다. |
| **[!UICONTROL Y축을 0에 고정]** | 차트에 표시된 모든 값이 0보다 매우 큰 경우 차트 기본값에 따라 y축의 하단이 0이 아닌 값으로 지정됩니다. 이 상자를 선택하면 y축이 0이 됩니다(그리고 차트가 다시 그려짐). |

{style="table-layout:auto"}
