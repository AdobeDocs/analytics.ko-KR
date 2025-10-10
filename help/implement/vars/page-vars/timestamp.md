---
title: timestamp
description: 히트의 타임스탬프를 수동으로 설정합니다.
feature: Appmeasurement Implementation
exl-id: 9d5ce5ef-2d84-4f65-b2e3-7aa3e219bc34
role: Admin, Developer
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 81%

---

# timestamp

`timestamp` 변수는 타임스탬프가 활성화된 보고서 세트에 대한 히트의 타임스탬프를 수동으로 설정합니다.

>[!WARNING]
>
>보고서 세트가 타임스탬프가 지정된 히트를 수락하도록 명시적으로 구성되지 않은 경우 이 변수를 사용하지 마십시오. AppMeasurement는 타임스탬프가 지정된 히트를 지원하지 않는 보고서 세트에 대해 히트 시간을 자동으로 설정합니다. 타임스탬프를 지원하지 않는 보고서 세트에 이 변수를 사용하는 히트를 전송하면 해당 데이터가 영구적으로 유실됩니다.

## 웹 SDK을 사용한 타임스탬프

타임스탬프가 XDM 필드 [&#x200B; 아래에 있는 &#x200B;](/help/implement/aep-edge/xdm-var-mapping.md)Adobe Analytics에 대해 매핑됨`xdm.timestamp`입니다. 이 필드는 Unix 시간만 지원합니다.

## Adobe Analytics 확장을 사용한 타임스탬프

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.timestamp

`s.timestamp` 변수는 히트의 날짜 및 시간을 포함하는 문자열입니다. 올바른 타임스탬프 형식에는 [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) 및 [Unix 시간](https://en.wikipedia.org/wiki/Unix_time)이(가) 포함됩니다(초).

```js
// Timestamp using ISO 8601
s.timestamp = "2024-01-01T00:00:00Z";

// Timestamp using Unix timestamp
s.timestamp = "1577836800";

// Automatically get the current Unix timestamp
s.timestamp = Math.round(new Date().getTime()/1000);

// Automatically get the current ISO 8601 timestamp
s.timestamp = new Date().toISOString();
```

## ISO 8601 값

[ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)에 표현된 날짜 및 시간은 몇 가지 다른 양식을 사용할 수 있습니다. Adobe는 ISO 8601의 일부 기능을 지원하지 않습니다.

* 날짜와 시간을 모두 `T`로 구분하여 모두 입력해야 합니다.
* 시간과 분은 필수이며, 초는 선택 사항이지만 사용하는 것이 좋습니다.
* 주차와 서수 날짜는 지원되지 않습니다.
* 날짜는 표준 형식이나 확장 형식으로 지정할 수 있습니다. 예를 들어 `2024-01-01T00:00:00Z`와 `20240101T000000Z`는 모두 유효합니다.
* 분수 분 및 초는 기술적으로 유효하지만 Adobe에서는 분수 부분을 무시합니다.
* 시간대는 표준 및 확장 형식으로 지원됩니다.

다음은 `timestamp` 변수의 유효한 ISO 8601 값 예입니다.

```text
2024-01-01T00:00:00+00:00
2024-01-01T00:00:00Z
2024-01-01T00:00:00
2024-01-01T00:00
20240101T000000+0000
20240101T000000Z
20240101T000000
20240101T0000
```
