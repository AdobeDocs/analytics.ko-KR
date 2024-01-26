---
title: 변수, 함수, 메서드 및 플러그인 개요
description: 보고를 개선하기 위해 Adobe에 보내는 데이터에 포함할 수 있는 변수를 알아봅니다.
keywords: appmeasurement, 변수, vars, 구성, 페이지, 구현
feature: Variables
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 69%

---

# 변수, 함수, 메서드 및 플러그인 개요

Analytics는 분석 데이터 수집을 위한 다양한 변수를 제공합니다. 이 섹션의 변수는 몇 가지 섹션으로 분류됩니다.

* **페이지 변수**&#x200B;는 일반적으로 보고에서 바로 사용되는 값입니다. 일반적인 페이지 변수에는 `props`, `eVars` 및 `events`가 포함됩니다.
* **구성 변수**&#x200B;는 올바른 데이터가 Adobe에 도달하는지 확인하는 데 도움이 되는 설정 값입니다. 일반적인 구성 변수에는 `trackingServerSecure`, `charSet` 및 `linkTrackVars`가 포함됩니다. 구성 변수는 일반적으로 차원 항목을 채우지 않습니다.
* **함수 및 메서드**&#x200B;는 참조 시 특정 작업을 수행하는 코드 조각입니다. 일반적인 함수에는 `t()`, `tl()` 및 `clearVars()`가 포함됩니다.

## 변수 및 구현 방법

Adobe에서는 Adobe Analytics를 구현하는 방법을 여러 가지 제공합니다. 각 페이지에는 Web SDK, Adobe Analytics 확장 기능 및 JavaScript용 AppMeasurement을 사용하여 변수를 구현하는 방법에 대한 섹션이 있습니다.

다음은 Adobe Analytics에서의 변수 구성에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/28755/?quality=12)

## 작업 순서

Adobe Analytics가 게시한 AppMeasurement 라이브러리는 데이터를 Adobe에 전송할 때 특정 순서를 따릅니다. 이러한 작업을 순서대로 실행하지 않을 경우 데이터가 불완전할 수 있습니다.

1. 사이트에서 데이터 계층을 사용하는 경우 적용 가능한 모든 변수가 채워졌는지 우선 확인합니다. 예를 들어 `adobeDataLayer.page.title` (페이지 제목 포함) 자세한 내용은 [데이터 계층](../prepare/data-layer.md)을 참조하십시오.
2. 데이터 계층을 사용하여 Analytics 변수를 채웁니다. <br/>Adobe Experience Platform에서 태그를 사용하는 경우 이 작업은 그 사이에 있는 데이터 요소를 사용하여 수행됩니다. 데이터 요소는 데이터 계층의 값으로 채워집니다. 예: 데이터 요소 `Page Title` 데이터 계층 변수에서 값을 가져옵니다. `adobeDataLayer.page.title`. <br/>그런 다음 데이터 요소를 사용하여 Analytics 변수를 채울 수 있습니다. 예 `eVar4` 데이터 요소에서 값을 가져옵니다. `Page Title`. <br/>자세한 내용은 을 참조하십시오 [데이터 요소](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=ko-KR), [데이터 레이어 개체를 데이터 요소에 매핑](../launch/layer-to-elements.md), 및 [태그 데이터 요소를 Analytics 변수에 매핑](../launch/elements-to-variable.md)
3. 마지막으로 추적 함수를 호출합니다. 대부분의 AppMeasurement 라이브러리는 `t()` 메서드를 사용하지만 일부 모바일 SDK는 `track()`을 사용합니다. 추적 함수가 호출되면 Analytics 개체에 정의된 모든 지원되는 변수가 이미지 요청 형태로 Adobe에 전송됩니다.

## 잘못된 문자

JavaScript 변수에는 다음 문자와 문자열을 사용할 수 없습니다.

* 탭 (`0x09`)
* 캐리지 리턴 (`0x0D`)
* 줄바꿈 (`0x0A`)
* HTML 태그 (예:`<b></b>` 또는 `&#153`)

일부 변수에는 추가적인 제한 사항이나 구문 요구 사항이 있습니다. 예를 들어 [`products`](page-vars/products.md) 변수는 세미콜론과 쉼표를 사용하여 제품과 범주를 구분합니다.
