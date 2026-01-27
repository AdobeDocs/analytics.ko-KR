---
title: Adobe Analytics로 XDM 오브젝트 변수 매핑
description: Edge가 Analytics 변수에 자동으로 매핑하는 XDM 필드를 봅니다.
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
feature: Implementation Basics
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 100%

---

# Adobe Analytics로 XDM 오브젝트 변수 매핑

다음 테이블에서는 Adobe Experience Platform Edge Network를 Adobe Analytics에 자동으로 매핑하는 XDM 변수를 보여 줍니다. 이러한 XDM 필드 경로를 사용하는 경우 Adobe Analytics로 데이터를 전송하기 위해 추가 구성이 필요하지 않습니다. 이러한 필드는 **[!UICONTROL Adobe Analytics ExperienceEvent 템플릿]** 필드 그룹에 포함됩니다. 데이터를 Adobe Analytics와 Adobe Experience Platform에 전송하려는 경우 이러한 필드를 사용하는 것이 좋습니다.

조직이 Customer Journey Analytics로 전환할 계획이라면, Adobe는 스키마를 따르지 않고 `data` 오브젝트를 사용하여 데이터를 Adobe Analytics로 직접 전송하는 것이 좋습니다. 이 전략을 사용하면 조직은 [!UICONTROL Adobe Analytics ExperienceEvent Template]&#x200B;(Customer Journey Analytics에는 덜 적용됨) 대신 고유한 스키마를 사용할 수 있습니다. 유사한 매핑 테이블이 필요하면 [Adobe Analytics에 대한 데이터 오브젝트 변수 매핑](data-var-mapping.md)을 참조하십시오.

## 값 우선순위

이 테이블의 XDM 오브젝트 필드는 대부분 [데이터 오브젝트 필드](data-var-mapping.md)와 일치합니다. 지정된 XDM 오브젝트 필드와 해당 데이터 오브젝트 필드를 모두 설정하면 데이터 오브젝트 필드가 우선합니다. Adobe XDM 오브젝트 필드와 데이터 오브젝트 필드를 모두 사용하는 경우 데이터 오브젝트 필드를 사용하여 사용자 정의 이벤트를 설정하는 것이 좋습니다. 필드 `data.__adobe.analytics.events`가 있으면 상거래 및 사용자 정의 이벤트와 관련된 모든 XDM 오브젝트 필드를 덮어씁니다.

## XDM 오브젝트 필드 매핑

