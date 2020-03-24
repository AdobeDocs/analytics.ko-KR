---
title: maxDelay
description: AppMeasurement가 이미지 요청을 보내기 전에 DFA의 응답을 기다리는 최대 시간을 결정합니다.
translation-type: ht
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# maxDelay

`s.maxDelay` 변수는 DFA 호스트를 접속할 때의 시간 제한 기간을 결정하기 위해 DFA Data Connector에서 주로 사용합니다. Adobe가 이 변수에 지정된 시간 설정 내에 DFA 서버의 응답을 받지 못하면 연결이 제공되고 데이터가 정상적으로 처리됩니다. 각 페이지에서의 DFA 응답 시간이 우려되는 경우에는 이 변수를 구현에 포함하십시오. 최적의 시간 제한 기간을 결정하려면 이 값으로 테스트하는 것이 좋습니다.

이 변수는 DFA Data Connector를 사용하는 구현에만 사용됩니다. DFA를 사용하는 구현에서도 이 변수는 선택 사항입니다.

## Adobe Experience Platform Launch의 최대 지연

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.maxDelay

이 `s.maxDelay` 변수는 AppMeasurement가 DFA의 응답을 기다리는 시간(밀리초)을 나타내는 정수입니다. AppMeasurement가 DFA로부터 제 시간에 응답을 받지 못하면 이미지 요청이 DFA 데이터 없이 Adobe로 전송됩니다.

```js
s.maxDelay = 750;
```

## 속성

* 대기 시간을 늘리면 더 많은 DFA 데이터가 모이지만, Analytics 히트 데이터를 잃을 위험도 늘어납니다. 사용자가 `s.maxDelay` 기간 중에 페이지를 떠나면 Analytics 히트 데이터가 손실됩니다.
* 대기 시간을 줄이면 Analytics 히트 데이터를 잃을 위험은 낮아지지만, 히트 데이터로 전송된 DFA 데이터의 양이 줄어들 수 있습니다.
* `s.maxDelay` 기간이 DFA 호스트가 응답할 충분한 시간을 수용하지 못하는 경우 DFA 통합 데이터가 손실됩니다.

> [!NOTE] Adobe에서는 DFA 응답 시간을 제어하지 않습니다. 최대 지연 시간을 합리적인 시간 범위로 올린 후에도 문제가 지속되는 경우에는 조직의 DFA 계정 관리자에게 문의하십시오.
