---
description: Analysis Workspace, Reports & Analytics, Report Builder, Data Warehouse 및 Data Workbench의 시스템 요구 사항 및 비교
title: Analytics 제품 비교 및 요구 사항
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
source-git-commit: 8f25dfefbc6fba1fb525d2e9e0fce654e21ef362
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 98%

---

# Analytics 제품 비교 및 요구 사항

이 페이지에는 Analysis Workspace, Reports &amp; Analytics, Report Builder, Data Warehouse, Data Workbench, 데이터 피드 및 Analytics API 2.0 등 다양한 Adobe Analytics 제품의 비교가 포함되어 있습니다.

사용할 Adobe Analytics 제품에 대해 알아보려면.[여기](/help/admin/c-analytics-product-comparison/which-analytics-tool.md)로 이동합니다.

| 제품 이름 및 도움말 링크 | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Reports &amp; Analytics](/help/analyze/reports-analytics/getting-started.md) | [Report Builder](/help/analyze/report-builder/home.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/home.html?lang=ko-KR) | [데이터 피드](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **액세스 방법** | [브라우저](/help/admin/sys-reqs.md) | [브라우저](/help/admin/sys-reqs.md) | [Windows용 MS Excel](/help/analyze/report-builder/setup/system-requirements.md) | 브라우저를 통해 설정합니다. [자세히 알아보기](/help/admin/sys-reqs.md) | [Windows 64비트](https://experienceleague.adobe.com/docs/data-workbench/using/install/c-data-workbench-client-install.html?lang=ko-KR) | 브라우저를 통해 설정합니다. [자세히 알아보기](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API 도구. Adobe Developer 자격 증명으로 로그인합니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **데이터 세부기간** | 집계됨 | 집계됨 | 집계됨 | 집계됨 | 히트 | 히트 | 집계됨 |
| **Experience Cloud ID (ECID) 사용 가능** | 아니요 | 아니요 | 아니요 | 예 | 예 | 예 | 아니요 |
| **타임스탬프 사용 가능** | 아니요 | 아니요 | 아니요 | 아니요 | 예 | 예 | 아니요 |
| **처리 수준** | 완전히 처리됨 | 완전히 처리됨, 별도의 [실시간 보고서](/help/components/c-real-time-reporting/realtime.md) 사용 | 완전히 처리됨, 별도의 [실시간 보고서](/help/components/c-real-time-reporting/realtime.md) 사용 | 완전히 처리됨 | 완전히 처리됨 | 완전히 처리됨 | 완전히 처리됨 |
| **관리 보트 필터 데이터 포함** <br> [자세히 알아보기](/help/admin/admin/bot-removal/bot-removal.md) | 아니요 | 예 - 별도의 보트 보고서 | 예 - 별도의 보트 보고서 | 아니요 | 아니요 | 아니요 | 아니요 |
| **낮은 트래픽 (고유 수가 초과되었습니다) 표시** <br> [자세히 알아보기](/help/technotes/low-traffic.md) | 예 | 예 | 예 | 아니요 | 아니요 | 아니요 | 예 |
| **표시 행 제한 (페이지 매김 전)** | 400 | 200 | 50000 | 제한 없음 | 제한 없음 | 제한 없음 | 50000 |
| **여러 보고서 세트** | [예](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | 예. 제한 사항 있음 | 예 | 아니요 | 예 | 아니요 | 예 |
| **분류 수** | 제한 없음 | 최대 2 | 최대 2 | 제한 없음 | 제한 없음 | 제한 없음 | 제한 없음, 여러 쿼리에서 실행 |
| **세그먼테이션** <br> [자세히 알아보기](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | 예 | 예 | 예 | 예. [제한 사항](/help/components/segmentation/seg-reference/seg-compatibility.md) 있음 | 예 | 아니요 | 예 |
| **계산된 지표** <br> [자세히 알아보기](/help/components/c-calcmetrics/cm-overview.md) | 예. [속성 IQ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 | 예 | 예 | 아니요 | 예 | 아니요 | 예. [속성 IQ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 |
| **마케팅 채널** <br> [자세히 알아보기](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | 예 | 예 | 예 | 예 | 예 | 예 - [va_finder, va_closer](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | 예 |
| **집단 분석** | [예](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | 아니요 | 아니요 | 아니요 | 예 | 아니요 | 아니요 |
| **속성** | 예. [속성 IQ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 | 제한적 | 제한적 | 아니요 | 예 | 아니요 | 예. [속성 IQ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 |
| **가상 분석가 기능** <br> [자세히 알아보기](/help/analyze/analysis-workspace/virtual-analyst/overview.md) | 예 | 아니요 | 아니요 | 아니요 | 아니요 | 아니요 | 예 |
| **큐레이션** <br> [자세히 알아보기](/help/analyze/analysis-workspace/curate-share/curate.md) | 예 - 프로젝트 및 VRS | 아니요 | 아니요 | 아니요 | 아니요 | 아니요 | 예 - VRS만 |
| **프로젝트 공유** <br> [자세히 알아보기](/help/analyze/analysis-workspace/curate-share/share-projects.md) | 예. 프로젝트 역할 사용 | 예 | 예 | 아니요 | 예 | 아니요 | 아니요 |
| **예약된 게재** | 예 | 예 | 예 | 예 | 아니요 | 예 | 아니요 |
| **게재 대상** | 이메일 | 이메일 | 이메일, FTP, SFTP, [Microsoft PowerBI에 게시](/help/analyze/report-builder/c-publish-power-bi/power-bi.md) | 이메일, FTP. SFTP, Azure Blob, Amazon S3 등 추가적인 대상 지원을 받으려면 고객 지원 센터에 문의하십시오. | - | FTP, SFTP, Azure Blob, Amazon S3 | - |
| **VRS 보고서 시간 처리** <br> [자세히 알아보기](/help/components/vrs/vrs-report-time-processing.md) | 예 | 아니요 | 아니요 | 아니요 | 아니요 | 아니요 | 예 |
