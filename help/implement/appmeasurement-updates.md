---
title: JavaScript 릴리스 노트의 AppMeasurement
description: JavaScript용 AppMeasurement에 대한 누적 릴리스 노트입니다.
subtopic: Release notes
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# JavaScript 릴리스 노트의 AppMeasurement

JavaScript용 [!DNL AppMeasurement]에 대한 누적 릴리스 노트입니다.

<!-- https://wiki.corp.adobe.com/display/omtrcache/AppMeasurement+Change+Log -->

[코드 관리자](/help/admin/admin/code-manager-admin.md)에서 최신 버전의 AppMeasurement를 다운로드할 수 있습니다.

## 버전 2.20.0

릴리스 날짜: **2020년 3월 5일**

* JSLint 경고를 표시하지 않도록 Internet Explorer 검색을 업데이트하여 보안 관련 문제를 해결했습니다.

## 버전 2.19.0

릴리스 날짜: **2020년 2월 21일**

* 대상 관리 모듈을 DIL 9.4로 업데이트했습니다. (AN-209341)

## 버전 2.18.0

릴리스 날짜: **2020년 2월 13일**

* 이제 AppMeasurement는 [`writeSecureCookies`](vars/config-vars/writesecurecookies.md) 변수를 설정하여 쿠키를 강제로 Secure 속성을 포함할 수 있습니다. 이 변수에 대한 요구 사항은 전체 클라이언트 웹 사이트가 안전하게 제공된다는 것입니다(HTTPS). (AN-204604)

## 버전 2.17.0

릴리스 날짜: **2019년 8월 23일**

* Baidu 쿼리 문자열 순서 조정 지원이 추가되었습니다. (AN-182483)
* 옵트인을 기다리는 동안 대기 중인 히트에 오래된 방문자 값이 발생하는 문제를 수정했습니다. (AN-184391)

## 버전 2.16.0

릴리스 날짜: **2019년 8월 15일**

* `sendBeacon`에 종료 링크에 대한 [!UICONTROL AppMeasurement] 지원 기능을 구현했습니다. 히트가 `sendBeacon`을 사용하고 페이지가 언로드되는 경우 요청이 여전히 완료됩니다. 이 기능은 히트가 데이터 수집 서버에 도달할 가능성이 높으므로 종료 링크에 매우 유용합니다. (AN-175142)
* 이제 OptIn 설정이 변경되더라도 ECID/fid 값이 첫 번째 히트에 캐시됩니다. (AN-175142)
* 대상 관리 모듈의 DIL 9.3 업데이트. (AN-182704)
* `s.ActivityMap.trackScrollReach`에 스위치를 노출하여 스크롤 도달 추적을 켜거나 끕니다. (AN-182754)
* 방문자 ID 서비스 4.4.0을 사용하도록 AppMeasurement를 업그레이드했습니다. (AN-182912)

## 버전 2.15.0

릴리스 날짜: **2019년 7월 15일**

* ActivityMap 스크롤 도달 추적이 Activity Map 확장에 추가되었습니다(AN -172949).
* AppMeasurement에 DIL 9.2가 추가되었습니다(AN-182472).

## 버전 2.14.0

릴리스 날짜: **2019년 5월 21일**

* 여러 개의 히트가 보류 중일 때 추적기 매개 변수의 상태 관리에 대한 문제가 해결되었습니다. (AN-176931, AN-176629, DTM-12758)
* Visitor.js 4.3.0을 포함하도록 AppMeasurement가 업데이트됨(AN-180049)

## 버전 2.13.0

릴리스 날짜: **2019년 4월 10일**

* clearVars와 관련하여 보고된 많은 문제가 해결되었습니다. 이 문제는 추적기가 준비되기 전에 히트를 전송하면 발생합니다. 추적기가 준비되면 라이브러리는 이미 지워졌거나 변경된 변수를 설정할 수 있습니다. (AN-176931, AN-176629, DTM-12758).

## 버전 2.12.0

릴리스 날짜: **2019년 2월 22일**

* 대상 관리 모듈을 DIL 9.1로 업데이트했습니다. (AN-175255)
* GTM 보안 정책이 Activity Map 모듈을 허용하지 않습니다. (AN-174679)
* ID 서비스가 옵트인에서 승인되지 않은 경우 옵트아웃을 허용하도록 AppMeasurement가 개선되었습니다. (AN-175259)

