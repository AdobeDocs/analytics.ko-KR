---
description: Analysis Workspace의 구성 요소는 프로젝트에 끌어서 놓을 수 있는 차원, 지표, 세그먼트 및 날짜 범위로 구성됩니다.
title: 구성 요소 개요
feature: Components
role: User, Admin
exl-id: e2c98c77-64ee-4349-956a-3ab092e36017
source-git-commit: 6247f44aca1e6aba6cf02ed34a0e26ef5e182021
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 71%

---

# 구성 요소 개요

Analysis Workspace의 구성 요소는 프로젝트에 끌어서 놓을 수 있는 차원, 지표, 세그먼트 및 날짜 범위로 구성됩니다.

구성 요소 메뉴에 액세스하려면 왼쪽 레일에서 **[!UICONTROL 구성 요소]** 아이콘을 클릭하십시오. 왼쪽 레일 아이콘에서 또는 [핫키](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md)를 사용하여 [패널](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko), [시각화](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=ko) 및 구성 요소 간에 전환할 수 있습니다.

![](assets/component-overview.png)

**[!UICONTROL 프로젝트 > 프로젝트 정보 및 설정 > 밀도 보기]**&#x200B;로 이동하여 프로젝트의 [밀도 보기 설정](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=ko-KR)을 조정하여 왼쪽 레일에서 한 번에 더 많은 값을 볼 수 있습니다.

## 차원 {#dimensions}

