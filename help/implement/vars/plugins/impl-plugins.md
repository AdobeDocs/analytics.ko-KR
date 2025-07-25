---
title: 플러그인 개요
description: 사이트에 코드를 붙여넣어 새로운 기능을 도입할 수 있습니다.
feature: Appmeasurement Implementation
exl-id: faae7963-078d-40ad-ba09-71efa0b90df1
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 96%

---

# 플러그인 개요

플러그인은 Analytics 구현에 도움이 되는 몇 가지 고급 기능을 수행하는 코드 조각입니다. 이러한 플러그인은 JavaScript의 기능을 확장함으로써 기본 구현으로는 사용할 수 없는 기능들을 브라우저에서 사용할 수 있도록 해 줍니다. Adobe에서는 고급 솔루션의 일부로서 다른 플러그인도 많이 제공하고 있습니다.

{{plug-in}}

Adobe에서는 특정 플러그인을 설치하는 몇 가지 방법을 제공합니다.

* Adobe Analytics 확장을 사용하여 &#39;일반적인 Analytics 플러그인&#39; 확장 사용
* 사용자 지정 코드 편집기를 사용하여 플러그인 코드 붙여넣기
* 플러그인 코드를 `AppMeasurement.js` 파일에 붙여넣기

각 조직에는 서로 다른 구현 요구 사항이 있으므로 구현에 이러한 요구 사항을 포함할 방법을 결정할 수 있습니다. 사이트에 코드를 포함할 때에는 다음 기준을 충족하는지 확인하십시오.

1. 먼저 Analytics 추적 개체 ([`s_gi`](../functions/s-gi.md) 사용)를 인스턴스화합니다.
   * 태그가 활성화된 사이트는 Adobe Analytics가 로드될 때 추적 개체를 자동으로 인스턴스화합니다.
   * `AppMeasurement.js`를 사용하는 구현은 일반적으로 JavaScript 파일의 맨 위에 있는 추적 개체를 초기화합니다.
2. 두 번째로 플러그인 코드를 포함합니다.
   * &#39;일반적인 Analytics 플러그인&#39; 확장에는 플러그인을 초기화할 수 있는 작업 구성이 있습니다.
   * 확장을 사용하지 않으려면 Analytics 확장을 구성할 때 사용자 지정 코드 편집기에 플러그인 코드를 붙여넣을 수 있습니다.
   * 구현이 Adobe Experience Platform의 태그를 사용하지 않는 경우에는 추적 개체를 인스턴스화 한 후 어디에서든 `AppMeasurement.js`에 플러그인 코드를 붙여넣을 수 있습니다.
3. 세 번째로 플러그인을 호출합니다.
   * 태그가 활성화된 사이트 내외의 모든 구현은 JavaScript를 사용하여 플러그인을 호출합니다. 해당 플러그인 페이지에 설명된 형식을 사용하여 플러그인을 호출하십시오.
4. 구현의 유효성을 검사하고 게시합니다.

많은 조직이 [`doPlugins`](../functions/doplugins.md) 기능을 사용하여 플러그인을 호출합니다. 이 기능이 필수는 아니지만 Adobe는 가장 좋은 사용 방법으로 간주하고 있습니다. AppMeasurement는 이미지 요청을 컴파일하고 전송하기 직전에 이 함수를 호출합니다. 몇 가지 플러그인은 다른 Analytics 변수에 따라 다르므로 이렇게 하는 것은 이상적입니다.
