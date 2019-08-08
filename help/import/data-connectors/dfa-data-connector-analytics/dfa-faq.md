---
description: 'null'
keywords: DFA
seo-description: 'null'
seo-title: FAQ
solution: Analytics
title: FAQ
topic: Data connectors
uuid: 59 d 187 e 9-1 ec 1-4 cf 3-8831-b 981 f 87 c 9372
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# FAQ{#frequently-asked-questions}

## Data Connectors 마법사가 내 로그인 자격 증명을 수락하지 않는 이유는 무엇입니까? {#section-f019b3de18774df3954af7881aa564fa}

로그인 자격 증명이 올바른지 확인한 경우에는 다음으로 통합에 제공한 사용자 이름이 API 액세스에 대해 활성화되었는지 확인합니다. Data Connectors 마법사는 DFA API를 사용하여 로그인 자격 증명을 확인하고 DFA API에서 Adobe 특정 설정을 끄고 켭니다. API 액세스는 관리자가 DFA 인터페이스 내에서 켜야 하는 설정입니다. 그런 다음 마법사에서 선택한 광고주 ID 또는 Floodlight 구성 ID에 대한 액세스 권한이 있는지 확인합니다.

## 밤마다 업로드한 지표(DFA 노출 횟수, DFA 클릭 수 등)의 데이터가 표시되지 않는 이유는 무엇입니까? {#section-465fd22ae6b447ffb6baf20b57daa433}

통합 버전 1.5를 사용하는 경우 통합이 클라이언트 사이트 ID에 아직 할당되지 않았기 때문일 수 있습니다. 밤마다 교환이 발생하고 DFA 광고 서버에서 데이터를 요청하려면 CSID(클라이언트 사이트 ID)가 필요합니다. CSID는 통합일로부터 Google과 교환하는 데 최대 3일이 걸릴 수 있습니다. Google에서 CSID를 받으면 최신 JavaScript 코드와 함께 새 CSID의 통합 이메일 주소로 알림을 받을 것입니다.

3일이 지난 후에도 설정 이메일을 받지 못하고 지표가 입력되지 않은 경우 가장 가능성 있는 문제는 CSID가 이미 다른 통합에 할당되었다는 것입니다. Google은 CSID와 보고서 세트 간에 1:1 매핑을 유지합니다. 즉, 한 보고서 세트의 통합이 다른 보고서 세트의 다른 통합과 같은 광고주 ID를 사용하면 첫 번째 보고서 세트에만 CS ID가 할당됩니다. CSID를 매핑할 보고서 세트 또는 광고주 ID를 변경하려면 Google 지원 팀과 함께 티켓을 열어야 합니다.

예를 들어, 광고주 ID Z가 있는 보고서 세트 A에 CSID가 할당되는 통합이 있다고 가정합니다. 다른 통합은 광고주 Z가 있는 보고서 세트 B에서 나중에 설정되는 경우 이 최신 통합이 CSID에 재할당되지 않습니다. 이 경우 Google 티켓이 필요합니다. 하지만 광고주 ID Z를 통해 보고서 세트 A에서 통합의 예를 가져오고 나중에 다른 통합을 보고서 세트 A에 가져오면 광고주 Z가 설정됩니다. 첫 번째 통합만 통합에 대한 데이터를 받습니다. 하지만, 이 경우 첫 번째 통합을 비활성화하면 데이터가 두 번째 통합에 입력됩니다.

>[!NOTE]
>
>CSID는 통합의 버전 2.0에서 사용되지 않으므로 CSID 협상 프로세스가 적용되지 않습니다.

## 통합 버전 2.0을 사용하는 데 내 DFA 광고에 대한 비용 지표가 표시되지 않습니다. 이유가 무엇입니까? {#section-805748111bbe4bbf918d6dbbb2641fff}

비용 지표는 양쪽 Google DFA 쪽에서 켜져 있고 DFA 인터페이스에서 제공해야 할 뿐만 아니라 Data Connectors 마법사에서 켜져 있어야 합니다. 먼저 DFA 미디어 비용에 대한 Analytics 이벤트를 매핑하고 통화 코드를 제공했는지 확인합니다. 미디어 비용 이벤트를 매핑하고 마법사를 완료한 후 저장하면 DFA omnitureCostData 플래그가 DFA API에서 켜집니다. 이는 밤마다 파일로 지표를 보내야 한다는 것을 Google에 알리는 것입니다. 통합된 Floodlight에서 속성을 보고 omnitureCostData가 활성화되었는지 DFA 인터페이스를 통해 다시 확인할 수 있습니다. 마지막으로, 이러한 두 위치를 확인한 후에 통합된 Floodlight에 포함된 광고에서 비용 데이터와 비용 구조를 지정하는지 확인합니다. 비용 데이터가 DFA 인터페이스에 제공되지 않으면 분석에 표시되지 않습니다.

## 특정 광고에 DFA 노출 횟수 또는 뷰스루가 표시되지 않지만 클릭 수 및 클릭스루가 표시되는 이유는 무엇입니까? {#section-39b2eeeefd7f43d1a373df0b987bacef}

clicktrackers라고 하는 클릭 데이터만 기록하는 몇 가지 광고가 있습니다. 이러한 유형의 광고는 Floodlight 서버에 쿼리하면 마지막 노출 횟수 데이터를 반환하지 않습니다. 특정 광고가 clicktracker이거나 클릭 전용 광고인지 확인하려면 DFA 에이전시 또는 Google 지원 담당자에게 문의하십시오.

## DFA 클릭 수를 표시하는 광고에 클릭스루가 없는 이유는 무엇입니까? {#section-758c1f1fc5b54bfc9294dcdc71bbd96a}

이에 대한 여러 가지 답변 중 하나는 다음과 같습니다.

먼저, 문제가 있는 광고에 (a) 불일치가 표시된 동일한 보고서 세트에 대해 Adobe 코드 태그가 지정되고 (b) *`clickThroughParam`* 쿼리 문자열 매개 변수가 포함된 랜딩 페이지 URL이 있는지 확인합니다.

둘째, 성공적인 DFA 통합 [확인 단계를 통해 작업 통합을 수행했는지](../dfa-data-connector-analytics/dfa-integration/dfa-confirm-integration.md#concept-c1c869d2a6fa46b09fe41fc286e407c6)확인합니다. 랜딩 페이지에서 Adobe 히트를 통해 DFA 추적 코드가 도착한 것이 보이면 클릭스루가 DFA 캠페인 보고서에 표시되는 것을 볼 수 있습니다. 도착했는지 모를 경우 랜딩 페이지의 *`s.account`* 변수와 보고 및 분석에서 본 보고서 세트 간에 보고서 세트가 일치하는지 확인합니다. 이들이 일치하면 뷰스루 eVar 보고서에서 추적 코드가 DFA:XXX:XXX:XXX:llXXX:XXX:XXX:XXX:XXX 형식인지 확인합니다.

이들은 DFA에서 원시 데이터를 다이제스트하는 DFA VISTA 규칙 오류를 나타냅니다. 이 문제는 Adobe 계정 담당자를 통해 지원 티켓을 열어서 해결할 수 있습니다.
위의 해결 방법들이 문제를 설명하는 것이 아니라면 [지표 불일치를](../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies/dfa-reconciling-metric-discrepancies.md#concept-8c31ebe761ca4b3fab1e3a18ef5d098f) 조정하여 다른 가능성을 탐색합니다.