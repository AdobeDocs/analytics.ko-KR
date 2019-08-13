---
description: JavaScript용 AppMeasurement에 대한 누적 릴리스 노트입니다.
seo-description: JavaScript용 AppMeasurement에 대한 누적 릴리스 노트입니다.
seo-title: JavaScript용 AppMeasurement
solution: 분석
subtopic: 릴리스 노트
title: JavaScript용 AppMeasurement
topic: 개발자 및 구현
uuid: 1440013 D-D 266-4 DCE -9807-8 B 9 ADAC 73315
translation-type: tm+mt
source-git-commit: 0143edbcbab3450f6932367f51e9e4c79bc1ae63

---


# JavaScript용 AppMeasurement{#appmeasurement-for-javascript}

Cumulative release notes for [!DNL AppMeasurement] for JavaScript.

<!-- 

<p>https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log </p>

 -->

The latest version of each library can be downloaded in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Code Manager]**.

## 버전 2.16.0

릴리스 날짜: **2019년 8월 15일**

| 기능 | 설명 |
| -----------| ---------- |
| 종료 링크에 대한 `sendBeacon` 지원 | [!UICONTROL AppMeasurement]에 종료 링크에 대한 `sendBeacon` 지원 기능을 구현했습니다. 이를 통해 종료 링크 추적 기능이 개선되고 트래픽이 증가할 수 있습니다. `SendBeacon` 페이지 컨텍스트에서는 실행되지만 브라우저의 컨텍스트에서는 실행되지 않습니다. 즉, 페이지가 언로드되는 `sendBeacon`경우 요청이 계속 완료됩니다. 종료 링크 요청이 완료될 가능성이 훨씬 더 높기 때문에 종료 링크에 매우 유용합니다. |
| ECID/fid 값 | 이제 OptIn 설정이 변경되더라도 ECID/fid 값이 첫 번째 히트에 캐시됩니다. |
| DIL 9.3 | 대상 관리 모듈의 DIL 9.3 업데이트 |
| 스크롤 도달 추적 | s.ActivityMap.trackScrollReach에 스위치를 노출하여 스크롤 도달 추적을 켜거나 끕니다. |
| 방문자 ID 서비스 4.4.0 | 방문자 ID 서비스 4.4.0을 사용하도록 AppMeasurement를 업그레이드했습니다. |

## 버전 2.15.0

릴리스 날짜: **2019년 7월 15일**

* Activity Map 확장에 activitymap 스크롤 도달 추적을 추가했습니다 (AN -172949).
* Appmeasurement에 DIL 9.2 추가 (AN -182472)

## 버전 2.14.0

릴리스 날짜: **2019년 5월 21일**

* 여러 개의 히트가 보류 중일 때 추적기 매개 변수의 상태 관리에 대한 문제가 해결되었습니다. (AN-176931, AN-176629, DTM-12758)
* Visitor.js 4.3.0을 포함하도록 AppMeasurement가 업데이트됨(AN-180049)

## 버전 2.13.0

릴리스 날짜: **2019년 4월 10일**

Clearvars에서 보고된 많은 문제를 수정했습니다. 추적기가 준비되기 전에 히트를 보낼 때 문제가 발생합니다. 추적기가 준비되면 라이브러리에서 이미 삭제 또는 변경된 변수를 설정할 수 있습니다. (AN-176931, AN-176629, DTM-12758).

## 버전 2.12.0

Release Date: **02/22/2019**

* 대상 관리 모듈이 DIL 9.1로 업데이트되었습니다. (AN-175255)
* GTM 보안 정책이 Activity Map 모듈을 허용하지 않습니다. (AN-174679)
* Identity Service가 옵트인에서 승인되지 않은 경우 옵트아웃을 준수하도록 appmeasurement가 개선되었습니다. (AN-175259)

## 버전 2.11.0

Release Date: **02/11/2019**

* AppMeasurement에 새로운 Adobe 옵트인 서비스 기능 지원이 추가되었습니다. (AN-163546)
* 세션-스토리지에서 링크 추적 데이터 저장 지원이 추가되었습니다. (AN-162272)
* Audio Analytics에 대한 미디어 스트림 유형 지원이 추가되었습니다. (AN-173265)

## 버전 2.10.0 {#section_0788526EF23049C9AEB1EE5E8FC985DD}

