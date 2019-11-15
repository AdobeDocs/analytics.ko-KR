---
description: Adobe Analytics를 시작하는 방법
keywords: Analysis Workspace
solution: Analytics
title: 시작 안내서
topic: Reports and analytics
uuid: 851feadb-5e30-45ab-9f66-02bdf844fa54
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analysis Workspace

Analysis Workspace는 Adobe의 대표적인 툴 중 하나로, 조직에서 실행 가능한 데이터 기반 의사 결정을 내릴 수 있습니다. 가장 일반적인 시각화인 자유 형식 테이블을 사용하면 차원, 지표, 세그먼트 및 날짜 범위를 사용하여 사용자 지정된 보고서를 쉽게 만들 수 있습니다.

## 전제 조건

[Adobe Experience Platform Launch를 사용하여 Adobe Analytics로 데이터 보내기](/help/implement/implement-with-launch/validate-publish-prod.md):분석 작업 공간을 사용하려면 작업 구현이 필요합니다. 조직에서 도구를 사용하기 전에 데이터를 Adobe로 보내야 합니다. DTM 또는 이전 수동 구현과 같은 다른 구현도 작동할 수 있습니다.

## 작업 공간에서 기본 등급 보고서 가져오기

분석 작업 공간을 사용하여 기본 등급 보고서를 가져옵니다. 등급 보고서는 각 차원 값의 집계된 전체 보기를 보여주며 가장 큰 값을 먼저 표시합니다. 이러한 유형의 보고서는 트래픽이 가장 많은 페이지 또는 가장 많이 판매되는 제품과 같이 사이트의 구성 요소가 가장 효과적인지 확인하는 데 유용합니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
3. 상단 탐색 막대에서 [작업 영역]을 클릭합니다.
4. '새 프로젝트 만들기' 버튼을 클릭합니다.
5. 모달 팝업에서 '빈 프로젝트'가 선택되어 있는지 확인하고 만들기를 클릭합니다.
6. 왼쪽의 차원, 지표, 세그먼트 및 날짜 범위 목록이 표시됩니다. 페이지 차원(주황색)을 찾아 캔버스로 드래그하여 '여기에 차원 놓기'라고 표시합니다.
7. 보고서 세트에 데이터가 있으면 이 달의 상위 페이지를 보여주는 보고서를 볼 수 있습니다. 분석 작업 공간은 자동으로 보고서를 발생 [지표로](/help/components/c-variables/c-metrics/metrics-occurrences.md) 채웁니다.
8. 방문 횟수 지표(녹색)를 찾아 발생 지표 헤더 **위** 또는 **옆에** 드래그합니다(지표 위에 두지 않음). 발생 횟수 위에 방문 횟수 지표를 드래그하면 보고서에서 지표가 바뀝니다. 발생 옆에 방문 횟수 지표를 드래그하면 두 지표가 나란히 표시됩니다.
9. 프로젝트를 저장하려면 왼쪽 위 메뉴에서 프로젝트 *[!UICONTROL &gt;]저장을[!UICONTROL 클릭합니다]* .

## 작업 공간에서 기본 트렌드 보고서 가져오기

분석 작업 공간을 사용하여 기본 트렌드 보고서를 가져옵니다. 트렌드 보고서는 선택한 날짜 범위를 사용하는 지표의 시간 보기를 보여줍니다. 이러한 유형의 보고서는 시간에 따른 트렌드를 식별하는 데 유용하며 비즈니스 의사 결정의 성공 또는 실패를 측정하는 데 사용할 수 있습니다. 예를 들어 시간에 따른 트렌드 페이지 보기 보고서에서 사이트 재디자인이 트래픽을 증가시키거나 줄이는 데 도움이 되었는지 확인할 수 있습니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
3. 상단 탐색 막대에서 [작업 영역]을 클릭합니다.
4. '새 프로젝트 만들기' 버튼을 클릭합니다.
5. 모달 팝업에서 '빈 프로젝트'가 선택되어 있는지 확인하고 만들기를 클릭합니다.
6. 왼쪽의 차원, 지표, 세그먼트 및 날짜 범위 목록이 표시됩니다. 페이지 보기 차원을 찾아 '여기에 지표 놓기'라는 레이블이 있는 캔버스의 작은 공간으로 드래그합니다. 차원용으로 예약된 공간에 드롭하지 마십시오(적어도 이 연습에서는).
7. 보고서 세트에 데이터가 있는 경우 현재 달에 대한 기본 페이지 보기 수 보고서가 표시됩니다. 분석 작업 공간이 자동으로 '일' 날짜 범위를 표시하므로 현재 달의 페이지 보기 트렌드를 볼 수 있습니다.
8. 왼쪽의 날짜 범위 구성 요소 목록에서 주 날짜 범위(컬러 자주색)를 찾습니다. 날짜 범위 제목을 클릭하여 모든 날짜 범위 구성 요소를 확장 및 확인하거나 검색 막대를 사용합니다.
9. 캔버스에서 일 날짜 범위 헤더의 맨 위에 있는 주 날짜 범위를 드래그하여 바꿉니다.
10. 이제 트렌드 보고서가 일 대신 주 단위로 집계됩니다.
11. 프로젝트를 저장하려면 왼쪽 위 메뉴에서 프로젝트 *[!UICONTROL &gt;]저장을[!UICONTROL 클릭합니다]* .

## 다양한 툴 사용

분석 작업 공간은 보고 도구이므로 데이터 수집에 영향을 주지 않습니다. 구성 요소를 프로젝트에 드래그하여 어떤 효과가 있는지 확인하는 데에는 아무런 영향이 없습니다. 다양한 차원 및 지표 조합을 작업 영역 프로젝트로 드래그하여 사용할 수 있는 항목을 확인할 수 있습니다.

