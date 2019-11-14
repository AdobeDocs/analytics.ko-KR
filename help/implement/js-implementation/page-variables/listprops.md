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



# List Props

목록 prop은 변수로 전달되는 값의 목록을 구분 기호로 구분한 후 개별 라인 항목으로 보고하는 것입니다. 목록 prop은 일반적으로 확인란 또는 라디오 단추와 같이 사용자가 선택 가능한 값이 포함된 페이지에 구현됩니다. 여러 이미지 요청을 보내지 않고 변수에서 여러 값을 정의하려는 경우 유용합니다.

<!-- 

list_props.xml

 -->

**고려 사항**

* 목록 Prop은 트래픽 변수([prop](/help/implement/js-implementation/c-variables/page-variables.md))에서만 활성화됩니다.
* 경로 지정 및 상관 관계는 목록 prop에 대해 활성화할 수 없습니다.
* Analytics에서는 모든 목록 prop 보고서를 포함하여 거의 모든 보고서에 방문 횟수 및 방문자 수를 제공합니다.
* 목록 Prop에는 분류가 지원됩니다.
* 모든 사용자 지정 트래픽 변수는 목록 Prop이 될 수 있습니다. (예외: [pageName](/help/implement/js-implementation/c-variables/page-variables.md), [channel](/help/implement/js-implementation/c-variables/page-variables.md) 및 [server](/help/implement/js-implementation/c-variables/page-variables.md))

* 동일한 이미지 요청에서 중복 값을 정의하면, 인스턴스가 중복되지 않습니다.

Prop은 [관리 도구] &gt; [보고서 세트] &gt; [트래픽 변수] 페이지에서 [목록 지원]을 활성화한 다음 구분 기호를 선택하여 목록 Prop으로 변경할 수 있습니다. 많이 사용하는 구분 기호는 콜론, 세미콜론, 쉼표 또는 파이프입니다. 기술적으로는 ASCII 문자의 처음 127개 중 원하는 것을 사용할 수 있습니다.

**구현 예제** {#section_A3DD7293A8BB4807B42BFB1F73BE11AC}

목록 Prop 활성화를 요청할 때 사용할 구분 기호를 지정합니다. 선택한 *`s.prop`*&#x200B;이 활성화되고 나면 다음 예와 같이 변수에 여러 값을 설정할 수 있습니다.

파이프를 구분 기호로 사용하며 두 값을 전달하는 목록 Prop:

```js
s.prop1="Banner ad impression|Sidebar impression"
```

쉼표를 구분 기호로 사용하며 여러 값을 전달하는 목록 Prop:

```js
s.prop2="cerulean,vermilion,saffron"
```

단일 값과 함께 목록 Prop을 전송할 수도 있습니다.

```js
s.prop3="Single value"
```

구분 기호는 언제든지 변경할 수 있습니다. 그러나 구현과 새 구분 기호가 일치해야 합니다. 올바른 구분 기호를 사용하지 않으면 보고서에서 목록 Prop 값이 단일 연결된 라인 항목으로 취급됩니다.

목록 Prop도 트래픽 변수이기 때문에 트래픽 변수의 제한이 적용됩니다. 목록 prop은 데이터가 100바이트로 제한되어 있으며, 대소문자 구분 설정의 영향을 받습니다.