Release Date: **09/20/2018**

This release ensures that the [!DNL AppMeasurement] library submits cookies correctly for all connection types.

* [!DNL AppMeasurement] 게시물 중에 쿠키 전송을 차단합니다. (AN-165538)
* XDomainRequest에 대한 지원을 삭제합니다. (AN-165733)
* [!DNL AppMeasurement] 기본 쿠키 라이프타임을 5 년에서 2 년으로 줄일 수 있습니다. (AN-158572)
* Remove the Media Module from the Code Manager ( [!DNL AppMeasurement]) (AN-166590)

## 버전 2.9.0 {#section_E973B8A628F348AA9A1A1599CFE37DB9}

릴리스 날짜: **2018/05/24**

>[!NOTE]
>
>Visitor API 3.0 or higher is required for customers using the [!DNL Experience Cloud] ID Service. 연관된 코드 라이브러리([!DNL at.js] 등)가 업데이트될 때마다 최신 방문자 API 버전으로 업그레이드할 수 있습니다.[!DNL AppMeasurement.js]

* Updated [!DNL AppMeasurement] to use the updated Visitor interface for requesting IDs. (AN-151483)
* 링크 추적이 해제된 후에도 링크 추적 쿠키가 계속 작성되는 문제가 수정되었습니다. (AN-156332)
* 여러 번 호출될 때 `registerPreTrackCallback` 및 `registerPostTrackCallback`이 콜백 함수 서명을 차단하는 문제가 해결되었습니다. (AN-158566)

## 버전 2.8.2 {#section_B70EAEDAB087464482DB04EC4187200D}

릴리스 날짜: **2018/04/12**

* Update [!DNL AppMeasurement] to use the updated visitor interface for requesting IDs. (AN-151483)
* 링크 추적이 해제되면 링크 추적 쿠키가 계속 기록됩니다. (AN-156332)
* [!DNL AppMeasurement] 기본 쿠키 라이프타임을 5 년에서 2 년으로 줄일 수 있습니다. (AN-158572)

## 버전 2.8.1 {#section_6C1C4091F2EE4C90B6F3D7EE783DD884}

릴리스 날짜: **2018/03/29**

핫픽스를 포함하는 방문자 API 3.1.0(AN-159524) 재구성: (CORE-11390, CORE-10634)

## 버전 2.8.0 {#section_A23AD604D34C497C9318D3EB211B7927}

릴리스 날짜: **2018/03/15**

핫픽스를 포함하는 방문자 API 3.1.0(AN-159524) 재구성: (CORE-11390, CORE-10634)

* Bundle VAPI v3.1 with [!DNL AppMeasurement] v2.8. (AN-158353)
* 리팩터는 공유를 용이하게 하기 위해 데이터 컬렉션 끝점을 작성합니다. (AN-156647)
* Add request round-trip timing metrics to [!DNL AppMeasurement]. (AN-158343)

## 버전 2.7.0 {#section_2C047D410B614CEE950DBBC75F035033}

릴리스 날짜: **2018/01/18**

* IE 6~9 지원 삭제
* 방문자 API v3.0.0 포함
* DIL v7.00 포함

## 버전 2.6.0 {#section_229356205EAB4D05890A00B39C42A650}

릴리스 날짜: **2017/11/09**

Fixed an issue where [!DNL AppMeasurement] library does not always set the correct account combination when s_gl is called. (AN-152153)

## 버전 2.5.0 {#section_3C0006D526CA405FA0C47E2D991012BA}

릴리스 날짜: **2017/09/21**

* Inclusion of [!DNL dil.js 6.12] ( [!DNL Audience Manager] module)

* 방문자 API 2.5.0 포함.

## 버전 2.4.0 {#section_60D01A128AEE4A97AC492DF8FBE1E7A3}

릴리스 날짜: **2017/08/17**

* dil.js v6.11 포함
* 방문자 API 2.4.0 포함

## 버전 2.3.0 {#section_D8F9BFF0D4E44E0F876840360D56E815}

릴리스 날짜: **2017/07/20**

* [!DNL s.Util.getQueryParam]으로 #이 캡처되던 버그를 수정했습니다.
* Added v6.10 of [!DNL dil.js] (AN-145701)

