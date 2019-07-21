---
description: Adobe Analytics 사용을 시작하는 방법
keywords: Analysis Workspace
seo-description: Adobe Analytics 사용을 시작하는 방법
seo-title: 시작 안내서
solution: Analytics
title: 시작 안내서
topic: Reports & Analytics
uuid: 851 feadb -5 e 30-45 ab -9 f 66-02 bdf 844 fa 54
translation-type: tm+mt
source-git-commit: a0158b98089c044091f61796d782604865aa4eba

---


# Analysis Workspace

Analysis Workspace는 조직을 위한 실행 가능한 데이터 기반 결정을 내리기 위한 Adobe의 대표적인 도구 중 하나입니다. 가장 일반적인 시각화인 자유 형식 테이블을 사용하면 차원, 지표, 세그먼트 및 날짜 범위를 사용하여 사용자 지정된 보고서를 쉽게 만들 수 있습니다.

## 전제 조건

[Adobe Experience Platform Launch를 사용하여 Adobe Analytics로 데이터를 전송합니다](../../implement/implement-with-launch/validate-publish-prod.md). 분석 작업 공간을 사용하려면 작업 구현이 필요합니다. 조직에서 도구를 사용하기 전에 Adobe에 데이터를 보내고 있는지 확인합니다. DTM 또는 이전 수동 구현과 같은 다른 구현도 사용할 수 있습니다.

## 작업 공간에서 기본 등급 보고서 가져오기

분석 작업 공간을 사용하여 기본 등급 보고서를 가져옵니다. 등급 보고서는 각 차원 값의 합계 보기를 보여주며 가장 큰 값을 먼저 표시합니다. 이러한 유형의 보고서는 가장 많은 트래픽을 얻는 페이지 또는 가장 많이 판매되는 제품 등 사이트의 어떤 구성 요소가 가장 효과적인지 확인하는 데 유용합니다.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
2. 오른쪽 상단의 9 개 사각형 아이콘을 클릭한 다음 컬러 분석 로고를 클릭합니다.
3. 위쪽 탐색 모음에서 작업 영역을 클릭합니다.
4. ' 새 프로젝트 만들기'버튼을 클릭합니다.
5. 모달 팝업에서'빈 프로젝트'가 선택되어 있는지 확인한 다음 만들기를 클릭합니다.
6. 왼쪽에는 차원, 지표, 세그먼트 및 날짜 범위에 대한 목록이 표시됩니다. 페이지 차원 (주황색) 를 찾아 캔버스로 드래그하여'여기에 차원 놓기'라고 적혀 있는 캔버스로 드래그합니다.
7. 보고서 세트에 데이터가 있으면 이 달의 최상위 페이지를 보여주는 보고서가 표시될 수 있습니다. Analysis Workspace automatically populated the report with the [Occurrences](../../components/c-variables/c-metrics/metrics-occurrences.md) metric.
8. Locate the Visits metric (colored green), and drag it either **over** or **next to** the Occurrences metric header (avoid placing it above the metric). 방문 횟수 지표에 방문 횟수 지표를 드래그하면 지표가 보고에서 대체됩니다. 발생 횟수 옆에 있는 방문 횟수 지표를 드래그하면 두 지표 모두 나란히 표시됩니다.
9. If you'd like to save your project, click *[!UICONTROL Project]&gt;[!UICONTROL Save]* in the upper left menu.

## 작업 공간에서 기본 트렌드 보고서 가져오기

