---
description: Analysis Workspace에서 기본 보고서를 사용하는 방법에 대한 개요입니다.
title: 보고서 사용
feature: Analysis Workspace
role: User, Admin
source-git-commit: cf0c15c1b81a243e35fbdcf32b43a6ef4ada9649
workflow-type: ht
source-wordcount: '1516'
ht-degree: 100%

---

# 사전 작성된 보고서 사용

Analysis Workspace의 사전 작성된 보고서는 가장 일반적인 보고 시나리오에 대한 빠른 인사이트를 제공합니다. 다음은 사전 작성된 보고서를 통해 답변할 수 있는 몇 가지 질문의 예입니다.

* 사이트 방문자 수
* 해당 방문자 중 고유 방문자 수 (한 번만 카운트)
* 방문자의 사이트 방문 경로 (예: 링크를 따라 사이트를 방문했는지 또는 사이트에 직접 방문했는지 여부)
* 방문자가 사이트 콘텐츠를 검색하는 데 사용한 키워드
* 특정 페이지 또는 전체 사이트에서 머문 시간
* 방문자가 클릭한 링크와 사이트를 떠난 시점
* 매출 생성이나 전환 이벤트 생성에 가장 효과적인 마케팅 채널
* 비디오 보는 데 걸린 시간
* 방문자가 사이트를 방문하는 데 사용한 브라우저 및 디바이스

다음 정보는 Analysis Workspace의 [!UICONTROL 보고서] 탭에서 사전 작성된 보고서에 액세스하고 이를 사용하는 방법을 설명합니다.

## 보고서 액세스 및 실행

1. Analysis Workspace에서 [!UICONTROL **Workspace**] 탭을 선택합니다.

1. [!UICONTROL **보고서**]&#x200B;를 선택합니다.

   ![보고서 탭](assets/view-prebuilt-reports.png)

1. 검색 필드에 찾으려는 보고서 이름을 입력한 다음, 보고서 목록에서 선택합니다. 이제 prop, eVar 및 이벤트 번호로 보고서 목록을 검색할 수도 있습니다. <!-- still true? -->

   또는

   보려는 보고서 범주를 선택한 다음, 보고서 목록에서 보고서를 선택합니다.

   >[!TIP]
   >
   >   화살표 키를 사용하여 메뉴를 탐색하려면 슬래시 키(/)를 누른 다음, 아래쪽 화살표 키를 누릅니다. 선택한 보고서를 로드하려면 Enter를 누릅니다.