[**차원**](https://experienceleague.adobe.com/docs/analytics/components/dimensions/overview.html?lang=ko-KR)은 방문자 행동을 설명하는 텍스트 속성으로, 분석에서 보고 분류하고 비교할 수 있습니다. 차원은 왼쪽 구성 요소 레일 (주황색 섹션)에서 찾을 수 있으며 일반적으로 테이블의 행으로 적용됩니다.

차원의 예로는 [!UICONTROL 페이지 이름], [!UICONTROL 마케팅 채널], [!UICONTROL 디바이스 유형] 및 [!UICONTROL 제품]이 있습니다. 차원은 Adobe에서 제공하며 맞춤형 구현 (eVar, Props, 분류 등)을 통해 캡처됩니다.

각 차원에는 **차원 항목**&#x200B;도 포함됩니다. 차원 항목은 차원 이름 (항목은 노란색임) 옆에 있는 오른쪽 화살표를 클릭하여 왼쪽 구성 요소 레일에서 찾을 수 있습니다.

차원 항목의 예로는 [!UICONTROL 홈페이지] ([!UICONTROL 페이지] 차원 내), [!UICONTROL 유료 검색] ([!UICONTROL 마케팅 채널«] 차원 내), [!UICONTROL 태블릿] ([!UICONTROL 모바일 디바이스 유형] 차원 내) 등이 있습니다.

![](assets/dimensions.png)

## 지표 {#metrics}

[**지표**](https://experienceleague.adobe.com/docs/analytics/components/metrics/overview.html?lang=ko-KR)는 방문자 행동에 대한 정량적 측정입니다. 왼쪽 구성 요소 레일 (녹색 섹션)에서 찾을 수 있으며 일반적으로 테이블의 열로 적용됩니다.

지표의 예로는 [!UICONTROL 페이지 조회수], [!UICONTROL 방문 횟수], [!UICONTROL 주문 수], [!UICONTROL 평균 소요 시간] 및 [!UICONTROL 매출/테두리]이 있습니다. 지표는 Adobe에서 제공하거나 맞춤형 구현 ([!UICONTROL 성공 이벤트])을 통해 캡처하거나 [계산된 지표 빌더](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=ko-KR)를 사용하여 생성합니다.

![](assets/metrics.png)

## 세그먼트 {#segments}

[**세그먼트**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html?lang=ko-KR)는 분석에 적용되는 대상 필터입니다. 왼쪽 구성 요소 레일 (파란색 섹션)에서 찾을 수 있으며 일반적으로 패널 상단 또는 테이블의 지표 열 위에 적용됩니다.

세그먼트의 예로는 [!UICONTROL 모바일 디바이스 방문자], [!UICONTROL 이메일을 통한 방문 ] 및 [!UICONTROL 인증된 히트]가 있습니다. 세그먼트는 Adobe에서 제공하거나 [패널 드롭 영역](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko-KR)에서 생성하거나 [세그먼트 빌더](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=ko-KR)를 사용하여 생성합니다.

![](assets/segments.png)

## 데이터 범위 {#date-ranges}

[**날짜 범위**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html?lang=ko-KR)는 분석을 수행하는 기간입니다. 왼쪽 구성 요소 레일 (보라색 섹션)에서 찾을 수 있으며 일반적으로 각 패널의 달력에 적용됩니다.

패널 달력에 상대적인 날짜 범위 구성 요소를 만들 수 있습니다. 자세한 내용은 [상대 패널 날짜 범위 정보](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates).

날짜 범위의 예로는 2019년 7월, [!UICONTROL 지난 4주] 및 [!UICONTROL 이번 달]이 있습니다. 날짜 범위는 Adobe에서 제공하거나 [패널 달력](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko-KR)에 적용하거나 [날짜 범위 빌더](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=ko-KR)를 사용하여 생성합니다.

![](assets/date-ranges.png)


## 구성 요소 관리 {#actions}

왼쪽 레일에서 구성 요소를 직접 관리할 수 있습니다.

1. 구성 요소를 마우스 오른쪽 단추로 클릭합니다.

   또는

   구성 요소를 선택한 다음, **작업** (3-dot) 아이콘을 클릭합니다.

   >[!TIP]
   >
   >   Shift 키를 누르거나 Command 키(Mac에서) 또는 Ctrl 키(Windows)를 눌러 여러 구성 요소를 선택할 수 있습니다.


   ![](assets/component-actions.png)

   | 구성 요소 작업 | 설명 |
   |--- |--- |
   | [!UICONTROL **태그**] | 구성 요소에 태그를 적용하여 구성 요소를 구성하거나 관리합니다. 그런 다음 필터를 클릭하거나 #을 입력하여 왼쪽 레일에서 태그로 검색할 수 있습니다. 태그는 구성 요소 관리자에서 필터 역할도 합니다. |
   | [!UICONTROL **즐겨찾기**] | 구성 요소를 즐겨찾기 목록에 추가합니다. 태그와 마찬가지로 왼쪽 레일에서 즐겨찾기로 검색하고 구성 요소 관리자에서 즐겨찾기별로 필터링할 수 있습니다. |
   | [!UICONTROL **승인**] | 구성 요소를 승인됨으로 표시하여 해당 구성 요소가 조직에서 승인되었음을 사용자에게 알립니다. 태그와 마찬가지로 왼쪽 레일에서 승인됨으로 검색하고 구성 요소 관리자에서 승인됨별로 필터링할 수 있습니다. |
   | [!UICONTROL **공유**] | 조직의 사용자와 구성 요소를 공유합니다. 이 옵션은 세그먼트 또는 계산된 지표와 같은 사용자 정의 구성 요소에만 사용할 수 있습니다. |
   | [!UICONTROL **삭제**] | 더 이상 필요하지 않은 구성 요소를 삭제하십시오. 이 옵션은 세그먼트 또는 계산된 지표와 같은 사용자 정의 구성 요소에만 사용할 수 있습니다. |

사용자 정의 구성 요소는 해당 구성 요소 관리자를 통해 관리할 수도 있습니다. 예: [세그먼트 관리자](/help/components/segmentation/segmentation-workflow/seg-manage.md).

## 구성 요소 목록 검색, 필터링 및 정렬

Analysis Workspace의 왼쪽 레일에서 구성 요소 목록을 검색, 필터링 및 정렬하여 특정 구성 요소를 빠르게 찾을 수 있습니다.

### 구성 요소 목록 검색

1. 을(를) 선택합니다 **구성 요소** 아이콘 ![구성 요소 아이콘](assets/components-icon.png) 왼쪽 레일에 있습니다.

1. 검색 필드에서 프로젝트에 사용할 구성 요소의 이름을 입력합니다.

   구성 요소 유형은 색상과 아이콘을 모두 사용하여 식별할 수 있습니다. **Dimension** ![Dimension 아이콘](assets/dimension-icon.png) 주황색이고, **세그먼트** ![세그먼트 아이콘](assets/segment-icon.png) 파란색, **날짜 범위** ![날짜 범위 아이콘](assets/date-range-icon.png) 보라색이고 **지표** ![지표 아이콘](assets/default-metric-icon.png) 녹색입니다. Adobe 아이콘 ![Adobe 아이콘](assets/default-calc-metric-icon.png) 계산된 지표 템플릿 또는 세그먼트 템플릿과 계산기 아이콘을 나타냅니다 ![계산기 아이콘](assets/calculated-metric-icon-created.png) 조직의 Analytics 관리자가 만든 계산된 지표를 표시합니다.

1. 구성 요소가 드롭다운 목록에 나타나면 해당 구성 요소를 선택합니다.

### 구성 요소 목록 필터링

1. 을(를) 선택합니다 **구성 요소** 아이콘 ![구성 요소 아이콘](assets/components-icon.png) 왼쪽 레일에 있습니다.

1. 을(를) 선택합니다 **필터** 아이콘 ![데이터 사전 필터 아이콘](assets/components-filter-icon.png).

   또는

   검색 필드에 파운드 기호(#)를 입력합니다.

1. 다음 필터 옵션 중 하나를 선택하여 구성 요소 목록을 필터링합니다.

   | 옵션 | 함수 |
   |---------|----------|
   | [!UICONTROL **승인됨**] | 관리자가 승인함으로 표시된 구성 요소만 표시합니다. |
   | [!UICONTROL **즐겨찾기**] | 즐겨찾기 목록에 있는 구성 요소만 표시합니다. 즐겨찾기 목록에 구성 요소를 추가하는 방법에 대한 자세한 내용은 [구성 요소 개요](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)를 참조하십시오. |
   | [!UICONTROL **차원**] | 차원인 구성 요소만 표시합니다. |
   | [!UICONTROL **지표**] | 지표인 구성 요소만 표시합니다. |
   | [!UICONTROL **세그먼트**] | 세그먼트인 구성 요소만 표시합니다. <!--this is Filters in CJA--> |
   | [!UICONTROL **날짜 범위**] | 날짜 범위인 구성 요소만 표시합니다. |
   | [!UICONTROL **모두 표시**] | 모든 구성 요소를 표시합니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | [!UICONTROL **승인되지 않음**] | 관리자가 승인함으로 표시하지 않은 구성 요소만 표시합니다. 관리자가 검토 및 승인이 필요한 구성 요소를 식별할 때 유용합니다. 이 옵션은 관리자만 사용할 수 있습니다. |

1. (선택 사항) 목록을 추가로 정렬하려면 [구성 요소 목록 정렬](#sort-the-component-list).

### 구성 요소 목록 정렬

1. (선택 사항) [구성 요소 목록 필터링](#filter-the-component-list).

1. 을(를) 선택합니다 **구성 요소** 아이콘 ![구성 요소 아이콘](assets/components-icon.png) 왼쪽 레일에 있습니다.

1. 을(를) 선택합니다 **정렬** 아이콘 ![구성 요소 정렬 아이콘](assets/component-sort-icon.png)을 선택한 다음, 다음 필터 옵션 중 하나를 선택하여 구성 요소 목록을 정렬합니다.

   {{components-sort-options}}
