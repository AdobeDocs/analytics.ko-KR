---
title: decodeLinkParameters
description: AppMeasurement 이중 인코딩 링크 추적 변수를 활성화하거나 비활성화합니다.
exl-id: 329c521a-b965-4114-93ce-f45f159d4a20
feature: Variables
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 8%

---

# decodeLinkParameters

`decodeLinkParameters` 변수는 링크 추적 변수가 한 번(`true`(으)로 설정된 경우) 또는 두 번(`false`(으)로 설정된 경우) 인코딩되는지 여부를 결정하는 부울입니다. `linkName`([`tl()`](../functions/tl-method.md) 메서드의 일부) 및 [`linkURL`](linkurl.md)에만 영향을 줍니다. 사용하려면 AppMeasurement v2.24.0 이상이 필요합니다. 이 변수의 기본값은 `false`입니다.

v2.24.0 이전 버전의 AppMeasurement에서 링크 추적 변수는 항상 URL로 두 번 인코딩되었습니다. 일반적으로 싱글바이트 문자를 사용하는 구현에는 문제가 없지만, 이중 인코딩이 보고서에서 멀티바이트 문자에 대해 잘못 인코딩된 값을 만들었습니다. 이 변수를 `true`(으)로 설정하면 링크 추적 값이 한 번 인코딩되며, 이는 일반적으로 원하는 동작입니다.

* 구현에서 멀티바이트 문자를 사용하고 링크 추적 변수가 AppMeasurement의 이중 인코딩을 오프셋하도록 URL 디코딩되는 경우 이 변수를 `false`(으)로 설정하십시오. 이 값은 기존 AppMeasurement 기능을 유지합니다.
* Adobe 구현에서 멀티바이트 문자를 사용하고 URL 디코딩 링크 추적 값이 없는 경우 이 변수를 `true`(으)로 설정하는 것이 좋습니다.
* 구현에서 멀티바이트 문자를 사용하지 않는 경우에는 이 변수가 필요하지 않습니다. Adobe 그러나 멀티바이트 문자를 보낼 수 있는 경우에는 이 변수를 `true`(으)로 설정하는 것이 좋습니다.

## 웹 SDK를 사용하여 링크 매개 변수를 두 번 인코딩

이 변수는 AppMeasurement 전용이며, 웹 SDK 구현 유형에는 필요하지 않습니다.

## Adobe Analytics 확장을 사용하여 링크 매개 변수를 두 번 인코딩

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.decodeLinkParameters

`s.decodeLinkParameters` 변수는 링크 추적 값이 이중 인코딩되는지 여부를 결정하는 부울입니다. 이 변수가 정의되지 않은 경우 기본값은 `false`입니다. 이 변수는 기존 구현에 대한 기능을 유지합니다. Adobe 특히 링크 추적 보고서에 URL 인코딩 값이 표시되면 모든 새 구현에 대해 이 값을 `true`(으)로 설정하는 것이 좋습니다.

```js
s.decodeLinkParameters = true;
```
