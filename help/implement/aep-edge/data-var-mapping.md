---
title: Adobe Analytics에 대한 데이터 개체 변수 매핑
description: Edge이 Analytics 변수에 자동으로 매핑하는 Experience Platform 데이터 개체 필드를 봅니다.
feature: Implementation Basics
role: Admin, Developer
exl-id: 45b2fbbc-73ca-40b3-9484-b406ae99fdad
source-git-commit: 59d9dd8055a13046d05ac4c3b5261a6c5a919b5c
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 2%

---

# Adobe Analytics에 대한 데이터 개체 변수 매핑

다음 표는 Adobe Experience Platform Edge Network이 Adobe Analytics에 자동으로 매핑하는 데이터 개체 변수를 보여 줍니다. 이러한 데이터 개체 필드 경로를 사용하는 경우 Adobe Analytics으로 데이터를 전송하기 위해 추가 구성이 필요하지 않습니다.

나중에 Customer Journey Analytics을 사용하려는 경우 이러한 필드를 사용하는 것이 좋습니다. 이 Adobe 방법을 사용하면 조직이 XDM 스키마를 준수하지 않고 웹 SDK를 사용하여 데이터를 구현으로 보낼 수 있습니다. 조직에서 Adobe Experience Platform으로 데이터를 보낼 준비가 되면 [데이터스트림 매핑](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/data-prep#mapping)을 사용하여 데이터 개체 필드를 해당 XDM 필드로 지정할 수 있습니다.

## 값 우선 순위

이 테이블의 데이터 개체 필드는 대부분 [매핑된 XDM 필드](xdm-var-mapping.md)와(과) 일치합니다. 지정된 데이터 개체 필드와 해당 XDM 필드를 모두 설정하면 데이터 개체 필드가 우선합니다. 예를 들어 필드 `data.__adobe.analytics.events`이(가) 있으면 모든 이벤트 관련 XDM 개체 필드를 덮어씁니다.

일부 데이터 개체 필드는 해당 [쿼리 매개 변수 값](../validate/query-parameters.md)도 축약 값으로 지원합니다. 표준 데이터 개체 필드와 축약 데이터 개체 필드는 각각 고유한 변수에 해당하는 한 서로 교환하여 사용할 수 있습니다. 표준 데이터 개체 필드와 각 축약 데이터 개체 필드를 동시에 설정하지 마십시오. Adobe은 우선 순위가 높은 필드를 보장할 수 없습니다.

## 데이터 개체 필드 매핑

이 테이블에 대한 이전 업데이트는 이 페이지의 [GitHub의 커밋 기록](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/data-var-mapping.md)에서 찾을 수 있습니다. AppMeasurement 변수와 마찬가지로 모든 데이터 개체 필드는 대/소문자를 구분합니다.

| 데이터 개체 필드 경로 | Analytics 변수 및 설명 |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | [브라우저 높이](../../components/dimensions/browser-height.md) 차원입니다. 축약 필드 `data.__adobe.analytics.bh`도 지원됩니다. |
| `data.__adobe.analytics.browserWidth` | [브라우저 너비](../../components/dimensions/browser-width.md) 차원입니다. 축약 필드 `data.__adobe.analytics.bw`도 지원됩니다. |
| `data.__adobe.analytics.campaign` | [추적 코드](../../components/dimensions/tracking-code.md) 차원입니다. 축약 필드 `data.__adobe.analytics.v0`도 지원됩니다. |
| `data.__adobe.analytics.channel` | [사이트 섹션](../../components/dimensions/site-section.md) 차원. 축약 필드 `data.__adobe.analytics.ch`도 지원됩니다. |
| `data.__adobe.analytics.colorDepth` | [색상 깊이](../../components/dimensions/color-depth.md) 차원입니다. 축약 필드 `data.__adobe.analytics.c`도 지원됩니다. |
| `data.__adobe.analytics.connectionType` | [연결 유형](../../components/dimensions/connection-type.md) 차원입니다. 축약 필드 `data.__adobe.analytics.ct`도 지원됩니다. |
| `data.__adobe.analytics.contextData` | [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | [쿠키 지원](../../components/dimensions/cookie-support.md) 차원. 축약 필드 `data.__adobe.analytics.k`도 지원됩니다. |
| `data.__adobe.analytics.currencyCode` | [`currencyCode`](../vars/config-vars/currencycode.md) 구현 변수입니다. 축약 필드 `data.__adobe.analytics.cc`도 지원됩니다. |
| `data.__adobe.analytics.dynamicVariablePrefix` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) 구현 변수입니다. |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [eVar](../../components/dimensions/evar.md) 차원. 축약 필드 `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250`도 지원됩니다. |
| `data.__adobe.analytics.events` | [사용자 지정 이벤트](../../components/metrics/custom-events.md). 이 필드의 형식은 [`events`](../vars/page-vars/events/events-overview.md) 구현 변수와 비슷합니다. |
| `data.__adobe.analytics.javaEnabled` | [Java 활성화](../../components/dimensions/java-enabled.md) 차원. 축약 필드 `data.__adobe.analytics.v`도 지원됩니다. |
| `data.__adobe.analytics.latitude` | [위치](../../components/dimensions/lifecycle-dimensions.md) 모바일 라이프사이클 차원을 설정하는 데 도움이 됩니다. 축약 필드 `data.__adobe.analytics.lat`도 지원됩니다. |
| `data.__adobe.analytics.linkName` | `data.__adobe.analytics.linkType`의 값에 따라 [사용자 지정 링크](../../components/dimensions/custom-link.md), [다운로드 링크](../../components/dimensions/download-link.md) 또는 [종료 링크](../../components/dimensions/exit-link.md) 차원입니다. 축약 필드 `data.__adobe.analytics.pev2`도 지원됩니다. |
| `data.__adobe.analytics.linkURL` | [`linkURL`](../vars/config-vars/linkurl.md) 구현 변수입니다. 축약 필드 `data.__adobe.analytics.pev1`도 지원됩니다. |
| `data.__adobe.analytics.linkType` | 클릭한 링크의 유형을 결정합니다. 유효한 값에는 `o`(사용자 지정 링크), `d`(다운로드 링크) 및 `e`(종료 링크)이(가) 포함됩니다. 축약 필드 `data.__adobe.analytics.pe`도 지원됩니다. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | 구현 변수 [`list`](/help/implement/vars/page-vars/list.md)개. 축약 필드 `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3`도 지원됩니다. |
| `data.__adobe.analytics.longitude` | [위치](../../components/dimensions/lifecycle-dimensions.md) 모바일 라이프사이클 차원을 설정하는 데 도움이 됩니다. 축약 필드 `data.__adobe.analytics.lon`도 지원됩니다. |
| `data.__adobe.analytics.pageName` | [페이지](/help/components/dimensions/page.md) 차원. |
| `data.__adobe.analytics.pageURL` | [페이지 URL](/help/components/dimensions/page-url.md) 차원. 축약 필드 `data.__adobe.analytics.g`도 지원됩니다. |
| `data.__adobe.analytics.pageType` | [`pageType`](../vars/page-vars/pagetype.md) 구현 변수입니다. |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [Prop](../../components/dimensions/prop.md) 차원. 축약 필드 `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75`도 지원됩니다. |
| `data.__adobe.analytics.purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) 구현 변수입니다. |
| `data.__adobe.analytics.products` | 유사한 형식을 따르는 [`products`](../vars/page-vars/products.md) 구현 변수입니다. |
| `data.__adobe.analytics.referrer` | [레퍼러](/help/components/dimensions/referrer.md) 차원. |
| `data.__adobe.analytics.resolution` | [모니터 해상도](../../components/dimensions/monitor-resolution.md) 차원입니다. 축약 필드 `data.__adobe.analytics.s`도 지원됩니다. |
| `data.__adobe.analytics.server` | [서버](/help/components/dimensions/server.md) 차원. |
| `data.__adobe.analytics.transactionID` | [`transactionID`](../vars/page-vars/transactionid.md) 구현 변수입니다. 축약 필드 `data.__adobe.analytics.xact`도 지원됩니다. |
| `data.__adobe.analytics.zip` | [우편 번호](../../components/dimensions/zip-code.md) 차원. |

{style="table-layout:auto"}
