---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
TQID: 'https://experienceleague.adobe.com/yw30Yij2NBaeuWFqxD4-VH1Hysf8dxOpxHUwsFCYEw8'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
    internal-label: Integrations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: d89ba969-e026-48bf-927e-e9df2f1e34f3
    internal-label: Release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: cf020d4d2b873668a17c978ed69a311db37e7cd0
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 52%
---
# 최신 Adobe Analytics 릴리스 정보 (2026년 10월)

**마지막 업데이트**: 2026년 10월 7일

이 릴리스 정보는 2026년 10월 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 및 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ---- |
| **Adobe Analytics MCP 서버에 대한 읽기 전용 권한**<br/>&#x200B;이제 관리자는 사용자에게 Adobe Analytics MCP 서버에 대한 읽기 전용 액세스 권한을 부여할 수 있습니다. 새 [!UICONTROL MCP 읽기 전용 액세스] 권한 항목은 사용자에게 프로젝트, 세그먼트 또는 계산된 지표를 만들지 않고도 모든 읽기 전용 도구에 액세스할 수 있도록 합니다.<p>기존 [!UICONTROL MCP 액세스] 권한 항목의 이름이 [!UICONTROL MCP 전체 액세스]&#x200B;(으)로 변경되었습니다. 이 권한이 있는 사용자는 구성 요소를 만들거나, 변경하거나, 삭제하는 도구를 포함하여 모든 도구에 대한 액세스 권한을 유지합니다.</p><p>자세한 내용은 Adobe Analytics MCP 서버 설명서에서 [권한 설정](https://developer.adobe.com/analytics-mcp/docs/guides/permissions)을 참조하십시오.</p> | | 2026년 10월 6일 |
| **구성 요소 설명 자동 생성** <br/>이제 차원, 지표, 계산된 지표, 세그먼트 및 날짜 범위에 대한 설명을 자동으로 생성할 수 있습니다. 이는 Workspace 사용자가 특히 큰 구성 요소 라이브러리가 있는 조직에서 사용할 구성 요소를 이해하는 데 도움이 됩니다. <p>단일 구성 요소에 대한 설명을 생성하거나 동시에 여러 구성 요소에 대한 설명을 생성할 수 있습니다.</p> <p>(참조할 설명서 링크입니다.)<!--For more information, see [Automatically generate descriptions](/help/components/add-component-descriptions.md#automatically-generate-descriptions).--></p> | | 2026년 10월 28일 |
| **Adobe Brand Visibility 통합**<br/> AI 기반 검색이 실제 웹 사이트 참여 및 비즈니스 성과로 이어지는 방식을 측정할 수 있도록 Adobe Brand Visibility을 조직의 Adobe Analytics 데이터와 연결합니다.<p>(설명서 링크는 추후 제공됩니다.)</p> | | 2026년 10월 |
| **CX Enterprise Coworker: 공동 작업자 채팅에서 Adobe Analytics 데이터 분석** <br/>Adobe CX Enterprise Coworker 채팅에서 이전에 Analysis Workspace에서만 가능했던 고급 데이터 분석을 수행할 수 있습니다. 동료 채팅은 Adobe Analytics 보고서 세트의 데이터에 액세스하여 해당 데이터를 탐색하고 자연어 프롬프트에 대한 답변을 얻을 수 있습니다.<p>(설명서 링크는 추후 제공됩니다.)</p> | 2026년 10월 2일 | TBD<p>(원래 2026년 9월 25일로 계획됨)</p> |

### Adobe Analytics의 수정 사항

**Activity Map**: AN-494609, AN-493182
**Analysis Workspace**: AN-495340, AN-494789, AN-493307, AN-468900
**분류**: AN-498043, AN-496619, AN-496468, AN-496217, AN-496133, AN-495567, AN-494651, AN-494345, AN-494312, AN-494261, AN-493645, AN-493507, AN-493336, AN-492869, AN-492812, AN-492751, AN-492750, AN-492741, AN-491032, AN-490802, AN-490796 467849
**데이터 피드 및 Data Warehouse**: AN-494937, AN-493065, AN-489796, AN-479109
**마이그레이션**: AN-489850, AN-468014
**내보내기**: AN-494337, AN-486563
**Report Builder**: AN-496602, AN-494224, AN-493737, AN-493508, AN-493505, AN-492806, AN-468981, AN-454376
**보고**: AN-493637, AN-461260
**보고서 세트**: AN-496773, AN-495227, AN-494981, AN-494372, AN-494370, AN-493629
**예약된 보고서**: AN-491103
**세분화**:
**기타**: AN-496398, AN-494453, AN-492494

### 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **이전 Report Builder** | 2025년 6월 18일 | 레거시 Report Builder 추가 기능은 2026년 6월에 사용이 중단되었습니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](/help/analyze/report-builder/rb-overview.md)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](/help/analyze/report-builder/convert-workbooks.md#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 | **2026년 8월 31일**&#x200B;에 다음 Analytics Legacy API 서비스가 수명이 종료되어 종료되었으며 이러한 서비스를 사용하여 빌드된 모든 통합이 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/)를 참조하십시오.</p> |

## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.

## 연기된 기능

| 기능 및 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| -----------|-----------|-----------|
| **스트리밍 미디어 서비스: 일정 데이터 지원** <br/>이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다.<p>다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.</p><ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul><p>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다.</p><p>이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.</p><p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다.</p><p>자세한 내용은 [라이브 콘텐츠를 추적할 일정 데이터 업로드](https://experienceleague.adobe.com/ko/docs/media-analytics/using/media-use-cases/track-schedule-data)를 참조하십시오.</p> | 2025년 10월 29일 | TBD<p>(원래 2025년 10월 29일로 계획됨)</p> |


>[!MORELIKETHIS]
>
>* [2026년 이전 릴리스 정보](/help/release-notes/2026.md)
>* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
>* [스트리밍 미디어 서비스 릴리스 정보](https://experienceleague.adobe.com/ko/docs/media-analytics/using/release-notes/release-notes)
>* [Adobe CX Enterprise 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

