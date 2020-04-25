---
description: Adobe Analytics 사용을 시작하는 방법.
keywords: Analysis Workspace
title: 시작 안내서
translation-type: tm+mt
source-git-commit: 825dc13b0294e5a96b30b95f14524175d44c621d

---


# Analysis Workspace

Analysis Workspace는 Adobe의 주요 도구 중 하나로, 조직에서 실행 가능한 데이터 기반 의사 결정을 내리는 데 사용할 수 있습니다. 가장 일반적인 시각화인 자유 형식 테이블을 사용하면 차원, 지표, 세그먼트 및 날짜 범위를 사용하여 사용자 지정된 보고서를 쉽게 만들 수 있습니다.

## 전제 조건

[Adobe Experience Platform Launch를 사용하여 Adobe Analytics에 데이터 보내기](/help/implement/launch/validate-publish-prod.md): Analysis Workspace를 사용하려면 실제로 구현해야 합니다. 도구를 사용하기 전에 조직에서 Adobe에 데이터를 보내도록 하십시오. DTM이나 기존 수동 구현과 같은 다른 구현도 작동할 수 있습니다.

## Workspace에서 기본 등급 보고서 가져오기

Analysis Workspace를 사용하여 기본 등급 보고서를 가져오십시오. 등급 보고서는 각 차원값의 집계된 합계 보기를 가장 큰 값을 먼저 표시하는 방식으로 보여줍니다. 이러한 유형의 보고서는 가장 많은 트래픽을 발생시키는 페이지 또는 가장 많이 팔리는 제품과 같이 사이트의 어떤 구성 요소가 가장 효과적인지를 확인하는 데 유용합니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
3. 맨 위 탐색 막대에서 작업 공간을 클릭합니다.
4. 새 프로젝트 만들기 단추를 클릭합니다.
5. 양식 팝업에서 &#39;빈 프로젝트&#39;가 선택되어 있는지 확인한 다음 만들기를 클릭합니다.
6. 왼쪽에는 차원, 지표, 세그먼트 및 날짜 범위 목록이 표시됩니다. 페이지 차원(주황색으로 표시됨)을 찾아 &#39;차원을 여기에 드래그하여 놓습니다&#39;라는 캔버스에 드래그하여 놓으십시오.
7. 보고서 세트에 데이터가 있는 경우 이달의 상위 페이지를 표시하는 보고서가 표시됩니다. Analysis Workspace가 자동으로 보고서를 [발생 횟수](/help/components/c-variables/c-metrics/metrics-occurrences.md) 지표로 채웠습니다.
8. 방문 횟수 지표(녹색으로 표시됨)를 찾아서 발생 횟수 지표 머리글 **위** 또는 **옆**&#x200B;으로 드래그합니다(지표 위에 놓지 않도록 합니다.). 방문 횟수 지표를 발생 횟수 위에 드래그하면 보고에서 지표가 대체됩니다. 방문 횟수 지표를 발생 횟수 옆으로 드래그하면 두 지표가 나란히 표시됩니다.
9. If you&#39;d like to save your project, click *[!UICONTROL Project]>[!UICONTROL Save]*in the upper left menu.

## Workspace에서 기본 트렌드 보고서 가져오기

Analysis Workspace를 사용하여 기본 트렌드 보고서를 가져오십시오. 트렌드 보고서에는 선택한 날짜 범위를 사용하여 시간 경과에 따른 지표 보기가 표시됩니다. 이러한 유형의 보고서는 시간 경과에 따른 트렌드를 식별하는 데 유용하며, 비즈니스 의사 결정의 성공 또는 실패를 측정하는 데 사용할 수 있습니다. 예를 들어, 사이트 재설계가 트래픽 증가 또는 감소에 도움이 되는지 확인하기 위해 시간 경과에 따른 트렌드가 있는 페이지 보기 횟수 보고서를 확인할 수 있습니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
3. 맨 위 탐색 막대에서 작업 공간을 클릭합니다.
4. 새 프로젝트 만들기 단추를 클릭합니다.
5. 양식 팝업에서 &#39;빈 프로젝트&#39;가 선택되어 있는지 확인한 다음 만들기를 클릭합니다.
6. 왼쪽에는 차원, 지표, 세그먼트 및 날짜 범위 목록이 표시됩니다. 페이지 보기 횟수 차원을 찾아 캔버스에서 &#39;여기에 지표 놓기&#39;라는 레이블이 지정된 작은 공간으로 드래그합니다. 차원용으로 예약된 공간에 놓지 마십시오(적어도 이 연습에서는).
7. 보고서 세트에 데이터가 있는 경우 이번 달 동안의 트렌드가 있는 기본 페이지 보기 횟수 보고서가 표시됩니다. Analysis Workspace는 자동으로 &#39;일&#39; 날짜 범위 기간을 가져오므로 이번 달의 페이지 보기 횟수 트렌드를 볼 수 있습니다.
8. 왼쪽의 날짜 범위 구성 요소 목록에서 주 날짜 범위(보라색으로 표시됨)를 찾습니다. 날짜 범위 제목을 클릭하여 확장하고 모든 날짜 범위 구성 요소를 보거나 검색 창을 사용하십시오.
9. 캔버스에서 일 날짜 범위 머리글 위에 주 날짜 범위를 드래그하여 바꿉니다.
10. 트렌드 보고서는 이제 하루가 아닌 주 단위로 집계됩니다.
11. If you&#39;d like to save your project, click *[!UICONTROL Project]>[!UICONTROL Save]*in the upper left menu.

## 도구 실험

