---
description: 변수 및 변수의 제한 사항에 대한 개요.
keywords: Analytics 구현; 변수; 제한 사항; limits
seo-description: 변수 및 변수의 제한 사항에 대한 개요.
seo-title: 변수 및 제한 사항
solution: Analytics
subtopic: 변수
title: 변수 및 제한 사항
topic: 개발자 및 구현
uuid: 028677 A 7-2132-4 EE 7-9 CC 1-697 C 2 C 09 B 087
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 변수 및 제한 사항

변수 및 변수의 제한 사항에 대한 개요.

>[!NOTE]
>
>See [Configuration Variables](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_8FCA630706334F54B4DCB607378BCD00) and [Page Variables](../../../implement/js-implementation/c-variables/page-variables.md#concept_37933DFF2FC547A0A3B296D5E646B6A3) for an in-depth look at the most common Analytics variables.

다음 표에는 [!DNL Analytics] 변수에 대한 요약 정보가 나와 있습니다. 

| 변수 | 설명 |
|---|---|
| s_account  | 데이터를 저장 및 보고하는 보고서 세트를 결정합니다. |
| browserHeight | 브라우저 창의 높이를 표시합니다. |
| browserWidth | 브라우저 창의 너비를 표시합니다. |
| campaign | 사이트로 방문자를 유도하는 데 사용된 마케팅 캠페인을 식별합니다. 변수 *`campaign`* 의 값은 대개 쿼리 문자열 매개 변수에서 가져옵니다. |
| channel | 보통 웹 사이트의 섹션을 식별합니다. 예를 들어 매장 주인에게는 전자 제품, 장난감 또는 의류 등의 섹션이 있을 수 있습니다. 미디어 사이트에는 뉴스, 스포츠 또는 비즈니스 등의 섹션이 포함될 수 있습니다. |
| charSet | 웹 페이지의 문자 집합을 UTF-8로 변환합니다. |
| colorDepth | 화면의 각 픽셀에 색상을 표시하는 데 사용된 비트 수를 표시합니다. |
| connectionType | (Microsoft Internet Explorer에서)브라우저가 LAN 또는 모뎀 연결에 대해 구성되어 있는지 여부를 나타냅니다. |
| cookieDomainPeriods | 페이지 URL 중 도메인에서 점의 수를 판단하여 [!DNL Analytics] [!UICONTROL 방문자 ID] (s_vi) 쿠키가 설정되는 도메인을 결정합니다. For `www.mysite.com`, *`cookieDomainPeriods`* should be "2." For `www.mysite.co.jp`, *`cookieDomainPeriods`* should be "3." |
| cookieLifetime | 쿠키의 수명을 결정할 때 JavaScript와 [!DNL Analytics] 서버 모두에서 사용됩니다. |
| cookiesEnabled | 자사 세션 쿠키를 JavaScript가 설정할 수 있는지 여부를 가리킵니다. |
| currencyCode | 매출이 [!DNL Analytics] 데이터베이스에 들어갈 때 매출에 적용할 전환율을 결정합니다. [!DNL Analytics] 데이터베이스는 모든 금액을 선택한 통화로 저장합니다. If that currency is the same as that specified in *`currencyCode`*, or *`currencyCode`* is empty, no conversion is applied. |
| dc | 데이터를 전송 받을 데이터 센터를 설정할 수 있게 해줍니다. |
| doPlugins | *`doPlugins`**`s_doPlugins`* 함수에 대한 참조입니다. It allows the *`s_doPlugins`* function to be called at the appropriate location within the JavaScript file. |
| dynamicAccountList | 데이터를 전송 받을 보고서 세트를 동적으로 선택합니다. the *`dynamicAccountList`* 변수에는 대상 보고서 세트를 결정하는 데 사용할 규칙이 포함됩니다. |
| dynamicAccountMatch | DOM 개체를 사용하여 *`dynamicAccountList`* 의 모든 규칙이 적용되는 URL 섹션을 검색합니다. This variable is only valid when *`dynamicAccountSelection`* is set to 'True.' |
| dynamicAccountSelection | 각 페이지의 URL을 기반으로 보고서 세트를 동적으로 선택할 수 있도록 해줍니다. |
| dynamicVariablePrefix | 동적으로 채워야 하는 변수에 배포 시 플래그가 지정될 수 있도록 해줍니다. 쿠키, 요청 헤더 및 이미지 쿼리 문자열 매개 변수는 동적으로 채울 수 있습니다. |
| eVarN | [!DNL Analytics] [!UICONTROL 전환 모듈] 내에서 사용자 지정 보고서를 작성하는 데 사용됩니다. eVar를 방문자에 대한 값으로 설정하면 [!DNL Analytics]는 값이 만료되기 전까지 해당 값을 기억합니다. eVar 값이 활성일 때 방문자가 발견하는 성공 이벤트는 eVar 값으로 카운트됩니다. |
| events | 일반적인 장바구니 성공 이벤트와 사용자 지정 성공 이벤트를 기록합니다. |
| fpCookieDomainPeriods | 페이지의 도메인에서 점의 수를 판단하여 [!DNL Analytics]방문자 ID[!UICONTROL (s_vi) 쿠키가 아닌 ] 쿠키가 설정되는 도메인을 결정합니다. |
| hierN | 사이트의 계층에서 페이지 위치를 결정합니다. 이 변수는 사이트 구조의 수준이 4 이상인 사이트에 가장 유용합니다. |
| homepage | (Internet Explorer에서)현재 페이지가 사용자의 홈 페이지로 설정되어 있는지 여부를 가리킵니다. |
| javaEnabled | 브라우저에서 Java가 활성화되어 있는지 여부를 가리킵니다. |
| javascriptVersion | 브라우저가 지원하는 JavaScript의 버전을 표시합니다. |
| linkDownloadFileTypes | 쉼표로 구분된 파일 확장자 목록입니다. 사이트에 이러한 확장자를 가진 파일에 대한 링크가 포함된 경우 해당 링크의 URL이 [!UICONTROL 파일 다운로드] 보고서에 나타납니다. |
| linkExternalFilters | 사이트에 외부 사이트에 대한 링크가 많이 포함되어 있고 일부 종료 링크만 추적하려는 경우, *`linkExternalFilters`* 를 사용하여 일부 특정 종료 링크들에 대해 보고할 수 있습니다. |
| linkInternalFilters | 사이트에서 어느 링크가 종료 링크인지를 결정합니다. 사이트에 속한 링크를 나타내는 필터들이 쉼표로 구분되어 있는 목록입니다. |
| linkLeaveQueryString | [!UICONTROL 종료 링크] 및 [!UICONTROL 파일 다운로드] 보고서에 쿼리 문자열을 포함해야 하는지 여부를 결정합니다. |
| linkName | 사용자 지정, 다운로드 또는 종료 링크의 이름을 결정하는 [!UICONTROL 링크 추적]에 사용되는 선택 변수입니다. the *`linkName`* 변수는 *`tl()`* 함수의 세 번째 매개 변수로 교체되기 때문에 보통은 필요가 없습니다. |
| linkTrackEvents | 사용자 지정, 다운로드 및 종료 링크로 전송해야 하는 이벤트가 들어 있습니다. 이 변수는 *`linkTrackVars`*&#x200B;에 "events"가 들어 있을 경우에만 고려됩니다. |
| linkTrackVars | 사용자 지정, 종료 또는 다운로드 링크로 전송할 변수들이 쉼표로 구분되어 표시된 목록입니다. if *`linkTrackVars`*&#x200B;가 ""로 설정되어 있으면 값이 있는 모든 변수가 링크 데이터와 함께 전송됩니다.  |
| linkType | 링크 이름 또는 URL이 나타날 보고서(사용자 지정, 다운로드 또는 종료 링크)를 결정하는 링크 추적에 사용되는 선택 변수입니다. *`linkType`* 함수의 두 번째 매개 변수가 교체되기 때문에 보통은 *`tl()`* 필요가 없습니다. |
| mediaLength | 재생되는 미디어의 전체 길이를 지정합니다. |
| mediaName | 비디오나 미디어 항목의 이름을 지정합니다. [!UICONTROL 데이터 삽입 API] 및 [!UICONTROL 데이터 소스 완전 처리]를 통해서만 사용할 수 있습니다. |
| mediaPlayer | 비디오나 미디어 항목을 사용하는 데 사용되는 플레이어를 지정합니다. |
| mediaSession | 사용되는 비디오나 미디어 자산의 세그먼트를 지정합니다. |
| Media.trackEvents | 미디어 히트와 함께 전송해야 하는 이벤트를 식별합니다. 이 변수는 JavaScript [!UICONTROL ActionSource]에서만 사용할 수 있습니다. |
| Media.trackVars | 미디어 히트와 함께 전송해야 하는 변수를 식별합니다. 이 변수는 JavaScript [!UICONTROL ActionSource]에서만 사용할 수 있습니다. |
| mobile | 쿠키와 구독자 ID가 방문을 식별하는 데 사용되는 순서를 제어합니다. |
| s_objectID | 링크의 [!UICONTROL onClick] 이벤트에 설정되는 글로벌 변수. 페이지의 링크 또는 링크 위치에 대한 고유 개체 ID를 작성함으로써 방문자 클릭 맵 추적을 개선하거나 방문자 클릭 맵을 사용하여, 링크 URL보다는 링크 유형 또는 위치에 대해 보고할 수 있습니다. |
| pageName | 사이트에 있는 각 페이지의 이름이 들어 있습니다. if *`pageName`*&#x200B;이 비어 있으면, [!DNL Analytics]에서 페이지 이름을 나타내는 데 URL이 사용됩니다. |
| pageType | 404 [페이지가 없습니다] 오류 페이지를 지정하는 데에만 사용됩니다. 여기에는 "errorPage", 이 하나의 값만 가능합니다. 404 오류 페이지에서는 *`pageName`*&#x200B;변수를 채우지 말아야 합니다.  |
| pageUrl | 페이지의 URL이 [!DNL Analytics]에 보고할 URL과 다른 경우가 드물게 나타납니다. To accommodate these situations, [!DNL Analytics] offers the *`pageURL`* variable, which overrides the actual URL of the page. |
| plugins | Netscape 및 Mozilla 기반 브라우저에서 브라우저에 설치된 플러그인을 나열합니다. |
| products | 구매 수량 및 구매 가격뿐만 아니라 제품 및 제품 카테고리를 추적하는 데에도 사용됩니다. the *`products`* 변수는 항상 성공 이벤트와 함께 설정해야 합니다. Optionally, the *`products`* variable can track custom numeric and currency events, as well as [!UICONTROL Merchandising] eVars. |
| propN | [!DNL Analytics] [!UICONTROL 트래픽 모듈] 내에서 사용자 지정 보고서를 작성하는 데 사용됩니다. [!UICONTROL props]는 경로 지정 보고서용으로 또는 상관 관계 보고서에서 카운터(페이지 보기가 전송되는 횟수 계산)로 사용할 수 있습니다. |
| purchaseID | [!DNL Analytics]에서 한 주문이 여러 번 카운트되지 않도록 하는 데 사용됩니다. Whenever the purchase event is used on your site, you should use the *`purchaseID`* variable. |
| referrer | 유실된 레퍼러 정보를 복원합니다. |
| resolution | 웹 페이지를 보는 방문자의 모니터 해상도를 표시합니다. |
| server | 웹 페이지의 도메인(방문자가 도착한 도메인 표시)이나, 페이지를 제공하는 서버(로드 밸런싱 빠른 참조용)를 보여 줍니다. |
| state | 사이트 방문자가 거주하는 시/도를 캡처합니다. |
| trackDownloadLinks | 사이트의 다운로드 가능 파일에 대한 링크를 추적하려면 *`trackDownloadLinks`* 를'true'로 설정합니다. If *`trackDownloadLinks`* is 'true,' *`linkDownloadFileTypes`* determines which links are downloadable files. |
| trackExternalLinks | If *`trackExternalLinks`* is 'true,' *`linkInternalFilters`* and *`linkExternalFilters`* determines whether any link clicked is an exit link. |
| trackingServer | 자사 쿠키 구현에서 이미지 요청 및 쿠키를 쓰는 도메인을 지정하는 경우에만 사용됩니다. 비보안 페이지에 사용됩니다.  |
| trackingServerSecure | 자사 쿠키 구현에서 이미지 요청 및 쿠키를 쓰는 도메인을 지정하는 경우에만 사용됩니다. 보안 페이지에 사용됩니다.  |
| trackInlineStats | 방문자 클릭 맵 데이터를 모으는지 여부를 결정합니다. |
| transactionID | 오프라인 데이터를 온라인 거래(예: 온라인으로 생성된 리드나 구매)에 연결합니다. Adobe에 전송된 각 고유 *`transactionID`*&#x200B;는 해당 거래에 대한 오프라인 정보의 [!UICONTROL 데이터 소스] 업로드를 준비하면서 기록됩니다. [데이터 소스 안내서](https://marketing.adobe.com/resources/help/en_US/sc/datasources/) 를 참조하십시오. |
| s_usePlugins | 만약 *`s_doPlugins`* 함수를 사용할 수 있고 유용한 코드가 들어 있으면 [!UICONTROL s_ useplugins] 를'true'로 설정해야 합니다. [!UICONTROL Useplugins] 가'true'이면 이 함수는 *`s_doPlugins`* 각 이미지 요청에 앞서 호출됩니다. |
| visitorID | Visitors may be identified by the *`visitorID`* tag, or by IP address/User Agent. The *`visitorID`* may be up to 100 alphanumeric characters and must not contain a hyphen. |
| visitorNamespace | If *`visitorNamespace`* is used in your JavaScript file, do not delete or alter it. 이 변수는 쿠키가 설정된 도메인을 식별하는 데 사용됩니다. if *`visitorNamespace`* 가 변경되면 [!DNL Analytics]에 보고된 모든 방문자가 새 방문자가 되는 수가 있습니다. 요컨대, Adobe 컨설턴트의 승인 없이 이 변수를 바꾸지 마십시오. |
| zip | 사이트 방문자가 거주하는 곳의 우편번호를 캡처합니다. |

