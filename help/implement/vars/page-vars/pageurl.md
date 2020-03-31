---
title: pageUrl
description: 사이트에서 자동으로 수집된 페이지 URL을 무시합니다.
translation-type: ht
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# pageUrl

AppMeasurement는 각 히트에서 페이지 URL을 자동으로 수집합니다. AppMeasurement에서 자동으로 수집한 페이지 URL을 무시하려면 이 변수를 사용할 수 있습니다. 대부분의 경우 이 변수를 설정할 필요가 없습니다.

> [!NOTE] 이 변수는 Analysis Workspace에서 사용할 수 있는 차원이 아닙니다. 이 변수는 Data Warehouse 및 데이터 피드에서만 사용할 수 있습니다. Analysis Workspace에서 페이지 URL을 차원으로 사용하려면 모든 히트에서 `pageURL` 변수를 eVar에 전달하는 것이 좋습니다.

경우에 따라 URL이 255바이트보다 길 수 있습니다. AppMeasurement는 이미지 요청에 있는 URL의 처음 255바이트에 대해 `g` 쿼리 문자열 매개 변수를 사용합니다. URL이 255바이트보다 긴 경우 URL의 나머지 부분은 `-g` 쿼리 문자열 매개 변수에 저장됩니다. URL의 프로토콜 및 쿼리 문자열은 이 변수에 포함됩니다.

## Adobe Experience Platform Launch의 페이지 URL

Launch는 페이지 URL을 자동으로 채웁니다. 하지만 Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 페이지 URL 무시를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 페이지 URL] 섹션을 찾습니다.

페이지 URL을 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.pageURL

`s.pageURL` 변수는 페이지의 URL을 포함하는 문자열입니다. AppMeasurement는 이 변수를 자동으로 수집하지만 원하는 경우 해당 값을 무시할 수 있습니다.

```js
s.pageURL = "https://example.com";
```

보고서에서 페이지 URL을 차원으로 사용하려면 구현에서 다음 내용을 사용하는 것이 좋습니다.

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```
