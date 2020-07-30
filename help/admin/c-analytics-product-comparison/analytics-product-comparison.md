---
description: Analysis Workspace, Reports & Analytics, Ad Hoc Analysis, Report Builder, Data Warehouse 및 Data Workbench의 시스템 요구 사항 및 비교
title: Analytics 제품 비교 및 요구 사항
translation-type: tm+mt
source-git-commit: 54d6b4c2993c5b0391b9243c76661db1da4087b8
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 54%

---


# Analytics 제품 비교 및 요구 사항

이 페이지에는 다양한 Adobe Analytics 제품 비교가 포함되어 있습니다. Analysis Workspace, 보고 및 Analytics, Report Builder, Data warehouse, Data Workbench, 데이터 피드 및 Analytics API 2.0

사용할 Adobe Analytics 제품에 대해 알아보려면.[여기](/help/admin/c-analytics-product-comparison/which-analytics-tool.md)로 이동합니다.

| 제품 이름 및 도움말 링크 | [Analysis Workspace](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/home.html) | [Reports &amp; Analytics](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/reports-analytics/getting-started.html) | [Report Builder](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/home.html) | [Data Warehouse](https://docs.adobe.com/content/help/ko-KR/analytics/export/data-warehouse/data-warehouse.html) | [Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html) | [데이터 피드](https://docs.adobe.com/content/help/ko-KR/analytics/export/analytics-data-feed/data-feed-overview.html) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|---|---|
| **액세스 방법** | [브라우저](https://docs.adobe.com/content/help/ko-KR/analytics/admin/sys-reqs.html) | [브라우저](https://docs.adobe.com/content/help/ko-KR/analytics/admin/sys-reqs.html) | [Windows용 MS Excel](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/report-builder-setup/system-requirements.html) | 브라우저를 통해 설정합니다. [추가 정보](https://docs.adobe.com/content/help/ko-KR/analytics/admin/sys-reqs.html) | [Windows 64비트](https://docs.adobe.com/content/help/ko-KR/data-workbench/using/install/c-data-workbench-client-install.html) | 브라우저를 통해 설정합니다. [추가 정보](https://docs.adobe.com/content/help/ko-KR/analytics/export/analytics-data-feed/data-feed-overview.html) | RESTful API 툴. Adobe I/O 자격 증명으로 로그인합니다. [추가 정보](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| **데이터 세부기간** | 집계됨 | 집계됨 | 집계됨 | 집계됨 | 히트 | 히트 | 집계됨 |
| **사용 가능한 Experience Cloud ID(ECID)** | 아니오 | 아니오 | 아니오 | 예 | 예 | 예 | 아니오 |
| **사용 가능한 타임스탬프** | 아니오 | 아니오 | 아니오 | 아니오 | 예 | 예 | 아니오 |
| **처리 수준** | 완전히 처리됨 | 완전히 처리됨, 별도의 [실시간 보고서 포함](https://docs.adobe.com/content/help/en/analytics/components/real-time-reporting/realtime.html) | 완전히 처리됨, 별도의 [실시간 보고서 포함](https://docs.adobe.com/content/help/en/analytics/components/real-time-reporting/realtime.html) | 완전히 처리됨 | 완전히 처리됨 | 완전히 처리됨 | 완전히 처리됨 |
| **관리 보트 필터 데이터 포함** 자세한 <br>[내용](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/bot-removal/bot-removal.html) | 아니요 | 예 - 보트 보고서 분리 | 예 - 보트 보고서 분리 | 아니오 | 아니오 | 아니오 | 아니오 |
| **낮은 트래픽(고유 수가 초과되었습니다)이** 나타나는 <br>[자세한 정보](https://docs.adobe.com/content/help/ko-KR/analytics/technotes/low-traffic.html) | 예 | 예 | 예 | 아니오 | 아니오 | 아니오 | 예 |
| **표시 행 제한(페이지 매김 전)** | 400 | 200 | 50000 | 제한 없음 | 제한 없음 | 제한 없음 | 50000 |
| **여러 보고서 세트** | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html) | 예, 제한 사항 | 예 | 아니오 | 예 | 아니오 | 예 |
| **분류 수** | 제한 없음 | 최대 2 | 최대 2 | 제한 없음 | 제한 없음 | 제한 없음 | 제한 없음, 여러 쿼리 실행 |
| **세그멘테이션** 자세한 <br>[내용](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-workflow.html) | 예 | 예 | 예 | 예, [제한](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segment-reference/seg-compatibility.html) | 예 | 아니오 | 예 |
| **계산된 지표** 자세한 <br>[내용](https://docs.adobe.com/content/help/ko-KR/analytics/components/calculated-metrics/cm-overview.html) | 예, [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) | 예 | 예 | 아니오 | 예 | 아니오 | 예, [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) |
| **마케팅 채널** 자세한 <br>[내용](https://docs.adobe.com/content/help/ko-KR/analytics/components/marketing-channels/c-getting-started-mchannel.html) | 예 | 예 | 예 | 예 | 예 | 예 - [va_finder, va_closer](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html) | 예 |
| **집단 분석** | [예](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) | 아니오 | 아니오 | 아니오 | 예 | 아니오 | 아니오 |
| **속성** | 예, [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) | 제한적 | 제한적 | 아니오 | 예 | 아니오 | 예, [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/attribution/overview.html) |
| **가상 애널리스트 기능** 자세한 <br>[내용](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/virtual-analyst/overview.html) | 예 | 아니오 | 아니오 | 아니오 | 아니오 | 아니오 | 예 |
| **조정** 자세한 <br>[내용](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/curate.html) | 예 - 프로젝트 및 VRS | 아니오 | 아니오 | 아니오 | 아니오 | 아니오 | 예 - VRS만 해당 |
| **프로젝트 공유** 자세한 <br>[내용](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/share-projects.html) | 예, 프로젝트 역할 포함 | 예 | 예 | 아니오 | 예 | 아니오 | 아니오 |
| **예약된 배달** | 예 | 예 | 예 | 예 | 아니오 | 예 | 아니오 |
| **배달 대상** | 이메일 | 이메일 | 이메일, FTP, SFTP, [Microsoft PowerBI에 게시](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/publish-powerbi/power-bi.html) | 이메일, FTP. 고객 지원 센터에 연락하여 SFTP, Azure Blob, Amazon S3 등 추가 대상 지원을 받으십시오. | - | FTP, SFTP, Azure Blob, Amazon S3 | - |
| **VRS 보고서 시간 처리** 자세한 <br>[내용](https://docs.adobe.com/content/help/ko-KR/analytics/components/virtual-report-suites/vrs-report-time-processing.html) | 예 | 아니오 | 아니오 | 아니오 | 아니오 | 아니오 | 예 |