## 버전 2.2.0 {#section_5E23F21413B1443B9A3021CCC9578C4B}

릴리스 날짜: **2017/06/08**

* Added support for multiple [!DNL AppMeasurement] instantiation order. (AN-138237)
* 방문자 API 2.2.0 버전 포함. (AN-144042)

## 버전 2.1.0 {#section_5FE53738F9124C86811DFA08923B6F7B}

* [!DNL dil.js] 최신 버전 포함(AN-140396)
* Added support for `adobe_mc_ref` parameter which overrides the page referrer. (AN-131920)
* 방문자 API 2.1.0이 다시 포함되었습니다. (AN-140873)
* `mcorgid` 매개 변수가 추가되었습니다. (AN-139586)
* cp (customerPerspective) 매개 변수가 추가되었습니다. (AN-140897)

## 버전 2.0.0 {#section_4C4A502CDFC84F06914EB16CE77736D1}

릴리스 날짜: **2017/03/09**

* 버전 번호를 2.0.0으로 업데이트해야 하는 새 빌드 프로세스로 이동했습니다. (AN-137878)
* 추적 호출이 생성된 올바른 섹션 위치로 mboxMCSDID 처리를 이동했습니다. (AN-138483)

## 버전 1.8.0 {#section_617B2F09F3494C04901E364ACEDE17E1}

릴리스 날짜: **2017/01/19**

* 방문자 API 2.0.0 포함
* 함수 호출 및 확인 순서가 변경되었으므로 중단 검사가 완료된 후에 SDID가 사용됩니다. (AN-134364)
* 다음 사전 및 사후 추적 호출 후크가 추가되었습니다. (AN-134567)

   * s.registerPreTrackCallback
   * s.registerPostTrackCallback
   이 함수들은 매개 변수로서 콜백(기능)을 사용하고 해당 기능에 대한 매개 변수를 사용합니다. 예:

   ```
   s.registerPreTrackCallback(function(requestUrl,a,b,c) { 
       console.log("pre track callback"); 
       console.dir(requestUrl); // Request URL 
       console.dir(a); // param1 
       console.dir(b); // param2 
       console.dir(c); // param3 
   }, "param1", "param2", "param3");
   ```

   콜백은 콜백을 등록할 때 전달되는 모든 매개 변수와 `requestUrl`과 함께 호출됩니다. 이러한 일은 콜백을 등록하는 데 사용되는 메서드에 따라 추적 호출 전 또는 후에 발생합니다. 이러한 콜백이 호출되는 순서는 보장되지 않습니다. 사전 함수에 등록된 콜백은 최종 추적 URL이 생성된 후 호출됩니다. 사후 콜백은 추적 호출 성공 시 호출됩니다(추적 호출이 실패하는 경우에는 이 함수들이 호출되지 않습니다). `registerPreTrackCallback`과 함께 등록된 모든 콜백은 추적 호출에 영향을 주지 않습니다. 또한, 등록된 임의의 콜백에서는 추적 메서드를 호출하지 않는 것이 좋으며, 호출하는 경우 무한 루프가 발생할 수 있습니다.

## 버전 1.7.0 {#section_A93F24391B1043F4A435D1AA76D9E4F0}

업데이트됨: **2016/11/10**

* 방문자 API 1.10.1 포함.

## 버전 1.7.0 {#section_107CDB8468AE4B06B900DCDEE5AD2F0A}

업데이트됨: **2016/10/20**

* Update [!DNL Audience Manager] module with Demdex Integration Library (DIL) 6.6. (AN-132065)
* 방문자 API 1.9.0 포함 (AN-132072)

## 버전 1.7.0 {#section_945311938EE2480A9A697BFE1E5B2AA7}

업데이트됨: **2016/9/15**

* Update [!DNL AppMeasurement] [!DNL Audience Manager] Module with DIL 6.5 and Additional Configurations (AN-129411)

* 방문자 API 1.8.0(AN-129887) 포함

## 버전 1.6.4 {#section_7C40FE01EA5B43E486098FCAC8FA5EC3}

업데이트됨: **2016/8/18**

* Updated [!DNL AppMeasurement] to read and write AMCV cookies. (AN-127098)
* 방문자 API 1.7.0 포함.

