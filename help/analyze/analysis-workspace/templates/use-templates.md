---
description: Analysis Workspace에서 템플릿을 사용하는 방법에 대한 개요입니다.
title: 템플릿 사용
feature: Analysis Workspace
role: User, Admin
exl-id: 9e5d1b35-e2b3-4fa5-af12-67bb913675bc
source-git-commit: dc1744cf4816971d52364a3131a12601787d9819
workflow-type: tm+mt
source-wordcount: '18673'
ht-degree: 83%

---

# 템플릿 사용

Analysis Workspace의 템플릿(또는 회사 템플릿)은 가장 일반적인 보고 시나리오에 대한 빠른 인사이트를 제공합니다. 다음은 템플릿으로 답변할 수 있는 질문의 예입니다.

* 사이트 방문자 수
* 해당 방문자 중 고유 방문자 수 (한 번만 카운트)
* 방문자의 사이트 방문 경로 (예: 링크를 따라 사이트를 방문했는지 또는 사이트에 직접 방문했는지 여부)
* 방문자가 사이트 콘텐츠를 검색하는 데 사용한 키워드
* 특정 페이지 또는 전체 사이트에서 머문 시간
* 방문자가 클릭한 링크와 사이트를 떠난 시점
* 매출 생성이나 전환 이벤트 생성에 가장 효과적인 마케팅 채널
* 비디오 보는 데 걸린 시간
* 방문자가 사이트를 방문하는 데 사용한 브라우저 및 디바이스

다음 정보는 Analysis Workspace의 [!UICONTROL 템플릿] 탭에서 템플릿에 액세스하고 사용하는 방법에 대해 설명합니다.

## 템플릿 액세스 및 실행

1. Analysis Workspace에서 [!UICONTROL **Workspace**] 탭을 선택합니다.

   <!--update screenshot -->

   ![보고서 탭](assets/view-prebuilt-templates.png)

1. [!UICONTROL **템플릿**] 섹션에서 다음 탭 중 하나를 선택합니다.

   * **[!UICONTROL Adobe 템플릿]**: Adobe에서 제공한 모든 템플릿을 표시합니다.

   * **[!UICONTROL _login_company_name _템플릿]**: 조직에 대해 만들어진 모든 회사 템플릿을 표시합니다.

     관리자만 회사 템플릿을 만들 수 있습니다. 회사 템플릿을 만드는 방법에 대한 자세한 내용은 [템플릿 만들기 및 관리](/help/analyze/analysis-workspace/reports/create-company-reports.md)를 참조하십시오.

1. 다음 옵션 중 하나를 사용하여 사용 가능한 템플릿을 보는 방법을 변경합니다.

   * 열 보기 ![열 보기 아이콘](assets/column-view-icon.png) 또는 카드 보기 ![카드 보기 아이콘](assets/card-view-icon.png) 아이콘을 선택하여 열 보기에서 템플릿을 볼 것인지 카드 보기에서 템플릿을 볼 것인지를 선택합니다.

   * 카드 보기 ![카드 보기 아이콘](assets/card-view-icon.png)을 사용할 때 다음 정렬 순서 중에서 선택하세요. **[!UICONTROL 가장 최근에 사용됨]**, **[!UICONTROL 가장 자주 사용됨]**, **[!UICONTROL 알파벳]**, **[!UICONTROL 범주형]**.

1. 검색 필드에서 찾을 템플릿의 이름을 입력한 다음 템플릿 목록에서 해당 이름을 선택합니다. prop, eVar 및 이벤트 번호로 템플릿 목록을 검색할 수도 있습니다. <!-- still true? -->

   또는

   보려는 템플릿의 범주를 선택한 다음 템플릿 목록에서 템플릿을 선택합니다.

   >[!TIP]
   >
   >화살표 키를 사용하여 메뉴를 탐색하려면 슬래시 키(/)를 누른 다음, 아래쪽 화살표 키를 누릅니다. Enter 키를 눌러 선택한 템플릿을 로드합니다.

   사용 가능한 템플릿 목록은 아래의 [사용 가능한 템플릿](#available-reports) 섹션을 참조하십시오.

## 템플릿을 기반으로 프로젝트 만들기 {#use-reports}

템플릿이 사용자의 요구 사항에 정확히 맞지 않을 수 있지만 사용자에게 가까이 다가갈 수 있습니다. 이러한 경우 템플릿을 시작점으로 사용한 다음 특정 목적에 가장 적합하게 사용자 지정할 수 있습니다.

변경 후 템플릿에서 다른 곳으로 이동하면 변경 사항을 저장하거나 취소하라는 메시지가 표시됩니다. 템플릿에 변경 사항을 저장하면 템플릿이 새 프로젝트로 저장됩니다.

템플릿을 사용자 정의하고 프로젝트로 저장하려면 다음과 같이 하십시오.

1. Adobe Analytics에서 [!UICONTROL **작업 영역**] 탭을 선택합니다.

1. [!UICONTROL **템플릿**] 탭을 선택합니다.

1. 보려는 템플릿을 선택합니다. 예를 들어 [!UICONTROL **가장 자주 사용하는 항목**]&#x200B;에서 [!UICONTROL **페이지**] 템플릿을 선택합니다.

   ![페이지 보고서](assets/pages-report.png)

1. Analysis Workspace에 표시되는 페이지 템플릿에는 두 개의 [시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)([막대 차트](/help/analyze/analysis-workspace/visualizations/bar.md) 및 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md))와 [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md)이 표시됩니다. 사용된 지표는 발생 횟수입니다.
1. 다음 중 하나를 수행합니다.

   * 템플릿을 봅니다.
   * 하나 이상의 세그먼트를 상단의 세그먼트 드롭 영역으로 드래그합니다. 예를 들어 [!UICONTROL **모바일 고객**]&#x200B;을 드래그하여 결과를 봅니다.
   * 오른쪽 상단의 달력으로 이동하여 날짜 범위를 변경합니다.
   * 차원 분류를 추가하고, 다른 지표를 드래그하고, 일반적으로 필요에 따라 템플릿을 사용자 정의합니다.

1. (선택 사항) [!UICONTROL **프로젝트**] > [!UICONTROL **저장**]&#x200B;을 선택하여 템플릿을 프로젝트로 저장합니다.

   템플릿은 새 프로젝트로 저장됩니다. 기존 템플릿은 수정되지 않습니다. 프로젝트 저장에 대한 자세한 내용은 [프로젝트 저장](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md)을 참조하세요.

## 사용 가능한 템플릿

사용 가능한 모든 사전 설치된 템플릿에 액세스하려면 다음을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **Workspace**] 탭을 선택한 다음 [!UICONTROL **템플릿**] 탭을 선택합니다.

   사전 빌드된 템플릿은 범주별로 구성됩니다.

   <!--add screenshot-->

