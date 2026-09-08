---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
hold: true
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
TQID: 'https://experienceleague.adobe.com/yw30Yij2NBaeuWFqxD4-VH1Hysf8dxOpxHUwsFCYEw8'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85eid: a421fb65-2c82-457a-921c-28c46b697a39
subfeature_v2: id: d89ba969-e026-48bf-927e-e9df2f1e34f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 8645907799594d2eb2d6bcf56f93ac1cc42578f8
workflow-type: tm+mt
source-wordcount: 1098
ht-degree: 50%

---

# 최신 Adobe Analytics 릴리스 정보 (2026년 9월)

**마지막 업데이트**: 2026년 9월 8일

이 릴리스 정보는 2026년 9월 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 및 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ---- |
| **세그먼트를 보고 날짜 범위로 제한**<br/>&#x200B;세그먼트에 날짜 범위 구성 요소가 포함된 경우 Workspace 보고서의 데이터는 보고 날짜 범위를 초과할 수 있습니다.<p>이제 세그먼트에 포함된 날짜 구성 요소에 관계없이 결과를 보고 날짜 범위로 제한할 수 있는 새 옵션을 사용할 수 있습니다. <p>이 옵션은 최상위 컨테이너가 방문자인 세그먼트를 만들거나 수정할 때 사용할 수 있습니다.</p><p>자세한 내용은 [세그먼트 빌드](/help/components/segmentation/segmentation-workflow/seg-build.md#components)를 참조하세요.</p> | 2026년 8월 26일 | 2026년 9월 9일 |
| **보트 검색 업데이트**<br/> Web SDK에서 Edge Data Collection을 사용할 때 다음 보트 검색 업데이트를 사용할 수 있습니다.<ul><li>이제 보트 탐지 규칙을 만들어 보트 생성으로 처리되는 트래픽의 예외를 식별할 수 있습니다. 기존 규칙과 향후 규칙은 일치하는 트래픽을 보트 생성으로 계속 표시합니다.</li><li>이제 사용자 지정 보트 규칙이 IAB 보트 감지 규칙보다 먼저 실행됩니다. 이 변경 사항은 보트 점수에 영향을 주지 않지만, 이벤트와 연결된 보트 규칙 이름은 변경될 수 있습니다.</li></ul><p>참고: 이 업데이트는 웹 SDK을 사용하는 Edge 데이터 수집 구현에만 적용됩니다. AppMeasurement과 같은 이전 라이브러리에는 적용되지 않습니다.</p></p><p>(설명서 링크는 추후 제공됩니다.)</p> | | 2026년 9월 초 |
| **Adobe Brand Visibility 통합**<br/> AI 기반 검색이 실제 웹 사이트 참여 및 비즈니스 성과로 이어지는 방식을 측정할 수 있도록 Adobe Brand Visibility을 조직의 Adobe Analytics 데이터와 연결합니다.<p>(설명서 링크는 추후 제공됩니다.)</p> | | 2026년 9월 |
| **분류 세트 API 업데이트**<br/>&#x200B;이제 분류 세트 API 설명서에 분류 세트 API 요청을 구성하기 위한 업데이트된 끝점과 매개 변수 정보가 포함되어 있습니다.<p>자세한 내용은 [분류 끝점 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/)를 참조하십시오.</p> | 2026년 9월 5일 | 2026년 9월 30일 |
| **2.0 API 보고서 안내서의 날짜 항목 ID 인코딩 지침**<br/>&#x200B;이제 Adobe Analytics 2.0 API 날짜 트렌드 보고서 안내서에 날짜 `itemId` 매개 변수와 값이 인코딩되는 방법을 설명하는 새로운 섹션이 포함됩니다. 이제 더 이상 사용되지 않는 1.4 API에서 2.0 API 서비스를 구성하고 마이그레이션하는 데 도움이 될 수 있습니다.<p>자세한 내용은 [KPI 보고서 가이드](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/kpi) 및 [고급 보고서 가이드](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/advanced)를 참조하십시오.</p> | 2026년 9월 5일 | 2026년 9월 30일 |

### Adobe Analytics의 수정 사항

**Activity Map**: AN-488579, AN-487247
**Analysis Workspace**: AN-487374, AN-487119, AN-468907, AN-468810, AN-468363, AN-468096, AN-467414, AN-466986, AN-466982, AN-465073, AN-463571, AN-462373
**분류**: AN-490825, AN-490802, AN-490549, AN-490472, AN-487782, AN-487286, AN-486531, AN-478859, AN-469929, AN-469033, AN-468944, AN-468827, AN-468592, AN-468326, AN-467115, AN-466995, AN-465636, AN-465616, AN-465380, AN-464911, AN-464338, AN-463677, AN-462729 462577 461040 459316
**데이터 피드 및 Data Warehouse**: AN-487624, AN-487287, AN-479923, AN-479166, AN-479109, AN-468483
**마이그레이션**:
**내보내기**: AN-467131
**Report Builder**: AN-487486, AN-478944, AN-470036, AN-468589, AN-468436, AN-456747, AN-456700, AN-442695
**보고**: AN-468621, AN-465383, AN-463924
**보고서 세트**: AN-468484, AN-468460, AN-465385
**예약된 보고서**:
**세그먼테이션**: AN-486561
**기타**: AN-488549, AN-467426, AN-465265, AN-464645, AN-459714, AN-459323, AN-454514

### 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **이전 Report Builder** | 2025년 6월 18일 | 이전 Report Builder 추가 기능은 2026년 6월에 지원이 중단됩니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](/help/analyze/report-builder/rb-overview.md)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](/help/analyze/report-builder/convert-workbooks.md#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/)를 참조하십시오.</p> |

## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.

## 연기된 기능

| 기능 및 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| -----------|-----------|-----------|
| **스트리밍 미디어 서비스: 일정 데이터 지원** <br/>이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다.<p>다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.</p><ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul><p>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다.</p><p>이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.</p><p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다.</p><p>자세한 내용은 [라이브 콘텐츠를 추적할 일정 데이터 업로드](https://experienceleague.adobe.com/ko/docs/media-analytics/using/media-use-cases/track-schedule-data)를 참조하십시오. | 2025년 10월 29일 | TBD<p>(원래 2025년 10월 29일로 계획됨)</p> |


>[!MORELIKETHIS]
>
>* [2026년 이전 릴리스 정보](/help/release-notes/2026.md)
>* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
>* [스트리밍 미디어 서비스 릴리스 정보](https://experienceleague.adobe.com/ko/docs/media-analytics/using/release-notes/release-notes)
>* [Adobe CX Enterprise 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

