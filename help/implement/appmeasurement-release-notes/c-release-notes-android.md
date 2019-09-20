---
description: Android 모바일 라이브러리에 대한 누적 릴리스 노트입니다.
seo-description: Android 모바일 라이브러리에 대한 누적 릴리스 노트입니다.
seo-title: Android
solution: Analytics,Experience Cloud
subtopic: 릴리스 노트
title: Android
topic: 개발자 및 구현
uuid: 32232d28-3459-4f78-bb00-ca3163c63461
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Android{#android}

Android 모바일 라이브러리에 대한 누적 릴리스 노트입니다.

>[!NOTE]
>
>현재 라이브러리 버전을 찾으려면 디버그 로깅을 설정합니다.

모바일 라이브러리 다운로드는 [GitHub](https://github.com/Adobe-Marketing-Cloud/mobile-services) 및 [Developer Connection](https://marketing.adobe.com/developer/gallery/app-measurement-for-android-1)에서 사용할 수 있습니다.

## 버전 4.13.4 {#section_E4743079D8E64B9C890180A025C94B44}

The [!DNL Android] SDK version 4.13.4 (Feb 16, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_C0197701CB9B45E596818AF0BE5AC4F2"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> In-App 메시징 </p> </td> 
   <td colname="2"> <p> 대상을 결정할 때 적절한 앱 버전이 사용되는 것을 막던 문제를 수정했습니다. 이 문제는 사용자가 새로운 라이프사이클을 시작하지 않고 앱 버전 업그레이드를 수행했을 때 발생했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>라이프사이클 </p> </td> 
   <td colname="2"> <p> 앱 버전 업그레이드가 제대로 보고되지 않도록 할 수 있었던 문제를 해결했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>획득 </p> </td> 
   <td colname="2"> <p> 지연된 심층 링크가 첫 번째 시작 시 트리거되지 않던 버그를 수정했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.13.3 {#section_1C235192E9FB46E2A651017C1CF24A7F}

The [!DNL Android] SDK version 4.13.3 (Jan 19, 2017) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_5E744C8C9D064E999EB5055A8E3A99C5"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> In-App 메시징 </p> </td> 
   <td colname="2"> <p> 클릭스루 단추가 없는 경고 메시지가 표시되지 않는 문제를 해결했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Analytics</span> </p> </td> 
   <td colname="2"> <p> 읽기 전용 데이터베이스 액세스 처리를 개선했습니다. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>범용 링크 </p> </td> 
   <td colname="2"> <p> 지연된 딥링크가 획득 데이터에 첨부되어 연속 실행을 수행하는 버그를 수정했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.13.2 {#section_CEA2FF01EA414A32A8D164D981FBE71F}

The [!DNL Android] SDK version 4.13.2 (Nov 10, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_812CAB7DDC364DAABB7CDEDE55532E39"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 방문자 ID 서비스 </p> </td> 
   <td colname="2"> <p>Added timestamp and Experience Cloud Organization ID to <code> adobe_mc</code> parameter. </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p> 심층 연결 </p> </td> 
   <td colname="2"> <p><code>trackAdobeDeepLink</code>를 호출할 때 이제 "<code>adb</code>" 및 "<code>ctx</code>" 접두사가 붙은 변수가 제대로 처리됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.13.1 {#section_647C43BA95A3485381AC2E8DEAA6D2E4}

The [!DNL Android] SDK version 4.13.1 (Oct 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_1D1AFD90F8BB4F59869FD417ED9C45AB"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>획득 </p> </td> 
   <td colname="2"> 이제 SDK는 사용자 지정 획득 데이터가 <code>AdobeDataCallback</code> 호출에 의해 적절하게 반환되도록 지원합니다. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>획득 </p> </td> 
   <td colname="2"> 이제 SDK는 Google Play 참조 변수와 사용자 지정 변수를 보관했다가 <code>AdobeDataCallback</code> 호출에서 적절히 반환합니다. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Target </p> </td> 
   <td colname="2"> 이제 방문자 ID 서비스 매개 변수가 <span class="keyword">mboxParams</span>를 통해 <code>Target</code> 요청에서 전달됩니다. </td> 
  </tr> 
 </tbody> 
</table>

**버그 수정**

* 전화에 대한 데이터 요청 시간이 때로 초과되는 버그를 수정했습니다.

## 버전 4.13.0 {#section_03370D8F93AE4B7A81C4B03910086556}

The [!DNL Android] SDK version 4.13.0 (Sept 15, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_AACF8B9BE89A4057B0396F487F82CF99"> 
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
  <tr rowsep="1"> 
   <td colname="1"> <p>딥링크 추적 </p> </td> 
   <td colname="2"> <p>새로운 기능: 타사 지연 딥링크를 추적할 수 있는 기능이 추가되었습니다. </p> <p> 
     <ul id="ul_DA54F09098A546B6A320E6B9F2937DAD"> 
      <li id="li_B483AEBE02F34E21B2CC731FC77448E8"><code> processAdobeDeepLink</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.12.0 {#section_3FBC1C24267141C08A60E288662160D8}

The [!DNL Android] SDK version 4.12.0 (Aug 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_3BDD15254859475CBE5E27870619FF3A"> 
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
 </tbody> 
</table>

## 버전 4.11.0 {#section_34B295F3697F4AD6B6A6B8DD70AD1ECA}

The [!DNL Android] SDK version 4.11.0 (June 22, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_C3DC3890E81744828DE8946AE8067E1A"> 
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
      <li id="li_A4B0ECDF200C438BB1AB24D613453A68"><code> loadRequest</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.10.0 {#section_262928ABA971490EA6B8E277E17BDD89}

The [!DNL Android] SDK version 4.10.0 (May 20, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_E6B19BD9903A41D9AAF0035CD66756B5"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> 타겟 메서드 </td> 
   <td colname="2"> <p><code>loadRequest</code> 메서드에 대한 새로운 구문 및 예를 추가되었습니다. </p> <p>다음과 같은 새로운 <span class="keyword">Target</span> 메서드가 추가되었습니다. </p> <p> 
     <ul id="ul_B32C3B3931764F21948E36384B775642"> 
      <li id="li_3421E7F78F3A4DDA8FF004903FC8C75E">setThirdPartyID </li> 
      <li id="li_0836075699C5480EB3D6B742FCF6D508">getThirdPartyID </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.9.0 {#section_7393D3A5EA61431D9E7C07ECE176D17C}

The [!DNL Android] SDK version 4.9.0 (May 5, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_7D893A6E12554E9CA9AF2B03DA4C1A4B"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> 옵트아웃 및 개인 정보 설정 </td> 
   <td colname="2"> <p>애플리케이션에서 심층 연결을 구현하여 사용자를 앱 또는 웹 링크 대상으로 데려갈 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.8.3 {#section_9BB3DFBECC434AC6B3D7C18AA9BC895C}

The [!DNL Android] SDK version 4.8.3 (February 18, 2016) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_6DE145BC30154B9FADCE584A9737018D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> 옵트아웃 및 개인 정보 설정 </td> 
   <td colname="2"> <p>Starting with <span class="keyword"> Android</span> SDK 4.8.3, privacy settings set via the <code> setPrivacyStatus</code> method affect activity from <span class="keyword"> Analytics</span>, <span class="keyword"> Target</span> , and <span class="keyword"> Audience Manager</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.8.0 {#section_18FA091344644B43AA0E226241FF90DC}

The [!DNL Android] SDK version 4.8.0 (November 2, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_C47B9AEB2BB649CFA1D5CF04093B497B"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> 새로운 Experience Cloud 방문자 ID 서비스 메서드 </td> 
   <td colname="2"> <p>다음과 같은 메서드를 추가했습니다. </p> 
    <ul id="ul_6B85F8A4826642BEB373225CA760D799"> 
     <li id="li_72B94B8CECB94229827BFCB06671DFC9"><code> syncIdentifer</code> </li> 
     <li id="li_CD0C6B6CEA064FDD8B109E01AEC63F5C"><code> syncIdentifiers</code> </li> 
     <li id="li_620A2D94F97A4451919F0867CA82B25D"><code> getIdentifiers</code> </li> 
    </ul> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"> 새로운 ADBMobile JSON 구성 변수  </td> 
   <td colname="2"> <p>다음 변수를 추가했습니다. </p> 
    <ul id="ul_7FF76521C59343A4ABC9573C3CD5DC38"> 
     <li id="li_1381E3EF082B4D7DBD131D8EC62F94D2"><code> analyticsForwardingEnabled</code> </li> 
    </ul> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="1"><span class="keyword"> PhoneGap 플러그인 메서드</span> </td> 
   <td colname="2"> <p>다음과 같은 새로운 메서드가 추가되었습니다. </p> <p><b>구성 메서드</b> </p> <p> 
     <ul id="ul_98C5E7B5C79446EEA00F0E7CBC213301"> 
      <li id="li_B403C06E57A0450CBB4ABAD45170C681">setPushIdentifier </li> 
      <li id="li_6D76C40601544D4FA13FD44F390C83CE">setAdvertisingIndentifier </li> 
      <li id="li_7D03005DBD9E4AC7BB78BA162CDC8153">keepLifecycleSessionAlive </li> 
      <li id="li_3DDE07508B764E679AF2ACECC4D935CB">trackingSendQueuedHits </li> 
     </ul> </p> <p><b>타겟 메서드</b> </p> <p> 
     <ul id="ul_9B6002F5642B4D888FBD0A8D44EF32DB"> 
      <li id="li_5C1C9EA770E048E48723528F346712B4">targetClearCookies </li> 
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
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.6.1 {#section_98CC97CF0F0C48F7855130044386845A}

The [!DNL Android] SDK version 4.6.1 (September 24, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_80693083398F472F8A4E7861606E602D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Android SDK 버전 4.6.1</span> </p> </td> 
   <td colname="2"> <p>SDK 4.6.0 or earlier supports <span class="keyword"> Android</span> 2.2(API 8) - <span class="keyword"> Android</span> 5.1.1 (API 22) </p> <p>SDK 4.6.1 or later supports <span class="keyword"> Android</span> 2.3(API 9) or later </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.6 {#section_ADF6F871CF3C4E2381464D62DA6E1EB1}

The [!DNL Android] SDK version 4.6 (September 17, 2015) includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_35D0692698EF49AE8204F2AEB57CABD7"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p>Push Messaging to <span class="keyword"> Analytics</span> Segments </p> </td> 
   <td colname="2"> <p><span class="keyword"> Adobe Mobile Services</span> 및 <span class="keyword">Adobe Mobile</span> SDK를 사용하면 푸시 메시지를 <span class="keyword">Analytics</span> 세그먼트에 보낼 수 있습니다. 또한 SDK를 사용하면 푸시 메시지를 연 결과로서 앱을 연 사용자를 쉽게 보고할 수도 있습니다. </p> </td> 
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
     <ul id="ul_84AD959FC65C445BB119F69657AB4AF8"> 
      <li id="li_418FD9EE570F491F9704F72AC70EEE8D"><code> setPushIdentifier</code> </li> 
      <li id="li_B350606A504449E5AAE208B1E590E2CA"> <code> submitAdvertisingIdentifierTask</code> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.5 {#section_6E7614D4AEA24B7E81C4FC094882F062}

The [!DNL Android] SDK version 4.5 includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_BF98A1E904EB4314828AC58A2A6E7016"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="1" class="entry"> 기능 </th> 
   <th colname="2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="1"> <p><span class="keyword"> Android Wearable 확장</span> </p> </td> 
   <td colname="2"> <p>Starting in <span class="keyword"> Android</span> SDK version 4.5, a new <span class="keyword"> Android</span> extension lets you collect data from your <span class="keyword"> Android</span> Wearable app. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 버전 4.4 {#section_8D7FC183081E4BCFA8ADC33FB55E057C}

The [!DNL Android] SDK version 4.4 includes the following changes:

<table frame="all" colsep="1" rowsep="1" id="table_E8628F3806E24A0FB7157847D97C7B7A"> 
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

## 버전 4.3 {#section_789F3DA3DD3146CAA126B303F62D1A1A}

릴리스 날짜: **2014년 11월 24일**

* 새로운 기능 - Adobe Experience Cloud ID 통합
* 명확성을 위해 디버그 로그가 개선됨
* 인앱 메시지를 확인할 때 발생할 수 있는 충돌이 해결됨

## 버전 4.2 {#section_EDF95BA0301C4B54AAE839768917D439}

릴리스 날짜: **2014년 10월 16일**

* 새로운 기능 - 인앱 메시징 기능
* 새로운 기능 - 이제 앱 시작 동안 구성 파일의 위치를 지정할 수 있습니다. 
* 새로운 기능 - 이제 새 구성 파일이 없어도 관심 영역을 자동으로 업데이트할 수 있습니다.
* New - [!DNL Analytics] calls are now sent as HTTP POST requests.
* 특정 시나리오에서 앱 충돌이 추적될 수 없도록 하는 문제를 해결했습니다.
* debugLogging이 활성화되었을 때 로그 메시지가 정리되고 자세한 기록이 추가되었습니다.
* 성능 및 안정성 기능이 다양하게 개선되었습니다.

## 버전 4.1.7 {#section_DD98F9A4F00A457AA79D223CB1113A06}

릴리스 날짜: **2014년 8월 4일**

* 레퍼러 제한 시간이 5초 이상이고 오프라인 추적이 비활성화되었을 때 라이프사이클 히트가 전송되지 않던 문제를 해결했습니다.

## 버전 4.1.6 {#section_B665DF1A4FB249539D73569B52FA8786}

릴리스 날짜: **2014년 7월 17일**

* 데이터베이스가 손상되거나 만들 수 없을 경우에 발생하는 예외에 대한 보호 기능을 추가했습니다.
* 구성을 로드할 수 없을 때(일반적으로 null 컨텍스트 때문) 발생할 수 있었던 문제에 대한 보호 기능을 추가했습니다.
* Timed Action에 대한 컨텍스트 데이터를 업데이트할 때 발생할 수 있었던 예외에 대한 보호 기능을 추가했습니다.

## 버전 4.1.1 {#section_E5EFA05CEE9D486BA6B5C12B1102C117}

릴리스 날짜: **2014년 4월 23일**

* 레퍼러 추적이 활성화되고 라이프사이클 이전에 추적 호출이 수행되는 경우에 발생할 수 있었던 잠재적인 문제를 해결했습니다.

## 버전 4.1.0 {#section_266B62F5B6A44F5F8E6AB8ED1870C4A3}

릴리스 날짜: **2014년 4월 17일**

* 새로운 기능 - Bluetooth 비콘 추적
* 새로운 기능 - 타임스탬프가 활성화된 앱에서 충돌 히트 수가 올바른 세션으로 백데이트됩니다.
* 새로운 기능 - 타임스탬프가 활성화된 앱에서 이전 세션이 올바른 세션으로 백데이트된 히트에서 전송됩니다. (더 이상 이전 세션은 없음)
* 새로운 기능 - 히트 일괄 처리.
* 지연된 google 레퍼러 데이터를 허용하도록 구성 가능한 제한 시간으로 google play 레퍼러 추적을 수정했습니다.
* 특정 시나리오에서 발생할 수 있는 StrictMode 경고를 해결했습니다.
* 특정 메서드가 특정 순서로 호출될 때 매우 드물지만 라이브러리를 잠그던 문제를 해결했습니다.

## 버전 4.0.4 {#section_DCFAC758872D42F0BF0CCFCDDEA05E41}

릴리스 날짜: **2014년 2월 24일**

* 중지가 호출된 후에 중간에 다른 호출 없이 닫기가 호출된 경우 연장된 미디어 시간이 재생될 수 있었던 문제를 해결했습니다.
* 임의의 시간 동안 미디어가 재생되지 않은 경우에도 미디어 닫기 히트가 전송되었던 문제를 해결했습니다.

## 버전 4.0.3 {#section_FCC3D7D22EBF4A2FA949A4E88AD89F5C}

릴리스 날짜: **2014년 2월 20일**

* Added safety to network code to prevent crash caused by [!DNL Android] bug: https://code.google.com/p/android/issues/detail?id=54072

## 버전 4.0.2 {#section_5A7F4D5D9CBD4B79B3B590A2C3F4D0F9}

릴리스 날짜: **2014년 1월 30일**

* 데이터베이스가 손상되었을 때 여러 히트가 전송될 수 있었던 문제를 해결했습니다.
* 장치의 시간 설정이 올바르지 않은 경우 세션 길이 평균이 커지도록 하는 문제를 해결했습니다.

## 버전 3.2.5 {#section_A6E60DB42241481DA62F660344128F53}

릴리스 날짜: **2014년 1월 30일**

* 히트를 반복되도록 하는 손상된 데이터베이스에 대한 보호 기능을 추가했습니다.
* 장치 시간이 올바르지 않을 때 아주 긴 세션을 피하도록 최대 세션 길이 제한을 추가했습니다.

## 버전 4.0.1 {#section_5F58DBABDAA049FE9070E46989B2E9A9}

릴리스 날짜: **2013년 11월 14일**

* 특정 로케일에서 trackLocation 데이터의 잘못된 서식을 해결했습니다.

## 버전 4.0.0 {#section_79DCFAAF1DCB404898E3BE389AC835A6}

릴리스 날짜: **2013년 9월 27일**

[!DNL Android] Experience Cloud 솔루션용 SDK 4.x는 이제 다음과 같은 새로운 기능을 제공합니다.

* 현저한 성능 개선 모든 처리가 백그라운드 스레드에서 수행되고 SDK는 완전히 스레드 안전 상태입니다.
* 지리적 위치 및 관심 영역
* 라이프타임 값
* 시한 이벤트
* 옵트인/옵트아웃 관리
* Audience Manager 지원
* Lifecycle metrics passed to [!DNL Target] as mbox parameters
* 컨텍스트 데이터 및 처리 규칙에 대해 표준화

## 버전 3.2.3 {#section_E3464DDC3B4844CF9CC5FC3E35C5C785}

릴리스 날짜: **2013년 9월 23일**

* 매개 변수에서 null 값 또는 키를 허용하지 않는 Audience Manager의 버그를 수정했습니다.

## 버전 3.2.2 {#section_7D631AA2474F4DBAA043703629E3ECC6}

릴리스 날짜: **2013년 9월 12일**

* linkTrackEvents의 미디어 이벤트가 요청에 추가되지 않았던 버그를 해결했습니다.
* 추적 호출로 전달된 후에 수정되는 ContextData 관련 잠재적 예외를 수정했습니다.

## 버전 3.2.1 {#section_D269F9145B2844B6855423A30B125D5C}

릴리스 날짜: **2013년 8월 16일**

* 이제 SSL 연결에 엄격한 호스트 유효성 검사가 사용됩니다.
* 네트워크 연결이 끊기고 offlineTracking이 비활성화되었을 때 히트가 몇 초 동안 빠르게 재시도되던 버그를 수정했습니다.

## 버전 3.2 {#section_ABD4D192E3FF4240B1451262EAEE4F17}

릴리스 날짜: **2013년 8월 6일**

* Adobe Audience Manager에 대한 지원이 추가되었습니다.
* 라이프사이클 추적이 활성화될 때 이제 라이프사이클 데이터가 Target Mbox 요청과 함께 전송됩니다.
* SQLite가 강제로 커서를 닫아 불필요한 로그 항목을 발생시킬 수 있었던 문제를 해결했습니다.

## 버전 3.1.0 {#section_836B4F580B1C436FABD524A91857F882}

릴리스 날짜: **2013년 6월 13일**

* SQLite를 사용하도록 오프라인 저장소를 업데이트했습니다.
* 오프라인 제한을 기본값(1000)으로 재설정할 수 있었던 버그를 수정했습니다.
* 이제 활동 또는 응용 프로그램 컨텍스트를 수락하도록 startActivity를 업데이트했습니다.
* lifcycleSessionTimeout을 0으로 설정하면 앱 전체에서 여러 시작 이벤트가 발생되던 버그를 수정했습니다.

## 버전 3.0.8 {#section_51F50CD81C6A40C8BCF62F6F332A0800}

릴리스 날짜: **2013년 4월 18일**

* 일부 UTF8 문자의 인코딩 문제를 수정했습니다.

## 버전 3.0.7 {#section_0F3FEE2886EB4AB7BA288891FF6B6BCD}

릴리스 날짜: **2013년 4월 18일**

* 이전 세션 길이를 종종 잘못 계산되도록 하던 문제를 해결했습니다.
* 새 방문자 ID는 더 이상 deviceID나 subscriberID를 기준으로 하지 않습니다.
* 변수의 특수 문자를 인코딩할 때 발생할 수 있는 충돌을 해결했습니다.

## 버전 3.0.6 {#section_72F3F9CB95BF4076AD882B3270F77B87}

릴리스 날짜: **2013년 3월 21일**

* visitorID를 먼저 설정하지 않으면 읽을 수 없던 문제를 해결했습니다.
* 명확성을 위해 일부 오류 로그 메시지의 명명 규칙을 변경했습니다.
* 혼란을 피하기 위해 여러 기본 클래스의 액세스 가능성을 변경했습니다.
* 여러 가지 성능이 개선되었습니다

## 버전 3.0.5 {#section_0540FF6477D74D1F8274E9340EDE7E16}

릴리스 날짜: **2013년 2월 21일**

* 설정으로서 가치가 떨어진 `offlineThrottleDelay`는 스레드 최적화로 인해 더 이상 필요하지 않습니다. 이 설정은 이전 버전과의 호환성을 유지하기 위해 남아 있을 뿐 더 이상 어떤 효과도 없습니다.
* 오프라인 히트 캐시에 대한 잠재적 동기화 문제가 수정되었습니다.
* 계층적 변수를 #5 이상으로 설정할 때 경고 메시지가 명확하게 표시됩니다.
* Fixed issue that could cause OSVersion to be misreported on versions of [!DNL Android] &gt; 4.0.
* 여러 가지 성능이 개선되었습니다.
* 잘못된 형식의 URL로 인해 발생할 수 있는 잠재적 예외가 해결되었습니다.

## 버전 3.0.4 {#section_69ADA2ACD9DE436692152C3836B14EEF}

릴리스 날짜: **2012년 11월**

* 앱 시작이 새 세션으로 간주하기 전 앱이 시작되는 사이 경과해야 하는 시간(초)을 지정할 수 있게 해주는 `lifecycleSessionTimeout` 구성 변수가 추가되었습니다.
* `lifecycleSessionTimeout` 구성 설정을 사용하여 세션 길이를 계산할 수 있도록 시간 초과 값을 설정할 수 있는 기능이 추가되었습니다.
* 보안 문제가 수정되었습니다.

## 버전 3.0.3 {#section_F16E1A36AE3F4CBC92E4925D6DCCFADE}

릴리스 날짜: **2012년 10월**

* [Google Play 캠페인 추적](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/android/index.html?f=referrer) 지원이 추가되었습니다.

## 버전 3.0.2 {#section_CB24859B34804F9391BA1BF8DF29CC86}

릴리스 날짜: **2012년 9월**

* 가끔 닫기 히트로 인해 미디어 모니터에서 루프 조건이 발생하게 되는 문제를 해결했습니다.

## 버전 3.0.1 {#section_541CE15B340E414AA018A0EFAEE459F0}

릴리스 날짜: **2012년 8월**

* 이제 컨텍스트 재정의 매개 변수가 `Hashmap<String, Object>` (이전의 `Hashmap<String, String>`)로 전송됩니다.

## 버전 3.0 {#section_2955C0AF3A23476B8CF06C469DE3284C}

릴리스 날짜: **2012년 7월**

초기 릴리스.

## 이전 Android 버전(1.x) {#section_F2CC015616184D55AC6D6529DFC9A18B}

The following release notes apply to the 1.x version of [!DNL AppMeasurement] for [!DNL Android]. 가능하면 3.x 버전으로 업그레이드할 것을 권장합니다.

## 버전 1.2.3 {#section_5189CCE11EEF4350844B1490D0A9F534}

릴리스 날짜: **2012년 3월**

* 컨텍스트 데이터를 사용하여 데이터를 전달하는 경우 일부 상황에서 예외가 발생하던 문제가 수정되었습니다.

## 버전 1.2.2 {#section_C42925D94F3A429EB1299B96A6EEF6DF}

릴리스 날짜: **2012년 2월**

링크 추적 호출이 pev1 - pev3 값을 이중 URL 인코딩하는 문제를 수정했습니다.

추적 호출에 사용된 변수(trackLight)에 타임스탬프를 추가했습니다.

## 버전 1.2.1 {#section_21845E8A7D0C48B38CB90F0D4C5696AF}

릴리스 날짜: **2012년 1월**

* Added [!DNL Android] 3.x and 4.x compatibility.
* Implemented a UUID for visitor ID on [!DNL Android] devices that do not have SIM cards (For example, Kindle Fire).

## 버전 1.2 {#section_EC83BE1F00BF481EA1C74A63E4B90F65}

릴리스 날짜: **2011년 6월**

* SIM 카드가 장치에 삽입되지 않은 경우 방문자 ID 값에 장치 ID를 사용할 수 있도록 라이브러리를 업데이트했습니다. 기본적으로, SIM 카드가 삽입되지 않은 경우 라이브러리는 구독자 ID를 존재하지 않는 방문자 ID로 사용합니다.

## 버전 1.1.4 {#section_C602EC5C11594669A8797B736D240D2C}

릴리스 날짜: **2011년 4월**

* Xoom을 포함한 모든 태블릿을 지원합니다.
* 보고서 실행 시 보고서 세트와 지표를 검색할 수 있습니다.
* 서버측 처리 규칙을 유도하는 contextData를 지원합니다(v15만 해당).
* 라이트 서버 호출을 지원합니다(현재 베타 버전).