>[!NOTE]
>
>Also see the following release notes for [!DNL JavaScript] version 1.6.3, which includes updated requirements for Marketing Cloud ID service.

## 버전 1.6.3 {#section_34C75470A84B461A89FEF8CFF7B94090}

업데이트됨: **2016/8/4**

* Fixed an issue where [!DNL AppMeasurement] prematurely terminated request connections. (AN-126448)

>[!IMPORTANT]
>
>Version 1.6.0 of the [!DNL Marketing Cloud] ID service *requires* [!DNL AppMeasurement] for [!DNL JavaScript] version 1.6.3 or higher. If you want to upgrade to version 1.6.0 of the Marketing Cloud ID service, please make sure you are using [!DNL AppMeasurement] code verison 1.6.3 or higher.

## 버전 1.6.2 {#section_419CBF264B5741DABB005AFDC6197C0D}

릴리스 날짜: **2016년 7월 21일**

* 방문자 API 1.6.0 포함
* Fixed an issue causing [!DNL AppMeasurement] to call the wrong obfuscated method in the Visitor API. (AN-126006)
* [!DNL JavaScript] 오류가 발생하는 문제를 수정했습니다. " 속성은 v 에서만 유효합니다. image ". (AN-124009)

<!-- 

<note type="important">
  Adobe strongly recommends upgrading to version 1.6.2 or higher. This version requires Visitor API 1.6.0, and vice-versa. 
</note>

 -->

## 버전 1.6.1 {#section_E69F5883F84F4D2CAE25D385F56C6AF6}

릴리스 날짜: **2016년 6월 16일**

방문자 API 1.5.7 포함.

## 버전 1.6.1 {#section_5927689A57164EC99BA501B4FDF0AE8F}

릴리스 날짜: **2016년 5월 19일**

[!DNL JavaScript] 버전 1.5.6

* 방문자 API 1.5.6 포함
* 완전한 이벤트를 발생하지 않던 Firefox의 링크 클릭 추적 처리를 수정했습니다.

## 버전 1.6 {#section_B132B272FC2E43E9A24198F459E29403}

릴리스 날짜: **2016년 4월 21일**

* [!DNL AppMeasurement][!DNL Activity Map] 모듈은 [!DNL AppMeasurement] 표준 모듈에 통합되었으므로 [!DNL .js] 하나의 파일만 참조할 수 있습니다. [!DNL Activity Map] 또한 추적이 기본적으로 활성화됩니다. (AN-112689)

* Fixed a truncation issue occurring with the order of query-string variables in [!DNL AppMeasurement], so that *`pageURLRest`* is last. (AN-114647)

## 버전 1.5.4 {#section_A230E5F656734ABD9917388790A37B5D}

릴리스 날짜: **2016년 3월 17일**

* 방문자 API 1.5.4 포함
* 방문자 API 1.5.4 이상에서 옵트아웃 지원

## 버전 1.5.3 {#section_796927A1BBF74DF6A1A4B9477E0BD20E}

릴리스 날짜: **2016년 1월 21일**

* Fixed handling of [!DNL Audience Manager] module when POSTs are used for tracking calls. (AN-115381)
* 페이지 URL의 나머지 부분("-g")을 추적 요청 쿼리 문자열 끝으로 이동했습니다. (AN-114647)

## 버전 1.5.2 {#section_17CFD0BBC8744447BDFCC833883BC93E}

릴리스 날짜: **2015년 11월 5일**

* 방문자 API 1.5.3 포함.
* URL Truncation 2047에 대한 IE11 검색 수정(AN-114914)

## 버전 1.5.1 {#section_432F3C69DDBB49C983D7CB0876C2152F}

릴리스 날짜: **2015년 9월 17일**

* 방문자 API 1.5.2 포함

## 버전 1.5.1 {#section_077DA135C1A5466EB00C44A3C3E472F8}

릴리스 날짜: **2015년 8월 29일**

* 방문자 API 1.5.1 포함.

## 버전 1.5.1 {#section_3C9637EDB058479184731067897E857C}

릴리스 날짜: **2015년 7월 16일**

* Updated [!DNL Audience Manager] module to use AAM DIL 6.2 - getCustomer IDs from VisitorAPI.js and pass them in /event call to AAM. (AN-104978)

## 버전 1.5 {#section_8809DBD822E440C6B5B7FF41E5DF3015}

