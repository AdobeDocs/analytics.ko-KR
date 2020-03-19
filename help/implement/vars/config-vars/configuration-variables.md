---
title: 구성 변수
description: 구성 변수를 사용하여 데이터를 수집하는 방법을 결정할 수 있습니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 구성 변수 개요

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 일반적으로 차원 또는 지표 값은 포함하지 않습니다.

## 구성 변수 설정

를 사용하여 JavaScript 구현에서 `AppMeasurement.js`구성 변수는 일반적으로 JS 파일의 맨 위에 설정됩니다.

Adobe Experience Platform Launch를 사용하는 구현에서 구성 변수는 일반적으로 Adobe Analytics 확장 기능을 구성하여 찾습니다.

1. Adobe ID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 편집할 속성을 클릭합니다.
3. Click the [!UICONTROL Extensions] tab, then Click [!UICONTROL Configure] under Adobe Analytics.

> [!IMPORTANT] 추적 메서드([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))를 호출하기 전에 모든 구성 변수가 설정되었는지 확인합니다. 함수에서 구성 변수를 설정하지 [`doPlugins()`](../functions/doplugins.md) 마십시오.
