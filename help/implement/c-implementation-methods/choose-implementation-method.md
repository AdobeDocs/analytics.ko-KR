---
description: Adobe Analytics를 구현하는 방법에는 여러 가지가 있습니다.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;javascript
solution: Analytics
title: 구현 방법 선택
topic: Developer and implementation
uuid: 20d3317f-7c63-4421-93e0-fff60dbd9f87
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 구현 방법 선택

Adobe Analytics를 구현하는 방법에는 여러 가지가 있습니다.

* [!UICONTROL Adobe Experience Platform Launch](권장)
* [!UICONTROL Dynamic Tag Management]
* JavaScript

## [!UICONTROL Adobe Experience Platform Launch] {#section_AEEA6AFE2C8D4182BC778F08EA171DC8}

[!UICONTROL Experience Platform Launch]는 Adobe의 차세대 웹 사이트 태그 및 모바일 SDK 관리 기능입니다. [!UICONTROL Experience Platform Launch]는 관련 고객 환경을 향상시키는 데 필요한 모든 분석, 마케팅 및 광고 통합 기능을 배포하고 관리하는 간단한 방법을 제공합니다.

[!UICONTROL Experience Platform Launch]는 확장이라고 하는 [!DNL Experience Platform Launch]와의 자체 통합을 구축하고 유지할 수 있는 권한을 누구에게나 부여합니다. 이러한 확장 기능은 앱 스토어 환경에서 웹 및 모바일 [!UICONTROL Experience Platform Launch] 고객이 사용할 수 있으므로, 고객은 통합 기능을 빠르게 설치, 구성 및 배포할 수 있습니다.

For more information, see [Getting Started with Experience Platform Launch](https://docs.adobelaunch.com/getting-started).

## [!UICONTROL Dynamic Tag Management] {#section_22E3F3F928894A6A8D77E6953E6CA51C}

[!UICONTROL Dynamic Tag Management]는 [!DNL Analytics]를 구현하는 데 필요한 세부 작업의 대부분을 자동화합니다. 양식 기반 인터페이스에 필수 정보를 입력하면 페이지에 추가해야 하는 코드를 [!DNL Dynamic Tag Management]에서 생성합니다.
JavaScript를 잘 알고 있고 다음과 같은 기본 Analytics 용어를 이해하고 있으면 도움이 됩니다.

* [eVar](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html) 정의 및 작동 방식
* [사용자 지정 이벤트](/help/implement/analytics-terminology-basics/c-props-evars/event-custom.md)를 사용해야 하는 경우

다이내믹 태그 관리에 액세스하고 실행하는 방법에 대한 자세한 내용은 다이내믹 태그 관리 제품 설명서의 [시작](https://marketing.adobe.com/resources/help/en_US/dtm/get_started.html)을 참조하십시오.

자세한 내용은 [Dynamic Tag Management를 사용하여 Analytics 구현](/help/implement/c-implement-with-dtm/dtm-implementation-overview.md)을 참조하십시오.

## JavaScript {#section_55429940D5094B9BB513E526F224D1B4}

JavaScript 구현 메서드를 사용하려면 페이지에서 JavaScript 코드를 수동으로 구성해야 합니다. Expereience Platform Launch 또는 Dynamic Tag Management 구현 메서드를 사용하는 경우 이러한 작업의 많은 부분을 단순화할 수 있습니다. 그러나 일부 사용자는 JavaScript 메서드가 필요할 수 있습니다.

JavaScript를 구현하려면 다음이 필요합니다.

* 강력한 JavaScript 기술
* Analytics 개념과 용어에 대한 완전한 이해

자세한 내용은 [JavaScript를 사용하여 Analytics 구현](/help/implement/js-implementation/javascript-implementation-overview.md)을 참조하십시오.
