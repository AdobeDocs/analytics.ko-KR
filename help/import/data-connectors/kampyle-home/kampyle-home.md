---
description: 'null'
title: Adobe Analytics용 Kampyle Data Connector
uuid: f7733c81-93f5-4c50-b83a-721a6fbd4e8e
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Adobe Analytics용 Kampyle Data Connector{#kampyle-data-connector-for-adobe-analytics}

Adobe Analytics용 Kampyle Data Connector는 Kampyle의 통합 피드백 시스템과 Adobe Analytics®의 행동 보고 기능을 결합하여 조직에 강력한 분석 및 최적화 기회를 제공합니다.

온라인 마케터는 브랜드 구축 및 비즈니스 성과 창출에 있어 고객 피드백의 관련성을 점점 더 많이 실감하고 있습니다. Adobe Analytics®용 Kampyle Data Connector는 Adobe Analytics에 방문자 피드백 지표 및 차원을 추가합니다. 방문자의 태도 및 의견 맥락에서 방문자 행동을 분석할 수 있도록 해줍니다. 따라서 피드백을 기반으로 최적화하고 전환율을 향상시킬 수 있습니다.

## 통합 사전 요구 사항{#integration-prerequisites}

Data Connectors를 활성화하기 전에 고려해야 할 사전 요구 사항입니다.

### Adobe 고객을 위한 사전 요구 사항: {#section-d9c2e266931249e596de5f4406b5b6f0}

* 현재 Adobe Analytics 고객이어야 합니다.
* 관리 사용자여야 합니다.
* 보고서 세트 내에 사용 가능하고 활성화된 eVar 변수가 1개 있어야 합니다.
* 보고서 세트 내에 사용 가능하고 활성화된 사용자 지정 이벤트가 3개 있어야 합니다(유형: counter).

### Kampyle 고객을 위한 사전 요구 사항: {#section-4bbbca50e74d4f218414ae0cc535b8e9}

* Kampyle for Websites의 현재 고객이어야 합니다.
* Data Connectors를 사용하려면 권한이 있는 Adobe Experience Cloud 관리 사용자여야 합니다.
* Kampyle 피드백 양식 관리 UI에서 Kampyle 개인 키를 검색할 수 있어야 합니다.

## Kampyle 개인 키 검색{#retrieve-the-kampyle-private-key}

Kampyle 인터페이스 내에서 키를 검색하는 단계입니다.

1. [https://www.kampyle.com/login](https://www.kampyle.com/login)에서 Kampyle 계정에 로그인합니다.
1. 왼쪽 탐색 창에서 **[!UICONTROL 피드백 양식]** > **[!UICONTROL 피드백 양식 사용자 지정]**&#x200B;으로 이동합니다.

   ![](assets/retrieve_key1.png)

1. 기본 컨텐츠 창의 아래쪽에 나열된 개인 키를 찾습니다.

   ![](assets/retrieve_key2.png)