## 버전 2.11.0

릴리스 날짜: **2019년 2월 11일**

* AppMeasurement에 새로운 Adobe 옵트인 서비스 기능 지원이 추가되었습니다. (AN-163546)
* 세션 저장소에 링크 추적 데이터를 저장할 수 있는 지원이 추가되었습니다. (AN-162272)
* Audio Analytics에 대한 미디어 스트림 유형 지원이 추가되었습니다. (AN-173265)

## 버전 2.10.0

릴리스 날짜: **2018년 9월 20일**

이 릴리스에서는 [!DNL AppMeasurement] 라이브러리가 모든 연결 유형에 대해 올바르게 쿠키를 제출하도록 합니다.

* [!DNL AppMeasurement]가 POST 중 쿠키 전송을 차단합니다. (AN-165538)
* XDomainRequest에 대한 지원을 삭제합니다. (AN-165733)
* [!DNL AppMeasurement] 기본 쿠키 수명을 5년에서 2년으로 줄였습니다. (AN-158572)
* 코드 관리자([!DNL AppMeasurement])에서 미디어 모듈 제거(AN-166590)

## 버전 2.9.0

릴리스 날짜: **2018년 5월 24일**

>[!NOTE][!DNL Experience Cloud] ID 서비스를 사용하는 고객은 방문자 API 3.0 이상이 필요합니다. 연관된 코드 라이브러리([!DNL at.js] 등)가 업데이트될 때마다 최신 방문자 API 버전으로 업그레이드할 수 있습니다.[!DNL AppMeasurement.js]

* ID 요청에 업데이트된 방문자 인터페이스를 사용하도록 [!DNL AppMeasurement]가 업데이트되었습니다. (AN-151483)
* 링크 추적이 해제된 후 링크 추적 쿠키가 계속 작성되는 문제가 해결되었습니다. (AN-156332)
* 여러 번 호출될 때 `registerPreTrackCallback` 및 `registerPostTrackCallback`이 콜백 함수 서명을 차단하는 문제가 해결되었습니다. (AN-158566)

## 버전 2.8.2

릴리스 날짜: **2018년 4월 12일**

* ID 요청에 업데이트된 방문자 인터페이스를 사용하도록 [!DNL AppMeasurement]를 업데이트합니다. (AN-151483)
* 링크 추적이 꺼지면 링크 추적 쿠키가 계속 작성됩니다. (AN-156332)
* [!DNL AppMeasurement] 기본 쿠키 수명을 5년에서 2년으로 줄였습니다. (AN-158572)

## 버전 2.8.1

릴리스 날짜: **2018년 3월 29일**

핫픽스를 포함하는 방문자 API 3.1.0(AN-159524) 재구성: (CORE-11390, CORE-10634)

## 버전 2.8.0

릴리스 날짜: **2018년 3월 15일**

핫픽스를 포함하는 방문자 API 3.1.0(AN-159524) 재구성: (CORE-11390, CORE-10634)

* VAPI v3.1을 [!DNL AppMeasurement] v2.8로 구성합니다. (AN-158353)
* 공유를 용이하게 하기 위해 데이터 수집 끝점을 다시 계수합니다. (AN-156647)
* 요청 라운드 트립 시간 지표를 [!DNL AppMeasurement]에 추가합니다. (AN-158343)

## 버전 2.7.0

릴리스 날짜: **2018년 1월 18일**

* IE 6 - 9에 대한 지원 삭제
* 방문자 API v3.0.0 포함
* DIL v7.00 포함

## 버전 2.6.0

릴리스 날짜: **2017년 11월 9일**

s_gl이 호출될 때 [!DNL AppMeasurement] 라이브러리가 올바른 계정 조합을 항상 설정하지는 않는 문제가 해결되었습니다. (AN-152153)

## 버전 2.5.0

릴리스 날짜: **2017년 9월 21일**

* [!DNL dil.js 6.12] 포함([!DNL Audience Manager] 모듈)
* 방문자 API 2.5.0 포함.

## 버전 2.4.0

릴리스 날짜: **2017년 8월 17일**

* dil.js v6.11 포함
* 방문자 API 2.4.0 포함

## 버전 2.3.0

