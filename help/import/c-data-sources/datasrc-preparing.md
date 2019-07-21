---
description: 데이터 소스 사용을 준비할 수 있는 절차
seo-description: 데이터 소스 사용을 준비할 수 있는 절차
seo-title: 데이터 소스 사용 준비
solution: Analytics
subtopic: Data Sources
title: 데이터 소스 사용 준비
topic: 개발자 및 구현
uuid: 876 EA 069-574 B -4 E 23-93 B 7-E 3828 BFD 90 F 5
translation-type: tm+mt
source-git-commit: 887f48d2ea5f21b7db95a1a8f716f7da9cf43662

---


# 데이터 소스 사용 준비

데이터 소스 사용을 준비할 수 있는 절차

* [지표 식별 및 이름 지정](../../import/c-data-sources/datasrc-preparing.md#section_0D1DA6D7768E4C4CB6E9A2F4639C0135)
* [데이터 차원 식별](../../import/c-data-sources/datasrc-preparing.md#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A)
* [캠페인 추적 코드](../../import/c-data-sources/datasrc-preparing.md#section_468222796FF449ABAA90D88EB3264CB1)
* [거래 ID](../../import/c-data-sources/datasrc-preparing.md#section_D9513C1204B7496C9B738C5B12CCCFC7)
* [데이터 소스 데이터에 대한 유효한 날짜 범위 식별](../../import/c-data-sources/datasrc-preparing.md#section_03AAB1291BDC4403BDC50905A78FDB71)

## 지표 식별 및 이름 지정 {#section_0D1DA6D7768E4C4CB6E9A2F4639C0135}

It is important to understand the metrics or measurements that are contained in your data sources, such as *`Off-line Sales Revenue by Product`*, *`Returns by Product`*, or *`Ad Impressions by Campaign`*. 이러한 이름을 보고서 지표(이벤트, prop 및 eVar)와 연결할 수 있습니다.

데이터 소스 데이터에 대한 적절한 지표-이벤트 매핑을 결정했으면 해당 연결 데이터 소스 지표에 적절한 설명 이름으로 이벤트 이름을 변경하십시오.

관리 도구 도움말의 [성공 이벤트](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=success_event)를 참조하십시오.

>[!NOTE]
>
>Data Sources 데이터에 새로운 빈 이벤트를 사용하는 것이 좋지만, 드물게 기존 이벤트를 사용하는 것이 적절할 수 있습니다.

## 데이터 차원 식별 {#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A}

데이터 소스를 통해 가져온 지표를 분류하는 데 사용할 데이터(보고서)를 식별하고 수집합니다. 이러한 데이터를 *`data dimensions`*.

예를 들어 데이터 소스 지표가 광고 노출 횟수를 측정하는 경우 데이터 차원은 캠페인 추적 코드일 가능성이 높습니다. 오프라인 매출을 측정하는 경우 제품 코드(또는 SKU)를 데이터 차원으로 사용할 수 있습니다.

여러 데이터 차원을 지표에 정의할 수 있지만, 각 지표는 연결된 데이터 차원 각각에 대해 관련된 값 또는 값 조합을 제공해야 합니다. 예를 들어 오프라인 판매 지표를 가져와서 *`Product`* 데이터 *`Partner`* 차원, 오프라인 판매 지표는 제품 및 파트너의 각 조합에 대해 관련이 있어야 합니다 (예: 총 매출).

>[!NOTE]
>
>데이터 차원으로 분류할 수 없는 전체 지표를 가져올 수 있습니다.

데이터 소스에 사용할 데이터 차원을 정의한 후에는 차원 데이터를 변수에 매핑하여 마케팅 보고서에 통합하십시오. 표준 보고서(예: 제품, 추적 코드, 검색 키워드)나 전환 트래픽 변수(eVar)를 사용합니다.

eVar 사용 시 기존의 eVar 또는 새로운 eVar를 데이터 차원으로 사용할 수 있습니다. 데이터 소스에서 데이터 차원을 수신할 eVar를 선택한 후에는 적절하게 이름을 지정하십시오. 

Analytics 도움말의 [성공 이벤트](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=success_event)를 참조하십시오.

## 캠페인 추적 코드 {#section_468222796FF449ABAA90D88EB3264CB1}

성공 이벤트를 가져오는 것 외에, 연결된 eVar 값을 가져올 수도 있습니다. 예를 들어 캠페인 추적 코드를 통해 온라인 활동을 추적하고 오프라인 지표에 대해 캠페인 추적 코드를 갖는 경우 이러한 지표와 캠페인 추적 코드를 가져올 수 있습니다. 이 접근 방식에서는 캠페인 보고서에서 온라인 지표와 오프라인 지표를 모두 볼 수 있습니다.

연결된 eVar 값으로 데이터 소스 지표를 가져오지 않으면, eVar별로 분류된 데이터 소스를 볼 수 없습니다. 오히려, 전체 지표만 볼 수 있습니다.

## 거래 ID {#section_D9513C1204B7496C9B738C5B12CCCFC7}

거래 ID는 온라인 이벤트를 오프라인 이벤트에 연결하는 데 사용됩니다.

## 데이터 소스 데이터에 대한 유효한 날짜 범위 식별 {#section_03AAB1291BDC4403BDC50905A78FDB71}

데이터 소스 지표(사용자 정의 이벤트)와 데이터 차원(eVar)을 정의한 후에는 가져오려는 데이터 소스 데이터의 날짜 범위를 검토하십시오. 기존 보고 데이터 날짜 범위 밖의 데이터 소스는 가져올 수 없습니다.

예를 들어 온라인 데이터 추적을 구현하기 전의 데이터 소스 데이터는 가져올 수 없습니다. 데이터 소스 데이터는 하루 단위로 분류됩니다. 
