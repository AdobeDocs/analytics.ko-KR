---
title: maxDelay
description: AppMeasurement가 이미지 요청을 보내기 전에 DFA의 응답을 기다리는 최대 시간을 결정합니다.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# maxDelay

The `s.maxDelay` variable is used in the DFA data connector to determine the timeout period in contacting the DFA host. Adobe가 이 변수에 설정된 지정된 기간 내에 DFA의 서버로부터 응답을 받지 못하면 연결이 끊기고 데이터가 정상적으로 처리됩니다. 각 페이지에서 DFA의 응답 시간이 걱정되는 경우 이 변수를 구현에 포함하십시오. 최적의 시간 초과 기간을 결정하려면 이 값으로 테스트하는 것이 좋습니다.

이 변수는 DFA 데이터 커넥터를 사용하는 구현에만 사용됩니다. DFA를 사용하는 구현에서도 이 변수는 선택 사항입니다.

## Adobe Experience Platform 론치의 최대 지연

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.maxDelay in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.maxDelay` 변수는 AppMeasurement가 DFA의 응답을 기다리는 시간(밀리초)을 나타내는 정수입니다. AppMeasurement가 DFA로부터 제 시간에 응답을 받지 못하면 DFA 데이터 없이 이미지 요청이 Adobe로 전송됩니다.

```js
s.maxDelay = 750;
```

## 속성

* 대기 시간을 늘리면 더 많은 DFA 데이터가 모이지만, Analytics 히트 데이터를 잃을 위험도 늘어납니다. Losing Analytics hit data happens when the user navigates away from the page during the `s.maxDelay` period.
* 대기 시간을 줄이면 Analytics 히트 데이터가 손실될 위험이 낮아지지만, 히트 데이터와 함께 전송된 DFA 데이터의 양을 줄일 수 있습니다.
* Losing DFA integration data happens when the `s.maxDelay` period does not accommodate enough time for the DFA host to respond.

> [!NOTE] Adobe에서는 DFA 응답 시간을 제어하지 않습니다. 최대 지연 시간을 적절한 시간으로 올린 후에도 문제가 일관적인 경우 조직의 DFA 계정 관리자에게 문의하십시오.
