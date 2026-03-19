---
title: Adobe Analytics의 데이터 처리 순서
description: Adobe Analytics에서 데이터를 처리하는 구성 요소 순서 및 서비스에 대해 알아봅니다.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
feature: Data Configuration and Collection
source-git-commit: 6c947812d4fd8bc2ee951a5933c6e3b6d8ca1a6b
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 35%

---

# Adobe Analytics의 데이터 처리 순서

Adobe는 보고에 표시되기 전에 데이터를 변경하거나 조작할 수 있는 다양한 방법을 제공합니다. 이 페이지에는 다양한 Adobe Analytics 기능이 데이터를 처리하는 순서가 표시됩니다. 이 목록을 사용하면 데이터 불일치 문제 해결이나 데이터 조정이 필요한 경우 사용할 최적의 기능을 결정할 수 있습니다.

![처리 순서 이미지](assets/processing-order.png)

## Adobe로 전송되기 전의 데이터

데이터가 Adobe로 전송되기 전에 일반적으로 다음 방법 중 하나를 사용하여 클라이언트측에서 컴파일됩니다.

* **AppMeasurement**: 사이트에서 호스팅되고 각 페이지에서 참조되는 JavaScript 파일. 데이터는 Adobe Analytics로 직접 전송됩니다.
* **Adobe Experience Platform Web SDK**: 사이트에서 호스팅되고 각 페이지에서 참조되는 JavaScript 파일. 데이터는 Adobe Experience Platform Edge Network으로 전송됩니다.
* **Adobe Experience Platform 데이터 수집의 태그**: 각 페이지에서 참조되는 JavaScript 파일로, 데이터 수집 UI 내에서 만들어진 규칙이 포함되어 있습니다. Adobe Analytics 확장을 사용하면 AppMeasurement를 보다 쉽게 구현할 수 있습니다. Web SDK 확장을 사용하면 Web SDK를 보다 쉽게 구현할 수 있습니다.
* **API**: AppMeasurement과 Edge Network은 모두 Adobe에 데이터를 보내기 위한 프로그래밍 방법을 제공합니다. AppMeasurement은 [데이터 삽입 API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-insertion/) 및 [대량 데이터 삽입 API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/)를 제공합니다. Edge Network은 [데이터 수집 API](https://developer.adobe.com/data-collection-apis/docs/)를 제공합니다.

Edge Network으로 데이터를 전송하는 경우 Adobe Analytics(및 기타 많은 Adobe Experience Cloud 솔루션)로 데이터를 전송하도록 구성할 수 있습니다. 구현 방법에 관계없이 수집된 히트 데이터는 최종적으로 구문 분석할 수 있는 형식으로 Adobe Analytics 처리 서버에 도달합니다.

## Adobe Analytics 컬렉션의 사전 처리

데이터가 Adobe Analytics에 도달하면 전처리 단계로 들어갑니다.

1. [**동적 변수**](/help/implement/vars/page-vars/dynamic-variables.md): 이미지 요청의 어느 부분에서든 동적 변수가 표시되면 값이 복사되어 향후 독립적인 값으로 처리됩니다.
1. [**IP 난독화(마지막 옥텟)**](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md): 보고서 세트가 마지막 옥텟만 난독화하도록 구성된 경우, 해당 난독화가 여기에 적용됩니다. IP 난독화(IP 제거)는 처리 파이프라인의 후반부에 발생합니다.
1. **조회 테이블**: Adobe 내부 조회 테이블에 의존하는 차원(예: [Browser](/help/components/dimensions/browser.md) 차원)이 해당 값과 일치합니다.
1. [**IP 제외**](/help/admin/tools/exclude-ip.md): 보고에서 명시적으로 제외하는 모든 IP 주소는 이 단계에서 플래그가 지정됩니다.
1. [**보트 규칙**](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md): 표준 또는 사용자 정의 보트 필터링을 적용하여 해당 데이터를 보고에서 제외합니다.
1. **지리적 위치 데이터**: IP 주소 조회에 의존하는 차원(예: [국가](/help/components/dimensions/countries.md) 차원)이 채워집니다.
1. [**처리 규칙**](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md): 조직에서 데이터에 적용하는 사용자 정의 규칙. 해당 Analytics 변수에 대한 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)의 매핑을 포함합니다.
1. [**VISTA 규칙**](vista.md): Adobe 컨설턴트가 데이터에 적용하는 유연한 사용자 정의 규칙. VISTA 규칙은 조직의 필요에 따라 처리 규칙 이전 또는 이후에 실행될 수 있습니다. 대부분의 VISTA 규칙은 일반적으로 처리 규칙 이후에 실행되지만 각 조직은 다르게 설정됩니다. 기존 VISTA 규칙에 대한 자세한 내용은 Adobe 계정 팀에 문의하십시오.
1. **통화 전환**: 히트에 보고서 세트의 통화와 다른 [`currencyCode`](/help/implement/vars/config-vars/currencycode.md)이(가) 포함된 경우 적용 가능한 모든 통화 변수가 현재 날짜의 환율을 사용하여 전환됩니다.
1. [**우편 번호**](/help/components/dimensions/zip-code.md): &#39;우편 번호&#39; 차원은 보고서 세트 설정을 기반으로 채워집니다.

