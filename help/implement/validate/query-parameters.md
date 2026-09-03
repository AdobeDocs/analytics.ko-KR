---
title: 데이터 수집 쿼리 매개변수
description: 이미지 요청에 사용된 모든 쿼리 문자열 매개변수를 나열합니다.
feature: Implementation Basics
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
role: Admin, Developer, Leader, User
TQID: https://experienceleague.adobe.com/aB92GXPxYSkjcDD9wi0vj47jijqndMbOGaECvXs38-Y
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 1111
ht-degree: 46%

---

# 데이터 수집 쿼리 매개변수

다음 테이블에는 Adobe가 이미지 요청에 사용하는 모든 쿼리 문자열 매개변수가 나와 있습니다. 이 정보는 [패킷 분석기](packet-monitor.md)를 사용하여 디버깅하거나, [이미지 요청을 하드코딩](../other/hardcoded.md)하거나, [동적 변수](../vars/page-vars/dynamic-variables.md)를 사용할 때 유용합니다.

| 매개변수 | Analytics 구현 변수 | 설명 |
| --- | --- | --- |
| `aamlh` | 없음 | Audience Manager 위치 힌트입니다. 방문자 ID 서비스를 통해 Audience Manager ID 동기화에 사용되는 지역 데이터 센터를 식별합니다. |
| `aamb` | 없음 | Audience Manager blob. ID 동기화 중에 방문자 ID 서비스를 통해 전달된 인코딩된 Audience Manager 프로필 데이터입니다. |
| `aid` | 없음 | `s_vi` 쿠키에 저장된 이전 Analytics 방문자 ID입니다. 최신 구현에서 `mid` 매개 변수로 대체되었습니다. |
| `AQB` | 없음 | 이미지 요청 쿼리 문자열의 시작을 나타냅니다. |
| `AQE` | 없음 | 이미지 요청의 끝, 즉 요청이 잘리지 않았음을 나타냅니다. |
| `bh` | 없음 | 브라우저 높이 (픽셀 단위). [[!UICONTROL 브라우저 높이]](/help/components/dimensions/browser-height.md) 차원에 사용됩니다. |
| `bw` | 없음 | 브라우저 폭 (픽셀 단위). [[!UICONTROL 브라우저 폭]](/help/components/dimensions/browser-width.md) 차원에 사용됩니다. |
| `c` | 없음 | 색상 품질 (비트). [[!UICONTROL 색상 심도]](/help/components/dimensions/color-depth.md) 차원에 사용됩니다. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | 컨텍스트 데이터 변수의 시작을 나타냅니다. 값을 포함하지 않습니다. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | 컨텍스트 데이터 변수의 끝을 나타냅니다. 값을 포함하지 않습니다. |
| `c1` - `c75` | [`prop1` - `prop75`](../vars/page-vars/prop.md) | [Prop](/help/components/dimensions/prop.md) 또는 사용자 정의 트래픽 변수입니다. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | 히트에서 사용되는 통화 유형. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **더 이상 사용되지 않습니다.** 도메인에 있는 점의 수. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | 이미지 요청의 문자 인코딩. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | 방문자 쿠키의 수명입니다. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | [[!UICONTROL 사이트 섹션]](/help/components/dimensions/site-section.md) 차원에 사용됩니다. |
| `cp` | [`customerPerspective`](../vars/page-vars/customerperspective.md) | 앱이 전경에 있는 동안 모바일 앱 히트가 발생했는지 배경에 있는 동안 발생했는지 여부를 지정합니다. [[!UICONTROL 히트 유형]](/help/components/dimensions/hit-type.md) 차원에 사용됩니다. |
| `ct` | 없음 | [[!UICONTROL 연결 유형]](/help/components/dimensions/connection-type.md) 차원에 사용됩니다. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | 동적 변수에 사용할 사항을 나타냅니다. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | `events` 매개 변수의 축약. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | 페이지에 있는 이벤트들을 쉼표로 구분한 목록. 대부분의 [지표](/help/components/metrics/overview.md)에서 사용됩니다. |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | 페이지의 현재 URL로서, 최대 255바이트입니다. [[!UICONTROL 페이지 URL]](/help/components/dimensions/page-url.md) 차원에 사용됩니다. |
| `-g` | [`pageURL`](../vars/page-vars/pageurl.md) | 255바이트보다 긴 URL은 분할됩니다. 처음 255바이트는 `g` 매개변수에 나타나고 나머지 모든 바이트는 `-g` 매개변수에 나타납니다. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | `pageName` 매개 변수의 축약. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | `pageType` 매개 변수의 축약. |
| `h.` | [`collectHighEntropyUserAgentHints`](../vars/config-vars/collecthighentropyuseragenthints.md) | [클라이언트 힌트](/help/technotes/client-hints.md)를 나타내는 여러 변수의 접두사입니다. |
| `h1` - `h5` | [`hier1` - `hier5`](../vars/page-vars/page-variables.md#retired-page-variables) | **더 이상 사용되지 않습니다.** 계층 차원입니다. |
| `hp` | 없음 | **더 이상 사용되지 않습니다.** 이전 버전의 Adobe Analytics에서 현재 URL이 브라우저의 홈 페이지인지 확인했습니다. |
| `j` | 없음 | **더 이상 사용되지 않습니다.** 브라우저에 설치된 JavaScript 버전. |
| `k` | 없음 | [[!UICONTROL 쿠키 지원]](/help/components/dimensions/cookie-support.md) 차원에 사용됩니다. |
| `l1` - `l3` | [`list1` - `list3`](../vars/page-vars/list.md) | 목록 변수. |
| `lat` | 없음 | **더 이상 사용되지 않습니다.** 위도. 기존 모바일 SDK 구현으로 설정되며, 현재 모바일 구현은 데이터스트림을 통해 지리적 위치를 전송합니다. |
| `lon` | 없음 | **더 이상 사용되지 않습니다.** 경도. 기존 모바일 SDK 구현으로 설정되며, 현재 모바일 구현은 데이터스트림을 통해 지리적 위치를 전송합니다. |
| `lrt` | 없음 | 마지막 요청의 왕복 시간인 &quot;마지막 요청 시간&quot;(밀리초)입니다. 단일 페이지 애플리케이션(SPA)에서와 같이 단일 페이지에서 두 개 이상의 요청이 전송되는 경우에만 전송됩니다. |
| `mcorgid` | 없음 | 방문자 ID 서비스에 조직을 식별하는 IMS 조직 ID입니다. |
| `mid` | 없음 | [[!UICONTROL Experience Cloud 방문자 ID]](/help/components/dimensions/experience-cloud-visitor-id.md) 차원에 사용됩니다. |
| `ms_a` | 없음 | 추적된 스트리밍 미디어가 비디오가 아닌 오디오인 경우 Media SDK에서 `1`(으)로 설정합니다. |
| `ndh` | 없음 | AppMeasurement에서 생성하는 모든 이미지 요청에 추가됩니다. 하드코딩된 요청에서는 일반적으로 이 히트가 생략되므로 이 히트가 AppMeasurement에서 왔음을 나타냅니다. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **더 이상 사용되지 않습니다.** 쿠키가 설정된 위치를 확인하는 데 도움이 됩니다. |
| `oi` | 없음 | **더 이상 사용되지 않습니다.** 마지막 페이지에 대한 개체 인스턴스. 이전 버전의 Activity Map에서 사용됩니다. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | 마지막 페이지에 대한 오브젝트 식별자. 현재 버전의 Activity Map에서 사용됩니다. |
| `oidt` | 없음 | **더 이상 사용되지 않습니다.** 마지막 페이지에 대한 개체 식별자 유형입니다. 이전 버전의 Activity Map에서 사용됩니다. |
| `ot` | 없음 | **더 이상 사용되지 않습니다.** 마지막 페이지에 대한 오브젝트 이름. 이전 버전의 Activity Map에서 사용됩니다. |
| `p` | 없음 | **더 이상 사용되지 않습니다.** 브라우저에서 사용되는 플러그인 목록. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | [[!UICONTROL 페이지]](/help/components/dimensions/page.md) 차원에 사용됩니다. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | [[!UICONTROL 페이지를 찾을 수 없음]](/help/components/dimensions/pages-not-found.md) 차원에 사용됩니다. |
| `pccr` | 없음 | 영구적 쿠키 검사 리디렉션 플래그. 새 방문자에 대해 Adobe 데이터 수집 서버에서 설정되며 항상 `true`(으)로 설정됩니다. 새 방문자의 쿠키 지원을 알 수 없는 경우 데이터 수집 서버는 이 플래그를 사용하여 이미지 요청을 자신에게 리디렉션하여 영구적 쿠키 확인이 이미 발생했음을 확인합니다. 이 매개 변수는 방문자가 쿠키를 거부하는 경우 무한 리디렉션을 방지합니다. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | 히트 유형을 결정합니다. 유효한 값에는 `lnk_o`([[!UICONTROL 사용자 지정 링크]](/help/components/dimensions/custom-link.md)), `lnk_d`([[!UICONTROL 다운로드 링크]](/help/components/dimensions/download-link.md)), `lnk_e`([[!UICONTROL 종료 링크]](/help/components/dimensions/exit-link.md)) 및 `tnt`(Analytics for Target 히트)이 포함됩니다. |
| `pev1` | [`linkURL`](../vars/config-vars/linkurl.md) | 사용자 지정 링크가 발생한 URL입니다. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | [사용자 지정 링크](/help/components/dimensions/custom-link.md)의 알기 쉬운 이름. |
| `pev3` | 없음 | **더 이상 사용되지 않습니다.** 비디오 보고의 이전 버전에서 추적된 이정표. |
| `pf` | 없음 | 플랫폼 플래그. Adobe 전용. 변경하지 마십시오. |
| `pid` | 없음 | **더 이상 사용되지 않습니다.** 마지막 페이지의 페이지 식별자. 이전 버전의 Activity Map에서 사용됩니다. |
| `pidt` | 없음 | **더 이상 사용되지 않습니다.** 마지막 페이지의 페이지 식별자 유형. 이전 버전의 Activity Map에서 사용됩니다. |
| `pl` | [`products`](../vars/page-vars/products.md) | `products` 매개 변수의 축약. |
| `products` | [`products`](../vars/page-vars/products.md) | Products 변수. [[!UICONTROL 제품]](/help/components/dimensions/product.md) 및 [[!UICONTROL 카테고리]](/help/components/dimensions/category.md) 차원에 사용됩니다. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | [[!UICONTROL 구매 ID]](/help/components/dimensions/purchase-id.md) 차원에 사용됩니다. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | 히트의 참조 URL. [[!UICONTROL 레퍼러]](/help/components/dimensions/referrer.md) 및 [[!UICONTROL 참조 도메인]](/help/components/dimensions/referring-domain.md)과 같은 트래픽 소스 차원에 사용됩니다. |
| `s` | 없음 | `width x height`로 표시되는 화면 해상도. [[!UICONTROL 모니터 해상도]](/help/components/dimensions/monitor-resolution.md) 차원에 사용됩니다. |
| `sdid` | 없음 | 보조 데이터 ID. [Analytics for Target](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t.html) 통합에서 Analytics 및 Target 히트와 같이 동일한 이벤트를 설명하는 여러 히트를 연결합니다. |
| `server` | [`server`](../vars/page-vars/server.md) | [[!UICONTROL 서버]](/help/components/dimensions/server.md) 차원에 사용됩니다. |
| `sv` | [`server`](../vars/page-vars/server.md) | `server` 매개 변수의 축약. |
| `state` | [`state`](../vars/page-vars/page-variables.md#retired-page-variables) | **더 이상 사용되지 않습니다.** 일반적으로 배송 또는 청구 양식을 통해 방문자가 입력한 미국 주를 캡처했습니다. |
| `t` | 없음 | 히트의 생성 날짜/시간. JavaScript에서 날짜/시간 형식 `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss`을(를) 사용합니다. `0`월은 1월이고 `11`월은 12월입니다.<br>- `w`월은 요일입니다. `0`은(는) 일요일이지만 `6`은(는) 토요일입니다.<br>- `o`은(는) 음수 GMT 오프셋(분 단위)입니다. 예를 들어 `420`은 GMT-7입니다. |
| `tnt` | 없음 | [Analytics for Target](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t.html) 통합에 사용되는 Target 데이터 페이로드입니다. `pe=tnt`에 전송됩니다. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | 히트와 함께 설정된 사용자 정의 타임스탬프. 보통 오프라인 추적에 사용됩니다. |
| `u` | 없음 | **더 이상 사용되지 않습니다.** 이전 버전의 Activity Map에서 사용된 계정 마커입니다. |
| `v` | 없음 | [[!UICONTROL Java 활성화]](/help/components/dimensions/java-enabled.md) 차원에 사용됩니다. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [[!UICONTROL 추적 코드]](/help/components/dimensions/tracking-code.md) 차원에 사용됩니다. |
| `v1` - `v250` | [`evar1` - `eVar250`](../vars/page-vars/evar.md) | [eVar](/help/components/dimensions/evar.md) 또는 사용자 정의 전환 차원입니다. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | 방문자 ID 재정의 변수입니다. |
| `vidn` | 없음 | 리디렉션된 이미지 요청에 `pccr` 매개 변수와 함께 새 방문자에 대해 Adobe 데이터 수집 서버에서 설정합니다. 방문자 쿠키에 저장된 방문자 ID 값을 포함합니다. |
| `vmf` | [`visitorMigrationServer`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **더 이상 사용되지 않습니다.** 서드파티 쿠키에서 자사 쿠키로 마이그레이션하는 동안 사용되는 방문자 마이그레이션 서버입니다. |
| `vmt` | [`visitorMigrationKey`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **더 이상 사용되지 않습니다.** 구현을 타사 쿠키에서 자사 쿠키로 마이그레이션하는 데 도움이 된 방문자 마이그레이션 키입니다. |
| `vvp` | 없음 | **더 이상 사용되지 않습니다.** Data Connectors에서 사용되는 변수 공급자입니다. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | 온라인 및 오프라인 데이터를 함께 연결하기 위해 Data Sources와 함께 사용됩니다. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | [우편 번호](/help/components/dimensions/zip-code.md) 차원에서 사용됩니다. |
