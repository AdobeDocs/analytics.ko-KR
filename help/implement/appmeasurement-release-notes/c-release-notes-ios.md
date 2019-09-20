---
description: iOS에 대한 누적 릴리스 노트입니다.
seo-description: iOS에 대한 누적 릴리스 노트입니다.
seo-title: iOS
solution: Analytics,Experience Cloud
subtopic: 릴리스 노트
title: iOS
topic: 개발자 및 구현
uuid: cc98f8f2-f619-4b31-abf9-e43f4dec64f
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# iOS{#ios}

iOS에 대한 누적 릴리스 노트입니다.

>[!NOTE]
>
>현재 라이브러리 버전을 찾으려면 디버그 로깅을 설정합니다.

모바일 라이브러리 다운로드는 [GitHub](https://github.com/Adobe-Marketing-Cloud/mobile-services) 및 [Developer Connection](https://marketing.adobe.com/developer/gallery/app-measurement-for-ios)에서 사용할 수 있습니다.

[4.x 설명서](https://marketing.adobe.com/resources/help/en_US/mobile/ios/)

[3.x 설명서](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/ios/)

## 버전 4.13.4 {#section_BF05D33CEF6E42358C8089441449449B}

The [!DNL iOS] SDK version 4.13.4 (Feb 16, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_657D643E874D47C099F2F43519C9C1C7"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App 메시징 </p> </td> 
   <td colname="2"> <p> 대상을 결정할 때 적절한 앱 버전이 사용되는 것을 막던 문제를 수정했습니다. 이 문제는 사용자가 새로운 라이프사이클을 시작하지 않고 앱 버전 업그레이드를 수행했을 때 발생했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 획득 </p> </td> 
   <td colname="2"> <p> 앱 설치 시 Apple Search Ad 데이터에 대한 API 호출 수행 전에 3초 지연을 추가했습니다(설명서의 권장에 따라). </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.13.3 {#section_39618D2B29F942FCBF37E4F5507AA131}

The [!DNL iOS] SDK version 4.13.3 (Jan 19, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_341D35BF18714139A95CA5491899185D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App 메시징 </p> </td> 
   <td colname="2"> <p> 이제 VoiceOver가 실행될 때 전체 화면 메시지를 비활성화할 수 있습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Analytics</span> </p> </td> 
   <td colname="2"> <p> 읽기 전용 데이터베이스 액세스 처리를 개선했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>일반 </p> </td> 
   <td colname="2"> <p> 앱 그룹을 사용하는 동안 백그라운드에서 추적 메서드를 호출할 때 경우에 따라 충돌을 일으킬 수 있는 문제를 해결했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.13.2 {#section_CB0DFFDB38FE4D14A84423DF40BF8FD3}

The [!DNL iOS] SDK version 4.13.2 (Nov 10, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AA26B14D271948FFBA44D4D06E3B71AA"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 방문자 ID 서비스 </p> </td> 
   <td colname="2"> <p> Added timestamp and Experience Cloud Organization ID to <code> adobe_mc</code> parameter. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 구성 </p> </td> 
   <td colname="2"> <p> <code>setAdvertisingIdentifier:</code>를 통해 SDK에 전달된 잘못된 IDFA(00000000-0000-0000-0000-000000000000)가 무시됩니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 심층 연결 </p> </td> 
   <td colname="2"> <p><code>trackAdobeDeepLink</code>를 호출할 때 이제 "<code>adb</code>" 및 "<code>ctx</code>" 접두사가 붙은 변수가 제대로 처리됩니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 획득 </p> </td> 
   <td colname="2"> <p>이제 Apple 검색 광고의 데이터가 획득 데이터와 함께 전송됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.13.1 {#section_18C8A7166EFD4E67AC0F7C06DFBBFE6A}

The [!DNL iOS] SDK version 4.13.1 (Oct 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_5B67A6B8B79D4783BA8DCDA7C2ACA765"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 획득 </p> </td> 
   <td colname="2"> <p> 이제 SDK는 사용자 지정 획득 데이터가 <code>AdobeDataCallback</code> 호출에 의해 적절하게 반환되도록 지원합니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Target </p> </td> 
   <td colname="2"> <p> 이제 <span class="keyword">방문자 ID 서비스</span> 매개 변수가 <span class="keyword">mboxParams</span>를 통해 <code>Target</code> 요청에서 전달됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**버그 수정**

* 추적 히트를 [!DNL Adobe Analytics]에 보낼 때 동시에 새로운 ID를 방문자 ID 서비스에 동기화하려 하면 충돌이 발생하는 문제를 수정했습니다.
* Fixed an issue that was causing build warnings when targeting [!DNL iOS] versions older than 8.

## 버전 4.13.0 {#section_F72A3357994E4887A9F3967F0FBFFCDD}

The [!DNL iOS] SDK version 4.13.0 (Sep 15, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_FD6156E58FF54BA2BEED7398BC780C46"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App 메시징 </p> </td> 
   <td colname="2"> <p>새로운 기능: 딥링크 URI를 여는 새 메시지 유형이 추가되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.12.0 {#section_2AD26AABBB434833AE961C8D71C9AFE8}

The [!DNL iOS] SDK version 4.12.0 (Aug 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_CC3CD01203ED4BDA9BC26427E925C70D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>방문자 ID 서비스 </p> </td> 
   <td colname="2"> <p> 방문자 ID를 주어진 URL에 더하여 ID를 웹 기반 구현으로 전송하는 새로운 방법이 추가되었습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>In-App 메시징 </p> </td> 
   <td colname="2"> <p>사용자 지정 전체 화면 메시지의 HTML 태그에서 "타겟" 특성을 "_blank"로 설정할 때 충돌을 일으킬 수 있는 문제가 해결되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.11.0 {#section_3ABABE0F0B964EB48BD482CCE260A13D}

The [!DNL iOS] SDK version 4.11.0 (June 22, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_14B23402BA3B41238F419CA57341B8F5"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>타겟 메서드 </p> </td> 
   <td colname="2"> <p>이제 다음의 새로운 <span class="keyword">Target</span> 메서드를 사용할 수 있습니다. </p> <p> 
     <ul id="ul_93CDE46E39C9431DA9104664F175708B"> 
      <li id="li_903FAC68526B4B7CB6555DC577CE493A"><code> targetLoadRequestWithName:defaultContent:profileParameters:orderParameters:mboxParameters:requestLocationParameters:callback:</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.10.0 {#section_F0D6D7FD89DE4DF5A121B05FA093CC5B}

The [!DNL iOS] SDK version 4.10.0 (May 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AC447B6E4D55489F803923BF5D1D6653"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>타겟 메서드 </p> </td> 
   <td colname="2"> <p>이제 다음의 새로운 <span class="keyword">Target</span> 메서드를 사용할 수 있습니다. </p> <p> 
     <ul id="ul_D0594A9ABFD8448186DED87599A0E50E"> 
      <li id="li_A4B0ECDF200C438BB1AB24D613453A68"><code> targetLoadRequestWithName:defaultContent:profileParameters:orderParameters:mboxParameters:callback:</code> </li> 
      <li id="li_C0FADBB3CEE141AE951CBD49F3A52642"><code> targetThirdPartyID</code> </li> 
      <li id="li_3E1B3725D9EE4ECE9DB0EB1A9E7682A4"><code> targetSetThirdPartyID:</code> </li> 
      <li id="li_659E295610F541819DD7486FC5177012"><code> targetPcID</code> </li> 
      <li id="li_B00ADCF98B6D4694BB7664DB42CDFF99"><code> targetSessionID</code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>TVJS 메서드 </p> </td> 
   <td colname="2"> <p>이제 다음의 새로운 <span class="keyword">Target</span> TVJS 메서드를 사용할 수 있습니다. </p> <p> 
     <ul id="ul_AED76A2B99534CF3A472AC0381B2618C"> 
      <li id="li_AA731652996C4A19A8E02D5D6B8BDC93"><code> targetThirdPartyID</code> </li> 
      <li id="li_744A63A62A8045E49C75F9D7AED5D75E"><code> targetSetThirdPartyID</code> </li> 
      <li id="li_72BC8D96FE0549A695D90B924FA80A02"> <code> targetPcID</code> </li> 
      <li id="li_FB7A9435B9994DB89FA80C2B2218C047"> <code> targetSessionID</code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>TVML/TVJS용 Adobe Target </p> </td> 
   <td colname="2"> <p>이제 <code>ADBTarget</code> 요소를 구성할 때 다음 속성 이름을 사용할 수 있습니다. </p> <p> 
     <ul id="ul_A0CEE891AE644B47ABD6F7425ACD464D"> 
      <li id="li_2EB0C3CA52014F45BA1EC07703E821B8"><code> ID</code> </li> 
      <li id="li_069D996CED534EE88A1EC82684E470D5"><code> total</code> </li> 
      <li id="li_97F290C03FFD46B8A1E78B7BF2021F55"> <code> purchasedProductIds</code> </li> 
      <li id="li_FAAC4BB12DF9491DA21F161711A7707D"> <code> mboxParameters</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.9.0 {#section_DA97D7294B214067A4904B9738450759}

The [!DNL iOS] SDK version 4.9.0 (May 5, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_0B3A0F44549C4DA48C7639048C030065"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>심층 연결 </p> </td> 
   <td colname="2"> <p>애플리케이션에서 심층 연결을 구현하여 사용자를 앱 또는 웹 링크 대상으로 데려갈 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.8.6 {#section_0150641B44CF4F6CBE2B21002F8EAB30}

The [!DNL iOS] SDK version 4.8.6 (March 9, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_5175CFFCA30B4DDBACFB23532111CB8A"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>앱 충돌 추적 </p> </td> 
   <td colname="2"> <p>The <span class="keyword"> iOS</span> SDK version 4.8.6 contains critical changes that prevent false crashes from being reported. 버전 4.8.6으로 업데이트할 것을 강력히 권장합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.8.5 {#section_F42EB64F91024748893E89575F2E4487}

The [!DNL iOS] SDK version 4.8.5 (February 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AB225AF04A374421BDD8A972506ACD06"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>옵트아웃 및 개인 정보 설정 </p> </td> 
   <td colname="2"> <p>Starting with <span class="keyword"> iOS</span> SDK 4.8.5, privacy settings set via the <code> setPrivacyStatus</code> method affect activity from <span class="keyword"> Analytics</span>, <span class="keyword"> Target</span>, and <span class="keyword"> Audience Manager</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.8.0 {#section_2CF142C8C2D24B529559DAF76F851BBF}

The [!DNL iOS] SDK version 4.8.0 (November 2, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_9DB41F070D66498FACF1A9C135603C7A"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> 새로운 Experience Cloud 방문자 ID 서비스 메서드 </td> 
   <td colname="2"> <p>다음과 같은 새로운 메서드를 추가했습니다. </p> 
    <ul id="ul_55D8F29ADE3746C484FEC7893FA9EF23"> 
     <li id="li_19F8AF546EEB45EBB5849EA6EB3CE6A3"><code> visitorSyncIdentifiers:authenticationState:</code> </li> 
     <li id="li_1AF1CF62B3ED442D81B438ECBF981583"><code> visitorSyncIdentifierWithType:identifier:authenticationState: </code> </li> 
     <li id="li_C116F0DA8E2A449A8B76637961C2100C"><code> visitorGetIDs</code> </li> 
    </ul> <p><code>visitorSyncIdentifiers:identifiers</code> 메서드를 <code>visitorSyncIdentifiers</code>로 변경했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> 새로운 TVJS 메서드 </td> 
   <td colname="2"> <p>다음과 같은 새로운 메서드를 추가했습니다. </p> 
    <ul id="ul_4C7F4BB1CF744444ABAA9F13BA98749E"> 
     <li id="li_5DAB089D115843CCA0A53873D6D676F0"><code> visitorSyncIdentifiersAuthenticationState</code> </li> 
     <li id="li_EDE2D1301E8648DB88A18D8C9F6A22C5"><code> visitorSyncIdentifierWithTypeIdentifierAuthenticationState</code> </li> 
     <li id="li_2CCED3C707774597934A2F08BC690B15"><code> visitorGetIDsJs</code> </li> 
    </ul> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> 새로운 ADBMobile JSON 구성 변수  </td> 
   <td colname="2"> <p>다음 변수를 추가했습니다. </p> 
    <ul id="ul_95065BC06FD540D2937D11111799F77F"> 
     <li id="li_7C8C68A41FBA4D098D6803E71D4CCF7A"><code> analyticsForwardingEnabled</code> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.7.0 {#section_B37B1CAF065346E9A2073A06AB7AFEC2}

The [!DNL iOS] SDK version 4.7.0 (October 15, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_3CCA327B859B498D828B2E056A075BEC"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> tvOS 지원 </td> 
   <td colname="2"> <p>Apple TV용의 tvOS가 지원됩니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> 앱 전송 보안 지원 </td> 
   <td colname="2"> <p>Starting with <span class="keyword"> iOS</span> 9, Apple introduced App Transport Security, a set of requirements that conforms to best practices for secure connections. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> PhoneGap 플러그인 메서드</span> </p> </td> 
   <td colname="2"> <p>다음과 같은 새로운 메서드를 추가했습니다. </p> <p><b>구성 메서드</b> </p> <p> 
     <ul id="ul_98C5E7B5C79446EEA00F0E7CBC213301"> 
      <li id="li_B403C06E57A0450CBB4ABAD45170C681">setPushIdentifier </li> 
      <li id="li_6D76C40601544D4FA13FD44F390C83CE">setAdvertisingIndentifier </li> 
      <li id="li_7D03005DBD9E4AC7BB78BA162CDC8153">keepLifecycleSessionAlive </li> 
      <li id="li_3DDE07508B764E679AF2ACECC4D935CB">trackingSendQueuedHits </li> 
     </ul> </p> <p><b>추적 메서드</b> </p> <p> 
     <ul id="ul_9B6002F5642B4D888FBD0A8D44EF32DB"> 
      <li id="li_5C1C9EA770E048E48723528F346712B4">trackPushMessageClickthrough </li> 
     </ul> </p> <p>새로운 Target 메서드: </p> <p> 
     <ul id="ul_E6A481FCD49D4CF48A4B0636312FCD19"> 
      <li id="li_6604FBB05C4E4988A04CB376D6667C79">targetClearCookies </li> 
     </ul> </p> <p><b>획득 메서드</b> </p> <p> 
     <ul id="ul_2015BFF019E64D5685A25E20D4B4A79B"> 
      <li id="li_D450F60189904C43BDAC5D658324AEAA">acquisitionCampaignStartForApp </li> 
     </ul> </p> <p><b>Audience Manager 메서드</b> </p> <p> 
     <ul id="ul_7D5F339A1A004593AE1D5C26A5A495C5"> 
      <li id="li_2F44037A508D49308F42961FDFB6486C">audienceGetVisitorProfile </li> 
      <li id="li_4F8F43C875384A74ADD48D4197C2ACFD">audienceGetDpuuid </li> 
      <li id="li_B38B6700AF2F4B9FA80CC6774B5B14E7">audienceGetDpid </li> 
      <li id="li_12579B472B404ABAA12DFBDBB22A0C30">audienceSetDpidAndDpuuid </li> 
      <li id="li_2CA997AF9FE241FD961BB0A9B50E14D9">audienceSignalWithData </li> 
      <li id="li_3545CB51B6B7409D8CE2B97E291267E6">audienceReset </li> 
     </ul> </p> <p><b>방문자 ID 서비스 메서드</b> </p> <p> 
     <ul id="ul_746B8A36715D4075B11C42F9FE82F538"> 
      <li id="li_A15AFA632E8C4C8D931CAB48B9A29ADB">visitorGetMarketingCloudId </li> 
      <li id="li_D80DD8DDE6AB4CB6BEE37DAA9BB28A98">visitorSyncIdentifiers </li> 
     </ul> </p> <p><b>앱 확장 및 Apple Watch 메서드</b> </p> <p> 
     <ul id="ul_66B1E1AC4A6D4970B0C77A46EA14ABA7"> 
      <li id="li_1EA7A063FED04E0585D463837A7555CE">setAppGroup </li> 
      <li id="li_5869EAB018C94EE4AC28B3EE62D9F0EF">syncSettings </li> 
      <li id="li_983A98CAEBAD404EBCE1D70CB0B52BA3">initializeWatch </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.6 {#section_D091872501DA49C1A18CDC33C84B8256}

The [!DNL iOS] SDK version 4.6 (September 17, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_084C27B1A75A4A2EB84822242E37ED35"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Push Messaging to <span class="keyword"> Analytics</span> Segments </p> </td> 
   <td colname="2"> <p> <span class="keyword"> Adobe Mobile Services</span> 및 <span class="keyword">Adobe Mobile</span> SDK를 사용하면 푸시 메시지를 <span class="keyword">Analytics</span> 세그먼트에 보낼 수 있습니다. 또한 SDK를 사용하면 푸시 메시지를 연 결과로서 앱을 연 사용자를 쉽게 보고할 수도 있습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>획득 메서드 </p> </td> 
   <td colname="2"> <p>사용자가 링크를 클릭한 것처럼 개발자가 앱 획득 캠페인을 시작할 수 있도록 해줍니다. 이것은 수동 획득 링크를 만들고 앱스토어 리디렉션을 직접 처리하는 데 도움이 됩니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>포스트백 </p> </td> 
   <td colname="2"> <p>포스트백을 이용하면 SDK로 수집한 데이터를 별도의 타사 서버에 보낼 수 있습니다. 인앱 메시지를 표시하는 데 사용하는 것과 동일한 트리거와 트레이트를 이용하면 사용자 지정된 데이터를 타사 대상에 보내도록 SDK를 구성할 수 있습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>식별자 </p> </td> 
   <td colname="2"> <p>다음의 새 식별자를 추가했습니다. </p> <p> 
     <ul id="ul_22EF89556F6B481ABE0D1B9C5EE70B55"> 
      <li id="li_C41F6FAC0B334B89B8B5D1A517CA2301"> <code> setPushIdentifier</code> </li> 
      <li id="li_B7893FB0453340EDB4290BC0B47BF096"><code> setAdvertisingIdentifier</code> </li> 
      <li id="li_85EF5F2B8837497B90F782946283622E"><code>trackPushMessageClickThrough</code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>WatchOS 2용 WatchKit 지원 </p> </td> 
   <td colname="2"> <p>WatchOS 2용 WatchKit 지원을 추가했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.5 {#section_53DFAF8CFD614F69B3168014EF84DE9F}

The [!DNL iOS] SDK version 4.5 includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_A69D0B8DA45348B8A5D6A014126F97C2"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> iOS 확장</span> </p> </td> 
   <td colname="2"> <p>Starting in <span class="keyword"> iOS</span> SDK version 4.5, a new <span class="keyword"> iOS</span> extension lets you collect usage data from your Apple Watch Apps, Today Widgets, Photo Editing widgets, and all the other <span class="keyword"> iOS</span> extension apps. </p> <p>We strongly recommend that you use the <span class="keyword"> iOS</span> SDK rather than using your own wrapper. </p> <p>Apple에서는 Watch 앱이 포함 앱과 통신(요청을 포함 앱에 보낸 다음, 응답을 받음)할 수 있도록 해주는 API 세트를 제공합니다. </p> <p>Watch 앱의 사전으로서 추적 데이터를 포함 앱에 전송한 다음, 포함 앱에서 추적 메서드를 호출하여 데이터를 전송할 수 있지만, 이 해결 방법에는 제한이 있습니다. </p> <p>대부분의 경우, 사용자가 Watch 앱을 사용할 때 포함 앱은 배경에서 실행되며 <code>TrackActionInBackground</code>, <code>TrackLocation</code> 및 <code>TrackBeacon</code>을 호출해야만 안전합니다. 다른 추적 메서드를 호출하면 라이프사이클 데이터가 방해되므로, 이 세 메서드만 사용하여 Watch 앱의 데이터를 전송해야 합니다. </p> <p>Even if these three tracking methods meet your requirements, we recommend using the <span class="keyword"> iOS</span> SDK because the SDK for watch app includes all <span class="keyword"> Mobile</span> features except in-app messaging. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.4 {#section_0B7A98761BF0400986C368E154A3B00B}

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
   <td colname="1"> <p>Beacon tracking support in <span class="keyword"> PhoneGap</span> </p> </td> 
   <td colname="2"> <p>이제 PhoneGap에서 <code>trackBeacon</code> 및 <code>clearCurrentBeacon</code><span class="keyword"> 호출을 사용할 수 있습니다</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.3 {#section_0FD2B2C4F54E4A9E8C6D0CD2F103BB9A}

릴리스 날짜: **2014년 11월 24일**

* 새로운 기능 - Adobe Experience Cloud ID 통합
* 명확성을 위해 디버그 로그가 개선됨

## 버전 4.2 {#section_806710F7720C410DAB46376C0A7A283E}

릴리스 날짜: **2014년 10월 16일**

* 새로운 기능 - 인앱 메시징 기능
* 새로운 기능 - 이제 앱 시작 동안 구성 파일의 위치를 지정할 수 있습니다. 
* 새로운 기능 - 이제 새 구성 파일이 없어도 관심 영역을 자동으로 업데이트할 수 있습니다.
* New - [!DNL Analytics] calls are now sent as HTTP POST requests.
* debugLogging이 활성화되었을 때 로그 메시지가 정리되고 자세한 기록이 추가되었습니다.
* 성능 및 안정성 기능이 다양하게 개선되었습니다.

## 버전 4.1.3 {#section_8D679B676F604E0B9A64748569185368}

릴리스 날짜: **2014년 9월 18일**

* Resolved potential crash that could occur if Audience Manager Submit Signal call or [!DNL Target] Load Request call failed due to an unknown network error.

## 버전 4.1.2 {#section_6128902E5AE142C4A95D2FB3053188F8}

릴리스 날짜: **2014년 8월 5일**

* 특정 구성 privacyStatus:optunknown 및 offlineEnabled:false를 사용할 때 발생할 수 있는 교착 상태 문제를 해결했습니다.

릴리스 날짜: **2014년 8월 4일**

* 레퍼러 제한 시간이 5초 이상이고 오프라인 추적이 비활성화되었을 때 라이프사이클 히트가 전송되지 않던 문제를 해결했습니다.

릴리스 날짜: **2014년 4월 17일**

* 블루투스 비콘 추적
* 앱 획득 분석.
* 타임스탬프가 활성화된 앱에서 충돌 히트 수가 올바른 세션으로 백데이트됩니다.
* 타임스탬프가 활성화된 앱에서 이전 세션이 올바른 세션으로 백데이트된 히트에서 전송됩니다. (더 이상 이전 세션은 없음)
* 히트 배치 처리.

## 버전 4.0.2 {#section_B78AE82CDFAD44DCAC6D61E0B80BF4C8}

릴리스 날짜: **2014년 2월 20일**

* 이전 미디어 항목을 닫지 않고 동일한 미디어 항목을 순서대로 열었을 때 잘못된 동작을 일으키는 문제를 해결했습니다.

## 버전 4.0.1 {#section_A6D017015BC742F69B6EE4A461D00FD7}

릴리스 날짜: **2014년 1월 30일**

* 데이터베이스가 손상되었을 때 여러 히트가 전송될 수 있었던 문제를 해결했습니다.
* 장치의 시간 설정이 올바르지 않은 경우 세션 길이 평균이 커지도록 하는 문제를 해결했습니다.

## 버전 3.3.2 {#section_6D12768F20C44BA4A0D1EA607D367147}

릴리스 날짜: **2014년 1월 30일**

* 장치의 시간 설정이 올바르지 않은 경우 세션 길이 평균이 커지도록 하는 문제를 해결했습니다.

## 버전 4.0.0 {#section_79DCFAAF1DCB404898E3BE389AC835A6}

릴리스 날짜: **2013년 9월 27일**

[!DNL iOS] Experience Cloud 솔루션용 SDK 4.x는 이제 다음과 같은 새로운 기능을 제공합니다.

* 현저한 성능 개선 모든 처리가 백그라운드 스레드에서 수행되고 SDK는 완전히 스레드 안전 상태입니다.
* 지리적 위치 및 관심 영역
* 라이프타임 값
* 시한 이벤트
* 옵트인/옵트아웃 관리
* Audience Manager 지원
* Lifecycle metrics passed to [!DNL Target] as mbox parameters
* 컨텍스트 데이터 및 처리 규칙에 대해 표준화

## 버전 3.3.0 {#section_28FB7CD64D6C49BF93E321587F1E8950}

릴리스 날짜: **2013년 9월 23일**

* ARM64 및 X64 시뮬레이터 아키텍처에 대한 지원을 추가했습니다(iPhone 5s).

## 버전 3.2.1 {#section_3E73A76401664C54B32C7F3BE8BE36E3}

릴리스 날짜: **2013년 8월 16일**

* 사용하지 않은 코드를 제거하여 최적화했습니다.
* clearVars가 스레드 시나리오에서 사용되었을 때 발생할 수 있었던 잠재적인 충돌을 해결했습니다.

## 버전 3.2 {#section_A51E0EB26EF246DABE27234C77598D99}

릴리스 날짜: **2013년 8월 6일**

* Adobe Audience Manager에 대한 지원이 추가되었습니다.
* Lifecycle data is now sent with [!DNL Target] Mbox requests when lifecycle tracking is enabled.

## 버전 3.1.8 {#section_849BCD1D4379433D874B8A0E0099E2B1}

릴리스 날짜: **2013년 6월 20일**

* Fixed a bug introduced in 3.1.7 that was causing issues with lifecycle on devices below [!DNL iOS] 5.0.

## 버전 3.1.7 {#section_EC59B76EE3A343D5921E906EB0A8DB49}

릴리스 날짜: **2013년 5월 23일**

* 앱을 시작하는 위치 알림 및 Newsstand 알림을 통해 과도한 라이프사이클 히트가 전송되지 않도록 하는 코드를 추가했습니다.

## 버전 3.1.6 {#section_4617D7A41D0841BEBD5829001DC74854}

릴리스 날짜: **2013년 4월 18일**

* 이전 세션 길이를 종종 잘못 계산되도록 하던 문제를 해결했습니다.

## 버전 3.1.5 {#section_620AA594868F47619A514AF3C1EAC93B}

릴리스 날짜: **2013년 3월 21일**

* `ADMS_Measurement.visitorID` 이제 기본값으로 미리 채워집니다.

## 버전 3.1.4 {#section_B04D1A4858A84A19AA65A57609C9F53F}

릴리스 날짜: **2013년 2월 21일**

* 설정으로서 가치가 떨어진 `offlineThrottleDelay`는 스레드 최적화로 인해 더 이상 필요하지 않습니다. 이 설정은 이전 버전과의 호환성을 유지하기 위해 남아 있을 뿐 더 이상 어떤 효과도 없습니다.

## 버전 3.1.3 {#section_CCFAE5A29FB14DAD9A9F14FE8EE09B75}

릴리스 날짜: **2012년 11월**

* Products 변수를 수동으로 설정할 때 잠재적인 EXEC_BAD_Access 문제를 해결했습니다.
* mbox가 시간 초과될 때 발생할 수 있었던 유효하지 않은 선택기 충돌을 해결했습니다.
* 미디어 측정에 대한 광고 추적 지원을 추가했습니다.

## 버전 3.1.2 {#section_25C8A6B67AB9487BA5DEB4DB196AE4BC}

릴리스 날짜: **2012년 10월**

* 앱 시작이 새 세션으로 간주하기 전 앱이 시작되는 사이 경과해야 하는 시간(초)을 지정할 수 있게 해주는 `lifecycleSessionTimeout` 구성 변수가 추가되었습니다.
* 측정 개체에 설정된 이벤트가 미디어 모듈에 의해 설정된 이벤트를 덮어쓰는 미디어 모듈 문제를 수정했습니다.
* Fixed an issue that caused an exception when allocating an mbox through the [!DNL Target] integration.

## 버전 3.1.0 {#section_0F3E939885DE4DF1B7430DF5F5749AD2}

릴리스 날짜: **2012년 9월**

* armv7s 아키텍처 지원이 추가되었습니다.
* armv6 아키텍처 지원이 제거되었습니다.
* Minimum supported [!DNL iOS] SDK is now 4.3

## 버전 3.0.2 {#section_1224693620524D6C8CCAB7707483536E}

릴리스 날짜: **2012년 8월**

* 미디어 모니터 위임을 사용하는 고객은 더 이상 두 개의 닫기 이벤트를 볼 수 없습니다.
* 가끔 닫기 히트로 인해 미디어 모니터에서 루프 조건이 발생하게 되는 문제를 해결했습니다.

## 버전 3.0 {#section_D28F56359EC04EDC8521BE93750AE90D}

릴리스 날짜: **2012년 7월**

초기 릴리스.

**향상된 기능**

* "자동 추적" 기능이 추가되었습니다.
* 라이브러리 크기가 appx로 축소되었습니다. 최종 빌드에서 90k입니다.
* "trackEvents" 및 "trackAppState" 메서드가 추가되었습니다.
* 컨텍스트 데이터 지원 및 기능이 개선되었습니다. (전송된 모든 정보에 컨텍스트 데이터 사용 권장)
* 추적이 간소화되어 기본 추적 구현이 5분 이내에 완료될 수 있습니다.

**변경 사항**

* [!DNL AppMeasurement] Class는 현재 ADMS_Measurement입니다.
* ADMS_Measurement는 현재 적절한 Singleton으로 작동하고 있습니다.
* eVars, prop, lists, hier, pev의 getter 및 setter가 변경되었습니다.
* "track" 호출로 전달되는 모든 변수가 해당 호출에 대해서만 지속됩니다.

**다음 변수 수정**

| 이전 버전(2.x) | 현재 버전(3.x) |
|---|---|
| 계정 | reportSuiteIDs |
| dc | dataCenter |
| pageName | appState |
| contextData | persistentContextData |
| state | geoState |
| zip | geoZip |
| server | appSection |
| debugTracking | debugLogging |
| trackOffline | offlineTrackingEnabled |
| offlineLimit | offlineHitLimit |
| OfflineThrottleDelay | offlineThrottleDelay |

**다음 변수의 용도 변경:**

* linkURL(trackLinkURL과 함께 전송:)
* linkName(trackLinkURL과 함께 전송:)
* linkType(trackLinkURL과 함께 전송:)
* lightProfileID(trackLight와 함께 전송:)
* lightStoreForSeconds(trackLight와 함께 전송:)
* lightIncrementBy(trackLight와 함께 전송:)
* trackingServerSecure(trackingServer는 ssl이 켜졌을 때 사용됨)

**다음 변수 삭제:**

* timestamp
* userAgent
* dynamicVariablePrefix
* visitorNamespace
* pageURL
* pageType
* referrer
* linkLeaveQueryString
* usePlugins
* useBestPractices(AutoTracking에 의해 처리됨)
* 위임
* retrieveLightData
* deleteLightProfiles
* retrieveLightProfiles

## 이전 iOS 버전(2.x) {#section_5F76C3DA854D4BAEA636A68B3811142B}

The following release notes apply to the 2.x version of [!DNL AppMeasurement] for [!DNL iOS]. 가능하면 3.x 버전으로 업그레이드할 것을 권장합니다.

## 버전 2.1.12 {#section_85C073B86B684D52A14E8038379F56DD}

릴리스 날짜: **2012년 4월**

*  비디오 측정에 대한 지원이 추가됨.
* linktrackvars 및 컨텍스트 데이터 관련 문제가 해결되었습니다.
* 몇 가지 성능이 추가로 개선되었습니다.

## 버전 2.1.11 {#section_F0AF2D4E5F504D798EEB95BE8FE61B4C}

릴리스 날짜: **2012년 3월**

* 일부 상황에서 오프라인 추적에서 데이터 전송이 중지되던 문제가 수정되었습니다.

## 버전 2.1.10 {#section_07C24EC83AA94A6AA6AB3DE7E8D6227F}

릴리스 날짜: **2012년 2월**

* 일부 환경에서 여러 개의 스레드가 동시에 추적 호출을 지정하려고 하면 EXC_BAD_ACCESS 예외가 발생하는 문제를 수정했습니다.
* 추적 호출에 사용된 변수(trackLight)에 타임스탬프를 추가했습니다.

## 버전 2.1.8 {#section_ACC6974CE3F741E58786CA8048F04521}

릴리스 날짜: **2012년 1월**

* 추적 스레드의 성능이 크게 향상되었습니다.
* iCloud 우수 사례를 따르기 위해 iCloud와 동기화되지 않은 위치로 오프라인 히트 스토리지를 이동했습니다.
* 라이브러리를 Apple FAT 이진 형식으로 업데이트했으므로 빌드 아키텍처에 대한 특정 라이브러리를 더 이상 포함시킬 필요가 없습니다.

## 버전 2.1.6 {#section_63B4967C537847C28D33EBB92CC15695}

릴리스 날짜: **2011년 11월**

* Added support for [!DNL iOS] 5.
* [!DNL AppMeasurement] for [!DNL iOS] 이 더 이상 visitorID의 기본값으로 사용되지 않도록 업데이트되었습니다. 애플리케이션에서 사용자 지정 visitorID를 설정하는 경우(예: `s.visitorID = @12345`) 이러한 변경의 영향을 받지 않습니다. 사용자 지정 visitorID를 설정하지 않은 경우 visitorID 값으로 UDID를 사용하는 대신 초기 실행 시 임의의 visitorID가 생성되어 사용자 기본 키에 저장됩니다. This key is used by [!DNL AppMeasurement] from that point forward. 또한 이 키는 표준 애플리케이션 백업 프로세스 시 저장되고 복원됩니다.

* Updated calls from the [!DNL iOS] Best Practices plug-in that are not associated with a page view to send hits using trackLink. 이러한 히트가 "애플리케이션 이름/버전" 이름의 기본값으로 페이지 뷰를 기록하는 것을 방지할 수 있습니다.

## 버전 2.1.3 {#section_E39666D780554B7398900C39C285CDB8}

릴리스 날짜: **2011년 10월**

* 위임 처리가 향상되었습니다. This fixes an issue that caused the [!DNL iOS] Best Practices Plug-in to crash when bringing the application out of the background.

## 버전 2.1.2 {#section_21014073AF804EFC8231047D8847485C}

릴리스 날짜: **2011년 9월**

* prop 및 eVar 51-75를 사용할 수 있도록 헤더를 업데이트했습니다.

## 버전 2.1.1 {#section_8FB3D7C77C884E2AB982103BF7E3312A}

릴리스 날짜: **2011년 8월**

* 보고서 실행 시 보고서 세트와 지표를 검색할 수 있습니다.
* 서버측 처리 규칙을 유도하는 contextData를 지원합니다(v15만 해당).
* 라이트 서버 호출을 지원합니다(현재 베타 버전).

