---
description: 데이터 소스 사용을 준비할 수 있는 절차
subtopic: Data sources
title: Data Sources 사용 준비
topic: Developer and implementation
uuid: 876ea069-574b-4e23-93b7-e3828bfd90f5
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Data Sources 사용 준비

데이터 소스 사용을 준비할 수 있는 절차

* [지표 식별 및 이름 지정](/help/import/c-data-sources/datasrc-preparing.md#section_0D1DA6D7768E4C4CB6E9A2F4639C0135)
* [데이터 차원 식별](/help/import/c-data-sources/datasrc-preparing.md#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A)
* [캠페인 추적 코드](/help/import/c-data-sources/datasrc-preparing.md#section_468222796FF449ABAA90D88EB3264CB1)
* [거래 ID](/help/import/c-data-sources/datasrc-preparing.md#section_D9513C1204B7496C9B738C5B12CCCFC7)
* [데이터 소스 데이터의 유효한 날짜 범위 식별](/help/import/c-data-sources/datasrc-preparing.md#section_03AAB1291BDC4403BDC50905A78FDB71)

## 지표 식별 및 이름 지정 {#section_0D1DA6D7768E4C4CB6E9A2F4639C0135}

*`Off-line Sales Revenue by Product`*, *`Returns by Product`* 또는 *`Ad Impressions by Campaign`*&#x200B;와 같이 데이터 소스에 포함된 지표나 측정을 이해하는 것이 중요합니다. 보고서 지표(이벤트, prop 및 eVar)와 연결할 수 있는 이름입니다.

Data Sources 데이터에 대한 적절한 지표-이벤트 매핑을 결정한 후 연결된 Data Sources 지표에 적합한 설명 이름으로 이벤트 이름을 변경하십시오.

관리 [도구](https://marketing.adobe.com/resources/help/ko_KR/reference/success_event.html) 도움말의 성공 이벤트를 참조하십시오.

>[!NOTE] 데이터 소스 데이터에서 새로운 빈 이벤트를 사용할 것이 좋지만, 드물게 기존 이벤트를 사용하는 것이 좋은 경우가 있습니다.

## 데이터 차원 식별 {#section_8EC6BDC4AA314D9EB85F6FCD8E6ABC0A}

Data Sources를 통해 가져온 지표를 분류하는 데 사용할 데이터(보고서)를 식별하고 수집합니다. 이 데이터를 *`data dimensions`*&#x200B;말합니다.

예를 들어 Data Sources 지표가 광고 노출 횟수를 측정하는 경우 데이터 차원은 캠페인 추적 코드일 가능성이 높습니다. 오프라인 판매를 측정하는 경우 제품 코드(또는 SKU)를 데이터 차원으로 사용할 수 있습니다.

지표에 여러 데이터 차원을 정의할 수 있지만, 각 지표는 각 연관된 데이터 차원에 대해 관련 값 또는 값 조합을 제공해야 합니다. 예를 들어 오프라인 판매 지표를 가져와서 *`Product`* 및 *`Partner`* 데이터 차원과 연결하는 경우 오프라인 판매 지표는 제품과 파트너의 각 조합에 대해 관련이 있어야 합니다(예: 총 매출).

>[!NOTE] 데이터 차원으로 분류할 수 없는 전체 지표 수를 가져올 수 있습니다.

데이터 소스에 사용할 데이터 차원을 정의한 후 변수에 매핑하여 차원 데이터를 마케팅 보고서에 통합합니다. 표준 보고서(예: 제품, 추적 코드, 검색 키워드) 또는 전환 트래픽 변수(eVar)를 사용합니다.

eVar를 사용할 때 기존 eVar 또는 새 eVar를 데이터 차원으로 사용할 수 있습니다. Data Sources에서 데이터 차원을 수신할 eVar를 선택한 후 이름을 적절하게 지정했는지 확인합니다.

Analytics [도움말의](https://marketing.adobe.com/resources/help/ko_KR/reference/success_event.html) 성공 이벤트를 참조하십시오.

## 캠페인 추적 코드 {#section_468222796FF449ABAA90D88EB3264CB1}

성공 이벤트를 가져오는 것 외에도, 연결된 eVar 값을 가져올 수도 있습니다. 예를 들어 캠페인 추적 코드를 사용하여 온라인 활동을 추적하고 오프라인 지표에 대한 캠페인 추적 코드를 가지고 있는 경우 캠페인 추적 코드와 함께 지표를 가져올 수 있습니다. 이 방법을 사용하면 캠페인 보고서에서 온라인 지표와 오프라인 지표를 모두 볼 수 있습니다.

연결된 eVar 값으로 Data Sources 지표를 가져오지 않으면 eVar로 분류된 데이터 소스 지표를 볼 수 없습니다. 대신, 전체 지표만 볼 수 있습니다.

## 거래 ID {#section_D9513C1204B7496C9B738C5B12CCCFC7}

거래 ID는 온라인 이벤트를 오프라인 이벤트에 연결하는 데 사용됩니다.

## 데이터 소스 데이터의 유효한 날짜 범위 식별 {#section_03AAB1291BDC4403BDC50905A78FDB71}

Data Sources 지표(사용자 지정 이벤트) 및 데이터 차원(eVar)을 정의한 후 가져올 데이터 소스 데이터의 날짜 범위를 검토하십시오. 기존 보고 데이터 범위를 벗어나는 데이터 소스는 가져올 수 없습니다.

예를 들어 온라인 데이터 추적을 구현하기 전에는 데이터 소스 데이터를 가져올 수 없습니다. Data Sources 데이터는 일별로 분류되어야 합니다.
