---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics 구현
seo-description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
seo-title: 페이지 변수
solution: Analytics
subtopic: 변수
title: 페이지 변수
topic: 개발자 및 구현
uuid: 2578 EDDD -74 DB -4 A 8 A -96 F 2-D 0289 EC 1826 B
translation-type: tm+mt
source-git-commit: af2c0dd5269fe54dec949d4bd98bb09f22c9bfa2

---


# 페이지 변수

페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.

## browserHeight {#concept_DB87062001824369A56AA1E7969EC02A}

 변수는 브라우저 창의 높이를 표시합니다.

<!-- 
browserheight.xml
-->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

**매개 변수**

<table id="table_94598A2204CF42FF9DD14D353D5C0468"> 
 <thead> 
  <tr> 
   <th class="entry"> 쿼리 매개 변수 </th> 
   <th class="entry"> 값 </th> 
   <th class="entry"> 예 </th> 
   <th class="entry"> 영향을 받은 보고서 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>bh </p> </td> 
   <td> <p>양의 정수 </p> </td> 
   <td> <p>865 </p> </td> 
   <td> <p>트래픽 &gt; 기술 &gt; 브라우저 높이 </p> </td> 
  </tr> 
 </tbody> 
</table>

## browserWidth {#concept_BA0C4C2D655D41A4AEF059E21E4A55A2}

 변수는 브라우저 창의 너비를 표시합니다.

<!-- 

browserwidth.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

**매개 변수**

<table id="table_B70F279A8CD240328520E5BD889806BD"> 
 <tbody> 
  <tr> 
   <td> <p> <b>쿼리 매개 변수</b> </p> </td> 
   <td> <p> <b>값</b> </p> </td> 
   <td> <p> <b>예</b> </p> </td> 
   <td> <p> <b>영향을 받은 보고서</b> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>bw </p> </td> 
   <td> <p>양의 정수 </p> </td> 
   <td> <p>1179 </p> </td> 
   <td> <p>트래픽 &gt; 기술 &gt; 브라우저 너비 </p> </td> 
  </tr> 
 </tbody> 
</table>

## campaign {#concept_C7BF7B8A69D048A6AB482052A98A91F8}

 변수는 사이트로 방문자를 유도하는 데 사용된 마케팅 캠페인을 식별합니다. 의 값은 일반적으로 쿼리 문자열 매개 변수에서 가져옵니다.

<!-- 

campaign.xml

 -->

**매개 변수**

<table id="table_A35175678B6C4D3D86287199AFBE6803"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>255바이트 </p> </td> 
   <td> <p>v0 </p> </td> 
   <td> <p>전환 &gt; 캠페인 &gt; 추적 코드 </p> </td> 
   <td> <p>"" </p> </td> 
  </tr> 
 </tbody> 
</table>

마케팅 캠페인의 모든 요소에는 연관된 고유 추적 코드가 있습니다. 예를 들어 유료 검색 엔진 키워드에는 112233 추적 코드가 있습니다. 누군가 112233 추적 코드가 있는 키워드를 클릭하고 해당 웹 사이트로 연결되면 *`campaign`* 변수가 추적 코드를 기록합니다.

There are two main ways to populate the *`campaign`* variable:

* JavaScript 파일에서 사용되는 [!UICONTROL getQueryParam] 플러그인은 URL의 쿼리 문자열 매개 변수를 검색합니다. [!UICONTROL getQueryParam] 플러그인에 대한 자세한 내용은 [구현 플러그인](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

* Assign a value to the *`campaign`* variable in the HTML on the Web page.

*`campaign`* 변수를 채우는 방법 중 하나를 사용하여, 뒤로 단추 트래픽이 캠페인 요소에서 실제 클릭스루의 실제 수를 부풀릴 수 있습니다.

방문자가 유료 검색 키워드를 클릭하여 사이트에 들어올 때를 예로 들어봅시다. 방문자가 랜딩 페이지에 도착할 때 URL에는 해당 키워드의 추적 코드를 식별하는 쿼리 문자열 매개 변수가 들어 있습니다. 방문자가 다른 페이지로 가는 링크를 클릭하지만 즉시 [뒤로] 단추를 클릭하여 랜딩 페이지로 다시 돌아갑니다. 방문자가 랜딩 페이지에 두 번째로 도착할 때 쿼리 문자열 매개 변수가 포함된 URL이 추적 코드를 다시 식별합니다. 그리고 두 번째 클릭스루가 등록되고 그에 따라 클릭스루의 수가 잘못 부풀려집니다.

클릭스루가 이렇게 부풀려지지 않도록 하려면 [!UICONTROL getValOnce] 플러그인을 사용하여 각 캠페인 클릭스루가 세션당 한 번씩만 계산되도록 하는 것이 좋습니다. [!UICONTROL getValOnce] 플러그인에 대한 자세한 내용은 [구현 플러그인](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

**구문 및 가능한 값** {#section_91A141841A6D4711A1EE08A6145A301D}

```js
s.campaign="112233"
```

*`campaign`* 이 변수에는 다른 모든 변수와 동일한 제한 사항이 있습니다. 따라서 값을 표준 ASCII 문자로 제한하는 것이 좋습니다.

**대/소문자 구분** {#section_112A9A0F886148B6BEF9A7C94BE0A36F}

eVar는 대/소문자를 구분하지는 않지만 처음 사용한 대/소문자대로 표시됩니다. 예를 들어 eVar1을 처음 사용할 때 "Logged In"으로 설정되었지만, 그 이후의 모든 사용에서는 "logged in"으로 전달되는 경우, 보고서는 항상 "Logged In"을 eVar의 값으로 보여 줍니다.

**예** {#section_705A25D05F6848E29C78320247AECB5F}

```js
s.campaign="112233"
```

```js
s.campaign=s.getQueryParam('cid');
```

**구성 설정** {#section_4083F281968443169EAF8C0E8529D7BC}

각 캠페인 값은 한 사용자에 대해 활성화 상태로 유지되며, 만료되기 전까지 해당 사용자의 활동과 성공 이벤트에 대한 크레딧을 받습니다. 관리 콘솔에서 캠페인 변수의 만료를 변경할 수 있습니다.

**함정, 질문 및 팁** {#section_94B5C4BF9DE84BA3A16F9E9E9D197F0C}

* 클릭스루가 부풀려지지 않도록 하려면 [!UICONTROL getValOnce] 플러그인을 사용하여 캠페인 클릭스루가 세션당 한 번씩만 계산되도록 하십시오. [!UICONTROL getValOnce] 플러그인에 대한 자세한 내용은 [구현 플러그인](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

* 마케팅 캠페인 추적 및 키워드 구입에 대한 자세한 내용은 [캠페인](https://marketing.adobe.com/resources/help/en_US/reference/?f=campaign)을 참조하십시오.
* [!DNL DigitalPulse Debugger]를 사용하여 캠페인의 실제 값(디버거의 v0)을 살펴 보십시오. v0이 디버거에 나타나지 않으면, 해당 페이지에 대해 캠페인 데이터가 기록되지 않습니다.

## channel {#concept_C7770B8C15724A99B10F8F468AF82D0D}

이 변수는 사이트의 섹션을 식별하는 데 가장 자주 사용됩니다.

<!-- 

channel.xml

 -->

예를 들어 매장 주인에게는 전자 제품, 장난감 또는 의류 등의 섹션이 있을 수 있습니다. 미디어 사이트에는 뉴스, 스포츠 또는 비즈니스 등의 섹션이 포함될 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | CH | 사이트 컨텐츠 &gt; 사이트 섹션 | "" |

모든 페이지에서 채널 변수를 채우는 것이 좋습니다. 또한 *`channel`* 과 [!UICONTROL page name] 변수 간에 상관 관계를 설정할 수도 있습니다.

When sections have one or more levels of subsections, you can show those sections in the *`channel`* variable or use separate variables to identify levels.

**구문 및 가능한 값** {#section_ED90592730B64242A737F4090F1DCEE4}

```js
s.channel="value"
```

The *`channel`* variable has no extra limitations on its values.

**예** {#section_2527B2BB1CFD46CB952178ABF7A9028A}

```js
s.channel="Electronics"
```

```js
s.channel="Media"
```

**함정, 질문 및 팁** {#section_61941D5E4E644B59A267A4F44FD5DE8C}

If your site contains multiple levels, you can use the *`hierarchy`* or another variable to designate those levels. *`channel`* 값이 지속되지 않지만 같은 페이지에서 실행된 성공 이벤트는 *`channel`* 값에 귀속됩니다.

## colorDepth {#concept_756516E181F449B996DA9CC5A53FFA3D}

 변수는 화면의 각 픽셀에 색상을 표시하는 데 사용된 비트 수를 표시하는 데 사용됩니다.

<!-- 

colordepth.xml

 -->

예를 들어 32는 화면에 32비트 색상을 사용함을 나타냅니다. 이 변수는 페이지 코드의 뒤에 *`doPlugins`* 가 실행되기 전에 채워집니다.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 `props/eVars`에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| c | 8,16 및 32 | 32 | 트래픽 &gt; 기술 &gt; 모니터 색상 깊이 |

## connectionType {#concept_2F98ECB8BB3D490F834F274EFF02860E}

 변수는 Internet Explorer에서 브라우저가 LAN 또는 모뎀 연결에 대해 구성되어 있는지 여부를 나타냅니다.

<!-- 

conntype.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 `props/eVars`에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| ct | lan 또는 modem | lan | 트래픽 &gt; 기술 &gt; 연결 유형 |

## cookiesEnabled {#concept_DF5B37E38D0D4F6DB910F419F92467ED}

 변수는 자사 세션 쿠키를 JavaScript가 설정할 수 있는지 여부를 나타냅니다.

<!-- 

cookiesenabled.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 `props/eVars`에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 |
|---|---|---|
| k | Y 또는 N | Y |

## dc {#concept_ECE6C83376704B3C84A920EFDD338A31}

(사용 안 함)  변수는 데이터를 전송 받을 데이터 센터를 선택하는 데 사용됩니다.

<!-- 

dc.xml

 -->

>[!NOTE]
>
>dc 변수는 더 이상 사용되지 않습니다. 모든 구성에 대한 *`trackingServer`를 s_code.js에서 코드 관리자가 생성하는 값으로 설정해야 합니다.*

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | 112 |

데이터 센터는 *`dc`* 변수에서 식별하여 [!UICONTROL ActionSource]와 일치시킵니다.

## eVarN {#concept_74FFDDB44B5344E18ABC6F2F99DF4649}

[!UICONTROL eVar] 변수는 사용자 지정 보고서를 작성하는 데 사용됩니다.

<!-- 

eVarN.xml

 -->

eVar가 방문자에 대한 값으로 설정되면 이 값은 만료되기 전까지 기억됩니다. eVar 값이 활성일 때 방문자가 발견하는 성공 이벤트는 eVar 값으로 카운트됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 255바이트 | V1-v75 ( [or v100 or v250](../../../implement/js-implementation/c-variables/page-variables.md#concept_558663F3B8164986AB5D94128FEA7B28)) | 사용자 지정 전환 | "" |

**만료** {#section_6DB5882B960D4660AE248B91B76883C4}

[!UICONTROL eVar]은 지정되는 일정 시간 후 만료되며, 만료된 후 eVar는 더 이상 성공 이벤트에 대한 크레딧을 받지 않습니다. eVar를 성공 이벤트에 대해 만료되도록 구성할 수도 있습니다. 예를 들어 방문이 끝날 때 만료되는 내부 판촉 행사가 있을 경우, 이 내부 판촉 행사는 방문 중 발생하여 활성화되는 구매 또는 등록에 대해서만 크레딧을 받습니다.

다음과 같은 두 가지 eVar 만료 방법이 있습니다.

* 지정된 시간이나 이벤트 후 eVar가 만료되도록 설정할 수 있습니다.
* eVar의 강제 만료 기능을 사용할 수 있으며, 이 기능은 변수를 다른 목적에 사용할 때 유용합니다.

Evar가 내부 판촉 행사를 반영하기 위해 5 월에 사용되고 6 월에 내부 검색 키워드를 캡처하는 데 사용되는 경우, 6 월 1 일에 변수를 만료하거나 재설정해야 합니다. 이렇게 하면 내부 판촉 행사 값을 6월의 보고서에서 빼는 데 유용합니다.

**대/소문자 구분** {#section_6E9145B7FCC2438E95BB35AAE3857412}

eVar는 대/소문자를 구분하지는 않지만 처음 사용한 대/소문자대로 표시됩니다. 예를 들어 eVar1을 처음 사용할 때 "Logged In"으로 설정되었지만, 그 이후의 모든 사용에서는 "logged in"으로 전달되는 경우, 보고서는 항상 "Logged In"을 eVar의 값으로 보여 줍니다.

**카운터**{#section_D8403F0C175E4BC9BE4F2E794B1F4D33}

eVar는 대부분 문자열 값을 보관하는 데 사용되지만, 카운터로 작동하도록 구성할 수도 있습니다. eVar는 이벤트 전에 사용자가 취하는 동작의 수를 세려고 할 때 카운터로 유용합니다. 예를 들어 구매 전에 eVar를 사용하여 내부 검색 횟수를 캡처할 수 있습니다. 방문자가 검색할 때마다, eVar에는 '+1'의 값이 포함되어 있어야 합니다. 방문자가 구매 전에 검색을 네 번 수행하면, 각각 총 횟수는 1.00, 2.00, 3.00 및 4.00이 됩니다. 하지만 구매 이벤트에 대해서는 4.00만 크레딧을 받습니다(주문 및 매출 지표). eVar 카운터의 값으로는 양수만 허용됩니다.

**하위 관계**{#section_2BEABBBC735241F4BA42E74D19B5AEE0}

[!UICONTROL 사용자 지정 eVar] 보고서에 대한 일반적인 요구 사항은 하나의 [!UICONTROL 사용자 지정 eVar] 보고서를 다른 eVar로 분류하는 기능입니다. 예를 들어 한 eVar에 성별이 들어 있고 다른 eVar에 급료가 들어 있는 경우, 사이트의 여성 방문자 중에 '연간 $50,000 이상을 버는 여성이 얼마의 매출을 생성했는가'라는 질문을 할 수 있습니다. 전체 하위 관계인 모든 eVar는 보고서에서 이러한 유형의 분류를 허용합니다. 예를 들어 성별 eVar에 전체 하위 관계가 활성화되어 있는 경우, 모든 다른 사용자 지정 eVar 보고서는 성별로 분류할 수 있고 성별은 모든 다른 eVar로 분류할 수 있습니다. 두 보고서 간의 관계를 보기 위해서는, 이 중 하나의 전체 하위 관계만 활성화되어 있어야 합니다. 기본적으로 [!UICONTROL 캠페인], [!UICONTROL 제품] 및 [!UICONTROL 카테고리] 보고서의 경우 전체 하위 관계가 활성화되어 있습니다(모든 eVar는 캠페인이나 제품으로 분류할 수 있음).

**구문 및 가능한 값** {#section_BD46438B14F3488FB9AC42994C317B06}

While eVars may be renamed, they should always be referred to in the JavaScript file by eVarX, where X is a number between 1 and 75 ( [or 100, or 250](../../../implement/js-implementation/c-variables/page-variables.md#concept_558663F3B8164986AB5D94128FEA7B28)).

```js
s.eVarX="value"
```

카운터로 사용하지 않는 eVar는 다른 모든 변수와 동일한 제한 사항을 가집니다. eVar가 "카운터"일 경우에는 "1" 또는 "2.5"와 같은 숫자 값을 받게 됩니다. 소수점 이하 자리 수가 세 자리 이상인 수가 지정되는 경우, eVar 카운터는 소수점 이하 두 자리로 반올림합니다. eVar 카운터에는 음수가 들어 있을 수 없습니다.

**예** {#section_B37F4B0D56734DA3AB02BB218825BA4E}

```js
s.eVar1="logged in"
```

```js
s.eVar23="internal spring promo 4"
```

**구성 설정** {#section_BD1FE63001C84D3DB69F3DEE243960B6}

eVars can be configured in [!UICONTROL Analytics &gt; Admin &gt; Report Suites &gt; Edit Settings &gt; Conversion &gt; Conversion Variables]. 모든 eVar는 [!UICONTROL 이름], [!UICONTROL 유형], [!UICONTROL 할당], [!UICONTROL 설정 후 만료] 또는 [!UICONTROL 재설정]으로 구성할 수 있습니다. 각 구성 설정은 개별적으로 지정됩니다.

<table id="table_5C524B71520849FA8A9A6B79A3EE77C9"> 
 <thead> 
  <tr> 
   <th class="entry"> 설정 </th> 
   <th class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 이름 </td> 
   <td> <span class="keyword">Analytics</span> 내에서 eVar 보고서의 이름을 변경할 수 있도록 해줍니다 . <p><span class="keyword">Analytics</span>에서 보고서에 어떤 이름이 지정되었는지에 관계없이 JavaScript 코드에서는 여전히 eVar를 s.eVarX로 참조해야 합니다 . </p> </td> 
  </tr> 
  <tr> 
   <td> 유형 </td> 
   <td> eVar가 텍스트 문자열인지 아니면 카운터인지 표시할 수 있도록 해줍니다. </td> 
  </tr> 
  <tr> 
   <td> 할당 </td> 
   <td> eVar의 값 중 어느 값이 성공 이벤트에 대한 크레딧을 받는지를 구성하는 데 사용됩니다. <p>할당이 "가장 최근(마지막)"으로 설정되면, B가 크레딧을 받습니다. </p> <p>할당이 "원래 값(처음)"으로 설정되면, A가 크레딧을 받습니다. </p> <p>할당이 "선형"으로 설정되면, A와 B 모두가 구매 가치의 반에 대한 크레딧을 받습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> 다음 날짜 이후에 만료 </td> 
   <td> eVar가 구매와 같은 특정 이벤트 발생 시 만료되는지, 아니면 사용자 지정 또는 사전 정의된 시간 후 만료되는지를 결정할 수 있도록 해줍니다. </td> 
  </tr> 
  <tr> 
   <td> 재설정 </td> 
   <td> eVar에 대한 <span class="wintitle">재설정</span> 확인란을 선택하고 페이지 하단에 있는 <span class="wintitle">저장</span>을 클릭하면, 해당 eVar의 모든 값이 즉시 만료됩니다. 이렇게 되면 eVar의 새 값만 성공 이벤트에 대한 크레딧을 받습니다. </td> 
  </tr> 
 </tbody> 
</table>

**함정, 질문 및 팁** {#section_DA6912C802E445F986C6DE4234C6C737}

* [!UICONTROL prop] 변수와 달리, eVar 변수는 구분된 값 목록이 될 수 없습니다. 값 목록으로 eVar를 채우는 경우(예: "one,two,three") 이 문자열이 그대로 보고서에 나타납니다.
* eVar 카운터는 음수를 포함할 수 없습니다.

## events{#concept_FFD115543D54401B98FE683BD7D5B3FE}에 나와 있습니다 

 변수는 일반적인 장바구니 성공 이벤트와 사용자 지정 성공 이벤트를 기록하는 데 사용됩니다.

<!-- 

events.xml

 -->

<table id="table_9EB9D08C80544CD68C4B1A2012440472"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 제한 없음 </td> 
   <td> events </td> 
   <td> <p>장바구니 이벤트 </p> <p>사용자 지정 이벤트 </p> </td> 
   <td> N/A </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL 이벤트]는 사이트 내에서 중대한 이벤트로 간주되어야 합니다. 성공 이벤트는 대개 등록 프로세스나 뉴스레터 가입과 같이, 프로세스의 최종 확인 페이지에서 채워집니다. 사용자 지정 이벤트는 아래의 가능한 값 섹션에 정의된 문자 값으로 events 변수를 채우는 방식으로 정의됩니다.

기본적으로, 성공 이벤트는 *카운터* 이벤트로 구성됩니다. 카운터 이벤트는 성공 이벤트가 설정되는 횟수(x+1)를 카운트합니다. 이벤트는 *숫자* 이벤트로도 구성됩니다. 숫자 이벤트를 사용하면 숫자를 증분으로 지정할 수 있습니다(내부 검색에서 반환되는 결과 수와 같이, 동적 또는 임의의 값을 카운트할 때 필요할 수 있기 때문에).

최종 이벤트 유형인 *통화*&#x200B;를 사용하면 추가되는 금액을 정의할 수 있습니다(숫자 이벤트와 유사). 하지만 통화는 보고서에서 통화로 표시되며,  *`currencyCode`*&#x200B;값과 보고서 세트에 대한 기본 통화 설정을 기반으로 통화 전환이 가능합니다. For additional information on using numeric and currency events, see [Products](../../../implement/js-implementation/c-variables/page-variables.md#concept_A4007F6307E4419DAA65E1668A8FEBA2).

**변수 구성** {#section_9195286C34C54B02B2598E2B856492C3}

[!UICONTROL s.events] 변수는 모든 구현에 대해 기본적으로 활성화되어 있습니다. 7개의 사전 구성된 전환 이벤트는 모든 새 보고서 세트에 대해 자동으로 활성화됩니다. New custom events (event1- [event100 or event1000](../../../implement/js-implementation/c-variables/page-variables.md#concept_558663F3B8164986AB5D94128FEA7B28)) can be enabled by any admin-level user using the Admin Console.

**가능한 값** {#section_18395A3BEFEB4E9F8D7B2ED0001FBE4E}

다음은 events 변수에 가능한 값의 목록입니다.

| 이벤트 | 설명 | 채워진 보고서 |
|---|---|---|
| prodView | 제품 보기 횟수 | 제품 |
| scOpen | 새 장바구니 열기/초기화 | 장바구니 |
| scAdd | 장바구니에 항목 추가 | 장바구니 추가 |
| scRemove | 장바구니에서 항목 제거 | 장바구니 제거 |
| scView | 장바구니 보기 | 장바구니 보기 |
| scCheckout | 체크아웃 프로세스의 시작 | 체크아웃 |
| purchase | 구매(주문) 완료 | 주문 |
| event1~event1000(포인트 제품의 경우 event100) | 사용자 지정 이벤트 | 사용자 지정 이벤트 |

**구문 및 예** {#section_45A159DF00114066B8551DDEB15E084C}

카운터 이벤트는 [!UICONTROL s.events] 변수에서, 쉼표로 구분된 목록(여러 이벤트를 전달해야 하는 경우)으로 원하는 이벤트를 삽입하여 설정합니다.

```js
s.events="scAdd"
```

```js
s.events="scAdd,event1,event7"
```

```js
s.events="event5"
```

```js
s.events="purchase,event10"
```

H23 이상의 코드인 경우, 카운터 이벤트에 2 이상의 정수가 지정되어 있을 수 있습니다.

```js
s.events="event1=10"
```

```js
s.events="scRemove=3,event6,event2=4"
```

지정된 정수 값이 있는 카운터 이벤트를 구현하면 이벤트가 이미지 요청 내에서 여러 번 실행되는 것처럼 취급됩니다. 카운터 이벤트에서는 소수를 허용하지 않으므로, 이 기능이 필요할 경우에는 숫자 이벤트를 대신 사용하는 것이 좋습니다.
보통 숫자 및 통화 이벤트가 [!UICONTROL s.products] 변수에서 숫자 값(예: 24.99)을 받기는 하지만, 이 이벤트들은 [!UICONTROL s.events] 변수에 포함되어야 합니다. 이렇게 하면 특정 숫자 및 통화 값을 개별 제품 항목에 연결할 수 있습니다.

**이벤트 정리** {#section_A89488EF4471405AAFC4D6DD05E77621}

기본적으로, 이벤트는 사이트에서 이벤트가 설정될 때마다 카운트됩니다.

자세한 내용은 [이벤트 정리](../../../implement/js-implementation/event-serialization.md#concept_092B638D7FEE423D91F8A57EA8E09705)를 참조하십시오.

**구문** {#section_8559D42D3F344AF3BB3C0125F78C4989}

```js
s.events="event1:3167fhjkah"
```

**예** {#section_7B5B5728A59648ADB3E2548CDAD2C9D4}

```js
s.events="scAdd:003717174"
```

```js
s.events="scAdd:user228197,event1:577247280,event7:P7fhF8571"
```

## hierN {#concept_C4475D1584D544ACB4C0A573EB60FA08}

[!UICONTROL 계층] 변수는 사이트의 계층에서 페이지의 위치를 결정합니다.

<!-- 

hierN.xml

 -->

이 변수는 사이트 구조의 수준이 4 이상인 사이트에 가장 유용합니다. 예를 들어 미디어 사이트의 스포츠 섹션에는 스포츠, 해외 스포츠, 야구 및 Red Sox, 이렇게 4개 수준이 있을 수 있습니다. 누군가 야구 페이지를 방문하면 스포츠, 해외 스포츠 및 야구가 해당 방문을 모두 반영합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 255바이트 | H1-H5 | 계층 | "" |

사용할 수 있는 [!UICONTROL 계층] 변수에는 5가지가 있으며, 이 변수들은 Adobe 고객 지원 센터에서 활성화해야 합니다. 계층 활성화 시, 변수에 대한 구분 기호와 계층의 최대 수준 수를 결정해야 합니다. 예를 들어, 구분 기호가 쉼표인 경우 스포츠 계층은 다음과 같이 표시될 수 있습니다.

```js
s.hier1="Sports,Local Sports,Baseball"
```

섹션 이름 중에 그 안에 구분 기호가 포함되는 섹션이 없도록 하십시오. 예를 들어 섹션 중 하나를 "Coach Griffin, Jim"이라고 한다면, 쉼표 이외의 구분 기호를 선택해야 합니다. 각 계층 섹션은 255바이트로 제한되며, 총 변수 제한도 255바이트입니다. 구분 기호를 선택한 후(계층이 만들어질 때)에는 쉽게 변경되지 않습니다.

기본 계층에 대한 구분 기호 변경에 대해서는 Adobe 고객 지원 센터에 문의하십시오. || 또는 /|\와 같이 여러 문자로 구성된 구분 기호를 사용할 수도 있지만, 계층 섹션에는 잘 사용되지 않습니다.

**구문 및 가능한 값** {#section_0739948A68A2420DAB1CBEA3115A5A66}

각 구분 기호 사이에 공백을 넣지 마십시오. 다음 예제 구문에서, N은 1과 5 사이의 숫자입니다.

```js
s.hierN="Level 1[<delimiter>Level 2[<delimiter>Level 3[...]]]"
```

계층 수준을 구분할 때를 제외하고는 구분 기호를 사용하지 마십시오. 구분 기호는 선택한 문자 또는 문자들일 수 있습니다.

**예** {#section_38E0929F88DD45B6ACDF473DF155971D}

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub"
```

```js
s.hier4="Sports/Local Sports/Baseball"
```

**구성 설정** {#section_E823FB3CAD744D2480EBCE2DF9B134CC}

없음

**함정, 질문 및 팁** {#section_104E5BD320764BDEA5FA8D13A70C78E3}

* 계층이 설정되고 나면 구분 기호를 변경할 수 없습니다. 계층의 구분 기호를 변경해야 하는 경우에는 Adobe 고객 지원 센터에 문의하십시오.
* 계층을 설정하고 나면 수준 수를 변경할 수 없습니다.

>[!NOTE]
>
>계층을 변경하면 서비스 요금이 발생할 수 있습니다.

## homepage {#concept_0A3E416F1A064BA396B5FCEABFB7B0B4}

 변수는 Internet Explorer에서 현재 페이지가 사용자의 홈 페이지로 설정되어 있는지 여부를 나타냅니다.

<!-- 

homepage.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| hp | Y 또는 N | Y | 트래픽 &gt; 기술 &gt; 홈 페이지 |

## javaEnabled {#concept_F24A3536F1F0453DA214B16BAA5A6F67}

 변수는 브라우저에서 Java가 활성화되어 있는지 여부를 가리킵니다.

<!-- 

javaEnabled.xml

 -->

이 변수는 페이지 코드의 뒤에, doPlugins가 실행되기 전에 채워집니다.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| v | Y 또는 N | Y | 트래픽 &gt; 기술 &gt; Java |

## javascriptVersion {#concept_19E2C9F87BB24E69B911C0F5873CAA90}

 변수는 브라우저가 지원하는 JavaScript 버전을 가리킵니다.

<!-- 

javascriptVersion.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| j | 1.0, 1.1, 1.2, … 1.7 | 1.7 | 트래픽 &gt; 기술 &gt; JavaScript 버전 |

버전 H.10 이상의 JavaScript 파일은 최대 버전 1.7(H.10 발표 당시 가장 높은 버전)까지 정확하게 감지합니다. 이전 JavaScript 파일 버전은 버전 1.3까지만 감지했습니다.

## linkName {#concept_1B2A3F56C9AD4C23A8A4331730EC2B8F}

The  variable is an optional variable used in [!UICONTROL Link Tracking] that determines the name of a custom, download, or exit link.

<!-- 

linkName.xml

 -->

The *`linkName`* variable is not normally needed because the third parameter in the *`tl()`* function replaces it.

<table id="table_4B0D1C9AADA542A59B626E077D5FC568"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 100바이트 </td> 
   <td> pev2 </td> 
   <td> <p>파일 다운로드 </p> <p>사용자 지정 링크 </p> <p>종료 링크 </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL 사용자 지정 링크]는 추적 데이터를 보내는 링크를 말합니다. the *`linkName`* 변수 (또는 *`tl()`* 함수의 세 번째 매개 변수) 는 [!UICONTROL 사용자 지정], [!UICONTROL 다운로드]또는 [!UICONTROL 종료 링크] 보고서에 나타나는 값을 식별하는 데 사용됩니다. If *`linkName`* is not populated, the URL of the link appears in the report.

**구문 및 가능한 값** {#section_C8D89834C98B4C7A858C947293C4148E}

```js
s.linkName="Link Name"
```

There are no limitations on *`linkName`* outside of the standard variable limitations.

**예** {#section_5F68766210184E82A23D2A6ECD80BA0B}

```js
s.linkName="Nav Bar Home Link"
```

```js
s.linkName="Partner Link to A.com"
```

**구성 설정** {#section_F15FF429FC274F708D50DF79D4668EA3}

없음

**함정, 질문 및 팁** {#section_170A78452A7340B5B229713AC1FB71FA}

* *`linkName`* 이 변수는 *`tl()`* 함수에서 세 번째 매개 변수로 대체됩니다.

* If the *`linkName`* variable and the third parameter in the *`tl()`* function are blank, the full URL of the link (with the exception of the query string) appears in the report (even if the link is relative).

## linkType {#concept_7695692AF5D843E3B370F6D345E32964}

 변수는 링크 이름 또는 URL이 표시되는 보고서(사용자 지정, 다운로드 또는 종료 링크)를 결정하는 링크 추적에 사용되는 선택 변수입니다.

<!-- 

linkType.xml

 -->

The *`linkType`* variable is not normally needed because the second parameter in the *`tl()`* function replaces it.

<table id="table_3D1A2FC1CECD4709BE2F9E32AC2DC730"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 1자 </td> 
   <td> pe=[lnk_o|lnk_d|lnk_e] </td> 
   <td> <p>파일 다운로드 </p> <p>사용자 지정 링크 </p> <p>종료 링크 </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

사용자 지정 링크는 데이터를 Analytics로 보냅니다. *`linkType`* 변수 (또는 *`tl()`* 함수의 두 번째 매개 변수) 는 링크 이름 또는 URL 이 표시되는 보고서 ( [!UICONTROL 사용자 지정], [!UICONTROL 다운로드]또는 [!UICONTROL 종료 링크] 보고서) 를 식별하는 데 사용됩니다.

For exit and download Links, the *`linkType`* variable is automatically populated depending on whether the link clicked is an exit or download link. A custom link may be configured to send data to any of the three reports with this variable or with the second parameter in the *`tl()`* function. By setting *`linkType`* to 'o,' 'e,' or 'd,' the *`linkName`* or link URL is sent to the [!UICONTROL Custom Links], [!UICONTROL Exit Links], or [!UICONTROL File Downloads] report respectively.

**구문 및 가능한 값** {#section_18DB3A8083FB4F75B970055ED336DA4E}

*`linkType`* 변수 구문은 XML 또는 쿼리 문자열을 사용하는지에 따라 다릅니다.

XML을 사용하는 경우 변수에는 단일 문자, 즉, 'o,' 'e' 또는 'd'만 포함될 수 있습니다.

```js
s.tl(this,’o’,’Link Name’);
```

If you are using the query-string `pe`, you need to use `lnk_d`, `lnk_e`, or `lnk_o`.

**예** {#section_242B5DFFD1C9462A9A8EB1556B2E3160}

```js
<a href="index.html" onClick=" 
 var s=s_gi('rsid'); **see note below on the rsid** 
 s.tl(this,'o','Link Name'); 
 ">My Page</a> 
```

**구성 설정** {#section_59738AD1B5E94294B8D36F4E772DEDB3}

없음

**함정, 질문 및 팁** {#section_F0D01DDE3FDA486C987162DA50A79C45}

* If *`linkType`* is not specified, custom links ('o') is assumed.

## List Props {#concept_83ED74232225431F83A796E22FFC75B4}

목록 prop은 변수로 전달되는 값의 목록을 구분 기호로 구분한 후 개별 라인 항목으로 보고하는 것입니다. 목록 prop은 일반적으로 확인란 또는 라디오 단추와 같이 사용자가 선택 가능한 값이 포함된 페이지에 구현됩니다. 여러 이미지 요청을 보내지 않고 변수에서 여러 값을 정의하려는 경우 유용합니다.

<!-- 

list_props.xml

 -->

**고려 사항**

* 목록 Prop은 트래픽 변수([prop](../../../implement/js-implementation/c-variables/page-variables.md#concept_0F10FA2DE69B4029A31EA5E9313AA254))에서만 활성화됩니다.
* 경로 지정 및 상관 관계는 목록 prop에 대해 활성화할 수 없습니다.
* Analytics에서는 모든 목록 prop 보고서를 포함하여 거의 모든 보고서에 방문 횟수 및 방문자 수를 제공합니다.
* 목록 Prop에는 분류가 지원됩니다.
* 모든 사용자 지정 트래픽 변수는 목록 Prop이 될 수 있습니다. (예외: [Pagename](../../../implement/js-implementation/c-variables/page-variables.md#concept_5827B499DAC34B5D8445F9D9140CC328), [channel](../../../implement/js-implementation/c-variables/page-variables.md#concept_C7770B8C15724A99B10F8F468AF82D0D)및 [server](../../../implement/js-implementation/c-variables/page-variables.md#concept_BF77952603BA454BAFC9A0A81D06A7D2).)

* 동일한 이미지 요청에서 중복 값을 정의하면, 인스턴스가 중복되지 않습니다.

Prop은 [관리 도구] &gt; [보고서 세트] &gt; [트래픽 변수] 페이지에서 [목록 지원]을 활성화한 다음 구분 기호를 선택하여 목록 Prop으로 변경할 수 있습니다. 많이 사용하는 구분 기호는 콜론, 세미콜론, 쉼표 또는 파이프입니다. 기술적으로는 ASCII 문자의 처음 127개 중 원하는 것을 사용할 수 있습니다.

**구현 예제** {#section_A3DD7293A8BB4807B42BFB1F73BE11AC}

목록 Prop 활성화를 요청할 때 사용할 구분 기호를 지정합니다. 선택한 *`s.prop`*&#x200B;이 활성화되고 나면 다음 예와 같이 변수에 여러 값을 설정할 수 있습니다.

파이프를 구분 기호로 사용하며 두 값을 전달하는 목록 Prop:

```js
s.prop1="Banner ad impression|Sidebar impression"
```

쉼표를 구분 기호로 사용하며 여러 값을 전달하는 목록 Prop:

```js
s.prop2="cerulean,vermilion,saffron"
```

단일 값과 함께 목록 Prop을 전송할 수도 있습니다.

```js
s.prop3="Single value"
```

구분 기호는 언제든지 변경할 수 있습니다. 그러나 구현과 새 구분 기호가 일치해야 합니다. 올바른 구분 기호를 사용하지 않으면 보고서에서 목록 Prop 값이 단일 연결된 라인 항목으로 취급됩니다.

목록 Prop도 트래픽 변수이기 때문에 트래픽 변수의 제한이 적용됩니다. 목록 prop은 데이터가 100바이트로 제한되어 있으며, 대소문자 구분 설정의 영향을 받습니다.

## 목록 변수 {#concept_AC42F2D69B674C02A484137CE5B4E687}

List Var라고도 합니다. 목록 Prop과 마찬가지로 목록 변수는 같은 이미지 요청에서 여러 값을 사용할 수 있도록 허용합니다. 변수가 정의된 이미지 요청을 넘어서까지 지속된다는 점에서 eVar와도 비슷하게 작동합니다. 이러한 변수를 사용하여 제품 목록, 위시리스트, 검색 세분화 또는 디스플레이 광고 목록과 같은 여러 요소 사이의 인과 관계를 단일 페이지로 볼 수 있습니다.

<!-- 

listN.xml

 -->

**고려 사항**

* 목록 변수는 방문자 브라우저의 VisitorID 쿠키를 참조하여 구체적인 값을 기억합니다.
* 250개의 최대값이라는 제한은 방문자에 대해 한 번에 저장됩니다. 방문자당 250개 값을 초과하면 최신 250개 값이 사용됩니다. 이러한 값의 만료는 변수에 대해 구성된 만료일을 기준으로 합니다.
* 구분 기호로 구분된 각 값에는 최대 255자를 포함할 수 있습니다(멀티바이트 문자를 사용하는 경우 더 적음). 이것은 각 요소의 최대 길이입니다.
* 이 변수의 문자 수에는 제한이 없습니다. 이 제한에 대한 유일한 예외는 이전 Internet Explorer 브라우저로서, 이전 Internet Explorer 브라우저는 모든 URL 요청에 대해 2083자 제한을 적용합니다.
* 보고서 세트당 총 세 개의 목록 변수를 사용할 수 있습니다.
* 목록 변수를 사용하려면 H23 코드 이상이 필요합니다.
* 목록 변수는 분류할 수 있습니다.
* 중복 값이 같은 이미지 요청에 정의되지 않을 경우, 목록 변수는 이 값의 모든 인스턴스에 대한 중복을 제거합니다.
* 가장 세분화된 목록 변수는 히트(또는 페이지 보기) 수준에서 세그먼트화할 수 있습니다. 같은 이미지 요청에 세 개의 값이 있는 목록 변수가 있을 경우, 하나의 값과 일치하는 모든 세그먼트 규칙은 세 개를 모두 보고에 포함합니다. 정반대로, 하나의 값을 만족하는 제외 규칙이 정의되면, 세 개의 값이 모두 제외됩니다.

**구성** {#section_8CADFF581D2447518BA3F7F79B2D80A9}

Adobe 고객 지원 센터의 도움 없이도 관리 콘솔에서 구성에 액세스하여 업데이트할 수 있습니다.

1. **[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리]** &gt; **[!UICONTROL 보고서 세트로 이동합니다.]**
1. 보고서 세트를 선택합니다.
1. Click  **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Conversion]** &gt; **[!UICONTROL List Variables]** .

* **이름**: 구분 기호로 구분된 각 값에는 최대 255자를 포함할 수 있습니다(멀티바이트 문자를 사용하는 경우 더 적음). 이것은 각 요소의 최대 길이입니다.
* **값 구분 기호**: 목록 변수에서 값을 구분하는 데 사용되는 문자입니다. 일반적으로 쉼표, 콜론, 파이프 또는 그와 비슷한 것이 사용됩니다.

   >[!NOTE]
   >
   >목록 변수에서는 멀티바이트 문자가 구분 기호로 지원되지 않습니다. 구분 기호는 싱글 바이트여야 합니다.

* **만료**: eVar 만료와 비슷하며 목록 변수와 전환 이벤트 사이에 허용되는 시간을 결정합니다.

   * **페이지 보기 또는 방문 수준에서**: 페이지 보기 또는 방문의 범위를 벗어나는 성공 이벤트는 목록 변수의 값으로 다시 링크되지 않습니다.
   * **일, 주, 월 등의 기간 기준**: 지정된 기간을 벗어나는 성공 이벤트는 목록 변수의 값으로 다시 링크되지 않습니다. 사용자 지정 일 수도 정의할 수 있습니다.
   * **특정 전환 이벤트**: 지정된 특정 이벤트가 목록 변수의 값으로 다시 링크되지 않을 경우 시작할 다른 성공 이벤트입니다.
   * **안 함**: 목록 변수와 성공 이벤트 사이에 허용되는 시간을 제한하지 않습니다.

* **할당**: 성공 이벤트가 다음과 같은 값들 간에 크레딧을 어떻게 나누는지를 결정합니다.

   * **전체**: 이 변수의 만료 전에 정의된 모든 변수가 성공 이벤트에 대한 전체 크레딧을 받습니다.
   * **선형**: 이 변수의 만료 전에 정의된 모든 변수가 전환 이벤트에 대한 크레딧이 나누어진 크레딧을 받습니다.
   * 변수 값은 절대 덮어써지지 않지만, 대신 성공 이벤트에 대한 크레딧을 받는 값에 추가됩니다.

* **최대값**: 이 목록 변수에서 허용되는 활성 값의 수를 지정합니다. 예를 들어 3으로 설정된 경우 마지막으로 캡처된 3개 값만 저장되고 이전 값은 지워집니다. 같은 목록 변수에 대한 여러 개의 값이 같은 히트로 전송되고 최대값 사용이 제한된 경우 각 값이 같은 타임스탬프를 갖기 때문에 어떤 값이 저장될지 보장할 수 없습니다.

   250개의 최대값이라는 제한은 방문자에 대해 한 번에 저장됩니다. 방문자당 250개 값을 초과하면 최신 250개 값이 사용됩니다. 이러한 값의 만료는 변수에 대해 구성된 만료일을 기준으로 합니다.

   최대값 설정은 속성을 특정한 개수의 값으로 제한할 때 유용합니다. 예를 들어 목록 변수가 방문 첫 번째 페이지에서 "A,B,C"로 설정되고 다음 페이지에서 "X,Y,Z"로 설정된 경우 할당을 기준으로 속성이 이러한 6개의 값으로 배포됩니다. 속성을 "X,Y,Z"로만 제한하려면 최대값을 3으로 설정하면 됩니다.

To set up or edit List Vars, go to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Conversion]** &gt; **[!UICONTROL List Variables]** .

**구현 예제** {#section_564AFE6A2F524BFEB372EC0F7FEBA656}

다음의 각 값은 쉼표를 구분 기호로 사용합니다.

**목록 변수 내 단일 값 정의:**

```js
s.list1="Cat";
```

**여러 값 전달:**

```js
s.list2="Tabby,Persian,Siamese"; 
s.list1="Product 1,Product 2,Product 3";
```

**매출에 대한 목록 변수의 기여:**

```js
//Define this code on the landing page: 
s.list3="Top Banner Ad,Side Bar Ad,Internal Campaign 1"; 
 
//Have these variables fire on the purchase confirmation page: 
s.products=";Kitten;1;50" 
s.events="purchase";
```

이 결과는 각각 매출이 $50인 세 개의 라인 항목을 표시합니다. (위쪽 배너 광고, 측면 배너 광고, 내부 캠페인 1.) 이 보고서의 합계에서는 매출 중복을 제거하므로 합계도 $50으로 표시됩니다.

**한 번 당문 동안 여러 번 설정된 목록 변수의 매출에 대한 기여:**

**할당**: 전체

**만료**: 방문

<table id="table_09E1879B44624A858555449E2DC74E69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 페이지 </th> 
   <th colname="col2" class="entry"> s.list1 </th> 
   <th colname="col3" class="entry"> s.events/s.products </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 페이지 1 </td> 
   <td colname="col2"> <code> s.list1=”value1,value2,value3”; </code> </td> 
   <td colname="col3"> (설정되지 않음) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 2 </td> 
   <td colname="col2"> <code> s.list1=”value4,value5,value6”; </code> </td> 
   <td colname="col3"> <p> <code> s.events=”purchase”; </code> </p> <p> <code> s.products=”;product;1;200” </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**결과**: 방문 동안 어느 시점에서 list var1에 설정된 모든 값(value1,value2,value3,value4,value5,value6)은 이 구매에 대해 전체 크레딧을 받습니다.

## maxDelay {#concept_B355038C3B094BB68C0DC6C80F9FE5B0}

s.maxDelay 변수는 DFA 호스트를 접속할 때의 시간 초과 제한 시간을 결정하기 위해 Genesis DFA 통합에서 주로 사용합니다. Adobe가 변수에 지정된 시간 설정 내에 DFA 서버의 응답을 받지 못하면 연결이 끊기고 데이터가 정상적으로 처리됩니다. 각 페이지에서의 DFA 응답 시간에 관심이 있다면 이 변수를 구현하십시오. 최적의 시간 초과 제한 시간을 결정하려면 이 값으로 실험해 보는 것이 좋습니다.

<!-- 

maxDelay.xml

 -->

**구현 예**

```
s.maxDelay="750";
```

**속성**

* 이 변수는 사이트에 구현된 JavaScript를 통해 채워진 선택 사항 이벤트 지표입니다.
* DFA 호스트가 주어진 시간 내에 응답하지 않을 경우, [시간 초과]에 지정된 이벤트가 실행됩니다(Genesis 통합 마법사를 통해 지정됨).
* 이 변수에는 숫자 값만 포함할 수 있습니다.
* 지정된 시간의 크기는 밀리초 단위로 측정됩니다.
* 대기 시간을 늘리면 더 많은 DFA 데이터가 모이지만, Analytics 히트 데이터를 잃을 위험도 늘어납니다.

   Losing Analytics hit data would occur when the user navigates away from the page during the *`s.maxDelay`* period.

* 대기 시간을 줄이면 Analytics 히트 데이터를 잃을 위험은 낮아지지만, 히트 데이터로 전송된 DFA 데이터의 양이 줄어들 수 있습니다.

   Losing DFA integration data would occur when the *`s.maxDelay`* period does not accommodate enough time for the DFA host to respond.

>[!NOTE]
>
>Adobe는 DFA 응답 시간을 제어하지 않습니다. 최대 지연 시간을 합리적인 시간 범위로 올린 후에도 문제가 지속되는 경우에는, 조직의 DFA 계정 관리자에게 문의하십시오.

## mediaLength {#concept_F52B1670122C4461824223E525307060}

 변수는 재생되는 미디어의 전체 길이를 지정합니다.

<!-- 

mediaLength.xml

 -->

<table id="table_B1AE8A9DF9D545C2965CDB2DB6C2969B"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 전체 pev3 요청에 대한 최대 크기 없음 - 크기는 브라우저의 URL 길이 제한으로 제한됩니다. </td> 
   <td> pev3 </td> 
   <td> 비디오 사용 시간; <p>본 비디오 세그먼트 </p> </td> 
   <td> 없음 </td> 
  </tr> 
 </tbody> 
</table>

**구문 및 가능한 값** {#section_FEC1B01FDD234ACEB63C0558BEEB5CBC}

** autoTrack 메서드: **

[!UICONTROL s.Media.autoTrack]을 사용하는 경우에는, [!UICONTROL mediaLength] 변수를 명시적으로 구현할 필요가 없습니다. JavaScript용 AppMeasurement 코드에 의해 자동으로 결정됩니다.

**수동 추적 메서드:**

구문:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**예** {#section_048B2D31BB584647A5D335AE94E5A599}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3= [Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**함정, 질문 및 팁** {#section_1CEDC78FEF4940E9BC02A2AF1EE2FB01}

* 플레이어를 [!UICONTROL s.Media.autoTrack] = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.
* [!UICONTROL autoTrack]을 사용하여 추적하는 경우가 아니라면, 반드시 길이를 초 단위로 설정해야 합니다.

## mediaName {#concept_A4CB1782DE244C23BA6CBB5E806DDE6A}

이 변수는 비디오나 미디어 항목의 이름을 지정합니다.

<!-- 

mediaName.xml

 -->

[!UICONTROL 데이터 삽입 API] 및 [!UICONTROL 데이터 소스 완전 처리]를 통해서만 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 64KB | pev3 | 비디오; 다음 비디오 흐름; 이전 비디오 흐름; 본 비디오 세그먼트; 비디오 사용 시간 | 없음 |

**구문 및 가능한 값** {#section_F97A2253BBD24FEBBC225F233A319F5D}

**autoTrack 메서드:**

[!UICONTROL s.Media.autoTrack]을 사용하는 경우, *`mediaName`*&#x200B;변수를 명시적으로 구현할 필요가 없습니다. JavaScript용 AppMeasurement 코드에 의해 자동으로 결정됩니다.

**수동 추적 메서드:**

구문:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName) 
```

```js
s.Media.play(mediaName,mediaOffset)
```

```js
s.Media.stop(mediaName,mediaOffset)
```

```js
s.Media.close(mediaName)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
s.Media.close("de_bofr_1045Making_400k")
```

**예** {#section_4B9584265B1A47289818141B2A88021D}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
s.Media.close("de_bofr_1045Making_400k")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 Values: 
  pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 
  11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32  
  
```

**함정, 질문 및 팁** {#section_941A445BB52E4063B0F6920E61BB90DE}

* 플레이어를 [!UICONTROL s.Media.autoTrack] = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.
* 이 변수는 VARCHAR(100)와는 대조적으로 mySQL TEXT 변수로 저장됩니다.

## mediaPlayer {#concept_1932756C093B4B2FBA0484E5A58EF927}

이 변수는 비디오나 미디어 항목을 사용하는 데 사용되는 플레이어를 지정합니다.

<!-- 

mediaPlayer.xml

 -->

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | pev3 | 비디오 플레이어 | 없음 |

**구문 및 가능한 값** {#section_EAA55A3A45B5405F903E3BE6ACAB143F}

**autoTrack 메서드:**

```js
s.Media.playerName = "My Custom Player Name"  //configure player name in global JavaScript or ActionSource
```

**수동 추적 메서드:**

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**예** {#section_64967E1333D542CCB6CF62F0A1E0EF88}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers] 
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**함정, 질문 및 팁** {#section_0020E031338F4A4880B9AC5B9A85BEF5}

플레이어를 s.Media.autoTrack = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.

## mediaSession {#concept_19E6C850C3244CB6973140709BDCB0B9}

이 변수는 사용되는 비디오나 미디어 자산의 세그먼트를 지정합니다.

<!-- 

mediaSession.xml

 -->

<table id="table_8681473270FE44DFBBCCC0FBA6737104"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 255바이트 </td> 
   <td> pev3 </td> 
   <td> 비디오 사용 시간 <p>본 비디오 세그먼트 </p> </td> 
   <td> 없음 </td> 
  </tr> 
 </tbody> 
</table>

**구문 및 가능한 값** {#section_9A63266633C4427CB4A6549E4D887B85}

**autoTrack 메서드:**

[!UICONTROL s.Media.autoTrack]을 사용하는 경우, *`mediaName`*&#x200B;을 명시적으로 구현할 필요가 없습니다. JavaScript용 AppMeasurement 코드에 의해 자동으로 결정됩니다.

**수동 추적 메서드:**

구문:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName) 
```

```js
s.Media.play(mediaName,mediaOffset)
```

```js
s.Media.stop(mediaName,mediaOffset)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

**예** {#section_3446EC37E017407FA3F43C9BDAEA0B85}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32 
```

**함정, 질문 및 팁** {#section_1BCEB037AB724B6EBE87420BD3604B88}

플레이어를 [!UICONTROL s.Media.autoTrack] = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.

## Media.trackEvents {#concept_B1C5FF6C437949EBA5D52040AC6BB6D9}

 변수는 미디어 히트와 함께 전송해야 하는 이벤트를 식별합니다.

<!-- 

media_trackEvents.xml

 -->

이 변수는 JavaScript와 [!UICONTROL ActionSource]에서만 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | s.Media.trackEvents="None" |

**구문 및 가능한 값** {#section_66A978EF56914BEAAE73359A268A1B4A}

event1이나 purchase와 같은 이벤트 이름

**예** {#section_140A55D80EA24011954F9383CF312237}

```js
s.Media.trackEvents=”event1,purchase”
```

**함정, 질문 및 팁** {#section_030B11C64EE84D46A85CA550DB732D28}

이 변수가 채워질 때마다 반드시 [!UICONTROL trackVars]를 events로 채우십시오.

## Media.trackVars {#concept_4350CA9A892148AE93C8133AB3B4BEA4}

 변수는 미디어 히트와 함께 전송해야 하는 변수를 식별합니다.

<!-- 

media_trackVars.xml

 -->

이 변수는 JavaScript와 [!UICONTROL ActionSource]에서만 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | s.Media.trackVars="None" |

**구문 및 가능한 값** {#section_7374684A7EB34AE685E8C40A66CFD289}

[!UICONTROL Propn]*`eVarN`**`events`*, 등의 *`channel`*&#x200B;변수 이름.

**예** {#section_48653222ABA14AB0A3C4471659971FAA}

```js
s.Media.trackVars=”prop2,events,eVar3”
```

**함정, 질문 및 팁** {#section_615AE1B696124B00B78F651B03813EAB}

* [!UICONTROL trackVars]에 eVar3이 지정되어 있어도, 미디어 히트와 함께 전송됩니다.

## mobile {#concept_0CEE045F57B444138C0EAA015FC7EA70}

 변수는 쿠키와 구독자 ID가 방문을 식별하는 데 사용되는 순서를 제어합니다.

<!-- 

mobile.xml

 -->

[모바일 네트워크 프로토콜을 참조하십시오](../../../implement/js-implementation/c-additional-libraries/network-protocols.md#concept_2425537FC9CB45DD868B5FA2298B6CAC).

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | 이미지 URL의 경로에 있는 /5/ 또는 /1/ | N/A | 없음 |

**구문 및 가능한 값** {#section_7F1C58090C454882BA9D3D66C9263A76}

```js
s.mobile="any_string" //subscriber id used first, produces /5/ in path of image url 
s.mobile=""  // if set to an empty string or not set at all, cookies used first, produces /1/ in path of image url 
```

**함정, 질문 및 팁** {#section_06CD5CB4EF1E4B9FBE3B9D1F18AAFA30}

Use cross-visitor identification to mitigate possible spikes in visitor traffic when using the *`s.mobile`* variable with the JavaScript cookie implementation.

## pageName {#concept_5827B499DAC34B5D8445F9D9140CC328}

 변수에는 사이트에 있는 각 페이지의 이름이 들어 있습니다.

<!-- 

pageName.xml

 -->

<table id="table_0D09BAEC2FFD43F7905ED3649B3F8E05"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 100바이트 </td> 
   <td> pageName </td> 
   <td> <p>페이지 </p> <p>경로 </p> </td> 
   <td> 페이지 URL </td> 
  </tr> 
 </tbody> 
</table>

the *`pageName`*&#x200B;변수는 비즈니스 사용자가 인식하는 값으로 채워야 합니다. In most cases the *`pageName`* value is not the URL or the path to the file. Common *`pageName`* values include names such as "Home Page," "Checkout," "Purchase Thank you," or "Registration."

줄바꿈, -em이나 -en 대시 또는 모든 HTML 문자가 페이지 이름과 다른 변수에 나타나지 않도록 주의하십시오. 일부 브라우저에서는 다른 브라우저에서 보내지 않는 줄바꿈 문자를 보내 보기에는 동일한 두 개의 페이지 이름 사이에서 Analytics의 데이터가 분리되기도 합니다. 많은 워드 프로세서 및 이메일 클라이언트는 하이픈을 입력하면 자동으로 -en이나 -em 대시로 변환합니다. -en 및 -em 대시는 Analytics 변수에 사용할 수 없는 문자(127개가 넘는 코드의 ASCII 문자)이므로, Analytics는 잘못된 문자가 들어 있는 페이지 이름을 기록하지 않고 대신 URL을 보여 줍니다.

If *`pageName`* is left blank, the URL is used to represent the page name. Leaving *`pageName`* blank is often problematic because the URL may not always be the same for a page `www.mysite.com` and `mysite.com` are the same page with different URLs).

**구문 및 가능한 값** {#section_7A61EE70F1A84D26B414404998C84BA8}

The *`pageName`* variable should contain a useful identifier for business users of Analytics.

```js
s.pageName="page_name"
```

There are no limitations on *`pageName`* outside of the standard variable limitations.

**예** {#section_8BB4F86F84E246A08B72DEC47FFC0765}

```js
s.pageName="Search Results" 
```

```js
s.pageName="Standard Offer List"
```

**구성 설정** {#section_58CBC68C805344A999EB47455FEBA8D5}

관리자는 [!UICONTROL 페이지 명명] 도구로 Analytics에서 표시되는 페이지 이름을 변경할 수 있지만, 이 도구를 사용하는 것은 위험할 수 있으며 보고서에 부정적인 영향을 줄 수 있습니다. 따라서 [!UICONTROL 페이지 명명] 도구를 사용하려면 그 전에 Adobe 고객 지원 센터에 문의하십시오.

**함정, 질문 및 팁** {#section_BB41DC9682C34385B9CAA80D5257C113}

Make sure the *`pageName`* doesn't contain illegal characters.

## pageType {#concept_F67870238EF74491B5D3909A33CDB985}

 변수는 404 [페이지가 없습니다] 오류 페이지를 지정하는 데만 사용됩니다.

<!-- 

pageType.xml

 -->

<table id="table_0492B136E9D14070A6CA49ED534BCA4C"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 20바이트 </td> 
   <td> pageType </td> 
   <td> 경로 &gt; 페이지 &gt; 페이지 <p>발견되지 않음 </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

the *`pageType`* 변수는 404 오류 페이지가 표시되면 잘못된 URL을 캡처하여 사용자 지정 사이트에서 더 이상 유효하지 않은 끊어진 링크 및 경로를 빨리 찾게 해줍니다. Set up the *`pageType`* variable on the error page exactly as shown below.

404 오류 페이지에 페이지 이름 변수를 사용하지 마십시오. 404 오류 페이지에는 *`pageType`* 변수만 사용됩니다.

대부분의 경우 404 오류 페이지는 하드 코딩된 정적 페이지입니다. 이러한 경우 .JS 파일 참조를 적절한 글로벌 또는 상대적 경로/디렉토리로 설정하는 것이 중요합니다.

**구문 및 가능한 값** {#section_C1C59968226446559B05F6EE7374D525}

The only allowable value of *`pageType`* is "errorPage" as shown below.

```js
s.pageType="errorPage"
```

**예** {#section_6CE22FCB835B4A19B633B7F67E73A115}

```js
s.pageType="errorPage"
```

**구성 설정** {#section_3B304A6D3A6C48F2BE90B4DA92A39DDB}

없음

**함정, 질문 및 팁** {#section_943681AB01FE47BEAC72E93CB60C53C8}

To capture other server-side errors (such as 500 errors), use a prop to capture the error message and put "`500 Error: <URL>`" where `<URL>` is the URL requested, in the *`pageName`* variable. 이 방법을 따르면 [!UICONTROL 경로 지정] 보고서를 사용하여 사용자가 500 오류를 생성하는 경로를 알 수 있습니다. Prop은 서버에 의해 지정되는 오류 메시지에 대해 설명합니다.

## pageUrl {#concept_A15F710CD0174297A2286BF3E7452113}

 변수는 페이지의 실제 URL을 무시합니다.

<!-- 

pageURL.xml

 -->

페이지의 URL이 Analytics에 보고할 URL과 다른 경우가 드물게 나타납니다.

<table id="table_D4DC6B476FFD4BEEB36A5C6B2D026255"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 제한 없음* </td> 
   <td> <p>G </p> </td> 
   <td> 트래픽 &gt; 세그먼테이션 &gt; 가장 방문 빈도가 높은 페이지 경로 </td> 
   <td> 페이지 URL </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Although Adobe allows *`pageURL`* values up to 64k, some browsers impose a size limit on the URL of image requests. To prevent truncation of other data, page URLs longer than 255 bytes are split, with the first 255 bytes appearing in the `g=` parameter, with the remaining bytes appearing later in the query sting in the `-g=` query parameter.

**구문 및 가능한 값** {#section_22AF3BF7C2F743549967B0C760A095C0}

*`pageURL`* 변수는 유효한 프로토콜이 있는 유효한 URL 이어야 합니다. 도메인을 보고서에 채우려면 먼저 강제로 소문자로 표시해야 하며 Analytics 설정에 따라 쿼리 문자열이 제거될 수 있습니다.

```js
s.pageURL="proto://domain/path?query_string"
```

페이지 URL에는 URL 호환 문자만 허용됩니다.

>[!NOTE]
>
>It is strongly advised that you contact your Adobe consultant or Customer Care before using the *`pageURL`* variable for custom purposes.

**예** {#section_45158FDA3F8F4574BDEB5CBC9F7E6C97}

```js
s.pageURL="https://mysite.com/home.jsp?id=1224" 
```

```js
s.pageURL="https://www.mysite.com/"
```

**구성 설정** {#section_A8F77DAD88164528ACC5C16C066B47DF}

없음

## plugins {#concept_B570F04FEDA34EB7A9826687FE633953}

 변수는 Netscape 및 Mozilla 기반 브라우저에서 브라우저에 설치된 플러그인을 나열합니다.

<!-- 

plugins.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| p | 인식된 플러그인 | IE Tab Plug-in;QuickTime Plug-in 7.1.6;Mozilla Default Plug-in;iTunes Application Detector;Adobe Acrobat;ActiveTouch General Plugin Container;Shockwave Flash;Microsoft Office 2003;Java(TM) Platform SE 6 U1;Windows Media Player Plug-in Dynamic Link Library;Microsoft® DRM; | 트래픽 &gt; 기술 &gt; 플러그인 |

## products {#concept_A4007F6307E4419DAA65E1668A8FEBA2}

 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적). 제품은 일반적으로 장바구니 이벤트나 이벤트와 연결하여 설정됩니다.

<!-- 

products.xml

 -->

>[!IMPORTANT]
>
>In January of 2016, we updated the logic that sets the *`prodView`* event automatically, which happens when there is a *`product`* but no *`event`*. 이 업데이트로 인해 *`prodView`이벤트가 늘어날 수 있습니다.* *`prodViews`*&#x200B;는 다음과 같은 경우에만 늘어납니다.
>
>1. The events variable contains nothing but an unrecognized event, such as *`shoppingCart`* or *`cart`*, which are not valid events.
   >
   >
1. *`products`변수가 비어 있지 않습니다.*
>
>
A possible side effect is that merchandising eVars triggered by *`prodView`* events could be associated with an empty *`product`*, but only if the *`product list`* contains only an invalid product (such as a semicolon with no product listed).

*`products`* 변수는 사용자가 사이트에서 제품과 상호 작용하는 방식을 추적합니다. 예를 들어 products 변수는 몇 번이나 제품을 보았는지, 장바구니에 추가했는지, 체크아웃했는지 및 구입했는지를 추적할 수 있습니다. 또한 사이트에 있는 머천다이징 카테고리의 상대적 효과를 추적할 수도 있습니다. 다음은 products 변수를 사용하는 일반적인 시나리오입니다.

the *`products`* 변수는 항상 성공 이벤트와 함께 설정해야 합니다.

<table id="table_D5A11AFDDD364D0993D387906343DDF3"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><span class="wintitle"> " products </span>"문자열의 크기는 최대 64 K 입니다. </p> </td> 
   <td> products </td> 
   <td> 제품 <p>카테고리(선택 사항) </p> <p>매출(선택 사항) </p> <p>판매량(선택 사항) </p> <p>사용자 지정 이벤트(선택 사항) </p> <p>eVar(선택 사항) </p> </td> 
   <td> " " </td> 
  </tr> 
 </tbody> 
</table>

**구문** {#section_ABA3682985E540E6AA67A510176CCFFC}

```js
"Category;Product;Quantity;Price;eventN=X[|eventN2=X2];eVarN=merch_category[|eVarN2=merch_category2]"
```

| 필드 | 정의 |
|---|---|
| 카테고리 | 연결된 제품 카테고리가 들어 있습니다. 버전 15에서는, 버전 14에 있는 제한을 수정하는 제품을 여러 카테고리와 연결할 수 있습니다. 이전에 제품 카테고리를 기록하지 않은 경우, 버전 15에 있는 보고서 세트에 대해 이 필드를 채우는 것이 좋습니다. |
| 제품 | (필수) 제품을 추적하는 데 사용되는 식별자. 이 식별자는 [!UICONTROL 제품] 보고서를 채우는 데 사용됩니다. 반드시 체크아웃 프로세스를 통해 동일한 식별자를 사용하십시오. |
| 수량 | 구매된 개수. 이 필드를 기록하려면 [!UICONTROL 구매] 이벤트가 설정되어 있어야 합니다. |
| 가격 | 개별 가격이 아니라, 구매한 총 수량의 복합 비용(판매량 x 개별 단위 가격)을 나타냅니다. 이 필드를 기록하려면 [!UICONTROL 구매] 이벤트가 설정되어 있어야 합니다. |
| 이벤트 | 지정된 제품과 연결된 통화 이벤트. [제품별 통화 이벤트](../../../implement/js-implementation/c-variables/page-variables.md#section_F814DF053C0D463A97DA039E6323720C) 및 [주문 범위 통화 이벤트](../../../implement/js-implementation/c-variables/page-variables.md#section_D06F76A8A1F8498EB1BD6D8C8B9D5BE0)를 참조하십시오. |
| eVar | 특정 제품과 연결된 머천다이징 eVar 값. [머천다이징 변수](/help/components/c-variables/c-merch-variables/var-merchandising.md)를 참조하십시오. |

에 포함된 값은 *`products`*&#x200B;변수에 포함된 값은 기록하고 있는 이벤트 유형을 기반으로 합니다. 카테고리/제품 구분 기호(;)는 카테고리 생략 시 자리 표시자로 필요합니다. 이 페이지의 예에서 보듯이, 다른 구분 기호는 포함하고 있는 매개 변수를 구분하는 데 필요할 경우에만 필요합니다.

**비구매 이벤트 관련 products 설정** {#section_D5E689D4AAE941EC851CA9B98328A4DE}

*`products`* 이 변수는 성공 이벤트와 함께 설정해야 합니다.

**구매 이벤트 관련 products 설정** {#section_618AAC96E7B541A7AABAA028E5F4E5C3}

*`purchase`* 이벤트는 최종 확인 ("감사합니다! ") 설정해야 합니다. 제품 이름, 카테고리, 수량 및 가격은 모두 *`products`* 변수. *`purchaseID`* 변수가 필수는 아니지만 중복 주문을 방지하는 것이 좋습니다.

**제품별 통화 이벤트** {#section_F814DF053C0D463A97DA039E6323720C}

If a currency event receives a value in the *`products`* variable instead of the events variable, it applies only to that value. 제품별 할인, 제품 배송 및 유사한 값을 추적하는 데 유용합니다. 예를 들어, 이벤트 1을 제품 배송을 추적하도록 구성한 경우, 배송비가 "4.50"인 제품이 다음과 유사하게 나타납니다.

```js
s.events="event1" 
s.products="Footwear;Running Shoes;1;99.99;event1=4.50"
```

이 예에서, 4.50이라는 값은 "Running Shoes" 제품과 바로 연결되어 있습니다. 제품 보고서에 event1을 추가하면, "Running Shoes" 라인 항목에 대해 "4.50"가 나열된 것을 보게 됩니다. 가격과 유사하게, 이 값은 나열된 수량에 대한 합계를 반영해야 합니다. 배송비가 각각 4.50인 항목이 2개가 있을 경우, event1은 "9.00"이어야 합니다.

**주문 범위 통화 이벤트** {#section_D06F76A8A1F8498EB1BD6D8C8B9D5BE0}

If a currency event receives a value in the events list instead of the *`products`* variable, it applies to all products in the *`products`* variable. 이는 제품 가격을 수정하거나 제품 목록에서 별도로 추적할 필요 없이 주문 전체에 대한 할인, 배송 및 유사한 값을 추적하는 데 유용합니다.

예를 들어, event10이 주문 전체에 대한 할인을 포함하도록 구성한 경우 10% 할인된 구매는 다음과 같이 표시될 수 있습니다.

```js
s.events="purchase,event10=9.95" 
s.products="Footwear;Running Shoes;1;69.95,Running Essentials;Running Socks;10;29.50" 
s.purchaseID="1234567890"
```

통화 이벤트 보고서에서 보고서 총계는 각 제품에 대한 이벤트 값의 합이 아닌 중복 제거된 이벤트 총계(보고 기간 동안의 총 할인 금액)를 나타냅니다. 예를 들어, "Running Shoes"와 "Running Socks"에 모두 "9.95"가 나열되고, 합계는 "9.95"가 됩니다.

>[!NOTE]
>
>*`products`* 변수와 *`events`* 변수에 동일한 숫자/통화 이벤트에 대한 값이 지정된 경우의 값이 *`events`* 사용됩니다.

**함정, 질문 및 팁** {#section_D38FD0B79C0347B9AB4CF1632183DA2E}

* *`products`* 이 변수는 [!UICONTROL 항상 성공] 이벤트와 함께 설정해야 합니다 (이벤트). [!UICONTROL 성공] 이벤트를 지정하지 않은 경우 기본 이벤트는 [!UICONTROL prodView]입니다.

* 제품을 채우려면 먼저 제품 및 카테고리 이름에서 모든 쉼표와 세미콜론을 제거하십시오.
* 모든 HTML 문자(등록 기호, 상표 등)를 제거하십시오.
* 가격에서 통화 기호($)를 제거하십시오.

**예** {#section_FCC6EF43D3534ECB9A95CDB05820F564}

<table id="table_6F1334E73CE048A5AC0CC28B561C1B2D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <code> s.products=”Category;ABC123” </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products=”Category2;ABC123,;ABC456” </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products=”Category3;ABC123;1;10” </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products=”Category;ABC123;1;10,;ABC456;2;19.98” </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1” </code> <p> <code> s.products="Category;ABC123;;;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99,;ABC123;2;19.98;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1,event2” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1,event2” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1,event2” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping|evar2=3 Stars" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1,event2” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping, ;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1,event2,event3” </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events=”event1,event2,event3=9.95” </code> <p> <code> s.products="Category;ABC123;,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## propN {#concept_0F10FA2DE69B4029A31EA5E9313AA254}

속성([!UICONTROL prop]) 변수는 [!UICONTROL 트래픽 모듈] 내에서 사용자 지정 보고서를 작성하는 데 사용됩니다.

<!-- 

propN.xml

 -->

props 변수는 경로 지정 보고서용으로 또는 상관 관계 보고서에서 카운터(페이지 보기가 전송되는 횟수 카운트)로 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | c1 - c75 | 사용자 지정 트래픽 | "" |

**구문 및 가능한 값** {#section_4D3013AF2979426B9589CA2BB9D254CD}

```js
s.propN="value"
```

[!UICONTROL 속성] 변수에는 표준 변수 제한 외에 제한이 없습니다.

**예** {#section_FFBB916DA9F44B668D5FAB7C511F6182}

```js
s.prop2="editorial" 
```

```js
s.prop15="toy category"
```

**구성 설정** {#section_25FDEB6ECA8242A2A44EE540C083078A}

[!UICONTROL prop] 변수의 [!UICONTROL 방문], [!UICONTROL 방문자] 및 [!UICONTROL 경로] 지표 표시에 대해서는 Adobe 고객 지원 센터에 문의하십시오.

## purchaseID {#concept_21937434E63F413CB469007623B933AE}

보고에서 주문이 여러 번 카운트되지 않도록 하는 데 사용됩니다.

<!-- 

purchaseID.xml

 -->

Whenever the [!UICONTROL purchase] event is used on your site, you should use the *`purchaseID`* variable.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 20바이트 | purchaseID | 전환 &gt; 구매 &gt; 매출 전환 | "" |

방문자가 사이트에서 항목을 구매하면 *`purchaseID`*&#x200B;가, [!UICONTROL 구매] 이벤트가 실행된 같은 곳의 "감사합니다" 페이지에서 채워집니다. If the *`purchaseID`* is populated, the products on the "Thank You" page are counted only once per *`purchaseID`*. 사이트를 방문하는 많은 방문자들이 자신만의 목적을 위해 "감사합니다" 또는 "확인 페이지"를 저장하므로 이것은 매우 중요합니다. the *`purchaseID`* 는 페이지를 볼 때마다 구매를 카운트하지 않도록 해줍니다.

In addition to keeping the purchase data from being counted twice, the *`purchaseID`*, when used, keeps all conversion data from being double counted in reports.

**구문 및 가능한 값** {#section_E352CE2370D54BA69A368E1F63A9C32D}

```js
s.purchaseID="unique_id"
```

The *`purchaseID`* must be 20 characters or fewer, and be standard ASCII.

**예** {#section_60A5C1EAF42F4611898CD6A4F4CF5A28}

```js
s.purchaseID="11223344" 
s.purchaseID="a8g784hjq1mnp3"
```

**구성 설정** {#section_1808631C96674380BF9C4A6D9A2C568E}

없음

**함정, 질문 및 팁** {#section_F5D010F234ED43F19AD1FCD2CD64E060}

*`purchaseID`* 이 변수를 사용하면 페이지에서 모든 전환 변수가 보고서에서 한 번만 카운트됩니다.

## referrer {#concept_3D8E6A5D30DC4D92982EFA34D4C7F81B}

 변수는 손실된 레퍼러 정보를 복원하는 데 사용할 수 있습니다.

<!-- 

referrer.xml

 -->

서버 측 및 JavaScript 리디렉션을 사용하여 방문자를 적절한 위치로 보내는 경우가 많습니다. 그러나 브라우저가 리디렉션되면 원래의 참조 URL이 손실됩니다. 

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 255바이트 | R | 트래픽 &gt; 검색 방법 전환 &gt; 검색 방법 | document.referrer |

많은 회사에서는 자신들의 웹 사이트 전체에서 리디렉션을 사용합니다. 예를 들어 방문자가 리디렉션을 통해 검색 엔진의 유료 검색 결과로 이동할 수도 있습니다. 브라우저가 리디렉션되면 레퍼러가 손실되는 경우가 많습니다. the *`referrer`* 변수는 리디렉션 후 첫 번째 페이지에서 원래 *`referrer`* 값을 복원하는 데 사용할 수 있습니다. The *`referrer`* may be populated server-side, or via JavaScript from the query string.

Analytics가 레퍼러를 기록하려면 "형식을 제대로 지정"해야 하며, 이것은 프로토콜과 적절한 위치로 표준 URL 형식을 따라야 함을 의미합니다.

**구문 및 가능한 값** {#section_A0365D76789C4F4A959E81FE5A9D491D}

```js
s.referrer="URL"
```

 *`referrer`*. 문자열이 URL 인코딩되어 있는지(공백 없음) 확인하십시오.

**예** {#section_86FB1577670C4AA18BF3718F0832FCD4}

```js
s.referrer="https://www.google.com/search?q=search+string" 
s.referrer=<%=referrerVar%> // populated server-side  
if(s.getQueryParam('ref') 
s.referrer=s.getQueryParam('ref') 
```

**구성 설정** {#section_7AAEF28A7CBC446984F32C0659EFBF8D}

없음

**함정, 질문 및 팁** {#section_B42BF7FBA1094FF9805707FEA810CFE1}

The *`referrer`* must look like a standard URL and include a protocol.

## resolution {#concept_8CBDDBE710744A3AA09E6B1E1519BF30}

 변수는 웹 페이지를 보는 방문자의 모니터 해상도를 가리킵니다.

<!-- 

resolution.xml

 -->

This variable is populated after the page code and before *`doPlugins`* is run.

>[!NOTE]
>
>이 변수는 읽기 및 절대 설정되지 않아야 합니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| s | WxH | 1680 x 1050 | 트래픽 &gt; 기술 &gt; 모니터 해상도 |

## s_objectID {#concept_48B50DE6B7E546EBB4D187033F1CAF2B}

The  variable is a global variable that should be set in the [!UICONTROL onClick] event of a link.

<!-- 

s_objectID.xml

 -->

By creating a unique object ID for a link or link location on a page, you can either improve visitor activity tracking or use [!UICONTROL Activity Map] to report on a link type or location, rather than the link URL.

>[!NOTE]
>
>A trailing semicolon (;) is required when using s_objectID with [Activity Map](https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/activitymap-link-tracking-use-case.html).

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | OID | [!UICONTROL Activity Map], [!UICONTROL clickmap] | 클릭한 링크의 절대 URL |

일반적으로 *`s_objectID`*:

* 하루 동안 자주 변하는 방문자 활동을 집계하기 위해
* To separate link activity that [!UICONTROL Activity Map] combines.
* To improve the accuracy of [!UICONTROL Activity Map] data reporting.

**매우 동적인 링크에 대한 클릭 집계** {#section_BA730A0393B149DDBCAA272C3C23A1C5}

If your site is highly dynamic, and links on some pages change throughout the day, *`s_objectID`* may used to identify the location of a link on the page. If *`s_objectID`* is set to "top left 1" or "top left 2," which represents the first link in the top left of the page for example, then all links that appear in that location (or that have *`s_objectID`* set to the same value) are reported together with visitor click map. If you don't use *`s_objectID`*, you see the number of times that a specific link was clicked, but you lose insight into how all the other links in that location were used by visitors to your site.

**결합된 클릭 구분** {#section_1AE91FB8A2D3423CBE064ACF02FEEA47}

If the *`pageName`* variable on your site is used to show the section or template a visitor is viewing, rather than the specific page the visitor is viewing, you may want to use *`s_objectID`* to separate links that appear on multiple versions of that page template. 예를 들어 사이트에 있는 모든 제품에 대한 템플릿 페이지가 있는 경우, 모든 페이지의 해당 템플릿에서 홈 페이지와 검색 상자에 연결된 링크가 있을 수 있습니다. 이러한 링크가 개별 제품 기반(템플릿 기반이 아닌)으로 어떻게 사용되는지를 알려면 *`s_objectID`*&#x200B;를 "prod 123789 home page" 또는 "prod 123789 search"와 같이, 제품별 값으로 채우면 됩니다. Once completed, [!UICONTROL Activity Map] reports on those links at an individual product basis.

**[!UICONTROL 활동 맵]정확도 개선**{#section_08B3406821294DCCABEEB99C90CF5C52}

경우에 따라 Internet Explorer, Firefox, Netscape, Opera 및 Safari 이외의 브라우저는 보고되지 않습니다. 이런 경우가 흔하지는 않지만, 일부 클릭 수와 기타 지표가 이 문제와 관련됩니다. Use *`s_objectID`* within links to uniquely identify the addresses the browser reporting issue. 다음은 링크가 *`s_objectID`*:

```js
<a href="/art.jsp?id=559" onClick="s_objectID='top left 1';">Article 559</a> 
<a href="/home.jsp" onClick="s_objectID='prod 123789 home page';">Home</a> 
```

**구문 및 가능한 값** {#section_85841DF9F06A4680953D9B2A884A1A5A}

s_objectID에는 모든 텍스트 식별자가 들어 있을 수 있습니다.

```js
s_objectID="unique_id" 
```

표준 변수 제한 외에는 *`s_objectID`* 에 적용되는 제한이 없습니다.

**예** {#section_33F119D532CA4ACAA3426253C42030BB}

```js
s_objectID="top left 2" 
```

```js
s_objectID="prod 123789 search"
```

**구성 설정** {#section_95396657D55B41ECB66B83D0534EA827}

없음

## server {#concept_BF77952603BA454BAFC9A0A81D06A7D2}

 변수는 웹 페이지의 도메인(방문자가 도착한 도메인 표시) 또는 페이지를 제공하는 서버(로드 밸런싱 빠른 참조용)를 보여주는 데 사용됩니다.

<!-- 

server.xml

 -->

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | server | 서버 | "" |

사이트에 동일한 컨텐츠를 제공하는 도메인이 두 개 이상 있을 경우, *`server`*&#x200B;변수를 사용하여 그 도메인들 중 방문자가 사용하고 있는 도메인을 추적할 수 있습니다. 다음 JavaScript는 페이지의 도메인을 server 변수에 채웁니다.

```js
s.server=window.location.hostname
```

server 변수를 사용하여 빠른 로드 밸런싱 지침을 제공하는 경우, 서버 이름이나 번호를 server 변수에 삽입하십시오. 다음 예를 참조하십시오.

```js
s.server="server 14"
```

[!UICONTROL 가장 방문 빈도가 높은 서버] 보고서를 빠른 로드 밸런싱 참조로 사용할 수는 있지만 이 보고서가 서버 로드에 대한 정확한 척도는 아닙니다. 예를 들어 [뒤로] 단추의 트래픽은 서버 로드를 증가시키지 않지만, 보고서에 표시됩니다. 이 보고서는 이미지나 큰 다운로드를 제공하는 서버를 보여주지 않습니다.

**구문 및 가능한 값** {#section_48E4B9BFEBFF4409A246D86EC0C0FB13}

```js
s.server="server_name"
```

There are no limitations on the *`server`* variable outside of the standard variable limitations.

**예** {#section_78B9EE3C27FB491384869E3D0BD503D6}

```js
s.server="server 18" 
s.server=window.location.hostname 
```

**구성 설정** {#section_969DB379D5BD469FBEE8D505D3000E49}

없음

**함정, 질문 및 팁** {#section_42A28F9B01574F38891D9D54B411D8FE}

*`server`* 이 변수를 사용하여 가장 인기 있는 도메인이나 가장 많은 페이지를 제공하는 서버를 표시할 수 있습니다.

## state {#concept_82295D22888947BF8B1C76182C635C6C}

AND 변수는 전환 변수입니다.

<!-- 

state.xml

 -->

이벤트를 캡처한다는 점은 eVar와 비슷하지만 지속되지 않는다는 점은 eVar와 다릅니다. the *`zip`**`state`* 변수와 변수는 즉시 만료되는 Evar와 같습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 50바이트 | state | 변환 &gt; 방문자 프로필 &gt; 방문자 상태 | "" |

*`state`* AND *`zip`* 변수는 즉시 만료되기 때문에 연결되는 유일한 이벤트는 이벤트가 채워지는 페이지에서 실행되는 이벤트입니다. For example, if you are using *`state`* to compare conversion rates by state, you should populate the *`state`* variable on every page of the checkout process. 전환 사이트의 경우, 청구 주소를 우편번호에 대한 소스로 사용하는 것이 좋지만, 대신 배송 주소를 사용하도록 선택할 수 있습니다(주문에 대해 배송 주소가 하나만 있다고 가정할 경우). 미디어 사이트는 등록이나 광고 클릭스루 추적에 *`zip`* 등록 *`state`* 또는 광고 클릭스루 추적을 수행할 수 있습니다.

**구문 및 가능한 값** {#section_EDD1F5F9EDBC457898E61695F08C1744}

```js
s.state="state"
```

*`state`* 변수에는 특수 값 또는 형식 제한이 적용되지 않습니다. There are no limitations on *`state`* outside of the standard variable limitations.

**예** {#section_D181B163F79A41D199CA4C70765E583F}

```js
s.state="california" 
```

```js
s.state="prince edward island"
```

**구성 설정** {#section_DB0D6DC3F4764AC59C11B10D27D2806C}

없음

**함정, 질문 및 팁** {#section_02F1620D0BB14AA6A838966FDB9A234F}

* Populate *`state`* on every page that a relevant event is fired (such as each page of the checkout process).
* *`zip`* AND *`state`* 변수는 페이지 뷰에서 만료되는 evar 처럼 작동합니다.

## timestamp {#concept_D997A2FF4D134C80A614C0BC7A4D7507}

이 변수를 사용하면 다른 플랫폼용 AppMeasurement 라이브러리와 유사한 히트의 타임스탬프를 사용자 지정할 수 있습니다.

<!-- 

timestamp.xml

 -->

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 4바이트 | 날짜/시간 | 바로 보고되지 않음. | 데이터 수집 서버에 의해 설정됨 |

**구문** {#section_1DF752B1202C4412A301AC7CC10874DF}

```js
s.timestamp="UNIX or ISO-8601 format timestamp"
```

*`timestamp`* 변수는 다음 섹션에 설명된 형식이어야 합니다.

>[!IMPORTANT]
>
>Your report suite must be timestamp-enabled by Customer Care before you can use the *`timestamp`* variable. After timestamp support is enabled, all hits sent to this report suite from JavaScript must have a timestamp manually set (using *`s.timestamp`*) or the hits will not be recorded.
>
>또한 보고서 세트에서 타임스탬프 지원을 활성화하여 오프라인 추적을 지원하는 경우 JavaScript에서 이 보고서 세트로 전송되는 모든 히트에도 *`s.timestamp`*). 타임스탬프가 있는 히트와 타임스탬프가 없는 히트를 같은 보고서 세트로 모두 전송할 수 없습니다.
>
>  [타임스탬프 선택 사항](../../../implement/js-implementation/timestamps-overview.md#concept_1A7DF6F7BDA34467B51A6F61E08BB73F) 설정을 사용하여 타임스탬프가 지정된 데이터와 지정되지 않은 데이터를 동일한 전역 보고서 세트에서 혼합할 수도 있고, 타임스탬프가 지정된 데이터를 모바일 앱에서 전역 보고서 세트에 보낼 수도 있고, 새 보고서 세트를 만들지 않고도 타임스탬프를 적용하도록 앱을 업그레이드할 수도 있습니다.

**타임스탬프 형식** {#section_C12CBCECCD7047D38EF63A5800761CE9}

타임스탬프는 UNIX(1970년 1월 1일 이후 경과한 초) 또는 ISO-8601 형식으로 되어 있어야 하며, 승인된 ISO-8601 형식에 대해 다음 제한 사항이 있습니다.

* 날짜와 시간을 "T"로 구분하여 모두 입력해야 합니다.
* 날짜는 연도, 월, 일을 모두 포함한 정확한 달력 표시 날짜여야 합니다. . 주차와 서수 날짜는 지원되지 않습니다.
* 날짜는 표준 또는 확장 형식(`YYYY-MM-DD` 또는 `YYYYMMDD`)이 될 수 있으나 시간과 분을 포함해야 합니다. Seconds are optional ( `HH:MM`, `HH:MM:SS`, `HHMM`, or `HHMMSS`). 분수 분과 초를 입력할 수 있지만 분수 부분은 무시됩니다.

* An optional time zone can be specified in standard or extended format ( `±HH`, `±HH:MM`, `±HH`, `±HHMM`, or Z)

UNIX 타임스탬프는 계속해서 지원됩니다(1970년 1월 1일 이후 경과한 초).

**예** {#section_FA19C53D70DE4CF2AF259A5B968B84C3}

```js
s.timestamp=Math.round((new Date()).getTime()/1000);
```

```js
s.timestamp="2012-04-20T12:49:31-0700";
```

다음 목록에는 유효한 ISO-8601 형식 타임스탬프의 예가 나와 있습니다.

```
2013-01-01T12:30:05+06:00 
2013-01-01T12:30:05Z 
2013-01-01T12:30:05 
2013-01-01T12:30
```

**구성 설정** {#section_5275D206F2CB4009B3681E8C4457124A}

보고서 세트가 고객 지원 센터에 의한 사용자 지정 타임스탬프를 수락하도록 활성화되어야 이 변수를 사용할 수 있습니다. 사용자 지정 타임스탬프가 활성화되면 보고서 세트로 보내지는 모든 히트에 타임스탬프가 들어 있어야 합니다. 그렇지 않으면 히트가 무시됩니다.

**함정, 질문 및 팁** {#section_EFDE8F67D13C4775A461E0B00D30AFD7}

* 타임스탬프는 모바일 플랫폼에서 오프라인 데이터를 추적하는 데 주로 사용됩니다. 동일한 보고서 세트에서 웹과 오프라인 앱 데이터를 모두 모으고 있지 않다면 사용자 지정 타임스탬프는 보통 비활성화되어 있습니다.
* 오프라인 데이터가 모바일 SDK에서 활성화될 때(기본 설정) 또는 보고서 세트가 타임스탬프가 있는 데이터를 허용하도록 구성되는 때면 언제든지 타임스탬프로 데이터를 기록합니다. 모바일 장치에서 오프라인으로 수집한 데이터는 수집된 지 몇 시간 또는 몇 주 후에 전송될 수 있습니다. 이러한 히트는 타임스탬프가 없는 히트보다 Analytics 플랫폼 내에서 몇 분 또는 몇 시간 더 큐에 올라가 있을 수 있습니다.

   * 아주 최근에 전송된 타임스탬프 데이터의 경우 예상되는 지연 시간은 10~15분입니다.
   * 어제 이후 전송된 타임스탬프 데이터의 경우 예상되는 지연 시간은 약 2시간입니다.
   * 어제 이전에 전송된 타임스탬프 데이터의 경우 지연 증가가 멈추었을 때 최대 15일까지 하루에 약 1시간을 추가합니다.

* 타임스탬프 사용 세션 데이터는 최대 92일 동안 유지됩니다.

## trackingServer {#concept_45EE91B1A99B4A37AFAEF1C0A8A6B02F}

 변수는 자사 쿠키 구현에서 이미지 요청 및 쿠키를 쓰는 도메인을 지정하는 데 사용됩니다.

<!-- 

trackingServer.xml

 -->

비보안 페이지에 사용됩니다. 만약 *`trackingServer`* 가 정의된 경우는 아무것도 2o7.net으로 전송되지 않습니다. If *`trackingServer`* is not defined (and dc is not defined), data goes to 112.2o7.net.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | "" |

Adobe 데이터 센터 목록은 [여기](https://helpx.adobe.com/analytics/kb/determining-data-center.html)에 있습니다.

## trackingServerSecure {#concept_28132A2606E34A2F87BEC9E7ACADC7DD}

 변수는 자사 쿠키 구현에서 이미지 요청 및 쿠키를 쓰는 도메인을 지정하는 데 사용됩니다.

<!-- 

trackingServerSecure.xml

 -->

보안 페이지에 사용됩니다. 만약 *`trackingServerSecure`* 가 정의되지 않은 경우는 SSL 데이터가 *`trackingServer`*.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | "" |

## transactionID {#concept_FBFA55E137E644A2BD97B41E92F6AFEF}

[!UICONTROL 통합 데이터 소스는 트랜잭션 ID를 사용하여 오프라인 데이터를 온라인 트랜잭션(예: 온라인에서 생성된 리드 또는 구매)에 연결합니다.]

<!-- 

transactionID.xml

 -->

Each unique *`transactionID`* sent to Adobe is recorded in preparation for a [!UICONTROL Data Sources] upload of offline information about that transaction. [ 데이터 소스](https://marketing.adobe.com/resources/help/en_US/sc/datasources/)를 참조하십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | xact | n/a | "" |

**거래 ID 저장 공간 활성화**{#section_3EA2C9DC9D4C4F0FBE4AB67981BCB52E}

Before *`transactionID`* values are recorded, [!UICONTROL Transaction ID Storage] must be enabled for the report suite selected in the Report Suite Manager. 이 설정은 다음 위치에 있습니다.

```
Analytics > Admin > Report Suites > Edit Settings > General > General Account Settings.
```

To see whether *`transactionID Storage`* is enabled for a report suite, go to

```
Analytics > Admin > Data Sources > Manage
```

**구문 및 가능한 값** {#section_0C18329203DC45E989DBAE70C0FB4801}

```js
s.transactionID="unique_id"
```

The *`transactionID`* should contain only alphanumeric characters. 여러 [!UICONTROL transactionID]를 한 번의 히트에 기록해야 할 경우, 쉼표를 사용하여 여러 값을 구분하면 됩니다.

**예** {#section_A4C1F0E54CB54AD7B86A22147E9B5FEF}

```js
s.transactionID="11123456"
```

```js
s.transactionID="lead_12345xyz"
```

```js
s.transactionID=s.purchaseID
```

**함정, 질문 및 팁** {#section_4299BAD5D0154DBC88A9EF0E2C252BB4}

* *`transactionID`* 기록이 활성화되지 않으면 *`transactionID`* 값이 무시되고 통합 Data Sources와 함께 [!UICONTROL 사용할 수 없게]됩니다. Make sure to set a conversion variable or event (an eVar or the events variable) on the page where *`transactionID`* is set. 설정되지 않으면 *`transactionID`*.

* If you are recording [!UICONTROL transactionIDs] for multiple systems, such as purchases and leads, make sure the value in *`transactionID`* is always unique. lead_1234 및 purchase_1234와 같이 ID에 접두사를 추가하면 됩니다. [!UICONTROL 고유 항목이 두 번 표시되는 경우 통합 데이터 소스가] 예상대로 작동되지 않습니다 ( [!UICONTROL 데이터 소스] 데이터가 잘못된 *`transactionID`* 데이터와 연결됨).

* *`transactionID`* 기본적으로 값은 90 일간 기억됩니다. 오프라인 상호 작용 프로세스가 90일 이상인 경우 고객 지원에 요청하여 한계를 늘리십시오.

>[!NOTE]
>
>The *`transactionID`* variable can contain any character other than a comma. 이 변수는 문자 제한(100바이트)이 지정된 동일한 위치에 있어야 합니다. 멀티바이트 문자를 사용하는 경우, 멀티바이트 문자 지원을 활성화해야 *`transactionID`*.

## visitorID {#concept_CD273CC915CC4ABD8F52E4209FF9557E}

방문자는 변수 또는 IP 주소/사용자 에이전트로 식별할 수 있습니다.

<!-- 

visitorID.xml

 -->

The *`visitorID`* can be up to 100 alpha-numeric characters and must not contain a hyphen.

사용자 지정 ID를 명시적으로 설정하는 경우, 다른 ID 방법 전에 항상 이 ID가 사용됩니다.

사용 순서는 s.visitorID &gt; s_vi &gt; s_fid &gt; IP/UA입니다.

| ** 최대 크기** | ** 디버거 매개 변수** | ** 채워진 보고서** | ** 기본값** |
|---|---|---|---|
| 100바이트 | vid | n/a | "" |

**구문 및 가능한 값** {#section_5F768C7AE6824557997E92B295C09280}

```js
s.visitorID="visitor_id"
```

>[!NOTE]
>
>The *`visitorID`* variable should not contain a hyphen.

**예** {#section_F7F07FEFAC3644A5A084D166ACE1315E}

```js
s.visitorID="abc123"
```

**구성 설정** {#section_582B376FE55C4BCA8F978E0F62B5DB54}

없음

## visitorNamespace {#concept_8369DDB3830C4BF2905F1CFC8C8B0D92}

 변수는 쿠키가 설정된 도메인을 식별하는 데 사용됩니다.

<!-- 

visitorNamespace.xml

 -->

If *`visitorNamespace`* is used in your JavaScript file, do not delete or alter it. If *`visitorNamespace`* changes, all visitors reported in Analytics may become new visitors. 방문자 내역은 현재 및 미래 트래픽에서 연결성이 없어집니다. 따라서 Adobe 담당자의 승인 없이 이 변수를 바꾸지 마십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | ns | N/A | "" |

Analytics는 쿠키를 사용하여 사이트 방문자를 고유하게 식별합니다. If *`visitorNamespace`* is not used, the cookie is associated 2o7.net. If *`visitorNamespace`* is used, the cookie is associated with a sub-domain of 2o7.net. 사이트의 모든 방문자는 같은 도메인 또는 하위 도메인에 쿠키를 연결해야 합니다.

The reason for using the *`visitorNamespace`*&#x200B;변수를 사용하는 이유는 브라우저의 쿠키 제한을 초과하지 않도록 하기 위한 것입니다. Internet Explorer에서는 도메인당 쿠키를 20개로 제한하고 있습니다. by using the *`visitorNamespace`* 변수를 사용하면, 다른 회사의 Analytics 쿠키가 사이트 방문자의 쿠키와 충돌하지 않게 됩니다.

**구문 및 가능한 값** {#section_EE247FE371784CA4B6058182181F3EA1}

The value of *`visitorNamespace`* must be provided by Adobe and is a string of ASCII characters that don't contain commas, periods, spaces, or special characters.

```js
s.visitorNamespace="company_specific_value"
```

**보고서 세트 간 방문자 식별** {#section_7AC5A97FC8C045DD8850245A62BB09F4}

If you do not specify a `visitorNamespace`, each report suite in your company receives its own visitor ID cookie written as `s_vi_[random string]`. `visitorNamespace`를 지정하는 경우에는, 지정된 `s_vi`에 데이터를 보내는 모든 보고서 세트에 대해 동일한 `trackingServer` 쿠키가 사용됩니다. 다중 세트 태깅을 구현한 경우에는 반드시 각 보고서 세트에서 동일한 쿠키를 사용하도록 방문자 네임스페이스를 지정하십시오.

**예** {#section_89A95852AB9446E794AD3283B8800B09}

```js
s.visitorNamespace="company_name"
```

```js
s.visitorNamespace="Adobe"
```

**구성 설정** {#section_1128A2531ECC43DFA6749ECC21F050A2}

없음

## zip {#concept_C1DF93083553410DA36EAB61FBFDF69A}

AND 변수는 전환 변수입니다.

<!-- 

zip.xml

 -->

이벤트를 캡처한다는 점은 eVar와 비슷하지만 지속되지 않는다는 점은 eVar와 다릅니다. the *`zip`**`state`* 변수와 변수는 즉시 만료되는 Evar와 같습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 50바이트 | zip | 전환 &gt; 방문자 프로필 &gt; Zip/우편 번호 | "" |

The *`state`**`zip`* And 변수는 즉시 만료되며, 연관된 유일한 이벤트는 채운 동일한 페이지에서 실행되는 이벤트입니다. For example, if you are using *`zip`* to compare conversion rates by Zip Code, you should populate *`zip`* on every page of the checkout process. 청구 주소를 우편번호에 대한 소스로 사용하는 것이 좋습니다. 대신 배송 주소를 사용하도록 선택할 수도 있습니다(주문에 대해 배송 주소가 하나만 있다고 가정할 경우). 미디어 사이트는 등록이나 광고 클릭스루 추적에 *`zip`* 등록 *`state`* 또는 광고 클릭스루 추적을 수행할 수 있습니다.

**구문 및 가능한 값** {#section_5EDCFCAC8FC241D1B4CC777996858CD7}

```js
s.zip="zip_code"
```

*`zip`* 변수에는 값 또는 형식 제한이 적용되지 않습니다. There are no limitations on *`zip`* outside of the standard variable limitations.

**예** {#section_F25C0D0CC3C04B81892A662CD605C593}

```js
s.zip="92806"
```

```js
s.zip="92806-4115"
```

**구성 설정** {#section_7987084EECC34DD38B643B94F82385CA}

없음

**함정, 질문 및 팁** {#section_E86774D5CE8B40EFA36353CDEE3A84D0}

* 관련 이벤트를 실행하는 모든 페이지(예: 체크아웃 프로세스의 각 페이지)에서 [!UICONTROL zip]을 채우십시오(체크아웃 프로세스의 각 페이지).
* *`zip`* AND *`state`* 변수는 페이지 뷰에서 만료되는 evar 처럼 작동합니다.

