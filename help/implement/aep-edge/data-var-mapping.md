---
title: Adobe Analytics에 대한 데이터 개체 변수 매핑
description: Experience Platform Edge가 Analytics 변수에 자동으로 매핑하는 데이터 개체 필드를 봅니다.
feature: Implementation Basics
role: Admin, Developer
exl-id: 45b2fbbc-73ca-40b3-9484-b406ae99fdad
source-git-commit: 3a530e3e47ac9d6cf2b711cecd07f2c33765d63c
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 5%

---

# Adobe Analytics에 대한 데이터 개체 변수 매핑

다음 표는 Adobe Experience Platform Edge Network가 Adobe Analytics에 자동으로 매핑하는 데이터 개체 변수를 보여 줍니다. 이러한 데이터 개체 필드 경로를 사용하는 경우 Adobe Analytics으로 데이터를 전송하기 위해 추가 구성이 필요하지 않습니다.

나중에 Customer Journey Analytics을 사용하려는 경우 이러한 필드를 사용하는 것이 좋습니다. 이 Adobe 방법을 사용하면 조직이 XDM 스키마를 준수하지 않고 웹 SDK를 사용하여 데이터를 구현으로 보낼 수 있습니다. 조직에서 Adobe Experience Platform으로 데이터를 전송할 준비가 되면 다음을 사용할 수 있습니다. [데이터 스트림 매핑](https://experienceleague.adobe.com/docs/experience-platform/datastreams/data-prep.html#mapping) 데이터 개체 필드를 해당 XDM 필드에 지정합니다.

## 값 우선 순위

이 테이블의 데이터 개체 필드는 대부분 [매핑된 XDM 필드](xdm-var-mapping.md). 두 가지를 모두 설정하시면 `data` 오브젝트 필드 및 해당 XDM 필드, 데이터 오브젝트 필드가 우선합니다. XDM 개체 필드와 데이터 개체 필드를 모두 사용하는 경우 데이터 개체 필드를 사용하여 Adobe 정의 이벤트를 설정하는 것이 좋습니다. 필드인 경우 `data.__adobe.analytics.events` 가 있으면 상거래 및 사용자 지정 이벤트와 관련된 모든 XDM 개체 필드를 덮어씁니다.

일부 데이터 개체 필드는 해당 필드도 지원합니다 [쿼리 매개 변수 값](../validate/query-parameters.md) 축약적인 값으로 사용됩니다. 표준 데이터 개체 필드와 축약 데이터 개체 필드는 각각 고유한 변수에 해당하는 한 서로 교환하여 사용할 수 있습니다. 표준 데이터 개체 필드와 각 축약 데이터 개체 필드를 동시에 설정하지 마십시오. Adobe은 우선 순위가 높은 필드를 보장할 수 없습니다.

## 데이터 개체 필드 매핑

이 테이블에 대한 이전 업데이트는 이 페이지의 [GitHub의 커밋 기록](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/data-var-mapping.md)에서 확인할 수 있습니다.

| 데이터 개체 필드 경로 | Analytics 변수 및 설명 |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | 다음 [브라우저 높이](../../components/dimensions/browser-height.md) 차원. 속기 분야 `data.__adobe.analytics.bh` 도 지원됩니다. |
| `data.__adobe.analytics.browserWidth` | 다음 [브라우저 너비](../../components/dimensions/browser-width.md) 차원. 속기 분야 `data.__adobe.analytics.bw` 도 지원됩니다. |
| `data.__adobe.analytics.campaign` | 다음 [추적 코드](../../components/dimensions/tracking-code.md) 차원. 속기 분야 `data.__adobe.analytics.v0` 도 지원됩니다. |
| `data.__adobe.analytics.channel` | 다음 [사이트 섹션](../../components/dimensions/site-section.md) 차원. 속기 분야 `data.__adobe.analytics.ch` 도 지원됩니다. |
| `data.__adobe.analytics.colorDepth` | 다음 [색상 깊이](../../components/dimensions/color-depth.md) 차원. 속기 분야 `data.__adobe.analytics.c` 도 지원됩니다. |
| `data.__adobe.analytics.connectionType` | 다음 [연결 유형](../../components/dimensions/connection-type.md) 차원. 속기 분야 `data.__adobe.analytics.ct` 도 지원됩니다. |
| `data.__adobe.analytics.contextData` | [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | 다음 [쿠키 지원](../../components/dimensions/cookie-support.md) 차원. 속기 분야 `data.__adobe.analytics.k` 도 지원됩니다. |
| `data.__adobe.analytics.currencyCode` | 다음 [`currencyCode`](../vars/config-vars/currencycode.md) 구현 변수입니다. 속기 분야 `data.__adobe.analytics.cc` 도 지원됩니다. |
| `data.__adobe.analytics.dynamicVariablePrefix` | 다음 [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) 구현 변수입니다. |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [eVar](../../components/dimensions/evar.md) 차원. 속기 필드 `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` 도 지원됩니다. |
| `data.__adobe.analytics.events` | [사용자 지정 이벤트](../../components/metrics/custom-events.md). 이 필드의 형식을 다음과 유사하게 지정합니다. [`events`](../vars/page-vars/events/events-overview.md) 구현 변수입니다. |
| `data.__adobe.analytics.javaEnabled` | 다음 [Java 활성화](../../components/dimensions/java-enabled.md) 차원. 속기 분야 `data.__adobe.analytics.v` 도 지원됩니다. |
| `data.__adobe.analytics.latitude` | 를 설정하는 데 도움이 됩니다. [위치](../../components/dimensions/lifecycle-dimensions.md) 모바일 라이프사이클 차원. 속기 분야 `data.__adobe.analytics.lat` 도 지원됩니다. |
| `data.__adobe.analytics.linkName` | 다음 [사용자 지정 링크](../../components/dimensions/custom-link.md), [다운로드 링크](../../components/dimensions/download-link.md), 또는 [종료 링크](../../components/dimensions/exit-link.md) 차원, 의 값에 따라 다름 `data.__adobe.analytics.linkType`. 속기 분야 `data.__adobe.analytics.pev2` 도 지원됩니다. |
| `data.__adobe.analytics.linkURL` | 다음 [`linkURL`](../vars/config-vars/linkurl.md) 구현 변수입니다. 속기 분야 `data.__adobe.analytics.pev1` 도 지원됩니다. |
| `data.__adobe.analytics.linkType` | 클릭한 링크의 유형을 결정합니다. 유효한 값은 다음과 같습니다 `o` (사용자 지정 링크), `d` (다운로드 링크) 및 `e` (종료 링크). 속기 분야 `data.__adobe.analytics.pe` 도 지원됩니다. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | [`list`](/help/implement/vars/page-vars/list.md) 구현 변수. 속기 필드 `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` 도 지원됩니다. |
| `data.__adobe.analytics.longitude` | 도움말 설정 [위치](../../components/dimensions/lifecycle-dimensions.md) 모바일 라이프사이클 차원. 속기 분야 `data.__adobe.analytics.lon` 도 지원됩니다. |
| `data.__adobe.analytics.pageName` | [페이지](/help/components/dimensions/page.md) 차원. |
| `data.__adobe.analytics.pageURL` | 다음 [페이지 URL](/help/components/dimensions/page-url.md) 차원. 속기 분야 `data.__adobe.analytics.g` 도 지원됩니다. |
| `data.__adobe.analytics.pageType` | 다음 [`pageType`](../vars/page-vars/pagetype.md) 구현 변수입니다. |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [Prop](../../components/dimensions/prop.md) 차원. 속기 필드 `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` 도 지원됩니다. |
| `data.__adobe.analytics.purchaseID` | 다음 [`purchaseID`](../vars/page-vars/purchaseid.md) 구현 변수입니다. |
| `data.__adobe.analytics.products` | 다음 [`products`](../vars/page-vars/products.md) 구현 변수를 참조하십시오. |
| `data.__adobe.analytics.referrer` | [레퍼러](/help/components/dimensions/referrer.md) 차원. |
| `data.__adobe.analytics.resolution` | 다음 [모니터 해상도](../../components/dimensions/monitor-resolution.md) 차원. 속기 분야 `data.__adobe.analytics.s` 도 지원됩니다. |
| `data.__adobe.analytics.server` | [서버](/help/components/dimensions/server.md) 차원. |
| `data.__adobe.analytics.tnta` | A4T 통합에 사용됩니다. |
| `data.__adobe.analytics.transactionID` | 다음 [`transactionID`](../vars/page-vars/transactionid.md) 구현 변수입니다. 속기 분야 `data.__adobe.analytics.xact` 도 지원됩니다. |
| `data.__adobe.analytics.zip` | 다음 [우편 번호](../../components/dimensions/zip-code.md) 차원. |

{style="table-layout:auto"}
