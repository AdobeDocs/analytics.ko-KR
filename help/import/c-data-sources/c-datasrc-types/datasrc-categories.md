---
description: 데이터 소스 카테고리는 유사한 기능을 제공하는 다양한 데이터 소스 유형을 식별합니다.
subtopic: Data sources
title: 데이터 유형 및 카테고리 개요
topic-fix: Developer and implementation
feature: Data Sources
exl-id: d459fd06-a0fe-49e6-8624-b42f0c60ee6e
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 100%

---

# 데이터 유형 및 카테고리 개요

데이터 소스 카테고리는 유사한 기능을 제공하는 다양한 데이터 소스 유형을 식별합니다.

카테고리를 사용하면 사용자의 관점에서 데이터 소스를 그룹화할 수 있습니다. [!DNL Data Sources] UI를 통해 데이터 소스를 생성할 때 먼저 데이터 소스 카테고리를 선택한 다음 특정 데이터 소스 유형을 선택합니다. 각 카테고리는 유사한 데이터 유형을 지원하는 데이터 소스 유형을 포함합니다. [!DNL Data Sources]는 다음과 같은 데이터 소스 카테고리를 제공합니다.

## 웹 사이트 사용 {#web-usage}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 웹 서버 로그 파일] | [웹 로그](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md) | 대부분의 웹 서버는 모든 서비스 제공 페이지를 기록하는 로그 파일을 생성합니다. 이 데이터 소스를 사용하면 대부분의 웹 서버 데이터의 로그 파일을 처리하고 이 데이터를 보고서에 추가할 수 있습니다. |
| [!UICONTROL Advertising Cloud 일괄 업로드] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | [!DNL Advertising Cloud]에서 수동 및 Excel 자동 일괄 업로드가 제공됩니다. |
| [!UICONTROL 사이트 수준 트래픽 데이터 소스] | [트래픽](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) | 전체 웹 사이트에 대한 트래픽 데이터를 가져옵니다. 예: [!UICONTROL 페이지 뷰] |
| [!UICONTROL 트래픽 데이터 소스 분류] | [트래픽](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) | 다른 웹 사이트 변수로 분류된 트래픽 데이터를 가져옵니다. 예: [!UICONTROL 제품]별로 분류된 [!UICONTROL 페이지 뷰] |

## 광고 캠페인 {#ad-campaigns}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 범용 광고 서버] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 광고 서버의 광고 서비스 활동에 대한 노출 횟수 및 기타 최상위 지표를 마케팅 보고서에 통합할 수 있습니다. 이는 범용 광고 서버 데이터 소스이며 특정 광고 서버가 지원되지 않는 경우에 사용해야 합니다. |
| [!UICONTROL 범용 이메일 캠페인 서버] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 이메일 캠페인 서버의 지표를 마케팅 보고서에 통합할 수 있습니다. 일반적으로 통합되는 지표로는 전송한 메시지 수, 배달된 메시지 수 및 읽은 메시지 수 등이 있습니다. 이는 범용 이메일 캠페인 데이터 소스이며 특정 이메일 캠페인 서버가 지원되지 않는 경우에 사용해야 합니다. |
| [!UICONTROL 범용 클릭당 과금 서비스] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 노출 수, 클릭 수, 비용을 포함한 클릭당 과금 실적 데이터를 가져올 수 있습니다. 이는 범용 클릭당 과금 데이터 소스이며 특정 클릭당 과금 서비스가 지원되지 않는 경우에 사용해야 합니다. |

## 고객 관계 관리(CRM) {#crm}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 범용 콜 센터] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 콜 센터 관련 정보를 마케팅 보고서에 통합할 수 있습니다. 일반적으로 가져오는 지표로는 통화 수, 통화 시간, 상담원, 총 매출액 등이 있습니다. 이는 범용 콜 센터 데이터 소스이며 특정 콜 센터 소프트웨어가 지원되지 않는 경우에 사용해야 합니다. |
| [!UICONTROL 범용 고객 지원 애플리케이션] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 고객 지원 소프트웨어의 정보를 마케팅 보고서에 통합할 수 있습니다. 여기에는 새 지원 건 수, 해결된 지원 건 수 및 지원에 소비된 시간 등의 지표가 포함됩니다. 이는 범용 고객 지원 데이터 소스이며 특정 고객 서비스 애플리케이션이 지원되지 않는 경우에 사용해야 합니다. |