Analysis Workspace는 보고 도구이므로 데이터 수집에는 영향을 주지 않습니다. 구성 요소를 프로젝트에 마구잡이로 드래그하여 놓아서 어떤 것이 효과가 있는지를 확인하는 데에는 아무 영향이 없습니다. 다양한 차원과 지표의 조합을 Workspace 프로젝트에 드래그하여 사용 가능한 조합을 확인하십시오.

실수로 유효하지 않은 구성 요소를 Workspace 프로젝트에 드래그하거나 단계를 다시 수행하려면 Ctrl+Z(Windows) 또는 Cmd+Z(Mac)를 눌러 마지막으로 수행한 작업을 취소하십시오. You can also start with a clean slate by clicking *[!UICONTROL Project]>[!UICONTROL New]*in the upper left menu.

## 문제 해결

**지표를 드래그하면 &#39;잘못된 데이터&#39;라고 표시됩니다.**

잘못된 데이터는 Adobe가 보고서에 사용된 차원과 지표의 조합을 사용하여 데이터를 반환할 수 없음을 의미합니다. 예를 들어, 서로 위에 스택된 두 개의 지표는 이런 식으로 두 개의 지표를 표시할 수 있는 방법이 없으므로 데이터로 반환되지 않습니다. 대신 지표들을 나란히 배치하십시오.

**지표를 드래그하면 실제 데이터가 표시되지 않고, 0만 표시됩니다.**

Workspace 보고서를 생성했지만 데이터가 없다면 확인할 수 있는 몇 가지 사항이 있습니다.

* 보고서 세트를 다시 확인하여 데이터가 채워져 있는지 확인하십시오.
* 보고서에서 세그먼트를 사용하고 있다면 세그먼트 기준이 데이터와 일치하지 않을 수 있습니다. 세그먼트를 제거하거나 세그먼트 정의를 조정해 보십시오.
* 오른쪽 위의 날짜 범위를 확인하고 예상한 값으로 설정되어 있는지 확인하십시오.
* 웹 사이트로 이동하고 디버거를 사용하여 데이터가 수집되고 있는지 확인하십시오.

## 추가 리소스

* [Analysis Workspace 릴리스 노트](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md): 도구에 도입된 최신 기능을 읽어 보십시오.
* [Analysis Workspace - YouTube](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): 이 광범위한 재생 목록을 통해 Analysis Workspace에 있는 대부분의 기능에 대한 사용법을 알아보십시오.
* 제품 내 팁: 간혹 Analysis Workspace의 오른쪽 아래에 오늘의 팁이 짧은 비디오와 함께 나타납니다. If these tips are dismissed, they can be reached through *[!UICONTROL Help]>[!UICONTROL Tips]*at any time.
* [Analysis Workspace 커뮤니티](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace): 동료 사용자와 Analysis Workspace에 대해 토론하고 도구에서 보고 싶은 기능에 투표하십시오.
* 블로그 게시물:
   * [발전된 지능형 분석으로 조직 지원](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [새 Adobe Analytics 기능을 통해 유용한 통찰력을 더욱 쉽게 활용 가능](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/)
   * [Analysis Workspace로 생산성을 극대화하기 위한 5가지 팁](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/)
   * [Analysis Workspace 관련 더 빠른 통찰력](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/)
   * [Analysis Workspace을 사용해야 하는 이유](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)

## 다음 단계

Analysis Workspace를 더 깊이 이해하기 위해서는 살펴볼 측면이 많습니다. Adobe가 권장하는 몇 가지 기본 사항은 다음과 같습니다.

### Analysis Workspace 사용법에 대한 지식을 확장하려는 최종 사용자의 경우

* [Workspace UI에 대한 세부 사항](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md): 이제 기본 보고서를 생성했으므로 나머지 인터페이스에 더 익숙해지도록 합니다.
* [Workspace에서의 시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md): 자유 형식 테이블은 Analysis Workspace에서 시각화의 한 유형일 뿐입니다. 선 차트, 막대그래프 및 지리 지도와 같은 다른 시각화 형태를 사용하는 방법을 알아봅니다.
* [Workspace의 차원](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): 차원의 의미와 등급 보고서 이외에서도 차원을 사용하는 방법에 대해 자세히 알아봅니다.
* [Workspace의 지표](/help/analyze/analysis-workspace/components/apply-create-metrics.md): 지표의 의미와 자유 형식 테이블의 다른 부분에서 지표를 사용하는 방법에 대해 자세히 알아봅니다.
* [세그멘테이션 소개](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md): 세그먼트의 의미에 대해 알아보고 세그먼트를 사용하여 기본 보고서를 가져옵니다.
* [Workspace의 날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): 상대적 날짜와 순환 날짜에 대해 알아보고 Workspace 프로젝트에서 사용합니다.
* Workspace에서 프로젝트 공유: 동료에게 자신이 만든 멋진 Workspace 프로젝트를 보여줍니다.
* [Workspace의 (고급) 패널](/help/analyze/analysis-workspace/c-panels/panels.md): 기여도 분석이나 세그먼트 비교와 같은 Workspace의 고급 기능을 사용합니다.

### 조직에서 작업 영역의 품질을 향상시키고자 하는 분석가 및 관리자

* [Analysis Workspace 권한](https://marketing.adobe.com/resources/help/ko_KR/mcloud/admin_getting_started.html): Adobe Admin Console을 통해 Workspace에 대한 권한을 사용자에게 할당합니다.
* [Workspace의 템플릿](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md): 동료가 자신의 요구에 맞는 프로젝트 공간으로 시작할 수 있도록 템플릿을 만듭니다.
* [Workspace 큐레이션](/help/analyze/analysis-workspace/curate-share/curate.md): 사용 가능한 구성 요소를 제한하는 프로젝트를 만들어 도구에 익숙하지 않은 사람들이 Workspace에 보다 쉽게 액세스할 수 있도록 합니다.