사용 가능한 보고서 목록을 보려면 아래의 [사용 가능한 보고서](#available-reports) 섹션을 참조하십시오.

## 보고서 저장 {#use-reports}

변경 후 보고서에서 다른 곳으로 이동하면 변경 사항을 저장하거나 취소하라는 메시지가 표시됩니다. 변경 사항을 보고서에 저장하면 보고서가 새 프로젝트로 저장됩니다.

1. [!UICONTROL **보고서**] 탭으로 이동합니다.
1. 보려는 보고서를 선택합니다. 예를 들어 [!UICONTROL **추천**] 아래에서 [!UICONTROL **페이지**] 보고서를 선택합니다.

   ![페이지 보고서](assets/pages-report.png)

1. Analysis Workspace에 표시되는 페이지 보고서에는 두 개의 [시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) ([막대 차트](/help/analyze/analysis-workspace/visualizations/bar.md) 및 [요약 번호](/help/analyze/analysis-workspace/visualizations/summary-number-change.md))와 [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md)이 표시됩니다. 사용된 지표는 발생 횟수입니다.
1. 다음 중 하나를 수행합니다.

   * 보고서를 봅니다.
   * 하나 이상의 세그먼트를 상단의 세그먼트 드롭 영역으로 드래그합니다. 예를 들어 [!UICONTROL **모바일 고객**]&#x200B;을 드래그하여 결과를 봅니다.
   * 오른쪽 상단의 달력으로 이동하여 날짜 범위를 변경합니다.
   * 차원 분류를 추가하고, 다른 지표를 드래그하고, 일반적으로 필요에 맞게 보고서를 사용자 정의합니다.

1. (선택 사항) [!UICONTROL **프로젝트**] > [!UICONTROL **저장**]&#x200B;을 선택하여 보고서를 프로젝트로 저장합니다.

   보고서가 새 프로젝트로 저장됩니다. 기존 보고서는 수정되지 않습니다. 보고서를 프로젝트로 저장하는 방법에 대한 자세한 내용은 [프로젝트 저장](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md)을 참조하십시오.

## 사용 가능한 보고서

다음 표에는 사전 작성된 사용 가능한 보고서의 전체 목록이 포함되어 있습니다.

사전 작성된 추천 보고서에는 플로우, 폴아웃, 마케팅 채널 및 실시간 보고서가 포함됩니다.

| 메뉴 항목 | 이 메뉴 항목 아래의 보고서 |
| --- | --- |
| **[!UICONTROL 가장 빈도가 높음]** | <ul><li>교육 튜토리얼(기존 Workspace 템플릿)</li><li>페이지(내 상위 페이지는 무엇입니까?)</li><li>페이지 조회수(얼마나 많은 페이지 조회수를 생성하고 있습니까?)</li><li>방문수(얼마나 많은 방문을 받고 있습니까?)</li><li>방문자수(얼마나 많은 방문자를 얻고 있습니까?)</li><li>주요 지표(내 가장 중요한 지표의 성과는 어떻습니까?)</li><li>사이트 섹션(내 사이트의 어느 섹션에서 가장 많은 페이지 조회수가 생성되었습니까?)</li><li>실시간(내 사이트의 트렌딩은 무엇이며 그 이유는 무엇입니까?)</li><li>다음 페이지(내 방문자가 다음으로 방문하는 페이지는 무엇입니까?)</li><li>이전 페이지(내 방문자가 이전에 방문한 페이지는 무엇입니까?)</li><li>캠페인(내 주요 지표를 유도하는 캠페인은 무엇입니까?)</li><li>제품(내 주요 지표를 유도하는 제품은 무엇입니까?)</li><li>마지막 터치 채널(성과가 가장 좋은 마지막 터치 채널은 무엇입니까?)</li><li>마지막 터치 채널 세부 정보(다른 채널보다 뛰어난 성과를 보이는 특정 마지막 터치 채널은 무엇입니까?)</li><li>매출(내 매출의 성과는 어떻습니까?)</li><li>주문(내 주문의 성과는 어떻습니까?)</li><li>개수(얼마나 많은 개수를 판매하고 있습니까?)</li></ul> |
| **[!UICONTROL 참여]** | <ul><li>주요 지표(내 가장 중요한 지표의 성과는 어떻습니까?)</li><li>페이지 조회수(얼마나 많은 페이지 조회수를 생성하고 있습니까?)</li><li>페이지(내 상위 페이지는 무엇입니까?)</li><li>방문수(얼마나 많은 방문을 받고 있습니까?)</li><li>방문자수(얼마나 많은 방문자를 얻고 있습니까?)</li><li>방문당 체류 시간(내 사용자는 방문당 얼마나 많은 시간을 소비합니까?)</li><li>이벤트 이전 시간(내 사용자는 성공 이벤트 전에 얼마나 많은 시간을 소비합니까?)</li><li>사이트 섹션(내 사이트의 어느 섹션에서 가장 많은 페이지 조회수가 생성되었습니까?)</li><li>웹 콘텐츠 사용량(어떤 콘텐츠가 가장 많이 소비되고 사용자의 관심을 끌고 있습니까?)</li><li>미디어 콘텐츠 사용량(어떤 콘텐츠가 가장 많이 소비되고 사용자의 관심을 끌고 있습니까?)</li><li>다음 및 이전 페이지 흐름(내 방문자가 선택한/선택했던 다음/이전 경로는 무엇입니까?)</li><li>폴아웃(내 디지털 속성 전체에서 어디에 폴아웃이 보입니까?)</li><li>디바이스 간 분석(Analysis Workspace에서 디바이스 간 분석 사용)</li><li>웹 유지(충성도가 높은 사용자는 누구이며 그들이 무슨 작업을 수행합니까?)</li><li>미디어 오디오 사용량(오디오 사용량의 트렌드 및 주요 지표는 무엇입니까?)</li><li>미디어 최신성, 빈도, 충성도(충성도 높은 독자는 누구입니까?)</li><li>페이지 분석 > 다시 로드(어떤 페이지가 가장 많은 다시 로드를 발생시킵니까?)</li><li>페이지 분석 > 방문당 체류 시간(내 사용자가 내 페이지에서 보내는 시간은 얼마입니까?)</li><li>시작 및 종료 > 시작 페이지(상위 시작 페이지는 무엇입니까?)</li><li>시작 및 종료 > 원래 시작 페이지(내 방문자가 원래 어떤 페이지에서 입장했습니까?)</li><li>시작 및 종료 >단일 페이지 방문(단일 페이지 방문이 가장 많이 발생한 페이지는 무엇입니까?)</li><li>시작 및 종료 > 종료 페이지(상위 종료 페이지는 무엇입니까?)</li></ul> |
| **[!UICONTROL 전환]** | <ul><li>제품 > 제품(내 주요 지표를 유도하는 제품은 무엇입니까?)</li><li>제품 > 제품 성과(성과가 가장 좋은 제품은 무엇입니까?)</li><li>제품 > 범주(내 제품 범주 중 가장 성과가 좋은 것은 무엇입니까?)</li><li>장바구니 > 장바구니(몇 명의 사용자가 장바구니에 제품을 추가했습니까?)</li><li>장바구니 > 장바구니 보기(내 방문자가 장바구니를 본 횟수는 몇 번입니까?)</li><li>장바구니 > 장바구니 추가(사용자가 얼마나 자주 장바구니에 제품을 추가합니까?)</li><li>장바구니 > 장바구니 제거(사용자가 얼마나 자주 장바구니에 제품을 제거합니까?)</li><li>구매 > 매출(내 매출의 성과는 어떻습니까?)</li><li>구매 > 주문(내 주문의 성과는 어떻습니까?)</li><li>구매 > 개수(얼마나 많은 개수를 판매하고 있습니까?)</li><li>[Magento: 마케팅 및 상거래](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#commerce)</li></ul> |
| **[!UICONTROL 대상자]** | <ul><li>사람 지표(얼마나 많은 사람들이 내 브랜드와 상호작용하고 있습니까?)</li><li>방문자 프로필 > 위치 개요(사용자들 사이에서 가장 많은 사용량을 유도하는 위치는 어디입니까?)</li><li>방문자 프로필 > 지리적 세분화 > 지리적 카운티, 지리적 미국 주, 지리적 지역, 지리적 도시, 지리적 미국 DMA(내 사용자는 어느 지역에서 방문합니까?)</li><li>방문자 프로필 > 언어(내 사용자가 선호하는 언어는 무엇입니까?)</li><li>방문자 프로필 > 시간대(내 사용자가 방문하는 시간대는 무엇입니까?)</li><li>방문자 프로필 > 도메인(내 방문자가 내 사이트에 액세스하는 데 사용하는 ISP는 무엇입니까?)</li><li>방문자 프로필 > 최상위 도메인(내 사이트로 트래픽을 유도하는 도메인은 무엇입니까?)</li><li>방문자 프로필 > 기술 > 기술 개요(사람들이 내 사이트에 액세스하는 데 사용하는 기술은 무엇입니까?)</li><li>방문자 프로필 > 기술 > 브라우저, 브라우저 유형, 브라우저 폭, 브라우저 높이(사람들이 내 사이트에 액세스하는 데 어떤 회사의 브라우저, 브라우저 버전, 너비 및 높이를 사용하고 있습니까?)</li><li>방문자 프로필 > 기술 > 운영 체제, 운영 체제 유형(내 방문자는 어떤 OS와 버전을 사용합니까?)</li><li>방문자 프로필 > 기술 > 이동통신사(내 방문자가 내 사이트에 액세스하는 데 사용하는 이동통신사는 무엇입니까?)</li><li>방문자 유지 > 재방문 주기(내 사용자의 현재 방문과 이전 방문 사이에 시간이 얼마나 걸립니까?)</li><li>방문자 유지 > 재방문 횟수(내 방문 중 재방문 사용자가 몇 명입니까?)</li><li>방문자 유지 > 방문 횟수(내 주요 지표의 대부분을 차지하는 방문 횟수 버킷은 무엇입니까?)</li><li>방문자 유지 > 판매 주기 > 고객 충성도(내 사용자는 어떤 충성도 세그먼트에 속합니까?)</li><li>방문자 유지 > 판매 주기 > 첫 구매까지 소요된 일 수(내 사용자의 첫 방문과 첫 구매 사이에 며칠이 지났습니까?)</li><li>방문자 유지 > 판매 주기 > 마지막 구매 이후 일 수(내 사용자의 현재 방문과 마지막 구매 사이에 며칠이 지났습니까?) ).</li><li>방문자 유지 > 모바일 > 디바이스 및 디바이스 유형(내 사용자가 사용하는 디바이스와 디바이스 유형은 무엇입니까?)</li><li>방문자 유지 > 모바일 > 제조업체(내 방문자가 사용하는 모바일 디바이스 제조업체는 무엇입니까?)</li><li>방문자 유지 > 모바일 > 화면 크기, 화면 높이, 화면 너비(내 방문자의 모바일 화면 크기/높이/너비는 무엇입니까?)</li><li>방문자 유지 > 모바일 > [모바일 앱 사용 현황](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li><li>방문자 유지 > 모바일 > [모바일 앱 여정](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li><li>방문자 유지 > 모바일 > [모바일 앱 지표](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li><li>방문자 유지 > 모바일 > [모바일 앱 메시지](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li><li>방문자 유지 > 모바일 > [모바일 앱 성과](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li><li>방문자 유지 > 모바일 > [모바일 앱 보존](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li></ul> |
| **[!UICONTROL 획득]** | <ul><li>마케팅 채널 > 첫 번째 터치 채널, 첫 번째 터치 채널 세부 정보(성과가 가장 좋은 첫 번째 터치 채널과 특정 첫 번째 터치 채널은 무엇입니까?)</li><li>마케팅 채널 > 마지막 터치 채널, 마지막 터치 채널 세부 정보(성과가 가장 좋은 마지막 터치 채널과 특정 마지막 터치 채널은 무엇입니까?)</li><li>캠페인 > 캠페인(내 주요 지표를 유도하는 캠페인은 무엇입니까?)</li><li>캠페인 > 캠페인 성과(가장 많은 매출을 창출하는 캠페인은 무엇입니까?)</li><li>캠페인 > 추적 코드(어떤 캠페인 추적 코드가 가장 성과가 좋습니까?)</li><li>[웹 고객 확보](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#web)</li><li>[모바일 고객 확보](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#mobile)</li><li>[Advertising Analytics 유료 검색](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html#advertising)</li><li>검색 키워드 - 모두, 유료, 자연어(어떤 검색 키워드와 유료/자연어 검색 키워드가 주요 지표를 가장 잘 유도합니까?)</li><li>검색 엔진 - 모두, 유료, 자연어(어떤 검색 키워드와 유료/자연어 검색 엔진 주요 지표를 가장 잘 유도합니까?)</li><li>전체 검색 페이지 순위(내 사용자는 어떤 검색 페이지에서 방문합니까?)</li><li>참조 도메인(내 사이트로 트래픽을 유도하는 도메인은 무엇입니까?)</li><li>원래 참조 도메인(내 사이트를 방문하기 전에 첫 번째 도메인 사용자는 무슨 도메인에 있었습니까?)</li><li>레퍼러(사용자가 내 사이트를 클릭하기 전에 어떤 URL을 사용했습니까?)</li><li>레퍼러 유형(내 추천 URL은 어떤 범주에 속합니까?)</li></ul> |
