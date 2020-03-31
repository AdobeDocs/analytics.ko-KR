---
title: server
description: '''서버'' 차원을 채웁니다.'
translation-type: ht
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# server

`server` 변수는 일반적으로 사이트의 호스트 이름을 저장합니다. 이 변수는 일반적으로 여러 도메인의 데이터를 포함하는 보고서 세트에서 사용됩니다. 기능적으로는 prop과 동일합니다.

## Adobe Experience Platform Launch의 서버

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 서버를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 서버] 섹션을 찾습니다.

서버는 어떤 문자열 값 또는 데이터 요소로도 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.server

`s.server` 변수는 일반적으로 사이트의 호스트 이름을 포함하는 문자열입니다. 이 변수의 값은 최대 100바이트이며 더 긴 값은 잘립니다.

```js
// Set the server variable to a static string
s.server = "Example server";

// Automatically set the server variable to the site's hostname
s.server = window.location.hostname;
```
