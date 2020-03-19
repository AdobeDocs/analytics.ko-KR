---
title: referrer
description: 히트에 대해 자동으로 수집된 레퍼러를 무시합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# referrer

이 `referrer` 변수는 보고서에서 자동으로 수집된 레퍼러를 무시합니다. 이 변수는 리디렉션을 수행하거나 방문자를 지불 처리자로 일시적으로 전달하는 등 레퍼러가 손실될 수 있는 상황에서 유용합니다. 이 변수는 &#39;레퍼러&#39; 및 &#39;참조 도메인&#39; 차원을 채우는 데 도움이 됩니다.

## Adobe Experience Platform Launch의 레퍼러

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 레퍼러를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. 섹션을 [!UICONTROL Referrer] 찾습니다.

레퍼러를 데이터 요소를 포함한 모든 문자열 값으로 설정할 수 있습니다.

## s.referrer in AppMeasurement and Launch custom code editor

이 `s.referrer` 변수는 이전 페이지의 URL을 포함하는 문자열입니다. 이 변수는 최대 255바이트를 저장할 수 있습니다.255바이트보다 큰 값은 잘립니다. AppMeasurement는 이 변수를 자동으로 다음으로 `document.referrer`설정합니다.자동으로 수집된 값을 무시하려면 이 변수를 설정할 필요가 없습니다.

```js
s.referrer = "https://example.com";
```

이 변수를 URL이 아닌 값으로 설정하지 마십시오.

## 예

많은 조직은 리디렉션에 대한 구현을 처리합니다. 사이트에서 레퍼러를 수용하는 경우 이 [`Util.getQueryParam()`](../functions/util-getqueryparam.md) 유틸리티를 사용하여 URL에서 레퍼러를 얻을 수 있습니다. URL이 쿼리 문자열에 포함된 모든 값을 인코딩하는지 확인하십시오.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
