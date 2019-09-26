---
description: AppMeasurement.js에서 설정된 구성 변수.
keywords: Analytics 구현
seo-description: Adobe Analytics용 AppMeasurement.js에 설정된 구성 변수
seo-title: 구성 변수
solution: Analytics
subtopic: 변수
title: 구성 변수
topic: 개발자 및 구현
uuid: a19484b6-e350-4c12-b4d6-a31c79a42db0
translation-type: tm+mt
source-git-commit: 9212d70ab8fd7bc0ccfb7e781a92b1731f0a40bd

---


# 구성 변수 개요

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 일반적으로 기본 전역 JavaScript AppMeasurement.js에서 설정되는 가장 일반적인 구성 변수. 이러한 변수는 적절한 경우 Analytics 페이지 수준 코드 및 링크 내에서 설정할 수 있습니다.

Not all of these variables appear in the code by default when you generate code through the **[!UICONTROL Admin Tool]** &gt; **[!UICONTROL Code Manager]**. 이러한 구성 변수 중 일부는 사이트의 구현 요구에 적용할 수 없을 수도 있습니다.

이러한 구성 변수를 사용하는 몇 가지 목적은 다음과 같습니다.

* 여러 사이트/도메인 추적
* 구매 시 임의 통화 사용
* 다양한 언어로 데이터 캡처
* 링크 추적(다운로드한 파일의 수, 외부 사이트에 대한 링크)
* 고유한 목적으로 사용자 지정 링크 추적

>[!NOTE]
>
>[!DNL AppMeasurement] requires that all configuration variables are set before the initial call to the track function, `t()`. 구성 변수가 호출 후에 설정되면 `t()`예기치 않은 결과가 발생할 수 있습니다. To ensure proper data collection, all configuration variables must be above the `doPlugins` function.

특정 구성 변수에 대한 도움말을 보려면 다음 링크 중 하나를 클릭하십시오.

* [s.account](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Specify the report suite where data is stored and reported.

* [s.dynamicAccountSelection](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html): Dynamically select the report suite based on the URL of each page.

* [s.dynamicAccountList](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):대상 보고서 세트를 결정하는 데 사용되는 규칙을 지정합니다.

* [s.dynamicAccountMatch](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):DOM 개체를 사용하여 모든 규칙이 적용되는 URL의 섹션을 검색합니다.

* [s.dynamicVariablePrefix](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):동적으로 채워진 변수에 대한 플래그 지정을 배포합니다.

* [s.charSet](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):Analytics의 저장 및 보고를 위해 수신 데이터를 UTF-8로 변환합니다.

* [s.currencyCode](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):매출에 적용할 전환율을 결정합니다.

* [s.cookieDomain](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):쿠키가 설정되는 도메인을 `s_cc` `s_sq` 결정합니다.

* [s.cookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):페이지 URL의 도메인에서 점의 수를 지정하여 `s_cc` 및 `s_sq` 쿠키의 도메인을 결정합니다.

* [s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):기본적으로 퍼스트 파티 쿠키인 JavaScript(`s_sq`, `s_cc`플러그인)로 설정된 쿠키(타사 `2o7.net` 또는 `omtrdc.net` 도메인 포함)를 지정합니다.

* [s.cookieLifetime](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):JavaScript 및 데이터 수집 서버 모두에서 처리한 쿠키의 수명을 결정합니다.

* [s.doPlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):JavaScript 파일 내의 적절한 위치에서 함수를 호출하도록 허용합니다.

* [s.registerPreTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):콜백(함수)와 해당 함수에 대한 매개 변수 모두를 매개 변수로 가져오는 함수입니다.

* [s.registerPostTrackCallback](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):콜백(함수)와 해당 함수에 대한 매개 변수 모두를 매개 변수로 가져오는 함수입니다.

* [s.track 파섹](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):사이트에서 다운로드 가능한 파일에 대한 링크를 추적할 수 있습니다.

* [s.trackExternalLinks](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):클릭한 링크가 종료 링크인지 여부를 결정합니다.

* [s.trackInlineStats](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):ClickMap 데이터를 모으는지 확인합니다.

* [s.linkDownloadFileTypes](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):쉼표로 구분된 파일 확장자 목록을 포함합니다.

* [s.linkInternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):사이트에 속한 링크를 나타내는 쉼표로 구분된 필터 목록을 포함합니다.

* [s.linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):종료 링크 및 파일 다운로드 보고서에 쿼리 문자열을 포함해야 하는지 여부를 결정합니다.

* [s.linkTrackVars](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):사용자 지정, 종료 및 다운로드 링크로 전송되는 변수의 쉼표로 구분된 목록을 포함합니다.

* [s.linkExternalFilters](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):종료 링크의 특정 하위 세트에 대해 보고하는 데 사용합니다.

* [s.usePlugins](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html):각 이미지 요청 전에 함수를 `s_doPlugins` 호출합니다.

