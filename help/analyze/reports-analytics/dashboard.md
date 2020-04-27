---
description: 대시보드는 reportlet이라고 부르는 썸네일 보고서의 콜렉션입니다. 대시보드는 검색 방법, 방문자 프로파일 등과 같은 사이트의 특정 측면에 대한 전체 개요를 설명하는 관련 reportlet이 들어 있을 때 가장 유용합니다.
subtopic: Dashboards
title: 대시보드 및 Reportlet
topic: Reports and analytics
uuid: 7a7b3bc9-0a3c-49b0-9168-e2878ae67b97
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 대시보드 및 Reportlet

대시보드는 reportlet이라고 부르는 썸네일 보고서의 콜렉션입니다. 대시보드는 검색 방법, 방문자 프로파일 등과 같은 사이트의 특정 측면에 대한 전체 개요를 설명하는 관련 reportlet이 들어 있을 때 가장 유용합니다.

## 대시보드 및 Reportlet {#concept_8CD3ACA2830A4994A68A31D8773B57E0}

대시보드는 *`reportlets`*&#x200B;이라고 하는 썸네일 보고서의 컬렉션입니다. 대시보드는 검색 방법, 방문자 프로파일 등과 같은 사이트의 특정 측면에 대한 전체 개요를 설명하는 관련 reportlet이 들어 있을 때 가장 유용합니다.

대부분의 마케팅 보고서를 대시보드에 추가할 수 있습니다. 여기에는 [!UICONTROL Fallout Report], [!UICONTROL Conversion Funnel Report]및 [!UICONTROL Pathfinder Report]과 같은 그래픽 중심 보고서가 포함됩니다.

대시보드를 랜딩 페이지로 설정하여 다른 사용자와 공유하고 배달 일정을 예약할 수도 있습니다. If you do not set a dashboard (or a bookmark) as a landing page, the [!UICONTROL My Recommended Reports] dashboard displays. **[!UICONTROL My Recommended Reports]** 보고서는 보고서와 가장 자주 본 보고서 5개를 **[!UICONTROL Key Metrics]** 보여줍니다. 이 보고서는 동적으로 변하며 가장 많이 보는 실제 보고서를 기반으로 합니다.

자주 본 보고서 중 일부는 대시보드가 될 수 없으며 나타나지 않습니다. 다음과 같은 보고서가 포함됩니다.

* 예외 항목 탐지 보고서
* 기여도 분석 보고서
* 폴아웃 보고서
* 경로 탐색 보고서
* 실시간 보고서
* 기타 대시보드

>[!NOTE] 대시보드가 더 이상 보고 및 분석에 표시되지 않습니다. **[!UICONTROL Site Overview]** 하지만 여전히 일부 또는 모든 Reportlet을 보게 되는 2가지 상황이 있습니다.

* If you have, say, only three frequently viewed reports, Reports &amp; Analytics will take two reports from the Site Overview dashboard to complete the **[!UICONTROL My Recommended Reports]** dashboard.
* 새 보고서 세트는 자주 보는 보고서로 대체될 때까지 처음의 사이트 개요 Reportlet 기능을 가지고 있습니다. 그렇다 하더라도 이제 대시보드가 **[!UICONTROL My Recommended Reports]**&#x200B;호출됩니다.

사용자가 만든 대시보드 이외에 사용자 각각에 대해 다음과 같은 미리 패키지한 대시보드가 포함됩니다.

**[!UICONTROL Components]>[!UICONTROL Dashboards]>[!UICONTROL Shared Dashboards]>[!UICONTROL Local Sites]**

사용자 지정 가능한 이 대시보드에서는 reportlet을 제공된 템플릿에 적용하는 방법을 제공합니다.

**[!UICONTROL Components]>[!UICONTROL Dashboards]>[!UICONTROL Shared Dashboards]>[!UICONTROL Site Operations Dashboard]**

이 대시보드는 웹 사이트 작업과 관련된 주요 지표의 개요를 제공합니다. 이 대시보드의 보고서에는 다음이 포함되어 있습니다.

* 종료 페이지
* 가장 방문 빈도가 높은 페이지
* 가장 방문 빈도가 높은 사이트 섹션
* KPI/측정 리포트릿
* 텍스트 리포트릿
* 회사 요약 리포트릿

Use the [!UICONTROL Dashboard Manager] to edit and manage dashboards, and enable them for DirectAccess.

See [Managing Dashboards](/help/analyze/reports-analytics/dashboard-manage.md).

## 대시보드 만들기 {#task_54EFBED59BDC4418A919E6EF84AB9CFF}

대시보드를 만드는 방법을 설명하는 단계입니다.

<!-- 

t_dashboard_add.xml

 -->

