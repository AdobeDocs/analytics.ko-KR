---
description: 리디렉션은 사용자 상호 작용 없이 브라우저를 새 위치로 지정합니다. 리디렉션은 웹 브라우저(클라이언트 측 리디렉션) 또는 웹 서버(서버측 리디렉션)에서 실행됩니다.
keywords: Analytics 구현
seo-description: 리디렉션은 사용자 상호 작용 없이 브라우저를 새 위치로 지정합니다. 리디렉션은 웹 브라우저(클라이언트 측 리디렉션) 또는 웹 서버(서버측 리디렉션)에서 실행됩니다.
seo-title: 리디렉션 및 별칭
solution: Analytics
subtopic: 리디렉션
title: 리디렉션 및 별칭
topic: 개발자 및 구현
uuid: 11f9ad7a-5c45-410f-86dd-b7d2cec2aae3
translation-type: ht
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 리디렉션 및 별칭

리디렉션은 사용자 상호 작용 없이 브라우저를 새 위치로 지정합니다. 리디렉션은 웹 브라우저(클라이언트 측 리디렉션) 또는 웹 서버(서버측 리디렉션)에서 실행됩니다.

## 리디렉션 및 별칭 {#concept_F4F1D53D473947FE8554897332545763}

리디렉션은 사용자 상호 작용 없이 브라우저를 새 위치로 지정합니다. 리디렉션은 웹 브라우저(클라이언트 측 리디렉션) 또는 웹 서버(서버측 리디렉션)에서 실행됩니다.

리디렉션은 사용자 조정이 필요 없으므로, 종종 사용자도 모르게 리디렉션이 실행됩니다. 리디렉션이 발생했음을 나타내는 유일한 단서는 브라우저의 주소 표시줄입니다. 주소 표시줄이 브라우저가 초기에 요청한 링크와 다른 URL을 표시합니다.

두 가지 유형의 리디렉션만 있더라도, 다양한 방법으로 리디렉션을 구현할 수 있습니다. 예를 들어 사용자가 자신의 브라우저를 향해 있는 웹 페이지에는 브라우저를 다른 URL로 리디렉션하는 스크립팅 또는 특수 HTML 코드가 들어 있으므로 클라이언트 측 리디렉션이 발생할 수 있습니다. 서버측 리디렉션은 페이지가 서버측 스크립팅을 포함하거나 사용자가 다른 URL로 향하도록 웹 서버가 구성되었기 때문에 발생할 수 있습니다.

## Analytics 및 리디렉션 {#concept_F9132879D0CB4AC1BE7AF45E388A47F7}

[!DNL Analytics]는 브라우저에서 일부 데이터를 수집하고 특정 브라우저 속성에 의존합니다. 이러한 속성 중 "참조 URL"(또는 "레퍼러")과 "현재 URL" 속성은 서버측 리디렉션으로 변경될 수 있습니다. 브라우저는, 한 URL이 요청되었지만 다른 URL이 반환되었음을 인식하므로, 참조 URL을 지웁니다. 그 결과, 참조 URL은 공백이 되고, [!DNL Analytics]가 페이지에 대한 레퍼러가 없음을 보고할 수 있습니다.

<!-- 

redirects_sc.xml

 -->

다음 예는 리디렉션의 유무에 따라 찾아보기가 어떻게 영향을 받는지를 나타냅니다.

