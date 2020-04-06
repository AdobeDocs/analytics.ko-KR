---
title: contextData
description: 컨텍스트 데이터 변수를 사용하면 처리 규칙이 읽을 수 있는 각 페이지에서 사용자 지정 변수를 정의할 수 있습니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# contextData

컨텍스트 데이터 변수를 사용하면 처리 규칙이 읽을 수 있는 각 페이지에서 사용자 지정 변수를 정의할 수 있습니다. 코드에서 값을 Analytics 변수에 명시적으로 할당하는 대신 컨텍스트 데이터 변수에 데이터를 보낼 수 있습니다. 그러면 처리 규칙이 컨텍스트 데이터 변수 값을 가져와 각 Analytics 변수에 전달합니다. 관리자 가이드의 [처리 규칙](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)을 참조하십시오.

컨텍스트 데이터 변수는 개발 팀이 번호가 매겨진 변수 대신 명명된 요소의 데이터를 수집하는 데 유용합니다. 예를 들어, 개발 팀에게 페이지의 작성자를 `eVar10`에 할당하도록 요청하는 대신 `s.contextData["author"]`에 할당하도록 요청할 수 있습니다. 그런 다음 조직의 Analytics 관리자는 처리 규칙을 만들어 컨텍스트 데이터 변수를 보고를 위한 분석 변수에 매핑할 수 있습니다. 개발 팀은 궁극적으로 Adobe가 제공하는 많은 페이지 변수 대신 컨텍스트 데이터 변수만 걱정하게 됩니다.

## Adobe Experience Platform Launch의 컨텍스트 데이터 변수

Launch에는 컨텍스트 데이터 변수를 설정하는 전용 위치가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.contextData

`s.contextData` 변수는 값을 바로 사용하지 않습니다. 대신 이 변수의 속성을 문자열로 설정합니다.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* 유효한 컨텍스트 데이터 변수에는 영숫자, 밑줄 및 마침표만 포함됩니다. Adobe는 하이픈과 같은 다른 문자를 포함하는 경우 처리 규칙을 통한 데이터 수집을 보장하지 않습니다.
* 컨텍스트 데이터 변수를 `"a."`으로 시작하지 마십시오. 이 접두사는 Adobe에 의해 예약되어 사용 중입니다. 예를 들어 `s.contextData["a.InstallEvent"]`를 사용하지 마십시오.
* 컨텍스트 데이터 변수는 대/소문자를 구분하지 않습니다. 변수 `s.contextData["example"]`과 `s.contextData["EXAMPLE"]`은 동일합니다.

## 처리 규칙을 사용하여 분석 변수 채우기

>[!IMPORTANT] 컨텍스트 데이터 변수는 처리 규칙 실행 후 무시됩니다. 값을 변수에 배치하는 처리 규칙이 활성화되어 있지 않으면 해당 데이터가 영구적으로 손실됩니다.

1. 구현을 업데이트하여 컨텍스트 데이터 변수 이름 및 값을 설정합니다.
2. Adobe Analytics에 로그인하고 관리 > 보고서 세트로 이동합니다.
3. 원하는 보고서 세트를 선택한 다음, 설정 편집 > 일반 > 처리 규칙으로 이동합니다.
4. Analytics 변수를 컨텍스트 데이터 변수 값으로 설정하는 처리 규칙을 만듭니다.
5. 변경 사항을 저장합니다.

처리 규칙은 저장 후 즉시 적용됩니다. 이전 데이터에는 적용되지 않습니다.

## 링크 추적 호출에서 컨텍스트 데이터 보내기

컨텍스트 데이터 변수를 [`s.linkTrackVars`](../config-vars/linktrackvars.md)의 다음 `contextData` 속성으로 포함하십시오.

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```
