---
description: 계산된 지표 빌더는 차원, 지표, 세그먼트 및 함수를 드래그하여 놓음으로써 컨테이너 계층 논리, 규칙 및 연산자를 기준으로 사용자 정의 지표를 만들 수 있는 캔버스를 제공합니다. 이러한 통합 개발 도구를 사용하여 간단한 계산된 지표나 복잡한 고급 계산된 지표를 빌드하고 저장할 수 있습니다.
title: 지표 작성
feature: Calculated Metrics
exl-id: 12bb3734-e25d-4c67-8c62-e1226d9aef94
source-git-commit: d9f95b12a43305cecff1190e6544334f3b48835d
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 100%

---

# 지표 작성 {#build-metrics}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_externalid"
>title="외부 ID"
>abstract="외부 ID를 변경하면 비즈니스 인텔리전스 도구와 같은 외부 소스에 계산된 지표가 표시되는 방식에 영향을 미칠 수 있습니다."


Adobe Analytics는 차원, 지표, 세그먼트 및 함수를 끌어다 놓음으로써 컨테이너 계층 논리, 규칙 및 연산자를 기준으로 사용자 정의 지표를 만들 수 있는 캔버스를 제공합니다. 이러한 통합 개발 도구를 사용하여 간단하거나 복잡한 계산된 지표를 빌드하고 저장할 수 있습니다.

## 계산된 지표 빌드 시작

계산된 지표 빌더를 사용하여 계산된 지표를 만들거나 편집할 수 있습니다. 이렇게 생성되면 계산된 지표가 구성 요소 목록에서 사용 가능하며, 조직 전체의 프로젝트에서 사용할 수 있습니다. 또는 [지표](/help/analyze/analysis-workspace/components/apply-create-metrics.md)에서 [단일 프로젝트에 대한 계산된 지표 만들기](/help/analyze/analysis-workspace/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project)에 설명된 대로 계산된 지표가 생성된 프로젝트에 대해서만 사용할 수 있는 계산된 지표를 빠르게 만들 수 있습니다.

계산된 지표 빌더에 액세스하여 구성 요소 목록에서 사용할 수 있는 계산된 지표를 만들기 시작합니다.

1. 다음 중 어떤 방법으로든 계산된 지표 빌더에 액세스합니다.

   * Analysis Workspace에서 프로젝트를 연 다음 **[!UICONTROL 구성 요소]** > **[!UICONTROL 지표 만들기]**&#x200B;를 선택합니다.
   * Analysis Workspace에서 프로젝트를 열고 왼쪽 레일의 [!UICONTROL **지표**] 섹션 옆에 있는 **플러스** 아이콘을 선택합니다.
   * [!DNL Adobe Analytics]에서 **[!UICONTROL 구성 요소]** > **[!UICONTROL 계산된 지표]**&#x200B;로 이동한 다음 계산된 지표 페이지 상단에서 **[!UICONTROL + 추가]**&#x200B;를 선택합니다.

