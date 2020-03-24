---
description: DFA용 Data Connectors 통합은 Analytics 변수를 사용하여 DFA 캠페인 결과를 추적합니다.
keywords: DFA
title: Analytics 변수 및 이벤트
topic: Data connectors
uuid: 8996cb58-c793-4600-99ef-af3064642b29
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Analytics 변수 및 이벤트{#analytics-variables-and-events}

DFA용 Data Connectors 통합은 Analytics 변수를 사용하여 DFA 캠페인 결과를 추적합니다.

캠페인 변수 외에 Analytics 이벤트 및 eVar을 사용할 수 있습니다. 이 DFA 통합에 사용할 이벤트 및 eVar을 확인했으면 Analytics 관리 콘솔을 사용하여 활성화하십시오. DFA 통합을 활성화하려면 먼저 통합 변수를 활성화해야 합니다. 아래 표는 DFA 통합에 필요한 Analytics 변수를 설명합니다.

| 변수 | 친숙한 이름 | 채우기 방법 | 설명 |
|---|---|---|---|
| s.campaign 또는 eVar | 광고 추적 코드 | DFA 캠페인에 대한 Data Connectors에 의해 자동으로 입력됩니다. | 모든 캠페인에 대해 클릭스루 전환을 추적합니다. |
| eVar* | 뷰스루 | DFA 캠페인용 VISTA 및 DFA를 통해 자동으로 입력됩니다. | DFA ID에 대한 뷰스루 데이터를 추적합니다. 이 eVar에는 *`s.campaign`* 변수를 채우는 방법을 설명합니다. 변수 공급자 ID에서 확인된 것과 같은 전환 변수여야 합니다. eVar에 전체 하위 관계가 활성화되어 있는지 확인합니다. 이 기능을 활성화하는 비용은 Data Connectors 통합 요금에 포함됩니다. |
| eVar* | DFA 쿼리 오류 | (선택 사항) JavaScript 수집 코드를 통해 입력됩니다. | DFA에서 반환되는 여러 오류 코드 중 하나를 포함합니다. |
| 업데이트* | 뷰스루 수 | DFA 캠페인에 대한 Data Connectors에 의해 자동으로 입력됩니다. | 사용자가 광고를 보고 클릭스루하지 않았지만 사이트에 도달한 횟수를 캡처합니다. |
| 업데이트* | 노출 횟수 | DFA의 데이터 피드를 통해 자동으로 입력됩니다. | 특정 DFA 광고가 게재된 횟수를 추적합니다. |
| 업데이트* | 클릭 수 | DFA의 데이터 피드를 통해 자동으로 입력됩니다. | 사용자가 특정 DFA 배너 광고를 클릭한 횟수를 추적합니다. 이 지표는 여러 가지 이유 중 하나로 인해 기본 Analytics 클릭스루 지표와 다른 횟수를 생성할 수 있습니다. 자세한 내용은 [지표 불일치 조정](/help/import/data-connectors/dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md)을 참조하십시오. |
| 업데이트* | DFA 시간 초과 | (선택 사항) JavaScript 수집 코드를 통해 입력됩니다. | DFA가 *`s.maxDelay`* 시간 초과 전에 응답하지 못한 횟수를 계산합니다. 이 경우 DFA 구현 문제가 있는지 판단하는 데 도움이 될 수 있습니다. |
| 업데이트* | DFA 미디어 비용 | DFA의 데이터 피드를 통해 자동으로 입력됩니다. | DFA 인터페이스에 입력한 미디어 비용 지표가 포함되어 있습니다. 이러한 지표가 표시되도록 하려면 DFA 쪽에서 이 기능을 활성화해야 합니다. |

*사용하지 않은 eVar 또는 사용자 지정 이벤트를 선택합니다.
