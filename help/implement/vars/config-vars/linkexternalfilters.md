---
title: linkExternalFilters
description: linkExternalFilters 변수를 사용하여 자동 종료 링크 추적을 돕습니다.
translation-type: tm+mt
source-git-commit: 8f7baa770f800ffe800e760f1eca59911d3db348

---


# linkExternalFilters

AppMeasurement는 사이트 외부의 링크를 자동으로 추적하는 기능을 제공합니다. 이 `trackExternalLinks` `true`경우 방문자가 링크를 클릭하여 사이트를 떠날 때 이미지 요청이 Adobe로 바로 전송됩니다. 및 `linkTrackExternalFilters` `linkTrackInternalFilters` 변수는 내부/외부 링크로 간주되는 링크를 결정합니다.

이 변수에 값이 포함되어 있으면 자동 종료 링크 추적은 화이트리스트 같은 방식으로 동작합니다. 링크 클릭이 `linkExternalFilters` 값과 일치하지 않으면 종료 링크로 간주되지 않습니다. 이 변수에 대해 전체 URL이 검사됩니다. 이 `linkLeaveQueryString` 경우 쿼리 문자열도 `true`검사됩니다.

> [!TIP] 종료 링크로 간주할 도메인을 정확히 알고 있는 경우에만 이 변수를 사용하십시오. 많은 조직은 종료 링크 추적 요구 사항에 `linkInternalFilters` 대해 를 사용해도 충분하며 사용하지 않는다는 것을 알고 `linkExternalFilters`있습니다.

동시에 `linkInternalFilters` 사용하는 경우 클릭한 링크가 `linkExternalFilters` 일치해야 하고 `linkExternalFilters` 종료 링크로 **** `linkInternalFilters` 간주되지 않습니다. 클릭한 링크가 종료 링크와 다운로드 링크 기준을 모두 만족하는 경우 다운로드 링크 유형이 우선순위가 지정됩니다.

## 아웃바운드 링크 - Adobe Experience Platform 실행에서 추적

추적 필드는 Adobe Analytics 확장 기능을 구성할 때 링크 추적 [!UICONTROL 아코디언 아래에 있는] 필터(일반적으로 도메인)의 쉼표로 구분된 목록입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. [아웃바운드 링크 [!UICONTROL - 추적] ] [!UICONTROL 필드를 표시하는 [링크 추적]] 아코디언을확장합니다.

이 필드에 항상 외부 필터를 배치할 수 있습니다. 공백 없이 여러 도메인을 쉼표로 구분합니다.

## s.linkExternalFilters in AppMeasurement and Launch custom code editor

이 `s.linkExternalFilters` 변수는 종료 링크를 고려하는 필터(예: 도메인)가 포함된 문자열입니다. 공백 없이 쉼표를 사용하여 여러 도메인을 구분합니다.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

다음 구현 예를 설정 `adobe.com`그대로 고려하십시오.

```html
<script>
  s.trackExternalLinks = true;
  s.linkExternalFilters = "example.com,example.net";
</script>

<!-- The following link is not considered an exit link, even though the link is outside adobe.com -->
<a href = "example.org">Example link 1</a>

<!-- The following link is an exit link because it matches the linkExternalFilters whitelist -->
<a href = "example.com">Example link 2</a>
```
