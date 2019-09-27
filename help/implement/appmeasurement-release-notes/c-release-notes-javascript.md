---
description: 이전 JavaScript H 코드에 대한 누적 릴리스 노트입니다.
seo-description: 이전 JavaScript H 코드에 대한 누적 릴리스 노트입니다.
seo-title: JavaScript H 코드- 이전
solution: Analytics
subtopic: 릴리스 노트
title: JavaScript H 코드- 이전
topic: 개발자 및 구현
uuid: 4586b250-0f1b-45b8-829c-18dc1201956f
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# JavaScript H 코드- 이전{#javascript-h-code-legacy}

이전 JavaScript H 코드에 대한 누적 릴리스 노트입니다.

>[!NOTE]
>
>To find the current library version, use [DigitalPulse Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger_about.html).

<!-- 

https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=omtrcache&title=AppMeasurement+Change+Log

 -->

## H.27.5 - Update {#section_DB9535C7EC4A4DDE9BA56B6C02BE8327}

릴리스 날짜: **2016년 6월 16일**

방문자 API 1.5.7 포함.

## H.25.5 - Update {#section_B10151D7718F4568AE523BE1553FCCB7}

릴리스 날짜: **2016년 5월 19일**

방문자 API 1.5.5 포함.

## H.27.5 - Update {#section_AD73ECD5CDAB4E158B509BA7B4B8CC1F}

릴리스 날짜: **2015년 11월 5일**

* 방문자 API 1.5.3 포함.

## H.27.5 - Update {#section_8A94D8A74A39486AAE248A22D661A261}

릴리스 날짜: **2015년 9월 17일**

* 방문자 API 1.5.2 포함.

## H.27.5 - Update {#section_62D1787F90FB4730B5F0C79EC1EF84B1}

릴리스 날짜: **2015년 8월 20일**

* 방문자 API 1.5.1 포함.

## H.27.5 - Update {#section_F58AF8B7FAE9470ABCBF2AAD9E7AF881}

릴리스 날짜: **2015년 6월 18일**

* 방문자 API 1.5 포함.

## H.27.5 - Update {#section_B3E310AFF909480BAD59A7F87D298348}

릴리스 날짜: **2015년 5월 21일**

* 방문자 API 1.4 포함

## H.27.5 - Update {#section_E7006FC903064376A85D3EC2AC1D2544}

릴리스 날짜: **2015년 4월 16일**

* Added Integrate module to s_code.js in legacy [!DNL AppMeasurement] for [!DNL JavaScript] H.X ZIP file. (AN-101001)

## H.27.5 {#section_22DCF43169614B28BC17F46426C5D5B6}

릴리스 날짜: **2015년 2월 19일**

* 방문자 API 1.3.5 포함.
* 첫 번째 추적 호출 전에 *`s.referrer`*&#x200B;가 수동으로 설정되었을 때 두 번째, 세 번째 등의 추적 호출(일반적으로 링크 추적)에서 레퍼러가 두 번 계산되지 않도록 첫 번째 추적 호출 이후에 자동 레퍼러 추적을 수행하지 않도록 변경되었습니다. (AN-92647)

## H.27.4 - Update {#section_ED38D59E83B4417180877F7C10BE4582}

릴리스 날짜: **2015년 1월 15일**

* 배포 zip이 방문자 API 1.3.4를 포함하도록 업데이트되었습니다.

릴리스 날짜: **2014년 9월 18일**

* 구현 시 추가적인 대시 문자 구분 기호와 함께 버전 문자열에 추가되는 최대 4개의 문자를 지정할 수 있도록 해주는 `tagContainerMarker` 변수를 추가했습니다. 이는 다이내믹 태그 관리에서 사용됩니다.

```js
  //  
<keyword>
  JavaScript 
</keyword> 
  s.tagContainerMarker = "D1.0"; 
    
  // Data Collection request 
  //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
```

## H.27.3 {#section_B38C61EE3BEA49CAA7A664395C85E4CF}

