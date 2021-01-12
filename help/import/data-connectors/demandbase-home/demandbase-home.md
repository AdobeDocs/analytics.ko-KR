---
description: 'null'
title: Adobe Analytics용 Demandbase Data Connector
uuid: 28fddb8f-06f6-4447-8257-4a59131bedbe
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 96%

---


# Adobe Analytics용 Demandbase Data Connector{#demandbase-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Adobe는 2021년 8월 1일에 Adobe 데이터 커넥터 기술을 사용 중단할 예정입니다. [추가 정보...](/help/import/data-connectors/data-connectors-eol.md)

이 Adobe® Data Connectors 통합은 Demandbase의 실시간 ID 서비스와 Adobe Analytics의 행동 정보를 결합하여 B2B 조직을 위한 강력한 분석, 최적화 및 컨텐츠 개인화 기회를 만듭니다.

사전 결정된 특성에 따라 잠재 고객에게 관련 컨텐츠를 전달하고 더 조건이 좋은 리드에 주력하여 전환율을 높일 수 있습니다. 특정 업계, 회사 규모 또는 특정 회사 자체와 관련된 컨텐츠를 제공하면 사이트에서 찾는 내용에 의존하지 않고 방문자에게 올바른 메시지를 직접 전달할 수 있습니다. 이를 통해 바운스 수가 줄어들고 더 정상적이고 조건이 좋은 전환 단계가 생성됩니다.

## 주요 이점 및 기능{#key-benefits-and-features}

5가지 주요 이점 및 기능을 나열합니다.

* 회사 이름, 업계 및 매출 범위와 같은 8개의 표준 Demandbase 조직 차원에 대한 트래픽 및 전환 보고를 제공합니다.
* 선택 가능한 8개의 추가 Demandbase 차원을 포함할 수 있습니다. 여기에는 계정 감시 차원이 포함될 수 있습니다.
* Demandbase 차원을 사용하여 Adobe Experience Cloud에서 세그먼트를 생성하고 적용할 수 있습니다.
* 보고서 세트 변수 최적화를 제공합니다. 2개의 사용자 지정 전환 변수(eVar)만 사용하여 가능한 16개의 모든 Demandbase 차원을 캡처할 수 있습니다.
* 통합 Demandbase 차원을 Adobe Target으로 전송하여 특정 대상을 타깃팅하는 데 사용할 수 있습니다.

## 통합 사전 요구 사항{#integration-prerequisites}

Adobe 및 Demandbase 고객을 위한 주요 사전 요구 사항을 설명합니다.

### Adobe 고객을 위한 사전 요구 사항 {#section-ce8963ca1c1741009d842222c6a49063}

* Adobe Analytics의 현재 고객이어야 합니다.
* Data Connectors를 사용하려면 권한이 있는 Adobe Experience Cloud 관리 사용자여야 합니다.
* 보고서 세트 내에 사용할 수 있고 활성화된 eVar 변수가 1개 이상 있어야 합니다. 두 번째 eVar는 선택 사항입니다.

### Demandbase 고객을 위한 사전 요구 사항 {#section-08e14afe216a4b0db9e7e2965894de6f}

* Demandbase의 현재 고객이어야 합니다.
* Analytics에 대해 라이선스가 부여된 유효한 Demandbase API 키가 있어야 합니다.
* **선택 사항:** 컨텐츠 개인화에 대해 라이선스가 부여된 유효한 Demandbase API 키가 있어야 합니다. Adobe Target 내에서 통합된 Demandbase 차원을 활성화하려는 경우에만 필요합니다.
