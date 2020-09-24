---
description: 'Analysis Workspace의 구성 요소는 프로젝트로 드래그하여 놓을 수 있는 차원, 지표, 세그먼트 및 날짜 범위로 구성됩니다. '
title: 구성 요소 개요
translation-type: tm+mt
source-git-commit: a290e5790591d73c397b2eb99f0c070e0ea71b10
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 13%

---


# 구성 요소 개요

Analysis Workspace의 구성 요소는 프로젝트로 드래그하여 놓을 수 있는 차원, 지표, 세그먼트 및 날짜 범위로 구성됩니다.

To access the Components menu, click the **[!UICONTROL Components]** icon in the left rail. 왼쪽 레일 아이콘 [에서](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/panels.html)또는 [핫키를 사용하여](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html)패널, 시각화 및 구성 요소 간에 전환할 수 [있습니다](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

![](assets/component-overview.png)

또한 프로젝트 > 프로젝트 정보 및 설정 > 밀도 보기로 이동하여 프로젝트 [의 밀도 보기 설정을](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) 조정하여 왼쪽 레일에 있는 더 많은 값을 한 번에 볼 수도 **[!UICONTROL 있습니다]**.

## 차원 {#dimensions}

[**Dimension**](https://docs.adobe.com/content/help/en/analytics/components/dimensions/overview.html) 는 방문자의 행동을 설명하고 분석에서 보고 분류하고 비교할 수 있는 텍스트 특성입니다. 왼쪽 구성 요소 레일(주황색 섹션)에서 찾을 수 있으며 일반적으로 표의 행으로 적용됩니다.

차원의 예로는 [!UICONTROL 페이지 이름], [!UICONTROL 마케팅 채널], [!UICONTROL 장치 유형]및 제품 등이 있습니다. Dimension은 Adobe에서 제공되며 사용자 지정 구현(eVar, Prop, 분류 등)을 통해 캡처됩니다.

각 차원에는 **차원 항목도** 포함되어 있습니다. Dimension 항목은 차원 이름 옆에 있는 오른쪽 화살표를 클릭하여 왼쪽 구성 요소 레일에서 찾을 수 있습니다(항목은 노란색).

차원 예로는 홈 페이지 [!UICONTROL (] 페이지 [!UICONTROL 차원 내),] 유료 검색 [!UICONTROL (Marketing Channel 차원 내] ), TabletWithin [!UICONTROL Mobile Device TypeDimension) 및 기타 등이 있습니다]   .

![](assets/dimensions.png)

## 지표 {#metrics}

[**지표는**](https://docs.adobe.com/content/help/en/analytics/components/metrics/overview.html) 방문자 행동에 대한 수량 측정값입니다. 왼쪽 구성 요소 레일(녹색 섹션)에서 찾을 수 있으며 일반적으로 표의 열로 적용됩니다.

지표의 예로는 [!UICONTROL 페이지 보기 횟수, [!UICONTROL 방문], [!UICONTROL 주문 수], [!UICONTROL 평균 체류]시간 [!UICONTROL 및 매출/주문]시간이 있습니다. 지표는 Adobe에서 제공하거나 사용자 지정 구현([!UICONTROL 성공 이벤트])을 통해 캡처하거나 [계산된 지표 빌더를 사용하여 만듭니다](https://docs.adobe.com/content/help/ko-KR/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html).

![](assets/metrics.png)

## 세그먼트 {#segments}

[**세그먼트는**](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html) 분석에 적용되는 대상 필터입니다. 왼쪽 구성 요소 레일(파란색 섹션)에서 찾을 수 있으며 일반적으로 표의 패널 상단 또는 위 지표 열에 적용됩니다.

세그먼트 예로는 [!UICONTROL 모바일 장치 방문자], [!UICONTROL 이메일의 방문]및 [!UICONTROL 인증된 히트]가 있습니다. 세그먼트는 Adobe에서 제공하거나 [패널 드롭존에서](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/panels.html)만들거나 [세그먼트 빌더를 사용하여 만듭니다](https://docs.adobe.com/content/help/ko-KR/analytics/components/segmentation/segmentation-workflow/seg-build.html).

![](assets/segments.png)

## 데이터 범위 {#date-ranges}

[**날짜 범위는**](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) 분석을 수행하는 날짜 범위입니다. 왼쪽 구성 요소 레일(자주색 섹션)에서 찾을 수 있으며 일반적으로 각 패널의 달력에 적용됩니다.

날짜 범위의 예로는 2019년 7월, [!UICONTROL 지난 4주]및 [!UICONTROL 이번 달이 있습니다]. 날짜 범위는 Adobe에서 제공하거나 [패널 달력에](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/panels.html)적용되거나 [날짜 범위 빌더를 사용하여 만듭니다](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html).

![](assets/date-ranges.png)

## 구성 요소 작업 {#actions}

왼쪽 레일에서 구성 요소(개별적으로 또는 두 개 이상 선택)를 직접 관리할 수 있습니다. 구성 요소를 마우스 오른쪽 단추로 클릭하거나 구성 요소 목록 맨 위에 있는 작업 점 아이콘을 클릭합니다.

![](assets/component-actions.png)

| 구성 요소 작업 | 설명 |
|--- |--- |
| 태그 | 구성 요소에 태그를 적용하여 구성 요소를 구성하거나 관리합니다. 그런 다음 필터를 클릭하거나 #을 입력하여 왼쪽 레일에서 태그로 검색할 수 있습니다. 태그는 구성 요소 관리자도 필터 역할을 합니다. |
| 즐겨찾기 | 구성 요소를 즐겨찾기 목록에 추가합니다. 태그와 마찬가지로 왼쪽 레일의 즐겨찾기로 검색하고 구성 요소 관리자에서 해당 즐겨찾기로 필터링할 수 있습니다. |
| 승인 | 구성 요소가 조직 승인되었음을 사용자에게 알리려면 구성 요소를 승인됨으로 표시합니다. 태그와 마찬가지로 왼쪽 레일에서 승인됨으로 검색하고 구성 요소 관리자에서 기준으로 필터링할 수 있습니다. |
| 공유 | 조직의 사용자에게 구성 요소를 공유합니다. 이 옵션은 세그먼트나 계산된 지표와 같은 사용자 지정 구성 요소에만 사용할 수 있습니다. |
| 삭제 | 더 이상 필요하지 않은 구성 요소를 삭제합니다. 이 옵션은 세그먼트나 계산된 지표와 같은 사용자 지정 구성 요소에만 사용할 수 있습니다. |

사용자 지정 구성 요소는 해당 구성 요소 관리자를 통해 관리할 수도 있습니다. 예: 세그먼트 [관리자](/help/components/segmentation/segmentation-workflow/seg-manage.md).
