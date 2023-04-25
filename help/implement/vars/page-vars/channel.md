---
title: channel
description: '''사이트 섹션'' 차원을 채웁니다.'
feature: Variables
exl-id: f494a051-a296-4f1c-9044-04a8b59376fa
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 77%

---

# channel

`channel` 변수는 일반적으로 지정된 페이지가 있는 사이트의 섹션을 저장합니다. 이 변수는 사이트에서 가장 인기 있는 그룹을 파악하는 데 유용합니다. 이 변수는 &#39;사이트 섹션&#39; 차원을 채웁니다.

## 웹 SDK를 사용한 채널

채널은 [Adobe Analytics용 매핑](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) XDM 필드 아래 `web.webPageDetails.siteSection`.

## Adobe Analytics 확장을 사용하는 채널

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 채널을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 설정 [!UICONTROL 확장] 드롭다운 목록을 Adobe Analytics 및 [!UICONTROL 작업 유형] to [!UICONTROL 변수 설정].
6. [!UICONTROL 채널] 섹션을 찾습니다.

채널은 어떤 문자열 값 또는 데이터 요소로도 설정할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.channel

`s.channel` 변수는 일반적으로 페이지의 사이트 섹션을 포함하는 문자열입니다. 이 변수의 값은 최대 100바이트이며 더 긴 값은 잘립니다.

```js
s.channel = "Example site section";
```

`digitalData` [데이터 레이어](../../prepare/data-layer.md)를 사용하는 경우:

```js
s.channel = digitalData.page.category.primaryCategory;
```
