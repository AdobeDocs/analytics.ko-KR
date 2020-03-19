---
title: s_gi()
description: AppMeasurement 인스턴스를 만들고 추적합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# s_gi

이 `s_gi()` 함수는 보고서 세트 ID로 AppMeasurement 인스턴스를 인스턴스화하거나 찾습니다. AppMeasurement keeps track of every instance created, and `s_gi()` returns the existing instance for a report suite if one exists. 인스턴스가 존재하지 않으면 새 인스턴스가 생성됩니다.

## Adobe Experience Platform Launch의 s_gi()

Analytics 확장 기능은 추적 개체를 인스턴스화하고 관리합니다. 그러나 Adobe Analytics 확장 기능을 구성할 때 [!UICONTROL Library Management] 아코디언에서 전역 추적 개체를 설정할 수도 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 아코디언을 [!UICONTROL Library Management] 확장하고 다른 라디오 단추를 선택합니다 [!UICONTROL Manage the library for me].

전역 변수 텍스트 필드를 사용하면 사용자 지정 추적 개체를 설정할 수 있습니다. Its default value is `s`.

## s_gi() in AppMeasurement 및 Launch 사용자 지정 코드 편집기

추적 개체를 인스턴스화하는 `s_gi()` 함수를 호출합니다. 이 인수에는 쉼표로 구분된 보고서 세트 ID 문자열이 들어 있습니다. 보고서 세트 ID 인수가 필요합니다.

> [!TIP] 이 `s` 변수를 추적 개체로 사용하는 것이 좋습니다. Adobe `s` 는 설명서, 구현 예제 및 플러그인에서 사용합니다. 하지만 사이트 전체에서 일관적인 변수를 사용할 수 있습니다.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

> [!CAUTION] 다음 섹션 및 예제는 복잡한 구현 주제를 포함합니다. 구현을 철저히 테스트하고 조직의 [솔루션 디자인 문서에서](../../prepare/solution-design.md)중요한 사용자 지정을 추적합니다.

## 다른 추적 개체를 사용하여 여러 구현 관리

여러 추적 개체를 인스턴스화하는 경우 다른 데이터를 다른 보고서 세트로 보낼 수 있습니다. 이러한 두 추적 개체는 서로 독립적으로 작동합니다.

```js
// Instantiate two separate tracking objects to two different report suites
var s = s_gi('examplersid1');
var z = s_gi('examplersid2');

// The s object and z object contain their own independent Analytics variables simultaneously
s.pageName = "Example page name 1";
z.pageName = "Example page name 2";

// Send data to the examplersid1 report suite
s.t();

// Send data to the examplersid2 report suite
z.t();
```

## s 개체를 덮어쓴 후 AppMeasurement 변수 복원

일부 타사 도구는 JavaScript `s` 개체를 사용할 수도 있습니다. 실수로 사이트의 `s` 개체를 덮어쓴 경우 동일한 RSID 문자열 인수로 `s_gi` 호출하여 덮어쓴 모든 변수와 메서드를 복원할 수 있습니다.

```js
// Step 1: Instantiate the tracking object
var s = s_gi("examplersid");

// Step 2: Set eVar1
s.eVar1 = "Example value";

// Step 3: Accidentally overwrite the tracking object
s = "3rd party tool";

// Step 4: If you attempt to send a tracking call, an error is returned. Instead, re-instantiate the tracking object
s = s_gi("examplersid");

// Step 5: The previous values of all variables are preserved. You can send a tracking call and eVar1 is correctly set
s.t();
```

## 여러 변수가 있는 동일한 추적 개체 참조

두 변수가 동일한 보고서 세트와 동일한 `s_gi()` 함수를 참조하는 경우 변수를 함께 사용할 수 있습니다.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
