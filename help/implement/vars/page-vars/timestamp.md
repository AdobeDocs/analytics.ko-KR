---
title: timestamp
description: 히트의 타임스탬프를 수동으로 설정합니다.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# timestamp

이 `timestamp` 변수는 타임스탬프가 활성화된 보고서 세트에 대한 히트의 타임스탬프를 수동으로 설정합니다.

> [!WARNING] 보고서 세트가 타임스탬프가 지정된 히트를 수락하도록 명시적으로 구성되지 않은 경우 이 변수를 사용하지 마십시오. AppMeasurement는 타임스탬프가 지정된 히트를 지원하지 않는 보고서 세트에 대한 히트 시간을 자동으로 설정합니다. 타임스탬프를 지원하지 않는 보고서 세트로 이 변수를 사용한 히트를 전송하는 경우 해당 데이터가 영구적으로 손실됩니다.

## Adobe Experience Platform Launch의 타임스탬프

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.timestamp in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.timestamp` 변수는 히트의 날짜 및 시간을 포함하는 문자열입니다. 유효한 타임스탬프 포맷에는 ISO [8601](https://en.wikipedia.org/wiki/ISO_8601) 및 [Unix 시간이](https://en.wikipedia.org/wiki/Unix_time)포함됩니다.

```js
// Timestamp using ISO 8601
s.timestamp = "2020-01-01T00:00:00Z";

// Timestamp using Unix timestamp
s.timestamp = "1577836800";

// Automatically get the current Unix timestamp
s.timestamp = Math.round(new Date().getTime()/1000);

// Automatically get the current ISO 8601 timestamp
s.timestamp = new Date().toISOString();
```

## ISO 8601 값

ISO 8601에서 [표현된 날짜 및](https://en.wikipedia.org/wiki/ISO_8601) 시간은 여러 가지 다른 양식을 사용할 수 있습니다. Adobe는 ISO 8601의 일부 기능을 지원하지 않습니다.

* Both the date and time must be provided, separated by `T`.
* 시간과 분,초는 선택 사항이지만 권장됩니다.
* 주차와 서수 날짜는 지원되지 않습니다.
* 날짜는 표준 형식 또는 확장 형식으로 지정할 수 있습니다. 예를 들어, `2020-01-01T00:00:00Z` 및 `20200101T000000Z` 은 모두 유효합니다.
* 분수 분 및 초는 기술적으로 유효하지만 Adobe는 분수 값을 무시합니다.
* 표준 및 확장 포맷에서 표준 시간대를 지원합니다.

다음은 `timestamp` 변수의 유효한 ISO 8601 값 예입니다.

```text
2020-01-01T00:00:00+00:00
2020-01-01T00:00:00Z
2020-01-01T00:00:00
2020-01-01T00:00
20200101T000000+0000
20200101T000000Z
20200101T000000
20200101T0000
```