1. 범주를 선택하여 범주 내에서 템플릿을 봅니다.

   다음 섹션은 사용 가능한 범주에 해당하며 각 템플릿에 대한 정보를 제공합니다.

   * [[!UICONTROL ](#most-popular)

   * [[!UICONTROL ](#engagement)

### 최고 인기 항목 {#most-popular}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--unitsOvertimeReport"
>title="모든 주문 내에서 구매된 상품의 총 개수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 시간이 지남에 따라 판매량이 어떻게 증가하거나 감소하는지 더 잘 이해하는 데 도움이 될 수 있습니다. 세그먼트를 적용하여 가장 많은 상품을 구매하는 고객 또는 지역과 시간 경과에 따른 판매량 트렌딩을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 판매량을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 기간 동안의 판매량을 비교할 수도 있습니다.<br/>이 템플릿은 일 차원과 판매량 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!--both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--training"
>title="교육 튜토리얼 템플릿"
>abstract="일반적인 Analysis Workspace 용어와 첫 번째 분석 구축 단계를 알아보십시오."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--pagesRankedReport"
>title="방문 빈도가 가장 높은 페이지와 가장 낮은 페이지를 파악합니다."
>abstract="**이를 통해** 대상자와 대상자가 가장 관심을 갖는 정보의 유형을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 조회수가 적은 페이지의 가시성을 높이기 위해 페이지 메타데이터를 조정하거나 가장 많이 조회된 페이지의 콘텐츠를 향상시키는 데 시간을 할애하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 페이지 차원과 페이지 조회수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--pageViewsOvertimeReport"
>title="총 페이지 조회수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. "
>abstract="**이를 통해** 사이트의 트래픽이 시간이 지남에 따라 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 사이트 트래픽을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 트래픽을 비교할 수도 있습니다.<br/>이 템플릿은 일 차원과 페이지 조회수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--visitsOvertimeReport"
>title="총 방문 횟수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 사이트의 트래픽이 시간이 지남에 따라 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 사이트 트래픽을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 트래픽을 비교할 수도 있습니다.<br/>이 템플릿은 일 차원과 방문 횟수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--visitorsOvertimeReport"
>title="총 고유 방문자 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. "
>abstract="**이를 통해** 사이트의 도달 범위와 대상자 수가 시간이 지남에 따라 또는 이전 기간과 비교하여 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 최근 시작된 마케팅 캠페인이 캠페인 시작 전후의 고유 방문자 수를 비교하여 새로운 사람들을 사이트로 유치하는 데 성공했는지 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 휴일 기간에 방문하는 사람 수를 전년 대비 비교할 수도 있습니다.<br/>이 템플릿은 일 차원과 고유 방문자 수 지표를 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--keyMetricsReport"
>title="페이지 조회수, 방문자 수, 고유 방문자 수 지표를 나란히 표시한 보고서를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 이러한 중요한 지표를 비교하여 사이트를 방문한 고유 사용자 수, 페이지 방문 횟수 및 세션 수를 보다 완벽하게 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 특정 주 또는 월에 사이트를 방문한 사람별로 조회한 평균 페이지 수, 일년 중 특정 시간대 또는 마케팅 캠페인이 실행되기 전과 후에 어떻게 변화했는지 평가하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 일 차원, 페이지 조회수 지표, 방문자 수 지표, 고유 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--siteSectionRankedReport"
>title="사이트의 최고 인기 항목이나 성과가 가장 높은 섹션을 확인할 수 있습니다."
>abstract="**이렇게 하면** 사이트에서 가장 많이 방문하는 섹션을 더 잘 파악할 수 있습니다.<br>**학습한 내용을 바탕으로** 제공하는 제품이나 서비스 중 어느 것이 가장 많은 관심을 불러일으키는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 사이트 섹션 차원과 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--next-page-report"
>title="특정 장소 방문 직후에 사람들이 가장 많이 가는 장소를 확인할 수 있습니다."
>abstract="**이를 통해** 특정 페이지를 방문한 후 사용자 행동을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 페이지 디자인이나 레이아웃을 최적화하여 어떻게 더 바람직한 페이지(예: 구매 페이지 또는 리뷰 작성 페이지)로 유도할 수 있는지 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 페이지 차원과 이벤트 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--previous-page-report"
>title="특정 장소 방문 직전에 사람들이 가장 많이 가는 장소를 확인할 수 있습니다."
>abstract="**이를 통해** 가장 많은 트래픽을 특정 페이지로 전송하는 페이지를 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 이전 페이지로 표시되지 않는 페이지에 현재 페이지로 연결되는 더 눈에 띄는 링크가 필요한지 여부를 평가하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--campaignRankedReport"
>title="사이트로 트래픽을 유도하는 데 가장 성공한 링크를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트에 접속하는 데 가장 많이 사용된 추적 코드(및 해당 코드와 연결된 링크)를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트에 링크를 추가하는 위치에 대한 전략을 조정하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 추적 코드 차원과 방문 횟수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--productsRankedReport"
>title="제품별 주문 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시됩니다."
>abstract="**이를 통해** 어떤 제품의 수요가 가장 높거나 가장 낮은지 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 마케팅 전략을 조정하여 성과가 높은 제품을 홍보하거나 성과가 저조한 제품을 개선하거나 중단하는 등 다양한 작업을 수행할 수 있습니다. 데이터 분석을 기반으로 제품 재고를 조정할 수도 있습니다.<br/>이 템플릿은 제품 차원과 주문 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--lastTouchChannelRankedReport"
>title="방문자가 참여 기간(기본 30일) 동안 매칭되는 최신 마케팅 채널을 확인할 수 있습니다."
>abstract="**이를 통해** 전환하는 사람들을 사이트로 유도하는 데 가장 효과적인 마케팅 채널을 이해하는 데 도움이 될 수 있습니다.<br/>**학습한 내용을 바탕으로** 성과가 좋은 채널에 더 많은 리소스를 할당하거나 성능이 저조한 채널에 더 적은 리소스를 할당하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 마지막 터치 채널 차원과 고유 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--lastTouchChannelDetailRankedReport"
>title="방문자가 참여 기간(기본은 30일) 동안 매칭되는 최신 마케팅 채널의 세부 정보를 확인할 수 있습니다."
>abstract="**이를 통해** 전환을 유도하는 데 가장 효과적이었던 마케팅 채널뿐만 아니라 해당 마케팅 채널에 대한 세부 정보를 파악할 수 있습니다. 예를 들어 방문자가 사이트에 도달하고 &#39;유료 검색&#39; 마케팅 채널과 일치하는 경우 채널 세부 사항을 사용하여 사용한 검색 엔진 또는 검색한 키워드를 확인할 수 있습니다.<br/>**학습한 내용을 바탕으로** 성과가 좋은 채널에 더 많은 리소스를 할당하거나 성능이 저조한 채널에 더 적은 리소스를 할당하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 마지막 터치 채널 세부 정보 차원과 고유 방문자 수 지표를 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--revenueOvertimeReport"
>title="모든 주문 내에서 모든 구매된 제품의 통화량을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 시간이 지남에 따라 수익이 어떻게 증가하거나 감소하는지 이해하는 데 도움이 될 수 있습니다. 이 지표를 임의의 차원과 결합하여 매출에 기여한 차원 항목을 알아볼 수 있습니다.<br/>**학습한 내용을 바탕으로** 이전 트렌드를 기반으로 미래 수익을 예측하는 등 다양한 작업을 수행할 수 있습니다. 추적 코드 차원과 같은 다른 차원을 추가하여 가장 많은 수익을 창출하는 캠페인을 알아볼 수도 있습니다.<br/>이 템플릿은 일 차원과 매출 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--ordersOvertimeReport"
>title="총 구매 이벤트 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 시간이 지남에 따라 제품 및 서비스에 대한 관심이 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다. 세그먼트를 적용하여 가장 많은 주문을 하는 고객 또는 지역과 시간 경과에 따른 주문 트렌딩을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 주문을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 주문을 비교할 수도 있습니다.<br/>이 템플릿은 일 차원과 주문 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

다음 템플릿을 사용할 수 있습니다.

| 템플릿 이름 | 이 템플릿 <!-- What do you do with it? What can it help you learn? and What are the potential actions? -->을(를) 사용하는 이유 |
| --- | --- | 
| [!UICONTROL **교육 튜토리얼**] | 첫 번째 분석을 구축하기 위한 일반적인 Analysis Workspace 용어 및 단계에 대해 알아봅니다 |
| [!UICONTROL **페이지**] | <!--duplicated in Engagement section--> 방문 빈도가 가장 높은 페이지와 가장 낮은 페이지를 파악합니다. <p>**이를 통해** 대상자와 대상자가 가장 관심을 갖는 정보의 유형을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라** 페이지 메타데이터를 조정하여 더 적게 본 페이지의 가시성을 향상시키거나 가장 많이 본 페이지의 콘텐츠를 개선하는 등 여러 가지 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [페이지 차원](/help/components/dimensions/page.md) 및 [페이지 보기 횟수 지표](/help/components/metrics/page-views.md)를 사용합니다.</p> |
| [!UICONTROL **페이지 보기 수**] | <!--duplicated in Engagement section--> 총 페이지 조회수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 사이트의 트래픽이 시간이 지남에 따라 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 사이트 트래픽을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 트래픽을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [페이지 보기 횟수 지표](/help/components/metrics/page-views.md)를 사용합니다.</p> |
| [!UICONTROL **방문 횟수**] | <!--duplicated in Engagement section--> 총 방문 횟수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 사이트의 트래픽이 시간이 지남에 따라 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 사이트 트래픽을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 트래픽을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [방문 횟수 지표](/help/components/metrics/visits.md)를 사용합니다.</p> |
| [!UICONTROL **방문자 수**] | <!--duplicated in Engagement section--> 총 고유 방문자 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 사이트의 도달 범위와 대상자 수가 시간이 지남에 따라 또는 이전 기간과 비교하여 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 최근 시작된 마케팅 캠페인이 캠페인 시작 전후의 고유 방문자 수를 비교하여 새로운 사람들을 사이트로 유치하는 데 성공했는지 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 휴일 기간에 방문하는 사람 수를 전년 대비 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)를 사용합니다.</p> |
| [!UICONTROL **주요 지표**] | <!--duplicated in Engagement section--> 페이지 조회수, 방문자 수, 고유 방문자 수 지표를 나란히 표시한 보고서를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 이러한 중요한 지표를 비교하여 사이트를 방문한 고유 사용자 수, 페이지 방문 횟수 및 세션 수를 보다 완벽하게 파악할 수 있습니다.</p><p>**학습한 내용에 따라** 주어진 주 또는 월로 사이트를 방문할 때 각 사용자가 본 평균 페이지 수와 해당 연도의 특정 기간 동안 또는 마케팅 캠페인 실행 전후에 변경된 정도를 평가하는 등 여러 가지 작업을 수행할 수 있습니다. </p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md), [페이지 보기 횟수 지표](/help/components/metrics/page-views.md), [방문 횟수 지표](/help/components/metrics/visits.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)을 사용합니다.</p> |
| [!UICONTROL **사이트 섹션**] | 사이트의 최고 인기 항목이나 성과가 가장 높은 섹션을 확인할 수 있습니다. <p>**이렇게 하면** 사이트에서 가장 많이 방문하는 섹션을 더 잘 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 제공하는 제품이나 서비스 중 어느 것이 가장 많은 관심을 불러일으키는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 [사이트 섹션 차원](/help/components/dimensions/site-section.md) 및 [방문 횟수 지표](/help/components/metrics/visits.md)를 사용합니다.</p> |
| [!UICONTROL **추적 코드**] | 사이트로 트래픽을 유도하는 데 가장 성공한 링크를 확인할 수 있습니다. <p>**이를 통해** 사이트에 접속하는 데 가장 많이 사용된 추적 코드(및 해당 코드와 연결된 링크)를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트에 링크를 추가하는 위치에 대한 전략을 조정하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [추적 코드 차원](/help/components/dimensions/tracking-code.md) 및 [방문 횟수 지표](/help/components/metrics/visits.md)를 사용합니다.</p> |
| [!UICONTROL **다음 페이지**] | 특정 장소 방문 직후에 사람들이 가장 많이 가는 장소를 확인할 수 있습니다. <p>**이를 통해** 특정 페이지를 방문한 후 사용자 행동을 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 페이지 디자인이나 레이아웃을 최적화하여 어떻게 더 바람직한 페이지(예: 구매 페이지 또는 리뷰 작성 페이지)로 유도할 수 있는지 평가하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 페이지 차원과 이벤트 지표를 사용합니다.</p> |
| [!UICONTROL **이전 페이지**] | 특정 장소 방문 직전에 사람들이 가장 많이 가는 장소를 확인할 수 있습니다. <p>**이를 통해** 가장 많은 트래픽을 특정 페이지로 전송하는 페이지를 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 이전 페이지로 표시되지 않는 페이지에 현재 페이지로 연결되는 더 눈에 띄는 링크가 필요한지 여부를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 페이지 차원과 이벤트 지표를 사용합니다.</p> |
| [!UICONTROL **제품**] | 제품별 주문 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시됩니다. <p>**이를 통해** 어떤 제품의 수요가 가장 높거나 가장 낮은지 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 마케팅 전략을 조정하여 성과가 높은 제품을 홍보하거나 성과가 저조한 제품을 개선하거나 중단하는 등 다양한 작업을 수행할 수 있습니다. 데이터 분석을 기반으로 제품 재고를 조정할 수도 있습니다.</p><p>이 템플릿은 [제품 차원](/help/components/dimensions/product.md) 및 [주문 지표](/help/components/metrics/orders.md)를 사용합니다.</p> |
| [!UICONTROL **마지막 터치 채널**] | 방문자가 참여 기간(기본 30일) 동안 매칭되는 최신 마케팅 채널을 확인할 수 있습니다.<p>**이를 통해** 전환하는 사람들을 사이트로 유도하는 데 가장 효과적인 마케팅 채널을 이해하는 데 도움이 될 수 있습니다.</p><p>**학습한 내용을 바탕으로** 성과가 좋은 채널에 더 많은 리소스를 할당하거나 성능이 저조한 채널에 더 적은 리소스를 할당하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [마지막 터치 채널 차원](/help/components/dimensions/last-touch-channel.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)를 사용합니다.</p> |
| [!UICONTROL **마지막 터치 채널 세부 사항**] | 방문자가 참여 기간(기본은 30일) 동안 매칭되는 최신 마케팅 채널의 세부 정보를 확인할 수 있습니다.<p>**이를 통해** 전환을 유도하는 데 가장 효과적이었던 마케팅 채널뿐만 아니라 해당 마케팅 채널에 대한 세부 정보를 파악할 수 있습니다. 예를 들어 방문자가 사이트에 도달하고 &#39;유료 검색&#39; 마케팅 채널과 일치하는 경우 채널 세부 사항을 사용하여 사용한 검색 엔진 또는 검색한 키워드를 확인할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 성과가 좋은 채널에 더 많은 리소스를 할당하거나 성능이 저조한 채널에 더 적은 리소스를 할당하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [마지막 터치 채널 세부 정보 차원](/help/components/dimensions/last-touch-detail.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)를 사용합니다.</p> |
| [!UICONTROL **매출**] | 모든 주문 내에서 모든 구매된 제품의 통화량을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다.<p>**이를 통해** 시간이 지남에 따라 수익이 어떻게 증가하거나 감소하는지 이해하는 데 도움이 될 수 있습니다. 이 지표를 임의의 차원과 결합하여 매출에 기여한 차원 항목을 알아볼 수 있습니다.</p><p>**학습한 내용을 바탕으로** 이전 트렌드를 기반으로 미래 수익을 예측하는 등 다양한 작업을 수행할 수 있습니다. 추적 코드 차원과 같은 다른 차원을 추가하여 가장 많은 수익을 창출하는 캠페인을 알아볼 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [매출 지표](/help/components/metrics/revenue.md)를 사용합니다.</p> |
| [!UICONTROL **주문**] | 총 구매 이벤트 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 시간이 지남에 따라 제품 및 서비스에 대한 관심이 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다. 세그먼트를 적용하여 가장 많은 주문을 하는 고객 또는 지역과 시간 경과에 따른 주문 트렌딩을 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 주문을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 주문을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [주문 지표](/help/components/metrics/orders.md)를 사용합니다.</p> |
| [!UICONTROL **판매량**] | 모든 주문 내에서 구매된 상품의 총 개수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 시간이 지남에 따라 판매량이 어떻게 증가하거나 감소하는지 더 잘 이해하는 데 도움이 될 수 있습니다. 세그먼트를 적용하여 가장 많은 상품을 구매하는 고객 또는 지역과 시간 경과에 따른 판매량 트렌딩을 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 판매량을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 기간 동안의 판매량을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [단위 지표](/help/components/metrics/units.md)을 사용합니다.</p> |

### 참여 {#web-engagement}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--real-time"
>title="현재 사이트에서 수집 중인 차원 및 지표를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트의 트렌드를 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 신속히 대응하고 현재 마케팅 콘텐츠 및 캠페인의 성과를 효과적으로 관리하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentVisitOvertimeReport"
>title="방문자가 사이트를 방문할 때마다 소비한 평균 시간을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 일 차원과 방문당 체류 시간(초) 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timePriorRankedReport"
>title="성공 이벤트가 발생하기 전까지 사용자가 소비한 평균 시간을 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 구매 등 원하는 작업을 수행하는 데 소요되는 시간을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트 변경이 방문자의 성공 이벤트에 빠르게 도달할 수 있는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 이벤트까지 남은 시간 차원과 고유 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--falloutReport"
>title="미리 정의된 페이지 시퀀스를 통해 사람들이 어디에서 떠나거나 계속 읽는지 확인할 수 있습니다."
>abstract="**이를 통해** 사용자가 사용자 여정 중 어디에서 이탈하는지 더 잘 이해할 있습니다.<br/>**학습한 내용을 바탕으로** 사이트의 특정 프로세스(예: 구매 또는 등록 프로세스)를 통한 전환율을 분석하거나 사이트에서 발생하는 이벤트 간의 상관 관계를 분석하는 등 다양한 작업을 수행할 수 있습니다. 예를 들어 개인정보 처리방침을 본 사람 중 실제로 제품을 구매한 사람의 비율을 확인할 수 있습니다. 또한 이 템플릿을 사용하여 동일한 보고서에서 두 개의 서로 다른 세그먼트를 나란히 비교할 수도 있습니다.<br/>이 템플릿은 폴아웃 시각화를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cross-device-analysis"
>title="여정의 모든 지점에서 사람들이 사용한 디바이스를 확인할 수 있습니다."
>abstract="**이를 통해** 얼마나 많은 사람들이 브랜드와 상호 작용하는지, 그들이 사용하는 디바이스 유형은 무엇인지와 여러 디바이스를 사용하는 것이 사용자 경험에 어떤 영향을 미치는지 더 잘 이해할 수 있습니다. 예를 들어 사람들이 모바일 디바이스에서 작업을 시작한 다음 나중에 데스크탑 PC로 이동하여 작업을 완료하는 빈도는 얼마나 됩니까? 사용자가 하나의 디바이스에서 다른 디바이스로 이동하는 가장 일반적인 경로는 무엇입니까? 어디에서 중단됩니까? 어디에서 성공합니까? 등의 질문에 대한 답을 구할 수 있습니다.<br/>**학습한 내용을 바탕으로** 모바일 경험에 대해 사용자 여정의 특정 부분을 최적화하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 플로우 시각화, 폴아웃 시각화, 코호트 분석, 사용자 지표 및 고유 디바이스 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--web-retention"
>title="사이트에서 충성도가 높은 사용자가 누구인지, 그들이 사이트에서 무엇을 하고 있는지 확인할 수 있습니다."
>abstract="**이를 통해** 일반 사용자가 사이트를 방문하는 횟수, 사람들이 사이트에 재방문하는 빈도 및 재방문 사이의 일 수를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사용자를 사이트를 재방문하도록 하는데 가장 효과적인 콘텐츠가 무엇인지 분석하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 방문 횟수 지표와 고유 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--audio-consumption-template"
>title="모든 디지털 디바이스에 걸쳐 미디어 오디오 소비 트렌드 및 상위 지표를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 사이트에서 오디오 콘텐츠를 어떻게 소비하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 많이 소비되는 콘텐츠가 무엇인지 분석하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 방문 횟수 지표와 고유 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--media-recency-frequency-loyalty"
>title="모든 디지털 디바이스에 걸쳐 미디어 소비 트렌드 및 상위 지표를 확인할 수 있습니다."
>abstract="**이를 통해** 일반 사용자가 사이트를 방문하는 횟수, 사람들이 사이트에 재방문하는 빈도 및 재방문 사이의 일 수를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사용자를 사이트를 재방문하도록 하는데 가장 효과적인 콘텐츠가 무엇인지 분석하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 방문 횟수 지표와 고유 방문자 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--reloadsRankedReport"
>title="다시 로드 중 차원 항목이 있었던 횟수를 확인할 수 있습니다. 방문자가 브라우저를 새로 고치는 것이 다시 로드를 트리거하는 가장 일반적인 방법입니다."
>abstract="**이를 통해** 특정 페이지에서 방문자가 페이지를 다시 로드해야 하는 문제가 발생하는 경우를 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 어떤 페이지에 해결해야 할 문제가 있는지 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 다시 로드 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentPageRankedReport"
>title="방문자가 사이트를 방문할 때마다 소비한 평균 시간을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 일 차원과 방문당 체류 시간(초) 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--entryPageOriginalRankedReport"
>title="사용자가 사이트를 처음 방문했을 때 액세스하는 상위 페이지를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트에 가장 많은 트래픽이 유입되는 페이지를 더 잘 이해하거나 방문자가 사이트에 대해 갖는 첫인상을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사람들이 사이트에서 처음 접하는 초기 경험을 최적화하거나 사이트에 들어갈 때 처음 보는 페이지가 환영하는 분위기이고 사이트의 다른 영역에 대한 필요한 링크를 제공하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 세션 지표를 사용합니다. 또한 막대 시각화와 자유 형식 테이블 시각화도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--singlePageVisitsRankedReport"
>title="단일 고유 페이지로 구성된 방문 횟수를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 단일 페이지 방문 횟수 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--sitePerformanceOverview"
>title="Adobe Experience Manager 사이트의 성과 데이터를 확인할 수 있습니다."
>abstract="**이를 통해** Adobe Experience Manager의 가치 실현을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** Experience Manager 설정을 최적화하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--formsPerformanceOverview"
>title="Adobe Experience Manager 양식의 성과 데이터를 확인할 수 있습니다."
>abstract="**이를 통해** Adobe Experience Manager의 가치 실현을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** Experience Manager 설정을 최적화하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--itp-impact"
>title="ITP(Intelligent Tracking Prevention)가 데이터 수집 및 보고에 미치는 효과를 확인하고 분석할 수 있습니다."
>abstract="**이를 통해** ITP가 부과한 쿠키 제한으로 인해 발생할 수 있는 잠재적인 데이터 손실을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** ITP의 영향을 최소화하도록 분석 설정을 조정하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template_time_spent"
>title="각 방문 기간 동안 방문자가 사이트에서 보낸 평균 시간과 성공 이벤트 전에 사용자가 보낸 평균 시간을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다."
>abstract="**이를 통해** 방문자 참여 수준과 방문자가 구매 등 원하는 작업을 수행하는 데 소요되는 시간을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트 변경이 방문자의 성공 이벤트에 빠르게 도달할 수 있는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 일 차원과 방문당 소요 시간(초) 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-content-consumption"
>title="어떤 웹 콘텐츠가 가장 많이 소비되고 사용자의 관심을 끌었는지 확인할 수 있습니다."
>abstract="**이를 통해** 사람들이 사이트에 처음 들어오는 위치, 사이트에서 사람들이 가장 많이 방문하는 섹션, 사이트에서 사람들을 멀어지게 할 가능성이 가장 높은 페이지를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트에서 가장 중요한 페이지로 이동하는 경로와 사이트에서 사람들을 멀어지게 할 가능성이 높은 페이지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 페이지 차원과 페이지 조회수 지표, 방문 횟수 지표, 고유 방문자 수 지표, 진입률 지표, 바운스 비율 지표, 이탈률 지표, 콘텐츠 속도 지표를 사용합니다. 또한 진입, 종료 및 상위 섹션에 흐름 시각화를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--media-content-consumption"
>title="어떤 미디어 콘텐츠가 가장 많이 소비되고 사용자의 관심을 끌고 있는지 확인할 수 있습니다."
>abstract="**이를 통해** 사람들이 사이트에 처음 들어오는 위치, 사이트에서 사람들이 가장 많이 방문하는 섹션, 사이트에서 사람들을 멀어지게 할 가능성이 가장 높은 페이지를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트에서 가장 중요한 페이지로 이동하는 경로와 사이트에서 사람들을 멀어지게 할 가능성이 높은 페이지를 평가하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 페이지 차원과 페이지 조회수 지표, 방문 횟수 지표, 고유 방문자 수 지표, 진입률 지표, 바운스 비율 지표, 이탈률 지표, 콘텐츠 속도 지표를 사용합니다. 또한 진입, 종료 및 상위 섹션에 흐름 시각화, 가장 일반적인 페이지에 대한 페이지 조회수를 표시하는 Satterplot 시각화, 버킷 시간별 페이지 조회수를 표시하는 막대 시각화, 사이트에서 보낸 평균 시간에 대한 트렌드 보기를 표시하는 선 시각화도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--flowreport"
>title="특정 장소 방문 직후 또는 방문 직전에 사람들이 가장 많이 가는 장소를 확인할 수 있습니다."
>abstract="**이를 통해** 트래픽이 특정 페이지에서 사이트의 다른 부분으로 이동하는 방식을 이해하고 사람들이 특정 페이지에 도달하기 위해 취하는 경로를 이해하는 데 도움이 될 수 있습니다.<br/>**학습한 내용을 바탕으로** 페이지 디자인이나 레이아웃을 최적화하여 어떻게 더 바람직한 페이지(예: 구매 페이지 또는 리뷰 작성 페이지)로 유도할 수 있는지 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 현재 페이지의 정보가 이전 페이지에서 사람들이 원하는 방향이나 액션을 제공할 가능성이 있는지 평가합니다. 또는 이전 페이지로 표시되지 않는 페이지를 현재 페이지로 연결하기 위해 더 눈에 띄는 링크가 필요한지 여부를 평가할 수 있습니다.<br/>이 템플릿은 다음 또는 이전 항목 패널을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--page-summary-report"
>title="속성 전반의 모든 페이지에 대한 주요 정보를 확인할 수 있습니다. 페이지 조회수, 트렌드 선, 흐름 시각화 등을 보여 줍니다."
>abstract="**이를 통해** 사용자가 특정 페이지와 상호 작용하는 방식을 더 잘 이해하는 데 도움이 될 수 있습니다.<br/>**학습한 내용을 바탕으로** 일정 기간 동안 페이지의 성능을 분석하거나 페이지로 트래픽을 유도하는 요인을 더 잘 이해하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 페이지 조회수 지표를 사용합니다. 또한 선 시각화 및 흐름 시각화도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--entryPageRankedReport"
>title="사용자가 사이트를 처음 방문했을 때 액세스하는 상위 페이지를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트에 가장 많은 트래픽이 유입되는 페이지를 더 잘 이해하거나 방문자가 사이트에 대해 갖는 첫인상을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사람들이 사이트에서 처음 접하는 초기 경험을 최적화하거나 사이트에 들어갈 때 처음 보는 페이지가 환영하는 분위기이고 사이트의 다른 영역에 대한 필요한 링크를 제공하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 세션 지표를 사용합니다. 또한 막대 시각화와 자유 형식 테이블 시각화도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--exitPageRankedReport"
>title="사이트를 떠나기 직전에 사람들이 액세스하는 상위 페이지를 확인할 수 있습니다."
>abstract="**이를 통해** 사람들이 사이트에서 어떤 페이지 기피하고 있는지 더 잘 파악할 수 있습니다. <br/>**학습한 내용을 바탕으로** 사람들이 떠나기 전에 경험하는 것을 최적화하기 위해 일반 종료 페이지를 업데이트하거나 사용자가 사이트에 머물도록 유도하는 콘텐츠 또는 링크를 포함하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 세션 지표를 사용합니다. 또한 막대 시각화와 자유 형식 테이블 시각화도 사용합니다."

<!-- markdownlint-enable MD034 -->

다음 템플릿을 사용할 수 있습니다.

| 템플릿 이름 | 이 템플릿 <!-- What do you do with it? What can it help you learn? and What are the potential actions? -->을(를) 사용하는 이유 |
| --- | --- | 
| [!UICONTROL **주요 지표**] | <!--duplicated in Most popular section--> 페이지 조회수, 방문자 수, 고유 방문자 수 지표를 나란히 표시한 보고서를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 이러한 중요한 지표를 비교하여 사이트를 방문한 고유 사용자 수, 페이지 방문 횟수 및 세션 수를 보다 완벽하게 파악할 수 있습니다.</p><p>**학습한 내용에 따라** 주어진 주 또는 월로 사이트를 방문할 때 각 사용자가 본 평균 페이지 수와 해당 연도의 특정 기간 동안 또는 마케팅 캠페인 실행 전후에 변경된 정도를 평가하는 등 여러 가지 작업을 수행할 수 있습니다. </p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md), [페이지 보기 횟수 지표](/help/components/metrics/page-views.md), [방문 횟수 지표](/help/components/metrics/visits.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)을 사용합니다.</p> |
| [!UICONTROL **페이지 보기 수**] | <!--duplicated in Most popular section-->총 페이지 조회수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 사이트의 트래픽이 시간이 지남에 따라 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 사이트 트래픽을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 트래픽을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [페이지 보기 횟수 지표](/help/components/metrics/page-views.md)를 사용합니다.</p> |
| [!UICONTROL **페이지**] | <!--duplicated in Most popular section-->방문 빈도가 가장 높은 페이지와 가장 낮은 페이지를 파악합니다. <p>**이를 통해** 대상자와 대상자가 가장 관심을 갖는 정보의 유형을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라** 페이지 메타데이터를 조정하여 더 적게 본 페이지의 가시성을 향상시키거나 가장 많이 본 페이지의 콘텐츠를 개선하는 등 여러 가지 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [페이지 차원](/help/components/dimensions/page.md) 및 [페이지 보기 횟수 지표](/help/components/metrics/page-views.md)를 사용합니다.</p> |
| [!UICONTROL **방문 횟수**] | <!--duplicated in Most popular section-->총 방문 횟수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 사이트의 트래픽이 시간이 지남에 따라 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 사이트 트래픽을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 트래픽을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [방문 횟수 지표](/help/components/metrics/visits.md)를 사용합니다.</p> |
| [!UICONTROL **방문자 수**] | <!--duplicated in Most popular section-->총 고유 방문자 수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 사이트의 도달 범위와 대상자 수가 시간이 지남에 따라 또는 이전 기간과 비교하여 어떻게 증가하거나 감소하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 최근 시작된 마케팅 캠페인이 캠페인 시작 전후의 고유 방문자 수를 비교하여 새로운 사람들을 사이트로 유치하는 데 성공했는지 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 휴일 기간에 방문하는 사람 수를 전년 대비 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)를 사용합니다.</p> |
| [!UICONTROL **방문당 체류 시간**] | 방문자가 사이트를 방문할 때마다 소비한 평균 시간을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md)과 [방문당 체류 시간(초) 지표](/help/components/metrics/time-spent-per-visit.md)을 사용합니다.</p> |
| [!UICONTROL **이벤트까지 남은 시간**] | 성공 이벤트가 발생하기 전까지 사용자가 소비한 평균 시간을 확인할 수 있습니다. <p>**이를 통해** 방문자가 구매 등 원하는 작업을 수행하는 데 소요되는 시간을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트 변경이 방문자의 성공 이벤트에 빠르게 도달할 수 있는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [이벤트까지 남은 시간](/help/components/dimensions/time-prior-to-event.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)를 사용합니다.</p> |
| [!UICONTROL **사이트 섹션**] | <!--duplicated in Most popular section-->사이트의 최고 인기 항목이나 성과가 가장 높은 섹션을 확인할 수 있습니다. <p>**이렇게 하면** 사이트에서 가장 많이 방문하는 섹션을 더 잘 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 제공하는 제품이나 서비스 중 어느 것이 가장 많은 관심을 불러일으키는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 [사이트 섹션 차원](/help/components/dimensions/site-section.md) 및 [방문 횟수 지표](/help/components/metrics/visits.md)를 사용합니다.</p> |
| [!UICONTROL **실시간**] | 현재 사이트에서 수집 중인 차원 및 지표를 확인할 수 있습니다. <p>**이를 통해** 사이트의 트렌드를 파악할 수 있습니다.</p><p>**학습한 내용에 따라**&#x200B;응답하고 현재 마케팅 콘텐츠와 캠페인의 성능을 적극적으로 관리할 수 있습니다.</p> <p>이 템플릿은 [실시간 보고서](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md)를 사용합니다.</p> |
| [!UICONTROL **웹 콘텐츠 사용량**] | 어떤 웹 콘텐츠가 가장 많이 소비되고 사용자의 관심을 끌었는지 확인할 수 있습니다.<p>**이를 통해** 사람들이 사이트에 처음 들어오는 위치, 사이트에서 사람들이 가장 많이 방문하는 섹션, 사이트에서 사람들을 멀어지게 할 가능성이 가장 높은 페이지를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트에서 가장 중요한 페이지로 이동하는 경로와 사이트에서 사람들을 멀어지게 할 가능성이 높은 페이지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 [페이지 차원](/help/components/dimensions/page.md) 및 [페이지 보기 수 지표](/help/components/metrics/page-views.md), [방문 횟수 지표](/help/components/metrics/visits.md), [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md), [시작 비율 지표](/help/components/metrics/entries.md), [바운스 비율 지표](/help/components/metrics/bounce-rate.md), [종료 비율 지표](/help/components/metrics/exits.md) 및 [콘텐츠 속도 지표](/help/components/metrics/content-velocity.md)를 사용합니다. 시작, 종료 및 상단 섹션에도 [흐름 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)를 사용합니다.</p> |
| [!UICONTROL **미디어 콘텐츠 사용량**] | 어떤 미디어 콘텐츠가 가장 많이 소비되고 사용자의 관심을 끌고 있는지 확인할 수 있습니다.<p>**이를 통해** 사람들이 사이트에 처음 들어오는 위치, 사이트에서 사람들이 가장 많이 방문하는 섹션, 사이트에서 사람들을 멀어지게 할 가능성이 가장 높은 페이지를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트에서 가장 중요한 페이지로 이동하는 경로와 사이트에서 사람들을 멀어지게 할 가능성이 높은 페이지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 [페이지 차원](/help/components/dimensions/page.md) 및 [페이지 보기 수 지표](/help/components/metrics/page-views.md), [방문 횟수 지표](/help/components/metrics/visits.md), [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md), [시작 비율 지표](/help/components/metrics/entries.md), [바운스 비율 지표](/help/components/metrics/bounce-rate.md), [종료 비율 지표](/help/components/metrics/exits.md) 및 [콘텐츠 속도 지표](/help/components/metrics/content-velocity.md)를 사용합니다. 또한 시작, 종료 및 상단 섹션에는 [플로우 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md), 가장 일반적인 페이지에 대한 페이지 보기를 표시하는 [Satterplot 시각화](/help/analyze/analysis-workspace/visualizations/scatterplot.md), 버킷된 시간별로 페이지 보기를 표시하는 [막대 시각화](/help/analyze/analysis-workspace/visualizations/bar.md), 사이트에서 보낸 평균 시간의 트렌드 보기를 표시하는 [선 시각화](/help/analyze/analysis-workspace/visualizations/line.md)를 사용합니다.</p> |
| [!UICONTROL **다음 및 이전 페이지 흐름**] | 특정 장소를 방문하기 전이나 후에 사람들이 가는 가장 일반적인 장소를 봅니다.<p>**이렇게 하면 사용자가 사이트에 처음 들어왔을 때 어디로 이동하는지, 사람들이 가장 많이 방문하는 사이트 섹션과 사이트를 떠나기 전에 방문할 가능성이 가장 높은 페이지를 더 잘 파악할 수 있습니다**.</p><p>**학습한 내용을 바탕으로** 사이트에서 가장 중요한 페이지로 이동하는 경로와 사이트에서 사람들을 멀어지게 할 가능성이 높은 페이지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 [페이지 차원](/help/components/dimensions/page.md) 및 [페이지 보기 수 지표](/help/components/metrics/page-views.md), [방문 횟수 지표](/help/components/metrics/visits.md), [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md), [시작 비율 지표](/help/components/metrics/entries.md), [바운스 비율 지표](/help/components/metrics/bounce-rate.md), [종료 비율 지표](/help/components/metrics/exits.md) 및 [콘텐츠 속도 지표](/help/components/metrics/content-velocity.md)를 사용합니다. 또한 시작, 종료 및 상단 섹션에 대해 [플로우 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md), 가장 일반적인 페이지에 대한 페이지 보기를 표시하는 [산점도 시각화](/help/analyze/analysis-workspace/visualizations/scatterplot.md), 버킷 시간별로 페이지 보기를 표시하는 [막대 시각화](/help/analyze/analysis-workspace/visualizations/bar.md), 사이트에서 보낸 평균 시간의 트렌드 보기를 표시하는 [선 시각화](/help/analyze/analysis-workspace/visualizations/line.md)를 사용합니다.</p> |
| [!UICONTROL **폴아웃**] | 미리 정의된 페이지 시퀀스를 통해 사람들이 어디에서 떠나거나 계속 읽는지 확인할 수 있습니다.<p>**이를 통해** 사용자가 사용자 여정 중 어디에서 이탈하는지 더 잘 이해할 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트의 특정 프로세스(예: 구매 또는 등록 프로세스)를 통한 전환율을 분석하거나 사이트에서 발생하는 이벤트 간의 상관 관계를 분석하는 등 다양한 작업을 수행할 수 있습니다. 예를 들어 개인정보 처리방침을 본 사람 중 실제로 제품을 구매한 사람의 비율을 확인할 수 있습니다. 또한 이 템플릿을 사용하여 동일한 보고서에서 두 개의 서로 다른 세그먼트를 나란히 비교할 수도 있습니다.</p> <p>이 템플릿은 [폴아웃 시각화](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md)를 사용합니다.</p> |
| [!UICONTROL **장치 간 분석**] | 여정의 모든 지점에서 사람들이 사용한 디바이스를 확인할 수 있습니다.<p>**이를 통해** 얼마나 많은 사람들이 브랜드와 상호 작용하는지, 그들이 사용하는 디바이스 유형은 무엇인지와 여러 디바이스를 사용하는 것이 사용자 경험에 어떤 영향을 미치는지 더 잘 이해할 수 있습니다. 예를 들어 사람들이 모바일 디바이스에서 작업을 시작한 다음 나중에 데스크탑 PC로 이동하여 작업을 완료하는 빈도는 얼마나 됩니까? 사용자가 하나의 디바이스에서 다른 디바이스로 이동하는 가장 일반적인 경로는 무엇입니까? 어디에서 중단됩니까? 어디에서 성공합니까? 등의 질문에 대한 답을 구할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 모바일 경험에 대해 사용자 여정의 특정 부분을 최적화하는 등 다양한 작업을 수행할 수 있습니다.</p> <p>이 템플릿은 [흐름 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md), [폴아웃 시각화](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md), [집단 분석](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md), [사람 지표](/help/components/metrics/people.md) 및 [고유 장치 지표](/help/components/metrics/unique-devices.md)를 사용합니다.</p> |
| [!UICONTROL **웹 유지**] | 사이트에서 충성도가 높은 사용자가 누구인지, 그들이 사이트에서 무엇을 하고 있는지 확인할 수 있습니다.<p>**이를 통해** 일반 사용자가 사이트를 방문하는 횟수, 사람들이 사이트에 재방문하는 빈도 및 재방문 사이의 일 수를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사용자를 사이트를 재방문하도록 하는데 가장 효과적인 콘텐츠가 무엇인지 분석하는 등 다양한 작업을 수행할 수 있습니다.<p>이 템플릿은 [방문 횟수 지표](/help/components/metrics/visits.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)을 사용합니다.</p> |
| [!UICONTROL **스트리밍 미디어 사용량**] | 모든 디지털 디바이스에 걸쳐 미디어 오디오 소비 트렌드 및 상위 지표를 확인할 수 있습니다.<p>**이를 통해** 방문자가 사이트에서 오디오 콘텐츠를 어떻게 소비하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 많이 소비되는 콘텐츠가 무엇인지 분석하는 등 다양한 작업을 수행할 수 있습니다.<p>이 템플릿은 [방문 횟수 지표](/help/components/metrics/visits.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)을 사용합니다.</p> |
| [!UICONTROL **미디어 최신성, 빈도, 충성도**] | 모든 디지털 디바이스에 걸쳐 미디어 소비 트렌드 및 상위 지표를 확인할 수 있습니다.<p>**이를 통해** 일반 사용자가 사이트를 방문하는 횟수, 사람들이 사이트에 재방문하는 빈도 및 재방문 사이의 일 수를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사용자를 사이트를 재방문하도록 하는데 가장 효과적인 콘텐츠가 무엇인지 분석하는 등 다양한 작업을 수행할 수 있습니다.<p>이 템플릿은 [방문 횟수 지표](/help/components/metrics/visits.md) 및 [고유 방문자 수 지표](/help/components/metrics/unique-visitors.md)을 사용합니다.</p> |
| **[!UICONTROL 페이지 분석]** > [!UICONTROL **페이지 요약**] | 방문자가 사이트를 방문할 때마다 소비한 평균 시간을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md)과 [방문당 체류 시간(초) 지표](/help/components/metrics/time-spent-per-visit.md)을 사용합니다.</p> |
| **[!UICONTROL 페이지 분석]** > [!UICONTROL **다시 로드**] | 다시 로드 중 차원 항목이 있었던 횟수를 확인할 수 있습니다. 방문자가 브라우저를 새로 고치는 것이 다시 로드를 트리거하는 가장 일반적인 방법입니다. <p>**이를 통해** 특정 페이지에서 방문자가 페이지를 다시 로드해야 하는 문제가 발생하는 경우를 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 어떤 페이지에 해결해야 할 문제가 있는지 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [다시 로드 지표](https://experienceleague.adobe.com/en/docs/analytics/components/metrics/reloads)를 사용합니다.</p> |
| **[!UICONTROL 페이지 분석]** > [!UICONTROL **페이지 체류 시간**] | 방문자가 사이트를 방문할 때마다 소비한 평균 시간을 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md)과 [방문당 체류 시간(초) 지표](/help/components/metrics/time-spent-per-visit.md)을 사용합니다.</p> |
| **[!UICONTROL 시작 및 종료]** > [!UICONTROL **시작 페이지**] | 사람들이 주어진 세션을 위해 사이트를 처음 방문할 때 액세스하는 상위 페이지를 봅니다. <p>**이를 통해** 사이트에 가장 많은 트래픽이 유입되는 페이지를 더 잘 이해하거나 방문자가 사이트에 대해 갖는 첫인상을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사람들이 사이트에서 처음 접하는 초기 경험을 최적화하거나 사이트에 들어갈 때 처음 보는 페이지가 환영하는 분위기이고 사이트의 다른 영역에 대한 필요한 링크를 제공하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 세션 지표를 사용합니다. 또한 막대 시각화와 자유 형식 테이블 시각화도 사용합니다.</p> |
| **[!UICONTROL 시작 및 종료]** > [!UICONTROL **원래 시작 페이지**] | 사용자가 사이트를 처음 방문했을 때 액세스하는 상위 페이지를 확인할 수 있습니다. <p>**이를 통해** 사이트에 가장 많은 트래픽이 유입되는 페이지를 더 잘 이해하거나 방문자가 사이트에 대해 갖는 첫인상을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사람들이 사이트에서 처음 접하는 초기 경험을 최적화하거나 사이트에 들어갈 때 처음 보는 페이지가 환영하는 분위기이고 사이트의 다른 영역에 대한 필요한 링크를 제공하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 세션 지표를 사용합니다. 또한 막대 시각화와 자유 형식 테이블 시각화도 사용합니다.</p> |
| **[!UICONTROL 시작 및 종료]** > [!UICONTROL **단일 페이지 방문**] | 단일 고유 페이지로 구성된 방문 횟수를 확인할 수 있습니다. <p>**이를 통해** 방문자 참여 수준과 방문자가 사이트에 체류한 시간을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트를 변경하면 방문자가 사이트에 체류하는 시간이 늘어나는지를 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 [단일 페이지 방문 횟수 차원](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/single-page-visits)을 사용합니다.</p> |
| **[!UICONTROL 시작 및 종료]** > [!UICONTROL **종료 페이지**] | 사이트를 떠나기 직전에 사람들이 액세스하는 상위 페이지를 확인할 수 있습니다.<p>**이렇게 하면**&#x200B;사람들이 사이트를 떠나게 하는 페이지를 더 잘 이해할 수 있습니다. </p><p>**학습한 내용을 바탕으로** 사람들이 떠나기 전에 경험하는 것을 최적화하기 위해 일반 종료 페이지를 업데이트하거나 사용자가 사이트에 머물도록 유도하는 콘텐츠 또는 링크를 포함하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 세션 지표를 사용합니다. 또한 막대 시각화와 자유 형식 테이블 시각화도 사용합니다.</p> |
| [!UICONTROL **Adobe Experience Manager**] > [!UICONTROL **사이트 성능 개요**] > [!UICONTROL **AEM 사이트 성능**] | Adobe Experience Manager 사이트의 성과 데이터를 확인할 수 있습니다.  <p>**이를 통해** Adobe Experience Manager의 가치 실현을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** Experience Manager 설정을 최적화하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| [!UICONTROL **Adobe Experience Manager**] > [!UICONTROL **양식 성능 개요**] > [!UICONTROL **AEM 양식 성능**] | Adobe Experience Manager 양식의 성과 데이터를 확인할 수 있습니다.  <p>**이를 통해** Adobe Experience Manager의 가치 실현을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** Experience Manager 설정을 최적화하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| [!UICONTROL **ITP 영향**] | ITP(Intelligent Tracking Prevention)가 데이터 수집 및 보고에 미치는 효과를 확인하고 분석할 수 있습니다. <p>**이를 통해** ITP가 부과한 쿠키 제한으로 인해 발생할 수 있는 잠재적인 데이터 손실을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** ITP의 영향을 최소화하도록 분석 설정을 조정하는 등 다양한 작업을 수행할 수 있습니다.</p> |

