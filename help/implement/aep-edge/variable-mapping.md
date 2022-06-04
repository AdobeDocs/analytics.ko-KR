---
title: Adobe Experience Edge의 Analytics 변수 매핑
description: Edge가 자동으로 Analytics 변수에 매핑하는 XDM 필드를 봅니다.
source-git-commit: 984d62f6ece15ebbd41dbbd1e3cb800faa7f323b
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---


# Adobe Experience Edge의 Analytics 변수 매핑

다음 표는 Adobe Experience Platform Edge Network가 자동으로 Adobe Analytics에 매핑되는 변수를 보여줍니다. 이러한 XDM 필드 경로를 사용하는 경우 Adobe Analytics으로 데이터를 전송하는 데 추가 구성이 필요하지 않습니다.

| XDM 필드 패스 | Analytics 차원 및 설명 |
| --- | --- |
| `application.id` | 모바일 차원 [앱 ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.isClose` | 모바일 지표를 정의하는 데 도움이 됩니다 [충돌](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.closeType` | 닫기 이벤트가 충돌인지 여부를 결정합니다. 유효한 값은 다음과 같습니다 `close` (라이프사이클 세션이 종료되고 이전 세션에 대한 일시 중지 이벤트가 수신됨) 및 `unknown` ( 일시 중지 이벤트 없이 라이프사이클 세션이 종료됩니다.) |
| `application.isInstall` | 모바일 지표 [설치](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isLaunch` | 모바일 지표 [론치](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.name` | 모바일 차원을 설정하는 데 도움이 됩니다. [앱 ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.launches.value` | 모바일 지표 [론치](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isUpgrade` | 모바일 지표 [업그레이드](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.version` | 모바일 차원을 설정하는 데 도움이 됩니다. [앱 ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.sessionLength` | 모바일 지표 [총 세션 길이](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `commerce.checkouts.id` | 적용 [이벤트 일련화](../vars/page-vars/events/event-serialization.md) 변환 후 [체크아웃](../../components/metrics/checkouts.md) 지표. |
| `commerce.checkouts.value` | 를 증가시킵니다 [체크아웃](../../components/metrics/checkouts.md) 원하는 금액별 지표입니다. |
| `commerce.order.currencyCode` | 를 설정합니다. [currencyCode](../vars/config-vars/currencycode.md) 구성 변수. |
| `commerce.order.purchaseID` | 를 설정합니다. [purchaseID](../vars/page-vars/purchaseid.md) 페이지 변수를 채우는 방법을 설명합니다. |
| `commerce.productListAdds.id` | 적용 [이벤트 일련화](../vars/page-vars/events/event-serialization.md) 변환 후 [장바구니 추가](../../components/metrics/cart-additions.md) 지표. |
| `commerce.productListAdds.value` | 를 증가시킵니다 [장바구니 추가](../../components/metrics/cart-additions.md) 원하는 금액별 지표입니다. |
| `commerce.productListOpens.id` | 적용 [이벤트 일련화](../vars/page-vars/events/event-serialization.md) 변환 후 [장바구니](../../components/metrics/carts.md) 지표. |
| `commerce.productListOpens.value` | 를 증가시킵니다 [장바구니](../../components/metrics/carts.md) 원하는 금액별 지표입니다. |
| `commerce.productListRemovals.id` | 적용 [이벤트 일련화](../vars/page-vars/events/event-serialization.md) 변환 후 [장바구니 제거 수](../../components/metrics/cart-removals.md) 지표. |
| `commerce.productListRemovals.value` | 를 증가시킵니다 [장바구니 제거 수](../../components/metrics/cart-removals.md) 원하는 금액별 지표입니다. |
| `commerce.productListViews.id` | 적용 [이벤트 일련화](../vars/page-vars/events/event-serialization.md) 변환 후 [장바구니 보기 수](../../components/metrics/cart-views.md) 지표. |
| `commerce.productListViews.value` | 를 증가시킵니다 [장바구니 보기 수](../../components/metrics/cart-views.md) 원하는 금액별 지표입니다. |
| `commerce.productViews.id` | 적용 [이벤트 일련화](../vars/page-vars/events/event-serialization.md) 변환 후 [제품 보기](../../components/metrics/product-views.md) 지표. |
| `commerce.productViews.value` | 를 증가시킵니다 [제품 보기](../../components/metrics/product-views.md) 원하는 금액별 지표입니다. |
| `commerce.purchases.value` | 를 증가시킵니다 [주문](../../components/metrics/orders.md) 원하는 금액별 지표입니다. |
| `device.manufacturer` | 모바일 장치 제조업체입니다. |
| `device.model` | 모바일 차원 [장치 이름](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `device.modelNumber` | 모바일 장치 모델 번호입니다. |
| `device.colorDepth` | 은(는) [색상 깊이](../../components/dimensions/color-depth.md) 차원. |
| `device.screenHeight` | 은(는) [모니터 해상도](../../components/dimensions/monitor-resolution.md) 차원. XDM 필드도 설정해야 합니다 `device.screenWidth`. |
| `device.screenWidth` | 은(는) [모니터 해상도](../../components/dimensions/monitor-resolution.md) 차원. XDM 필드도 설정해야 합니다 `device.screenHeight`. |
| `device.type` | 모바일 장치 유형입니다. |
| `environment.browserDetails.acceptLanguage` | 은(는) [언어](../../components/dimensions/language.md) 차원. |
| `environment.browserDetails.cookiesEnabled` | 를 설정합니다. [쿠키 지원](../../components/dimensions/cookie-support.md) 차원. 유효한 값은 다음과 같습니다 `Y` (브라우저가 쿠키를 승인함) 및 `N` (브라우저가 쿠키를 거부함). |
| `environment.browserDetails.javaEnabled` | 를 설정합니다. [Java 활성화](../../components/dimensions/java-enabled.md) 차원. 유효한 값은 다음과 같습니다 `Y` (Java가 활성화됨) 및 `N` (Java가 비활성화되어 있습니다.) |
| `environment.browserDetails.userAgent` | 폴백으로 사용됨 [고유 방문자](../../components/metrics/unique-visitors.md) 식별 방법. 일반적으로 을 사용하여 채워집니다 `User-Agent` HTTP 요청 헤더. 보고서에서 사용하려면 이 필드를 eVar에 매핑할 수 있습니다. |
| `environment.browserDetails.viewportHeight` | 를 설정합니다. [브라우저 높이](../../components/dimensions/browser-height.md) 차원. |
| `environment.browserDetails.viewportWidth` | 를 설정합니다. [브라우저 너비](../../components/dimensions/browser-width.md) 차원. |
| `environment.carrier` | 모바일 차원 [통신사 이름](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.connectionType` | 은(는) [연결 유형](../../components/dimensions/connection-type.md) 차원. |
| `environment.ipV4` | 폴백으로 사용됨 [고유 방문자](../../components/metrics/unique-visitors.md) 식별 방법. 일반적으로 을 사용하여 채워집니다 `X-Forwarded-For` HTTP 헤더. |
| `environment.language` | 모바일 차원 로케일입니다. |
| `environment.operatingSystem` | 모바일 차원 [운영 체제](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.operatingSystemVersion` | 모바일 차원 [운영 체제 버전](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.type` | 이벤트가 [착용형](https://experienceleague.adobe.com/docs/mobile-services/android/wearables-android/c-android-wearables--additional-notes.html) 장치. 유효한 값은 다음과 같습니다 `Application` (앱에서 발생함), `Extension` (이벤트는 웨어러블 앱에서 발생함) 또는 `Widget` (이 이벤트는 모바일 위젯에서 발생함). |
| `identityMap.ECID[0].id` | 다음 [Adobe Experience Cloud Identity 서비스 ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| `marketing.trackingCode` | 를 설정합니다. [추적 코드](../../components/dimensions/tracking-code.md) 차원. |
| `media.mediaTimed.completes.value` | Media Analytics 지표 [컨텐츠 완료](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-complete). |
| `media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `media.mediaTimed.federated.value` | Media Analytics 지표 [페더레이션 데이터](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#federated-data). |
| `media.mediaTimed.firstQuartiles.value` | Media Analytics 지표 [25% 진행률 마커](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#twenty-five-progress-marker). |
| `media.mediaTimed.mediaSegmentView.value` | Media Analytics 지표 [컨텐츠 세그먼트 보기 수](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment-views). |
| `media.mediaTimed.midpoints.value` | Media Analytics 지표 [50% 진행률 마커](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#fifty-progress-marker). |
| `media.mediaTimed.pauseTime.value` | Media Analytics 지표 [총 일시 중지 기간](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#total-pause-duration). |
| `media.mediaTimed.pauses.value` | Media Analytics 지표 [이벤트 일시 중지](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#pause-events). |
| `media.mediaTimed.primaryAssetReference.@id` | Media Analytics 차원 [자산 ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#asset-id). |
| `media.mediaTimed.primaryAssetReference.dc:title` | Media Analytics 차원 [비디오 이름](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-name). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | Media Analytics 차원 [작성자](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#originator). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Episode.iptc4xmpExt:Number` | Media Analytics 차원 [에피소드](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#episode). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Genre` | Media Analytics 차원 [장르](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#genre). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | Media Analytics 차원 [컨텐츠 등급](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-rating). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Season.iptc4xmpExt:Number` | Media Analytics 차원 [시즌](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#season). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Series.iptc4xmpExt:Identifier` | Media Analytics 차원 [컨텐츠 ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-id). |
| `media.mediaTimed.primaryAssetReference.iptc4xmpExt:Series.iptc4xmpExt:Name` | Media Analytics 차원 [표시](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show). |
| `media.mediaTimed.primaryAssetReference.showType` | Media Analytics 차원 [표시 유형](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show-type). |
| `media.mediaTimed.primaryAssetReference.xmpDM:duration` | Media Analytics 차원 [비디오 길이](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-length). |
| `media.mediaTimed.primaryAssetViewDetails.@id` | Media Analytics 차원 [미디어 세션 ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-session-id). |
| `media.mediaTimed.primaryAssetViewDetails.broadcastChannel` | Media Analytics 차원 [컨텐츠 채널](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-channel). |
| `media.mediaTimed.primaryAssetViewDetails.broadcastContentType` | Media Analytics 차원 [컨텐츠 유형](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-type). |
| `media.mediaTimed.primaryAssetViewDetails.broadcastNetwork` | Media Analytics 차원 [네트워크](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#network). |
| `media.mediaTimed.primaryAssetViewDetails.mediaSegmentView.value` | Media Analytics 차원 [컨텐츠 세그먼트](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment). |
| `media.mediaTimed.primaryAssetViewDetails.playerName` | Media Analytics 차원 [컨텐츠 플레이어 이름](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-player-name). |
| `media.mediaTimed.primaryAssetViewDetails.playerSDKVersion.version` | Media Analytics 차원 [SDK 버전](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#sdk-version). |
| `media.mediaTimed.primaryAssetViewDetails.sourceFeed` | Media Analytics 차원 [미디어 피드 유형](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-feed-type). |
| `media.mediaTimed.primaryAssetViewDetails.streamFormat` | Media Analytics 차원 [스트림 형식](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#stream-format). |
| `media.mediaTimed.progress10.value` | Media Analytics 지표 [10% 진행률 마커](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ten-progress-marker). |
| `media.mediaTimed.progress95.value` | Media Analytics 지표 [95% 진행률 마커](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ninety-five-progress-marker). |
| `media.mediaTimed.resumes.value` | Media Analytics 지표 [컨텐츠 다시 시작](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-resumes). |
| `media.mediaTimed.starts.value` | Media Analytics 지표 [미디어 시작](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-starts). |
| `media.mediaTimed.thirdQuartiles.value` | Media Analytics 지표 [75% 진행률 마커](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#seventy-five-progress-marker). |
| `media.mediaTimed.timePlayed.value` | Media Analytics 지표 [컨텐츠 체류 시간](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-time-spent). |
| `media.mediaTimed.totalTimePlayed.value` | Media Analytics 지표 [미디어 체류 시간](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-time-spent). |
| `placeContext.geo.latitude` | 모바일 차원 위도입니다. |
| `placeContext.geo.longitude` | 모바일 차원 경도입니다. |
| `placeContext.geo.postalCode` | 다음 [우편 번호](../../components/dimensions/zip-code.md) 차원. |
| `placeContext.geo.stateProvince` | 다음 [미국 주](../../components/dimensions/us-states.md) 차원. |
| `productListItems[N].lineItemId` | 다음 [카테고리](../../components/dimensions/category.md) 차원. |
| `productlistitems[N].name` | 다음 [제품](../../components/dimensions/product.md) 차원. |
| `productlistitems[N].priceTotal` | 은(는) [매출](../../components/metrics/revenue.md) 지표. |
| `productlistitems[N].quantity` | 은(는) [판매량](../../components/metrics/units.md) 지표. |
| `web.webInteraction.URL` | 다음 [linkURL](../vars/config-vars/linkurl.md) 구현 변수 입니다. |
| `web.webInteraction.name` | 다음 [사용자 지정 링크](../../components/dimensions/custom-link.md), [다운로드 링크](../../components/dimensions/download-link.md), 또는 [종료 링크](../../components/dimensions/exit-link.md) 차원, 의 값에 따라 `web.webInteraction.type` |
| `web.webInteraction.type` | 클릭한 링크의 유형을 결정합니다. 유효한 값은 다음과 같습니다 `lnk_o` (사용자 지정 링크), `lnk_d` (다운로드 링크) 및 `lnk_e` (종료 링크). |
| `web.webPageDetails.URL` | 다음 [페이지 URL](../../components/dimensions/page-url.md) 차원. |
| `web.webPageDetails.errorPage` | &#39;페이지를 찾을 수 없음&#39;을 결정하는 데 도움이 되는 플래그 [차원](../../components/dimensions/pages-not-found.md) 및 [지표](../../components/metrics/pages-not-found.md). |
| `web.webPageDetails.name` | 다음 [페이지](../../components/dimensions/page.md) 차원. |
| `web.webPageDetails.server` | 다음 [서버](../../components/dimensions/server.md) 차원. |
| `web.webPageDetails.siteSection` | 다음 [사이트 섹션](../../components/dimensions/site-section.md) 차원. |
| `web.webReferrer.URL` | 다음 [레퍼러](../../components/dimensions/referrer.md) 차원. |

{style=&quot;table-layout:auto&quot;}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## 다른 XDM 필드를 Analytics 변수에 매핑

Adobe Analytics에 추가하려는 차원 또는 지표가 있는 경우 다음을 통해 추가할 수 있습니다 [컨텍스트 데이터 변수](../vars/page-vars/contextdata.md). 모든 XDM 필드 요소는 접두사가 있는 컨텍스트 데이터로 Adobe Analytics에 전송됩니다 `a.x`. 그런 다음 을 사용하여 이 컨텍스트 데이터 변수를 원하는 Analytics 변수에 매핑할 수 있습니다 [처리 규칙](../../admin/admin/c-processing-rules/processing-rules.md). 예를 들어 다음 이벤트를 전송하는 경우

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

웹 SDK는 해당 데이터를 컨텍스트 데이터 변수로 Adobe Analytics에 전송합니다 `a.x._atag.search.term`. 그런 다음 처리 규칙을 사용하여 컨텍스트 데이터 변수 값을 원하는 Analytics 변수(예: eVar)에 할당할 수 있습니다.

![검색어 처리 규칙](assets/examplerule.png)
