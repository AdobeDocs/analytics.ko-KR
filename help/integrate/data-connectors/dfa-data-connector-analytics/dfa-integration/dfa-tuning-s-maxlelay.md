---
description: DFA를 성공적으로 구현하면 특정 사이트에 맞게 s.maxDelay가 최적화됩니다.
keywords: DFA
seo-description: DFA를 성공적으로 구현하면 특정 사이트에 맞게 s.maxDelay가 최적화됩니다.
seo-title: s.maxDelay 조정
solution: Analytics
title: s.maxDelay 조정
topic: Data connectors
uuid: 7640 af 26-6 ac 6-427 e -9 cfc -932 c 86 ccf 5 ab
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# s.maxDelay 조정{#tuning-s-maxdelay}을 참조하십시오

DFA를 성공적으로 구현하면 특정 사이트에 맞게 s.maxDelay가 최적화됩니다.

In general, the decision to raise or lower *`s.maxDelay`* involves a tradeoff between obtaining more DFA visitor data and endangering collecting Adobe visitor data. Increasing *`s.maxDelay`* obtains more DFA visitor data, but (placed excessively high) could endanger the collection of Adobe visitor data. s.maxDelay를 줄이면 Adobe 방문자 데이터 수집이 보장되지만 DFA 방문자 데이터를 손실할 수 있습니다.

*`s.maxDelay`* 는 네트워크 통신에서 DFA에 연락하는 시간 이상을 캡슐화합니다. 또한 이러한 통신이 기반으로 하는 JavaScript를 실행하고 평가하는 브라우저 지연을 나타냅니다. This is because the Integrate module begins the *`s.maxDelay`* timer after it has inserted the HTML element in to the DOM which pulls the data from the DFA Floodlight server. 브라우저에서 이 새 HTML 요소를 기반으로 하여 HTTP 요청을 실제로 시작하는 데 걸리는 시간은 동시에 로드하는 다른 이미지 또는 JavaScript 파일, 방문자 컴퓨터의 속도 및 특정 브라우저 구현에 따라 달라집니다. 또한 JSON 데이터를 DFA Floodlight 서버에서 검색할 때 브라우저에서 JavaScript를 평가해야 합니다. 이 작업은 브라우저에서 완전히 통제되며, 동시에 실행되는 JavaScript 코드 양이 많거나 비동기 JavaScript 요청이 많은 경우 지연될 수 있습니다.

이러한 사항을 염두에 두고 랜딩 페이지의 복잡성과 DFA의 네트워크 지연 정도에 따라 *`s.maxDelay`* 를 설정해야 합니다. 일부 사이트에서 복잡성을 줄이는 한 가지 방법은 페이지 로드 초반에 Adobe 수집 코드를 실행하여 Floodlight 서버에 요청할 때 브라우저에서 진행 중인 작업이 적어지도록 하는 것입니다.

시간 초과 변수는 *`s.maxDelay`*&#x200B;로 설정되기 때문입니다. When deciding whether to increase or decrease *`s.maxDelay`* we recommend following this process:

1. Collect several days of data with *`s.maxDelay`* set to a particular value.
1. Run a [!DNL Daily Unique Visitors Report] for the time range.
1. Run the [!DNL Timeout Event Report] to check the number of timeouts that are coming through. 시간 초과는 방문자당 한 번만 수집됩니다.

이제 숫자를 확인하고 계산해 보겠습니다

```
Timeout Percentage = [Step 3] / [Step 2] * 100
```

시간 초과 비율은 실제로 사이트에 대한 모든 방문자를 고려합니다. 그러한 방문자 중 일부는 DFA에 전혀 연결되지 않으므로 시간 초과가 잘못된 것입니다. To improve this computation, another analysis could consider only unique visitors to pages with the `clickThroughParam` set (for example, `?CID=1`). 이로 인해 정확성이 더 향상됩니다.

시간 초과 비율이 매우 낮으면 *`s.maxDelay`*. 너무 높으면 *`s.maxDelay`*. When decreasing *`s.maxDelay`*, you will want to rerun the [!DNL Timeout Report] to ensure that timeouts have not dramatically increased. When increasing *`s.maxDelay`*, you will want to run a [!DNL Page Views Report] to make sure page views aren’t falling out due to lost data. Each time *`s.maxDelay`* is changed observe the data for several days in order to ensure that the data represents a trend, and not just a day-to-day fluctuation.

The optimal setting for *`s.maxDelay`* is the point at which the timeout percentage is minimized while Page Views do not drop off.

시간 초과는 통합 버전 2.0으로 이동할 때 줄어들 수 있습니다. 302개 리디렉이 삭제되기 때문입니다. 베타 클라이언트에서 초기 찾기는 시간 초과에서 일관된 감소를 보여 주었으므로 더 많은 DFA 데이터가 수집되고 있음을 보여주었습니다.
