---
title: 데이터 수집 쿼리 매개변수
description: 이미지 요청에 사용된 모든 쿼리 문자열 매개변수를 나열합니다.
feature: Implementation Basics
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
role: Admin, Developer, Leader, User
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 100%

---

# 데이터 수집 쿼리 매개변수

다음 테이블에는 Adobe가 이미지 요청에 사용하는 모든 쿼리 문자열 매개변수가 나와 있습니다. 이 정보는 [패킷 분석기](packet-monitor.md)를 사용하여 디버깅하거나, [이미지 요청을 하드코딩](../other/hardcoded.md)하거나, [동적 변수](../vars/page-vars/dynamic-variables.md)를 사용할 때 사용할 수 있습니다.

| 매개변수 | Analytics 구현 변수 | 설명 |
| --- | --- | --- |
| `aamlh` | 없음 | Audience Manager 위치 힌트. Experience Cloud 공유 프로필 통합에 사용됩니다. |
| `aamb` | 없음 | Audience Manager Blob. Experience Cloud 공유 프로필 통합에 사용됩니다. |
| `aid` | 없음 | Analytics 방문자 ID. |
| `AQB` | 없음 | 이미지 요청 쿼리 문자열의 시작을 나타냅니다. |
| `AQE` | 없음 | 이미지 요청의 끝, 즉 요청이 잘리지 않았음을 나타냅니다. |
| `bh` | 없음 | 브라우저 높이 (픽셀 단위). [브라우저 높이](/help/components/dimensions/browser-height.md) 차원에 사용됩니다. |
| `bw` | 없음 | 브라우저 폭 (픽셀 단위). [브라우저 폭](/help/components/dimensions/browser-width.md) 차원에 사용됩니다. |
| `c` | 없음 | 색상 품질 (비트). [색상 심도](/help/components/dimensions/color-depth.md) 차원에 사용됩니다. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | 컨텍스트 데이터 변수의 시작을 나타냅니다. 값을 포함하지 않습니다. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | 컨텍스트 데이터 변수의 끝을 나타냅니다. 값을 포함하지 않습니다. |
| `c1` - `c75` | [`prop1` - `prop75`](../vars/page-vars/prop.md) | [Prop](/help/components/dimensions/prop.md) 또는 사용자 정의 트래픽 변수입니다. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | 히트에서 사용되는 통화 유형. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | 도메인에 있는 점의 수. 쿠키를 올바로 저장하는 데 사용됩니다. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | 이미지 요청의 문자 인코딩. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | 방문자 쿠키의 수명입니다. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | [사이트 섹션](/help/components/dimensions/site-section.md) 차원에 사용됩니다. |
| `cp` | 없음 | [히트 유형](/help/components/dimensions/hit-type.md) 차원에 사용됩니다. |
| `ct` | 없음 | [연결 유형](/help/components/dimensions/connection-type.md) 차원에 사용됩니다. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | 동적 변수에 사용할 사항을 나타냅니다. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | `events` 쿼리 문자열의 축약. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | 페이지에 있는 이벤트들을 쉼표로 구분한 목록. 대부분의 [지표](/help/components/metrics/overview.md)에서 사용됩니다. |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | 페이지의 현재 URL로서, 최대 255바이트입니다. [페이지 URL](/help/components/dimensions/page-url.md) 차원에 사용됩니다. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | 255바이트보다 긴 URL은 분할됩니다. 처음 255바이트는 `g` 매개변수에 나타나고 나머지 모든 바이트는 `-g` 매개변수에 나타납니다. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | `pageName` 쿼리 문자열의 축약. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | `pageType` 쿼리 문자열의 축약. |
| `h.` | [`collectHighEntropyUserAgentHints`](../vars/config-vars/collecthighentropyuseragenthints.md) | [클라이언트 힌트](/help/technotes/client-hints.md)를 나타내는 여러 변수의 접두사입니다. |
| `h1` - `h5` | [`hier1` - `hier5`](../vars/page-vars/hier.md) | 계층 차원입니다. |
| `hp` | 없음 | 더 이상 사용되지 않습니다. 이전 버전의 Adobe Analytics에서 현재 URL이 브라우저의 홈 페이지인지 확인했습니다. |
| `j` | 없음 | 브라우저에 설치된 JavaScript 버전. |
| `k` | 없음 | [쿠키 지원](/help/components/dimensions/cookie-support.md) 차원에 사용됩니다. |
| `l1` - `l3` | [`list1` - `list3`](../vars/page-vars/list.md) | 목록 변수. |
| `lrt` | 없음 | 마지막 요청의 왕복 시간인 &quot;마지막 요청 시간&quot;(밀리초)입니다. 한 페이지에서 둘 이상의 요청이 전송되거나 페이지가 단일 페이지 애플리케이션(SPA)일 때만 전송됩니다. |
| `mid` | 없음 | Experience Cloud 방문자 ID. |
| `ndh` | 없음 | 이미지 요청이 AppMeasurement에서 발생했는지 여부를 나타내는 플래그. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | 쿠키가 설정된 위치를 확인하는 데 도움이 됩니다. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | 마지막 페이지에 대한 오브젝트 식별자. Activity Map에 사용됩니다. |
| `ot` | 없음 | 마지막 페이지에 대한 오브젝트 이름. 이전 버전의 Activity Map에서 사용됩니다. |
| `p` | 없음 | 더 이상 사용되지 않습니다. 브라우저에서 사용되는 플러그인 목록. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | [페이지](/help/components/dimensions/page.md) 차원에 사용됩니다. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | [페이지를 찾을 수 없음](/help/components/dimensions/pages-not-found.md) 차원에 사용됩니다. |
| `pccr` | 없음 | 새 방문자에 대해서만 설정되고 항상 `true`로 설정됩니다. 방문자가 쿠키를 거부하는 경우 발생할 수 있는 무한 리디렉션을 방지할 수 있습니다. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | 사용자 정의 링크의 유형을 결정합니다. [사용자 정의 링크](/help/components/dimensions/custom-link.md), [다운로드 링크](/help/components/dimensions/download-link.md) 및 [종료 링크](/help/components/dimensions/exit-link.md)에 필요합니다. |
| `pev1` | [`linkURL`](../vars/config-vars/linkurl.md) | 사용자 정의 링크가 발생한 URL. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | 사용자 정의 링크의 친숙한 이름. |
| `pev3` | 없음 | 더 이상 사용되지 않습니다. 비디오 보고의 이전 버전에서 추적된 이정표. |
| `pf` | 없음 | 플랫폼 플래그. Adobe 전용. 변경하지 마십시오. |
| `pid` | 없음 | 마지막 페이지의 페이지 식별자. 이전 버전의 Activity Map에서 사용됩니다. |
| `pidt` | 없음 | 마지막 페이지의 페이지 식별자 유형. 이전 버전의 Activity Map에서 사용됩니다. |
| `pl` | [`products`](../vars/page-vars/products.md) | `products` 쿼리 문자열의 축약. |
| `products` | [`products`](../vars/page-vars/products.md) | Products 변수. [제품](/help/components/dimensions/product.md) 및 [범주](/help/components/dimensions/category.md) 차원에 사용됩니다. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | 구매 중복 제거에 사용됩니다. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | 히트의 참조 URL. [레퍼러](/help/components/dimensions/referrer.md) 및 [참조 도메인](/help/components/dimensions/referring-domain.md)과 같은 트래픽 소스 차원에 사용됩니다. |
| `s` | 없음 | `width x height`로 표시되는 화면 해상도. [모니터 해상도](/help/components/dimensions/monitor-resolution.md) 차원에 사용됩니다. |
| `server` | [`server`](../vars/page-vars/server.md) | [서버 차원.](/help/components/dimensions/server.md) |
| `sv` | [`server`](../vars/page-vars/server.md) | `server` 쿼리 문자열의 축약. |
| `state` | [`state`](../vars/page-vars/state.md) | 상태 차원. |
| `t` | 없음 | 히트의 생성 날짜/시간. `dd/mm/yyyy hh:mm:ss w o` 형식을 사용합니다.<br>- `dd/mm/yyyy hh:mm:ss`는 JavaScript의 날짜/시간입니다. 달 `0`은 1월이고 달 `11`은 12월입니다.<br>- `w`는 요일입니다. `0`은 일요일이고 `6`은 토요일입니다.<br>- `o`는 음수 GMT 오프셋 (분 단위)입니다. 예를 들어 `420`은 GMT-7입니다. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | 히트와 함께 설정된 사용자 정의 타임스탬프. 보통 오프라인 추적에 사용됩니다. |
| `v` | 없음 | [Java 활성화](/help/components/dimensions/java-enabled.md) 차원에 사용됩니다. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [추적 코드 차원.](/help/components/dimensions/tracking-code.md) |
| `v1` - `v250` | [`evar1` - `eVar250`](../vars/page-vars/evar.md) | [eVar](/help/components/dimensions/evar.md) 또는 사용자 정의 전환 차원입니다. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | 방문자 ID 변수입니다. |
| `vidn` | 없음 | 새 방문자에 대해 AppMeasurement에서 설정됩니다. 방문자 쿠키에 저장된 ID 값을 포함합니다. |
| `vmk` | `vmk` | 더 이상 사용되지 않습니다. 구현을 서드파티 쿠키에서 자사 쿠키로 마이그레이션하는 데 도움을 준 방문자 마이그레이션 키입니다. |
| `vvp` | `variableProvider` | Data Connectors에서 사용됩니다. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | 온라인 및 오프라인 데이터를 함께 연결하기 위해 Data Sources와 함께 사용됩니다. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | [우편 번호](/help/components/dimensions/zip-code.md) 차원에서 사용됩니다. |