분석 작업 공간을 사용하여 기본 트렌드 보고서를 가져옵니다. 트렌드 보고서는 선택한 날짜 범위를 사용하는 지표의 기간 보기를 보여줍니다. 이러한 유형의 보고서는 시간에 따른 트렌드를 식별하는 데 유용하며, 비즈니스 의사 결정의 성공 또는 실패를 측정하는 데 사용할 수 있습니다. 예를 들어 시간 경과에 따른 페이지 뷰 수를 확인하여 사이트 재디자인이 트래픽 증가 또는 감소를 지원하는지 확인할 수 있습니다.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
2. 오른쪽 상단의 9 개 사각형 아이콘을 클릭한 다음 컬러 분석 로고를 클릭합니다.
3. 위쪽 탐색 모음에서 작업 영역을 클릭합니다.
4. ' 새 프로젝트 만들기'버튼을 클릭합니다.
5. 모달 팝업에서'빈 프로젝트'가 선택되어 있는지 확인한 다음 만들기를 클릭합니다.
6. 왼쪽에는 차원, 지표, 세그먼트 및 날짜 범위에 대한 목록이 표시됩니다. 페이지 보기 차원을 찾아'여기에 지표 놓기'레이블이 지정된 캔버스의 작은 공간으로 드래그합니다. 공간이 예약된 공간에 드롭하지 마십시오 (이 연습).
7. 보고서 세트에 데이터가 있으면, 기본 페이지 보기 보고서 트렌드가 현재 달에 걸쳐 표시됩니다. 분석 작업 공간은'날짜'날짜 범위에서 자동으로 표시되므로 현재 월의 페이지 보기 트렌드를 볼 수 있습니다.
8. 왼쪽의 날짜 범위 구성 요소 목록에서 주 날짜 범위 (컬러 자주색) 를 찾습니다. 날짜 범위 제목을 클릭하여 모든 날짜 범위 구성 요소를 확장하거나 보거나 검색 막대를 사용합니다.
9. 캔버스의 날짜 범위 범위 머리글에서 주 날짜 범위를 드래그하여 바꿀 수 있습니다.
10. 트렌드 보고서는 이제 일 대신 주 단위로 집계됩니다.
11. If you'd like to save your project, click *[!UICONTROL Project]&gt;[!UICONTROL Save]* in the upper left menu.

## 툴 사용

분석 작업 공간은 보고 도구이므로 데이터 수집에는 영향을 주지 않습니다. 어떤 효과가 있는지 보기 위해 구성 요소를 프로젝트로 과도하게 드래그하는 데에는 불합리한 영향이 없습니다. 차원 및 지표 조합을 작업 영역 프로젝트로 드래그하여 사용할 수 있는 항목을 확인합니다.

실수로 잘못된 구성 요소를 작업 영역 프로젝트로 드래그하거나 단계로 돌아가려면 Ctrl + Z (Windows) 또는 Cmd + Z (Mac) 를 눌러 마지막으로 수행한 작업을 실행 취소합니다. You can also start with a clean slate by clicking *[!UICONTROL Project]&gt;[!UICONTROL New]* in the upper left menu.

## 문제 해결

**지표를 위로 드래그하면'잘못된 데이터'가 표시됩니다.**

잘못된 데이터는 Adobe가 보고서에 사용된 차원 및 지표의 조합을 사용하여 데이터를 반환하지 않는다는 것을 의미합니다. 예를 들어 두 개의 지표를 서로 겹쳐 스택된 지표는 두 가지 지표를 표시하는 방법은 없으므로 데이터로 돌아갈 수 없습니다. 대신 지표를 나란히 배치하십시오.

**지표를 드래그하면 실제 데이터가 표시되지 않고 0만 표시됩니다.**

작업 공간 보고서를 성공적으로 만들었지만 데이터가 없는 경우 몇 가지 사항이 있습니다.

* 보고서 세트를 두 번 확인하고 데이터가 데이터로 채워졌는지 확인합니다.
* 보고서에서 세그먼트를 사용하는 경우 세그먼트 기준이 데이터와 일치하지 않을 수 있습니다. 세그먼트를 제거하거나 세그먼트 정의를 조정해 보십시오.
* 오른쪽 상단의 날짜 범위를 확인하고 예상한 값으로 설정되었는지 확인합니다.
* 웹 사이트로 이동하고 디버거를 사용하여 데이터가 수집되고 있는지 확인합니다.

## 추가 리소스

