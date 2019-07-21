---
description: Analytics와 Audience Manager는 모두 세그먼트를 사용합니다. 그러나 Analytics 세그먼트는 Audience Manager 세그먼트와 정확히 일치하지 않습니다. 이러한 차이는 부분적으로 Analytics와 Audience Manager 보고서에서 나타나는 불일치에 기인합니다. 결과적으로 이러한 두 가지 솔루션에서 세그먼트로 작업을 시작할 때 이러한 차이점을 이해하는 것이 중요하고 유용합니다.
seo-description: Analytics와 Audience Manager는 모두 세그먼트를 사용합니다. 그러나 Analytics 세그먼트는 Audience Manager 세그먼트와 정확히 일치하지 않습니다. 이러한 차이는 부분적으로 Analytics와 Audience Manager 보고서에서 나타나는 불일치에 기인합니다. 결과적으로 이러한 두 가지 솔루션에서 세그먼트로 작업을 시작할 때 이러한 차이점을 이해하는 것이 중요하고 유용합니다.
seo-title: Analytics 및 Audience Manager의 세그먼트 이해
title: Analytics 및 Audience Manager의 세그먼트 이해
uuid: 13 F 7 D 1 D 7-6 A 3 F -42 F 1-822 E -8 D 3523999 EFA
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Analytics 및 Audience Manager의 세그먼트 이해

Analytics와 Audience Manager는 모두 세그먼트를 사용합니다. 그러나 Analytics 세그먼트는 Audience Manager 세그먼트와 정확히 일치하지 않습니다. 이러한 차이는 부분적으로 Analytics와 Audience Manager 보고서에서 나타나는 불일치에 기인합니다. 결과적으로 이러한 두 가지 솔루션에서 세그먼트로 작업을 시작할 때 이러한 차이점을 이해하는 것이 중요하고 유용합니다.

## Audience Manager 세그먼트 {#section_417DC4B5648547778A27E42CE1D09900}

Audience Manager 세그먼트는 논리적 규칙에 따라 결합된 일련의 정의된 트레이트의 대상 방문자 그룹(사용자 ID)입니다. 다음 네 가지 기준에 따라 방문자(사용자 ID)가 Audience Manager의 세그먼트에 속하는지 판단합니다.

* 세그먼트 자체 및 각 세그먼트를 구성하는 트레이트에 설정된 규칙. 이러한 규칙은 세그먼트의 대상이 되기 위해 사용자 ID가 충족해야 하거나 나타내야 하는 조건을 정의합니다.
* 알고리즘 모델링. 특정 세그먼트의 대상 사용자는 알고리즘 모델링 및 분석을 기반으로 한 다른 세그먼트의 대상일 수 있습니다.
* TTL(Time-to-Live) 간격. 세그먼트 멤버십은 설정된 간격 이후에 만료되거나 무기한 유지될 수 있습니다.
* 최신성 및 빈도. 사용자가 상호 작용(트레이트 실현)을 하는 시기와 빈도를 정의하면 사이트, 섹션 또는 특정 크리에이티브의 실제 관심 수준을 기반으로 하여 세그먼트를 만드는 데 도움이 됩니다.

Audience Manager 세그먼트 멤버십은 유동적입니다. 사용자는 현재 시점에서 세그먼트 기준에 적합한지 여부에 따라 세그먼트를 입력하거나 제외시킬 수 있습니다. 즉, Audience Manager 세그먼트 채우기는 시간이 지나면서 증가하거나 감소할 수 있습니다.

Audience Manager 세그먼트는 Analytics의 대상으로 표시됩니다.

자세한 내용은 [세그먼트 빌더의 트레이트 및 세그먼트 채우기 데이터](https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html) 및 [신호, 트레이트 및 세그먼트](https://marketing.adobe.com/resources/help/en_US/aam/c_signal_trait_segment.html)를 참조하십시오.

## Analytics 세그먼트 {#section_62EC584BB7134E10923BCBA7F9BD89A8}

Analytics 세그먼트는 보고서의 데이터를 필터링하는 메커니즘입니다. 필터링은 Audience Manager 에서처럼 방문자 수준에서와는 달리 방문자, 방문 또는 히트 수준에서 발생할 수 있습니다. Analytics 세그먼트를 Audience Manager 세그먼트와 비교할 때 고려할 몇 가지 중요한 요소가 있습니다.

* Analytics 세그먼트는 Audience Manager 세그먼트와 다른 데이터 세트에서 작동합니다. 데이터 수집 중에 Analytics는 Audience Manager에서 사용할 수 없는 데이터에 다른 여러 후 처리 단계를 적용합니다. 후 처리에는 eVar 지속성, 처리 규칙, 조회(지리적 위치, 모바일 장치), VISTA 등이 포함될 수 있습니다. Audience Manager는 서버측 전달(또는 DIL)을 통해 사전 처리된 데이터를 수신합니다.

   일반 데이터 불일치는 Analytics에서 만료되지 않는 차원을 기준으로 한 세그먼트를 Audience Manager의 동일한 차원과 비교할 때 발생합니다. 예를 들면 만료되지 않는 listVars 또는 머천다이징 eVars가 해당됩니다.

   예를 들어 eVar = blue이고 Analytics에 만료되지 않도록 설정된 경우 "eVar = blue" 기준을 사용한 Analytics의 세그먼트에는 항상 이 방문자가 포함됩니다. 반면 Audience Manager에서는 이 방문자가 설정된 기간 이후에 비슷하게 정의된 세그먼트에서 제외될 수 있습니다.

* Analytics 세그먼트에는 AAM 세그먼트보다 많은 기능이 있습니다. Audience Manager 세그먼트는 항상 방문자 수준에서 평가됩니다. Analytics 세그먼트는 방문자, 방문 또는 히트 수준(또는 이들 수준의 조합)에서 정의할 수 있습니다. 또한 Analytics는 순차 세그멘테이션과 같이 Audience Manager가 지원하지 않는 고급 세그멘테이션 기능을 지원합니다.
* 앞에서 언급했듯이 Audience Manager 방문자는 현재 시점에서 세그먼트 기준에 적합한지 여부에 따라 세그먼트를 입력하거나 제외시킬 수 있습니다.

   반대로 Analytics에서 방문자는 보고 날짜 범위에 따라 세그먼트에 포함되거나 제외됩니다. 예를 들어 한 방문자가 지난달에 구매했습니다. AAM에서 해당 방문자는 날짜 범위에 관계없이 "구매자" 세그먼트에 포함됩니다. Analytics에서 이번 달을 기준으로 한 보고서에는 세그먼트에 방문자를 포함하지 않습니다. 그러나 이번 달과 지난 달을 기준으로 한 보고서에는 세그먼트에 방문자가 포함됩니다.

자세한 내용은 [Analytics 세그멘테이션 안내서](https://marketing.adobe.com/resources/help/en_US/analytics/segment/)를 참조하십시오.
