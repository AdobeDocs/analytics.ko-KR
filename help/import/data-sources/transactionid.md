---
title: 거래 ID 데이터 소스
description: 온라인 히트의 저장된 값을 사용하여 거래 ID를 공유하는 오프라인 히트를 보강합니다.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 8%

---

# 거래 ID 데이터 소스

거래 ID 데이터 소스는 온라인 히트에서 저장된 값을 동일한 거래 ID를 공유하는 오프라인 행에 적용할 수 있는 요약 데이터 소스의 변형입니다. 이 방법은 온라인으로 트랜잭션을 캡처하지만 나중에 다른 시스템에서 세부 정보를 수신할 때 유용합니다. 주요 예로는 제품 반환, 예약 취소 또는 콜 센터 상호 작용의 결과가 있습니다.

>[!NOTE]
>
>거래 ID 데이터 소스를 사용하기 전에 먼저 원하는 보고서 세트에 대해 [일반 계정 설정](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)에서 활성화해야 합니다.

## 작동 방식

거래 ID의 개념에는 두 가지 부분이 필요합니다.

* **온라인 히트**: 보고서 세트(AppMeasurement, Web SDK, API 등)로 전송된 모든 전체 Analytics 히트. 이 히트에서 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 구현 변수를 설정했습니다.
* **오프라인 히트**: 데이터 원본을 통해 업로드된 행입니다. 파일 내에 온라인 히트와 일치하는 값이 있는 `transactionID` 열을 포함합니다.

`transactionID` 구현 변수가 포함된 온라인 히트를 보낼 때 Adobe은 해당 시점에 설정되었거나 지속된 다음 차원의 &quot;스냅숏&quot;을 만듭니다.

* [카테고리](/help/components/dimensions/category.md)
* [첫 구매까지 소요된 일 수](/help/components/dimensions/days-before-first-purchase.md)
* [마지막 구매 이후 일 수](/help/components/dimensions/days-since-last-purchase.md)
* [eVar 1-250](/help/components/dimensions/evar.md)
* eVar와 유사하게 동작하는 [보고서 세트 설정](/help/admin/tools/manage-rs/report-suites-admin.md)에서 사용할 수 있는 기능별 차원입니다. prop과 유사하게 동작하는 기능별 차원은 포함되지 않습니다.
* [목록 변수](/help/implement/vars/page-vars/list.md)
* [마케팅 채널](/help/components/dimensions/marketing-channel.md)
* [마케팅 채널 세부 사항](/help/components/dimensions/marketing-detail.md)
* [모바일 차원](/help/components/dimensions/mobile-dimensions.md)
* [최초 참조 도메인](/help/components/dimensions/original-referring-domain.md)
* [제품](/help/components/dimensions/product.md)
* [참조 도메인](/help/components/dimensions/referring-domain.md)
* [검색 엔진](/help/components/dimensions/search-engine.md)
* [검색 키워드](/help/components/dimensions/search-keyword.md)
* [추적 코드](/help/components/dimensions/tracking-code.md)
* [방문 횟수](/help/components/dimensions/visit-number.md)

>[!NOTE]
>
>지표(예: [주문](/help/components/metrics/orders.md) 또는 [사용자 지정 이벤트](/help/components/metrics/custom-events.md))는 &quot;스냅숏&quot;에 포함되지 않습니다.

일치하는 거래 ID가 포함된 데이터 소스를 통해 오프라인 히트를 업로드하면 &quot;스냅숏&quot; 내에서 사용 가능한 모든 차원이 데이터 소스 행에 자동으로 추가됩니다. 주어진 차원이 온라인 및 오프라인 히트 모두에 있는 경우 오프라인 히트 값이 사용됩니다.

>[!IMPORTANT]
>
>거래 ID 데이터 소스의 개념은 데이터 소스 행(오프라인 히트)만 채우는 데 도움이 됩니다. 온라인 히트에 영향을 주거나 변경되지 않습니다.

## 거래 ID 데이터 소스 고려 사항

거래 ID 데이터 소스에는 다음 속성이 있습니다.

* 온라인 데이터를 먼저 수집하고 처리해야 합니다. 보고서 세트가 해당 거래 ID와 일치하는 히트를 처리하기 전에 거래 ID 데이터 소스가 업로드되는 경우 데이터는 요약 데이터 소스처럼 처리됩니다.
* 온라인 히트에서 수집된 거래 ID는 25개월 후에 만료됩니다.
* 만료된 거래 ID로 업로드된 데이터 소스는 거래 ID 없이 업로드된 데이터와 유사하게 처리됩니다.
* 여러 온라인 히트에 대해 동일한 거래 ID를 설정하는 경우, 첫 번째 발생의 &quot;스냅샷&quot;만 사용됩니다. 후속 중복 거래 ID 온라인 히트는 거래 ID가 없는 것처럼 처리됩니다.
* 지정된 `transactionID` 값을 채우면 해당 트랜잭션 ID가 만료될 때까지 연결된 &quot;스냅숏&quot;을 변경할 수 없는 것으로 간주됩니다.
* 여러 데이터 소스 행에 동일한 거래 ID를 설정하면 온라인 히트에서 사용할 수 있는 모든 차원이 각 오프라인 히트에 추가됩니다. 동일한 거래 ID에 대한 오프라인 히트는 서로에 대해 아무것도 모르며, 오프라인 히트 간에 데이터가 전달되지 않습니다.
