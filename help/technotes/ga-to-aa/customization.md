---
title: Adobe Analytics의 보고서 사용자 지정
description: Adobe Analytics에서 보고서를 사용자 지정하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 6fc8145d9a94427ec942d55776b6029f7dd6f79c
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 78%

---


# 보고서 사용자 지정

Google Analytics와 같은 타사 플랫폼에서 여러 가지 사용자 지정 옵션을 사용할 수 있습니다. 이러한 사용자 지정을 사용하여 사용자가 대시보드, 사용자 지정 보고서, 저장된 보고서 및 사용자 지정 경고를 만들 수 있습니다. Analysis Workspace를 사용하면 사용자가 빈 캔버스에서 보고서를 작성할 수 있으므로 대부분의 사용자 지정 항목이 도구에 직접 빌드되어 있습니다.

This page assumes the user has a basic knowledge of using [!UICONTROL Analysis Workspace]. Adobe Analytics의 도구에 아직 익숙하지 않은 경우 [Google Analytics 사용자를 위한 Analysis Workspace에서 기본 보고서 만들기](reports/create-report.md)를 참조하십시오.

## 대시보드

The [!UICONTROL Analysis Workspace] architecture is built similar to the concept of dashboard widgets. Projects in [!UICONTROL Analysis Workspace] are the approximate equivalent to dashboards in Google Analytics. Visualizations in [!UICONTROL Analysis Workspace] are the approximate equivalent of widgets in Google Analytics.

### 프로젝트에 컨텐츠 추가

1. Click the [!UICONTROL Visualizations] icon on the left and drag the desired visualization onto the workspace.
2. Click the [!UICONTROL Components] icon on the left and drag the desired dimensions and metrics onto the visualization to populate it with data.
3. 시각화의 가장자리를 끌어서 크기를 조정하고 시각화의 제목을 끌어서 이동합니다.

All Google Analytics widgets are available in [!UICONTROL Analysis Workspace]:

* **지표 위젯**&#x200B;은 요약 번호 시각화와 거의 같습니다.
* **타임라인 위젯**&#x200B;은 선 시각화와 거의 같습니다.
* **Geomap 위젯**&#x200B;은 맵 시각화와 거의 같습니다.
* **테이블 위젯**&#x200B;은 자유 형식 테이블 시각화와 거의 같습니다.
* **파이 위젯**&#x200B;은 도넛 시각화와 거의 같습니다.
* **막대 위젯**&#x200B;은 막대 시각화와 거의 같습니다.

[!UICONTROL Analysis Workspace에는 보고 요구 사항에 가장 적합한 방식으로 데이터를 제공하기 위한 다양한 시각화 옵션이 포함되어 있습니다. ] 자세한 내용은 분석 사용 안내서의 [Analysis Workspace에서 시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)를 참조하십시오.

### 프로젝트 공유

컨텐츠를 프로젝트에 추가하고 나면 프로젝트를 공유할 수 있습니다.

* To share the project with your colleagues, go to **[!UICONTROL Share > Share Project]**. 수신자는 Adobe Analytics 계정이 있는 조직의 다른 사용자입니다.
* To share your project via a link, go to **[!UICONTROL Share > Get Project Link]**. 이렇게 하려면 조직 내에서 Adobe Analytics에 로그인해야 합니다.

### 프로젝트 내보내기

In addition to PDF, [!UICONTROL Analysis Workspace] offers a CSV export.

1. *[!UICONTROL 공유]* > *[!UICONTROL 지금 파일 보내기]*&#x200B;를 클릭하여 모달 창을 엽니다.
2. 파일 유형 및 수신자를 지정합니다.
3. [!UICONTROL 지금 보내기]를 클릭합니다.

## 사용자 지정 보고서

Google Analytics에서 사용자 지정 보고서를 만들 때 필수 필드는 작업 공간에서 시각화를 작성하는 워크플로우와 유사합니다. 차원, 지표 및 필터 정의는 플랫폼 간에 유사합니다. Analysis Workspace에서는 목록에서 차원 및 지표를 선택하는 대신 차원 및 지표를 자유 형식 테이블로 끌어서 놓습니다.

### 사용자 지정 보고서에 계산된 지표

사용자 지정 보고서는 Google Analytics에서 계산된 지표를 사용할 수 있는 몇 가지 영역 중 하나입니다. Analysis Workspace가 캔버스처럼 작동하므로 계산된 지표는 소급해서 모든 컨텍스트에서 작동합니다.

계산된 지표를 만들려면:

1. 지표 목록 근처에 있는 **+**[!UICONTROL  아이콘을 클릭하여 계산된 지표 빌더를 엽니다].
2. 계산된 지표에 이름을 지정하고 형식을 지정합니다.
3. 지표 구성 요소를 정의 영역으로 끌어서 놓고 각 구성 요소 사이의 드롭다운을 사용하여 연산자를 지정합니다.
4. 계산된 지표에 원하는 공식이 포함되면 저장을 클릭하여 작업 공간으로 다시 돌아갑니다.
5. 새로 정의된 계산된 지표를 작업 공간으로 끌어서 놓습니다.

   구성 요소 사용 안내서에서 [계산된 지표](/help/components/c-calcmetrics/cm-overview.md)에 대해 자세히 알아보십시오.

## 사용자 지정 경고

경고는 두 플랫폼 모두에서 사용할 수 있습니다. Adobe Analytics에서 헤더 탐색 메뉴를 사용하여 *[!UICONTROL 구성 요소]* > *[!UICONTROL 경고]*&#x200B;로 이동합니다. 자세한 내용은 구성 요소 사용 안내서의 [지능적인 경고](/help/components/c-alerts/intellligent-alerts.md)를 참조하십시오.
