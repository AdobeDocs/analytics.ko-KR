---
description: Activity Map의 기능 설정, 구성 및 채택에 대한 FAQ입니다.
title: Activity Map FAQ
topic: Activity map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
translation-type: tm+mt
source-git-commit: 5a8ff1c81644c12f7d00ef147db197f54c48f60c

---


# Activity Map FAQ

Activity Map의 기능 설정, 구성 및 채택에 대한 FAQ입니다.

## 구현 및 AppMeasurement

**Q:새 Activity Map 활성화를 위한 구현 단계는 무엇입니까?**

A:Activity [Map 활성화를 검토하십시오.](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**Q: 모든 Analytics 고객이 관리 도구 ActivityMap 지원 페이지에 액세스할 수 있습니까?**

A: Adobe SiteCatalyst 고객은 관리 콘솔의 Activity Map 지원 페이지에 액세스할 수 없습니다. Adobe Analytics Standard 및 Adobe Analytics Premium 계약에 해당하는 회사만 이 구성 페이지에 액세스할 수 있습니다.

**Q:DTM(다이내믹 태그 관리)을 통해 새 AppMeasurement 코드를 구성할 수 있습니까?**

A:예. 새 AppMeasurement 코드를 [수동으로 구현할](https://marketing.adobe.com/resources/help/en_US/dtm/analytics_dtm.html) 수 있습니다.

**Q:AppMeasurement v1.6 라이브러리의 큰 변경 사항은 무엇입니까?**

A:AppMeasurement v1.6의 유일한 변경 사항은 페이지 이름, 링크 ID 및 RegionID의 컬렉션을 필요로 하는 Activity Map 링크 추적 프로세스 방법론입니다.

**Q:AppMeasurement는 특정 페이지가 아닌 도메인 수준에서 롤아웃됩니까?**

A:AppMeasurement는 보고서 세트 수준에서 롤아웃됩니다. 보고서 세트 수준은 일반적으로 도메인 수준과 연관되지만, 각 구현과 다릅니다.

**Q:DTM은 Activity Map이 원하는 버전(1.5.1)보다 이전 버전의 방문자 API를 자동으로 로드합니다. 이게 문제인가요?**

A: 아니요. Activity Map 기능은 VisitorAPI에 종속되지 않습니다.

## Activity Map 애플리케이션

<!--**Q: How does Activity Map support Single-Page Applications (SPA)?**

A: 

* Every few seconds, Activity Map scans the web page, looking for changes to the page. ActivityMap finds new content on the page without needing a new page load, but this new content is always attributed to the first pageName found when the page loaded.

* Activity Map checks to see if the visibility of links that it knows about has changed. If a change in visibility is found, then the [Links On Page](/help/analyze/activity-map/activitymap-links-report.md) table's Present column for that link updates with **[!UICONTROL Displayed]** or **[!UICONTROL Hidden]**.

* When user interaction creates new content, any new elements that are found by AppMeasurement to be a link will be added to the **[!UICONTROL Links On Page]** table. Activity Map sends a new data request that includes these new links. The new links should appear in the **[!UICONTROL Links On Page]** table when the data request is handled by the UI.-->

**Q:Activity Map은 &quot;보기&quot; 데이터를 제공합니까?**

A:아니요. Adobe는 본 링크를 추적하지 않습니다.

**Q:이전에 웹 사이트에서 방문자 ClickMap을 사용하지 않은 경우 Activity Map을 사용할 수 있습니까?**

A:이전 버전(이제 ClickMap이라고 함)이 설치되어 있는 것은 새 버전을 구현하기 위한 전제 조건이 아닙니다. Adobe는 제한된 기간 동안 이전 버전을 계속 지원할 예정입니다.

**Q:Activity Map에서는 어떤 브라우저와 버전을 지원합니까?**

A:Adobe는 최신 버전의 4개의 기본 브라우저(Chrome, Firefox, Safari 및 IE)를 지원합니다.

**Q:기본 오버레이 설정이란 무엇입니까?**

A:기본적으로 Activity Map은 데이터를 수집한 모든 링크를 표시합니다.

팝업 패널이 고객 웹 페이지의 맨 위에 표시되면 팝업 패널 아래에 있는 링크에 속하는 오버레이가 팝업 패널 상단에 표시될 수 있습니다.

**Q:일부 등급 항목 오버레이가 없는 이유는 무엇입니까?**

A:일부 등급 링크는 페이지에서 숨겨져 있을 수 있습니다(예: 하위 메뉴 링크). 따라서 해당 링크 오버레이는 표시되지 않습니다. 따라서 등급은 페이지의 모든 링크(현재 링크 + 숨겨진 링크)에 대해 계산되므로 일부 특정 등급 값이 없는 오버레이 등급이 표시될 수 있습니다.

**Q:모든 링크 보고서에서 링크 등급은 어떻게 결정됩니까?**

* 그라데이션 **및** 버블 **모드에서** :등급은 지표 열에 의해 결정됩니다. 동일한 지표 값이 있는 링크의 경우 등급은 링크 ID 알파벳순을 기반으로 합니다.
* 승자 **및 패자** 모드에서 등급은 주로 % 게인 열에 의해 결정됩니다. 동일한 게인이 있는 링크의 경우 등급은 링크 ID 알파벳순을 기반으로 합니다.

**Q:Activity Map이 실행 중일 때 링크 클릭 데이터가 수집되지 않는 이유는 무엇입니까?**

A:Activity Map이 사용 중인 동안에는 링크 클릭 데이터가 Analytics 태그로 수집되지 않습니다. 이 동작은 ClickMap 플러그인의 동작을 따릅니다.

**Q:Activity Map 모든 링크 보고서는 보고 및 분석 Activity Map 보고와 어떻게 비교합니까?**

A: Activity Map에서 모든 링크 보고서를 가져오기 위해 다음과 같이 분류 요청을 만듭니다. Activity Map 페이지 = &quot;visitedpage&quot;, `<list of link&regions present in the page at rendering time>`에서 Activity Map 링크 및 지역으로 분류됩니다.

보고 및 분석에서 상응하는 보고서를 얻으려면 먼저 Activity Map 페이지 보고서로 이동해야 합니다. 여기에서 Activity Map에서 방문한 페이지 이름을 필터링합니다. 방문한 페이지 이름은 Activity Map 페이지 세부 사항 하단 패널의 왼쪽 열에 표시됩니다. 페이지가 발견되면 해당 페이지에서 분류하고 Activity Map 링크 및 지역을 보조 차원으로 선택할 수 있습니다.

그러나 R&amp;A에서 얻은 보고서에는 해당 페이지에 대해 수집된 모든 링크 및 지역이 나열됩니다. 그러나 Activity Map은 현재 웹 페이지에 있는 링크 및 지역에 대해서만 보고합니다. 따라서 뉴스 사이트가 있다면, 그것은 이 시간에 있는 뉴스 스토리에 대한 데이터만 보여주며, 그 날 일찍 있었던 뉴스 스토리는 표시하지 않습니다.

**Q:Activity Map은 여러 보고서 세트를 나열하는 여러 태그가 포함된 페이지에서 어떻게 작동합니까?**

A:기본적으로 Activity Map에서는 페이지에서 보낸 첫 번째 태그와 연결된 보고서 세트를 사용합니다. Activity Map 설정 > 기타 탭을 통해 서로 다른 태그가 지정된 보고서 세트를 선택할 수 있습니다.

**Q:Activity Map은 Analytics 태그를 얼마나 오랫동안 스캔합니까?**

A:페이지 전체 이벤트 후 최대 20초 동안 Analytics 태그를 검색합니다.

**Q:Activity Map은 다이내믹 컨텐츠를 어떻게 처리합니까?**

A:Activity Map은 2초마다 다음과 같은 웹 페이지의 상태에 변경 사항이 있는지 확인합니다.

* 표시되는 HTML 컨텐츠
* 숨겨진 HTML 컨텐츠
* 삽입된 새 HTML 컨텐츠

컨텐츠가 숨겨지거나 표시되는 경우, 애플리케이션이 영향을 받는 링크 상태를 숨김에서 표시 또는 표시에서 숨김으로 자동으로 변경합니다(따라서 오버레이).

새 컨텐츠가 주입되면 애플리케이션은 연결된 링크를 검색하고, 해당 링크에 대한 분석 데이터를 가져오고, 이러한 링크에 대한 오버레이를 추가합니다.

**Q:페이지 흐름 보고서는 어떤 지표를 기반으로 합니까?**

A:표시된 모든 데이터는 페이지 보기를 기반으로 합니다.

**Q:다양한 유형의 페이지에서 Activity Map 행동을 설명할 수 있습니까?**

*Analytics 태그가 없는 웹 페이지*

도구 모음 아래에 태그가 없음을 나타내는 경고 메시지가 표시됩니다.

*호환되지 않는 Analytics 태그가 있는 웹 페이지(AppMeasurement v1.5 이하)*

페이지 코드를 v1.6 이상으로 업그레이드해야 함을 나타내는 경고 메시지가 표시됩니다.

*호환하는 Analytics 태그(AppMeasurement v1.6 이상)가 있지만, 관리 도구에 Activity Map 보고가 활성화되어 있지 않은 웹 페이지*

관리자에게 \[Activity Map 보고서를 활성화\](/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md&quot;) 하도록 요청해야 한다고 알려주는 경고 페이지가 표시됩니다.

**Q:[Analytics 데이터 피드](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-overview.html)를 통해 Activity Map 데이터(contextData)를 내보낼 수 있습니까?**

A: 아니요.

## Activity Map의 세그멘테이션

**Q:세그먼트가 개별 사용자 세그먼트에 연결되어 있습니까? Activity Map에서 공유 세그먼트를 사용할 수 있습니까?**

A:Activity Map은 Analytics에서 보고 세그먼트를 상속합니다.

**Q:세그먼트가 라이브 모드에서 작동합니까?**

A:아니요. 세그먼트는 라이브 모드에서 작동하지 않습니다. 이 기능은 보고 및 분석의 실시간 보고 기능과 같습니다.

## 가상 보고서 세트

**Q:Activity Map은 가상 보고서 세트와 호환됩니까?**

A: 예. 하지만 가상 보고서 세트 제한으로 인해 Activity Map의 라이브 모드는 가상 보고서 세트와 호환하지 않습니다.
