---
title: 자유 형식 테이블
description: 자유 형식 테이블 및 자유 형식 테이블 빌더에 대한 자세한 내용
translation-type: tm+mt
source-git-commit: ce06a5ca2caeb266c729947c76e93c611502e6d9

---


# 자유 형식 테이블

분석 작업 공간에서 자유 형식 테이블은 데이터 테이블일 뿐만 아니라 대화형 시각화이기도 합니다. 구성 요소 [](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) 조합을 행과 열로 드래그하여 놓아 분석에 사용할 사용자 정의 테이블을 만들 수 있습니다. 각 구성 요소가 삭제되면 테이블이 즉시 업데이트되므로 신속하게 분석할 수 있습니다.

다음과 같은 다양한 방법으로 표를 사용자 정의할 수 있습니다.

* **다른 결과를 표시했던**
   * 페이지 매김이 발생하기 전에 각 차원 행은 최대 400개의 행을 표시할 수 있습니다. 프로젝트의 [보기 밀도를](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html)조정하여 더 많은 행을 단일 화면에 맞출 수 있습니다.
   * 행은 추가 구성 요소로 분류할 수 있습니다. 한 번에 여러 행을 분류하려면 여러 행을 선택한 다음 선택한 행 위에 다음 구성 요소를 드래그하면 됩니다. 분류에 대한 자세한 내용을 [살펴보십시오](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.html).
   * 행을 [필터링하여](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/pagination-filtering-sorting.html) 축소된 항목 집합을 표시할 수 있습니다. 추가 설정은 행 설정에서 [사용할](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/table-settings.html)수 있습니다.

* **열**
   * 구성 요소를 열 내에 스택하여 세그먼트화된 지표, 탭 간 분석 등을 만들 수 있습니다.
   * 각 열의 보기는 [열 설정에서](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html)조정할 수 있습니다.
   * 몇 가지 작업은 [마우스 오른쪽 단추 클릭 메뉴를](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/using-the-right-click-menu.html)통해 사용할 수 있습니다. 이 메뉴는 표 머리글, 행 또는 열을 클릭하는지 여부에 따라 다른 작업을 제공합니다.

## 자유 형식 테이블 빌더

테이블에 여러 구성 요소를 추가하려면 먼저 데이터를 렌더링하면 자유 형식 테이블 빌더를 활성화할 수 있습니다. 빌더가 활성화되면 많은 차원, 분류, 지표 및 세그먼트를 드래그하여 놓는 방식으로 보다 복잡한 질문에 대한 해답을 만들 수 있습니다. 데이터는 즉시 업데이트되지 않고 빌드를 클릭하면 업데이트됩니다 ****.

테이블 빌더는 데이터에 대한 복잡한 질문이 있을 때 시간을 절약할 수 있는 옵션이며 질문에 응답하기 위해 구성할 표에 대한 아이디어가 있습니다. 테이블 빌더의 다른 이점은 다음과 같습니다.

* 각 작업이 렌더링될 때까지 기다리지 않고 필요한 정확한 형식으로 표를 배열합니다.
* 최대 4가지 수준의 분류를 신속하게 수행할 수 있습니다.
* 모든 테이블 행 및 차원 열에 대한 행 및 분류 설정을 정의합니다.
* **[!UICONTROL 기본적으로 테이블의]**모든 레벨에 대한 위치별 분류(기존의 자유 형식 테이블에서 기본값은 품목별**[!UICONTROL &#x200B;분류입니다]**.)
* 테이블에서 정적 행의 순서를 수동으로 지정합니다. 예를 들어 지표 행을 특정 순서로 표시하려면
* 실제 데이터를 렌더링하기 전에 표 형식을 미리 볼 수 있습니다.

자유 형식 테이블 빌더 기능을 [살펴보십시오](https://youtu.be/GUMWiJAmMGI).

## 자유 형식 테이블 데이터 내보내기

자유 형식 테이블의 데이터는 다음과 같은 몇 가지 방법으로 분석 작업 공간에서 복사할 수 있습니다.

* 테이블 헤더를 마우스 오른쪽 단추로 클릭하고 클립보드에 **[!UICONTROL 복사를 선택합니다]**. 전체(보이는) 테이블을 내보냅니다.
* 표에서 특정 셀을 강조 표시하거나, 마우스 오른쪽 단추를 클릭하고 클립보드에 **[!UICONTROL 복사를 선택하거나]**, Ctrl + C 핫키를 사용합니다.
* **[!UICONTROL 프로젝트 > CSV 다운로드를]**참조하십시오. 이렇게 하면 프로젝트의 보이는 모든 테이블이 CSV로 내보내집니다.
