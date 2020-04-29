---
description: 빠른 통찰력 빌더는 새로운 작업 영역 사용자가 데이터 테이블 및 시각화 작성을 안내하는 도구입니다
title: 빠른 인사이트 빌더
translation-type: tm+mt
source-git-commit: 0bf00f990a34768b93cef5d57a126ebe93087e91

---


# 빠른 인사이트 빌더

>[!IMPORTANT]
>
>**[!UICONTROL Quick Insights]** 는 현재 제한된 테스트 중이며 아직 모든 Adobe Analytics 고객에게 일반적으로 제공되지 않습니다.

[!UICONTROL Quick Insights] 비분석가 및 새로운 사용자에게 비즈니스 질문에 빠르고 손쉽게 대답하는 방법을 [!UICONTROL Analysis Workspace] 소개하는 지침을 제공합니다. 또한 표를 직접 만들지 않고도 간단한 질문에 신속하게 답변하고자 하는 고급 사용자에게는 탁월한 툴입니다.

이 기능을 처음 사용할 [!UICONTROL Analysis Workspace]때 가장 유용한 시각화, 통찰력을 용이하게 하는 차원 및 지표, 항목을 드래그 앤 드롭할 위치, 세그먼트를 만들 위치 등이 궁금해질 수 있습니다.

이를 돕기 위해, 그리고 회사의 데이터 구성 요소 사용을 기반으로, 회사에서 사용하는 가장 인기 있는 차원, 지표, 세그먼트 및 날짜 범위를 제공하는 알고리즘을 [!UICONTROL Analysis Workspace][!UICONTROL Quick Insights] 활용합니다.

[!UICONTROL Quick Insights] 도움

* 에서 데이터 테이블 및 관련 시각화를 올바르게 작성합니다 [!UICONTROL Analysis Workspace].
* 기본 구성 요소 및 부분에 대한 용어 및 어휘를 [!UICONTROL Analysis Workspace]살펴보십시오.
* 차원을 간단하게 분류하거나, 여러 지표를 추가하거나, 한 [!UICONTROL Freeform table]번에 세그먼트를 쉽게 비교할 수 있습니다.
* 다양한 시각화 유형을 변경하거나 테스트하여 분석에 필요한 찾기 툴을 신속하고 직관적으로 찾을 수 있습니다.

## 기본 키 용어

다음은 익숙해져야 하는 몇 가지 기본 용어입니다. 각 데이터 테이블은 데이터 스토리를 전달하는 데 사용하는 2개 이상의 구성 요소(구성 요소)로 구성됩니다.

| 빌딩 블록(구성 요소) | 정의 |
|---|---|
| [!UICONTROL Dimension] | 차원은 프로젝트에서 보고, 분류하고 비교할 수 있는 지표 데이터의 설명 또는 특성입니다. 숫자가 아닌 값 및 차원 항목으로 분류되는 날짜입니다. 예를 들어 &quot;browser&quot; 또는 &quot;page&quot;는 차원입니다. |
| [!UICONTROL Dimension item] | 차원 항목은 차원에 대한 개별 값입니다. 예를 들어 브라우저 차원의 차원 항목은 &quot;Chrome&quot;, &quot;Firefox&quot;, &quot;Edge&quot; 등이 됩니다. |
| [!UICONTROL Metric] | 지표는 보기 수, 클릭스루 횟수, 다시 로드 횟수, 평균 체류 시간, 판매량, 주문 수, 매출액 등과 같은 방문자 활동에 대한 수량 정보입니다. |
| [!UICONTROL Visualization] | Workspace [는 막대 차트, 도넛 차트, 히스토그램, 라인 차트, 지도, 스캐터플로 등과 같이 데이터를 시각적으로 표시하는](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md) 많은 시각화를 제공합니다. |
| [!UICONTROL Breakdown] | 분류는 차원을 다른 차원으로 실제로 분류하는 방법입니다. 이 예에서는 미국 주를 모바일 장치별로 분류하여 주별 모바일 장치 방문을 받거나 모바일 장치 유형별로, 지역별, 내부 캠페인 등으로 모바일 장치를 분류할 수 있습니다. |
| [!UICONTROL Segment] | 세그먼트를 사용하면 특성 또는 웹 사이트 상호 작용을 기반으로 방문자의 하위 집합을 식별할 수 있습니다. 예를 들어 속성을 기반으로 [!UICONTROL Visitor] 세그먼트를 만들 수 있습니다.브라우저 유형, 장치, 방문 횟수, 국가, 성별 또는 상호 작용에 따른 상호 작용캠페인, 키워드 검색, 검색 엔진 또는 종료 및 항목 기반:Facebook의 방문자, 정의된 랜딩 페이지, 참조 도메인 또는 사용자 지정 변수 기반양식 필드, 정의된 카테고리, 고객 ID. |