### 전환 {#web-conversion}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--categoryRankedReport"
>title="사이트의 각 제품 카테고리와 연계된 방문 횟수를 확인할 수 있습니다. 이 기능은 제품 변수를 사용하고 제품 카테고리에 대한 지표를 보려는 구현에 유용합니다. 사이트에 제품이 없을 경우 이 템플릿을 채우는 차원을 의도적으로 비워 둘 수 있습니다."
>abstract="**이를 통해** 가장 많이 판매되는 제품 또는 가장 많이 본 제품을 파악할 수 있습니다. &lt;/br/>**학습한 내용을 바탕으로** 특정 제품의 마케팅 캠페인 효과를 측정하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 카테고리 차원과 방문 횟수 지표를 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--commerce-and-marketing-management"
>title="판매 개선에 도움이 되는 상거래 활동에 대한 소매점을 위해 미리 제작된 인사이트를 확인할 수 있습니다. 이는 Adobe Commerce 사용자를 대상으로 하지만 모든 온라인 소매점에서 활용할 수 있습니다."
>abstract="**이를 통해** 상거래 활동이 매출 수치에 어떻게 기여하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 많은 ROI를 얻는 활동에 대한 예산을 조정하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--productConversionReport"
>title="장바구니, 체크아웃, 주문을 표시하는 단계 시각화에서 제품 전환을 확인할 수 있습니다. 전환율, 매출 평균, 단위 평균, 주문 평균을 확인할 수도 있습니다."
>abstract="**이를 통해** 사람들이 전환 프로세스를 어떻게 진행하고 드롭 오프하는지 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 웹 사이트를 개선하여 체크아웃 프로세스를 더욱 원활하게 진행하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--retail-products-template"
>title="어떤 제품이 가장 성과가 좋은지 확인할 수 있습니다."
>abstract="**이를 통해** 어떤 제품이 가장 성공적인지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 성공적인 제품에 대한 자금 지원을 늘리고 덜 성공적인 제품에 대한 자금 지원을 줄이는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 제품 조회수, 장바구니 추가, 주문, 매출 및 판매량 지표를 사용합니다. 또한 제품 차원도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartConversionReport"
>title="장바구니에 제품 추가, 장바구니 보기, 장바구니에서 제품 제거, 체크아웃 등 주요 체크아웃 이벤트를 수행한 횟수를 확인할 수 있습니다."
>abstract="**이를 통해** 체크아웃 프로세스의 어떤 부분이 전환으로 이어지는지, 어떤 부분이 장바구니 포기 가능성이 높은지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 체크아웃 프로세스의 특정 단계에서 마찰을 줄이는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 다음을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartsOvertimeReport"
>title="장바구니에 제품을 추가한 사람의 수를 확인할 수 있습니다."
>abstract="**이를 통해** 장바구니에 추가되는 전체 제품 수 대비 장바구니에 제품을 추가하는 사람의 수를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 제품 페이지의 효과를 측정하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 장바구니 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartViewsOvertimeReport"
>title="사람들이 장바구니를 조회한 횟수를 확인할 수 있습니다."
>abstract="**이를 통해** 장바구니 포기율을 낮추기 위해 체크아웃 경험을 더 잘 이해하거나 다양한 제품 간의 장바구니 추가와 체크아웃 사이의 시간을 분석할 수 있습니다.<br/>**학습한 내용을 바탕으로** 장바구니에 가장 오래 보관되어 포기 위험이 가장 큰 제품에 대한 프로모션을 제공하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 장바구니 조회수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartAdditionsOvertimeReport"
>title="사람들이 장바구니에 제품을 추가한 횟수를 확인할 수 있습니다."
>abstract="**이를 통해** 제품에 대한 고객의 관심이 장바구니에 추가할 만큼 높은 전환 단계 부분을 더 잘 이해하는 데 도움이 될 수 있습니다.<br/>**학습한 내용을 바탕으로** 모든 고객을 위한 제품 추천 개선과 같은 다양한 작업을 수행할 수 있습니다. 이 작업은 동일한 장바구니에 자주 추가되는 제품을 분석하고 이미 장바구니에 있는 품목을 기준으로 관련 제품을 제안함으로써 이루어질 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartRemovalsOvertimeReport"
>title="사람들이 장바구니에서 제품을 제거한 횟수를 확인할 수 있습니다."
>abstract="**이를 통해** 고객이 더 이상 제품에 관심이 없는 전환 단계 부분을 더 잘 이해하거나 체크아웃 프로세스에서 문제가 발생할 수 있는 부분을 이해하는 데 도움이 될 수 있습니다.<br/>**학습한 내용을 바탕으로** 복잡한 사용자 경험 등 체크아웃 프로세스에 존재할 수 있는 잠재적 장벽을 제거하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 장바구니 제거 수 지표를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--purchaseConversionReport"
>title="세션, 장바구니, 주문을 표시하는 단계 시각화에서 구매 전환을 확인할 수 있습니다. 전환율, 매출 평균, 단위 평균, 주문 평균을 확인할 수도 있습니다."
>abstract="**이를 통해** 사람들이 전환 프로세스를 어떻게 진행하고 드롭 오프하는지 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 웹 사이트를 개선하여 체크아웃 프로세스를 더욱 원활하게 진행하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