실수로 잘못된 구성 요소를 작업 영역 프로젝트로 드래그하거나 한 단계로 돌아가려면 Ctrl+Z(Windows) 또는 cmd+Z(Mac)를 눌러 마지막으로 수행한 작업을 취소합니다. 왼쪽 위 메뉴에서 프로젝트 &gt; 새로 만들기를 클릭하여 *[!UICONTROL 처음부터]새로[!UICONTROL 만들기]* 작업을 시작할 수도 있습니다.

## 문제 해결

**지표를 위로 드래그하면 '잘못된 데이터'라고 표시됩니다.**

잘못된 데이터는 Adobe가 보고서에서 사용된 차원 및 지표 조합을 사용하여 데이터를 반환할 수 없음을 의미합니다. 예를 들어, 두 지표를 같은 방식으로 표시하는 방법은 없으므로 두 개의 지표를 데이터로 반환할 수 없습니다. 대신 지표를 나란히 배치합니다.

**지표를 위로 드래그하면 실제 데이터가 표시되지 않습니다. 0만 표시됩니다.**

작업 공간 보고서를 성공적으로 만들었지만 데이터가 없는 경우 다음과 같은 사항을 확인할 수 있습니다.

* 보고서 세트를 다시 확인하고 데이터가 포함된 보고서 세트인지 확인합니다.
* 보고서에서 세그먼트를 사용 중인 경우 세그먼트 기준이 데이터와 일치하지 않을 수 있습니다. 세그먼트를 제거하거나 세그먼트 정의를 조정해 보십시오.
* 오른쪽 상단에서 날짜 범위를 확인하고 예상한 값으로 설정되어 있는지 확인합니다.
* 웹 사이트로 이동하여 디버거를 사용하여 데이터가 수집되고 있는지 확인합니다.

## 추가 리소스

* [분석 작업 공간 릴리스 노트](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md):툴에 도입된 최신 기능을 살펴볼 수 있습니다.
* [YouTube의 분석 작업 공간](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS):이 광범위한 재생 목록을 통해 분석 작업 공간에서 대부분의 기능을 사용하는 방법을 알아봅니다.
* 제품 내 팁:짧은 비디오와 함께 오늘의 팁은 분석 작업 공간의 오른쪽 아래에 종종 나타납니다. 이러한 팁이 종료되면 언제든지 도움말 &gt; *[!UICONTROL 팁을]통해[!UICONTROL 확인할 수]* 있습니다.
* [분석 작업 공간 커뮤니티](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace):다른 사용자와 분석 작업 공간에 대해 토론하고 도구에서 보려는 기능에 대해 투표합니다.
* 블로그 게시물:
   * [발전된 지능형 분석으로 조직 지원](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [새로운 Adobe Analytics 기능을 통해 보다 손쉽게 액세스할 수 있는 강력한 인사이트 제작](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/)
   * [분석 작업 공간에서 생산성 극대화 팁 5](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/)
   * [분석 작업 공간에서 더욱 빨라진 인사이트](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/)
   * [Analysis Workspace을 사용해야 하는 이유](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)

## 다음 단계

분석 작업 공간에 대한 이해도를 높이려면 다양한 방법을 살펴봅니다. 다음은 Adobe에서 권장하는 몇 가지 기본 사항입니다.

### 분석 작업 공간 사용 방법에 대한 지식을 확장하려는 최종 사용자

* [작업 영역 UI에 대한 세부 사항](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md):기본 보고서를 만들었으므로 나머지 인터페이스에 대해 더 잘 알 수 있습니다.
* [작업 영역의 시각화](visualizations/freeform-analysis-visualizations.md):자유 형식 테이블은 분석 작업 공간에서 하나의 시각화 유형에 불과합니다. 라인 차트, 막대 그래프 및 지역 맵과 같은 다른 시각화를 사용하는 방법을 알아봅니다.
* [작업 공간의 차원](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md):차원이 무엇이고 등급 보고서에서만 차원을 사용하는 방법에 대해 자세히 알아보십시오.
* [작업 공간의 지표](/help/analyze/analysis-workspace/components/apply-create-metrics.md):지표의 정의와 자유 형식 테이블의 다른 부분에서 지표를 사용하는 방법에 대해 자세히 알아보십시오.
* [세그멘테이션 소개](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md):세그먼트가 무엇인지 알아보고 세그먼트를 사용하여 기본 보고서를 가져옵니다.
* [작업 공간의 날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md):상대적 날짜와 롤링 날짜에 대해 알아보고 작업 영역 프로젝트에서 사용할 수 있습니다.
* 작업 공간에서 프로젝트 공유:만든 멋진 작업 영역 프로젝트를 동료에게 보여 줍니다.
* [(고급) 작업 영역의 패널](c-panels/panels.md):기여도 및 세그먼트 비교와 같은 작업 공간에서 고급 기능을 사용합니다.

### 조직의 작업 영역 품질을 향상시키려는 애널리스트 및 관리자

* [분석 작업 공간 권한](https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html):Adobe Admin Console을 통해 작업 공간에 사용자 권한을 할당할 수 있습니다.
* [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)만들기:조직에서 사이트 고유의 추가 차원이나 지표를 수집하는 방법을 계획합니다.
* [작업 공간의 템플릿](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md):템플릿을 만들어 직장 동료가 자신의 요구 사항에 맞는 프로젝트 공간을 만들 수 있습니다.
* [작업 영역 조정](curate-share/curate.md):사용 가능한 구성 요소를 제한하는 프로젝트를 만들어 도구에 익숙하지 않은 사용자도 작업 영역에 보다 손쉽게 액세스 가능
