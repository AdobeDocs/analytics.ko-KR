---
title: 구성 변수
description: 구성 변수를 사용하여 데이터를 수집하는 방법을 결정합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 구성 변수 개요

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 이 변수는 일반적으로 차원 또는 지표 값을 포함하지 않습니다.

## 구성 변수 설정

`AppMeasurement.js`를 사용하는 JavaScript 구현에서 구성 변수는 일반적으로 JS 파일의 맨 위에 설정됩니다.

Adobe Experience Platform Launch를 사용하는 구현에서 구성 변수는 일반적으로 Adobe Analytics 확장을 구성하여 찾습니다.

1. Adobe ID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 편집할 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭을 클릭한 다음 Adobe Analytics 아래의 [!UICONTROL 구성]을 클릭합니다.

>[!IMPORTANT] 추적 메서드([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))를 호출하기 전에 모든 구성 변수가 설정되었는지 확인하십시오. [`doPlugins()`](../functions/doplugins.md) 함수에서 구성 변수를 설정하지 마십시오.
