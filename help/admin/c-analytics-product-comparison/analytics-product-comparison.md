---
description: Analysis Workspace, Reports & Analytics, Ad Hoc Analysis, Report Builder, Data Warehouse 및 Data Workbench의 시스템 요구 사항 및 비교
title: Analytics 제품 비교 및 요구 사항
translation-type: tm+mt
source-git-commit: 9265fb410b20a764ecc86c56b453b045122fcd05
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 86%

---


# Analytics 제품 비교 및 요구 사항

Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis, Report Builder, Data Warehouse 및 Data Workbench의 시스템 요구 사항 및 비교.

사용할 Adobe Analytics 제품에 대해 알아보려면.[여기](/help/admin/c-analytics-product-comparison/which-analytics-tool.md)로 이동합니다.

| 제품 이름 및 도움말 링크 | [Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) | [Reports &amp; Analytics](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/reports-analytics/getting-started.html) | [Ad Hoc Analysis](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/ad-hoc-analysis/adhoc-home.html) | [Report Builder](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/home.html) | [Data Warehouse](https://docs.adobe.com/content/help/ko-KR/analytics/export/data-warehouse/data-warehouse.html) | [Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html) |
|---|---|---|---|---|---|---|
| **액세스 방법** | 강력한 사용자 지정 분석 프로젝트를 구축하고 통찰력을 보여주기 위한 브라우저 솔루션입니다. | 디지털 분석을 위한 브라우저 솔루션입니다. | 고급 디지털 분석용 Java 기반 도구입니다. | R&amp;A 데이터에서 사용자 지정 요청을 작성하고 Microsoft Excel을 사용하여 시각화할 수 있는 Excel 추가 기능입니다. | .csv 형식으로 보고서를 생성하는 브라우저 솔루션입니다. 타블로 형식 파일을 생성할 수 있습니다. | 사용자 지정 속성 모델링, 예측 분석 및 360 고객 분석과 같은 고급 분석용 다중 채널 분석 도구입니다. |
| **보고서 분류** | 제한 없음 | 최대 2개 상관 관계 | 제한 없음 | 최대 2개 상관 관계 | 세그먼트를 기준으로 분류된 완전히 확장된 무제한 분류를 수행합니다. | 제한 없음 |
| **세그먼트 비교** | 제한 없음 | 최대 2개 세그먼트 | 제한 없음 | 제한 없음(데이터 요청 스택) | 1개 세그먼트. 여러 개의(스택) 세그먼트를 지원합니다. | 제한 없음 |
| **행 출력 제한** | 400 | 200 | 50,000 | 50,000 | 제한 없음 | 사용자 지정 가능 |
| ****&#x200B;고유한 값 제한(eVar/ prop 보고서 내) | 500K-2MM | 500K-2MM | 500K-2MM | 500K-2MM | 제한 없음 | 사용자 지정 가능 |
| **단계/경로 지정** | 예: [폴아웃](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)/[흐름](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/flow/flow.html) | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/reports-analytics/reports.html) | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/ad-hoc-analysis/c-reports-paths.html) | 예 | 아니오 | 예 |
| **고급 고객의 움직임 분석** | Yes: [Customer Journey Analytics](https://docs.adobe.com/content/help/ko-KR/analytics-platform/using/cja-landing.html) | 아니오 | 예 | 아니오 | 아니오 | 예 |
| **집단 분석** | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) | 아니오 | 아니오 | 아니오 | 아니오 | 예 |
| **Advanced Attribution** | [기여도 분석 IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution-iq.html) | 제한됨 - 첫 번째/마지막/선형 | 제한됨 - 첫 번째/마지막/선형 | 제한됨 - 첫 번째/마지막/선형 | 제한됨 - 첫 번째/마지막/선형 | 예 |
| **향상된 시각화 옵션** | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) | 아니오 | 예 | 예 | 아니오 | 예 |
| **사용자 지정 가능한 레이아웃** | [예](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) | 예 - [대시보드](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/dashboard.html) | 아니요 | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/layout/configure-the-custom-layout.html) | 분류별 또는 지표별로 결과를 정렬합니다. | 예 |
| ****&#x200B;프로젝트 조정(비분석가를 위해 보고서 간소화) | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/curate.html) | 아니오 | 아니오 | 예 | 아니오 | 예 |
| **프로젝트 공유** | [예: 모든/모든 사용자](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/curate.html) | [예: 모든/모든 사용자](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/reports-analytics/scheduling.html) | Ad Hoc Analysis 사용자만 | 예: 모든/모든 사용자 | 아니오 | 예 |
| **예약된 보고서** 배달 | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/schedule-projects.html) | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/reports-analytics/scheduling.html) | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/ad-hoc-analysis/c-schedule.html) | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/t-schedule-a-data-request.html) | 예 | 예 |
| **시스템 요구 사항** | 브라우저<br>[자세히..](https://docs.adobe.com/content/help/ko-KR/analytics/admin/sys-reqs.html) | 브라우저<br>[자세히..](https://docs.adobe.com/content/help/ko-KR/analytics/admin/sys-reqs.html) | Java<br>[자세히..](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/ad-hoc-analysis/c-getting-started.html) | Windows, MS<br>[Excel자세히...](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/report-builder-setup/system-requirements.html) | MS Excel처럼 .csv 파일을 여는 브라우저 및 프로그램입니다. 타블로 형식 파일을 생성할 수 있습니다. | Windows 64 bit, good graphics adapter for OpenGL 3.2 [More...](https://docs.adobe.com/content/help/ko-KR/data-workbench/using/install/c-data-workbench-client-install.html) |
| **가상 보고서 세트(보고서 시간 처리) 호환성** | 예 | 예 | 예 | 예 | 아니오 | 예? |
| **여러 보고서 세트** | 예 | 아니오 | 아니오 | 아니오 | 아니오 | 예? |
| **계산된 지표** | 예 | 예 | 예 | 예 | 예 | 예 |
| **마케팅 채널 호환성** | 예 | 예 | 예 | 예 | ? | ? |
| **세부기간 수준** |  |  |  |  |  |  |
| **예외 항목 탐지** | 예 | 아니오 |  |  |  |  |
| **기여도 분석** | 예 | 아니오 | 아니오 | 아니오 | 아니오 | 예 |
| **세그먼트 유형** |  |  |  |  |  |  |