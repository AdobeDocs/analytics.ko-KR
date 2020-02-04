---
title: campaign
description: '''추적 코드'' 차원을 채웁니다.'
translation-type: tm+mt
source-git-commit: c5a60bc9756af2742740dbc6a26a081f55ee3235

---


# campaign

이 `campaign` 변수는 사이트에서 추적 코드를 수집하기 위해 사용됩니다. 이전 버전의 Adobe Analytics에서는 대부분의 차원에 대한 분류로 사용할 수 있는 특별 처리가 있었습니다. 현재 버전의 Adobe Analytics에서는 eVar와 동일하게 작동합니다.

이 변수는 &#39;추적 코드&#39; 차원을 채웁니다.

## Adobe Experience Platform Launch의 캠페인

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 캠페인을 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [ [!UICONTROL 동작]]에서 기존 Adobe Analytics - [!UICONTROL 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을 변수][!UICONTROL 설정으로]설정합니다.
6. 캠페인 [!UICONTROL 섹션을] 찾습니다.

캠페인을 값 또는 쿼리 문자열 매개 변수로 설정할 수 있습니다.

## s.campaign in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.campaign` 변수는 일반적으로 마케팅 활동에 사용되는 추적 코드를 포함하는 문자열입니다. 최대 길이는 255바이트입니다.100바이트보다 긴 값은 Adobe로 전송될 때 자동으로 잘립니다.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
