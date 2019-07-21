---
description: '추가 정보를 추적하려고 하지만 충분한 변수가 없다면 이제 추가 Evar 및 성공 이벤트에 액세스할 수 있습니다. '
keywords: Analytics 구현; Evar; events; Evar 번호; Evar의 몇; 이벤트 수
seo-description: '추가 정보를 추적하려고 하지만 충분한 변수가 없다면 이제 추가 Evar 및 성공 이벤트에 액세스할 수 있습니다. '
seo-title: 추가 Evar 및 이벤트
solution: Analytics
title: 추가 Evar 및 이벤트
topic: 개발자 및 구현
uuid: 6 F 53069 B -6941-40 F 1-9 DB 6-2 D 1839822 B 8 F
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 추가 Evar 및 이벤트

추가 정보를 추적하려고 하는데 충분한 변수가 없다면 이제 추가 eVar 및 성공 이벤트에 액세스할 수 있습니다.

>[!NOTE]
>
>JavaScript H-Code는 이러한 추가 evar 및 이벤트를 지원하지 않습니다.

## 사용자 지정 차원 및 이벤트에 대한 자격 {#section_869EC3D8A5614036A9C586F2B74FA7DC}

| Adobe Analytics 제품 |  |  |  |
|---|---|---|---|
| Adobe Analytics - 기본 | prop 75개 | eVar 200개 | 이벤트 1000개 |
| Adobe Analytics - [선택](https://www.adobe.com/data-analytics-cloud/analytics/select.html) | prop 75개 | eVar 200개 | 이벤트 1000개 |
| Adobe Analytics - [프라임](https://www.adobe.com/data-analytics-cloud/analytics/prime.html) | prop 75개 | eVar 200개 | 이벤트 1000개 |
| Adobe Analytics - [Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html) | prop 75개 | eVar 250개 | 이벤트 1000개 |

## 변수 및 이벤트 채우기 {#section_DEA51A22BCBB4B92BDD25814AAD296E4}

* Variables can be populated in the data collection library if you are using these versions of [!DNL AppMeasurement]:

   * JavaScript 버전 1.4+용 AppMeasurement
   * Flash 버전 3.9+용 AppMeasurement
   * Java 버전 1.2.8+용 AppMeasurement
   * Silverlight/.NET 버전 1.4.2+용 AppMeasurement
   * PHP 버전 1.2.2+용 AppMeasurement

* 이전 버전의 코드 또는 JavaScript H*를 사용하고 있는 경우 컨텍스트 데이터를 채우고 처리 규칙을 사용하여 변수를 채울 수 있습니다.
* 모든 버전의 데이터 수집 코드에는 이벤트 101~1000을 채울 수 있습니다.
* 처리 규칙은 컨텍스트 데이터 또는 다른 변수에 기반하여 eVar 76~250을 채우는 데 사용됩니다.

## FAQ {#section_E915B03236BD47DCA065F1FC5A6E30C6}

* **Adobe Analytics 인터페이스로 이러한 새 변수에 즉시 액세스할 수 있습니까?** 이러한 인터페이스는 즉시 이용할 수 있습니다. [!UICONTROL 분석 작업 공간], [!UICONTROL 보고 및 분석], [!UICONTROL 리포트 빌더], [!UICONTROL 애드혹 분석], API 및 [!UICONTROL 데이터 워크벤치].

* **이러한 추가 eVar 및 이벤트는 사용자 데이터 피드에 자동으로 표시됩니까?** 데이터 피드가 활성화되면 새 변수 및 이벤트에 액세스할 수 있습니다. 새 eVar 열은 포함하도록 선택할 때까지 표시되지 않습니다. 하지만 새 이벤트는 활성화되는 즉시 event_list 열에 표시되며 이벤트 조회 테이블에는 이러한 이벤트 ID에 대한 이벤트 이름이 포함됩니다. 새 이벤트를 데이터 피드에서 사용할 준비가 되지 않은 경우 활성화하지 마십시오.

* **새 데이터 피드 열을 어떻게 요청합니까?** 새 열을 요청하려면 [데이터 피드 구성](https://marketing.adobe.com/resources/help/en_US/sc/clickstream/datafeeds_configure.html)을 참조하십시오.

* **Analytics Prime으로 돌아가기를 원하는 Analytics Ultimate 고객이며, 현재 eVar가 200개 이상 활성화되어 있다면 어떻게 됩니까?** Adobe가 기존의 eVars를 비활성화하지 않지만, 더 이상 활성화할 수 없습니다. eVars를 비활성화하는 경우에는 Analytics Prime에서 활성화할 수 있는 eVar 한계(200)에 도달할 때까지 이를 다시 활성화할 수 없습니다.

