---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
TQID: https://experienceleague.adobe.com/yw30Yij2NBaeuWFqxD4-VH1Hysf8dxOpxHUwsFCYEw8
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 1be0f3577403db7cf9bd40ef9e7c4bfcfa6c0b17
workflow-type: tm+mt
source-wordcount: 1241
ht-degree: 79%

---

# 최신 Adobe Analytics 릴리스 정보 (2026년 4월)

**마지막 업데이트**: 2026년 4월 22일

이 릴리스 정보에는 2026년 4월 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 및 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ---- |
| **Adobe Analytics용 MCP 서버** <br/>Analytics MCP(Model Context Protocol) 서버를 사용하면 지원되는 MCP 클라이언트를 Adobe Analytics에 연결할 수 있습니다. 연결되면 MCP 클라이언트는 제품별 도구를 호출하여 데이터를 검색하거나 쿼리를 실행하거나 LLM 또는 에이전트 워크플로우의 일부로 지원되는 작업을 수행할 수 있습니다. 자세한 내용은 [Analytics MCP 서버](https://developer.adobe.com/analytics-mcp/docs/)를 참조하십시오.<p>Beta 기간 동안 이러한 MCP 서버를 사용한 경우 Beta와 프로덕션 엔드포인트 간에 서로 다른 URL이 있습니다. 베타 기간 동안 만들어진 모든 에이전트 워크플로가 5월 31일 이전에 프로덕션 끝점을 사용하도록 업데이트되었는지 확인하십시오.</p> | | 2026년 5월 5일 |
| **스트리밍 미디어 서비스: 일정 데이터 지원** <br/>이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다.<p>다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.</p><ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul><p>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다.</p><p>이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.</p><p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다.</p><p>자세한 내용은 [라이브 콘텐츠를 추적할 일정 데이터 업로드](https://experienceleague.adobe.com/ko/docs/media-analytics/using/media-use-cases/track-schedule-data)를 참조하십시오.</p> | 2025년 10월 29일 | 2026년 상반기<p>(원래 2025년 10월 29일 릴리스로 계획됨)</p> |
| **추가 API 날짜 범위 형식**<br/>&#x200B;이제 Analytics 2.0 API 보고서 요청에서 날짜 범위를 지정하는 두 가지 새로운 형식이 지원됩니다. 여기에는 날짜 수식과 혼합 형식이 포함됩니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/#date-range-field--supported-formats) | | 2026년 3월 |
| **API 보고서 요청의 선택적 차원**<br/>&#x200B;보고서 API 요청에는 차원 오브젝트가 필요하지 않습니다. 차원이 지정되지 않으면 응답에 총합 보고서에 대한 데이터가 표시됩니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/#using-dimension-in-report-payload-requests) | | 2026년 3월 |
| **날짜 트렌드 고급 API 보고서**<br/>&#x200B;새로운 Adobe Analytics 2.0 API 날짜 트렌드 고급 보고서 안내서. 날짜 범위 비교 및 세그먼트를 사용하여 고급 날짜 트렌드 API 보고서를 만듭니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/advanced/) | | 2026년 3월 |

## Adobe Analytics의 수정 사항

**Activity Map**:
**Analysis Workspace**: AN-442813, AN-442410, AN-441943, AN-441717, AN-434855, AN-431409, AN-429777, AN-429048, AN-428892, AN-428189, AN-425215
**분류**: AN-443453, AN-443275, AN-443148, AN-442906, AN-442232, AN-442207, AN-442148, AN-442133, AN-441937, AN-441901, AN-441807, AN-441671, AN-441333, AN-441302, AN-441149, AN-441132, AN-441085, AN-441048, AN-440846, AN-440727, AN-440716, AN-440511 440496 432100
**데이터 피드 및 Data Warehouse**: AN-442211, AN-441719, AN-441183, AN-441011, AN-440625, AN-438953
**마이그레이션**: AN-442467, AN-440380, AN-440357
**내보내기**:
**Report Builder**: AN-441136, AN-438147, AN-425150
**보고**: AN-441506, AN-440919, AN-440545, AN-440300
**보고서 세트**: AN-439429, AN-439423, AN-430988
**예약된 보고서**:
**세그먼테이션**:
**기타**: AN-423359, AN-406242, AN-397985


## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **LiveStream 처리 개선 사항** | 2026년 1월 14일 | Adobe는 LiveStream 페이로드의 형식을 개선하고 변경할 계획입니다. 이러한 업데이트는 LiveStream과 Analysis Workspace와 같은 다른 Adobe Analytics 기능 간의 패리티를 향상합니다. 계획된 변경 사항을 테스트할 수 있는 미리보기 엔드포인트가 있습니다. 변경 사항의 전체 목록과 엔드포인트 세부 정보 미리보기에 대해서는 [LiveStream 릴리스 정보](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/release-notes/)를 참조하십시오. Adobe는 2026년 4월 13일에 업데이트된 페이로드 형식으로 하드 컷오버를 계획합니다. |
| **TLS 1.2 암호 세트 제거** | 2026년 2월 11일 | 관리자에게 알림: Adobe는 2026년 5월 27일에 Adobe 데이터 수집 서버에서 다음 TLS 1.2 암호 세트에 대한 지원을 중단할 예정입니다.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_GCM_SHA256`</li><li>`TLS_RSA_WITH_AES_256_GCM_SHA384`</li></ul><p>대부분의 구현에서 고객 액션 필요하지 않습니다. 이 변경 사항은 주로 오래된 TLS 라이브러리를 사용하는 이전 기본 애플리케이션과 구식 브라우저 또는 운영 체제에서 소수의 웹 방문자로부터 전송된 Analytics 데이터에 영향을 미칩니다. 이러한 암호 세트에 대한 지원을 제거하면 보안이 강화되고 Adobe가 최신 암호화 표준에 맞게 조정됩니다. 현재 데이터 수집 트래픽의 0.1% 미만이 이러한 암호 세트에 의존합니다.</p> |
| **이전 Report Builder** | 2025년 6월 18일 | 이전 Report Builder 추가 기능은 2026년 6월에 지원이 중단됩니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](/help/analyze/report-builder/rb-overview.md)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](/help/analyze/report-builder/convert-workbooks.md#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **레거시 도메인 또는 레거시 SSO를 통한 액세스** | 2025년 4월 10일 | Adobe는 보안을 강화하고 로그인 환경을 간소화하기 위해 사용자가 Adobe Analytics에 액세스하는 방식을 업데이트할 계획입니다. 이러한 업데이트의 일환으로 `my.omniture.com`을 비롯한 기존 도메인 또는 기존 SSO를 통한 액세스는 **2026년 1월 2일**&#x200B;부터 영구 중단됩니다. 이 날짜 이후에는 기존 로그인 자격 증명과 기존 SSO가 더 이상 작동하지 않습니다. 모든 사용자는 Adobe Experience Cloud ID를 사용하여 `experience.adobe.com`을 통해 로그인해야 합니다. Experience Cloud ID와 관련하여 도움이 필요한 경우, 조직의 Adobe Analytics 관리자 또는 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/contact.html)에 문의하십시오. |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/)를 참조하십시오.</p> |


## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 노트](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko)
* [스트리밍 미디어 서비스 릴리스 정보](https://experienceleague.adobe.com/ko/docs/media-analytics/using/release-notes/release-notes)
* [Adobe Experience Cloud 제품](https://business.adobe.com/kr/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
