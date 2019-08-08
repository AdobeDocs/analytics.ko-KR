---
description: Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.
keywords: Analytics 구현; Javascript; Javascript 구현; Appmeasurement; Appmeasurement 다운로드; Identity Service; Visitorapi. js; 캐싱; Appmeasurement 압축
seo-description: Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.
seo-title: JavaScript 구현 개요
solution: Analytics
title: JavaScript 구현 개요
topic: 개발자 및 구현
uuid: bb 661 d 8 c-faf 9-4454-ac 3 c -0 c 1 a 4 c 0 a 9336
translation-type: tm+mt
source-git-commit: 0a1db598a2b113ad71eb5d05d3f5c97f1af7cd62

---


# JavaScript 구현 개요

Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.

The easiest and recommended way to send data to [!DNL Analytics] is by using [Launch](/help/implement/implement-with-launch/create-analytics-property.md). 그러나 경우에 따라 이전 JavaScript 메서드를 사용하여 Analytics를 구현할 수 있습니다.

>[!NOTE]
>
>이 섹션에서는 Analytics를 구현하는 기존 방법을 설명합니다. All Analytics customers have access to [Launch](/help/implement/implement-with-launch/create-analytics-property.md), which is the standard method to deploy Experience Cloud tags.

## 구현 절차 {#section_73961BAD5BB4430A95E073DE5C026277}

데이터를 모으는 코드 페이지를 성공적으로 구현하기 위해서는, 새로운 컨텐츠를 웹 사이트에 업로드할 수 있도록 호스팅 서버에 대한 액세스 권한을 가지고 있어야 합니다. 코드를 구현할 기존 사이트가 있으면 유용합니다. 

다음은 기초 Analytics 구현 단계입니다.

| 작업 | 설명 |
|--- |--- |
| 1. JavaScript 용 appmeasurement 및 ID 서비스를 다운로드합니다. | Experience Cloud를 통해 Analytics에 로그인합니다. 다운로드 파일은 Analytics &gt; 관리 &gt; 코드 관리자에서 사용할 수 있습니다. 이 다운로드 ZIP에는 여러 파일이 포함되어 있습니다.  AppMeasurement.js 및 VisitorAPI.js는 Analytics를 구현할 때 관련된 파일입니다. |
| 2. ID 서비스를 설정합니다. (이전에 방문자 ID 서비스) | Analytics에 대한 ID 서비스 [설정을 참조하십시오.](https://docs.adobe.com/content/help/en/id-service/using/home.html) |
| 3. Update `AppMeasurement.js`. | Copy the [example AppMeasurement.js code](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_4351543F2D6049218E18B48769D471E2) and paste it at the beginning of your `AppMeasurement.js` file. 최소한 다음 변수를 업데이트하십시오.<ul><li>s.account="INSERT-RSID-HERE"</li><li>s.trackingServer="INSERT-TRACKING-SERVER-HERE"</li><li>s.visitorNamespace = "INSERT-NAMESPACE-HERE"</li><li>s.visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE")</li></ul><br>Trackingserver [및 trackingserversecure 변수](https://helpx.adobe.com/analytics/kb/determining-data-center.html) 올바로 채우기를 참조하거나 클라이언트 지원 센터에 문의하십시오. 이 변수들이 올바로 설정되지 않으면, 구현해도 데이터가 수집되지 않습니다.</br> |
| 4. 호스트 `AppMeasurement.js` 및 `VisitorAPI.js`. | 코어 JavaScript 파일은 사이트의 모든 페이지에서 액세스할 수 있는 웹 서버에 호스팅되어야 합니다. 다음 단계에서 이 파일에 대한 경로가 필요합니다. |
| 5. Reference `AppMeasurement.js` and `VisitorAPI.js`  on all site pages. | <ul><li>Include the Visitor ID Service by adding the following line of code in the `head` or `body` tag on each page. (`VisitorAPI.js` must be included before `AppMeasurement.js`).<br>`script language="JavaScript" type="text/javascript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/VisitorAPI.js"`</br></li><li>Include AppMeasurement for JavaScript by adding the following line of code in the `head` or `body` tag on each page:<br>`script language="JavaScript" type="text/javascript"  src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"`</br></li></ul> |
| 6. 페이지 코드를 업데이트 및 배포합니다. | [예제 페이지 코드를](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7) 복사하여 추적할 각 페이지의 열기 `body` 태그 바로 뒤에 붙여넣습니다. 최소한 다음 변수를 업데이트하십시오.<ul><li>var s=s_gi("INSERT-RSID-HERE")</li><li>s. pagename = "INSERT-NAME-HERE" (예: s. pagename = document. title)</li></ul> |
| 7. Experience Cloud 디버거를 사용하여 데이터가 전송되고 있는지 확인합니다. | [Experience Cloud 디버거를 설치합니다](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/debugger.html#concept_B26FFE005EDD4E0FACB3117AE3E95AA2). 설치가 끝나면 페이지 코드를 배포한 페이지를 불러온 다음 디버거를 엽니다. 디버거가 전송된 수집 데이터에 대한 정보를 표시합니다. |

## 캐시 {#section_4E2D1D962DF046418134C43CFC49AD4A}

JavaScript 파일은 처음에 로드된 후 방문자의 브라우저에 캐싱되며 일반적으로 세션당 한 번 이상 다운로드되지 않습니다. 이 파일은 사이트의 모든 페이지에서 사용되더라도 각 페이지에서 다운로드되지 않습니다. 대부분의 웹 사이트에서 사용자는 평균적으로 세션당 여러 번 페이지를 보기 때문에 여러 번 사용되는 JavaScript를 이 파일로 전송하면 다운로드되는 전체 데이터가 줄어들 수 있습니다.

## AppMeasurement 압축용 JavaScript {#section_C10BBC84C81C414088F97363D29E021B}

H 코드(JavaScript 1.0용 AppMeasurement는 사전에 압축되어 있음)의 페이지 무게(크기)가 걱정되는 경우에는, GZIP을 사용한 파일 압축을 고려해 보는 것이 좋습니다. GZIP은 모든 주요 브라우저에서 지원되며, JavaScript 압축보다 나은 성능을 제공하여 코어 [!DNL s_code.js] JavaScript 파일을 압축 및 압축 해제할 수 있도록 해줍니다.

다음 링크는 사이트에서 GZIP 기능을 사용하여 [!DNL s_code.js] JavaScript 코드의 압축을 처리할 수 있는 방법을 이해하는 데 도움이 됩니다.

[Apache 모듈 mod_deflate](https://httpd.apache.org/docs/2.0/mod/mod_deflate.html)

[Tomcat 및 Flex로 gzip 압축 활성화](https://www.cubicleman.com/2007/04/06/enabling-gzip-compression-with-tomcat-and-flex/)
