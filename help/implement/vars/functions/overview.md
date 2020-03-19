---
title: 함수 및 메서드
description: 구현에서 Adobe가 제공하는 함수와 방법을 사용하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 함수 및 메서드

Adobe는 구현에 사용할 수 있는 몇 가지 함수와 방법을 제공합니다. 이러한 함수나 메서드를 참조할 때 이 함수는 단일 코드 행을 사용하여 일반적인 작업을 수행합니다.

이러한 단일 코드 줄 중 일부는 다음 범주에 속합니다.

* **추적 호출**:가장 일반적인 방법이며 많은 구현에서 매우 중요합니다. 여기에는 [`t()`](t-method.md) 및 [`tl()`](tl-method.md) 메서드가 포함됩니다.
* **AppMeasurement 유틸리티**:이전 버전의 AppMeasurement에서 구현은 이러한 작업을 수행하기 위해 자체 코드를 작성해야 했습니다. Adobe는 이러한 일반적인 작업을 간소화하기 위해 이러한 유틸리티 방법을 제공합니다. AppMeasurement 유틸리티에는 [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md)및 [`Util.getQueryParam()`](util-getqueryparam.md)가 포함됩니다.
* **함수 등록**:직접 함수를 작성하고 AppMeasurement가 Adobe에 추적 호출을 보내기 전이나 후에 자동으로 실행되도록 할 수 있습니다. 이 카테고리에 속하는 변수는 [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md)및 [`registerPostTrackCallback()`](registerposttrackcallback.md)입니다.