릴리스 날짜: **2017년 7월 20일**

* `s.Util.getQueryParam`으로 `#`이 캡처되던 버그를 수정했습니다.
* `dil.js` v6.10이 추가되었습니다(AN-145701).

## 버전 2.2.0

릴리스 날짜: **2017년 6월 8일**

* 여러 [!DNL AppMeasurement] 인스턴스화 순서에 대한 지원이 추가되었습니다. (AN-138237)
* 버전 2.2.0 방문자 API 포함. (AN-144042)

## 버전 2.1.0

릴리스 날짜: **2017년 4월 20일**

* `dil.js` 최신 버전 포함(AN-140396)
* 페이지 레퍼러를 재지정하는 `adobe_mc_ref` 매개 변수에 대한 지원이 추가되었습니다. (AN-131920)
* 다시 포함된 방문자 API 2.1.0. (AN-140873)
* `mcorgid` 매개 변수가 추가되었습니다. (AN-139586)
* cp(customerPerspective) 매개 변수가 추가되었습니다. (AN-140897)

## 버전 2.0.0

릴리스 날짜: **2017년 3월 9일**

* 버전 번호를 2.0.0으로 업데이트해야 하는 새 빌드 프로세스로 옮겨졌습니다. (AN-137878)
* mboxMCSDID 처리를 추적 호출이 이루어진 올바른 섹션 위치로 이동했습니다. (AN-138483)

## 버전 1.8.0

릴리스 날짜: **2017년 1월 19일**

* VisitorAPI 2.0.0 포함
* 중단 검사가 완료된 후 SDID가 사용되도록 함수 호출 및 확인 순서를 다시 지정합니다. (AN-134364)
* `s.registerPreTrackCallback` 및 `s.registerPostTrackCallback` 후크를 추가했습니다. (AN-134567)

## 버전 1.7.0

업데이트 날짜: **2016년 11월 11일**

* 방문자 API 1.10.1 포함.
* [!DNL Audience Manager] 모듈이 DIL(Demdex Integration Library) 6.6으로 업데이트되었습니다. (AN-132065)
* 방문자 API 1.9.0 포함. (AN-132072)
* [!DNL AppMeasurement] [!DNL Audience Manager] 모듈이 DIL 6.5 및 추가 구성으로 업데이트되었습니다(AN-129411).
* 방문자 API 1.8.0(AN-129887) 포함

## 버전 1.6.4

업데이트 날짜: **2016년 8월 18일**

* AMCV 쿠키를 읽고 쓸 수 있도록 [!DNL AppMeasurement]가 업데이트되었습니다. (AN-127098)
* 방문자 API 1.7.0 포함.

>[!NOTE][!DNL JavaScript] 버전 1.6.3에 대한 릴리스 노트를 참조하십시오. 이 릴리스 노트에는 Experience Cloud ID 서비스에 대해 업데이트된 요구 사항이 포함되어 있습니다.

## 버전 1.6.3

업데이트 날짜: **2016년 8월 4일**

* [!DNL AppMeasurement]에서 요청 연결을 너무 빨리 종료한 문제가 수정되었습니다. (AN-126448)

>[!IMPORTANT][!DNL Experience Cloud] ID 서비스 버전 1.6.0을 사용하려면 *용* 버전 1.6.3 이상이 [!DNL AppMeasurement]필요합니다[!DNL JavaScript]. Experience Cloud ID 서비스 버전 1.6.0으로 업그레이드하려면 코드 [!DNL AppMeasurement] 버전 1.6.3 이상을 사용하는지 확인하십시오.

## 버전 1.6.2

릴리스 날짜: **2016년 7월 21일**

* 방문자 API 1.6.0 포함
* [!DNL AppMeasurement]가 방문자 API에서 잘못 난독화되는 방법을 호출하는 문제가 해결되었습니다. (AN-126006)
* [!DNL JavaScript] 오류: &quot;속성이 v:image에서만 유효합니다.&quot; 문제의 원인이 해결되었습니다. (AN-124009)

## 버전 1.6.1

릴리스 날짜: **2016년 6월 16일**

* 방문자 API 1.5.7 포함.
* 완전한 이벤트를 발생하지 않던 Firefox의 링크 클릭 추적 처리를 수정했습니다.

## 버전 1.6

