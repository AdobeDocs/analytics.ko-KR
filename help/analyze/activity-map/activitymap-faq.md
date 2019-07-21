---
description: 'Activity Map 기능의 설정, 구성 및 사용과 관련하여 자주 묻는 질문입니다. '
seo-description: 'Activity Map 기능의 설정, 구성 및 사용과 관련하여 자주 묻는 질문입니다. '
seo-title: Activity Map FAQ
solution: Analytics
title: Activity Map FAQ
topic: Activity Map
uuid: E 4 F 6 D 4 E 2-55 D 1-4 E 32-BF 70-A 334178 AF 370
translation-type: tm+mt
source-git-commit: 8f72f8cf086be0eade5616b074123a9f22e33347

---


# Activity Map FAQ

Activity Map 기능의 설정, 구성 및 사용과 관련하여 자주 묻는 질문입니다. 

## 구현 및 AppMeasurement {#section_FB46DD652E854C07AD339D7DD5CBCEC6}

**Q: 새로운 Activity Map을 활성화하기 위한 구현 절차는 무엇입니까?**

A: [Activity Map 활성화](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**Q: 모든 Analytics 고객이 관리 도구 ActivityMap 지원 페이지에 액세스할 수 있습니까?**

A: Adobe SiteCatalyst 고객은 관리 콘솔의 Activity Map 지원 페이지에 액세스할 수 없습니다. Adobe Analytics Standard 및 Adobe Analytics Premium 계약을 맺은 회사만 이 구성 페이지에 액세스할 수 있습니다.

**Q: 새로운 AppMeasurement 코드는 DTM(다이내믹 태그 관리)을 통해 구성할 수 있습니까?**

A: 예. 새로운 AppMeasurement 코드를 [수동으로 구현](https://marketing.adobe.com/resources/help/en_US/dtm/analytics_dtm.html)할 수 있습니다.

**Q: AppMeasurement v1.6 라이브러리의 큰 변경 사항은 무엇입니까?**

A: AppMeasurement v1.6의 유일한 변경 사항은 페이지 이름, 링크 ID 및 RegionID의 컬렉션을 필요로 하는 Activity Map 링크 추적 프로세스 방식입니다.

**Q: AppMeasurement는 특정 페이지보다는 도메인 수준에서 롤아웃됩니까?**

A: AppMeasurement는 보고서 세트 수준에서 롤아웃됩니다. 보고서 세트 수준은 보통 도메인 수준과 연결되어 있지만, 이것은 각 구현과는 다릅니다.

**Q: DTM은 Activity Map이 원하는 버전(1.5.1)보다 이전 버전(1.3.4)의 방문자 API를 자동으로 로드합니다. 이것이 문제입니까?**

A: 아니요. Activity Map 기능은 방문자 API에 따라 변하지 않습니다.

## Activity Map application {#section_E4F2DAC09EBA4E3BA7BACB49A0A89F8D}

**Q: 이전에 내 웹 사이트에서 Visitor ClickMap을 사용하지 않았어도 Activity Map을 사용할 수 있습니까?**

A: 새 버전을 설치하기 위해 반드시 기존 버전(지금은 간단히 ClickMap이라 함)이 설치되어 있어야 하는 것은 아닙니다. Adobe에서는 제한된 기간 동안 기존 버전을 계속 지원합니다.

**Q: Activity Map에서는 어떤 브라우저 및 버전을 지원합니까?**

A: Adobe에서는 4가지 최신 주요 브라우저 버전(Chrome, Firefox, Safari 및 IE)만 지원합니다.

**Q: 기본 오버레이 설정은 무엇입니까?**

A: 기본적으로 Activity Map에는 데이터를 수집한 모든 링크가 표시됩니다.

팝업 패널이 고객 웹 페이지의 맨 위에 표시되면, 팝업 패널 아래에 있는 링크에 속하는 오버레이가 팝업 패널의 맨 위에 표시될 수 있습니다.

**Q: 왜 일부 등급 항목 오버레이가 누락되어 있습니까?**

일부 등급 링크가 페이지에서 숨겨져 있을 수 있습니다(예: 하위 메뉴 링크). 그 결과 해당 링크 오버레이는 표시되지 않습니다. 따라서 등급은 페이지의 모든 링크(현재 링크 + 숨겨진 링크)에 대해 계산되므로, 일부 특정 등급 값이 없는 오버레이 등급이 표시될 수 있습니다(현재 항목 + 숨겨진 항목).

**Q: 모든 링크 보고서에서 링크 등급은 어떻게 결정됩니까?**

* **그라데이션** 및 **버블** 모드에서 등급은 지표 열에 의해 결정됩니다. 동일한 지표 값이 있는 링크의 경우, 등급은 추가적으로 링크 ID 알파벳순을 기반으로 합니다.
* **승자 및 패자** 모드에서 등급은 주로 % 증가 열로 결정됩니다. 동일한 증가 값이 있는 링크의 경우, 등급은 추가적으로 링크 ID 알파벳순을 기반으로 합니다.

**Q: Activity Map이 실행 중일 때 왜 링크 클릭 데이터가 수집되지 않습니까?**

A: Activity Map이 사용 중이면 링크 클릭 데이터가 Analytics 태그로 수집되지 않습니다. 이 동작은 ClickMap 플러그인의 동작 후 이루어집니다.

**Q: 왜 지표 드롭다운에 동일한 지표가 여러 번 나열됩니까?**

A: Activity Map에서는 모든 보고서 세트에 대한 지표를 나열합니다. 그 결과, 회사가 [지표 통합 프로세스](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/cm_transition.html)를 진행하지 않은 경우 중복 항목이 표시될 수 있습니다.

[지표] 드롭다운을 사용하면 계산된 지표 목록을 방문한 페이지의 보고서 세트에 지정된 지표로 제한할 수 있습니다.

**Q: Activity Map 모든 링크 보고서는 Reports &amp; Analytics Activity Map 보고와 어떻게 비교됩니까?**

A: To pull the All Links Report in Activity Map, we create a breakdown request as follows: Activity Map Page = “visitedpage”, broken down by Activity Map Link&amp;Region in `<list of link&regions present in the page at rendering time>`.

Reports &amp; Analytics에서 상응하는 보고서를 얻으려면, 먼저 Activity Map 페이지 보고서로 이동해야 합니다. 여기에서는 Activity Map에서 방문한 페이지 이름에 대해 필터링하게 됩니다. 방문한 페이지 이름은 Activity Map 페이지 상세정보 하단 패널에서 왼쪽 열에 표시됩니다. 이 페이지를 찾으면, 해당 페이지에서 분류하고, Activity Map 링크 및 지역을 보조 차원으로 선택할 수 있습니다.

하지만, 보고 및 분석에서 획득한 보고서에 해당 페이지에 대해 수집한 모든 링크 및 지역이 나열된다는 것을 주목해야 합니다. 그러나 Activity Map은 웹 페이지에 현재 있는 링크 및 지역에 대해서만 보고합니다. 따라서 뉴스 사이트가 있는 경우에는 이 사이트에 당일 일찍 있었던 뉴스가 아니라, 당시에 있는 뉴스에 대한 데이터가 표시됩니다.

**Q: Activity Map은 여러 보고서 세트를 나열하는 여러 태그가 포함된 페이지에서 어떻게 작동합니까?**

A: 기본적으로 Activity Map에서는 페이지가 보내는 첫 번째 태그와 연결된 보고서 세트를 사용합니다.

Activity Map 설정 &gt; 기타 탭을 통해 서로 다른 태그가 지정된 보고서 세트를 선택할 수 있습니다.

**Q: Activity Map은 Analytics 태그를 얼마나 오래 검사합니까?**

A: Adobe에서는 페이지 완료 이벤트 후 최대 20초 동안 Analytics 태그를 검사합니다.

**Q: Activity Map은 어떻게 다이내믹 컨텐츠를 처리합니까?**

A: Activity Map은 2초마다 다음과 같은 웹 페이지의 상태에 변화가 발견되었는지를 확인합니다.

* 표시된 HTML 컨텐츠
* 숨겨진 HTML 컨텐츠
* 주입된 새 HTML 컨텐츠

컨텐츠가 숨거나 표시되는 경우, 애플리케이션이 영향을 받은 링크 상태를 자동으로 숨김에서 표시로, 또는 표시에서 숨김으로 변경합니다(따라서 오버레이합니다).

새 컨텐츠가 주입되면, 애플리케이션은 연결된 링크를 검색하고, 해당 링크에 대한 분석 데이터를 가져오고 해당 링크에 대한 오버레이를 추가합니다.

**Q: 페이지 흐름 보고서는 어떤 지표를 기반으로 합니까?**

A: 표시된 모든 데이터는 페이지 보기를 기반으로 합니다.

**Q: 다양한 유형의 페이지로 Activity Map 행동을 설정할 수 있습니까?**

*Analytics 태그가 없는 웹 페이지*

도구 모음 아래에 태그가 존재하지 않음을 가리키는 경고 메시지가 표시됩니다.

*호환하지 않는 Analytics 태그(AppMeasurement v1.5 또는 그 이전 버전)가 있는 웹 페이지*

(/home/analyze/activity-map/activitymap-getting-started-admins/activitymap-enable-started-admins-enable. md) 이 페이지 코드를 v 1.6로 업그레이드해야 한다는 경고 메시지가 표시됩니다.

*호환하는 Analytics 태그(AppMeasurement v1.6 이상)가 있는 웹 페이지지만, 관리 도구에 Activity Map 보고가 활성화되어 있지 않았음*

관리자에게\ [Activity Map 보고서 활성화\] (/home/analyze/activity-map/activitymap-getting-started-admins/activitymap-enable-started-admins-enable. md ") 를 요청해야 한다는 경고 메시지가 표시됩니다.

**Q:[Analytics 데이터 피드](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html)를 통해 Activity Map 데이터(contextData)를 내보낼 수 있습니까?**

A: 아니요.

## Activity Map의 세그멘테이션 {#section_44D6C5F59B8542DC8A3AF38BD8078DCA}

**Q: 세그먼트가 개별 사용자 세그먼트에 연결되어 있습니까? 또는 공유된 관리자 수준 세그먼트를 Activity Map에서 사용할 수 있습니까?**

A: Activity Map는 Analytics에서 관리자 수준 세그먼트 (보고 세그먼트) 를 상속받습니다.

**Q: 세그먼트는 라이브 모드에서 작동합니까?**

A: 아니요. 세그먼트는 라이브 모드에서 작동하지 않습니다. 이 기능은 Reports &amp; Analytics의 실시간 보고 기능과 같습니다.

## Virtual report suites {#section_BDB0CA9E732F478EAC349A79753A78DB}

**Q: Activity Map은 가상 보고서 세트와 호환합니까?**

A: 예. 하지만, 가상 보고서 세트 제한 사항으로 인해 Activity Map의 라이브 모드는 가상 보고서 세트와 호환하지 않습니다.