다음 템플릿을 사용할 수 있습니다.

| 템플릿 이름 | 이 템플릿 <!-- What do you do with it? What can it help you learn? and What are the potential actions? -->을(를) 사용하는 이유 |
| --- | --- | 
| [!UICONTROL **제품 전환 단계**] | 장바구니, 체크아웃, 주문을 표시하는 단계 시각화에서 제품 전환을 확인할 수 있습니다. 전환율, 매출 평균, 단위 평균, 주문 평균을 확인할 수도 있습니다.<p>**이를 통해** 사람들이 전환 프로세스를 어떻게 진행하고 드롭 오프하는지 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 웹 사이트를 개선하여 체크아웃 프로세스를 더욱 원활하게 진행하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| **제품** | 최상위 판매자나 가장 많이 본 항목과 같은 주요 지표를 유도하는 제품을 봅니다. <p>**이를 통해** 어떤 제품이 가장 성공적인지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 성공적인 제품에 대한 자금 지원을 늘리고 덜 성공적인 제품에 대한 자금 지원을 줄이는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 주문 지표와 제품 차원을 사용합니다. |
| **제품 성능** | 어떤 제품이 가장 성과가 좋은지 확인할 수 있습니다.<p>**이를 통해** 어떤 제품이 가장 성공적인지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 성공적인 제품에 대한 자금 지원을 늘리고 덜 성공적인 제품에 대한 자금 지원을 줄이는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 제품 보기, 장바구니 추가, 주문, 매출 및 판매량 지표를 사용합니다. 또한 제품 차원도 사용합니다. |
| **범주** | 사이트의 각 제품 카테고리와 연계된 방문 횟수를 확인할 수 있습니다. 이 기능은 제품 변수를 사용하고 제품 카테고리에 대한 지표를 보려는 구현에 유용합니다. 사이트에 제품이 없을 경우 이 템플릿을 채우는 차원을 의도적으로 비워 둘 수 있습니다.<p>**가장 많이 팔린 제품이나 가장 많이 본 제품을 더 잘 이해하는 데 도움이 됩니다**. </p><p>**학습한 내용에 따라, 특정 제품에 대한 마케팅 캠페인의 효과를 측정하는 것과 같이**&#x200B;할 수 있습니다.</p><p>이 템플릿은 카테고리 차원 및 방문 횟수 지표를 사용합니다. |
| **장바구니 전환 단계** | 장바구니에 제품 추가, 장바구니 보기, 장바구니에서 제품 제거, 체크아웃 등 주요 체크아웃 이벤트를 수행한 횟수를 확인할 수 있습니다. <p>**이를 통해** 체크아웃 프로세스의 어떤 부분이 전환으로 이어지는지, 어떤 부분이 장바구니 포기 가능성이 높은지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 체크아웃 프로세스의 특정 단계에서 마찰을 줄이는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 |
| **장바구니** | 장바구니에 제품을 추가한 사람의 수를 확인할 수 있습니다.<p>**이를 통해** 장바구니에 추가되는 전체 제품 수 대비 장바구니에 제품을 추가하는 사람의 수를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 제품 페이지의 효과를 측정하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿에서는 장바구니 지표를 사용합니다. |
| **장바구니 보기** | 사람들이 장바구니를 조회한 횟수를 확인할 수 있습니다. <p>**이를 통해** 장바구니 포기율을 낮추기 위해 체크아웃 경험을 더 잘 이해하거나 다양한 제품 간의 장바구니 추가와 체크아웃 사이의 시간을 분석할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 장바구니에 가장 오래 보관되어 포기 위험이 가장 큰 제품에 대한 프로모션을 제공하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 장바구니 보기 수 지표를 사용합니다. |
| **장바구니 추가** | 사람들이 장바구니에 제품을 추가한 횟수를 확인할 수 있습니다. <p>**이를 통해** 제품에 대한 고객의 관심이 장바구니에 추가할 만큼 높은 전환 단계 부분을 더 잘 이해하는 데 도움이 될 수 있습니다.</p><p>**학습한 내용을 바탕으로** 모든 고객을 위한 제품 추천 개선과 같은 다양한 작업을 수행할 수 있습니다. 이 작업은 동일한 장바구니에 자주 추가되는 제품을 분석하고 이미 장바구니에 있는 품목을 기준으로 관련 제품을 제안함으로써 이루어질 수 있습니다. |
| **장바구니 제거** | 사람들이 장바구니에서 제품을 제거한 횟수를 확인할 수 있습니다.<p>**이를 통해** 고객이 더 이상 제품에 관심이 없는 전환 단계 부분을 더 잘 이해하거나 체크아웃 프로세스에서 문제가 발생할 수 있는 부분을 이해하는 데 도움이 될 수 있습니다.</p><p>**학습한 내용을 바탕으로** 복잡한 사용자 경험 등 체크아웃 프로세스에 존재할 수 있는 잠재적 장벽을 제거하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 장바구니 제거 수 지표를 사용합니다. |
| **구매 전환 단계** | 세션, 장바구니, 주문을 표시하는 단계 시각화에서 구매 전환을 확인할 수 있습니다. 전환율, 매출 평균, 단위 평균, 주문 평균을 확인할 수도 있습니다.<p>**이를 통해** 사람들이 전환 프로세스를 어떻게 진행하고 드롭 오프하는지 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 웹 사이트를 개선하여 체크아웃 프로세스를 더욱 원활하게 진행하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| **매출** | <!--duplicated in Most popular section-->모든 주문 내에서 구매된 제품의 금액을 확인합니다.<p>**매출 지표를 임의의 차원과 결합하여 매출에 기여한 차원 항목을 더 잘 이해하는 데**&#x200B;도움이 될 수 있습니다. 예를 들어 매출에 기여한 상위 캠페인 (추적 코드 차원 사용)을 볼 수 있습니다. </p><p>**학습한 내용에 따라** 예상한 매출 목표를 충족하지 않는 캠페인 조정과 같은 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 매출 지표를 사용합니다. |
| **주문** | <!--duplicated in Most popular section-->사이트에서 수행된 총 구매 이벤트 수를 봅니다. <p>**이렇게 하면 Orders 지표를 임의의 차원과 결합하여 주문에 기여한 차원 항목을 더 잘 이해할 수 있습니다**. 예를 들어 구매에 기여한 상위 캠페인(추적 코드 차원 사용)을 볼 수 있습니다.</p><p>**학습한 내용에 따라** 예상한 구매 목표를 충족하지 않는 캠페인 조정과 같은 여러 작업을 수행할 수 있습니다. </p><p>이 템플릿은 주문 지표를 사용합니다. |
| [!UICONTROL **판매량**] | 모든 주문 내에서 구매된 상품의 총 개수를 확인할 수 있습니다. 데이터는 일정 기간 동안 표시되며 이전 기간과 비교됩니다. <p>**이를 통해** 시간이 지남에 따라 판매량이 어떻게 증가하거나 감소하는지 더 잘 이해하는 데 도움이 될 수 있습니다. 세그먼트를 적용하여 가장 많은 상품을 구매하는 고객 또는 지역과 시간 경과에 따른 판매량 트렌딩을 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 캠페인이 시작되기 전과 후의 판매량을 비교하여 최근에 시작된 마케팅 캠페인의 효과를 평가하는 등 다양한 작업을 수행할 수 있습니다. 또는 전년 대비 휴일 기간 동안의 판매량을 비교할 수도 있습니다.</p><p>이 템플릿은 [일 차원](/help/components/dimensions/day.md) 및 [단위 지표](/help/components/metrics/units.md)을 사용합니다.</p> |
| [!UICONTROL **Magento: 마케팅 및 상거래**] | 판매 개선에 도움이 되는 상거래 활동에 대한 소매점을 위해 미리 제작된 인사이트를 확인할 수 있습니다. 이는 Adobe Commerce 사용자를 대상으로 하지만 모든 온라인 소매점에서 활용할 수 있습니다. <p>**이를 통해** 상거래 활동이 매출 수치에 어떻게 기여하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 많은 ROI를 얻는 활동에 대한 예산을 조정하는 등 다양한 작업을 수행할 수 있습니다.</p> |