## 고객 만족 {#csat}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 범용 조사 데이터] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 서드파티 도구를 통해 얻은 조사 결과를 마케팅 보고서에 통합하고, 이를 통해 고객이 사이트와의 상호 작용에서 느끼는 만족도를 파악할 수 있습니다. 이는 범용 조사 데이터 소스이며 특정 조사 데이터 서비스가 지원되지 않는 경우에 사용해야 합니다. |

## 사이트 실적 {#performance}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 범용 사이트 다운로드 속도] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 다운로드 속도를 추적하는 애플리케이션이나 서비스에서 얻은 데이터를 데이터에 통합할 수 있습니다. 이는 범용 다운로드 속도 데이터 소스이며 특정 다운로드 속도 소프트웨어 또는 서비스가 지원되지 않는 경우에 사용해야 합니다. |

## 범용 {#generic}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 범용 데이터 소스(요약 데이터만)] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 마케팅 보고 및 분석에 가져오려는 데이터 유형과 유사한 내용이 검색되지 않을 때 이 데이터 소스를 사용하십시오. |
| [!UICONTROL 범용 데이터 소스(전체 처리)] | 전체 처리 | Adobe는 2022년 1월 31일에 전체 처리 데이터 소스에 대한 사용을 중단합니다. [자세히 알아보기](/help/import/c-data-sources/c-datasrc-types/datasrc-fullproc-eol.md) Adobe는 대신 [Bulk Data Insertion API(BDIA)](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)를 사용할 것을 권장합니다. |
| [!UICONTROL 범용 데이터 소스(거래 ID)] | <ul><li>거래 ID</li><li>방문자 ID</li></ul> | 오프라인 이벤트를 온라인 이벤트에 연결할 수 있습니다. [!UICONTROL 거래 ID]는 오프라인 이벤트와 온라인 이벤트 간에 핵심 역할을 합니다. |

## 온라인 구매 {#purchases}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 제품 반환] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 제품 반환 데이터를 가져와서 구매 ID와 연결하여 검색 엔진, 키워드, 캠페인, 그 외 반환을 일으킬 가능성이 높은 특성을 파악할 수 있습니다. |
| [!UICONTROL 제품 비용] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 비용이나 수익을 개별 제품과 연결함으로써 웹 사이트에서 구매되어 배송된 제품의 실제 비용을 제공하여 웹 사이트에 대한 가장 수익성 있는 캠페인, 키워드 및 내부 프로모션을 정확히 보고할 수 있습니다. |
| [!UICONTROL 주문 상태] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 지표를 사용하여 모든 주문의 상태(예: 취소된 주문, 배송된 주문, 완료된 주문 또는 부정 주문)를 나타낼 수 있습니다. 주문 상태 보고를 사용하면 어떤 획득 방법이 주문 완료율을 가장 많이 높이는지를 파악할 수 있습니다. |

## 리드 및 견적 {#leads}

| 데이터 소스 | 처리 유형 | 설명 |
| --- | --- | --- |
| [!UICONTROL 리드 생성] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 실제 발생 매출을 포함하여 웹 사이트에서 생성된 모든 리드에 대한 리드 결과 정보를 업로드할 수 있습니다. 매출이 실제로 리드 ID에 기여하면 수익이 가장 많이 나는 캠페인과 프로모션을 파악할 수 있습니다. |
| [!UICONTROL 온라인 견적] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 실제 발생 매출을 포함하여 웹 사이트에서 생성된 모든 리드에 대한 리드 결과 정보를 업로드할 수 있습니다. 매출이 실제로 리드 ID에 기여하면 수익이 가장 많이 나는 캠페인과 프로모션을 파악할 수 있습니다. |
| [!UICONTROL 콜 센터 데이터] | [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | 콜 센터 거래를 업로드하여 고객이 전화를 하게 만든 방법(캠페인, 프로모션 등)을 파악할 수 있습니다. |
