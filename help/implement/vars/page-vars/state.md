---
title: 주/도
description: 보고 및 분석에서 '방문자 주 보고서'를 채웁니다.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# state

> [!IMPORTANT] 이 변수는 삭제되었으며 분석 작업 공간에서 사용할 수 있는 차원이 아닙니다. AppMeasurement가 방문자의 위치를 기반으로 자동으로 수집하는 &#39;미국 주&#39; 차원을 대신 사용하십시오.

이전 버전의 Adobe Analytics에서는 방문자가 소매 사이트에서 배송 정보를 입력할 때 `state` 변수가 사용되었습니다. 기능적으로 prop과 동일하지만 분석 작업 공간에서 사용할 수 없습니다.

## Adobe Experience Platform Launch의 상태

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 상태를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [ [!UICONTROL 동작]]에서 기존 Adobe Analytics - [!UICONTROL 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을 변수][!UICONTROL 설정으로]설정합니다.
6. 상태 [!UICONTROL 섹션을] 찾습니다.

상태를 임의의 문자열 값 또는 데이터 요소로 설정할 수 있습니다.

## s.state in AppMeasurement and Launch custom code editor

이 `s.state` 변수는 일반적으로 방문자의 시/도를 포함하는 문자열입니다. 전체 상태 이름이나 두 문자 코드는 모두 유효합니다. 최대 값은 50바이트입니다.긴 값이 잘립니다. 기본값은 빈 문자열입니다.

```js
s.state = "Utah";
```
