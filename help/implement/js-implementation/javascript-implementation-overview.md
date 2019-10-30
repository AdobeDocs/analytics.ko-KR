---
description: Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.
keywords: Analytics 구현;javascript;javascript 구현;appmeasurement;appmeasurement 다운로드;ID 서비스;visitorapi.js;캐싱;appmeasurement 압축
seo-description: Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.
seo-title: JavaScript 구현 개요
solution: Analytics
title: JavaScript 구현 개요
topic: 개발자 및 구현
uuid: bb661d8c-faf9-4454-ac3c-0c1a4c0a9336
translation-type: ht
source-git-commit: 0a1db598a2b113ad71eb5d05d3f5c97f1af7cd62

---


# JavaScript 구현 개요

Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.

[!DNL Analytics]로 데이터를 보내는 가장 쉽고 권장되는 방법은 [Launch](/help/implement/implement-with-launch/create-analytics-property.md)를 사용하는 것입니다. 그러나 경우에 따라 이전 JavaScript 메서드를 사용하여 Analytics를 구현할 수 있습니다.

>[!NOTE]
>
>이 섹션에서는 Analytics를 구현하는 기존 방법을 설명합니다. 모든 Analytics 고객은 Experience Cloud 태그를 배포하는 표준 방법인 [Launch](/help/implement/implement-with-launch/create-analytics-property.md)에 액세스할 수 있습니다.

## 구현 절차 {#section_73961BAD5BB4430A95E073DE5C026277}

데이터를 모으는 코드 페이지를 성공적으로 구현하기 위해서는, 새로운 컨텐츠를 웹 사이트에 업로드할 수 있도록 호스팅 서버에 대한 액세스 권한을 가지고 있어야 합니다. 코드를 구현할 기존 사이트가 있으면 유용합니다. 

다음은 기초 Analytics 구현 단계입니다.

| 작업 | 설명 |
|--- |--- |
| 1. JavaScript용 AppMeasurement 및 ID 서비스를 다운로드합니다.  | Experience Cloud를 통해 Analytics에 로그인합니다. 다운로드 파일은 Analytics &gt; 관리자 &gt; 코드 관리자에서 사용할 수 있습니다. 이 다운로드 ZIP에는 여러 파일이 포함되어 있습니다.  AppMeasurement.js 및 VisitorAPI.js는 Analytics를 구현할 때 관련된 파일입니다. |
| 2. ID 서비스를 설정합니다. 이전 방문자 ID 서비스입니다. | [Analytics용 ID 서비스 설정](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)을 참조하십시오. |
| 3. `AppMeasurement.js`를 업데이트합니다. | [예제 AppMeasurement.js 코드](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_4351543F2D6049218E18B48769D471E2)를 복사하여 `AppMeasurement.js` 파일의 시작 위치에 붙여넣습니다. 최소한 다음 변수를 업데이트하십시오.<ul><li>s.account="INSERT-RSID-HERE"</li><li>s.trackingServer="INSERT-TRACKING-SERVER-HERE"</li><li>s.visitorNamespace = "INSERT-NAMESPACE-HERE"</li><li>s.visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE")</li></ul>이러한 변수에 대해 잘 모를 경우 <br>See [올바르게 trackingServer 및 trackingServerSecure 변수 채우기](https://helpx.adobe.com/kr/analytics/kb/determining-data-center.html)를 참조하거나 Client Care에 문의하십시오. 이 변수들이 올바로 설정되지 않으면, 구현해도 데이터가 수집되지 않습니다.</br> |
| 4. `AppMeasurement.js` 및 `VisitorAPI.js`를 호스팅합니다. | 코어 JavaScript 파일은 사이트의 모든 페이지에서 액세스할 수 있는 웹 서버에 호스팅되어야 합니다. 다음 단계에서 이 파일에 대한 경로가 필요합니다. |
| 5. 모든 사이트 페이지에서 `AppMeasurement.js` 및 `VisitorAPI.js`를 참조합니다. | <ul><li>각 페이지의 `head` 또는 `body` 태그에 다음 코드 행을 추가하여 방문자 ID 서비스를 포함합니다. `VisitorAPI.js`는 `AppMeasurement.js` 앞에 포함해야 합니다.<br>`script language="JavaScript" type="text/javascript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/VisitorAPI.js"`</br></li><li>다음 코드 행을 각 페이지의 `head` 또는 `body` 태그에 추가하여 JavaScript용 AppMeasurement를 포함합니다.<br>`script language="JavaScript" type="text/javascript"  src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"`</br></li></ul> |
| 6. 페이지 코드를 업데이트하고 배포합니다. | [예제 페이지 코드](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7)를 복사하여 추적할 각 페이지의 `body` 열기 태그 뒤에 붙여넣습니다. 최소한 다음 변수를 업데이트하십시오.<ul><li>var s=s_gi("INSERT-RSID-HERE")</li><li>s.pageName="INSERT-NAME-HERE"(예: s.pageName=document.title)</li></ul> |
| 7. Experience Cloud 디버거를 사용하여 데이터가 전송되고 있는지 확인합니다. | [Experience Cloud 디버거](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/testing-and-validation/debugger.html#concept_B26FFE005EDD4E0FACB3117AE3E95AA2)를 설치합니다. 설치가 끝나면 페이지 코드를 배포한 페이지를 불러온 다음 디버거를 엽니다. 디버거가 전송된 수집 데이터에 대한 정보를 표시합니다. |

## 캐시 {#section_4E2D1D962DF046418134C43CFC49AD4A}

JavaScript 파일은 처음에 로드된 후 방문자의 브라우저에 캐싱되며 일반적으로 세션당 한 번 이상 다운로드되지 않습니다. 이 파일은 사이트의 모든 페이지에서 사용되더라도 각 페이지에서 다운로드되지 않습니다. 대부분의 웹 사이트에서 사용자는 평균적으로 세션당 여러 번 페이지를 보기 때문에 여러 번 사용되는 JavaScript를 이 파일로 전송하면 다운로드되는 전체 데이터가 줄어들 수 있습니다.

## AppMeasurement 압축용 JavaScript {#section_C10BBC84C81C414088F97363D29E021B}

H 코드(JavaScript 1.0용 AppMeasurement는 사전에 압축되어 있음)의 페이지 무게(크기)가 걱정되는 경우에는, GZIP을 사용한 파일 압축을 고려해 보는 것이 좋습니다. GZIP은 모든 주요 브라우저에서 지원되며, JavaScript 압축보다 나은 성능을 제공하여 코어 [!DNL s_code.js] JavaScript 파일을 압축 및 압축 해제할 수 있도록 해줍니다.

다음 링크는 사이트에서 GZIP 기능을 사용하여 [!DNL s_code.js] JavaScript 코드의 압축을 처리할 수 있는 방법을 이해하는 데 도움이 됩니다.

[Apache 모듈 mod_deflate](https://httpd.apache.org/docs/2.0/mod/mod_deflate.html)

[Tomcat 및 Flex로 gzip 압축 활성화](https://www.cubicleman.com/2007/04/06/enabling-gzip-compression-with-tomcat-and-flex/)