### 대상자 {#web-audience}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--people"
>title="내 브랜드와 상호작용하는 사람의 수를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트의 사용 추세를 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트의 새 방문자를 생성하는 데 있어 최근 마케팅 활동의 효과를 측정하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--bots"
>title="사이트의 봇 트래픽과 관련된 페이지 조회수와 추세를 확인할 수 있습니다."
>abstract="**이를 통해** 구성된 봇 규칙에 따라 보고서에서 필터링되고 있는 봇 트래픽 양을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 봇 활동을 계속 모니터링하여 새 패턴을 식별하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstvsrepeatvisitors"
>title="처음 방문자 수와 재방문자 수를 비교해 보십시오."
>abstract="**이를 통해** 고객 충성도를 유지하는 데 있어 사이트의 효과를 이해하거나 새로운 고객을 확보하는 속도를 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 첫 방문자에게 추후 구매를 장려하는 인센티브를 제공하여 다시 방문하도록 유도하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--personid"
>title="다양한 채널에서 개별 사용자 행동을 확인할 수 있습니다."
>abstract="**이를 통해** 여러 터치포인트에서 전체 고객 여정과 상호작용을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사용자 환경 설정 타기팅에 가장 적합한 마케팅 활동을 개인화하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeZoneRankedReport"
>title="방문자가 사이트에 액세스하는 상위 시간대를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 어느 시간대에 활동하고 있는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 적은 사용자에게 영향을 미치는 시간대로 사이트 유지 관리를 조정하는 등 여러 가지 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--location"
>title="맵 시각화를 통해 방문자 위치 개요를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트 방문자의 위치를 파악할 수 있습니다. <br/>**학습한 내용을 바탕으로** 가장 많은 관심과 기회가 표시된 위치에서 마케팅 리소스를 집중하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--domainRankedReport"
>title="방문자가 사이트에 액세스하는 상위 도메인을 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 어떤 조직에 속해 있는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 큰 고객을 겨냥한 콘텐츠를 제작하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--topLevelDomainRankedReport"
>title="방문자가 사이트에 액세스하는 상위 도메인을 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 어떤 조직에 속해 있는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 큰 고객을 겨냥한 콘텐츠를 제작하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserWidthRankedReport"
>title="사람들이 사이트에 액세스하는 데 사용하는 상위 브라우저 폭을 확인할 수 있습니다."
>abstract="**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 일반적인 브라우저 폭을 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.<br/>이 템플릿은 브라우저 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserHeightRankedReport"
>title="사람들이 사이트에 액세스하는 데 사용하는 상위 브라우저 높이를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 일반적인 브라우저 높이를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.<br/>이 템플릿은 브라우저 차원을 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 운영 체제와 버전을 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 가장 많이 사용하는 운영 체제와 버전을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 상위 운영 체제 및 버전을 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemTypeRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 운영 체제를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자가 가장 많이 사용하는 운영 체제를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 상위 운영 체제를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--returnFrequencyRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다."
>abstract="**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 이동통신사 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--returnVisitorsOvertimeReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다."
>abstract="**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 이동통신사 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--visitNumberRankedReport"
>title="방문자 한 명이 사이트를 몇 번 방문했는지 확인할 수 있습니다."
>abstract="**이렇게 하면** 방문자가 사이트를 재방문할 때의 참여도를 더 잘 이해할 수 있습니다. 이는 프로젝트 날짜 범위와 상관없이 방문자의 라이프타임에 적용됩니다.<br/>**학습한 내용을 바탕으로** 자주 방문하는 고객을 대상으로 마케팅 활동을 조정하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 방문 횟수 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--customerLoyaltyRankedReport"
>title="이전 구매 횟수가 0회, 이전 구매 횟수가 1회, 이전 구매 횟수가 2회 또는 이전 구매 횟수가 3회 이상인 사이트 방문자 수를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트가 구매 행동에 어떤 영향을 미치는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 재방문하여 구매하는 방문자에 초점을 맞추는 등 다양한 작업을 수행하여 신규 방문자에게도 비슷한 행동을 장려할 수 있습니다.<br/>이 템플릿은 고객 충성도 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysBeforeFirstPurchaseRankedReport"
>title="방문자가 사이트에 처음 방문한 후 구매를 수행하는 시점까지 경과된 시간(일)을 확인할 수 있습니다. 예를 들어 방문자가 처음 방문한 다음 하루 후에 구매한다면 그 이후의 모든 방문 또는 이벤트는 1일 차원 항목에 속합니다."
>abstract="**이를 통해** 방문자가 구매하는 데 걸리는 시간을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트를 업데이트하여 더 빠른 고객 확보를 촉진하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 첫 구매까지 소요된 일 수 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysSinceLastPurchaseRankedReport"
>title="방문자의 현재 히트와 해당 시점의 가장 최근 구매 사이에 경과된 시간을 확인할 수 있습니다."
>abstract="**이렇게 하면** 방문자가 사용자의 사이트에서 구매를 한 후 취하는 행동을 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트를 업데이트하여 후속 구매를 장려하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 마지막 구매 이후 일수 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenSizeRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 상위 모바일 화면 크기를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 일반적인 모바일 화면 크기를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenHeightRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 상위 모바일 화면 높이를 확인할 수 있습니다."
>abstract="**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 일반적인 모바일 화면 높이를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenWidthRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 상위 모바일 화면 폭을 확인할 수 있습니다."
>abstract="**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 일반적인 모바일 화면 폭을 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--countryGeoReport"
>title="사이트를 방문하는 사람들의 출신 국가를 확인할 수 있습니다."
>abstract="**이를 통해** 어느 국가에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 데이터를 사용하여 해당 국가에서 마케팅 활동에 집중하거나 기본 언어가 다른 국가에서 사이트 경험이 최적화되도록 하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 국가 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--stateGeoReport"
>title="사이트를 방문하는 사람들이 (미국) 어느 주에서 왔는지 확인할 수 있습니다. 이 차원은 미국에만 해당된다는 점을 제외하면 지리적 지역 템플릿과 유사합니다."
>abstract="**이를 통해** 미국 어디에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 데이터를 사용하여 해당 주에서 마케팅 활동에 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 미국 주 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--regionGeoReport"
>title="사이트를 방문한 사람들이 어느 지리적 지역에서 왔는지 확인할 수 있습니다. 한 지역은 국가보다는 작지만 도시보다는 큰 지리적 영역입니다. 일부 국가의 경우 지역이 주, 도 또는 현입니다. 기타 영역에서는 자치국, 부서 또는 대도시권입니다. "
>abstract="**이를 통해** 어느 지역에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 데이터를 사용하여 해당 지역에서 마케팅 활동에 집중하거나 기본 언어가 다른 지역에서 사이트 경험이 최적화되도록 하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 ID(변수/지리국가) 및 지역 차원을 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cityGeoReport"
>title="사이트를 방문하는 사람들의 출신 도시를 확인할 수 있습니다."
>abstract="**이를 통해** 어느 도시에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 데이터를 사용하여 해당 도시에서 마케팅 활동에 집중하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 도시 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--dmaGeoReport"
>title="사이트 방문자가 미국 내 지정 마케팅 지역(DMA) 중 어디에서 가장 많이 방문했는지 확인할 수 있습니다."
>abstract="**이를 통해** 어느 지역에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 데이터를 사용하여 가장 성공적인 지역에서 마케팅 활동에 집중하는 등 다양한 작업을 수행할 수 있습니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--languageRankedReport"
>title="방문자가 콘텐츠를 보기 위해 선호하는 상위 언어를 확인할 수 있습니다."
>abstract="**이를 통해** 가장 자주 선호하는 방문자 언어를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 인기 있는 언어에 대한 집중 현지화 노력이나 마케팅 활동과 같은 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 언어 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-technology-template"
>title="운영 체제, 브라우저, 디바이스 등 사람들이 사이트에 액세스하는 데 사용하는 기술과 관련된 정보를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트에 액세스할 때 가장 자주 사용되는 기술을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사용 중인 기술에 맞게 사이트를 최적화하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--browserRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 상위 브라우저의 이름과 버전을 확인할 수 없습니다."
>abstract="**이를 통해** 방문자가 가장 많이 사용하는 브라우저를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 상위 브라우저를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.<br/>이 템플릿은 브라우저 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--browserTypeRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 상위 브라우저를 만든 조직의 이름을 확인할 수 있습니다. 이는 동일한 브라우저의 다른 버전을 별도의 차원 항목으로 나열하지 않는다는 점에서 브라우저 템플릿과 다릅니다."
>abstract="**이를 통해** 방문자가 가장 많이 사용하는 브라우저를 더 잘 이해할 수 있습니다. <br/>**학습한 내용을 바탕으로** 상위 브라우저를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다. <br/>이 템플릿은 브라우저 유형 차원을 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileappscreens"
>title="모바일 앱에서 각 화면과 관련된 이벤트, 세션 및 참여자 수를 확인할 수 있습니다."
>abstract="**이를 통해** 사이트에서 방문 빈도가 높은 화면을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 방문 빈도가 높은 화면의 콘텐츠를 개선하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileappactions"
>title="모바일 앱에서 사람들이 수행하는 작업을 확인할 수 있습니다."
>abstract="**이를 통해** 사람들이 앱을 어떻게 사용하고 있는지 앱을 통해 어떤 가치를 얻을 수 있는지 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 방문 빈도가 높은 페이지를 보완하는 기능을 개발하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!--CJA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-lifecycle-metrics-app-usage-template"
>title="앱에서 사용자, 시작 및 첫 번째 시작의 수와 평균 세션 길이를 확인합니다."
>abstract="**이를 통해** 앱의 사용량을 파악할 수 있습니다. <br/>**학습한 내용을 바탕으로** 사용량에 맞게 확장할 수 있도록 앱 성능 개선 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-journeys"
>title="모바일 앱의 눈에 띄는 사용 패턴을 확인합니다."
>abstract="**이를 통해** 사람들이 앱을 어떻게 사용하고 있는지 파악할 수 있습니다. <br/>**학습한 내용을 바탕으로** 가장 일반적인 워크플로를 타기팅하기 위해 사람들이 한 화면에서 다른 화면으로 이동하는 방법을 개선하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-key-metrics"
>title="가장 일반적인 모바일 앱 지표를 확인합니다."
>abstract="**이를 통해** 모바일 앱의 기본 성능을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 앱의 전반적인 상태 및 성능을 평가하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-messaging"
>title="인앱 메시지와 앱의 푸시 메시지의 실질 데이터를 확인합니다."
>abstract="**이를 통해** 사람들이 인앱 메시지 기능을 어떻게 사용하고 있는지, 푸시 알림이 얼마나 효율적으로 앱으로 트래픽을 유도하고 있는지 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 인앱 메시지 푸시 알림 경험을 개선하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-performance-template"
>title="앱의 성능과 사용자 문제가 발생하고 있는 위치를 확인합니다."
>abstract="**이를 통해** 속도나 성능 저하 등 앱 사용자가 직면하는 문제를 파악할 수 있습니다. <br/>**학습한 내용을 바탕으로** 기존 문제를 해결하거나 문제가 발생하기 이전에 앱 성능을 개선하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-retention"
>title="충성도가 가장 높은 앱 사용자가 누구인지, 앱에서 어떤 작업을 하는지 확인합니다."
>abstract="**이를 통해** 충성도가 가장 높은 사용자가 앱을 어떻게 사용하고 있는지 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 충성도가 가장 높은 사용자가 사용하는 기능에 대한 마케팅 활동을 개선하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

