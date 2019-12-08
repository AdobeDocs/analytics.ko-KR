---
description: 'null'
keywords: Analytics Implementation
title: Adobe 옵트아웃 구현
topic: Developer and implementation
uuid: fc3a411c-8476-409d-99de-05b34ace5019
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Adobe 옵트아웃 구현

웹 사이트 방문자의 일부는 Adobe Experience Cloud 제품 및 서비스에서 탐색 정보 집계 및 분석 또는 관련 컨텐츠 및 광고 제공을 위한 활용을 원치 않을 수 있습니다. Adobe는 웹 사이트 방문자가 다음 Adobe 제품에 의한 정보 수집을 옵트아웃할 수 있는 기능을 제공합니다.

* Adobe Analytics
* Adobe Target
* Adobe 크리에이티브 대상 타깃팅
* Adobe AudienceManager
* Adobe AdLens
* Adobe Experience Manager

## 개인정보 보호정책 권장 사항 {#section_BBDEE21C259842F7881642E31FB3D9B7}

Adobe는 Adobe 제품 또는 서비스에 의한 브라우징 정보 수집을 옵트아웃하는 기능에 관해 찾기 쉽고 읽기 쉬운 정보를 웹 사이트 방문자에게 제공할 것을 권장합니다.

방문자는 [Adobe 개인정보 보호 센터](https://www.adobe.com/privacy.html)에서 Adobe가 제품 및 서비스 제공과 관련하여 수집하는 정보를 보통 어떻게 활용하는지 자세히 알아볼 수 있습니다. 하지만 웹 사이트에서 서비스 구현 방식은 귀하가 전적으로 통제하며 웹 사이트 방문자에게 구체적인 제품 및 서비스 사용 방식을 설명하는 것도 귀하에게 달려 있습니다. 귀하는 자체 개인정보 보호정책 작성, 개인정보 보호정책 준수, Adobe와의 서비스 계약 준수, 모든 적용 가능한 법규 준수에 대한 책임을 집니다.

## Adobe Analytics(Reports &amp; Analytics, Data Warehouse, Ad Hoc Analysis 포함) 옵트아웃 {#section_8089B80CDA4043C9BC2DED49E484E8D7}

Adobe는 Adobe Analytics([!UICONTROL Reports &amp; Analytics], [!UICONTROL Data Warehouse], [!UICONTROL Ad Hoc Analysis] 포함)에 대한 3가지 옵트아웃 방식을 제공합니다.

* 자사 쿠키로 Adobe Analytics 제품을 구현하는 경우 웹 사이트 방문자에 대한 [사용자 지정된 고유한 옵트아웃 링크를 개발](/help/implement/js-implementation/data-collection/opt-out-link.md)해야 합니다.
* 고객은 브라우저의 쿠키 설정을 사용하여 옵트아웃을 활성화할 수 있습니다. [브라우저 쿠키에 대한 개인 정보 설정 활성화](https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/browser_cookie_settings.html)를 참조하십시오.

선택한 옵트아웃 메커니즘에 관계없이 Adobe는 옵트아웃 메커니즘의 가용성을 귀하의 개인정보 보호정책에 자세히 설명하거나 법에 의해 요구되는 방법 또는 최신 우수 사례에 따라 권장되는 방법으로 설명할 것을 권장합니다.
