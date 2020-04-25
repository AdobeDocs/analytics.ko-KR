---
title: 레퍼러
description: 히트에 대해 자동으로 수집된 레퍼러를 무시합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 레퍼러

`referrer` 변수는 보고서에서 자동으로 수집된 레퍼러를 무시합니다. 이 변수는 리디렉션하거나 방문자를 일시적으로 결제 프로세서에 전달하는 동안 등 레퍼러가 손실될 수 있는 상황에서 유용하며, &#39;레퍼러&#39; 및 &#39;참조 도메인&#39; 차원을 채우는 데에도 도움이 됩니다.

## Adobe Experience Platform Launch의 레퍼러

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 레퍼러를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 레퍼러] 섹션을 찾습니다.

레퍼러를, 데이터 요소를 포함한 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.referrer

`s.referrer` 변수는 이전 페이지의 URL을 포함하는 문자열입니다. 이 변수는 최대 255바이트를 저장할 수 있습니다. 255바이트보다 큰 값은 잘립니다. AppMeasurement는 이 변수를 자동으로 `document.referrer`로 설정합니다. 자동으로 수집된 값을 무시하려면 이 변수를 설정할 필요가 없습니다.

```js
s.referrer = "https://example.com";
```

이 변수를 URL이 아닌 값으로 설정하지 마십시오.

## 예

많은 조직은 리디렉션에 따라 구현을 처리합니다. 사이트가 레퍼러를 포함하는 경우 [`Util.getQueryParam()`](../functions/util-getqueryparam.md) 유틸리티를 사용하여 URL에서 레퍼러를 얻을 수 있습니다. URL이 쿼리 문자열에 포함된 모든 값을 인코딩하는지 확인하십시오.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