다음 템플릿을 사용할 수 있습니다.

| 템플릿 이름 | 이 템플릿 <!-- What do you do with it? What can it help you learn? and What are the potential actions? -->을(를) 사용하는 이유 |
| --- | --- | 
| [!UICONTROL **사람 지표**] | 내 브랜드와 상호작용하는 사람의 수를 확인할 수 있습니다. <p>**이를 통해** 사이트의 사용 추세를 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트의 새 방문자를 생성하는 데 있어 최근 마케팅 활동의 효과를 측정하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| **방문자 프로필** > **위치 개요** | 맵 시각화를 통해 방문자 위치 개요를 확인할 수 있습니다.<p>**이를 통해**&#x200B;사이트를 방문하는 방문자의 위치를 더 잘 파악할 수 있습니다. </p><p>**학습한 내용을 바탕으로** 가장 많은 관심과 기회가 표시된 위치에서 마케팅 리소스를 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |
| **방문자 프로필** > **지역 세분화** > **지역 국가** | 사이트를 방문하는 사람들의 출신 국가를 확인할 수 있습니다.<p>**이를 통해** 어느 국가에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 데이터를 사용하여 해당 국가에서 마케팅 활동에 집중하거나 기본 언어가 다른 국가에서 사이트 경험이 최적화되도록 하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿에서는 국가 차원을 사용합니다. </p> |
| **방문자 프로필** > **지역 세분화** > **미국 지역** | 사이트를 방문하는 사람들이 (미국) 어느 주에서 왔는지 확인할 수 있습니다. 이 차원은 미국에만 해당된다는 점을 제외하면 지리적 지역 템플릿과 유사합니다.<p>**이를 통해** 미국 어디에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 데이터를 사용하여 해당 주에서 마케팅 활동에 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 미국 주 차원을 사용합니다. </p> |
| **방문자 프로필** > **지역 세분화** > **지역** | 사이트를 방문한 사람들이 어느 지리적 지역에서 왔는지 확인할 수 있습니다. 한 지역은 국가보다는 작지만 도시보다는 큰 지리적 영역입니다. 일부 국가의 경우 지역이 주, 도 또는 현입니다. 기타 영역에서는 자치국, 부서 또는 대도시권입니다. <p>**이를 통해** 어느 지역에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라 데이터를 사용하여 해당 지역의 마케팅 활동에 주력하거나 기본 언어가 다른 지역에서 사이트 경험이 최적인지 확인하는 등 여러 가지 작업을 수행할 수 있습니다**. </p><p>이 템플릿은 ID(변수/지역) 및 지역 차원을 사용합니다. </p> |
| **방문자 프로필** > **지역 세분화** > **지역 도시** | 사이트를 방문하는 사람들의 출신 도시를 확인할 수 있습니다. <p>**이를 통해** 어느 도시에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라 데이터를 사용하여 해당 도시에서의 마케팅 활동에 집중하는 등 여러 가지 작업을 수행할 수 있습니다**. </p><p>이 템플릿은 도시 차원을 사용합니다. </p> |
| **방문자 프로필** > **지역 세분화** > **지역 US DMA** | 사이트 방문자가 미국 내 지정 마케팅 지역(DMA) 중 어디에서 가장 많이 방문했는지 확인할 수 있습니다.<p>**이를 통해** 어느 지역에서 가장 많이 사이트에 방문하는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 데이터를 사용하여 가장 성공적인 지역에서 마케팅 활동에 집중하는 등 다양한 작업을 수행할 수 있습니다. </p><!-- This template uses the --> |
| **방문자 프로필** > **언어** | 방문자가 콘텐츠를 보기 위해 선호하는 상위 언어를 확인할 수 있습니다. <p>**이를 통해** 가장 자주 선호하는 방문자 언어를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 인기 있는 언어에 대한 집중 현지화 노력이나 마케팅 활동과 같은 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 언어 차원을 사용합니다.</p> |
| **방문자 프로필** > **시간대** | 방문자가 사이트에 액세스하는 상위 시간대를 확인할 수 있습니다. <p>**이를 통해** 방문자가 어느 시간대에 활동하고 있는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 적은 사용자에게 영향을 미치는 시간대로 사이트 유지 관리를 조정하는 등 여러 가지 작업을 수행할 수 있습니다.</p> |
| **방문자 프로필** > **도메인** | 방문자가 사이트에 액세스하는 상위 도메인을 확인할 수 있습니다. <p>**이를 통해** 방문자가 어떤 조직에 속해 있는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 큰 고객을 겨냥한 콘텐츠를 제작하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| **방문자 프로필** > **최상위 도메인** | 사이트에 액세스하는 방문자의 최상위 도메인을 확인합니다. <p>**이를 통해** 방문자가 어떤 조직에 속해 있는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 큰 고객을 겨냥한 콘텐츠를 제작하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| **방문자 프로필** > **기술** > **기술 개요** | 운영 체제, 브라우저 및 장치와 같이 사람들이 사이트에 액세스하는 데 사용하는 기술과 관련된 정보를 봅니다. <p>**이를 통해** 사이트에 액세스할 때 가장 자주 사용되는 기술을 파악할 수 있습니다.</p><p>**학습한 내용에 따라**&#x200B;사이트에서 사용되는 기술을 최적화하는 등 여러 가지 작업을 수행할 수 있습니다.</p> |
| **방문자 프로필** > **기술** > **브라우저** | 사용자가 사이트에 액세스하는 데 사용하는 상위 브라우저의 이름과 버전을 확인할 수 없습니다.<p>**이를 통해** 방문자가 가장 많이 사용하는 브라우저를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 상위 브라우저를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p><p>이 템플릿은 브라우저 차원을 사용합니다. </p> |
| **방문자 프로필** > **기술** > **브라우저 유형** | 사용자가 사이트에 액세스하는 데 사용하는 상위 브라우저를 만든 조직의 이름을 확인할 수 있습니다. 이는 동일한 브라우저의 다른 버전을 별도의 차원 항목으로 나열하지 않는다는 점에서 브라우저 템플릿과 다릅니다.<p>**방문자가 사용하는 가장 일반적인 브라우저를 더 잘 이해하는 데 도움이 됩니다**</p><p>**학습한 내용을 바탕으로** 상위 브라우저를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다. </p><p>이 템플릿은 브라우저 유형 차원을 사용합니다. </p> |
| **방문자 프로필** > **기술** > **브라우저 너비** | 사람들이 사이트에 액세스하는 데 사용하는 상위 브라우저 폭을 확인할 수 있습니다.<p>**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 브라우저 폭을 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p><p>이 템플릿은 브라우저 차원을 사용합니다. </p> |
| **방문자 프로필** > **기술** > **브라우저 높이** | 사람들이 사이트에 액세스하는 데 사용하는 상위 브라우저 높이를 봅니다.<p>**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 브라우저 높이를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p><p>이 템플릿은 브라우저 차원을 사용합니다. </p> |
| **방문자 프로필** > **기술** > **운영 체제** | 사용자가 사이트에 액세스하는 데 사용하는 운영 체제와 버전을 확인할 수 있습니다.<p>**이를 통해** 방문자가 가장 많이 사용하는 운영 체제와 버전을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 상위 운영 체제 및 버전을 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p> |
| **방문자 프로필** > **기술** > **운영 체제 유형** | 사용자가 사이트에 액세스하는 데 사용하는 운영 체제를 확인할 수 있습니다.<p>**이를 통해** 방문자가 가장 많이 사용하는 운영 체제를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 상위 운영 체제를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p> |
| **방문자 프로필** > **기술** > [!UICONTROL **이동통신사**] | 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 이동통신사 차원을 사용합니다.</p> |
| **방문자 유지** > **반환 주기** | 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 이동통신사 차원을 사용합니다.</p> |
| **방문자 유지** > **재방문** | 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 이동통신사 차원을 사용합니다.</p> |
| **방문자 유지** > **방문 횟수** | 방문자 한 명이 사이트를 몇 번 방문했는지 확인할 수 있습니다.<p>**이렇게 하면** 방문자가 사이트를 재방문할 때의 참여도를 더 잘 이해할 수 있습니다. 이는 프로젝트 날짜 범위와 상관없이 방문자의 라이프타임에 적용됩니다.</p><p>**학습한 내용을 바탕으로** 자주 방문하는 고객을 대상으로 마케팅 활동을 조정하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 방문 횟수 차원을 사용합니다.</p> |
| **방문자 유지** > **판매 주기** > **고객 충성도** | 이전 구매 횟수가 0회, 이전 구매 횟수가 1회, 이전 구매 횟수가 2회 또는 이전 구매 횟수가 3회 이상인 사이트 방문자 수를 확인할 수 있습니다. <p>**이를 통해** 사이트가 구매 행동에 어떤 영향을 미치는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 재방문하여 구매하는 방문자에 초점을 맞추는 등 다양한 작업을 수행하여 신규 방문자에게도 비슷한 행동을 장려할 수 있습니다.</p><p>이 템플릿은 고객 충성도 차원을 사용합니다.</p> |
| **방문자 유지** > **판매 주기** > **첫 구매까지 소요된 일** | 방문자가 사이트에 처음 방문한 후 구매를 수행하는 시점까지 경과된 시간(일)을 확인할 수 있습니다. 예를 들어 방문자가 처음 방문한 다음 하루 후에 구매한다면 그 이후의 모든 방문 또는 이벤트는 &quot;1일&quot; 차원 항목에 속합니다.<p>**이를 통해** 방문자가 구매하는 데 걸리는 시간을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트를 업데이트하여 더 빠른 고객 확보를 촉진하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 첫 구매까지 소요된 일수 차원을 사용합니다.</p> |
| **방문자 유지** > **판매 주기** > **마지막 구매 이후 일수** | 방문자의 현재 히트와 해당 시점의 가장 최근 구매 사이에 경과된 시간을 확인할 수 있습니다.<p>**이렇게 하면** 방문자가 사용자의 사이트에서 구매를 한 후 취하는 행동을 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트를 업데이트하여 후속 구매를 장려하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 마지막 구매 이후 일 수 차원을 사용합니다.</p> |
| **모바일** > **장치** | 사람들이 귀하의 사이트에 접속하는 데 사용하는 모바일 디바이스의 제조사와 모델을 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 모바일 디바이스를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 모바일 디바이스에 맞게 사이트 렌더링을 최적화하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 모바일 장치 이름 차원을 사용합니다.</p> |
| **모바일** > **장치 유형** | 휴대폰 및 태블릿과 같이 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스 유형을 확인할 수 있습니다.<p>**이렇게 하면**&#x200B;사이트에 액세스하는 데 사용되는 다양한 종류의 모바일 장치를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라 가장 많이 사용되는 모바일 장치 유형에 맞게 사이트를 최적화하는 등 여러 가지 작업을 수행할 수 있습니다**.</p><p>이 템플릿은 모바일 디바이스 유형 차원을 사용합니다.</p> |
| **모바일** > **제조업체** | Apple 및 삼성과 같이 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스를 생산하는 제조업체를 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 제조업체를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 다양한 제조업체의 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 모바일 제조업체 차원을 사용합니다.</p> |
| **모바일** > **화면 크기** | 사용자가 사이트에 액세스하는 데 사용하는 상위 모바일 화면 크기를 확인할 수 있습니다.<p>**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 모바일 화면 크기를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p> |
| **모바일** > **화면 높이** | 사용자가 사이트에 액세스하는 데 사용하는 상위 모바일 화면 높이를 확인할 수 있습니다.<p>**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 모바일 화면 높이를 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p> |
| **모바일** > **화면 너비** | 사용자가 사이트에 액세스하는 데 사용하는 상위 모바일 화면 폭을 확인할 수 있습니다.<p>**이를 통해** 방문자에게 콘텐츠가 어떻게 표시되는지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 모바일 화면 폭을 사용하여 사이트의 새 버전을 테스트하여 사이트 품질을 개선하는 등 다양한 작업을 수행할 수 있습니다. 이렇게 하면 품질 관리 노력의 효과를 극대화할 수 있습니다.</p> |
| **모바일** > **모바일 앱 사용** | 앱에서 사용자, 시작 및 첫 번째 시작의 수와 평균 세션 길이를 확인합니다.<p>**앱이 얼마나 사용되고 있는지 이해하는 데**&#x200B;도움이 됩니다. </p><p>**학습한 내용을 바탕으로** 사용량에 맞게 확장할 수 있도록 앱 성능 개선 등 다양한 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |
| **모바일** > **모바일 앱 여정** | 모바일 앱의 눈에 띄는 사용 패턴을 확인합니다. <p>**사람들이 앱을 사용하는 방법을 이해하는 데 도움이 됩니다**. </p><p>**학습한 내용을 바탕으로** 가장 일반적인 워크플로를 타기팅하기 위해 사람들이 한 화면에서 다른 화면으로 이동하는 방법을 개선하는 등 다양한 작업을 수행할 수 있습니다. </p><!-- This template uses the --> |
| **모바일** > **모바일 앱 지표** | 가장 일반적인 모바일 앱 지표를 확인합니다. <p>**이를 통해** 모바일 앱의 기본 성능을 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 앱의 전반적인 상태 및 성능을 평가하는 등 다양한 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |
| **모바일** > **모바일 앱 메시지** | 인앱 메시지와 앱의 푸시 메시지의 실질 데이터를 확인합니다.<p>**이를 통해** 사람들이 인앱 메시지 기능을 어떻게 사용하고 있는지, 푸시 알림이 얼마나 효율적으로 앱으로 트래픽을 유도하고 있는지 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 인앱 메시지 푸시 알림 경험을 개선하는 등 다양한 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |
| **모바일** > **모바일 앱 성능** | 앱의 성능과 사용자 문제가 발생하고 있는 위치를 확인합니다. <p>**앱을 사용하는 사용자의 속도가 느려지거나 성능이 저하되는 경우**&#x200B;더 잘 이해할 수 있습니다. </p><p>**학습한 내용을 바탕으로** 기존 문제를 해결하거나 문제가 발생하기 이전에 앱 성능을 개선하는 등 다양한 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |
| **모바일** > **모바일 앱 유지** | 충성도가 가장 높은 앱 사용자가 누구인지, 앱에서 어떤 작업을 하는지 확인합니다. <p>**이를 통해** 충성도가 가장 높은 사용자가 앱을 어떻게 사용하고 있는지 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 충성도가 가장 높은 사용자가 사용하는 기능에 대한 마케팅 활동을 개선하는 등 다양한 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |
| **보트** | 사이트의 봇 트래픽과 관련된 페이지 조회수와 추세를 확인할 수 있습니다. <p>**이를 통해** 구성된 봇 규칙에 따라 보고서에서 필터링되고 있는 봇 트래픽 양을 파악할 수 있습니다.</p><p>**학습한 내용에 따라** 보트 활동을 계속 모니터링하여 새로운 패턴을 식별하는 등 여러 가지 작업을 수행할 수 있습니다.</p><!-- This template uses the --> |

