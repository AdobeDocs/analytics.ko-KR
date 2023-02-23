---
title: campaign
description: '''추적 코드'' 차원을 채웁니다.'
feature: Variables
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
source-git-commit: e46b15eedda78303e6e29faceea6db8483eee277
workflow-type: ht
source-wordcount: '244'
ht-degree: 100%

---

# campaign

`campaign` 변수는 사이트에서 추적 코드를 수집하는 데 사용됩니다. 이전 버전의 Adobe Analytics에는 대부분의 차원에 대한 분류로 사용할 수 있는 특별 처리 방법이 있었습니다. 현재 버전의 Adobe Analytics에서는 이 변수가 eVar와 동일하게 작동합니다.

이 변수는 [추적 코드](/help/components/dimensions/tracking-code.md) 차원을 채웁니다. 일반적으로 [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) 유틸리티 메서드를 사용하여 쿼리 문자열에서 값을 가져옵니다. 그러나 이 변수의 설정 방법을 정확히 결정하는 것은 조직입니다.

## Web SDK를 사용한 캠페인

캠페인은 XDM 필드 `marketing.trackingCode` 아래에서 [Adobe Analytics에 대해 매핑됩니다](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html).

## Adobe Analytics 확장을 사용한 캠페인

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 캠페인을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 캠페인] 섹션을 찾습니다.

캠페인을 값 또는 쿼리 문자열 매개 변수로 설정할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.campaign

`s.campaign` 변수는 일반적으로 마케팅 활동에 사용되는 추적 코드를 포함하는 문자열입니다. 최대 길이는 255바이트이고, 255바이트보다 긴 값은 Adobe에 전송될 때 자동으로 잘립니다.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
