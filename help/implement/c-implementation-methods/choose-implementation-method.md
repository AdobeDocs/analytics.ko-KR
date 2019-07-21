---
description: Adobe Analytics를 구현하는 방법에는 여러 가지가 있습니다.
keywords: Analytics 구현; 구현 방법; 다이내믹 태그 관리; DTM; Javascript
seo-description: Adobe Analytics를 구현하는 방법에는 여러 가지가 있습니다.
seo-title: 구현 메서드 선택
solution: Analytics
title: 구현 메서드 선택
topic: 개발자 및 구현
uuid: 20 D 3317 F -7 C 63-4421-93 E 0-FFF 60 DBD 9 F 87
translation-type: tm+mt
source-git-commit: b1e69abd65f171b804e7f56031e594890bbd27bb

---


# 구현 메서드 선택

Adobe Analytics를 구현하는 방법에는 여러 가지가 있습니다.

* [!UICONTROL Adobe Experience Platform Launch] (권장)
* [!UICONTROL Dynamic Tag Management]
* JavaScript

## [!UICONTROL Adobe Experience Platform Launch]{#section_AEEA6AFE2C8D4182BC778F08EA171DC8}

[!UICONTROL Experience Platform Launch] 는 Adobe의 차세대 웹 사이트 태그 및 모바일 SDK 관리 기능입니다. [!UICONTROL 경험 플랫폼 Launch] 를 사용하면 관련 고객 경험을 강화하는 데 필요한 모든 분석, 마케팅 및 광고 통합을 배포 및 관리할 수 있습니다.

[!UICONTROL 경험 플랫폼 Launch] 를 사용하면 익스텐션이라는 자체 [!DNL Experience Platform Launch]통합을 구축하고 유지할 수 있습니다. These extensions are available to web and mobile [!UICONTROL Experience Platform Launch] customers in an app-store experience, so customers can quickly install, configure, and deploy their integrations.

For more information, see [Getting Started with Experience Platform Launch](https://docs.adobelaunch.com/getting-started).

## [!UICONTROL Dynamic Tag Management] {#section_22E3F3F928894A6A8D77E6953E6CA51C}

[!UICONTROL 다이내믹 태그 관리는] 구현에 필요한 많은 세부 작업을 자동화합니다 [!DNL Analytics]. Enter the required information in a form-based interface, and [!DNL Dynamic Tag Management] generates the code you need to add to your pages.
JavaScript에 익숙하고

* [eVar](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html) 정의 및 작동 방식
* 언제 [사용자 지정 이벤트](../../implement/analytics-terminology-basics/c-props-evars/event-custom.md#concept_CDA3C98C85B24A71B4B5C71F24BF918F) 사용 시기

다이내믹 태그 관리에 액세스하고 실행하는 방법에 대한 자세한 내용은 다이내믹 태그 관리 제품 설명서의 [시작](https://marketing.adobe.com/resources/help/en_US/dtm/get_started.html)을 참조하십시오.

자세한 내용은 [다이내믹 태그 관리를 사용하여 Analytics 구현](../../implement/c-implement-with-dtm/dtm-implementation-overview.md).

## JavaScript {#section_55429940D5094B9BB513E526F224D1B4}

JavaScript 구현 메서드를 사용하려면 페이지에서 JavaScript 코드를 수동으로 구성해야 합니다. Expereience 플랫폼 론치 또는 다이내믹 태그 관리 구현 방법을 사용하는 경우 이러한 노력의 상당 부분을 단순화할 수 있습니다. 그러나 일부 사용자는 JavaScript 메서드가 필요할 수 있습니다.

JavaScript를 구현하려면 다음이 필요합니다.

* 강력한 JavaScript 기술
* Analytics 개념과 용어에 대한 완전한 이해

자세한 내용은 [JavaScript를 사용하여 Analytics 구현을](../../implement/js-implementation/javascript-implementation-overview.md)참조하십시오.