### 획득 {#web-acquisition}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-acquisition-template"
>title="웹 사이트가 모바일 디바이스에서 방문자를 확보하는 방식을 확인할 수 있습니다."
>abstract="**이를 통해** 검색 키워드, 참조 도메인 등 확보로 이어지는 다양한 요인에 대해 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 효과적인 채널에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 바운스 비율 지표와 바운스 지표를 사용합니다. 또한 검색 엔진 차원, 검색 키워드 차원, 진입 페이지 차원, 참조 도메인 차원, 추적 코드 차원 및 참조자 차원도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--advertisingAnalyticsPaidSearch"
>title="모든 Google 및 Bing 유료 검색 데이터를 나란히 확인할 수 있습니다."
>abstract="**이를 통해** 사이트로 유입되는 트래픽 양과 고객이 전환되는지 여부를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 광고 캠페인의 비용 효율을 예측하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--searchEngineRankRankedReport"
>title="방문자가 사이트에 접속하기 위해 클릭한 검색 결과 페이지를 확인할 수 있습니다. 예를 들어 사이트가 검색 엔진의 검색 결과 중 두 번째 페이지에 나타나는 경우 이 변수의 차원 항목은 검색 페이지 2입니다."
>abstract="**이렇게 하면** 검색 결과에서 페이지 순위가 얼마나 높은지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 콘텐츠가 검색 결과 중 첫 번째 페이지에 나타나도록 SEO 전략을 개선하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--marketing-channel-overview-template"
>title="사용자 정의 속성을 사용할 때 이 템플릿은 방문자가 사이트에 접속하는 방법을 보여 줍니다."
>abstract="**이를 통해** 어떤 마케팅 채널이 가장 효과적인지 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 효과적인 마케팅 채널에 더 많이 투자하고 효과가 낮은 마케팅 채널에서 철수하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 ID(변수/마케팅채널) 차원과 매출 지수를 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstouchChannelRankedReport"
>title="방문자의 참여 기간(기본 30일) 동안 방문자가 매칭한 첫 번째 마케팅 채널을 확인할 수 있습니다."
>abstract="**이를 통해** 사이트로 초기 트래픽을 유도하는 마케팅 채널을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 효과적인 분야에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 첫 번째 터치 채널 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstouchChannelDetailRankedReport"
>title="방문자의 참여 기간(기본 30일) 동안 방문자가 매칭한 첫 번째 마케팅 채널의 세부 정보를 확인할 수 있습니다."
>abstract="**이를 통해** 마케팅 채널과 일치하는 히트의 요소를 더 잘 이해할 수 있습니다. 예를 들어 방문자가 사이트에 도달하고 &#39;유료 검색&#39; 마케팅 채널과 일치하는 경우 채널 세부 사항을 사용하여 사용한 검색 엔진 또는 검색한 키워드를 확인할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 효과적인 분야에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 첫 번째 터치 채널 세부 정보 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--campaignConversionReport"
>title="캠페인에 대한 클릭스루 수와 체크아웃 수를 확인할 있습니다."
>abstract="**이를 통해** 마케팅 캠페인으로 전환을 유도하는 방법을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 많은 ROI를 생성하는 마케팅 캠페인을 확인하는 등 다양한 작업을 수행할 수 있습니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--retail-campaign-performance-template"
>title="마케팅 캠페인의 성과에 대한 세부 정보를 확인할 수 있습니다."
>abstract="**이를 통해** 매출, 제품 조회수, 주문 등 캠페인과 관련된 다양한 성공 지표에 대해 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 많은 매출을 창출한 캠페인에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 매출 지표, 제품 조회수 지표, 장바구니 추가 지표, 주문 지표, 판매량 지표를 사용합니다. 또한 추적 코드 차원과 참조 도메인 차원도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-acquisition-template"
>title="웹 사이트에 방문자가 확보되는 방법을 확인할 수 있습니다."
>abstract="**이를 통해** 검색 키워드, 참조 도메인 등 확보로 이어지는 다양한 요인에 대해 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 효과적인 채널에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 바운스 비율 지표와 바운스 지표를 사용합니다. 또한 검색 엔진 차원, 검색 키워드 차원, 진입 페이지 차원, 참조 도메인 차원, 추적 코드 차원 및 참조자 차원도 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchKeywordRankedReport"
>title="유료 검색이든 자연어 검색이든, 방문자가 사이트에 접속하는 데 사용하는 검색 키워드를 확인할 수 있습니다."
>abstract="**이를 통해** 검색에서 사용자가 사이트 트래픽을 초래하는 키워드를 더 잘 이해할 수 있습니다. <br/>**학습한 내용을 바탕으로** 사용 중인 키워드와 사이트 트래픽을 유발하는 키워드 간의 SEO 격차를 파악하고 채우는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 검색 키워드 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchPaidKeywordRankedReport"
>title="방문자가 사이트에 도달하는 데 사용하는 검색 키워드를 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치합니다."
>abstract="**이를 통해** 검색에서 사용자가 사이트 트래픽을 초래하는 키워드를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사용 중인 키워드와 사이트 트래픽을 유발하는 키워드 간의 SEO 격차를 파악하고 채우는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 검색 키워드 - 유료 차원을 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchNaturalKeywordRankedReport"
>title="방문자가 사이트에 도달하는 데 사용하는 검색 키워드를 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치하지 않습니다."
>abstract="**이를 통해** 검색에서 사용자가 사이트 트래픽을 초래하는 키워드를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사용 중인 키워드와 사이트 트래픽을 유발하는 키워드 간의 SEO 격차를 파악하고 채우는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 검색 키워드 - 자연어 차원을 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchRankedReport"
>title="유료 검색이든 자연어 검색이든, 방문자가 사이트에 접속하는 데 사용하는 검색 엔진을 확인할 수 있습니다."
>abstract="**이를 통해** 사용자가 사용 시 사이트 트래픽을 초래하는 검색 엔진을 더 잘 이해할 수 있습니다. <br/>**학습한 내용을 바탕으로** 사이트에 가장 많은 트래픽을 유도하는 검색 엔진에 SEO 작업을 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 검색 엔진 차원을 사용합니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchPaidRankedReport"
>title="방문자가 사이트에 도달하는 데 사용하는 검색 엔진을 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치합니다."
>abstract="**이를 통해** 사용자가 사용 시 사이트 트래픽을 초래하는 검색 엔진을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트에 가장 많은 트래픽을 유도하는 검색 엔진에 SEO 작업을 집중하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 검색 엔진 - 유료 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchNaturalRankedReport"
>title="방문자가 사이트에 도달하는 데 사용하는 검색 키워드를 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치하지 않습니다."
>abstract="**이를 통해** 사용자가 사용 시 사이트 트래픽을 초래하는 검색 엔진을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 사이트에 가장 많은 트래픽을 유도하는 검색 엔진에 SEO 작업을 집중하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 검색 엔진 - 자연어 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referringDomainRankedReport"
>title="사용자가 사이트에 액세스하기 위해 클릭하는 도메인을 확인할 수 있습니다."
>abstract="**이를 통해** 트래픽이 가장 많이 발생하는 서드파티 사이트를 파악할 수 있습니다. (링크는 외부 사이트에 있어야 하며, 차원 항목을 표시하려면 방문자가 링크를 클릭해야 합니다.)<br/>**학습한 내용을 바탕으로** 최고 상위 참조 도메인에서 오는 방문자의 관심사에 더 잘 부합하는 콘텐츠를 만들거나 조정하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 참조 도메인 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referringDomainOriginalRankedReport"
>title="사용자가 사이트에 도달하기 위해 클릭한 첫 번째 참조 도메인을 확인할 수 있습니다. (설정되면 해당 방문자 ID의 전체 라이프타임 동안 동일한 값을 포함합니다.)"
>abstract="**이를 통해** 원래 사이트로 트래픽을 유도하는 서드파티 사이트를 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 최초 상위 참조 도메인에서 오는 방문자의 관심사에 더 잘 부합하도록 콘텐츠를 만들거나 조정하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 최초 참조 도메인 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referrerRankedReport"
>title="방문자가 사이트에 접속하기 위해 클릭했던 URL을 확인할 수 있습니다. (링크는 외부 URL에 있어야 하며, 차원 항목을 표시하려면 방문자가 링크를 클릭해야 합니다.)"
>abstract="**이를 통해** 사이트에 가장 많은 트래픽을 전송하는 특정 URL을 파악할 수 있습니다.<br/>**학습한 내용을 바탕으로** 상위 URL에서 오는 방문자의 관심사에 더 잘 부합하도록 콘텐츠를 만들거나 조정하는 등 다양한 작업을 수행할 수 있습니다. <br/>이 템플릿은 참조 도메인 차원을 사용합니다.</p>"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referrerTypeRankedReport"
>title="방문자가 사이트에 접속하기 위해 클릭한 일반 채널을 확인할 수 있습니다. Adobe는 각 채널에 대한 규칙을 유지 관리합니다. 가능한 채널로는 검색 엔진, 소셜 네트워크, 다른 웹 사이트, 하드 드라이브 또는 이메일 등이 있습니다."
>abstract="**이를 통해** 사이트에 가장 많은 트래픽을 유도하는 참조자 유형을 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 특정 채널에서 오는 방문자의 관심사에 더 잘 부합하도록 콘텐츠를 만들거나 조정하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 참조자 유형 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

다음 템플릿을 사용할 수 있습니다.

