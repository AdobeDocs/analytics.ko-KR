---
title: 데이터 수집 쿼리 매개 변수
description: 이미지 요청에 사용된 모든 쿼리 문자열 매개 변수를 나열합니다.
translation-type: tm+mt
source-git-commit: edf3ac3ebc99444b86bcd9239cef9ed84d797565
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 75%

---


# 데이터 수집 쿼리 매개 변수

다음 표에는 Adobe가 이미지 요청에 사용하는 모든 쿼리 문자열 매개 변수가 나와 있습니다. 이 정보는 [패킷 분석기](packet-monitor.md)를 사용하여 디버깅하거나, [이미지 요청을 하드코딩](../other/hardcoded.md)하거나, [동적 변수](../vars/page-vars/dynamic-variables.md)를 사용할 때 사용할 수 있습니다.

| 매개 변수 | Analytics 구현 변수 | 설명 |
| --- | --- | --- |
| `aamlh` | 없음 | Audience Manager 위치 힌트. Experience Cloud 공유 프로필 통합에 사용됩니다. |
| `aamb` | 없음 | Audience Manager Blob. Experience Cloud 공유 프로필 통합에 사용됩니다. |
| `aid` | 없음 | Analytics 방문자 ID. |
| `AQB` | 없음 | 이미지 요청 쿼리 문자열의 시작을 나타냅니다. |
| `AQE` | 없음 | 이미지 요청의 끝, 즉 요청이 잘리지 않았음을 나타냅니다. |
| `bh` | 없음 | 브라우저 높이(픽셀 단위). Used in the [Browser height](/help/components/dimensions/browser-height.md) dimension. |
| `bw` | 없음 | 브라우저 너비(픽셀 단위). Used in the [Browser width](/help/components/dimensions/browser-width.md) dimension. |
| `c` | 없음 | 색상 품질(비트). Used in the [Color depth](/help/components/dimensions/color-depth.md) dimension. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | 컨텍스트 데이터 변수의 시작을 나타냅니다. 값을 포함하지 않습니다. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | 컨텍스트 데이터 변수의 끝을 나타냅니다. 값을 포함하지 않습니다. |
| `c1` - `c75` | [`prop1` - `prop75`](../vars/page-vars/prop.md) | [Prop](/help/components/dimensions/prop.md)또는 사용자 지정 트래픽 변수. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | 히트에서 사용되는 통화 유형. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | 도메인에 있는 점의 수. 쿠키를 올바로 저장하는 데 사용됩니다. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | 이미지 요청의 문자 인코딩. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) |  방문자 쿠키의 수명입니다. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Used in the [Site sections](/help/components/dimensions/site-section.md) dimension. |
| `cp` | 없음 | Used in the [Hit Type](/help/components/dimensions/hit-type.md) dimension. |
| `ct` | 없음 | Used in the [Connection Type](/help/components/dimensions/connection-type.md) dimension. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | 동적 변수에 사용할 사항을 나타냅니다. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | `events` 쿼리 문자열의 축약. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | 페이지에 있는 이벤트들을 쉼표로 구분한 목록. 대부분의 [지표에서 사용됩니다](/help/components/metrics/overview.md). |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | 페이지의 현재 URL(최대 255바이트) Used in the [Page URL](/help/components/dimensions/page-url.md) dimension. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | 255바이트보다 긴 URL은 분할됩니다. 처음 255바이트는 `g` 매개 변수에 나타나고 나머지 모든 바이트는 `-g` 매개 변수에 나타납니다. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | `pageName` 쿼리 문자열의 축약. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | `pageType` 쿼리 문자열의 축약. |
| `h1` - `h5` | [`hier1` - `hier5`](../vars/page-vars/hier.md) | 계층 차원입니다. |
| `hp` | 없음 | 더 이상 사용되지 않습니다. 이전 버전의 Adobe Analytics에서 현재 URL이 브라우저의 홈 페이지인지 확인했습니다. |
| `j` | 없음 | 브라우저에 설치된 JavaScript 버전. |
| `k` | 없음 | Used in the [Cookie support](/help/components/dimensions/cookie-support.md) dimension. |
| `l1` - `l3` | [`list1` - `list3`](../vars/page-vars/list.md) | 목록 변수. |
| `mid` | 없음 | Experience Cloud 방문자 ID. |
| `ndh` | 없음 | 이미지 요청이 AppMeasurement에서 발생했는지 여부를 나타내는 플래그. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | 쿠키가 설정된 위치를 확인하는 데 도움이 됩니다. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | 마지막 페이지에 대한 개체 식별자. Activity Map에 사용됩니다. |
| `ot` | 없음 | 마지막 페이지에 대한 개체 이름. 이전 버전의 Activity Map에서 사용됩니다. |
| `p` | 없음 | 더 이상 사용되지 않습니다. 브라우저에서 사용되는 플러그인 목록. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Used in the [Page](/help/components/dimensions/page.md) dimension. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Used in the [Pages not found](/help/components/dimensions/pages-not-found.md) dimension. |
| `pccr` | 없음 | 새 방문자에 대해서만 설정되고 항상 `true`로 설정됩니다. 무한 리디렉션 방지 |
| `pe` | [`linkType`](../vars/config-vars/linktype.md) | 사용자 지정 링크의 유형을 결정합니다. 사용자 [지정 링크](/help/components/dimensions/custom-link.md), 다운로드 링크 [및](/help/components/dimensions/download-link.md)종료 링크에 [필요합니다](/help/components/dimensions/exit-link.md). |
| `pev1` | 없음 | 사용자 지정 링크가 발생한 URL. |
| `pev2` | [`linkName`](../vars/config-vars/linkname.md) | 사용자 지정 링크의 친숙한 이름. |
| `pev3` | 없음 | 더 이상 사용되지 않습니다. 비디오 보고의 이전 버전에서 추적된 이정표. |
| `pf` | 없음 | 플랫폼 플래그. Adobe 전용. 변경하지 마십시오. |
| `pid` | 없음 | 마지막 페이지의 페이지 식별자. 이전 버전의 Activity Map에서 사용됩니다. |
| `pidt` | 없음 | 마지막 페이지의 페이지 식별자 유형. 이전 버전의 Activity Map에서 사용됩니다. |
| `pl` | [`products`](../vars/page-vars/products.md) | `products` 쿼리 문자열의 축약. |
| `products` | [`products`](../vars/page-vars/products.md) | Products 변수. 제품 [및](/help/components/dimensions/product.md) 카테고리 [차원에](/help/components/dimensions/category.md) 사용됩니다. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | 구매 중복 제거에 사용됩니다. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | 히트의 참조 URL. 레퍼러 및 참조 도메인과 같은 트래픽 소스 [차원에](/help/components/dimensions/referrer.md) [사용됨](/help/components/dimensions/referring-domain.md) |
| `s` | 없음 | `width x height`로 표시되는 화면 해상도. Used in the [Monitor resolutions](/help/components/dimensions/monitor-resolution.md) dimension. |
| `server` | [`server`](../vars/page-vars/server.md) | [서버 차원.](/help/components/dimensions/server.md) |
| `sv` | [`server`](../vars/page-vars/server.md) | `server` 쿼리 문자열의 축약. |
| `state` | [`state`](../vars/page-vars/state.md) | 상태 차원. |
| `t` | 없음 | 히트의 생성 날짜/시간. `dd/mm/yyyy hh:mm:ss w o` 형식을 사용합니다.<br>- `dd/mm/yyyy hh:mm:ss`는 JavaScript의 날짜/시간입니다. 달 `0`은 1월이고 달 `11`은 12월입니다.<br>- `w`는 요일입니다. `0`은 일요일이고 `6`은 토요일입니다.<br>- `o`는 음수 GMT 오프셋(분 단위)입니다. 예를 들어 `420`은 GMT-7입니다. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | 히트와 함께 설정된 사용자 지정 타임스탬프. 보통 오프라인 추적에 사용됩니다. |
| `v` | 없음 | Used in the [Java enabled](/help/components/dimensions/java-enabled.md) dimension. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [추적 코드 차원.](/help/components/dimensions/tracking-code.md) |
| `v1` - `v250` | [`evar1` - `eVar250`](../vars/page-vars/evar.md) | [eVar](/help/components/dimensions/evar.md)또는 사용자 지정 전환 차원입니다. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | 방문자 ID 변수. |
| `vmk` | `vmk` | 더 이상 사용되지 않습니다. 방문자 마이그레이션 키입니다. 이 키는 구현이 타사 쿠키에서 퍼스트 파티 쿠키로 마이그레이션되도록 도와줍니다. |
| `vvp` | `variableProvider` | Data Connectors에서 사용됩니다. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | 온라인 및 오프라인 데이터를 함께 연결하기 위해 데이터 소스와 함께 사용됩니다. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Used in the [Zip code](/help/components/dimensions/zip-code.md) dimension. |
