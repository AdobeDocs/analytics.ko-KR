---
title: Analytics 데이터 수집 디버그
description: Adobe Analytics이 AppMeasurement, Analytics 확장, Web SDK, Mobile SDK 및 데이터 삽입 API에서 예상하는 데이터를 수신하는지 확인합니다.
keywords: 디버깅, 유효성 검사, 패킷 분석기, 패킷 모니터, /b/ss/, Edge 추적, Assurance, hitdebugger, 보고서 세트
feature: Implementation Basics
role: Admin, Developer
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 049b9b7447c7f91d67eb58fc781898b685bd9d91
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 2%
---
# Analytics 데이터 수집 디버그

이 문서에서는 Adobe Analytics으로 전송된 데이터를 디버깅할 때 확인할 사항을 설명합니다. 다음 표에서 구현 방법을 찾아 해당 섹션을 따르십시오. 예기치 않은 보고서 데이터를 조사하는 경우 [요청과 보고서 비교](#reports)(으)로 시작하십시오.

네트워크 요청 캡처, 디버그 로깅 활성화, 취소된 요청 조사와 같이 모든 Adobe 데이터 수집에 적용되는 단계 및 도구는 [데이터 수집 디버깅 및 문제 해결](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/overview)을 참조하십시오.

| 구현 방식 | Analytics에서 수신하는 데이터를 볼 수 있는 위치 | 지침 |
| --- | --- | --- |
| AppMeasurement 또는 Analytics 태그 확장 | 브라우저에서 Analytics 데이터 수집 서버로 직접 요청 | [AppMeasurement](#appmeasurement) |
| Web SDK | Edge 추적, Edge Network에서 이벤트를 Analytics 히트로 전환한 후 | [웹 SDK](#web-sdk) |
| Mobile SDK | Assurance의 Analytics 이벤트 보기. Edge Network 또는 Edge Bridge 확장을 사용하는 경우 **[!UICONTROL Analytics Edge 보기]**&#x200B;를 켭니다. | [Assurance의 Adobe Analytics 이벤트 보기](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/adobe-analytics) |
| 데이터 삽입 API | 서버의 보내는 요청 및 응답 | [데이터 삽입 API 요청 문제 해결](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/troubleshooting) |

## AppMeasurement 및 Analytics 확장 {#appmeasurement}

### 요청 찾기 {#appmeasurement-find}

[네트워크 요청을 캡처](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/inspect-requests#web)하고 `/b/ss/`을(를) 필터링합니다. Adobe Experience Platform Debugger과 같은 태그 디버거는 이러한 요청을 식별하고 디코딩합니다.

`/b/ss/` 요청이 표시되지 않는 경우:

* 브라우저 콘솔에서 JavaScript 오류를 확인합니다.
* Analytics 태그 확장을 사용하는 경우 태그 포함 코드가 페이지의 `<head>` 요소 내에 있고 라이브러리가 테스트 중인 환경에 게시되었는지 확인합니다. [태그 디버그 모드](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/logging)에서는 히트를 보내는 규칙이 실행되었는지 여부를 보여 줍니다.
* AppMeasurement을 직접 호스팅하는 경우 라이브러리의 URL을 직접 열어 파일이 로드되고 코드가 포함되어 있는지 확인합니다.
* 요청이 전송되지 않도록 하는 브라우저 확장 기능(예: 광고 차단기)을 비활성화합니다.
* 디버거가 iframe 내에서 전송된 요청을 인식하지 않습니다. 대신 브라우저 개발자 도구를 사용합니다. [iFrame에서 AppMeasurement 사용](../use-cases/iframe.md)을 참조하세요.

### Analytics가 받은 항목 확인 {#appmeasurement-contents}

* **보고서 세트**: `/b/ss/` 이후의 경로 세그먼트에는 히트를 받는 보고서 세트 ID가 나열됩니다. 개발 페이지의 개발 보고서 세트와 같이 예상하는 보고서 세트인지 확인합니다.
* **변수**: 원시 요청은 변수 이름이 아닌 쿼리 매개 변수 이름을 사용합니다. 예를 들어, eVar1은 `v1`(으)로 표시되고 prop1은 `c1`(으)로 표시됩니다. [변수 참조](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference)를 참조하십시오. 요청이 너무 길면 AppMeasurement에서 HTTP `POST`을(를) 사용하여 보내므로 변수가 URL 대신 요청 본문에 나타납니다.
* **히트 형식**: [`tl()`](../vars/functions/tl-method.md)이(가) 보낸 요청에 `pe` 매개 변수가 포함되어 있으며 페이지 보기를 증가시키지 않습니다. [`t()`](../vars/functions/t-method.md)이(가) 보낸 요청에는 `pe`이(가) 포함되지 않습니다.

값이 있지만 잘못된 경우 따옴표, 대문자 및 공백과 같은 일반적인 원인을 보려면 [JavaScript 구현 문제 해결](../js/troubleshooting.md)을 참조하십시오.

### 응답 확인 {#appmeasurement-response}

`2xx` 응답은 데이터 수집 서버가 요청을 수신했는지 확인하기만 하고 히트가 기록되지 않았는지 확인합니다. 기본 응답 유형을 사용하면 히트가 삭제되더라도 요청이 성공을 반환할 수 있습니다. 새 방문자의 첫 번째 요청에 `302` 응답이 필요합니다. [HTTP 응답 코드](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/troubleshooting#http-response-codes)를 참조하세요.

AppMeasurement은 [`useBeacon`](../vars/config-vars/usebeacon.md)이(가) 활성화된 경우 `navigator.sendBeacon()`과(와) 함께 종료 링크 요청 및 모든 요청을 보냅니다. 개발자 도구는 브라우저가 이러한 요청을 보냈을 때에도 이러한 요청에 취소된 것으로 레이블을 지정할 수 있습니다. [중단된 요청](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/inspect-requests#aborted-requests)을 참조하십시오.

## Web SDK {#web-sdk}

### 요청 찾기 {#web-sdk-find}

Web SDK을 사용하면 브라우저가 Analytics에 직접 연결하는 대신 Edge Network에 이벤트를 보내므로 `/b/ss/` 요청이 표시되지 않습니다. [Edge Network 요청을 검사하고](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/inspect-requests#edge-network-requests) 다음을 확인하십시오.

* `configId` 매개 변수는 예상한 보고서 세트와 함께 [Adobe Analytics 서비스](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#analytics)가 활성화된 데이터 스트림과 일치합니다.
* 페이로드는 페이지 보기 또는 링크 이벤트로 유효합니다. Analytics에서는 페이지 세부 사항이나 웹 상호 작용 유형을 포함하지 않는 페이로드를 무시합니다. [Adobe Analytics의 Edge Network 이벤트 유형](../aep-edge/hit-types.md)을 참조하세요.

### Analytics가 받은 항목 확인 {#web-sdk-contents}

[Edge 추적](https://experienceleague.adobe.com/en/docs/experience-platform/debugger/edge-trace)을(를) 시작하고 작업을 재현합니다. **[!UICONTROL Analytics 자동 매핑]**(으)로 시작하는 행을 찾은 다음 `mappedQueryParams` 및 그 아래의 보고서 세트 ID를 확장합니다.

* **변수**: 매핑된 값은 AppMeasurement 요청과 동일한 쿼리 매개 변수 이름을 사용하며, 경우에 따라 페이지 이름의 경우 `gn`, 제품의 경우 `pl`과(와) 같은 약식 형식일 수 있습니다. [XDM 개체 필드 매핑](../aep-edge/xdm-var-mapping.md) 및 [데이터 개체 필드 매핑](../aep-edge/data-var-mapping.md)을 참조하세요.
* **컨텍스트 데이터**: Analytics 변수에 매핑되지 않는 XDM 필드는 `c.a.x.` 접두사가 있는 컨텍스트 데이터로 표시됩니다. [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)을(를) 사용하여 변수에 할당합니다.
* **보고서 세트**: 보고서 세트 재정의를 사용하는 경우 Edge 추적의 데이터스트림 구성 행에 Edge Network에서 사용한 보고서 세트가 표시됩니다.

### 처리 확인 {#web-sdk-processing}

Edge 추적이 열리는 Assurance 세션에서 `hitdebugger`에 대한 이벤트를 검색합니다. 이러한 이벤트는 공급업체 `com.adobe.analytics.hitdebugger`을(를) 사용하며, 페이로드는 Analytics 처리 후 Experience Cloud ID(`mcvisId`) 및 `pageName`과(와) 같은 값을 표시합니다.

자세한 내용은 [Adobe Experience Platform Web SDK을 사용하여 Adobe Analytics 설정](https://experienceleague.adobe.com/ko/docs/platform-learn/implement-web-sdk/applications-setup/setup-analytics)을 참조하십시오.

## 요청을 보고서와 비교 {#reports}

Analytics에 도달하는 히트는 보고서에 즉시 표시되지 않으며 보고된 값이 요청의 값과 다를 수 있습니다.

* **지연**: 전체 데이터는 일반적으로 수집 후 약 2시간 후에 보고서에 표시됩니다. 타임스탬프가 지정된 히트와 같은 일부 데이터는 더 오래 걸릴 수 있습니다. [데이터 가용성 및 대기 시간](/help/technotes/latency.md)을 참조하세요.
* **처리**: 처리 규칙, VISTA 규칙, 보트 규칙 및 기타 처리 단계는 수집 후 값을 변경하거나 제외할 수 있습니다. [Adobe Analytics의 데이터 처리 순서](/help/technotes/processing-order.md)를 참조하세요. Assurance 사후 처리 데이터는 개별 히트에 대한 처리 결과를 보여 줍니다.
* **보고서 세트**: 요청 또는 데이터 스트림을 대상으로 하는 동일한 보고서 세트를 보고 있는지 확인하십시오.
* **예기치 않은 값**: 차원에 예기치 않은 스파이크나 값이 표시되면 [해시 충돌](hash-collisions.md)을 참조하세요.

더 광범위한 트래픽 변경 사항은 [데이터 증가 및 감소 문제 해결](/help/technotes/event/spikes-drops.md)을 참조하십시오.
