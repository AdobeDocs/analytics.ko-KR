---
title: doubleEncodeLinkParameter
description: AppMeasurement 이중 인코딩 링크 추적 변수를 활성화하거나 비활성화합니다.
source-git-commit: d0e3b28590b24d630a192ee857a7d84c115dc8c1
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 7%

---

# doubleEncodeLinkParameter

다음 `doubleEncodeLinkParameters` 변수는 링크 추적 변수가 한 번 인코딩되는지 여부를 결정하는 부울입니다( 로 설정된 경우). `false`) 또는 두 번(로 설정된 경우) `true`). 영향만 미칩니다. `linkName` (일부 [`tl()`](../functions/tl-method.md) 방법) 및 [`linkURL`](linkurl.md). 사용하려면 AppMeasurement 2.23.1 이상이 필요합니다. 이 변수의 기본값은 입니다 `true`.

이전 버전의 AppMeasurement에서 링크 추적 변수는 항상 URL로 두 번 인코딩되었습니다. 일반적으로 싱글바이트 문자를 사용하는 구현에는 문제가 없지만, 이중 인코딩이 보고서에서 멀티바이트 문자에 대해 잘못 인코딩된 값을 만들었습니다. 이 변수를 로 설정 `false` 링크 추적 값을 한 번 인코딩합니다. 이는 일반적으로 원하는 동작입니다.

* 구현에서 멀티바이트 문자를 사용하고 링크 추적 변수가 AppMeasurement의 이중 인코딩을 오프셋하기 위해 URL 디코딩되는 경우 이 변수를 로 설정하십시오. `true`. 이 값은 기존 AppMeasurement 기능을 유지합니다.
* Adobe 구현에서 멀티바이트 문자를 사용하고 URL 디코딩 링크 추적 값이 없는 경우 이 변수를 로 설정하는 것이 좋습니다. `false`.
* 구현에서 멀티바이트 문자를 사용하지 않는 경우에는 이 변수가 필요하지 않습니다. 그러나 Adobe은 이 변수를 로 설정할 것을 권장합니다 `false` 멀티바이트 문자를 보낼 수 있는 경우.

## 웹 SDK를 사용하여 링크 매개 변수를 두 번 인코딩

이 변수는 AppMeasurement 전용이며, 웹 SDK 구현 유형에는 필요하지 않습니다.

## Adobe Analytics 확장을 사용하여 링크 매개 변수를 두 번 인코딩

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.doubleEncodeLinkParameters

다음 `s.doubleEncodeLinkParameters` 변수는 링크 추적 값이 이중 인코딩되는지 여부를 결정하는 부울입니다. 이 변수가 정의되지 않으면 기본값은 입니다. `true` 를 사용하여 기존 구현에 대한 기능을 유지할 수 있습니다. Adobe은 이 값을 로 설정할 것을 권장합니다 `false` 모든 새로운 구현, 특히 링크 추적 보고서에 URL 인코딩 값이 표시되는 경우.

```js
s.doubleEncodeLinkParameters = false;
```
