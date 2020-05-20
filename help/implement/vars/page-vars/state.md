---
title: 주/도
description: Reports and Analytics에서 '방문자 주 보고서'를 채웁니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# state

>[!IMPORTANT] 이 변수는 사용이 중단되었으며 Analysis Workspace에서 사용할 수 있는 차원이 아닙니다. AppMeasurement가 방문자의 위치를 기반으로 자동으로 수집하는 &#39;미국 주&#39; 차원을 대신 사용하십시오.

이전 버전의 Adobe Analytics에서는 방문자가 소매 사이트에서 배송 정보를 입력할 때 `state` 변수가 사용되었습니다. 이 변수는 기능적으로 prop과 동일하지만 Analysis Workspace에서 사용할 수는 없습니다.

## Adobe Experience Platform Launch의 주

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 주를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 주] 섹션을 찾습니다.

주는 어떤 문자열 값 또는 데이터 요소로도 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.state

`s.state` 변수는 일반적으로 방문자의 주 또는 시/도를 포함하는 문자열입니다. 전체 주 이름이나 2자 코드 모두 유효합니다. 이 변수의 값은 최대 50바이트이며 더 긴 값은 잘립니다. 기본값은 빈 문자열입니다.

```js
s.state = "Utah";
```
