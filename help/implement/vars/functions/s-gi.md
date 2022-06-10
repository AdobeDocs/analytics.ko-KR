---
title: s_gi ()
description: AppMeasurement 인스턴스를 생성하고 추적합니다.
feature: Variables
exl-id: f87eff07-7e60-480b-8334-3db538c1030e
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 68%

---

# s_gi

`s_gi()` 함수는 보고서 세트 ID로 AppMeasurement 인스턴스를 인스턴스화하거나 찾습니다. AppMeasurement는 생성된 모든 인스턴스를 추적하고 `s_gi()`는 보고서 세트에 대한 기존 인스턴스가 존재하면 이를 반환합니다. 인스턴스가 존재하지 않는 경우에는 새로운 인스턴스가 생성됩니다.

## 웹 SDK 확장을 사용하여 추적 개체를 인스턴스화합니다

웹 SDK 확장은 추적 개체를 인스턴스화하고 관리합니다. 그러나 확장 설정에서 추적 개체 이름을 사용자 지정할 수 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동합니다. [!UICONTROL 확장] 탭을 클릭한 다음 **[!UICONTROL 구성]** 단추를 클릭합니다.
1. 변경 [!UICONTROL 이름] 필드를 원하는 값으로 설정합니다. 기본값은 `alloy`입니다.

## 웹 SDK를 수동으로 구현하는 추적 개체를 인스턴스화합니다

다음 코드는 웹 SDK를 로드하고 추적 개체를 인스턴스화합니다. 문자열을 변경하여 추적 개체 이름을 사용자 지정할 수 있습니다 `"alloy"` 인라인 스크립트의 끝에서 원하는 값으로 되돌립니다.

```js
<script>
  !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
  []).push(o),n[o]=function(){var u=arguments;return new Promise(
  function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
  (window,["alloy"]);
</script>
<script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.min.js" async></script>
```

자세한 내용은 [SDK 설치](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=ko-KR?lang=ko-KR) 를 참조하십시오.

## Adobe Analytics 확장을 사용하여 추적 개체를 인스턴스화합니다

Analytics 확장은 추적 개체를 인스턴스화하고 관리합니다. 그러나 Adobe Analytics 확장을 구성할 때 [!UICONTROL 라이브러리 관리] 아코디언에서 전역 추적 개체를 설정할 수도 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 라이브러리 관리] 아코디언을 확장하고 [!UICONTROL 라이브러리 자동 관리]를 제외한 임의의 라디오 버튼을 선택합니다.

전역 변수 텍스트 필드를 사용하면 사용자 지정 추적 개체를 설정할 수 있습니다. 기본값은 `s`입니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s_gi()

추적 개체를 인스턴스화하려면 `s_gi()` 함수를 호출하십시오. 이 함수의 유일한 인수에는 쉼표로 구분된 보고서 세트 ID 문자열이 들어 있습니다. 보고서 세트 ID 인수는 필수입니다.

>[!TIP]
>
>`s` 변수를 추적 개체로 사용하는 것이 좋습니다. Adobe에서는 설명서, 구현 예 및 플러그인에서 `s`를 사용합니다. 하지만 사이트 전체에서 일관적이기만 하다면 어떤 변수든 사용할 수 있습니다.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

>[!CAUTION]
>
>다음 섹션 및 예에는 복잡한 구현 주제가 포함되어 있습니다. 구현을 철저히 테스트하고 조직의 [솔루션 디자인 문서](../../prepare/solution-design.md)에서 중요한 사용자 지정 사항을 추적하십시오.

## 다양한 추적 개체를 사용한 여러 구현 관리

여러 추적 개체를 인스턴스화하는 경우 다양한 데이터를 다양한 보고서 세트에 보낼 수 있습니다. 다음 두 추적 개체는 서로 독립적으로 작동합니다.

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

일부 서드파티 도구는 JavaScript `s` 개체를 사용할 수도 있습니다. 실수로 사이트의 `s` 개체를 덮어쓴 경우 동일한 RSID 문자열 인수로 `s_gi`를 호출하여 덮어쓴 모든 변수와 메서드를 복원할 수 있습니다.

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

두 변수가 동일한 보고서 세트로 동일한 `s_gi()` 함수를 참조하는 경우 변수를 서로 교환하여 사용할 수 있습니다.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