* [예: 리디렉션 없이 찾아보기](../../implement/js-implementation/redirects-overview.md#section_5C835A4D665A4625A23333C2C21F152D)
* [예: 리디렉션을 사용하여 찾아보기](../../implement/js-implementation/redirects-overview.md#section_921DDD32932847848C4A901ACEF06248)

## 예: 리디렉션 없이 찾아보기 {#section_5C835A4D665A4625A23333C2C21F152D}

사용자가 리디렉션을 발견하지 않는 다음 가설 시나리오를 고려하십시오.

1. 사용자가 자신의 브라우저를 `www.google.com`**을 가리키게 하고, 검색 필드에 "할인 항공 티켓"을 입력한 다음[!UICONTROL 검색]단추를 클릭합니다.**
1. 브라우저가 해당 사이트([!DNL https://www.flywithus.com/])/)에 대한 링크를 포함하는 검색 결과를 표시합니다. 검색 결과가 표시되고 브라우저의 주소 표시줄에 사용자가 검색 필드(`https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`)에 입력한 검색어가 표시됩니다. 검색어는 `https://www.google.com/search?` 다음에 오는 URL 쿼리 문자열 매개 변수에 포함됩니다.
1. 사용자가 가설 사이트([!DNL https://www.flywithus.com/])/)로 이동하는 링크를 클릭합니다. 사용자가 이 링크를 클릭하고 [!DNL flywithus.com] 웹 사이트로 이동하면 [!DNL Analytics]는 JavaScript를 사용하여 참조 URL(`https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`)과 현재 URL(`https://www.flywithus.com/`)을 수집합니다.
1. [!DNL Analytics]는 [!UICONTROL 참조 도메인], [!UICONTROL 검색 엔진] 및 [!DNL Search Keywords] 등의 여러 보고서에 이러한 상호 작용 중에 수집된 정보를 보고합니다.

## 예: 리디렉션을 사용하여 찾아보기 {#section_921DDD32932847848C4A901ACEF06248}

리디렉션으로 인해 브라우저는 실제 참조 URL을 완전히 지울 수 있습니다. 다음 시나리오를 참조하십시오.

1. 사용자는 브라우저가 `https://www.google.com`을 가리키게 하고 검색 필드에 *할인 항공 티켓*&#x200B;을 입력한 다음 **[!UICONTROL 검색]** 단추를 클릭합니다.
1. 브라우저 창의 주소 표시줄에 사용자가 검색 필드에 입력한 검색어(`https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`)가 표시됩니다. 검색어는 `https://www.google.com/search?` 다음에 오는 URL 쿼리 문자열 매개 변수에 포함됩니다. 또한 브라우저는 도메인 이름 중 하나([!DNL https://www.flytohawaiiforfree.com/])/)에 대한 링크를 포함하는 검색 결과를 포함하는 페이지를 표시합니다. *vanity* 도메인은 사용자를 `https://www.flywithus.com/` /으로 리디렉션하도록 구성되었습니다.
1. 사용자가 `https://www.flytohawaiiforfree.com/` 링크를 클릭하면 서버가 사용자를 주 사이트인 `https://www.flywithus.com`으로 리디렉션합니다. 리디렉션이 발생할 때 브라우저가 참조 URL을 지우므로 [!DNL Analytics] 데이터 수집에 중요한 데이터가 유실됩니다. 따라서 [!DNL Analytics] 보고서(예: [!UICONTROL 참조 도메인], [!UICONTROL 검색 엔진], [!UICONTROL 검색 키워드])에 사용된 원래 검색 정보가 유실됩니다.

[리디렉션 구현](../../implement/js-implementation/redirects-overview.md#concept_5EC2EE9677A44CC5B90A38ECF28152E7)에서 [!DNL Analytics] 변수를 활용하여 리디렉션에서 유실된 데이터를 캡처하는 방법을 설명합니다. 특히, 이 섹션에서는 위에서 설명한 "할인 항공 티켓" 상황을 해결하는 방법을 설명합니다.

## 구현 리디렉션 {#concept_5EC2EE9677A44CC5B90A38ECF28152E7}

리디렉션에서 [!DNL Analytics][!DNL AppMeasurement] 데이터를 캡처하려면 리디렉션 및 JavaScript용 파일을 만드는 코드에 대해 4가지 사항을 조정해야 합니다.

<!-- 

redirects_implement.xml

 -->

다음 단계를 완료하면 원래 레퍼러(예: 위의 시나리오에서 `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`)가 사용자 사이트에 전달하는 정보는 그대로 유지됩니다.

## 레퍼러 대체 JavaScript 코드 구성 {#section_87BB1D47D9C345C18339078824645CC4}

<!-- 

redirects_js_override.xml

 -->

아래의 코드 조각은 두 개의 JavaScript 변수인 *`s_referrer`*&#x200B;와 *`s_pageURL`*&#x200B;을 보여줍니다. 이 코드는 리디렉션의 최종 랜딩 페이지에 삽입됩니다.

```js
<script language="JavaScript" src="//INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="" 
s.pageURL=""
```

>[!IMPORTANT]
>
>페이지에서 *`s.referrer`*&#x200B;를 한 번만 설정합니다. 모든 추적 호출이나 추적되는 모든 링크 클릭으로 두 번 이상 설정하면 검색 엔진 및 키워드와 같은 레퍼러 및 관련 차원들이 두 번씩 계산됩니다.

## getQueryParam를 사용한 리디렉션 {#section_EE924E399F7A431C8FC8E8A2BEF84DEC}

[!UICONTROL getQueryParam]은 [!DNL Analytics] 변수를 쿼리 문자열 값으로 채우는 쉬운 방법이지만, 쿼리 문자열이 비어 있을 때 적합한 레퍼러가 덮어쓰이지 않도록 임시 변수와 연결해서 구현해야 합니다. [!UICONTROL getQueryParam]를 사용하는 가장 좋은 방법은 다음의 의사 코드로 설명했듯이 [!UICONTROL getValue]와 관련되어 있습니다.

```js
// AppMeasurement 1.x 
var tempVar=s.Util.getQueryParam('origref') 
if(tempVar) 
  s.referrer=tempVar;
```

```js
// H Code 
var tempVar=s.getQueryParam('origref') 
if(tempVar) 
  s.referrer=tempVar;
```

## 리디렉션 메커니즘 수정 {#section_2FF9921E8FCA4440B6FF90F15386E548}

<!-- 

redirects_modify_mechanism.xml

 -->

브라우저는 URL을 참조하여 스크립트를 작성하므로, 원래 레퍼러 정보를 전달할 리디렉션(예: 웹 서버, 서버측 코드, 클라이언트 측 코드)을 처리하는 메커니즘을 구성해야 합니다. 또한 별칭 링크 URL을 기록할 경우에도 이것을 최종 랜딩 페이지로 전달해야 합니다. 현재 URL을 대체하려면 *`s_pageURL`* 변수를 사용하십시오.

리디렉션을 구현하는 방법으로는 여러 가지가 있으므로, 웹 운영 그룹 또는 온라인 광고 파트너과 함께 확인해서 웹 사이트에서 리디렉션을 실행하는 특정 메커니즘을 식별해야 합니다.

## 원래 레퍼러 캡처 {#section_7F1A77F447CF485385B456A64B174050}

<!-- 

redirects_referrer.xml

 -->

일반적으로 [!DNL Analytics]는 브라우저의 [!UICONTROL document.referrer] 속성에서 참조 URL을 획득하고 [!UICONTROL document.location] 속성에서 현재 URL을 획득합니다. 값을 *`referrer`* 및 *`pageURL`* 변수에 전달하여 기본 처리를 재정의할 수 있습니다. referrer 변수로 값을 전달하여 [!DNL Analytics]에 [!UICONTROL document.referrer] 속성에 있는 레퍼러 정보를 무시하고 사용자가 정의한 대체 값을 사용할 것을 지시합니다.

따라서 랜딩 페이지의 최종 버전은 "할인 항공 티켓" 시나리오에서 나타난 문제를 수정하기 위해 다음 코드를 포함해야 합니다.

```js
<script language="JavaScript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets" 
// Setting the s.pageURL variable is optional. 
s.pageURL="https://www.flytohawaiiforfree.com"
```

## Adobe Debugger로 레퍼러 확인 {#section_B3E85941982E4E1698B271375AD669B9}

<!-- 

redirects_verify_referrer.xml

 -->

테스트를 실행하여 레퍼러, 원래 URL(*`s_server`*) 및 캠페인 변수가 캡처되고 있는지 확인합니다.

이러한 변수는 [Experience Cloud Debugger](https://marketing.adobe.com/resources/help/ko_KR/experience-cloud-debugger/)에서 다음 매개 변수로 표시됩니다.

<table id="table_5F3B987D4D514CA283F7B9F52EBC2301"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> <b>URL 또는 쿼리 문자열 값</b> </th> 
   <th class="entry"> <b>DigitalPulse Debugger에 표시된 값</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>원래 레퍼러 </p> </td> 
   <td> <p> <span class="filepath"> https://www.google.com/search%3F hl%3Den %26ie%3DUTF826q%3 Ddiscount%2Bairline%2Btickets </span> </p> </td> 
   <td> <p> <span class="filepath"> r=https:/ref=www.google.com/search?hl=en&amp;ie=UTF -8&amp;q=discount+airline+tickets </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>페이지 URL </p> </td> 
   <td> <p> <span class="filepath"> https://www.flytohawaiiforfree.com </span> </p> </td> 
   <td> <p> <span class="filepath"> g=https://www.flytohawaiiforfree.com </span> </p> <p>이 값은 <span class="varname"> pageURL </span> 변수를 사용하는 경우 DigitalPulse Debugger에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>최종 랜딩 페이지 URL </p> </td> 
   <td> <p> <span class="filepath"> https://www.flywithus.com </span> </p> </td> 
   <td> <p>이 값은 <span class="varname"> pageURL </span> 변수를 사용하는 경우 DigitalPulse Debugger에 표시되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

디버거가 표시하는 텍스트는 다음 예와 일치해야 합니다.

```
Image 
 
https://flywithuscom.112.2o7.net/b/ss/flywithuscom/1/JS-1.4/s61944015791667?[AQB] 
ndh=1 
t=4/8/2014 13:34:28 4 360 
pageName=Welcome to FlyWithUs.com 
r=https://ref=www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets 
cc=USD 
g=https://www.flytohawaiiforfree.com 
s=1280x1024 
c=32 
j=1.3 
v=Y 
k=Y 
bw=1029 
bh=716 
ct=lan 
hp=N 
[AQE]
```

Adobe [!UICONTROL Debugger]에 이러한 변수가 표시되는지 확인하면 항상 검색어와 원래 참조 도메인(리디렉션 전)이 보고서에서 트래픽을 등록 중인지 확인하는 데 유용합니다.