1. [계산된 지표 빌더의 영역](#areas-of-the-calculated-metrics-builder)으로 계속합니다.

## 계산된 지표 빌더의 영역

다음 이미지와 첨부된 테이블에서는 계산된 지표 빌더의 주요 영역과 기능을 설명합니다.

![](assets/cm_builder_ui.png)

| 이미지의 위치 | 이름 및 기능 |
|---|---|
| 1 | **제목:** 지표에 이름을 지정하는 것은 필수입니다. 이름을 지정하지 않으면 지표를 저장할 수 없습니다. |
| 2 | **설명:** 사용자에게 친근한 설명을 지정하여 용도를 알고 유사한 지표들과 구별할 수 있도록 하십시오. <p>이 설명은 보고서 내에도 나타납니다. 설명에 공식을 넣지 않는 것이 좋습니다. 대신 이 지표를 어디에 사용하고 어디에 사용하지 말아야 하는지 설명하십시오. (공식은 지표를 만들면 요약 머리글 아래에 생성됩니다. 따라서 공식을 설명에 추가할 필요가 없습니다.) </p> |
| 3 | **형식:** 선택 사항에는 소수, 시간, 비율 및 통화가 포함됩니다. |
| 4 | **소수점 이하 자리 수:** 보고서에 소수점 이하 몇 자리가 표시될 것인지 보여 줍니다. 지정할 수 있는 소수점 이하 최대 자릿수는 10자리입니다. |
| 5 | **증가 트렌드를 다음으로 표시:** 이 지표 극성 설정은 Analytics가 지표에서 증가 트렌드를 양호(녹색)으로 간주할지 또는 불량(빨간색)으로 간주할지를 보여 줍니다. 그 결과, 보고서의 그래프는 증가할 때 녹색 또는 빨간색으로 표시됩니다. |
| 6 | **태그:** 태깅은 지표를 구성하는 좋은 방법입니다. 모든 사용자는 태그를 만든 후 지표에 하나 이상의 태그를 적용할 수 있습니다. 그렇지만 본인이 소유하거나 본인과 공유된 세그먼트에 대한 태그만 볼 수 있습니다. 어떤 종류의 태그를 만들어야 합니까? 다음은 제안되는 유용한 태그입니다.<ul><li>**팀 이름**(예: 소셜 마케팅, 모바일 마케팅)</li><li>**프로젝트**(분석 태그) (예: 시작 페이지 분석)</li><li>**카테고리**(예: 여성, 지리).</li><li>**워크플로**(예: 승인용, 처리됨(특정 비즈니스 단위))</li></ul> |
| 7 | **요약:** <p>요약 공식은 지표 정의를 변경할 때마다 업데이트됩니다. 이 공식은 마우스로 지표를 가리키고 <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> 아이콘을 클릭하면 왼쪽의 지표 레일에 표시됩니다. </p> |
| 8 | **정의:** 이곳은 계산된 지표를 빌드하기 위해 지표/계산된 지표, 세그먼트 및/또는 함수를 드래그하여 놓는 곳입니다. <ul><li>계산된 지표에서 드래그하면 그 지표 정의를 자동으로 확장합니다. </li> <li>정의를 컨테이너와 중첩시킬 수 있습니다. 단, 세그먼트 컨테이너와 달리, 컨테이너는 수학 표현식처럼 작동하고 작업 순서를 결정합니다. </li> </ul> |
| 9 | **연산자:** 나누기( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" />)가 기본 연산자이며 이외에도 +, -, x 연산자가 있습니다. |
| 10 | **미리보기:** 모든 가능한 오류 시 빨리 읽을 수 있도록 해 줍니다. 이 미리보기는 마지막 90일에 적용됩니다. 해당 지표에 대해 올바른 구성 요소를 선택했는지를 초기에 판단하는 방법입니다. 예상치 않은 결과는 지표 정의 시 두 번 확인해야 함을 의미합니다. |
| 11 | **제품 호환성:** 제품 호환성은 지표가 <a href="https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html"  > 현재 데이터 </a>와 호환되는지, 완전히 처리된 데이터와 호환되는지 또는 마케팅 채널 보고서와 호환되는지를 보여 줍니다(첫 번째 터치 할당). <p>참고: 현재 데이터는 일부 데이터를 지원하지 않습니다. 세그먼트나 함수가 들어 있는 지표는 현재 데이터와 호환하지 않습니다. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > 자세히... </a> </p> </p> |
| 12 | **추가:** 모든 유형의 계산된 지표의 경우, 컨테이너 및 정적 수를 정의에 추가할 수 있습니다. 고급 계산된 지표의 경우 세그먼트 및 함수를 추가할 수도 있습니다. <ul><li>컨테이너는 수학 표현식처럼 작동하고 작업 순서를 결정합니다. 그러므로 컨테이너에 있는 모든 것은 다음 작업 전에 처리됩니다.</li><li>세그먼트를 컨테이너에 드래그하면 해당 컨테이너에 있는 모든 내용이 세그먼트화됩니다. (고급 계산된 지표만)</li><li>한 컨테이너에서 여러 세그먼트를 스택할 수 있습니다.</li></ul> |
| 13 | **톱니바퀴 아이콘(지표 유형, 기여도 분석):** 지표 옆에 있는 톱니바퀴 아이콘을 선택하여 <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  > 지표 유형 및 기여도 분석 모델 </a>을 지정할 수 있습니다. |
| 14 | **신규:** 새로운 세그먼트(<a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  > 세그먼트 빌더 </a>로 이동)와 같은 새 구성 요소를 만듭니다. |
| 15 | **검색 구성 요소:** 이 검색 창을 사용하여 차원, 지표, 세그먼트(고급 계산된 지표만) 및 함수(고급 계산된 지표만)를 검색할 수 있습니다. |
| 16 | **차원 목록:** 세그먼트 빌더에서 “Page = Homepage”와 같은 간단한 세그먼트를 작성하기 위해 계산된 지표 빌더를 종료하지 않고, 페이지에서 끌어서 홈 페이지를 계산된 지표 빌더에서 직접 선택할 수 있습니다.<p>그 결과 세그먼트화된 계산된 지표를 생성할 훨씬 능률적인 워크플로가 만들어집니다.</p> |
| 17 | **지표 목록:** 지표는 3가지 카테고리로 나뉩니다. <ul> <li>표준 지표(<img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li><li>계산된 지표( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li><li id="li_8735E76637ED4C3F983731A66E04C93E">지표 템플릿( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg" id="image_D236601511CC4DD3828F223431E27E88" />) - 목록의 맨 아래. </li> </ul> <p>마우스로 지표를 가져다 대면 그 오른쪽에 정보 아이콘이 표시됩니다. <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" width="15px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. 이 아이콘을 클릭하면 다음 정보가 표시됩니다. </p><ul> <li>계산되는 방식에 대한 공식. </li><li>지표의 미리보기 트렌드. </li><li>이 계산된 지표를 <img placement="break" align="center"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg" width="15px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> 편집할 수 있는 계산된 지표 빌더를 표시하는 오른쪽 상단의 편집(연필) 아이콘. </li></ul> |
| 18 | **세그먼트 목록:** (고급 계산된 지표만 해당) 관리자로서, 이 목록은 로그인 회사에서 만든 모든 세그먼트를 보여 줍니다. 사용자가 관리 사용자가 아닐 경우, 이 목록에는 사용자가 소유한 세그먼트와 사용자와 공유된 세그먼트가 표시됩니다. <a href="https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-rights.html"  > 자세히... </a> |
| 19 | **함수 목록:** (고급 계산된 지표만) 함수는 <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  > 기본 </a>(가장 자주 사용됨) 및 <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  > 고급 </a>, 이렇게 두 개의 목록으로 나뉩니다. |
| 20 | **보고서 세트 선택기:** 다른 보고서 세트로 전환할 수 있습니다. |

{style="table-layout:auto"}
