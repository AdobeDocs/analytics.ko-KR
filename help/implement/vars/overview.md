---
title: 변수, 함수, 메서드 및 플러그인 개요
description: Adobe로 전송한 데이터에 포함할 수 있는 변수를 파악하여 보고를 향상시킬 수 있습니다.
keywords: appmeasurement,variables,vars,configuration,page,implementation
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 변수, 함수, 메서드 및 플러그인 개요

Analytics는 분석 데이터 수집을 위한 다양한 변수를 제공합니다. 이 섹션의 변수는 여러 섹션으로 분할됩니다.

* **페이지 변수는** 일반적으로 보고에 직접 사용되는 값입니다. 일반적인 페이지 변수에는 `props`, `eVars`및 `events`가 포함됩니다.
* **구성 변수는** 올바른 데이터가 Adobe에 도달하는지 확인하는 데 도움이 되는 설정 값입니다. 일반적인 구성 변수에는 `trackingServerSecure`, `charSet`및 `linkTrackVars`가 포함됩니다. 구성 변수는 일반적으로 차원 값을 채우지 않습니다.
* **함수 및 메서드는** 참조할 때 특정 작업을 수행하는 코드 조각입니다. 일반적인 함수에는 `t()`, `tl()`및 `clearVars()`가 포함됩니다.

## 변수 및 구현 방법

Adobe는 Adobe Analytics를 구현하는 다양한 방법을 제공합니다. 각 페이지는 Launch 및 AppMeasurement for JavaScript를 사용하여 변수를 구현하는 방법에 대한 섹션을 제공합니다.

## 작업 순서

Adobe Analytics에서 게시한 AppMeasurement 라이브러리는 Adobe로 데이터를 전송할 때 특정 순서에 따릅니다. 이러한 작업을 순서대로 실행할 경우 데이터가 불완전할 수 있습니다.

1. 사이트에서 데이터 레이어를 사용하는 경우 적용 가능한 모든 변수가 먼저 채워졌는지 확인합니다. See [Data layer](../prepare/data-layer.md) for more information.
2. 데이터 레이어를 사용하여 Analytics 변수를 채웁니다. 론치를 사용하는 경우 데이터 요소를 사용한 다음 변수에 데이터 요소를 할당하여 이 작업을 쉽게 수행할 수 있습니다. See [Data elements](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html) in the Launch user guide.
3. 추적 함수를 호출합니다. 대부분의 AppMeasurement 라이브러리는 이 `t()` 메서드를 사용하지만 일부 모바일 SDK는 `track()`사용합니다. 추적 함수가 호출되면 Analytics 개체에 정의된 모든 지원 변수가 이미지 요청 형식으로 Adobe로 전송됩니다.

## 잘못된 문자

JavaScript 변수에는 다음 문자와 문자열을 사용할 수 없습니다.

* 탭 (`0x09`)
* 캐리지 리턴(`0x0D`)
* 줄바꿈 (`0x0A`)
* HTML 태그(예:`<b></b>` 또는 `&#153`)

일부 변수에는 추가 제한 사항이나 구문 요구 사항이 있습니다. 예를 들어 `products` 변수는 세미콜론과 쉼표를 사용하여 제품과 카테고리를 구분합니다.
