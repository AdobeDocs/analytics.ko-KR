---
description: 세그먼트 빌더는 컨테이너 계층 논리, 규칙 및 연산자를 기반으로 지표 차원, 세그먼트 및 이벤트를 세그먼트 방문자로 드래그하여 놓을 수 있는 캔버스를 제공합니다. 이러한 통합 개발 도구를 사용하여 방문과 페이지 히트에 걸쳐 방문자 특성 및 작업을 식별하는 간단하거나 복잡한 세그먼트를 작성하고 저장할 수 있습니다.
title: 세그먼트 작성
topic: Segments
uuid: c01393df-ccdd-431c-83a6-3c2700bd4999
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 세그먼트 빌더

The [!UICONTROL Segment Builder] provides a canvas to drag and drop Metrics, Dimensions, Segments, and Events to segment visitors based on container hierarchy logic, rules, and operators. 이러한 통합 개발 도구를 사용하여 방문과 페이지 히트에 걸쳐 방문자 특성 및 작업을 식별하는 간단하거나 복잡한 세그먼트를 작성하고 저장할 수 있습니다.

>[!IMPORTANT]
>
>2019년 6월 릴리스에서는 차원 기여도 분석 모델이 도입되었습니다. 아래의 웹 UI 기능에 있는 6번을 참조하십시오.

세그먼트 빌더에 액세스하는 방법에는 여러 가지가 있습니다.

