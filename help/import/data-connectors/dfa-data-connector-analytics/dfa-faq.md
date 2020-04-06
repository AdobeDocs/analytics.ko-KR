---
description: 'null'
keywords: DFA
title: FAQ
topic: Data connectors
uuid: 59d187e9-1ec1-4cf3-8831-b981f87c9372
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# FAQ{#frequently-asked-questions}

## Data Connectors 마법사가 내 로그인 자격 증명을 수락하지 않는 이유는 무엇입니까? {#section-f019b3de18774df3954af7881aa564fa}

로그인 자격 증명이 유효한지 확인한 경우 통합에 제공된 사용자 이름이 API 액세스에 대해 활성화되었는지 확인합니다. 데이터 커넥터 마법사는 DFA API를 사용하여 로그인 자격 증명을 확인하고 DFA API에서 Adobe 관련 설정을 끕니다. API 액세스는 관리자가 DFA 인터페이스 내에서 설정해야 하는 설정입니다. 그런 다음 마법사에서 선택한 광고주 ID 또는 Floodlight 구성 ID에 액세스할 수 있는 권한이 있는지 확인합니다.

## 야간 업로드된 지표(DFA 노출 횟수, DFA 클릭 수 등)의 데이터가 표시되지 않는 이유는 무엇입니까? {#section-465fd22ae6b447ffb6baf20b57daa433}

통합 버전 1.5를 사용 중인 경우 통합에 클라이언트 사이트 ID가 아직 지정되지 않았기 때문일 수 있습니다. 야간 교환을 수행하고 DFA 광고 서버에서 데이터를 요청하려면 CSID(클라이언트 사이트 ID)가 필요합니다. CSID는 Google과 통합한 날로부터 최대 3일 정도 소요될 수 있습니다. Google에서 CSID를 받으면 최신 JavaScript 코드와 함께 새 CSID의 통합 이메일 주소로 알림을 받을 것입니다.

3일 이상 경과했지만 설정 이메일을 받지 못했고 지표가 실행되지 않는 경우 CSID가 이미 다른 통합에 할당되어 있는 것이 가장 큰 문제가 됩니다. Google은 CSID와 보고서 세트 간 1-1 매핑을 유지 관리합니다. 즉, 한 보고서 세트의 통합에서 다른 보고서 세트의 다른 통합과 동일한 광고주 ID를 사용하는 경우 첫 번째 보고서만 CS ID가 지정됩니다. CSID가 매핑되는 보고서 세트 또는 광고주 ID를 변경하려면 Google 지원으로 티켓을 열어야 합니다.

예를 들어 광고주 ID Z가 있는 보고서 세트 A에 CSID가 할당되는 통합이 있다고 가정합니다. 나중에 광고주 Z와 함께 보고서 세트 B에서 다른 통합이 설정되면, 이 최신 통합은 CSID에 다시 할당되지 않습니다. 이 경우 Google 티켓이 필요합니다. 반면에 광고주 ID Z와 함께 보고서 세트 A의 통합 예를 살펴보고, 보고서 세트 A의 다른 통합에서 광고주 Z가 설정됩니다. 첫 번째 통합만이 통합에 대한 데이터를 수신하게 됩니다.그러나 이 경우 첫 번째 통합을 비활성화할 수 있으며 두 번째 통합으로 데이터가 전달됩니다.

>[!NOTE] CSID는 통합 버전 2.0에서 사용되지 않으므로, CSID 협상 처리가 적용되지 않습니다.

## 통합 버전 2.0을 사용하고 있으며 비용 지표가 DFA 광고에 나타나지 않습니다. 왜 그럴까요? {#section-805748111bbe4bbf918d6dbbb2641fff}

비용 지표는 Google DFA 측에서 모두 켜지고 DFA 인터페이스에서 제공되어야 하며 데이터 커넥터 마법사에서 켜져야 합니다. 먼저 DFA 미디어 비용에 대한 Analytics 이벤트를 매핑하고 통화 코드를 제공했는지 확인합니다. 미디어 비용 이벤트를 매핑하고 마법사를 완료하고 저장하는 경우 DFA API에서 DFA omnitureCostData 플래그가 설정됩니다. 이 메시지는 Google에 지표가 야간 파일로 전송되어야 함을 알립니다. 통합된 Floodlight에서 속성을 확인하여 omnitureCostData가 활성화되었는지 DFA 인터페이스를 통해 다시 확인할 수 있습니다. 마지막으로 이 두 곳을 확인한 후 통합 Floodlight의 일부인 광고가 비용 데이터 및 비용 구조를 지정하는지 확인합니다. 비용 데이터가 DFA 인터페이스에 제공되지 않으면 Analytics에 표시되지 않습니다.

## 특정 광고는 DFA 노출 횟수 또는 뷰스루를 표시하지 않지만 클릭과 클릭스루를 표시하는 이유는 무엇입니까? {#section-39b2eeeefd7f43d1a373df0b987bacef}

클릭 데이터만 기록하는 일부 광고인 클릭추적기라고 합니다. 이러한 유형의 광고는 Floodlight 서버를 쿼리할 때 마지막 노출 데이터를 반환하지 않습니다. 특정 광고가 클릭 추적기 또는 클릭 전용 광고인지 확인하려면 DFA 에이전시 또는 Google 지원 담당자에게 문의하십시오.

## DFA 클릭 수를 표시하는 광고에 클릭스루가 없는 이유는 무엇입니까? {#section-758c1f1fc5b54bfc9294dcdc71bbd96a}

이것에 대한 많은 대답 중 하나가 있을 수 있습니다.

첫째, 문제의 광고에 (a) 불일치를 보고 있는 동일한 보고서 세트에 대해 Adobe 코드로 태그 지정된 랜딩 페이지 URL이 있는지 확인하고 (b) *`clickThroughParam`* 쿼리 문자열 매개 변수를 포함하는지 확인합니다.

두 번째, [성공적인 DFA 통합 확인](../dfa-data-connector-analytics/dfa-integration.md)의 단계를 수행하여 작동 중인 통합이 있는지 확인합니다. 랜딩 페이지에서 Adobe 히트를 통해 DFA 추적 코드가 도착한 것이 보이면 클릭스루가 DFA 캠페인 보고서에 표시되는 것을 볼 수 있습니다. 표시되지 않는 경우 보고서 세트가 랜딩 페이지의 *`s.account`* 변수와 Reports &amp; Analytics에 표시 중인 보고서 세트 간에 일치하는지 확인하십시오. 이러한 일치의 경우, DFA:XXX:XXX:XXX:XXX:llXXX:XXX:XXX:XXX:XXX:XXX와 같은 eVar를 통해 보기 보고서에서 추적 코드를 확인합니다.

DFA의 원시 데이터를 다이제스트할 DFA VISTA 규칙의 실패를 나타냅니다. 이 문제는 Adobe 계정 담당자에게 지원 티켓을 열어 해결할 수 있습니다.

위의 해결 방법 중 하나라도 문제를 설명하는 것이 없으면 지표 [불일치](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md) 조정을 참조하여 다른 가능성을 모색하십시오.
