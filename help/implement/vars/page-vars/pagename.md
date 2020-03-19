---
title: pageName
description: 사이트의 페이지 이름.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# pageName

이 `pageName` 변수는 일반적으로 지정된 페이지의 이름을 저장합니다. 가장 인기 있는 개별 페이지를 결정하는 데 유용합니다. 이 변수는 &#39;페이지 이름&#39; 차원을 채웁니다.

> [!NOTE] 이 차원은 항상 링크 추적 호출에서 제거됩니다. 링크가 추적된 페이지 이름을 보려면 이 변수를 eVar에 복사하는 것이 좋습니다.

이 변수가 지정된 페이지 추적 호출에 정의되지 않은 경우 [`pageURL`](pageurl.md) 변수가 대신 사용됩니다.

## Adobe Experience Platform Launch의 페이지 이름

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 페이지 이름을 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. 섹션을 [!UICONTROL Page name] 찾습니다.

페이지 이름을 데이터 요소를 포함한 모든 문자열 값으로 설정할 수 있습니다.

## s.pageName in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.pageName` 변수는 일반적으로 페이지 이름을 포함하는 문자열입니다. 최대 값 100바이트입니다.긴 값이 잘립니다. 이 잘림에는 이 변수가 비어 있는 `pageURL` 경우 이 변수가 다시 잘리는 인스턴스가 포함됩니다.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```