보고서를 reportlet으로 대시보드에 추가하기 전에 대시보드의 레이아웃을 정의합니다.

1. Go to **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Manage Dashboards]**.
1. 클릭 **[!UICONTROL Add Dashboard]**.
1. 대시보드 이름을 입력합니다.
1. **[!UICONTROL 3 x 2]** 또는 **[!UICONTROL 2 x 2]**&#x200B;를 클릭하여 대시보드 페이지에 놓을 reportlet의 수를 지정합니다.
1. 대시보드 페이지 레이아웃을 구성합니다. 

   * **[!UICONTROL Add Page]**:컨텐츠를 드래그하여 reportlet을 만들 수 있는 빈 페이지를 대시보드에 추가합니다.
   * **[!UICONTROL Paper]**:가로, 세로 및 A4와 같은 용지 크기를 지정할 수 있습니다.
   * **[!UICONTROL Find Content]**:메뉴 [!UICONTROL Add Content] 및 [!UICONTROL Dashboard Contents] 메뉴에서 컨텐츠를 검색할 수 있습니다.

1. 항목을 reportlet 캔버스로 드래그하여 사용할 수 있는 컨텐츠를 대시보드에 추가합니다.

   [Reportlet 만들기](/help/analyze/reports-analytics/dashboard.md#task_EC3AFBBAA51C45CEBAF632F841C305B3) 및 [대시보드 설정 편집](/help/analyze/reports-analytics/dashboard.md#task_90D7FAC1CC3E4DB786B4C87CC33B5459)을 참조하십시오.
1. 확대/축소한 후에 **[!UICONTROL Save.]**

   Saving a dashboard makes it available in the **[!UICONTROL Dashboard]** menu. The new dashboard is also available in the [!UICONTROL Dashboard Manager] ( **[!UICONTROL Favorites]** > **[!UICONTROL Dashboards]** > **[!UICONTROL Manager]**), where you can edit, organize, share, schedule, archive dashboards, and more. ([대시보드 관리](/help/analyze/reports-analytics/dashboard-manage.md)를 참조하십시오.)

1. (선택 사항) 대시보드를 랜딩 페이지로 설정하려면 **[!UICONTROL More Options]** > **[!UICONTROL Set as Landing Page]**&#x200B;을 클릭합니다.

## Reportlet 만들기 {#task_EC3AFBBAA51C45CEBAF632F841C305B3}

reportlet을 만드는 방법을 설명하는 단계입니다. reportlet을 만들면 대시보드를 표시하는 데 사용할 수 있습니다.

<!-- 

t_dashboard_add_report.xml

 -->

1. 보고서 실행.
1. 확대/축소한 후에 **[!UICONTROL Dashboard.]**
1. 페이지에서 보고서의 이름을 지정한 다음, [!UICONTROL Add Reportlet] 대시보드에서 대시보드를 선택합니다 **[!UICONTROL Place in Dashboard]**.
1. (선택 사항) 날짜 범위를 구성합니다.

   * **[!UICONTROL Rolling]**:시간 범위(일별, 월별 등)에 따라 시간이 경과함에 따라 날짜를 변경합니다. 예를 들어, 오늘이 1월 17일인 경우 1월 15일 - 16일 범위의 날짜를 설정할 수도 있습니다. Then if you select **[!UICONTROL Rolling]**, on January 27 the reportlet displays data for January 25 - 26.
   * **[!UICONTROL Fixed]**:시간이 경과하면 날짜가 앞으로 이동하지 않습니다.

1. (선택 사항) 게시 배포 목록을 무시합니다.

   **[!UICONTROL Publishing List Override]**:이 옵션을 활성화하면 게시 목록에 배포할 때 이 reportlet에서 참조되는 보고서 세트가 항상 사용됩니다. 이 옵션을 비활성화하면 이 게시 목록에서 식별된 보고서 세트가 이 reportlet의 보고서 세트를 대체합니다.

1. 클릭 **[!UICONTROL Create New]**.

   The reportlet is added to the **[!UICONTROL Dashboard Contents]** menu in the dashboard editor.

## 대시보드에 컨텐츠 추가 {#task_90D7FAC1CC3E4DB786B4C87CC33B5459}

다른 대시보드 및 공유 대시보드에서 컨텐츠를 추가하는 방법을 설명하는 단계입니다. 텍스트 및 이미지와 같은 사용자 지정 및 외부 소스에서 컨텐츠를 추가할 수도 있습니다.

<!-- 

t_dashboard_content.xml

 -->

1. Open a dashboard, then click **[!UICONTROL Layout]**.
1. Click **[!UICONTROL Add Content]**, then drag items to the dashboard.

   The [!UICONTROL Add Content] menu displays reportlet content from other dashboards, legacy dashboards, and shared dashboards.

   >[!NOTE]
   >
   >대시보드에 있는 페이지 수의 현재 제한은 30개입니다.

   **사용자 지정 Reportlet**

   *데이터 컨텐츠:*

   * 회사 요약: 사용자가 선택하는 여러 보고서 세트와 지표에 대한 페이지 보기를 표시합니다.
   * 지표 측정: 지정한 임계값과 관련하여 지표 수치의 위치를 알려주는 측정치를 표시합니다.

      지표, 그래프 유형, 색상 범위 및 임계값을 선택할 수 있습니다. 지표의 개수가 임계값 보다 큼인 경우 측정은 reportlet의 초과 필드 위에 있는 색을 사용하여 reportlet임을 가리킵니다. 지표의 개수가 임계값 보다 작음인 경우 측정은 미만 필드 위에 있는 색을 사용하여 reportlet임을 가리킵니다. 이 필드에서 지정하는 값은 페이지 보기, 달러 금액, 장바구니 보기 횟수 등과 같이 계산할 수 있는 지표 값입니다. (특수 문자는 사용하지 마십시오.)
   * 보고서 세트 요약: 선택한 지표와 보고서 세트의 전체 또는 높은 값과 낮은 값을 표시합니다.
   * 사용 요약: 조직 내의 사람들이 인터페이스에서 액세스하는 데이터를 보여줍니다. 이 reportlet은 사용자 이름 액세스, 보고서 액세스 또는 보고서 세트 액세스별로 데이터를 보여줄 수 있습니다.
URL을 제공하여 다음 사용자 컨텐츠 reportlet을 만들 수 있습니다. 이미지 또는 기타 리소스 URL이 https://로 시작되지 않는 경우 Internet Explorer는 혼합 컨텐츠 경고를 표시할 수 있습니다. 브라우저의 보안 설정에서 혼합 컨텐츠에 대한 경고를 비활성화할 수 있습니다.
   *사용자 컨텐츠:*

   * 외부 보고서: .xml 및 .csv 형식으로 외부 보고서를 추가할 수 있습니다.
   * HTML: 사용자 지정 HTML reportlet을 추가할 수 있습니다. URL은 HTTP 또는 HTTPS를 사용해야 합니다. 그렇지 않은 경우 `Specified URL could not be retrieved` 오류가 표시됩니다. 문서의 컨텐츠에서 데이터: 및 javascript: 프로토콜을 사용하는 특성이 있는 모든 태그가 제거됩니다. 스크립트, 프레임, 애플릿, 이벤트 핸들러, 플래시 및 기타 임베디드 개체가 제거됩니다. 비HTTPS를 사용하여 리소스를 지정한 경우 IE 사용자에게는 혼합 컨텐츠에 대한 경고가 표시됩니다.
   * 이미지: 이미지 URL로부터 대시보드를 만들 수 있습니다. URL이 HTTP 프로토콜을 사용하는 경우 Internet Explorer에 혼합 컨텐츠 경고가 나타납니다. HTTPS가 있는 URL을 사용하면 경고가 제거됩니다. 모든 기타 프로토콜은 `Specified URL could not be retrieved` 오류가 발생합니다.
   * RSS: RSS 웹 피드를 추가할 수 있습니다. HTTP 또는 HTTPS여야 합니다. 그렇지 않은 경우 `Specified URL could not be retrieved` 오류가 표시됩니다. 
   * 텍스트: XHTML 코드를 사용하여 자신의 데이터를 만들 수 있습니다. URL에 HTTP 또는 HTTPS를 사용합니다. HTTP 프로토콜이 있는 텍스트 reportlet 컨텐츠에 이미지를 사용하면 IE 사용자에게 혼합된 컨텐츠에 대한 경고 메시지가 표시됩니다. 다른 프로토콜을 사용하여 포함된 이미지는 reportlet에 표시되지 않습니다.
   **내 대시보드**

   컨텐트를 새 대시보드로 이동시킬 수 있는 업그레이드된 대시보드를 나열합니다.

   **기존 대시보드**

   컨텐츠를 새 대시보드로 이동시킬 수 있는 공유된 대시보드를 나열합니다.

   **공유 대시보드**

   컨텐츠를 새 대시보드로 이동시킬 수 있는 기존 대시보드를 나열합니다. 이전의 버전과 같은 형식으로 대시보드를 유지하려면 기존 대시보드를 사용하는 것이 유용합니다.

   **대시보드 컨텐트**

   이미 대시보드에 추가한 항목을 표시합니다.

1. 확대/축소한 후에 **[!UICONTROL Save.]**

## 대시보드 및 Reportlet 데이터 편집 {#task_B460CCD70D9F40FCAC6BBC1C044CC460}

대시보드 또는 reportlet 수준에서 데이터 설정을 변경할 수 있습니다. 예를 들어, 보고서 세트를 잠그고 날짜를 변경하고 세그먼트를 적용하는 등 보고서 세트를 변경할 수 있습니다. 또한, 회사의 기밀 보호 관련 내용을 삽입하여 대시보드를 원하는 대로 수정하고 사용자 지정 reportlet에 HTML, XML, Web API 및 CSV 데이터를 포함시킬 수 있습니다.

<!-- 

t_dashboard_edit.xml

 -->

**대시보드 및 Reportlet 데이터를 편집하려면**

1. Click **[!UICONTROL Components]** > **[!UICONTROL Dashboards]** > *dashboard name* to open a dashboard.
1. 클릭 **[!UICONTROL Layout]**.

| 종료 | 방법 |
|--- |--- |
| 대시보드의 보고서 세트 변경 | Experience Cloud 헤더에서 메뉴를 클릭한 다음 보고서 세트를 선택합니다. |
| reportlet의 보고서 세트 변경 | In the reportlet, click the report suite name, then select a report suite from the [!UICONTROL Report Suite] menu. |
| 대시보드에 세그먼트 적용 | In the Experience Cloud header, click [!UICONTROL Show Segments], then select a segment. |
| reportlet에 세그먼트 적용 | 대시보드에서 레이아웃을 클릭하여 대시보드를 편집합니다.   reportlet에서 보고서 세트 이름을 클릭한 다음 세그먼트 필드에서 값을 선택하고 업데이트를 클릭합니다. |
| 보고서 세트 잠금(reportlet에 있는 보고서 세트가 변경되지 않도록 합니다.) | In the reportlet, click the report suite name, then enable [!UICONTROL Lock Report Suite]. 업데이트를 클릭합니다. |
| 보고 날짜 변경 | 대시보드에 대해 달력을 클릭합니다. (대시보드에 있는 모든 reportlet이 변경 내용을 반영합니다.)<br>reportlet에 대해 날짜 링크를 클릭한 다음 달력을 구성합니다. |
| 대시보드 이름 지정 | Open a dashboard, then click  [!UICONTROL More] >  [!UICONTROL Rename]. |
| 대시보드 아카이브 보기 | 클릭  [!UICONTROL More] >  [!UICONTROL View Archive]. |
| 대시보드를 랜딩 페이지로 설정 | In a dashboard, click  [!UICONTROL More] > [!UICONTROL Set As Landing Page]. |
| 대시보드 다운로드 | In a dashboard, click  [!UICONTROL More] >  Download. |
| 대시보드 인쇄 | In a dashboard, click  [!UICONTROL More] >  Print. |
| 대시보드 저장 | 대시보드에서 다른 이름으로 저장을 클릭한 다음 이름을 지정합니다. |

## 대시보드 공동 브랜딩 {#task_603BDE7700B945699AF5514C2DEB81F7}

대시보드에서 표시할 이미지를 업로드하는 방법을 설명하는 단계입니다.

<!-- 

t_dashboard_branding.xml

 -->

1. **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Company Settings]**.
1. 페이지에서 [!UICONTROL Company Settings] 을 클릭합니다 **[!UICONTROL Co-Brand the Adobe Experience Cloud]**.
1. 클릭 **[!UICONTROL Enable Co-Branding]**.
1. Browse to upload the image, then click **[!UICONTROL Save.]**

   브라우저에서 이미지를 볼 때 최상의 결과를 얻으려면 100px x 30px 이미지를 업로드하십시오. PDF 출력에서 최상의 결과를 얻으려면 417px x 125px(300dpi) 이미지를 업로드하십시오. 크기를 초과한 이미지는 가로/세로 비율이 유지된 채 축소됩니다.

## 대시보드에서 세그먼트 사용 {#concept_ED030C3713D54D03971FB7B209285750}

Adobe Analytics의 대부분 보고서와 마찬가지로 대시보드는 세그먼트를 사용하여 원하는 데이터를 검색할 수 있습니다.

<!-- 

segments_dashboards.xml

 -->

세그먼트는 전체 대시보드 또는 특정 Reportlet의 두 가지 수준으로 적용할 수 있습니다.

* **Reportlet 수준**:을 **[!UICONTROL Layout]**&#x200B;클릭한 다음 세그먼트화할 reportlet의 보고서 세트를 클릭합니다. Reportlet이 사용하는 세그먼트를 추가하거나 변경할 수 있는 양식 창이 나타납니다.
* **대시보드 수준**: 왼쪽 탐색 메뉴에서 세그먼트 아이콘을 클릭하고 사용할 세그먼트를 선택한 다음 [적용]을 클릭합니다. 선택한 세그먼트는 모든 Reportlet 수준 세그먼트를 재정의하고 대체합니다.