## 데이터 수집 파이프라인의 &quot;중간 값&quot; 단계

사전 처리가 완료되면 여러 기능에서 &quot;중간 값&quot;이라고 하는 이 부분 처리된 데이터 형식을 사용합니다. 데이터가 어디에나 전송되기 전에 일부 중간 값별 처리가 적용됩니다.

1. [**히트 수준 마케팅 채널 처리 규칙**](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md): 이러한 처리 규칙은 특히 Analytics Source 커넥터에 대해 실행됩니다. 아직 방문 또는 방문자 수준 컨텍스트가 없으므로 이러한 처리 규칙은 히트가 방문의 첫 번째 히트가 아니라고 가정합니다. 히트에 대한 처리 규칙을 실행한 결과는 `channel.typeAtSource` 및 `channel._id`에서 사용할 수 있습니다.
1. [**IP 난독화(IP 제거)**](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md): 보고서 세트가 IP 주소를 완전히 난독화하도록 구성된 경우 해당 난독화가 여기에 적용됩니다(mid 값에만 해당).

이 시점에서 중간 값 데이터는 해당 기능으로 전송됩니다.

* [**Livestream API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/): 수집된 데이터 흐름을 위해 응용 프로그램을 Adobe의 livestream 서비스에 연결합니다.
* [**Analytics Source 커넥터**](https://experienceleague.adobe.com/ko/docs/experience-platform/sources/connectors/adobe-applications/analytics): Adobe Experience Platform 데이터 집합에서 Adobe Analytics 보고서 세트 데이터를 수집합니다.
* [**실시간 보고**](/help/components/c-real-time-reporting/realtime.md): Analysis Workspace에서 구성 가능한 실시간 보고서를 최대 3개까지 제공합니다.

## 방문 및 방문자 수준 처리

이 시점까지 주어진 히트에는 이전 또는 이후에 수집된 히트에 대한 지식이나 컨텍스트가 없습니다. 이 처리 단계는 방문 및 방문자 수준 필드를 채웁니다.

1. [**방문 + 방문자 정의**](/help/implement/id/overview.md): 히트는 포함된 방문자 변수를 기반으로 식별됩니다.
1. [**방문 횟수**](/help/components/dimensions/visit-number.md): 식별된 방문자의 다른 방문 횟수를 기반으로 방문 횟수가 계산됩니다.
1. **이벤트 중복 제거**: 히트에 중복 [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) 또는 [이벤트 직렬화](/help/implement/vars/page-vars/events/event-serialization.md)가 포함된 경우 해당 ID를 확인하고 각각 플래그를 지정합니다.
1. [**방문 수준 마케팅 채널 처리 규칙**](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md): 모든 히트는 마케팅 채널 처리 규칙을 통해 실행되며 히트가 규칙과 일치하는지 채널 + 채널 세부 정보가 결정됩니다. 이러한 규칙은 Analysis Workspace에서 사용할 수 있는 [마케팅 채널](/help/components/dimensions/marketing-channel.md) 및 [마케팅 채널 세부 정보](/help/components/dimensions/marketing-detail.md) 차원을 채웁니다.
1. **변수 지속성**: 지속성이 있는 차원(예: [eVars](/help/components/dimensions/evar.md))의 경우 이 단계에서 해당 값이 결정됩니다. 일반적으로 `post`개의 값이 여기에 설정됩니다.
1. **거래 ID**: 히트에 새 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 값이 포함된 경우 지원되는 모든 값의 &quot;스냅숏&quot;이 저장됩니다. 데이터 소스 업로드에 일치하는 트랜잭션 ID가 포함되어 있는 경우 이 스냅샷에서 지원되는 모든 값이 해당 데이터 소스 행에 포함됩니다.
1. [**IP 난독화(IP 제거)**](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md): 보고서 세트가 IP 주소를 완전히 난독화하도록 구성된 경우 다른 모든 처리가 완료된 후에 해당 난독화가 여기에 적용됩니다.

이 시점에서 개별 히트는 보고서 세트 데이터 테이블에 기록됩니다. 표준 [지연](latency.md) 시간이 경과하면 보고에서 사용할 수 있습니다.

## 데이터 처리 후 변경

Adobe Analytics의 데이터는 대부분 영구적이지만 선택적으로 데이터를 조정하거나 삭제할 수 있는 몇 가지 기능이 있습니다.

* [**데이터 복구 API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): 특정 열을 편집하거나 원하는 데이터 행을 삭제합니다.
* [**데이터 거버넌스**](/help/technotes/privacy/privacy-overview.md): 데이터를 영구적으로 삭제할 수 있도록 개인 정보 보호 요청을 수용합니다.
* [**분류**](/help/components/classifications/classifications-overview.md): 다양한 방식으로 데이터를 구성할 수 있는 규칙이나 업로드된 데이터를 기반으로 차원을 만듭니다. 기본 보고서 세트 데이터는 변경되지 않으므로 분류 데이터를 자유롭게 편집하거나 덮어쓸 수 있습니다.
* [**가상 보고서 세트**](/help/components/vrs/vrs-about.md): 방문 시간 제한을 변경할 수 있는 대체 보고서 세트 보기를 만듭니다.