이 테이블에 대한 이전 업데이트는 이 페이지의 [GitHub의 커밋 기록](https://github.com/AdobeDocs/analytics.ko-KR/commits/main/help/implement/aep-edge/xdm-var-mapping.md)에서 확인할 수 있습니다.

| XDM 필드 경로 | Analytics 변수 및 설명 |
| --- | --- |
| `xdm.application.isClose` | 모바일 라이프사이클 지표 [충돌](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/)을 정의하는 데 도움이 됩니다. |
| `xdm.application.isInstall` | 모바일 라이프사이클 지표 [첫 실행](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/)을 늘릴 시기를 결정하는 데 도움이 됩니다. |
| `xdm.application.closeType` | 닫기 이벤트가 충돌인지 여부를 결정합니다. 유효한 값은 `close`(라이프사이클 세션이 종료되고 이전 세션에 대해 일시 중지 이벤트가 수신됨) 및 `unknown`(라이프사이클 세션이 일시 중지 이벤트 없이 종료됨)입니다. 모바일 라이프사이클 지표 [충돌](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/) 지표를 설정하는 데 도움이 됩니다. |
| `xdm.application.isInstall` | 모바일 라이프사이클 지표 [설치](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.isLaunch` | 모바일 라이프사이클 지표 [런치](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.name` | 모바일 라이프사이클 차원 [앱 ID](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/)를 설정하는 데 도움이 됩니다. |
| `xdm.application.isUpgrade` | 모바일 라이프사이클 지표 [업그레이드](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.version` | 모바일 라이프사이클 차원 [앱 ID](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/)를 설정하는 데 도움이 됩니다. |
| `xdm.application.sessionLength` | 모바일 라이프사이클 지표 [이전 세션 길이](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.commerce.checkouts.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 [체크아웃](/help/components/metrics/checkouts.md) 지표에 적용합니다. |
| `xdm.commerce.checkouts.value` | 원하는 수량만큼 [체크아웃](/help/components/metrics/checkouts.md) 지표를 증가시킵니다. |
| `xdm.commerce.order.currencyCode` | [currencyCode](../vars/config-vars/currencycode.md) 구성 변수를 설정합니다. |
| `xdm.commerce.order.purchaseID` | [purchaseID](../vars/page-vars/purchaseid.md) 페이지 변수를 설정합니다. |
| `xdm.commerce.order.payments[0].transactionID` | [transactionID](../vars/page-vars/transactionid.md) 페이지 변수를 설정합니다. |
| `xdm.commerce.productListAdds.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 [장바구니 추가](/help/components/metrics/cart-additions.md) 지표에 적용합니다. |
| `xdm.commerce.productListAdds.value` | [장바구니 추가](/help/components/metrics/cart-additions.md) 지표를 증가시킵니다. |
| `xdm.commerce.productListOpens.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 [장바구니](/help/components/metrics/carts.md) 지표에 적용합니다. |
| `xdm.commerce.productListOpens.value` | [장바구니 수](/help/components/metrics/carts.md) 지표를 증가시킵니다. |
| `xdm.commerce.productListRemovals.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 [장바구니 제거](/help/components/metrics/cart-removals.md) 지표에 적용합니다. |
| `xdm.commerce.productListRemovals.value` | [장바구니 제거 수](/help/components/metrics/cart-removals.md) 지표를 증가시킵니다. |
| `xdm.commerce.productListViews.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 [장바구니 보기](/help/components/metrics/cart-views.md) 지표에 적용합니다. |
| `xdm.commerce.productListViews.value` | [장바구니 보기 수](/help/components/metrics/cart-views.md) 지표를 증가시킵니다. |
| `xdm.commerce.productViews.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 [제품 보기](/help/components/metrics/product-views.md) 지표에 적용합니다. |
| `xdm.commerce.productViews.value` | [제품 보기](/help/components/metrics/product-views.md) 지표를 증가시킵니다. |
| `xdm.commerce.purchases.value` | [주문](/help/components/metrics/orders.md) 지표를 증가시킵니다. |
| `xdm.device.model` | 모바일 라이프사이클 차원 [디바이스 이름](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.device.colorDepth` | [색상 심도](/help/components/dimensions/color-depth.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.device.screenHeight` | [모니터 해상도](/help/components/dimensions/monitor-resolution.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.device.screenWidth` | [모니터 해상도](/help/components/dimensions/monitor-resolution.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.device.type` | 모바일 디바이스 유형. |
| `xdm.environment.browserDetails.acceptLanguage` | [언어](/help/components/dimensions/language.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.environment.browserDetails.cookiesEnabled` | [쿠키 지원](/help/components/dimensions/cookie-support.md) 차원을 설정합니다. 유효한 값에는 `Y`(브라우저에서 쿠키를 수락) 및 `N`(브라우저에서 쿠키를 거부)이 포함됩니다. |
| `xdm.environment.browserDetails.javaEnabled` | [Java 활성화](/help/components/dimensions/java-enabled.md) 차원을 설정합니다. 유효한 값에는 `Y`(Java가 활성화됨) 및 `N`(Java가 비활성화됨)이 포함됩니다. |
| `xdm.environment.browserDetails.userAgent` | 대체 [고유 방문자](/help/components/metrics/unique-visitors.md) 식별 방법으로 사용됩니다 일반적으로 `User-Agent` HTTP 요청 헤더를 사용하여 채워집니다. 보고서에서 이 필드를 사용하려는 경우 이 필드를 eVar에 매핑할 수 있습니다. |
| `xdm.environment.browserDetails.viewportHeight` | [브라우저 높이](/help/components/dimensions/browser-height.md) 차원을 설정합니다. |
| `xdm.environment.browserDetails.viewportWidth` | [브라우저 너비](/help/components/dimensions/browser-width.md) 차원을 설정합니다. |
| `xdm.environment.carrier` | 모바일 라이프사이클 차원 [통신사 이름](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.environment.connectionType` | [연결 유형](/help/components/dimensions/connection-type.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.environment._dc.language` | 컨텍스트 데이터 변수 `a.locale`을 설정합니다. `xdm.environment.language`가 설정되지 않은 경우에만 사용됩니다. Adobe는 `xdm.environment.language` 보다 이 필드를 사용할 것이 좋습니다. |
| `xdm.environment.ipV4` | 대체 [고유 방문자](/help/components/metrics/unique-visitors.md) 식별 방법으로 사용됩니다 일반적으로 `X-Forwarded-For` HTTP 헤더를 사용하여 채워집니다. |
| `xdm.environment.language` | 컨텍스트 데이터 변수 `a.locale`을 설정합니다. Adobe는 대신 `xdm.environment._dc.language`를 사용하는 것을 추천합니다. |
| `xdm.environment.operatingSystem` | 모바일 라이프사이클 차원 [운영 체제](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.environment.operatingSystemVersion` | 모바일 라이프사이클 차원 [운영 체제 버전](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/)을 설정하는 데 도움이 됩니다. |
| `xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar250` | 해당 [eVar](/help/components/dimensions/evar.md) 차원을 설정합니다. |
| `xdm._experience.analytics.customDimensions.`<br/>`hierarchies.hier1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`hierarchies.hier5` | 해당 [계층](/help/components/dimensions/hierarchy.md) 차원을 설정합니다. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | 목록 Prop 구분 기호 재정의 구분 기호는 보고서 세트 설정의 [트래픽 변수 관리자](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md)에서 자동으로 검색되므로 이 필드를 사용하는 것은 권장되지 않습니다. 이 필드를 사용하면 사용된 구분 기호와 Analytics에서 예상하는 구분 기호가 일치하지 않을 수 있습니다. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.values`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | 해당 [목록 Prop](../vars/page-vars/prop.md#list-props) 값을 포함하는 문자열 배열입니다. |
| `xdm._experience.analytics.customDimensions.`<br/>`lists.list1.list[].value`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | `value`각 배열의 모든 문자열`list[]`을 해당 [목록 변수](../vars/page-vars/list.md)에 연결합니다. 구분 기호는 [보고서 세트 설정](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md)에 설정된 값을 기준으로 자동으로 선택됩니다. |
| `xdm._experience.analytics.customDimensions.`<br/>`props.prop1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`props.prop75` | 해당 [Prop](/help/components/dimensions/prop.md) 차원을 설정합니다. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.id`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.id` | [이벤트 일련화](../vars/page-vars/events/event-serialization.md)를 해당 [사용자 정의 이벤트](/help/components/metrics/custom-events.md) 지표에 적용합니다. 각 이벤트 ID는 100개의 상위 그룹에 있습니다. 예를 들어 직렬화를 `event678`에 적용하려면 `xdm._experience.analytics.event601to700.event678.id`를 사용합니다. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.value`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.value` | 원하는 수량만큼 해당 [사용자 정의 이벤트](/help/components/metrics/custom-events.md) 지표를 증가시킵니다. 각 이벤트는 100개의 상위 그룹에 있습니다. 예를 들어 `event567`에 대한 필드는 `xdm._experience.analytics.event501to600.event567.value`입니다. |
| `xdm.identityMap.ECID[0].id` | [Adobe Experience Cloud ID 서비스 ID](https://experienceleague.adobe.com/kr/docs/id-service/using/home). |
| `xdm.marketing.trackingCode` | [추적 코드](/help/components/dimensions/tracking-code.md) 차원을 설정합니다. |
| `xdm.media.mediaTimed.completes.value` | 스트리밍 미디어 서비스 지표 [콘텐츠 완료](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-complete). |
| `xdm.media.mediaTimed.dropBeforeStart.value` | `a.media.view`, `a.media.timePlayed`, `a.media.play` |
| `xdm.media.mediaTimed.federated.value` | 스트리밍 미디어 서비스 지표 [페더레이션된 데이터](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#federated-data). |
| `xdm.media.mediaTimed.firstQuartiles.value` | 스트리밍 미디어 서비스 지표 [25% 진행률 마커](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#twenty-five--progress-marker). |
| `xdm.media.mediaTimed.mediaSegmentView.value` | 스트리밍 미디어 서비스 지표 [콘텐츠 세그먼트 조회수](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-segment-views). |
| `xdm.media.mediaTimed.midpoints.value` | 스트리밍 미디어 서비스 지표 [50% 진행률 마커](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#progress-marker). |
| `xdm.media.mediaTimed.pauseTime.value` | 스트리밍 미디어 서비스 지표 [총 일시 중지 기간](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#total-pause-duration). |
| `xdm.media.mediaTimed.pauses.value` | 스트리밍 미디어 서비스 지표 [일시 중지 이벤트](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#pause-events). |
| `xdm.mediaCollection.sessionDetails.assetID` | 스트리밍 미디어 서비스 차원 [자산 ID](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#asset-id). |
| `xdm.mediaCollection.sessionDetails.friendlyName` | 스트리밍 미디어 서비스 차원 [비디오 이름](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#video-name). |
| `xdm.mediaCollection.sessionDetails.originator` | 스트리밍 미디어 서비스 차원 [작성자](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#originator). |
| `xdm.mediaCollection.sessionDetails.episode` | 스트리밍 미디어 서비스 차원 [에피소드](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#episode). |
| `xdm.mediaCollection.sessionDetails.genre` | 스트리밍 미디어 서비스 차원 [장르](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#genre). |
| `xdm.mediaCollection.sessionDetails.rating` | 스트리밍 미디어 서비스 차원 [콘텐츠 등급](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-rating). |
| `xdm.mediaCollection.sessionDetails.season` | 스트리밍 미디어 서비스 차원 [시즌](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#season). |
| `xdm.mediaCollection.sessionDetails.name` | 스트리밍 미디어 서비스 차원 [콘텐츠 ID](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-id). |
| `xdm.mediaCollection.sessionDetails.show` | 스트리밍 미디어 서비스 차원 [표시](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#show). |
| `xdm.mediaCollection.sessionDetails.showType` | 스트리밍 미디어 서비스 차원 [표시 유형](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#show-type). |
| `xdm.mediaCollection.sessionDetails.length` | 스트리밍 미디어 서비스 차원 [비디오 길이](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#video-length). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.@id` | 스트리밍 미디어 서비스 차원[미디어 세션 ID](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-session-id). |
| `xdm.mediaCollection.sessionDetails.channel` | 스트리밍 미디어 서비스 차원 [콘텐츠 채널](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-channel). |
| `xdm.mediaCollection.sessionDetails.contentType` | 스트리밍 미디어 서비스 차원 [콘텐츠 유형](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-type). |
| `xdm.mediaCollection.sessionDetails.network` | 스트리밍 미디어 서비스 차원 [네트워크](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#network). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | 스트리밍 미디어 서비스 차원 [콘텐츠 세그먼트](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-segment). |
| `xdm.mediaCollection.sessionDetails.playerName` | 스트리밍 미디어 서비스 차원 [콘텐츠 플레이어 이름](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-player-name). |
| `xdm.mediaCollection.sessionDetails.appVersion` | 스트리밍 미디어 서비스 차원 [SDK 버전](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#sdk-version). |
| `xdm.mediaCollection.sessionDetails.feed` | 스트리밍 미디어 서비스 차원 [미디어 피드 유형](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-feed-type). |
| `xdm.mediaCollection.sessionDetails.streamFormat` | 스트리밍 미디어 서비스 차원 [스트림 포맷](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#stream-format). |
| `xdm.media.mediaTimed.progress10.value` | 스트리밍 미디어 서비스 지표 [10% 진행률 마커](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#ten--progress-marker). |
| `xdm.media.mediaTimed.progress95.value` | 스트리밍 미디어 서비스 지표 [95% 진행률 마커](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#ninety-five--progress-marker). |
| `xdm.mediaCollection.sessionDetails.hasResume` | 스트리밍 미디어 서비스 지표 [콘텐츠 다시 시작](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-resumes). |
| `xdm.media.mediaTimed.starts.value` | 스트리밍 미디어 서비스 지표 [미디어 시작](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-starts). |
| `xdm.media.mediaTimed.thirdQuartiles.value` | 스트리밍 미디어 서비스 지표 [75% 진행률 마커](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#seventy-five--progress-marker). |
| `xdm.media.mediaTimed.timePlayed.value` | 스트리밍 미디어 서비스 지표 [콘텐츠 체류 시간](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-time-spent). |
| `xdm.media.mediaTimed.totalTimePlayed.value` | 스트리밍 미디어 서비스 지표 [미디어 사용 시간](https://experienceleague.adobe.com/kr/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-time-spent). |
| `xdm.placeContext.geo._schema.latitude` | 방문자의 위도 위치. [모바일 라이프사이클 위치](/help/components/dimensions/lifecycle-dimensions.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.placeContext.geo._schema.longitude` | 방문자의 경도 위치. [모바일 라이프사이클 위치](/help/components/dimensions/lifecycle-dimensions.md) 차원을 설정하는 데 도움이 됩니다. |
| `xdm.placeContext.geo.postalCode` | [우편번호](/help/components/dimensions/zip-code.md) 차원. |
| `xdm.placeContext.geo.stateProvince` | [미국 주](/help/components/dimensions/us-states.md) 차원. |
| `xdm.placeContext.localTime` | [데이터 피드](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md)에 `t_time_info`로 표시됩니다. |
| `xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | [제품 구문](../vars/page-vars/products.md) 머천다이징을 eVar에 적용합니다. |
| `xdm.productListItems[]._experience.analytics.`<br/>`event1to100.event1.value`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | [제품 구문](../vars/page-vars/products.md) 머천다이징을 이벤트에 적용합니다. |
| `xdm.productListItems[].productCategories[].categoryID` | [카테고리](/help/components/dimensions/category.md) 차원. [제품](../vars/page-vars/products.md) 페이지 변수도 참조하십시오. |
| `xdm.productListItems[].name` | [제품](/help/components/dimensions/product.md) 차원. [제품](../vars/page-vars/products.md) 페이지 변수도 참조하십시오. `xdm.productListItems[].SKU` 및 `xdm.productListItems[].name`에 모두 데이터가 포함되어 있으면 `xdm.productListItems[].SKU`의 값이 사용됩니다. |
| `xdm.productListItems[].priceTotal` | [매출](/help/components/metrics/revenue.md) 지표를 확인하는 데 도움이 됩니다. [제품](../vars/page-vars/products.md) 페이지 변수도 참조하십시오. |
| `xdm.productListItems[].quantity` | [단위](/help/components/metrics/units.md) 지표를 확인하는 데 도움이 됩니다. [제품](../vars/page-vars/products.md) 페이지 변수도 참조하십시오. |
| `xdm.productListItems[].SKU` | [제품](/help/components/dimensions/product.md) 차원. [제품](../vars/page-vars/products.md) 페이지 변수도 참조하십시오. `xdm.productListItems[].SKU` 및 `xdm.productListItems[].name`에 모두 데이터가 포함되어 있으면 `xdm.productListItems[].SKU`의 값이 사용됩니다. |
| `xdm.web.webInteraction.URL` | [linkURL](../vars/config-vars/linkurl.md) 구현 변수. |
| `xdm.web.webInteraction.name` | `xdm.web.webInteraction.type`의 값에 따라 [사용자 정의 링크](/help/components/dimensions/custom-link.md), [다운로드 링크](/help/components/dimensions/download-link.md) 또는 [종료 링크](/help/components/dimensions/exit-link.md) 차원. |
| `xdm.web.webInteraction.type` | 클릭한 링크의 유형을 결정합니다. 유효한 값에는 `other`(사용자 정의 링크), `download`(다운로드 링크) 및 `exit`(종료 링크)가 포함됩니다. |
| `xdm.web.webPageDetails.URL` | [페이지 URL](/help/components/dimensions/page-url.md) 차원. |
| `xdm.web.webPageDetails.isErrorPage` | &#39;페이지를 찾을 수 없음&#39; [차원](/help/components/dimensions/pages-not-found.md) 및 [지표](/help/components/metrics/pages-not-found.md)를 결정하는 데 도움이 되는 플래그. |
| `xdm.web.webPageDetails.name` | [페이지](/help/components/dimensions/page.md) 차원. |
| `xdm.web.webPageDetails.server` | [서버](/help/components/dimensions/server.md) 차원. |
| `xdm.web.webPageDetails.siteSection` | [사이트 섹션](/help/components/dimensions/site-section.md) 차원. |
| `xdm.web.webReferrer.URL` | [레퍼러](/help/components/dimensions/referrer.md) 차원. |

{style="table-layout:auto"}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Analytics 변수에 다른 XDM 필드 매핑

Adobe Analytics에 추가할 차원 또는 지표가 있는 경우 [컨텍스트 데이터 변수](../vars/page-vars/contextdata.md)를 통해 추가할 수 있습니다.

### 암시적 매핑

자동으로 매핑되지 않은 모든 XDM 필드 요소는 `a.x.` 접두사가 있는 컨텍스트 데이터로 Adobe Analytics에 전송됩니다. 그런 다음 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)을 사용하여 이 컨텍스트 데이터 변수를 원하는 Analytics 변수에 매핑할 수 있습니다. 예를 들어 다음 이벤트를 전송하는 경우:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "search":{
                "term":"Example search term"
            }
        }
    }
})
```

Web SDK는 해당 데이터를 Adobe Analytics에 컨텍스트 데이터 변수 `a.x._atag.search.term`으로 전송합니다. 그런 다음 처리 규칙을 사용하여 해당 컨텍스트 데이터 변수 값을 `eVar` 같은 원하는 Analytics 변수에 할당할 수 있습니다.

![검색어 처리 규칙](assets/examplerule.png)

## 명시적 매핑

XDM 필드 요소를 컨텍스트 데이터로 명시적으로 매핑할 수도 있습니다. `contextData` 요소를 사용하여 명시적으로 매핑된 모든 XDM 필드 요소는 접두사 없이 컨텍스트 데이터로 Adobe Analytics에 전송됩니다. 그런 다음 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)을 사용하여 이 컨텍스트 데이터 변수를 원하는 Analytics 변수에 매핑할 수 있습니다. 예를 들어 다음 이벤트를 전송하는 경우:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "analytics": {
                "contextData" : {
                    "someValue" : "1"
                }
            }
        }
    }
})
```

웹 SDK는 해당 데이터를 값 `1`이 포함된 컨텍스트 데이터 변수 `somevalue`로 Adobe Analytics에 전송합니다.  그런 다음 처리 규칙을 사용하여 해당 컨텍스트 데이터 변수 값을 `eVar` 같은 원하는 Analytics 변수에 할당할 수 있습니다.

![검색어 처리 규칙](assets/examplerule-explicit.png)