## 빠른 인사이트 시작하기

1. 제공된 자격 증명을 사용하여 Adobe Analytics에 로그인합니다.
1. 이동 [!UICONTROL Workspace] 후 **[!UICONTROL Create New Project]** 클릭한 다음 을 클릭합니다 **[!UICONTROL Quick Insights]**.

   ![](assets/qibuilder.png)

1. 처음 시작할 때 몇 가지 [!UICONTROL Quick Insights panel] 기본 사항을 설명하는 간단한 튜토리얼을 살펴봅니다. 또는 을 클릭하여 **[!UICONTROL Skip Tutorial]**&#x200B;선택합니다.
1. 구성 요소라고도 하는 구성 요소를 선택합니다.차원(주황색), 지표(녹색), 세그먼트(파란색) 또는 날짜 범위(자주색) 자동으로 만들 표에 대해 하나 이상의 차원과 하나의 지표를 선택해야 합니다.

   ![](assets/qibuilder2.png)

   다음 세 가지 방법으로 구성 요소를 선택할 수 있습니다.
   * 왼쪽 레일에서 드래그하여 놓습니다.
   * 원하는 내용을 알고 있는 경우:입력을 시작하면 빈 칸을 채울 [!UICONTROL Quick Insights] 수 있습니다.
   * 드롭다운을 클릭하고 목록을 검색합니다.

1. 하나 이상의 차원과 하나의 지표를 추가하면 다음과 같은 항목이 생성됩니다.

   * 차원(여기, 미국 주)이 수직으로 있고 지표(여기, 방문 횟수)가 맨 위에 가로로 있는 자유 형식 테이블. 다음 표를 확인하십시오.
   ![](assets/qibuilder3.png)

   * 함께 제공되는 시각화, 이 경우 [막대 차트입니다](/help/analyze/analysis-workspace/visualizations/bar.md). 생성된 시각화는 표에 추가한 데이터 유형을 기반으로 합니다. 옆에 있는 드롭다운 화살표를 클릭하여 시각화 유형을 변경할 수 **[!UICONTROL Bar]**&#x200B;있습니다.


1. (선택 사항) 차원 옆의 > 오른쪽 화살표를 클릭하여 차원을 드릴다운하고 차원 항목을 봅니다.

1. 아래의 &quot;기타 유용한 옵션&quot;에 설명된 대로 세부 사항을 추가해 보십시오.

## 기타 유용한 옵션

다른 유용한 힌트가 [!UICONTROL Quick Insights Builder]표시됩니다. 일부 힌트는 마지막 동작에 따라 달라집니다.

* 먼저 **[!UICONTROL More tips]** 튜토리얼을 완료하십시오.도움말(?)을 통해 액세스합니다. 아이콘 옆에 [!UICONTROL Quick Insights Panel] 있는 아이콘을 클릭합니다.

   ![](assets/qibuilder4.png)

* **분류 기준**:차원에서 최대 3개의 분류 수준을 사용하여 필요한 데이터로 드릴다운할 수 있습니다.

   ![](assets/qibuilder5.png)

* **지표**&#x200B;추가:AND 연산자를 사용하여 표에 지표를 추가하여 최대 2개의 지표를 추가할 수 있습니다.

   ![](assets/qibuilder6.png)

* **세그먼트**&#x200B;추가:AND 또는 OR 연산자를 사용하여 테이블을 추가하여 최대 2개의 세그먼트를 추가할 수 있습니다. 모바일 사용자 또는 단골 방문자를 추가할 때 표에 나타나는 상황을 살펴봅니다. 지표 위에 서로 나란히 있습니다. 모바일 사용자 및 단골 방문자를 추가한 경우 두 세그먼트의 결과가 함께 표시되고, 이 두 세그먼트는 표의 서로 겹치게 됩니다.

   ![](assets/qibuilder7.png)

## 알려진 제한 사항

표 내에서 직접 편집하려고 하면 [!UICONTROL Quick Insights] 패널(빈 칸 채우기 도구)이 동기화되지 않습니다. 패널 오른쪽 상단에서 을 클릭하여 이전 [!UICONTROL Quick Insights] 설정으로 복원할 **[!UICONTROL Resync Builder]** 수 있습니다.

![](assets/qibuilder9.png)

테이블에 직접 추가하기 전에 경고가 표시됩니다.

![](assets/qibuilder8.png)

그렇지 않은 경우 직접 작성하면 새 사용자에게 유용한 기능을 제공하지 않고 테이블이 기존의 자유 형식 테이블로 동작합니다.