* **Analytics 상단 탐색**:> **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Segments]**&#x200B;을 클릭합니다.
* **[!UICONTROL Analysis Workspace]**:> **[!UICONTROL Analytics]** 를 **[!UICONTROL Workspace]**&#x200B;클릭하고 프로젝트를 연 다음 **[!UICONTROL + New]** > 를 **[!UICONTROL Create Segment]**&#x200B;클릭합니다.
* **[!UICONTROL Reports & Analytics]**:> **[!UICONTROL Analytics]** 를 **[!UICONTROL Reports]**&#x200B;클릭하고 기존 보고서를 열고 왼쪽 탐색 영역에서 세그먼트 아이콘을 클릭한 다음 ![](assets/segment_icon.png) **[!UICONTROL Add]**&#x200B;을 클릭합니다.
* **[!UICONTROL Ad Hoc Analysis]**:애드혹 [분석에서 세그먼트를 만듭니다](/help/components/c-segmentation/c-segmentation-workflow/seg-build.md#build-segments).
* **[!UICONTROL Report Builder]**:리포트 [빌더에서 세그먼트를 추가하거나 편집합니다](https://marketing.adobe.com/resources/help/ko_KR/arb/segmentation.html).

## 세그먼트 빌더 사용자 인터페이스 {#concept_643F2DF74C544796B58F4656ABC5F726}

이 [!UICONTROL Segment Builder] 기능을 사용하면 방문 및 페이지 히트 전체에서 방문자 특성 및 작업을 식별하는 간단하거나 복잡한 세그먼트를 만들 수 있습니다. 계층 논리, 규칙 및 연산자를 기반으로 방문자를 세그먼트화하기 위해 지표 차원, 이벤트 또는 기타 세그먼트를 드래그하여 놓을 수 있는 캔버스를 제공합니다.

## 웹 UI 기능 {#section_F61C4268A5974C788629399ADE1E6E7C}

이 [!UICONTROL Segment Builder] 도구를 사용하여 웹 UI(또는 애드혹 분석의 Java [UI)에서 세그먼트를 만들고 편집할 수 있습니다](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md). 규칙 정의 및 컨테이너를 추가하여 세그먼트를 세분화하고 스택하고 중첩하여 세분화할 수 있습니다. 또한 현재 세그먼트 정의에서 발생한 페이지 보기 횟수, 방문 횟수 및 고유 방문자 수를 확인할 수 있습니다. 그런 다음 향후 요구 사항에 맞게 세그먼트를 저장합니다.

다음 방법을 통해 세그먼트 빌더에 액세스합니다.

* 기존 보고서를 표시하고 왼쪽 탐색에서 세그먼트 아이콘 ![](assets/segment_icon.png)을 클릭합니다. In the segment rail that displays, click **[!UICONTROL Add]**.

* From within the Segment Manager, clicking **[!UICONTROL + Add]**.
* 세그먼트 관리자에서 기존 세그먼트 제목을 클릭하여 세그먼트 빌더에서 세그먼트 편집

![](assets/segment_builder_ui.png)

1. **[!UICONTROL Title]**:세그먼트의 이름을 지정하거나 이름을 변경할 수 있습니다.
1. **[!UICONTROL Description]**:세그먼트에 대한 설명을 제공합니다. 세그먼트를 공유하려면 설명을 제공해야 합니다.
1. **[!UICONTROL Tags]**:기존 [태그 목록에서 선택하거나 새 태그를 만들어 만들고 있는 세그먼트에](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) 태그를 지정합니다.
1. **[!UICONTROL Definitions]**:여기에서 세그먼트를 [](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md)작성 및 구성하고 규칙을 추가하고 컨테이너를 중첩하고 순서를 지정할 수 있습니다. 컨테이너를 선택하고 차원, 세그먼트 또는 지표를 드래그하여 정의에 드롭하는 식으로 새 세그먼트 설명을 입력할 수 있습니다.
1. **[!UICONTROL Show]**:(상단 컨테이너 선택기.) 최상위 수준 [컨테이너](/help/components/c-segmentation/seg-overview.md) ( [!UICONTROL Visitor], [!UICONTROL Visit], [!UICONTROL Hit])를 선택할 수 있습니다. 기본 최상위 수준 컨테이너는 히트 컨테이너입니다.
1. **[!UICONTROL Options]**:(톱니바퀴) 아이콘

   * **[!UICONTROL + Add container]**:세그먼트 정의에 새 컨테이너(최상위 컨테이너 아래)를 추가할 수 있습니다.
   * **[!UICONTROL + Add container from selection]**:정의 필드에서 선택한 요소(다중)에서 새 컨테이너를 만들 수 있습니다.
   * **[!UICONTROL Exclude]**:하나 이상의 차원, 세그먼트 또는 지표를 제외하여 세그먼트를 정의할 수 있습니다.

1. **[!UICONTROL Attribution Models]**:차원 세그멘테이션의 경우 차원 모델은 플로우 시각화를 지원하는 경우와 같이 순차적 세그먼테이션에서 특히 유용합니다.

   * **[!UICONTROL Repeating]** ((기본값):차원에 대한 인스턴스 및 지속적인 값을 포함합니다.
   * **[!UICONTROL Instance]**: 차원에 대한 인스턴스 포함.
   * **[!UICONTROL Non-repeating instance]**: 차원에 대한 고유한 인스턴스(비반복) 포함.
   ![](assets/attribution-models.jpg)

1. **[!UICONTROL Dimensions]**:차원 목록(주황색 세로 막대)에서 차원을 드래그하여 놓습니다.
1. **[!UICONTROL Comparison]**:선택한 연산자를 사용하여 값을 비교하고 제한할 수 있습니다.
1. **[!UICONTROL Value]**:차원이나 세그먼트 또는 지표에 대해 입력하거나 선택한 값.
1. **[!UICONTROL And/Or/Then]**:컨테이너 또는 규칙 사이에 [!UICONTROL AND/OR/THEN] 연산자를 할당합니다. THEN 연산자를 사용하여 [순차적 세그먼트를 정의](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md)할 수 있습니다.
1. **[!UICONTROL Metric]**:(녹색 세로 막대) 지표 목록에서 드래그하여 놓은 지표입니다.
1. **[!UICONTROL Comparison]** 연산자:선택한 연산자를 사용하여 값을 비교하고 제한할 수 있습니다.
1. **[!UICONTROL Value]**:차원이나 세그먼트 또는 지표에 대해 입력하거나 선택한 값.
1. **[!UICONTROL X]**:(삭제) 이 세그먼트 정의 부분을 삭제할 수 있습니다.
1. **[!UICONTROL Save]** 또는 **[!UICONTROL Cancel]**&#x200B;세그먼트를 저장하거나 취소합니다. After clicking **[!UICONTROL Save]**, you are taken to the Segment Manager where you can manage the segment.
1. **[!UICONTROL Search]**:차원, 세그먼트 또는 지표 목록을 검색합니다.
1. **[!UICONTROL Dimensions]**:(목록) 확장하려는 헤더를 클릭합니다.
1. **[!UICONTROL Metrics]**:헤더를 클릭하여 확장합니다.
1. **[!UICONTROL Segments]**:헤더를 클릭하여 확장합니다.
1. **[!UICONTROL Report suite selector]**:이 세그먼트가 저장될 보고서 세트를 선택할 수 있습니다. 모든 보고서 세트의 세그먼트를 계속 활용할 수 있습니다.
1. **[!UICONTROL Segment Preview]**:주요 지표를 미리 보고 올바른 세그먼트가 있는지 여부 및 세그먼트의 범위를 확인할 수 있습니다. 이 세그먼트를 적용하는지 확인할 수 있는 데이터 세트의 분류를 나타냅니다. 3개의 동심원 및 목록을 표시하여 데이터 세트에 대해 실행된 [!UICONTROL Hits]세그먼트의 일치 수 및 비율을 [!UICONTROL Visits][!UICONTROL Visitors] 보여줍니다. 이 차트는 세그먼트 정의를 만들거나 변경한 직후에 업데이트됩니다.
1. **[!UICONTROL Product Compatibility]**:만든 세그먼트가 호환되는 Adobe Analytics 제품(분석 작업 공간, [!UICONTROL Reports & Analytics]애드혹 분석, 데이터 웨어하우스) 목록을 제공합니다. 대부분의 세그먼트는 모든 제품과 호환됩니다. 그러나 일부 연산자 및 차원이 모든 Analytics 제품, 특히 데이터 웨어하우스와 호환되는 것은 [아닙니다](/help/components/c-segmentation/seg-reference/seg-compatibility.md). 이 차트는 세그먼트 정의를 변경한 직후에 업데이트됩니다.

Segments with embedded date ranges continue to operate differently in Analysis Workspace versus [!UICONTROL Reports & Analytics]: In Workspace, a segment with an embedded date range overrides the panel date range. 반대로 [!UICONTROL Reports & Analytics]는 보고서 날짜 범위와 세그먼트의 포함된 날짜 범위의 교차 날짜를 제공합니다.

**[!UICONTROL Publish to Experience Cloud (for `<report suite name>`)]**:(화면에 표시되지 않음) 이 옵션은 이 세그먼트를 저장할 보고서 세트가 Experience Cloud에 대해 [활성화된 경우에만 나타납니다](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md). By publishing a segment to the Experience Cloud, you can use the segment for marketing activity in the [!UICONTROL Audience Library], [!DNL Target], and [!DNL Audience Manager]. 세그먼트 제목 및 설명이 필요합니다.

>[!NOTE] Analytics에서 게시된 세그먼트를 편집하거나 삭제할 수 있습니다. 세그먼트가 사용 중인 경우 세그먼트를 편집할 때 경고 메시지가 표시됩니다. 게시된 세그먼트가 Adobe [!DNL Target]에서 사용 중이면 삭제할 수 없습니다.

![](assets/segment_publish_to_mac_copy.png)

>[!IMPORTANT]
>
>처리가 지연되는 것을 방지하기 위해 Analytics에서 공유하는 대상 수를 20명으로 제한해야 합니다. Analytics에서 Experience Cloud에 공유된 대상은 2천만 명의 고유 구성원을 초과할 수 없습니다. 또한 캐싱으로 인해 Analytics에서 삭제된 보고서 세트는 삭제가 Experience Cloud에 표시되기 12시간이 필요합니다.

>[!IMPORTANT]
>
>방문자가 Analytics에서 공유한 대상 자격을 얻으면 24~ 48시간이 지연된 후에 [!DNL Target], [!DNL Advertising Cloud] 및 [!DNL Campaign]에서 정보를 실행할 수 있습니다.

## 세그먼트 작성 {#build-segments}

1. 차원, 세그먼트 또는 지표 이벤트를 왼쪽 창에서 [!UICONTROL Definitions] 필드로 드래그하면 됩니다.

   ![](assets/drag_n_drop_dimension.png)

   요소를 로 드래그하면 기본 최상위 수준 [!UICONTROL Hit] 컨테이너가 표시됩니다 [!UICONTROL Definitions]. You can change the container type to Visit or Visitor from the **[!UICONTROL Show]** drop-down menu.

1. 드롭다운 메뉴에서 [연산자](/help/components/c-segmentation/seg-reference/seg-operators.md)를 설정합니다.
1. 선택한 항목에 대한 값을 입력하거나 선택합니다.
1. Add additional containers if needed, using **[!UICONTROL And]**, **[!UICONTROL Or]**, or **[!UICONTROL Then]** rules.
1. 컨테이너를 배치하고 규칙을 설정한 후 오른쪽 상단의 유효성 검사 차트에서 세그먼트 결과를 확인합니다. 유효성 검사기는 만든 세그먼트와 일치하는 페이지 보기, 방문 및 고유 방문자의 비율 및 절대 수를 나타냅니다.
1. Under **[!UICONTROL Tags]**, [tag](/help/components/c-segmentation/c-segmentation-workflow/seg-tag.md) the container by selecting an existing tag or creating a new one.
1. Click **[!UICONTROL Save]** to save the segment.

이제 여러 가지 방법으로 세그먼트에 태깅하고, 세그먼트를 공유 및 관리할 수 있는 [세그먼트 관리자](/help/components/c-segmentation/c-segmentation-workflow/seg-manage.md)가 표시합니다.

## 컨테이너 작성 및 중첩 {#section_1C38F15703B44474B0718CEF06639EFD}

[컨테이너 프레임워크를 작성한 다음](/help/components/c-segmentation/seg-overview.md) 사이에 논리 규칙 및 연산자를 배치할 수 있습니다.

1. 클릭 **[!UICONTROL Options > Add Container]**.

   ![](assets/add_container.png)

   새 [!UICONTROL Hit] 컨테이너는 식별된 [!UICONTROL Hit] (페이지 보기) 없이 열립니다.

   ![](assets/new_container.png)

1. 필요에 따라 컨테이너 유형을 변경합니다.
1. 왼쪽 창에서 차원, 세그먼트 또는 이벤트를 컨테이너로 드래그합니다.
1. Continue to add new containers from the top-level **[!UICONTROL Options]** > **[!UICONTROL Add container]** button at the top of the definition, or add containers from within a container to nest logic.

   **또는**

   하나 이상의 규칙을 선택한 다음 **[!UICONTROL Options]** > **[!UICONTROL Add container from selection]**&#x200B;을 클릭합니다. 이렇게 하면 선택 영역이 별도의 컨테이너로 바뀝니다.

## 세그먼트에서 날짜 범위 사용 {#concept_252A83D43B6F4A4EBAB55F08AB2A1ACE}

진행 중인 캠페인 또는 이벤트에 대한 질문에 답변하는 순서로 롤링 날짜 범위를 포함하는 세그먼트를 작성할 수 있습니다.

예를 들면 &quot;지난 60일 동안 구매한 모든 사람&quot;을 포함하는 세그먼트를 쉽게 작성할 수 있습니다.

방문 컨테이너를 만들고 그 안에 AND 연산자로 [!UICONTROL Last 60 days] 시간 범위 및 지표를 [!UICONTROL Orders is greater than or equal to 1]추가합니다.

![](assets/date-ranges.png)

## 세그먼트 스택 {#task_58140F17FFD64FF1BC30DC7B0A1B0E6D}

세그먼트 스택은 &#39;and&#39; 연산자를 사용하여 각 세그먼트의 기준을 결합한 다음 결합된 기준을 적용하여 작동합니다.

예를 들어 &quot;휴대폰 사용자&quot; 세그먼트 및 &quot;미국 지역&quot; 세그먼트는 미국의 휴대폰 사용자에 대한 데이터만 반환합니다.

이러한 세그먼트를 사용자가 원하는 대로 사용할 수 있도록 세그먼트 라이브러리에 포함할 수 있는 구성 요소 또는 모듈로 생각해 보십시오. 이렇게 하면 필요한 세그먼트 수를 대폭 줄일 수 있습니다. 예를 들어 40개의 세그먼트가 있다고 가정합니다.

* 다른 국가의 휴대폰 사용자를 위한 20개(US_mobile, Germany_mobile, France_mobile, Brazil_mobile 등)
* 다른 국가의 태블릿 사용자를 위한 20개(US_tablet, Germany_tablet, France_tablet, Brazil_tablet 등)

세그먼트 스택을 사용하여 세그먼트 수를 22개로 줄이고 필요에 따라 스택할 수 있습니다. 다음 세그먼트를 만들어야 합니다.

* 모바일 사용자를 위한 단일 세그먼트
* 태블릿 사용자를 위한 단일 세그먼트
* 서로 다른 지역에 대해 20개의 세그먼트

>[!NOTE] 2개의 세그먼트를 스택할 때 기본적으로 AND 문으로 연결됩니다. OR 문으로 변경할 수 없습니다.

1. 세그먼트 빌더로 이동합니다.
1. 세그먼트에 대한 제목과 설명을 제공합니다.

   단계 결과 1. Click **[!UICONTROL Show Segments]** to bring up the list of segments in the left navigation.

   단계 결과 1. 스택할 세그먼트를 세그먼트 정의 캔버스로 드래그하여 놓습니다. 다음은 기존 세그먼트 &quot;태블릿의 방문&quot; 및 &quot;미국 지역&quot;을 스택하는 세그먼트의 예입니다.

   ![](assets/seg_stack2.png)

1. 세그먼트를 저장합니다.

   단계 결과

## 세그먼트 템플릿 사용 {#concept_5098446CC78D441E93B8E4D1D1EA6558}

템플릿은 미리 구성된 이전 Suite 세그먼트를 나타냅니다.

In the Segment Manager, click **[!UICONTROL Add]**, which takes you to the Segment Builder. 이제 세그먼트 아이콘 ![](assets/segment_icon.png)을 클릭하여 

세그먼트 레일을 표시합니다. 세그먼트 템플릿이 세그먼트 목록 하단에 나타납니다. 템플릿 이름 왼쪽에 있는 폴더 아이콘으로 식별할 수 있습니다.

![](assets/seg_template.png)

이러한 템플릿을 정의 캔버스로 드래그하여 정의한 대로 사용하거나 수정할 수 있습니다.

<table id="table_98B87D807E9344C9BEBF072C65D87B1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 템플릿 이름 </th> 
   <th colname="col2" class="entry"> 정의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 장바구니 포기 </td> 
   <td colname="col2">장바구니에 항목을 추가했지만 주문하지 않은 방문자에 대한 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 순차적 세그먼트에 대한 규칙은 <p> 장바구니 추가가 null이 아닙니다. </p> <p>그런 다음 </p> <p>주문은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최초 방문 </td> 
   <td colname="col2">최대 [1]회 방문한 방문자에 대한 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>방문 번호가 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비구매자 </td> 
   <td colname="col2">주문 이벤트에 참가하지 않은 방문자에 대한 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문자입니다. 이 세그먼트는 제외 로직을 사용합니다. 규칙은 <p>주문은 null이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비단일 페이지 방문 (비바운스 수) </td> 
   <td colname="col2">두 번 이상 방문한 방문자에 대한 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문자입니다. 이 세그먼트는 제외 로직을 사용합니다. 규칙은 <p>단일 액세스가 null이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 유료 검색 </td> 
   <td colname="col2">유료 검색에서 온 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>유료 검색은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구매자 </td> 
   <td colname="col2">주문 이벤트에 참여한 방문자에 대한 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문자입니다. 규칙은 <p>주문은 null이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재방문 </td> 
   <td colname="col2">한 번 이상 방문한 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>방문 번호가 1보다 큽니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 단일 페이지 방문 횟수 </td> 
   <td colname="col2"> 해당 방문 동안 여러 페이지 보기를 제출할 수 있더라도 단일 페이지 값이 표시되는 방문의 데이터를 봅니다. 종료 링크 이벤트가 있는 단일 페이지 방문이 세그먼트에 포함됩니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>단일 페이지 방문 횟수는 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 본 제품이 장바구니에 추가되지 않음 </td> 
   <td colname="col2">제품을 열람했지만 장바구니에 추가하지 않은 방문자에 대한 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 순차적 세그먼트에 대한 규칙은 <p>제품 보기가 null이 아닙니다. </p> <p>그런 다음 </p> <p> 장바구니 추가는 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 캠페인에서 방문 </td> 
   <td colname="col2">캠페인에서 참조한 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>추적 코드가 null이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 모바일 기기로부터 찾아온 방문 </td> 
   <td colname="col2">모바일 장치를 사용하는 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>모바일 장치가 null이 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 자연어 검색으로 찾아온 방문 </td> 
   <td colname="col2">유료 검색에서 시작하지 않은 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>유료 검색은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비모바일 장치에서 찾아온 방문 </td> 
   <td colname="col2">모바일 장치를 사용하지 않는 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 이 세그먼트는 제외 로직을 사용합니다. 규칙은 <p>모바일 장치 유형이 휴대폰임 </p> <p>또는 </p> <p>모바일 장치 유형이 태블릿입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 휴대폰의 방문 </td> 
   <td colname="col2">휴대폰을 사용하는 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>장치 유형이 휴대폰입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 검색 엔진의 방문 </td> 
   <td colname="col2">검색 엔진에서 참조한 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>레퍼러 유형이 검색 엔진입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 소셜 사이트를 통한 방문 수 </td> 
   <td colname="col2">소셜 사이트에서 참조한 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>레퍼러 유형이 소셜 네트워크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 태블릿의 방문 </td> 
   <td colname="col2">태블릿을 사용하여 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>장치 유형이 태블릿입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 ID를 갖는 방문 </td> 
   <td colname="col2">지속적인 쿠키가 필요한 사이트 방문자의 데이터를 봅니다. 세그먼트 정의에서 컨테이너는 방문입니다. 규칙은 <p>영구 쿠키는 1입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예: 캠페인 방문자 세그먼트 {#concept_61AC6115097B4EB3AEFE8CE98F38315D}

자주 사용되는 이 세그먼트의 예를 표시합니다.

많은 고객이 특정 캠페인에 응답한 방문자의 지표를 보려고 합니다. 캠페인 방문자 세그먼트를 만드는 것은 이 데이터를 얻는 쉬운 방법입니다.

세그먼트 빌더에서 이 세그먼트를 작성하면 최상위 방문 컨테이너에서 캠페인 차원(이 경우 캠페인 이름)을 드래그합니다.

![](assets/seg_campaign_visitor.png)

(선택 사항) 모든 캠페인 관련 세그먼트를 쉽게 필터링하려면 이 세그먼트에 캠페인 태그를 적용할 수도 있습니다.