* [분석 작업 공간 릴리스 노트](../../analyze/analysis-workspace/new-features-in-analysis-workspace.md): 툴에 도입된 최신 기능을 살펴보십시오.
* [YouTube의 분석 작업 공간](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): 이 광범위한 재생 목록을 통해 분석 작업 공간에서 대부분의 기능을 사용하는 방법을 알아봅니다.
* 제품 내 팁: 짧은 비디오와 함께 짧은 시간 안에 분석 작업 공간의 오른쪽 하단에 나타나는 팁입니다. If these tips are dismissed, they can be reached through *[!UICONTROL Help]&gt;[!UICONTROL Tips]* at any time.
* [분석 작업 공간 커뮤니티](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace): 동료 사용자와 분석 작업 공간에 대해 토론하고 도구에서 보고 싶은 기능에 대해 투표합니다.
* 블로그 게시물:
   * [발전된 지능형 분석으로 조직 지원](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [강력한 통찰력을 제공하는 새로운 Adobe Analytics 기능](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/)
   * [분석 작업 공간에서 생산성을 극대화할 수 있는 5 가지 팁](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/)
   * [분석 작업 공간에서 더욱 빨라진 인사이트](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/)
   * [Analysis Workspace을 사용해야 하는 이유](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)

## 다음 단계

분석 작업 공간에 대한 이해를 높이려면 다양한 지침이 있습니다. 다음은 Adobe에서 권장하는 기본 사항입니다.

### 분석 작업 공간을 사용하는 방법에 대한 지식을 확장하려는 최종 사용자

* [작업 영역 UI에 대한 자세한](../../analyze/analysis-workspace/build-workspace-project/t-freeform-project.md)내용: 이제 기본 보고서를 만들었으므로 인터페이스의 나머지 부분에 더 익숙해지십시오.
* [작업 영역의 시각화](visualizations/freeform-analysis-visualizations.md): 자유 형식 테이블은 분석 작업 공간에서 한 가지 시각화 유형일 뿐입니다. 라인 차트, 막대 그래프 및 지리 맵과 같은 다른 시각화를 사용하는 방법을 알아봅니다.
* [작업 공간의 차원](../../analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): 차원에 대한 자세한 내용과 단순한 보고서 이상의 보고서에서 사용하는 방법에 대해 자세히 알아보십시오.
* [작업 공간의 지표](../../analyze/analysis-workspace/components/apply-create-metrics.md): 지표에 대한 자세한 내용과 자유 형식 테이블의 다른 부분에서 지표를 사용하는 방법에 대해 알아보십시오.
* [세그멘테이션 소개](../../analyze/analysis-workspace/components/t-freeform-project-segment.md): 세그먼트에 대해 알아보고 세그먼트를 사용하여 기본 보고서를 가져옵니다.
* [작업 공간의 날짜 범위](../../analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): 상대적 및 연속 날짜에 대해 알아보고 작업 영역 프로젝트에서 사용합니다.
* 작업 공간에서 프로젝트 공유: 동료에게 멋진 작업 영역 프로젝트 제시
* [(고급) 작업 영역의 패널](c-panels/panels.md): 기여도 분석 및 세그먼트 비교 등 작업 영역의 고급 기능을 사용할 수 있습니다.

### 조직 내의 작업 영역 품질을 향상시키고자 하는 애널리스트 및 관리자에게는

* [분석 작업 공간 권한](https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html): Adobe Admin Console를 통해 작업 공간에 사용자 권한을 할당할 수 있습니다.
* [솔루션 디자인 문서 만들기](../../implement/prepare/solution-design.md): 조직에서 사이트에 대한 추가 차원이나 지표를 수집하는 방법을 계획합니다.
* [작업 공간의 템플릿](../../analyze/analysis-workspace/build-workspace-project/starter-projects.md): 템플릿을 만들어 동료에게 자신의 요구 사항에 맞는 프로젝트 공간을 제공할 수 있습니다.
* [작업 영역 조정](curate-share/curate.md): 사용 가능한 구성 요소를 제한하는 프로젝트를 제작하여 도구에 익숙하지 않은 사용자도 작업 영역을 보다 쉽게 액세스 가능