릴리스 날짜: **2015년 6월 18일**

* *`getCustomerIDs`* 메서드를 사용하여 고객 ID와 인증된 상태를 수집하고 데이터 수집 요청으로 해당 ID를 전송하는 방문자 API 1.5에 대한 지원.
* **[!UICONTROL Audiencemanagement]** 모듈 (DIL 6.1) 에서 복제 대상 iframe의 생성을 수정했습니다.
* 릴리스 1.4.5에 설명된 알려진 문제를 해결했습니다.

## 버전 1.4.5 {#section_FA2E94DF78614ACE9944660E14EF3A75}

릴리스 날짜: **2015년 5월 21일**

<table id="table_E0F3EF51FED44420AC97ACF0684554D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 기능 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="keyword"> iOS 확장</span> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> iOS </span> SDK 버전 4.5 부터 새로운 <span class="keyword"> iOS </span> 확장 기능을 사용하면 Apple Watch Apps, Today Widgets, Photo Editing 위젯 및 기타 <span class="keyword"> 모든 iOS </span> 확장 앱의 사용 데이터를 수집할 수 있습니다. </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=ios_ext" format="https" scope="external">iOS 확장 구현</a>을 참조하십시오 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="keyword"> Android Wearable 확장</span> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Android </span> SDK 버전 4.5 부터 새로운 <span class="keyword"> Android </span> 확장 기능을 사용하면 <span class="keyword"> Android </span> Wearable 앱의 데이터를 수집할 수 있습니다. </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=android_wearable" format="https" scope="external">Android Wearable 확장</a>을 참조하십시오 . </p> </td> 
  </tr> 
 </tbody> 
</table>

* 방문자 API 1.4 포함.
* DIL 버전 6.0을 사용하도록 AudienceManagement 모듈을 업데이트했습니다.

**알려진 문제**

방문자 API/ [!DNL AppMeasurement][!DNL Audience Manager] 모듈 통합에는 IE 6-9에서 수행되는 두 가지 대상 게시 iframe 요청이 있습니다. `//fast.<subdomain>.demdex.net/dest5.html` `//fast.<subdomain>.demdex.net/dest4.html`And. 다른 브라우저에 표시될 때 올바른 동작은 `//fast.<subdomain>.demdex.net/dest5.html`.

## 버전 1.4.4 {#section_C069FA04496C4F7DAC165B04E836CF1F}

릴리스 날짜: **2015년 4월 16일**

<table frame="all" colsep="1" rowsep="1" id="table_812CAB7DDC364DAABB7CDEDE55532E39"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 라이프사이클 지표가 있는 사용자 지정 데이터 </p> </td> 
   <td colname="2"> <p>이제 라이프사이클 지표가 있는 사용자 지정 컨텍스트 데이터 변수를 포함할 수 있습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Beacon tracking support in <span class="keyword"> PhoneGap </span> </p> </td> 
   <td colname="2"> <p>이제 PhoneGap에서 <code>trackBeacon</code> 및 <code>clearCurrentBeacon</code><span class="keyword"> 호출을 사용할 수 있습니다 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

`trackLight` 호출 후에 경량 서버 호출 프로필 ID를 지우도록 약간 수정되었습니다.

## 버전 1.4.3 {#section_C307052BA42248ADB1969AE7A2593177}

릴리스 날짜: **2015년 2월 19일**

* 지연된 추적 호출의 모든 처리가 일관되도록 했습니다. 이에 따라 클릭한 개체와 같이 지연 동안 백업한 변수 관련 문제가 수정되었습니다.
* 첫 번째 추적 호출 전에 *`s.referrer`*&#x200B;가 수동으로 설정되었을 때 두 번째, 세 번째 등의 추적 호출(일반적으로 링크 추적)에서 레퍼러가 두 번 계산되지 않도록 첫 번째 추적 호출 이후에 자동 레퍼러 추적을 수행하지 않도록 변경되었습니다. 
* 배포 zip이 방문자 API 1.3.5를 포함하도록 업데이트되었습니다.

## 버전 1.4.2 {#section_0A0BE40D32144A338231022F97B0E72B}

릴리스 날짜: **2015년 1월 15일**