릴리스 날짜: **2014년 8월 21일**

* 예정된 기능을 지원하기 위한 내부 변경.

## H.27.2 {#section_402A4142C4B846DE945FD59DAD9D9298}

릴리스 날짜: **2014년 6월 19일**

* Fixed handling of done and waiting flags for Visitor API fields such as the legacy [!DNL Analytics] Visitor ID, that was causing errors.
* 방문자 ID 서비스 1.3의 새로운 기능에 대한 지원

## H.27.1 {#section_CC2556C734EE4BAAB71D6A93095DB38F}

릴리스 날짜: **2014년 6월 11일**

* Fixed an issue in the [!DNL Analytics] for [!DNL Target] integration that caused some hits to incorrectly be merged.

## H.27 {#section_023B6267C0DB424F99A23EBB732B8C69}

릴리스 날짜: **2014년 5월 22일**

* Support for the Experience Cloud Visitor ID service.[](https://marketing.adobe.com/resources/help/en_US/mcvid/)
* [타겟 통합을 위한 Analytics](https://marketing.adobe.com/resources/help/en_US/target/a4t/)를 지원합니다.

## H.26.2 {#section_DE82C8BC7645400785E5B136565616F1}

릴리스 날짜: **2013년 10월 17일**

* Added `alt=""` to all Image objects to comply with Accessible Video and Communications Act.

## H.26.1 {#section_C3BDD9A19EF84467A8FDC283AEAE2DB5}

릴리스 날짜: **2013년 7월 18일**

* 이제 해시/단편이 자동 링크 추적에서 무시됩니다. Previously the following URL was automatically tracked since the entire `href` ended in `.pdf`:

```js
  <a href="index.htm#anchor.pdf">Test Link</a>
```

이제 해시/단편이 무시되므로 파일 이름이 일치하는 확장명으로 끝나는 경우에만 해당 링크가 추적됩니다.

## H.26 {#section_E25814ACC21E41718EE1741A85AE567B}

릴리스 날짜: **2013년 4월 29일**

* `useForcedLinkTracking`사용자 지정 링크 코드를 사용하여 수동으로 링크 추적[에 설명된 ](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_manuallinktrackcustomlink.html) 옵션이 Firefox 20+에 적용됩니다(이전에는 WebKit 브라우저에만 이 옵션이 적용되었음).

* 이미지 개체 ID 생성은 이제 인스턴스 간에 고유하게 변경되어 두 개 이상의 인스턴스가 동일한 페이지에 있어도 충돌이 발생하지 않습니다.

## H.25.5 {#section_A528D1D5E84146F9A56680E4427B2750}

릴리스 날짜: **2013년 4월 19일**

* Fixed an issue in forced link tr [!DNL Windows]acking that caused a [!DNL JavaScript] error on some [!DNL Android] 2.2 Devices.

*  Media Player의 비디오 자동 추적 기능에서, 재생된 시간이 제대로 추적되지 않았던 스크러빙 시의 문제를 해결했습니다.

## H.25.4 {#section_009AF895C8DD47CABC9A3776D27E8300}

릴리스 날짜: **2013년 2월**

* Changed automatic exit link tracking to always ignore links with `HREF` attributes that start with `#`, `about:`, or `javascript:`.

* `useForcedLinkTracking`에 의해 영향을 받는 클릭 이벤트의 범위가 미세 조정되었습니다. 자동 강제 링크 추적은 다음의 경우에만 적용됩니다.

   * `<A>` 및 `<AREA>` 태그

   * 태그에 `HREF` 특성이 반드시 있어야 함
   * The `HREF` can't start with `#`, `about:`, or `javascript:`

   * The `TARGET` attribute must not be set, or the `TARGET` needs to refer to the current window ( `_self`, `_top`, or the value of `window.name`)

## H.25.3 {#section_FA6A6F9F5D64455DA5A54C007081341A}

릴리스 날짜: **2013년 1월**

* Adobe 데이터 수집 서버의 페이지 URL 필드 확장을 지원할 수 있도록 255바이트보다 긴 URL을 전송하는 지원이 추가되었습니다. Page URLs longer than 255 bytes are split, with the first 255 bytes appearing in the `g=` parameter, with the remaining bytes appearing later in the query sting in the `-g=` query parameter. 따라서 브라우저가 잘리는 경우 긴 URL이 다른 데이터보다 우선하는 경우를 방지하면서도 긴 URL을 여전히 캡처할 수 있습니다.

* `escape` 및 `encodeURIComponent`가 함께 사용되어 인코딩된 문자열에 대한 URL 디코딩 처리가 수정되었습니다.

* WebKit 브라우저에서 첫 번째 서버를 페이지가 시간 초과되었을 때 요청할 경우 링크 추적을 실패하는 문제를 수정했습니다.
* 새로운 대체 방문자 식별 메서드가 추가되었습니다. [고유한 방문자 식별](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_identifying_unique_visitors.html)을 참조하십시오.
* `abort` 내에서 설정할 수 있는 새로운 `doPlugins` 플래그가 추가되었습니다. 이 플래그를 true로 설정하면 [!DNL AppMeasurement] 라이브러리가 해당 추적 호출을 계속할 수 없습니다. abort 플래그가 모든 추적 호출로 재설정되므로, 추적 호출 또한 무시해야 할 경우 우 플래그를 `doPlugins` 내에서 다시 설정해야 합니다.

```js
  s.doPlugins = function(s) { 
       s.campaign = s.getQueryParam("cid"); 
       if ((!s.campaign) && (!s.events)) { 
            s.abort = true; 
       } 
  };
```

이는 사용하는 로직에 집중할 수 있게 하여 일부 사용자 지정 링크 또는 디스플레이 광고의 외부 링크와 같이 추적하지 않으려는 활동을 식별할 수 있습니다.

## H25.2 {#section_647D7638D0C04019B8C9986CD124914E}

릴리스 날짜: **2012년 10월**

* Added support for reporting an additional version number in the [!DNL JavaScript] version report. 이전에 이 버전은 2자(예: 1.8)로 제한되어 있었습니다. 3자 버전 번호(예: 1.8.5)에 지원이 추가되었습니다.
* Fixed an issue with [!DNL Tag Manager] that prevented repeated values in Dependant Code blocks from being sent.

## H.25.1 {#section_680CE31CFA9945978F42612B684DB831}

릴리스 날짜: **2012년 9월**

* 다음 문자에 대해 URL 인코딩을 강제로 적용했습니다.

```
  ~ 
  ! 
  * 
  ( 
  ) 
  '
```

This resolves issues with un-escaped characters being stored in the [!DNL ClickMap] `s_sq` cookie.

* 미디어 닫기 이벤트를 추적하는 사용자 지정 `media.monitor` 메서드를 사용하는 경우 비디오 완료 이벤트가 전송되지 않는 문제를 해결했습니다.

```
  If(media.event==”CLOSE”) { 
  … 
  } 
  
```

## H.25 {#section_BE76FEDFE03B44658808B0BDF779DE97}

릴리스 날짜: **2012년 7월**

WebKit 브라우저(Safari 및 Chrome)에서 링크 추적이 성공적으로 완료되도록 업데이트를 수행했습니다. 이 업데이트 후에는 자동 추적되는(`s.trackDownloadLinks` 및 `s.trackExternalLinks`로 판별됨)다운로드 및 종료 링크가 성공적으로 추적됩니다. If you are tracking custom links using manual [!DNL JavaScript] calls, you need to modify how these calls are made.

예를 들어, 종료 및 다운로드 링크는 종종 다음과 유사한 코드를 사용하여 추적됩니다.

```js
  <a href="http://anothersite.com" onclick="s.tl(this,'o','link name',null)">
```

Firefox 및 Internet Explorer는 추적 링크 호출을 실행하고 새 페이지를 엽니다. 그러나, 새 페이지가 열릴 때 WebKit 브라우저는 추적 링크 호출 실행을 취소할 수 있습니다. 종종 이 때문에 WebKit 브라우저를 사용할 때 추적 링크 호출이 완료되지 않습니다.

이 동작을 해결하기 위해 H.25는 추적 링크 호출이 완료될 때까지 WebKit 브라우저가 대기하도록 하는 오버로드된 추적 링크 메서드(`s.tl`)를 포함합니다. 이 새 메서드는 기본 브라우저 작업을 사용하는 대신, 추적 링크 호출을 실행한 다음 탐색 이벤트를 처리합니다. 이 오버로드된 메서드에는 링크 추적 호출이 완료될 때 수행될 작업을 지정하는 `doneAction`이라는 추가 매개 변수가 필요합니다.

이 새 메서드를 사용하려면 다음과 같이, 추가 `s.tl` 매개 변수로 `doneAction`에 대한 호출을 업데이트하십시오.

```js
  <a href="http://anothersite.com" onclick="s.tl(this,'o','link name',null 
  <codeph outputclass="syntax"> ,'navigate');return false"> 
  </codeph outputclass="syntax">
```

'navigate'를 `doneAction`으로 전달하면 기본 브라우저 동작이 미러링되고 추적 호출이 완료될 때 `href` 속성으로 지정된 URL이 열립니다.

다음 표는 구성 변수와 이 기능을 지원할 수 있도록 H.25에서 수행된 업데이트를 요약한 표입니다.

<table id="table_E67157D710874146B26EFB7D84762542"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>변수 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>useForcedLinkTracking </p> </td> 
   <td colname="col2"> <p>이 플래그는 WebKit 브라우저에 대한 강제 링크 추적을 비활성화하는 데 사용됩니다. 강제 추적 링크는 WebKit 브라우저 기본값에 의해 비활성화되며 다른 브라우저에 의해 무시됩니다. </p> <p> <b>기본값</b> </p> <p> <code> true </code> </p> <p> <b>예</b> </p> 
    <code class="syntax javascript">
      s.useForcedLinkTracking&amp;nbsp;=&amp;nbsp;false </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>forcedLinkTrackingTimeout </p> </td> 
   <td colname="col2"> <p><code>s.tl</code>로 전달된 <code>doneAction</code>을 수행하기 전에 완료할 수 있도록 추적을 기다리는 최대 밀리초 수입니다. 이 값은 최대 대기 시간을 지정합니다. 이 시간 초과 전에 추적 링크 호출이 완료되면 <code>doneAction</code>이 즉시 실행됩니다. 추적 링크 호출이 완료되지 않고 있다는 것을 안 경우 이 시간 초과를 늘려야 할 수도 있습니다. </p> <p> <b>기본값</b> </p> <p>250 </p> <p> <b>예</b> </p> 
    <code class="syntax javascript">
      s.forcedLinkTrackingTimeout&amp;nbsp;=&amp;nbsp;500 </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trackLink(<code>s.tl </code>) </td> 
   <td colname="col2"> <p>종료, 다운로드 및 사용자 지정 링크를 추적합니다. 추적 링크 호출이 WebKit 브라우저에서 완료된 후에 실행할 탐색 작업을 지정할 수 있도록 옵션 매개 변수를 제공합니다. </p> <p> <b>구문</b> </p> 
    <code class="syntax javascript">
      s.tl(linkObject,linkType,linkName,variableOverrides,doneAction) </code> <p> <b>doneAction</b>: (선택적) 링크 추적 호출이 전송되거나 시간 초과된 후에 취할 조치를 지정합니다(<code>s.forcedLinkTrackingTimeout</code>에 의해 지정된 값 기준 ). <code>doneAction</code>은 문자열 'navigate'가 될 수 있으며, 이는 메서드가 <code>document.location</code>을 <code>linkObject</code>의 <code>href</code> 특성으로 설정하는 원인이 됩니다 . 또한, <code>doneAction</code>은 고급 사용자 지정을 허용하는 함수가 될 수 있습니다. </p> <p>If providing a value for <code> onclick </code> in an anchor <code> false </code> event, you must return <code> s.tl </code> after the <code> href </code> call to prevent the default browser navigation. </p> <p> To mirror the default behavior and follow the URL specified by the <code> doneAction </code> attribute, provide a string of 'navigate' as the <code> doneAction </code>. </p> <p>Optionally, you can provide your own function to handle the navigation event by passing this function as the <code>$1</code>. </p> <p> <b>예</b> </p> 
    <code class="syntax javascript">
      &lt;a&amp;nbsp;href="..."&amp;nbsp;onclick="s.tl(this,'o','MyLink',null,'navigate');return&amp;nbsp;false"&gt;Click&amp;nbsp;Here&lt;/a&gt; </code> <code class="syntax javascript">&lt;a&amp;nbsp;href="#"&amp;nbsp;nsp;onclick="s.tl(this,'o','MyLink',null,function(){if(confirm('Continue?'))document.location=..});return&amp;nbsp;false"&gt;Click&amp;nbsp;Here&lt;/a&gt; </code> </td> 
  </tr> 
 </tbody> 
</table>

## H.24.4 {#section_1989179F10A34E88968CA5A5290CF17C}

릴리스 날짜: **2012년 4월**

이 업데이트는 모든 고객에게 권장됩니다.

* 페이지가 Google Chrome Prerender를 사용하여 사전 렌더링되는 시점을 탐지하기 위한 기능이 향상되었습니다([https://developers.google.com/chrome/whitepapers/prerender](https://developers.google.com/chrome/whitepapers/prerender)). Since Prerender loads and executes [!DNL JavaScript] and other code, this could result in page views being sent before a user clicks to visit your site. The [!DNL JavaScript] library now waits until the user visits your site before sending server calls for these prerendered pages.
* 다른 라이브러리와 유사한 타임스탬프 데이터를 사용자 지정하려는 고객을 위해 라이브러리에 `timestamp`[!DNL JavaScript] 변수를 추가했습니다.[!DNL AppMeasurement]

```js
  s.timestamp=Math.round((new Date()).getTime()/1000); 
  s.timestamp="2012-04-20T12:49:31-0700";
```

## H.24.3 {#section_F3D471B201F54C089320D3CE6D441DC0}

릴리스 날짜: **2012년 2월**

* Javascript `Object.prototype` 무시를 사용하는 고객에 대한 이미지 요청에 추가 데이터가 포함되는 문제를 해결했습니다. 컨텍스트 데이터 변수를 처리할 때 이제 모든 `Object.prototype` 사용을 건너뜁니다.
* 일부 환경에서 `pe` 쿼리 매개 변수가 같은 값으로 두 번 전달되는 문제를 해결했습니다.
* Fix to [!DNL ClickMap] tracking in [!DNL JavaScript] to ignore clicks to the body tag, even when the tag has an `onClick` event handler.
* 추적 호출에 사용된 변수(`trackLight`)에 타임스탬프를 추가했습니다.

## H.24.2 {#section_91CF07C2BC9B4C8BA0235DFDFB95A4D9}

릴리스 날짜: **2012년 1월**

* 전체 비디오 보기 횟수를 추적하는 새로운 방법을 사용하여 비디오 추적을 업데이트했습니다.
* Fixed an issue that caused an "Attribute only valid on v:image" [!DNL JavaScript] error for `OnClick` events on VML elements in IE.
* 컨텍스트 데이터 변수가 linkTrackVars에서 참조되지만 링크 서버 호출에 포함되지 않던 버그를 `linkTrackVars`. 컨텍스트 데이터 변수가 처리 규칙과 함께 사용됩니다.

## H.24.1 {#section_967356D219FE4E9CAA110D03EDF4C8B1}

릴리스 날짜: **2011년 11월**

* 동시에 발생하는 세그먼트 및 마일스톤에 대한 히트를 통합하도록 비디오 추적을 업데이트했습니다.

## H.24 {#section_78FF9B245643406BB7E9967E784A90AE}

릴리스 날짜: **2011년 11월**

* 지원을 위한 내부 업데이트 [!DNL Adobe Tag Manager].

## H.23.9 {#section_3834625A639A47428683E08A472359C7}

릴리스 날짜: **2011년 11월**

* 지원을 위한 내부 업데이트 [!DNL Adobe Tag Manager].

## H.23.8 {#section_FF3CEEAB6C6744D6B5EE314A0B5841CA}

릴리스 날짜: **2011년 10월**

* Fixed an issue that caused the `linkTrackVars=none` and `linkTrackEvents=none` settings to not apply when using automatic exit link tracking. 현재 이러한 설정이 자동 종료 링크에 적용되므로 prop, eVar 및 이벤트를 종료 링크 이미지 요청과 함께 보내지 않습니다.

## H.23.7 {#section_D9D0CF343EBF49D9844C6BDA0C3C7A2E}

릴리스 날짜: **2011년 9월**

* WML(무선 마크업 언어) 표준을 준수하기 위해 모바일 장치의 이미지 태그에서 테두리 특성을 제거했습니다. 이를 통해 일부 모바일 장치의 렌더링 문제를 수정했습니다.

## H.23.6 {#section_461A208BE1B64EDDA87A8D7C4FD5456C}

릴리스 날짜: **2011년 8월**

비디오 추적의 비율 측정 정확성이 수정되었습니다.

## H.23.5 {#section_FCE48EE33C9A42F08386FA30037BF4E0}

릴리스 날짜: **2011년 7월**

* Added support for [!DNL Adobe Tag Manager].

## H.23.4 {#section_E9152B4437C24107A68D264F70361930}

릴리스 날짜: **2011년 6월**

* Fixed an issue that caused [!DNL JavaScript] errors when accessing certain properties of Vector Markup Language (VML) shape elements.
* 255자를 초과하는 참조 문자열은 이제 쿼리 문자열이 아닌 경로를 줄이는 것으로 잘립니다. 이를 통해 쿼리 문자열 매개 변수가 잘리고 수집되지 않는 문제를 수정했습니다.

## H.23.3 {#section_EAB0602E07EE4A5CA6521351F461D22D}

릴리스 날짜: **2011년 5월**

* 비디오 추적(pev3) 변수 전송을 방해하는 문제를 수정했습니다.
* G 및 H 코드와 호환될 수 있도록 `s_gi`가 코드를 활성화하는 것을 방해하는 문제를 수정했습니다. 두 번째 매개 변수로 1을 이 호출로 전달하면 이제 코드가 양쪽 버전과 호환될 수 있도록 구성됩니다.

## H.23.2 {#section_274143E83A8D42F1AD40CAE4326E99CE}

릴리스 날짜: **2011년 4월**

* 서버측 처리 규칙을 유도하는 contextData를 지원합니다(v15만 해당).
* 라이트 서버 호출을 지원합니다(v15만 해당).
* 이벤트 목록에서 카운터 이벤트에 1이 아닌 값을 할당할 수 있도록 지원합니다.
* 전환 eVar 및 이벤트를 사용하여 비디오를 추적하는 새로운 메서드를 지원합니다(현재 베타 버전).
* Media.trackWhilePlaying을 fasle로 설정하는 지원을 제거했습니다. 항상 true로 설정됩니다.
* 요청의 로깅이 다른 플랫폼과 같이 Firebug 콘솔로 전송을 활성화할 수 있도록 debugTracking 플래그가 추가되었습니다.
* "+"가 브라우저에 상관없이 항상 URL로 인코딩되는지 확인하십시오.
