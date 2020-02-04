---
title: channel
description: '''사이트 섹션'' 차원을 채웁니다.'
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# channel

이 `channel` 변수는 일반적으로 지정된 페이지가 있는 사이트의 섹션을 저장합니다. 사이트에서 가장 인기 있는 그룹을 파악하는 것이 유용합니다. 이 변수는 &#39;사이트 섹션&#39; 차원을 채웁니다.

## Adobe Experience Platform Launch의 채널

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 채널을 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [ [!UICONTROL 동작]]에서 기존 Adobe Analytics - [!UICONTROL 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을 변수][!UICONTROL 설정으로]설정합니다.
6. 채널 [!UICONTROL 섹션을] 찾습니다.

채널을 모든 문자열 값 또는 데이터 요소로 설정할 수 있습니다.

## s.channel in AppMeasurement and Launch custom code editor

이 `s.channel` 변수는 일반적으로 페이지의 사이트 섹션이 포함된 문자열입니다. 최대 100바이트;긴 값이 잘립니다.

```js
s.channel = "Example site section";
```
