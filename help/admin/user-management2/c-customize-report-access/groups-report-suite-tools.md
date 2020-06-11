---
description: API 액세스, 보고서 세트 관리, 도구 및 보고서, 대시보드 항목에 대한 사용자 권한을 활성화합니다.
keywords: groups;permissions
subtopic: Users and groups
title: 보고서 세트 도구 권한 사용자 지정
topic: Admin tools
uuid: 3c95d296-ffd0-4971-9c5f-110ddbe042ce
translation-type: tm+mt
source-git-commit: 6fc8145d9a94427ec942d55776b6029f7dd6f79c
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 93%

---


# 보고서 세트 도구 권한 사용자 지정

>[!IMPORTANT]
>
>사용자 및 제품 관리를 [Admin Console](https://helpx.adobe.com/kr/enterprise/using/admin-console.html)로 이동 중입니다. Adobe는 사용자를 마이그레이션할 때가 되면 통지합니다. 모든 고객이 마이그레이션되면 **[!UICONTROL Analytics]** > **[!UICONTROL 관리 도구]** > **[!UICONTROL 사용자 관리]**&#x200B;에 대한 도움말 컨텐츠가 사용되지 않습니다.

API 액세스, 보고서 세트 관리, 도구 및 보고서, 대시보드 항목에 대한 사용자 권한을 활성화합니다.

**[!UICONTROL 사용자 관리]** > **[!UICONTROL 그룹]** > **[!UICONTROL 보고서 액세스]** > **[!UICONTROL 보고서 세트 도구]** > **[!UICONTROL 사용자 지정]**

[!UICONTROL 보고서 세트 도구 사용자 지정] 페이지에서 그룹 구성원에게 다음 항목에 대한 액세스 권한을 제공합니다.

![](assets/report-suite-tools.png)

## 필드 설명

이 페이지의 설정은 [!UICONTROL 사용자 그룹 정의] 페이지에서 선택한 보고서 세트와 관련된 것입니다.

| 요소 | 설명 |
|--- |--- |
| **웹 서비스** |  |
| 이러한 설정을 사용하여 사용자가 Data Warehouse 메서드를 호출하고 보고서 세트 설정을 가져올 수 있습니다. |  |
| Data Warehouse | 관리자가 아닌 사용자가 웹 서비스 API를 통해 Data Warehouse 메서드를 사용하여 호출할 수 있도록 허용합니다. [Data Warehouse - 개발자 설명서](/help/export/data-warehouse/data-warehouse.md) 참조 |
| 보고서 세트(읽기) | 관리자가 아닌 사용자가 API에서 보고서 세트 메서드를 사용할 수 있도록 허용합니다. |
| 보고서 세트(쓰기) | 관리자가 아닌 사용자가 API에서 보고서 세트 메서드를 사용할 수 있도록 허용합니다. |
| **보고서 세트 관리** |  |
| 이러한 설정은 관리자 > 보고서 세트  >  설정 편집([보고서 세트 관리자](/help/admin/c-manage-report-suites/report-suites-admin.md))의 메뉴 항목에 대한 액세스 권한을 부여합니다. |  |
| [트래픽 관리](/help/admin/c-traffic-management/traffic-management.md) | 트래픽 관리에 대한 권한을 부여합니다. |
| [보고서 세트 관리](/help/admin/c-manage-report-suites/report-suites-admin.md) | 보고서 세트를 관리할 권한을 부여합니다. |
| [계정 요약](/help/admin/admin/general-acct-settings-admin.md) | 보고서 세트에 대한 계정 설정을 편집할 권한을 부여합니다. |
| [URL 필터](/help/admin/admin/internal-url-filter-admin.md) | 보고서 세트의 내부 URL 필터에 대한 권한을 부여합니다. 내부 URL 필터는 어느 레퍼러 또는 참조 페이지가 사이트 내부인지 결정하는 데 사용됩니다. |
| [사용자 지정 달력](/help/admin/admin/custom-calendar.md) | 사용자 지정 달력을 편집할 권한을 부여합니다. |
| [유료 검색](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) | 유료 검색 감지는 검색 엔진 및 검색 키워드 보고서에서 유료 검색과 자연어 검색을 구별합니다. |
| [메뉴 사용자 지정](/help/admin/admin/customize-menus.md) | Reports &amp; Analytics에 표시되는 보고서 메뉴를 사용자 지정합니다. |
| [실시간 보고서 구성](/help/admin/admin/realtime/t-realtime-admin.md) | 실시간 보고서 Analytics를 설정하는 권한입니다. |
| [비디오 설정](/help/admin/admin/video-management.md) | 일련의 사용자 지정 전환 변수(eVar)와 사용자 지정 이벤트를 비디오 추적 및 보고용으로 지정하는 권한입니다. |
| [비디오 분류](https://docs.adobe.com/content/help/ko-KR/media-analytics/using/media-overview.html) | 일련의 사용자 지정 전환 변수(eVar)와 사용자 지정 이벤트를 비디오 추적 및 보고용으로 지정하는 권한입니다. |
| [트래픽 변수](/help/admin/admin/c-traffic-variables/traffic-var.md) | 특정 트래픽 관련 이벤트와 사용자 지정 데이터를 관련 지을 권한입니다. |
| [트래픽 분류](/help/admin/admin/c-traffic-variables/traffic-classifications.md) | 분류([도구 및 보고서] 아래에 있음)로 통합되었습니다. |
| [채널](/help/components/c-marketing-channels/analyze-mc.md) | 보고서 세트 관리자 > 설정 편집 > 마케팅 채널의 마케팅 채널 설정에 대한 권한을 부여합니다. |
| [비용](https://docs.adobe.com/content/help/ko-KR/analytics/components/marketing-channels/analyze-mc.html) | 보고서 세트 관리자에서 마케팅 채널 > 마케팅 채널 비용에 대한 권한을 사용하도록 설정합니다. |
| [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) | 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다. |
| [검색 방법](/help/admin/admin/finding-methods.md) | 여러 검색 방법 보고서가 사용자 사이트에서 전환 성공 이벤트에 대한 크레딧을 받는지 확인할 수 있습니다. |
| [전환 분류](/help/admin/admin/conversion-var-admin/conversion-classifications.md) | 분류([도구 및 보고서] 아래에 있음)로 통합되었습니다. |
| [고유 방문자 수](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/unique-visitor-variable/t-unique-visitor-variable.html) | 고유한 방문자 변수를 지정할 권한을 부여합니다. |
| [성공 이벤트](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/success-events/success-event.html) | 제품 보기, 체크아웃 및 구매처럼 추적이 가능한 작업입니다. |
| [분류 계층](/help/components/c-classifications2/classification-hierarchies.md) | 분류([도구 및 보고서] 아래에 있음)로 통합되었습니다. |
| [목록 변수](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/vars/page-vars/page-variables.html) | List Var라고도 합니다. 목록 Prop과 마찬가지로 목록 변수는 같은 이미지 요청에서 여러 값을 사용할 수 있도록 허용합니다.  |
| [기본 지표](/help/admin/admin/default-metrics.md) | 사용자가 사용자 지정 지표 세트를 선택하지 않는 경우 Reports &amp; Analytics 기능은 모든 전환 보고서에 기본 지표 세트를 표시합니다. 선택된 지표가 연관된 보고서 세트의 모든 사용자에게 표시됩니다. |
| [처리 규칙](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/processing-rules/processing-rules.html) | 데이터 수집을 단순화하고 보고서로 전송되는 대로 콘텐츠를 관리하는 처리 규칙에 대한 액세스 권한을 부여합니다. |
| **도구 및 보고서** |  |
| [예외 항목 탐지](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) | 주어진 지표가 이전 데이터와 관련하여 어떻게 변했는지 파악하는 통계적 방법을 제공하는 예외 항목 탐지에 대한 권한을 부여합니다. |
| [채널 보고서](/help/components/c-marketing-channels/analyze-mc.md) | 보고서 > 마케팅 채널 보고서에 있는 마케팅 채널 보고서에 대한 권한을 부여합니다. |
| [실시간 보고서](/help/admin/admin/realtime/t-realtime-admin.md) | 실시간 보고서에 대한 액세스 권한을 부여합니다. |
| [보트 페이지](/help/admin/admin/bot-removal/bot-rules.md) | **참고: 보트 페이지는 특정 보고 및 분석 보고서용이지 보트 규칙 관리용이 아닙니다. 현재 보트 규칙 편집을 허용할 권한이 없습니다.**&#x200B;보트 규칙을 사용하여 알려진 스파이더 및 보트가 생성하는 트래픽을 보고서 세트에서 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트에서 사용자 활동을 더 정확하게 측정할 수 있습니다. |
| [보트](/help/admin/admin/bot-removal/bot-rules.md) | **참고: 보트는 특정 보고 및 분석 보고서용이지 보트 규칙 관리용이 아닙니다. 현재 보트 규칙 편집을 허용할 권한이 없습니다.** 보트를 사용하면 알려진 스파이더 및 보트가 생성하는 트래픽을 보고서 세트에서 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트에서 사용자 활동을 더 정확하게 측정할 수 있습니다. |
| [사용자 지정 데이터 웨어하우스 보고서](/help/export/data-warehouse/data-warehouse.md) | Data Warehouse는 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 지정 보고서에 대한 원시의 처리되지 않은 데이터 사본을 참조합니다. 특별한 질문에 따라 원시 데이터의 고급 데이터 관계를 표시하는 보고서를 요청할 수 있습니다. |
| 일별 재방문 | 특정 날짜에 웹 사이트에 여러 번 방문한 방문자의 수를 보여주는 보고서. 하루는 마지막 24시간으로 정의됩니다. |
| [데이터 소스 관리자](/help/admin/admin/data-sources.md) | 데이터 소스 기능을 사용하면 오프라인 소스의 데이터를 Analytics로 가져올 수 있습니다. |
| [IP 주소별로 제외](/help/admin/admin/exclude-ip.md) | 보고서에서 내부 웹 사이트 활동, 사이트 테스트 및 직원 사용과 같은 특정 IP 주소의 데이터를 제거할 수 있습니다. |
| 기존 ClickMap | 기존 ClickMap 오버레이 도구의 메뉴에 대한 액세스 권한을 부여합니다. |
| 기존 Clickmap 설치 | 기존 ClickMap 도구에 대한 설치 권한을 부여합니다. |
| 재방문 | 방문 번호가 1보다 큰 방문의 수를 표시하는 보고서입니다. 재방문 보고서에는 비쿠키 방문자도 포함됩니다. |
| [분류 가져오기](https://docs.adobe.com/content/help/ko-KR/analytics/components/classifications/classifications-importer/c-working-with-saint.html)/내보내기 및 [규칙 빌더](https://docs.adobe.com/content/help/ko-KR/analytics/components/classifications/classifications-rulebuilder/classification-rule-builder.html) | 분류로 통합되었습니다(아래 참조). |
| 데이터 피드 관리자 | 권한을 Analytics 데이터 피드. |
| 분류 | 다음 &#39;트래픽 분류&#39;, &#39;비디오 분류&#39;, &#39;전환 분류&#39;, &#39;분류 계층&#39;, &#39;분류 관리자&#39; 및 &#39;분류 가져오기/내보내기 및 규칙 빌더&#39; 권한을 결합합니다.  참고:  이 권한을 사용하여 사용자는 선택한 세트뿐만 아니라 모든 보고서 세트에 대한 분류를 편집합니다. |
| [기여도 분석](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) | Analysis Workspace에서 기여도 분석을 사용할 수 있는 권한을 부여합니다. |
| **대시보드 항목** |  |
| 대시보드 항목의 설정을 사용하면 Reports &amp; Analytics에서 내 권장 보고서, 회사 요약 리포트릿, 이미지, KPI/측정 리포트릿, 보고서 세트 합계, 텍스트, 리포트릿, 사용 요약 리포트릿 및 웹 리소스 등의 [리포트릿](https://docs.adobe.com/content/help/ko-KR/analytics/admin/server-call-usage/server-call-usage-dashboard.html)에 액세스할 수 있습니다. |  |
| **기타** |  |
| 소셜 | 보고서 세트 관리자의 소셜 관리 메뉴에 대한 액세스를 제어합니다. |
