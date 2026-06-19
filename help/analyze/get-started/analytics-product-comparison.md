---
description: Analysis Workspace, Report Builder, Data Warehouse 및 Data Workbench의 시스템 요구 사항 및 비교
title: Analytics 제품 비교 및 요구 사항
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
TQID: https://experienceleague.adobe.com/VQgK6DUSlz-UA3zk-Q18-QOAI5M6xfK7KqBYwW56j6w
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: af53ada8-1b7d-4929-ac91-ac971dd20ec7id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705cid: dcae653e-62c6-4cc8-84e6-ee110b848296id: e9cb007b-c8b7-4975-bc81-11a788c535faid: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 530
ht-degree: 67%

---

# Analytics 제품 비교 및 요구 사항

이 페이지에는 Analysis Workspace, Report Builder, Data Warehouse, 데이터 피드 및 Analytics API 2.0 등 다양한 Adobe Analytics 제품의 비교가 포함되어 있습니다.

사용할 Adobe Analytics 제품에 대한 자세한 내용은 [어떤 Adobe Analytics 도구를 사용해야 합니까?](/help/analyze/get-started/which-analytics-tool.md)를 참조하십시오.

| 제품 이름 및 도움말 링크 | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Report Builder](/help/analyze/report-builder/rb-overview.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [데이터 피드](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytics API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|
| **액세스 방법** | [브라우저](/help/analyze/get-started/sys-reqs.md) | [Windows용 MS Excel](/help/analyze/legacy-report-builder/setup/system-requirements.md) | 브라우저를 통해 설정합니다. [자세히 알아보기](/help/analyze/get-started/sys-reqs.md) | 브라우저를 통해 설정합니다. [자세히 알아보기](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful API 도구. Adobe Developer 자격 증명으로 로그인합니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **데이터 세부 기간** | 집계됨 | 집계됨 | 집계됨 | 히트 | 집계됨 |
| **Experience Cloud ID (ECID) 사용 가능** | 아니요 | 아니요 | 예 | 예 | 아니요 |
| **타임스탬프 사용 가능** | 아니요 | 아니요 | 아니요 | 예 | 아니요 |
| **처리 수준** | 완전히 처리됨 | 완전히 처리됨, 별도의 [실시간 보고서](/help/admin/tools/manage-rs/edit-settings/realtime/realtime.md) 사용 | 완전히 처리됨 | 완전히 처리됨 | 완전히 처리됨 |
| **관리 보트 필터 데이터 포함** <br> [자세히 알아보기](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md) | 아니요 | 예 - 별도의 보트 보고서 | 아니요 | 아니요 | 아니요 |
| **낮은 트래픽 (고유 수가 초과되었습니다) 표시** <br> [자세히 알아보기](/help/technotes/low-traffic.md) | 예 | 예 | 아니요 | 아니요 | 예 |
| **표시 행 제한 (페이지 매김 전)** | 400 | 50000 | 제한 없음 | 제한 없음 | 50000 |
| **여러 보고서 세트** | [예](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | 예 | 아니요 | 예 | 아니요 |
| **분류 수** | 제한 없음 | 최대 2 | 제한 없음 | 제한 없음 | 제한 없음, 여러 쿼리에서 실행 |
| **세분화** <br> [자세히 알아보기](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | 예 | 예 | 예. [제한 사항](/help/export/data-warehouse/segment-compatibility.md) 있음 | 아니요 | 예 |
| **계산된 지표** <br> [자세히 알아보기](/help/components/calculated-metrics/cm-overview.md) | 예. [속성 ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 | 예. 속성 사용 | 예 | 아니요 | 예. [속성 ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 |
| **마케팅 채널** <br> [자세히 알아보기](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | 예 | 예 | 예 | 예 - [va_finder, va_closer](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | 예 |
| **집단 분석** | [예](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | 예 | 아니요 | 아니요 | 아니요 |
| **속성** | 예. [속성 ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 | 제한적 | 아니요 | 아니요 | 예. [속성 ](/help/analyze/analysis-workspace/attribution/overview.md) 사용 |
| **큐레이션** <br> [자세히 알아보기](/help/analyze/analysis-workspace/curate-share/curate.md) | 예 - 프로젝트 및 가상 보고서 세트 | 아니요 | 아니요 | 아니요 | 예 - 가상 보고서 세트만 해당 |
| **프로젝트 공유** <br> [자세히 알아보기](/help/analyze/analysis-workspace/curate-share/share-projects.md) | 예. 프로젝트 역할 사용 | 예 | 아니요 | 아니요 | 아니요 |
| **예약된 게재** | 예 | 예 | 예 | 예 | 아니요 |
| **게재 대상** | 이메일 | 이메일, FTP, SFTP, [Microsoft PowerBI에 게시](/help/analyze/legacy-report-builder/c-publish-power-bi/power-bi.md) | Amazon S3, Google Cloud Platform, Azure SAS, Azure RBAC 및 이메일 | Amazon S3, Azure RBAC, Azure SAS 및 Google Cloud Platform | - |
| **가상 보고서 세트 보고서 시간 처리** <br> [자세히 알아보기](/help/components/vrs/vrs-report-time-processing.md) | 예 | 아니요 | 아니요 | 아니요 | 예 |
| **지역 및 기술 보고서** | 예 <p>게시물 필드가 아닌 mid 값을 사용합니다. 방문 첫 번째 히트 논리는 `visit_page_num=1` 대신 `post_cust_hit_time_gmt`을(를) 기반으로 합니다. IP가 방문 중간에 변경되거나, 히트가 잘못된 순서로 도달하거나, 방문이 월 경계를 넘는 경우 결과는 다른 도구와 다를 수 있습니다.</p> | 예 <p>게시물 필드가 아닌 mid 값을 사용합니다. 방문 첫 번째 히트 논리는 `visit_page_num=1` 대신 `post_cust_hit_time_gmt`을(를) 기반으로 합니다. IP가 방문 중간에 변경되거나, 히트가 잘못된 순서로 도달하거나, 방문이 월 경계를 넘는 경우 결과는 다른 도구와 다를 수 있습니다.</p> | 예 <p>게시물 값과 `visit_page_num=1`을(를) 사용하여 방문의 첫 번째 히트를 결정합니다. 첫 번째 히트의 값을 이러한 차원에 대한 방문의 모든 히트에 적용합니다.</p> | 예 <p>게시물 값과 `visit_page_num=1`을(를) 사용하여 방문의 첫 번째 히트를 결정합니다. 첫 번째 히트의 값을 이러한 차원에 대한 방문의 모든 히트에 적용합니다.</p> | 예 <p>게시물 필드가 아닌 mid 값을 사용합니다. 방문 첫 번째 히트 논리는 `visit_page_num=1` 대신 `post_cust_hit_time_gmt`을(를) 기반으로 합니다. IP가 방문 중간에 변경되거나, 히트가 잘못된 순서로 도달하거나, 방문이 월 경계를 넘는 경우 결과는 다른 도구와 다를 수 있습니다.</p> |