릴리스 날짜: **2016년 4월 21일**

* [!DNL AppMeasurement] Activity Map 모듈이 [!DNL AppMeasurement] 표준 모듈에 통합되었으므로 한 [!DNL .js] 파일만 참조하면 됩니다. 또한 Activity Map 추적은 기본적으로 활성화됩니다. (AN-112689)
* [!DNL AppMeasurement]의 쿼리-문자열 변수 순서에서 발생하는 잘림 문제가 해결되었으므로 *`pageURLRest`*&#x200B;이 마지막입니다. (AN-114647)

## 버전 1.5.4

릴리스 날짜: **2016년 3월 17일**

* 방문자 API 1.5.4 포함
* 방문자 API 1.5.4 이상에서 옵트아웃 지원

## 버전 1.5.3

릴리스 날짜: **2016년 1월 21일**

* POST가 추적 호출에 사용되는 경우 [!DNL Audience Manager] 모듈에 대한 처리가 수정되었습니다. (AN-115381)
* 페이지 URL의 나머지 부분(&quot;-g&quot;)을 추적 요청 쿼리 문자열 끝으로 이동했습니다. (AN-114647)

## 버전 1.5.2

릴리스 날짜: **2015년 11월 5일**

* 방문자 API 1.5.3 포함.
* URL Truncation 2047에 대한 IE11 감지 수정 (AN-114914)

## 버전 1.5.1

릴리스 날짜: **2015년 9월 17일**

* 방문자 API 1.5.2 포함
* VisitorAPI.js에서 AAM DIL 6.2 - getCustomer ID를 사용하여 /event 호출로 AAM에 전달하도록 [!DNL Audience Manager] 모듈이 업데이트되었습니다. (AN-104978)

## 버전 1.5

릴리스 날짜: **2015년 6월 18일**

* *`getCustomerIDs`* 메서드를 사용하여 고객 ID와 인증된 상태를 수집하고 데이터 수집 요청으로 해당 ID를 전송하는 방문자 API 1.5에 대한 지원.
* **[!UICONTROL AudienceManagement]** 모듈(DIL 6.1)에서 중복 대상 iframe의 생성이 수정되었습니다.
* 릴리스 1.4.5에 설명된 알려진 문제를 해결했습니다.

## 버전 1.4.5

릴리스 날짜: **2015년 5월 21일**

