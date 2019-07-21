---
title: Adobe Analytics의 보고서 사용자 정의
description: Adobe Analytics에서 보고서를 사용자 지정하는 방법 알아보기
translation-type: tm+mt
source-git-commit: a5f612ba5e8446a56bc2bd252a8781e8ab1de403

---


# 보고서 사용자 지정

Google Analytics와 같은 타사 플랫폼에서 여러 사용자 정의 옵션을 사용할 수 있습니다. 이러한 사용자 정의 기능을 통해 사용자는 대시보드, 사용자 정의 보고서, 저장된 보고서 및 사용자 정의 경고를 만들 수 있습니다. 분석 작업 공간에서는 사용자가 빈 캔버스에서 보고서를 작성할 수 있으므로 대부분의 사용자 정의는 도구에 직접 빌드됩니다.

이 페이지에서는 사용자가 분석 작업 공간 사용에 대한 기본적인 지식을 가지고 있다고 가정합니다. See [Create a basic report in Analysis Workspace for Google Analytics users](reports/create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## 대시보드

Analysis Workspace의 아키텍처는 대시보드 위젯의 개념과 유사하게 구축되었습니다. 분석 작업 공간의 프로젝트는 Google Analytics의 대시보드와 거의 비슷한 수준입니다. 분석 작업 공간의 시각화는 Google Analytics의 위젯과 거의 비슷한 수준입니다.

### 프로젝트에 컨텐츠 추가

1. 왼쪽에 있는 시각화 아이콘을 클릭하고 원하는 시각화 기능을 작업 영역으로 드래그합니다.
2. 왼쪽에 있는 구성 요소 아이콘을 클릭하고 원하는 차원과 지표를 시각화로 드래그하여 데이터로 채웁니다.
3. 시각화의 가장자리를 드래그하여 크기를 조정하고 시각화의 제목을 드래그하여 이동할 수 있습니다.

모든 Google Analytics 위젯은 분석 작업 공간에서 사용할 수 있습니다.

* **지표 위젯은** 요약 번호 시각화와 거의 동일합니다.
* **타임라인 위젯은** 라인 시각화와 거의 동일합니다.
* **Geomap 위젯은** 맵 시각화와 거의 동일합니다.
* **테이블 위젯은** 자유 형식 테이블 시각화와 거의 동일합니다.
* **파이 위젯은** 도넛 시각화와 거의 동일합니다.
* **막대 위젯은** 막대 시각화와 거의 동일합니다.

Analysis Workspace 에는 보고 요구 사항에 가장 적합한 방식으로 데이터를 제공하기 위한 더 많은 시각화 옵션이 포함되어 있습니다. See [Visualizations in Analysis Workspace](../../analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) in the Analyze User Guide for more information.

### 프로젝트 공유

프로젝트에 컨텐츠 추가가 완료되면 공유할 수 있습니다.

* 동료와 프로젝트를 공유하려면 공유 &gt; 프로젝트 공유를 선택합니다. 수신자는 조직의 Adobe Analytics 계정이 있는 다른 사용자입니다.
* 링크를 통해 프로젝트를 공유하려면 [공유] &gt; [프로젝트 가져오기] 링크로 이동합니다. 이 경우 조직 내에서 Adobe Analytics에 로그인해야 합니다.

### 프로젝트 내보내기

분석 작업 공간은 PDF 이외에도 CSV 내보내기를 제공합니다.

1. *[!UICONTROL [공유]* ] &gt; *[!UICONTROL []*&#x200B;지금 파일 보내기] 를 클릭하면 모달 창이 열립니다.
2. 파일 유형 및 수신자를 지정합니다.
3. Click [!UICONTROL Send Now].

## 사용자 지정 보고서

Google Analytics에서 사용자 지정 보고서를 만들 때 필요한 필드는 작업 공간에서 시각화 작성에 있는 워크플로우와 비슷합니다. 차원, 지표 및 필터 정의는 플랫폼 간에 유사합니다. 분석 작업 공간에서 목록에서 차원 및 지표를 선택하는 대신 차원 및 지표를 자유 형식 테이블로 드래그합니다.

### 사용자 지정 보고서의 계산된 지표

사용자 지정 보고서는 계산된 지표를 사용할 수 있는 Google Analytics의 몇 가지 영역 중 하나입니다. 분석 작업 공간은 캔버스와 같이 작동하므로 계산된 지표는 모든 컨텍스트에서 소급하여 작동합니다.

계산된 지표를 만들려면:

1. Click the **+** icon near the metric list to open the Calculated Metric Builder.
2. 계산된 지표에 이름을 지정하고 형식을 지정합니다.
3. 지표 구성 요소를 정의 영역으로 드래그하고 각 구성 요소 간에 드롭다운을 사용하여 연산자를 지정합니다.
4. 계산된 지표에 원하는 공식이 포함되면 저장을 클릭하여 작업 영역으로 돌아갑니다.
5. 새로 정의된 계산된 지표를 작업 공간으로 드래그합니다.

   Learn more about [Calculated Metrics](../../components/c-variables/c-metrics/calculated-metric.md) in the Components user guide.

## 사용자 정의 경고

두 플랫폼에서 경고를 사용할 수 있습니다. In Adobe Analytics, use the header navigation menu and go to *[!UICONTROL Components]* &gt; *[!UICONTROL Alerts]*. See [Intelligent Alerts](../../components/c-alerts/intellligent-alerts.md) in the Components User Guide for more information.