* 보이지 않는 사전 렌더링된 페이지의 추적을 막기 위해 WebKit 사전 렌더링 처리를 수정했습니다.
* The distribution zip was updated to include Visitor API 1.3.4 and an updated **[!UICONTROL AudienceManagement]** module that includes DIL version 5.5.

## 버전 1.4.1 {#section_616FF936062F44E8B70032D18AAAFC5F}

릴리스 날짜: **2014년 9월 18일**

* 구현 시 추가적인 대시 문자 구분 기호와 함께 버전 문자열에 추가되는 최대 4개의 문자를 지정할 수 있도록 해주는 `tagContainerMarker` 변수를 추가했습니다. 이는 다이내믹 태그 관리에서 사용됩니다.

   ```js
   // JavaScript 
   s.tagContainerMarker = "D1.0"; 
   
   // Data Collection request 
   //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
   ```

   4개의 문자는 영숫자 및 마침표와 같이 URL 파일 경로에 허용되는 문자로 제한됩니다.

* H 코드로 이중 태그가 지정된 페이지에서, 강제 링크 추적이 활성화되면(Webkit 브라우저에서 기본값) 자동 링크 추적(다운로드 및 종료) 시 발생할 수 있는 루프를 수정했습니다. 또한 유사한 루프를 방지하기 위해 자동 링크 추적 주위에 일반적인 보호 조치를 추가했습니다. 이 안전 조치는 *동일한* 개체에 대한 보고된 클릭 수의 자동 링크 추적을 10초마다 한 번으로 제한합니다. 이 안전 조치는 자동 링크 추적에만 적용되므로, 수동 링크 추적(s.tl) 호출은 제한되지 않습니다. 다른 개체에 대한 클릭도 이 안전 조치의 영향을 받지 않으며, 추적됩니다.
* 지연이 필요할 때 클릭한 개체에 대한 처리를 수정했습니다.
* 방문자 API에 필요한 값이 아직 없을 경우 링크 onclick 함수에서 s.t가 호출될 때 이중 페이지 보기 카운트를 초래하던 문제를 수정했습니다.
* HTTP POST 지원.

   >[!IMPORTANT]
   >
   >For an [!DNL Analytics] call to use the POST method instead of the GET method in [!DNL AppMeasurement] (a method of solving [truncated URLs in IE](https://helpx.adobe.com/analytics/kb/shortening-image-request-urls.html)), you must be using the latest [Visitor ID Service](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_implement) implementation for Marketing Cloud.

## 버전 1.4 {#section_56ADFF9416B14ABCB3862B00F72B30A1}

릴리스 날짜: **2014년 8월 21일**

* 플러그인으로서 제거된 브라우저 플러그인(`p` 쿼리 매개 변수) 추적이 버전 15에서 더 이상 보고되지 않습니다.
* Addition of the **[!UICONTROL AudienceManagement]** Module in the download zip.

[추가 eVars](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=evars_events)(76 - 250) 및 이벤트(101-1000)에 대한 지원을 추가했습니다.

>[!NOTE]
>
>H-Code는 추가 evar 및 이벤트를 지원하지 않습니다.

[!DNL JavaScript]

## 버전 1.3.2 {#section_402A4142C4B846DE945FD59DAD9D9298}

릴리스 날짜: **2014년 6월 19일**

* Fixed handling of done and waiting flags for Visitor API fields such as the legacy [!DNL Analytics] Visitor ID, that was causing errors.
* 방문자 ID 서비스 1.3의 새로운 기능에 대한 지원

## 버전 1.3.1 {#section_5E65422B9C1E4437A2473B119A14163E}

릴리스 날짜: **2014년 5월 22일**

* [!DNL AppMeasurement] 함수의 경우 [!DNL JavaScript]`s_gi` H 코드를 사용하여 만든 인스턴스를 올바르게 찾지 `s_gi`못했습니다. Note that this issue only impacted some dual tagging implementations where [!DNL AppMeasurement] for [!DNL JavaScript] and H code were on the same page with separate instances, and `s_gi` was being used to find instances by report suite.

## 버전 1.3 {#section_56B2C625368E4A5BA1E8770A8C78117D}

릴리스 날짜: **2014년 4월 17일**

* [Marketing Cloud 방문자 ID 서비스](https://marketing.adobe.com/resources/help/en_US/mcvid/)에 대한 지원

## 버전 1.2.4 {#section_94D9521FDBAB4224994B1671A9BD036B}

릴리스 날짜: **2014년 3월 13일**

* 하트비트 비디오에 대한 버그 수정

## 버전 1.2.3 {#section_7ED201192D05463DA9B1990EC281B142}

릴리스 날짜: **2014년 2월 20일**

* 하트비트 비디오에 대한 버그 수정

## 버전 1.2.2 {#section_E6CDDDB8EE214ADCBF3047EC42711F13}

릴리스 날짜: **2014년 2월 6일**

* Fixed a compatibility issue with the [!DNL Audience Manager] DIL module. [!DNL Audience Manager] 고객은 DIL 모듈 버전 4.8로도 업데이트해야 합니다.

## 버전 1.2.1 {#section_6DA9384BC2C84698952D51FFB3732019}

릴리스 날짜: **2013년 11월 15일**

* [하트비트 비디오 측정](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/)에 사용된 페이지 이벤트를 수정했습니다.

## 버전 1.2 {#section_BDBE0C3D15F04856ABC6F111DDE6C8DB}

릴리스 날짜: **2013년 11월 14일**

* [하트비트 비디오 측정](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/)에 대한 지원이 추가되었습니다.
* [!DNL VisitorAPI.js][](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_service#)가 추가되었습니다.

## 버전 1.1.1 {#section_31F06384039648BB99F4BD630B685794}

* "opera:"로 시작하는 링크의 경우 링크 추적 호출이 Opera 브라우저에서 전송되지 않았습니다("opera:"는 다른 브라우저에서 "about:" 및 "chrome:"과 유사함).
* Added `alt=""` to all Image objects to comply with Accessible Video and Communications Act.

## 버전 1.1 {#section_4508FF0A14AE46DF96A08B5C6703E123}

릴리스 날짜: **2013년 9월 18일**

* Fixed support for placing the library and page code in the `head` tag.
* Added missing module `onLoad` support.

## 버전 1.0.3 {#section_A74A78C30067480AB36C54A06706DF89}

릴리스 날짜: **2013년 8월 15일**

* Adobe 태그 관리를 통한 배포 지원을 추가했습니다.
* Fixed an issue that prevented hierarchy variables from being set on the [!DNL AppMeasurement] object.

## 버전 1.0.2 {#section_C3BDD9A19EF84467A8FDC283AEAE2DB5}

릴리스 날짜: **2013년 7월 18일**

* 이제 해시/단편이 자동 링크 추적에서 무시됩니다. Previously the following URL was automatically tracked since the entire `href` ended in `.pdf`:

   ```js
   <a href="index.htm#anchor.pdf">Test Link</a>
   ```

   이제 해시/단편이 무시되므로 파일 이름이 일치하는 확장명으로 끝나는 경우에만 해당 링크가 추적됩니다.

## 버전 1.0.1 {#section_3758B0C47171436ABB4B29F5924BE893}

릴리스 날짜: **2013년 5월 23일**

A new [!DNL JavaScript] [!DNL AppMeasurement] library is now available in Code Manager. 이 라이브러리는 [!DNL s_code.js]의 동일한 핵심 기능을 제공하면서도, 모바일 사이트와 데스크톱 사이트 모두에서 사용할 수 있도록 보다 가볍고 빠릅니다.

* H.25 코드보다 3~7배 더 빠릅니다.
* 21k만 압축 해제되어 있고 8k는 gzip이 사용되었습니다(H.25 코드는 33k 압축 해제되어 있고 13k gzip이 사용됨).
* 쿼리 매개 변수 가져오기, 쿠키 읽기 및 쓰기, 고급 링크 추적 수행과 같은 기본 지원을 제공합니다.
* 모바일 사이트에서 사용할 수 있을 만큼 작고 빠르고 데스크톱 웹에서 사용할 수 있을 만큼 강력하므로, 모든 웹 환경에서 단일 라이브러리를 사용할 수 있습니다.

 구현 안내서의 [Javascript용 AppMeasurement](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=appmeasure_mjs)를 참조하십시오.[!DNL Analytics]

>[!NOTE]
>
>일부 플러그인은 이 새 버전에서 지원되지 않습니다. 자세한 내용은 [플러그인 지원](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=plugins_support)을 참조하십시오