| 템플릿 이름 | 이 템플릿 <!-- What do you do with it? What can it help you learn? and What are the potential actions? -->을(를) 사용하는 이유 |
| --- | --- | 
| [!UICONTROL **마케팅 채널**] > [!UICONTROL **채널 개요 보고서**] | 사용자 정의 속성을 사용할 때 이 템플릿은 방문자가 사이트에 접속하는 방법을 보여 줍니다.<p>**이를 통해** 어떤 마케팅 채널이 가장 효과적인지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 효과적인 마케팅 채널에 더 많이 투자하고 효과가 낮은 마케팅 채널에서 철수하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 ID(변수/마케팅 채널) 차원과 매출 지표를 사용합니다.</p> |
| [!UICONTROL **마케팅 채널**] > [!UICONTROL **첫 번째 터치 채널**] | 방문자의 참여 기간(기본 30일) 동안 방문자가 매칭한 첫 번째 마케팅 채널을 확인할 수 있습니다. <p>**이를 통해** 사이트로 초기 트래픽을 유도하는 마케팅 채널을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 효과적인 분야에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 첫 번째 터치 채널 차원을 사용합니다.</p> |
| [!UICONTROL **마케팅 채널**] > [!UICONTROL **첫 번째 터치 채널 세부 정보**] | 방문자의 참여 기간(기본 30일) 동안 방문자가 매칭한 첫 번째 마케팅 채널의 세부 정보를 확인할 수 있습니다.<p>**이를 통해** 마케팅 채널과 일치하는 히트의 요소를 더 잘 이해할 수 있습니다. 예를 들어 방문자가 사이트에 도달하고 &#39;유료 검색&#39; 마케팅 채널과 일치하는 경우 채널 세부 사항을 사용하여 사용한 검색 엔진 또는 검색한 키워드를 확인할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 효과적인 분야에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 첫 번째 터치 채널 세부 사항 차원을 사용합니다.</p> |
| [!UICONTROL **마케팅 채널**] > [!UICONTROL **마지막 터치 채널**] | 해당 방문자의 참여 기간(기본적으로 30일) 동안 방문자가 일치하는 가장 최근 마케팅 채널을 봅니다.<p>**이를 통해**&#x200B;사이트 트래픽을 유도하여 전환되는 마케팅 채널을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 효과적인 분야에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 마지막 터치 채널 차원을 사용합니다.  </p> |
| [!UICONTROL **마케팅 채널**] > [!UICONTROL **마지막 터치 채널 세부 정보**] | 해당 방문자의 참여 기간(기본적으로 30일) 동안 방문자가 일치하는 가장 최근 마케팅 채널에 대한 세부 정보를 봅니다<p>**이를 통해** 마케팅 채널과 일치하는 히트의 요소를 더 잘 이해할 수 있습니다. 예를 들어 방문자가 사이트에 도달하고 &#39;유료 검색&#39; 마케팅 채널과 일치하는 경우 채널 세부 사항을 사용하여 사용한 검색 엔진 또는 검색한 키워드를 확인할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 효과적인 분야에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다. </p><p>이 템플릿은 마지막 터치 채널 세부 사항 차원을 사용합니다. </p> |
| [!UICONTROL **캠페인**] > [!UICONTROL **캠페인 전환 단계**] | 캠페인에 대한 클릭스루 수와 체크아웃 수를 확인할 있습니다. <p>**이를 통해** 마케팅 캠페인으로 전환을 유도하는 방법을 파악할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 많은 ROI를 생성하는 마케팅 캠페인을 확인하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| [!UICONTROL **캠페인**] > [!UICONTROL **캠페인 성과**] | 마케팅 캠페인의 성과에 대한 세부 정보를 확인할 수 있습니다.<p>**이를 통해** 매출, 제품 조회수, 주문 등 캠페인과 관련된 다양한 성공 지표에 대해 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라** 가장 많은 매출을 창출하는 캠페인에 마케팅 노력을 집중하는 것과 같이 여러 가지 작업을 수행할 수 있습니다. </p><p>이 템플릿은 매출 지표, 제품 보기 지표, 장바구니 추가 지표, 주문 지표 및 판매량 지표를 사용합니다. 또한 추적 코드 차원과 참조 도메인 차원도 사용합니다. </p> |
| [!UICONTROL **캠페인**] > [!UICONTROL **추적 코드**] | 사이트에서 추적 코드의 이름을 봅니다. 인터넷의 서로 다른 위치에 서로 다른 쿼리 문자열 매개 변수 값이 있는 링크를 배치할 수 있습니다.<p>**이렇게 하면**&#x200B;사이트로 트래픽을 유도하는 데 가장 성공한 링크를 더 잘 이해할 수 있습니다. 추적 코드 쿼리 문자열 추가는 조직이 사용하는 이메일, 광고, 소셜 미디어 게시물 및 기타 마케팅 노력에서 일반적입니다</p><p>**학습한 내용에 따라** 가장 많은 매출을 창출하는 캠페인에 마케팅 노력을 집중하는 것과 같이 여러 가지 작업을 수행할 수 있습니다.</p><p>이 템플릿은 추적 코드 차원을 사용합니다. </p> |
| **웹 고객 확보** | 웹 사이트에 방문자가 확보되는 방법을 확인할 수 있습니다.<p>**이를 통해** 검색 키워드, 참조 도메인 등 확보로 이어지는 다양한 요인에 대해 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 효과적인 채널에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 바운스 비율 지표와 바운스 수 지표를 사용합니다. 또한 검색 엔진 차원, 검색 키워드 차원, 진입 페이지 차원, 참조 도메인 차원, 추적 코드 차원 및 참조자 차원도 사용합니다.  </p> |
| **모바일 고객 확보** | 사이트가 모바일 장치에서 방문자를 확보하는 방법을 봅니다.<p>**이를 통해** 검색 키워드, 참조 도메인 등 확보로 이어지는 다양한 요인에 대해 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 효과적인 채널에 마케팅 활동을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 바운스 비율 지표와 바운스 수 지표를 사용합니다. 또한 검색 엔진 차원, 검색 키워드 차원, 진입 페이지 차원, 참조 도메인 차원, 추적 코드 차원 및 참조자 차원도 사용합니다.  </p> |
| **Advertising Analytics 유료 검색** | 모든 Google 및 Bing 유료 검색 데이터를 나란히 확인할 수 있습니다. <p>**이를 통해** 사이트로 유입되는 트래픽 양과 고객이 전환되는지 여부를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 광고 캠페인의 비용 효율을 예측하는 등 다양한 작업을 수행할 수 있습니다.</p> |
| **검색 키워드 - 모두** | 유료 검색이든 자연어 검색이든, 방문자가 사이트에 접속하는 데 사용하는 검색 키워드를 확인할 수 있습니다. <p>**이를 통해** 검색에서 사용자가 사이트 트래픽을 초래하는 키워드를 더 잘 이해할 수 있습니다. </p><p>**학습한 내용에 따라** 사용된 키워드와 사이트 트래픽을 유도하는 키워드 간의 SEO 간격을 식별하고 채우는 등의 여러 작업을 수행할 수 있습니다.</p><p>이 템플릿은 검색 키워드 차원을 사용합니다. </p> |
| **검색 키워드 - 유료** | 방문자가 사이트에 도달하는 데 사용하는 검색 키워드를 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치합니다.<p>**이를 통해** 검색에서 사용자가 사이트 트래픽을 초래하는 키워드를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라** 사용된 키워드와 사이트 트래픽을 유도하는 키워드 간의 SEO 간격을 식별하고 채우는 등의 여러 작업을 수행할 수 있습니다. </p><p>이 템플릿은 검색 키워드 - 유료 차원을 사용합니다. </p> |
| **검색 키워드 - 자연어** | 방문자가 사이트에 도달하는 데 사용하는 검색 키워드를 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치하지 않습니다.<p>**이를 통해** 검색에서 사용자가 사이트 트래픽을 초래하는 키워드를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라** 사용된 키워드와 사이트 트래픽을 유도하는 키워드 간의 SEO 간격을 식별하고 채우는 등의 여러 작업을 수행할 수 있습니다.</p><p>이 템플릿은 검색 키워드 - 자연어 차원을 사용합니다. </p> |
| **검색 엔진 - 모두** | 유료 검색이든 자연어 검색이든, 방문자가 사이트에 접속하는 데 사용하는 검색 엔진을 확인할 수 있습니다. <p>**이를 통해** 사용자가 사용 시 사이트 트래픽을 초래하는 검색 엔진을 더 잘 이해할 수 있습니다. </p><p>**학습한 내용을 바탕으로** 사이트에 가장 많은 트래픽을 유도하는 검색 엔진에 SEO 작업을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 검색 엔진 차원을 사용합니다. </p> |
| **검색 엔진 - 유료** | 방문자가 사이트에 도달하는 데 사용하는 검색 엔진을 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치합니다.<p>**이를 통해** 사용자가 사용 시 사이트 트래픽을 초래하는 검색 엔진을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트에 가장 많은 트래픽을 유도하는 검색 엔진에 SEO 작업을 집중하는 등 다양한 작업을 수행할 수 있습니다. </p><p>이 템플릿은 검색 엔진 - 유료 차원을 사용합니다. </p> |
| **검색 엔진 - 자연어** | 방문자가 사이트에 도달하는 데 사용하는 검색 키워드를 확인할 수 있으며, 이 키워드는 유료 검색 감지와 일치하지 않습니다.<p>**이를 통해** 사용자가 사용 시 사이트 트래픽을 초래하는 검색 엔진을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 사이트에 가장 많은 트래픽을 유도하는 검색 엔진에 SEO 작업을 집중하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 검색 엔진 - 자연어 차원을 사용합니다. </p> |
| **모든 검색 페이지 순위** | 방문자가 사이트에 접속하기 위해 클릭한 검색 결과 페이지를 확인할 수 있습니다. 예를 들어, 사이트가 검색 엔진의 검색 결과 중 두 번째 페이지에 나타나는 경우 이 변수의 차원 항목은 &quot;검색 페이지 2&quot;입니다.<p>**이렇게 하면** 검색 결과에서 페이지 순위가 얼마나 높은지 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라** 검색 결과의 첫 페이지에 콘텐츠가 표시되도록 SEO 전략을 개선하는 등 여러 가지 작업을 수행할 수 있습니다. </p> |
| **참조 도메인** | 사용자가 사이트에 액세스하기 위해 클릭하는 도메인을 확인할 수 있습니다.<p>**이를 통해** 트래픽이 가장 많이 발생하는 서드파티 사이트를 파악할 수 있습니다. (링크는 외부 사이트에 있어야 하며, 차원 항목을 표시하려면 방문자가 링크를 클릭해야 합니다.)</p><p>**학습한 내용에 따라** 콘텐츠를 만들거나 조정하는 등 다양한 작업을 수행하여 상위 참조 도메인에서 온 방문자의 관심사에 더 가깝게 맞출 수 있습니다. </p><p>이 템플릿은 참조 도메인 차원을 사용합니다. </p> |
| **원래 참조 도메인** | 사용자가 사이트에 도달하기 위해 클릭한 첫 번째 참조 도메인을 확인할 수 있습니다. (설정되면 해당 방문자 ID의 전체 라이프타임 동안 동일한 값을 포함합니다.)<p>**이를 통해** 원래 사이트로 트래픽을 유도하는 서드파티 사이트를 파악할 수 있습니다.</p><p>**학습한 내용에 따라** 콘텐츠를 만들거나 조정하는 등 다양한 작업을 수행하여 상위 최초 참조 도메인에서 온 방문자의 관심사에 더 가깝게 맞출 수 있습니다. </p><p>이 템플릿은 최초 참조 도메인 차원을 사용합니다. </p> |
| **레퍼러** | 방문자가 사이트에 접속하기 위해 클릭했던 URL을 확인할 수 있습니다. (링크는 외부 URL에 있어야 하며, 차원 항목을 표시하려면 방문자가 링크를 클릭해야 합니다.)  <p>**이를 통해** 사이트에 가장 많은 트래픽을 전송하는 특정 URL을 파악할 수 있습니다.</p><p>**학습한 내용에 따라** 콘텐츠를 만들거나 조정하는 등 여러 가지 작업을 수행하여 상위 URL에서 온 방문자의 관심사에 더 가깝게 맞출 수 있습니다. </p><p>이 템플릿은 참조 도메인 차원을 사용합니다. </p><p>이 템플릿은 레퍼러 차원을 사용합니다. </p> |
| **레퍼러 유형** | 방문자가 사이트에 접속하기 위해 클릭한 일반 채널을 확인할 수 있습니다. Adobe는 각 채널에 대한 규칙을 유지 관리합니다. 가능한 채널로는 검색 엔진, 소셜 네트워크, 다른 웹 사이트, 하드 드라이브 또는 이메일 등이 있습니다.<p>**이를 통해** 사이트에 가장 많은 트래픽을 유도하는 참조자 유형을 더 잘 이해할 수 있습니다.</p><p>**학습한 내용에 따라 특정 채널에서 온 방문자의 관심사에 더 가깝게 맞추기 위해 콘텐츠를 만들거나 조정하는 등 여러 가지 작업을 수행할 수 있습니다**.</p><p>이 템플릿은 레퍼러 유형 차원을 사용합니다.</p> |

## 모바일 템플릿

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileCarrierRankedReport"
>title="사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다."
>abstract="**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 이동통신사 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileDeviceNameRankedReport"
>title="사람들이 귀하의 사이트에 접속하는 데 사용하는 모바일 디바이스의 제조사와 모델을 확인할 수 있습니다."
>abstract="**이를 통해** 사용자 사이에서 가장 인기 있는 모바일 디바이스를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 일반적인 모바일 디바이스에 맞게 사이트 렌더링을 최적화하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 모바일 디바이스 이름 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileDeviceTypeRankedReport"
>title="휴대폰 및 태블릿과 같이 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스 유형을 확인할 수 있습니다."
>abstract="**이를 통해** 사이트에 액세스하는 데 사용되는 다양한 종류의 모바일 디바이스를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 가장 많이 사용되는 모바일 디바이스 유형에 맞게 사이트를 최적화하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 모바일 디바이스 유형 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileManufacturerRankedReport"
>title="Apple 및 삼성과 같이 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스를 생산하는 제조업체를 확인할 수 있습니다."
>abstract="**이를 통해** 사용자 사이에서 가장 인기 있는 제조업체를 더 잘 이해할 수 있습니다.<br/>**학습한 내용을 바탕으로** 다양한 제조업체의 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.<br/>이 템플릿은 모바일 디바이스 제조업체 차원을 사용합니다."

<!-- markdownlint-enable MD034 -->

다음 템플릿을 사용할 수 있습니다.

| 템플릿 이름 | 이 템플릿 <!-- What do you do with it? What can it help you learn? and What are the potential actions? -->을(를) 사용하는 이유 |
| --- | --- | 
| [!UICONTROL **이동통신사**] | 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스에 셀룰러 네트워크 연결을 제공하는 통신 회사를 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 이동통신사를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 다양한 통신사의 네트워크 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 이동통신사 차원을 사용합니다.</p> |
| **장치** | 사람들이 귀하의 사이트에 접속하는 데 사용하는 모바일 디바이스의 제조사와 모델을 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 모바일 디바이스를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 일반적인 모바일 디바이스에 맞게 사이트 렌더링을 최적화하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 모바일 장치 이름 차원을 사용합니다.</p> |
| **장치 유형** | 휴대폰 및 태블릿과 같이 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스 유형을 확인할 수 있습니다.<p>**이를 통해** 사이트에 액세스하는 데 사용되는 다양한 종류의 모바일 디바이스를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 가장 많이 사용되는 모바일 디바이스 유형에 맞게 사이트를 최적화하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 모바일 디바이스 유형 차원을 사용합니다.</p> |
| **제조업체** | Apple 및 삼성과 같이 사용자가 사이트에 액세스하는 데 사용하는 모바일 디바이스를 생산하는 제조업체를 확인할 수 있습니다.<p>**이를 통해** 사용자 사이에서 가장 인기 있는 제조업체를 더 잘 이해할 수 있습니다.</p><p>**학습한 내용을 바탕으로** 다양한 제조업체의 기능을 기반으로 콘텐츠 게재를 맞춤화하여 원활한 사용자 경험을 보장하는 등 다양한 작업을 수행할 수 있습니다.</p><p>이 템플릿은 모바일 제조업체 차원을 사용합니다.</p> |
