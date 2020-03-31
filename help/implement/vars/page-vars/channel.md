---
title: channel
description: '''사이트 섹션'' 차원을 채웁니다.'
translation-type: ht
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# channel

`channel` 변수는 일반적으로 지정된 페이지가 있는 사이트의 섹션을 저장합니다. 이 변수는 사이트에서 가장 인기 있는 그룹을 파악하는 데 유용합니다. 이 변수는 &#39;사이트 섹션&#39; 차원을 채웁니다.

## Adobe Experience Platform Launch의 채널

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 채널을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 채널] 섹션을 찾습니다.

채널은 어떤 문자열 값 또는 데이터 요소로도 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.channel

`s.channel` 변수는 일반적으로 페이지의 사이트 섹션을 포함하는 문자열입니다. 이 변수의 값은 최대 100바이트이며 더 긴 값은 잘립니다.

```js
s.channel = "Example site section";
```