* iOS SDK 버전 4.5부터 새로운 iOS 확장을 사용하면 Apple Watch 앱, 오늘 위젯, 사진 편집 위젯 및 기타 모든 iOS 확장 앱의 사용 데이터를 수집할 수 있습니다. Mobile Services 사용 안내서에서 [iOS 확장 구현](https://docs.adobe.com/content/help/ko-KR/mobile-services/ios/ios-ext/ios-ext.html)을 참조하십시오.
* Android SDK 버전 4.5에서 시작하는 새 Android 확장 기능을 사용하면 Android 웨어러블 앱의 데이터를 수집할 수 있습니다. Mobile Services 사용 안내서에서 [Android 웨어러블](https://docs.adobe.com/content/help/ko-KR/mobile-services/android/wearables-android/android-wearable.html)을 참조하십시오.
* 방문자 API 1.4 포함.
* DIL 버전 6.0을 사용하도록 AudienceManagement 모듈을 업데이트했습니다.

>[!NOTE] **알려진 문제**: 방문자 API/[!DNL AppMeasurement] [!DNL Audience Manager] 모듈 통합에서 IE6-9에 두 개의 대상 게시 iFrame 요청(`//fast.<subdomain>.demdex.net/dest5.html` 및 `//fast.<subdomain>.demdex.net/dest4.html`)이 있습니다. 다른 브라우저에 표시될 때 올바른 동작은 `//fast.<subdomain>.demdex.net/dest5.html`.

## 버전 1.4.4

릴리스 날짜: **2015년 4월 16일**

* 이제 라이프사이클 지표가 있는 사용자 지정 컨텍스트 데이터 변수를 포함할 수 있습니다.
* 이제 PhoneGap에서 `trackBeacon` 및 `clearCurrentBeacon` 호출을 사용할 수 있습니다.
* `trackLight` 호출 후에 경량 서버 호출 프로필 ID를 지우도록 약간 수정되었습니다.

## 버전 1.4.3

릴리스 날짜: **2015년 2월 19일**

* 지연된 추적 호출에 대한 모든 처리가 일관되게 수행되었으며, 클릭한 개체와 같은 지연 동안 백업된 변수와 관련된 문제가 수정되었습니다.
* Changed to not do automatic referrer tracking after the first tracking call so the 2nd, 3rd, etc tracking call (usually link tracking) will not double-count the referrer when *`s.referrer`* was manually set before the first tracking call.
* 배포 zip이 방문자 API 1.3.5를 포함하도록 업데이트되었습니다.

## 버전 1.4.2

릴리스 날짜: **2015년 1월 15일**

* 보지 않은 사전 렌더링된 페이지의 추적을 방지하기 위해 WebKit 사전 렌더링 처리 문제를 수정했습니다.
* 배포 zip이 DIL 버전 5.5를 포함하는 업데이트된 **[!UICONTROL AudienceManagement]** 모듈과 방문자 API 1.3.4를 포함하도록 업데이트되었습니다.

## 버전 1.4.1

릴리스 날짜: **2014년 9월 18일**

* 구현 시 추가적인 대시 문자 구분 기호와 함께 버전 문자열에 추가되는 최대 4개의 문자를 지정할 수 있도록 해주는 `tagContainerMarker` 변수를 추가했습니다. 이는 Dynamic Tag Management에서 사용됩니다.

   ```js
   // JavaScript
   s.tagContainerMarker = "D1.0";
   
   // Data Collection request
   //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
   ```

   4문자는 영숫자 및 마침표와 같은 URL 파일 경로에 허용되는 문자로 제한됩니다.

* H 코드로 이중 태그가 지정된 페이지에서, 강제 링크 추적이 활성화될 때(Webkit 브라우저의 기본값) 자동 링크 추적(다운로드 및 종료) 중에 발생할 수 있는 루프를 수정했습니다. 또한 유사한 루프를 방지하기 위해 자동 링크 추적에 대한 일반적인 보호 기능을 추가했습니다. 이 안전 조치는 *동일한* 개체에 대한 반복 클릭의 자동 링크 추적을 10초마다 한 번으로 제한합니다. 이 안전 조치는 자동 링크 추적에만 적용되므로, 수동 링크 추적(s.tl) 호출은 제한되지 않습니다. 다른 개체에 대한 클릭도 이 안전 조치의 영향을 받지 않으며 추적됩니다.
* 지연이 필요할 때 클릭한 개체에 대한 처리를 수정했습니다.
* 방문자 API에 필요한 값이 아직 없는 경우 링크 onclick 함수에서 s.t가 호출될 때 이중 페이지 보기 카운트가 발생하는 문제를 수정했습니다.
* HTTP POST 지원.

   > [!IMPORTANT] [!DNL Analytics] 호출이 [!DNL AppMeasurement]에서 GET 메서드([IE의 잘린 URL](https://helpx.adobe.com/kr/analytics/kb/shortening-image-request-urls.html)을 해결하는 메서드) 대신 POST 메서드를 사용하도록 하려면 Experience Cloud에 대해 최신 방문자 ID 서비스 구현을 사용해야 합니다.

## 버전 1.4

릴리스 날짜: **2014년 8월 21일**

* 플러그인으로서 제거된 브라우저 플러그인(`p` 쿼리 매개 변수) 추적이 버전 15에서 더 이상 보고되지 않습니다.
* 다운로드 zip에서 **[!UICONTROL AudienceManagement]** 모듈 추가.
* 추가 eVars(76 - 250) 및 이벤트(101-1000)에 대한 지원을 추가했습니다.

>[!NOTE] H-Code는 추가 eVar 및 이벤트를 지원하지 않습니다.

## 버전 1.3.2

릴리스 날짜: **2014년 6월 19일**

* 기존 [!DNL Analytics] 방문자 ID와 같은 방문자 API 필드에 대한 완료 및 대기 플래그 처리에서 오류가 발생하던 문제를 수정했습니다.
* 방문자 ID 서비스 1.3의 새로운 기능에 대한 지원

## 버전 1.3.1

릴리스 날짜: **2014년 5월 22일**

* [!DNL JavaScript]용 [!DNL AppMeasurement]의 `s_gi` 함수는 H 코드 `s_gi`를 사용하여 생성된 인스턴스를 올바로 찾지 못했습니다. 이 문제는 [!DNL JavaScript]용 [!DNL AppMeasurement] 및 H 코드가 인스턴스가 여러 개인 동일한 페이지에 있는 일부 이중 태그 지정 구현에만 영향을 주었고, `s_gi`는 보고서 세트별로 인스턴스를 찾는 데이터 사용되었습니다.

## 버전 1.3

릴리스 날짜: **2014년 4월 17일**

* [Experience Cloud 방문자 ID 서비스](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html) 지원.

## 버전 1.2.4

릴리스 날짜: **2014년 3월 13일**

* 하트비트 비디오에 대한 버그 수정.

## 버전 1.2.3

릴리스 날짜: **2014년 2월 20일**

* 하트비트 비디오에 대한 버그 수정.

## 버전 1.2.2

릴리스 날짜: **2014년 2월 6일**

* [!DNL Audience Manager] DIL 모듈과의 호환성 문제가 해결되었습니다. [!DNL Audience Manager] 고객은 DIL 모듈 버전 4.8로도 업데이트해야 합니다.

## 버전 1.2.1

릴리스 날짜: **2013년 11월 15일**

* 하트비트 비디오 측정에 사용된 페이지 이벤트를 수정했습니다.

## 버전 1.2

릴리스 날짜: **2013년 11월 14일**

* [하트비트 비디오 측정](https://docs.adobe.com/content/help/ko-KR/media-analytics/using/media-overview.html)에 대한 지원을 추가했습니다.
* [방문자 ID 서비스](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 지원하기 위해 `VisitorAPI.js`가 추가되었습니다.

## 버전 1.1.1

* &quot;opera:&quot;로 시작하는 링크의 경우 링크 추적 호출이 Opera 브라우저에서 전송되지 않았습니다(&quot;opera:&quot;는 다른 브라우저에서 &quot;about:&quot; 및 &quot;chrome:&quot;과 유사함).
* Accessible Video and Communications Act(비디오 및 통신 접근성 법률)를 준수하도록 모든 이미지 개체에 `alt=""`가 추가되었습니다.

## 버전 1.1

릴리스 날짜: **2013년 9월 18일**

* `head` 태그에서 라이브러리 및 페이지 코드 배치에 대한 지원이 수정되었습니다.
* 누락된 모듈 `onLoad` 지원이 추가되었습니다.

## 버전 1.0.3

릴리스 날짜: **2013년 8월 15일**

* Adobe Tag Management를 통한 배포 지원을 추가했습니다.
* [!DNL AppMeasurement] 개체에서 계층 변수가 설정되지 않는 문제가 해결되었습니다.

## 버전 1.0.2

릴리스 날짜: **2013년 7월 18일**

* 이제 해시/단편이 자동 링크 추적에서 무시됩니다. 이전에는 전체 `href`가 `.pdf`로 끝났으므로 다음 URL이 자동으로 추적되었습니다.

   ```js
   <a href="index.htm#anchor.pdf">Test Link</a>
   ```

   이제 해시/단편이 무시되므로 파일 이름이 일치하는 확장명으로 끝나는 경우에만 해당 링크가 추적됩니다.

## 버전 1.0.1

릴리스 날짜: **2013년 5월 23일**

이제 코드 관리자에서 새 [!DNL JavaScript] [!DNL AppMeasurement] 라이브러리를 사용할 수 있습니다. 이 라이브러리는 [!DNL s_code.js]의 동일한 핵심 기능을 제공하면서도, 모바일 사이트와 데스크톱 사이트 모두에서 사용할 수 있도록 보다 가볍고 빠릅니다.

* H.25 코드보다 3-7배 더 빠릅니다.
* 21k 압축되지 않은 경우 및 8k gzip(H.25 코드는 33k 압축되지 않은 경우 및 13k gzip)입니다.
* 쿼리 매개 변수 가져오기, 쿠키 읽기 및 쓰기, 고급 링크 추적을 수행하는 기본 지원.
* 모바일 사이트에서 사용할 수 있을 만큼 작고 빠르고 전체 데스크탑 웹에서 사용할 수 있을 만큼 강력하므로 모든 웹 환경에서 단일 라이브러리를 활용할 수 있습니다.
