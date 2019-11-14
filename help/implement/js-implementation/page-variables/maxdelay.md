---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# maxDelay

s.maxDelay 변수는 DFA 호스트를 접속할 때의 시간 초과 제한 시간을 결정하기 위해 Genesis DFA 통합에서 주로 사용합니다. Adobe가 변수에 지정된 시간 설정 내에 DFA 서버의 응답을 받지 못하면 연결이 끊기고 데이터가 정상적으로 처리됩니다. 각 페이지에서의 DFA 응답 시간에 관심이 있다면 이 변수를 구현하십시오. 최적의 시간 초과 제한 시간을 결정하려면 이 값으로 실험해 보는 것이 좋습니다.

<!-- 

maxDelay.xml

 -->

**구현 예**

```
s.maxDelay="750";
```

**속성**

* 이 변수는 사이트에 구현된 JavaScript를 통해 채워진 선택 사항 이벤트 지표입니다.
* DFA 호스트가 주어진 시간 내에 응답하지 않을 경우, [시간 초과]에 지정된 이벤트가 실행됩니다(Genesis 통합 마법사를 통해 지정됨).
* 이 변수에는 숫자 값만 포함할 수 있습니다.
* 지정된 시간의 크기는 밀리초 단위로 측정됩니다.
* 대기 시간을 늘리면 더 많은 DFA 데이터가 모이지만, Analytics 히트 데이터를 잃을 위험도 늘어납니다.

   사용자가 *`s.maxDelay`* 기간 중에 페이지에서 멀리 탐색하면 Analytics 히트 데이터가 손실됩니다.

* 대기 시간을 줄이면 Analytics 히트 데이터를 잃을 위험은 낮아지지만, 히트 데이터로 전송된 DFA 데이터의 양이 줄어들 수 있습니다.

   *`s.maxDelay`* 기간이 DFA 호스트가 응답할 충분한 시간을 수용하지 못하는 경우 DFA 통합 데이터가 손실됩니다.

> [!NOTE] Adobe에서는 DFA 응답 시간을 제어하지 않습니다. 최대 지연 시간을 합리적인 시간 범위로 올린 후에도 문제가 지속되는 경우에는, 조직의 DFA 계정 관리자에게 문의하십시오.
