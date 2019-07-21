---
description: 'null'
seo-description: 'null'
seo-title: WinRT for Windows 8
solution: Analytics, Marketing Cloud
subtopic: 릴리스 노트
title: WinRT for Windows 8
topic: 개발자 및 구현
uuid: CEC 19 d 63-114 c -4 ef 6-a 55 e-db 6 aad 4 e 948 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# WinRT for Windows 8{#winrt-for-windows}

>[!NOTE]
>
>현재 라이브러리 버전을 찾으려면 디버그 로깅을 켭니다.

Mobile library [downloads](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) are available on [!DNL Developer Connection].

>[!NOTE]
>
>The [!DNL WinRT] for [!DNL Windows] 8 SDK is replaced by the [Windows 8.1 Universal App Store](../appmeasurement-release-notes/c-release-notes-winu.md#concept_79EEB87B0FEC4F6DB11BE8ED417A970E) SDK. 이 SDK에 대한 추가 개발 예정은 없습니다.

## 버전 4.0 {#section_248BF5A38F1843A5BCF6DBD62A5D3D59}

릴리스 날짜: **2014년 6월 17일**

지리적 위치, 라이프타임 값, Timed Action 및 옵트인 지원을 비롯한 새 기능이 있는 새 버전입니다.

## 버전 3.1.1 {#section_6E925545B72240BB816DA2333CA93E46}

릴리스 날짜: **2014년 5월 22일**

버그 수정 및 성능 향상

## 버전 3.1.0 {#section_F9059928B6FE43C99322A0DA35EB85C3}

릴리스 날짜: **2013년 10월 17일**

* [!DNL Windows] 8.1 호환성

## 버전 3.0.5 {#section_8F163FF1E88142F180091A88C9FD9D12}

릴리스 날짜: **2013년 4월 18일**

* 이전 세션 길이를 종종 잘못 계산되도록 하던 문제를 해결했습니다.

## 버전 3.0.4 {#section_FD242F9BA3D1481090E45998883E4CDD}

릴리스 날짜: **2013년 3월 21일**

* `ADMS_Measurement.visitorID` 기본값이 기본값으로 미리 채워집니다.
* 장치 정보 검색 문제를 해결했습니다.

## 버전 3.0.3 {#section_5865E881249441ADBB03A9637548650F}

릴리스 날짜: **2013년 2월 21일**

* 설정으로서 가치가 떨어진 `offlineThrottleDelay`는 스레드 최적화로 인해 더 이상 필요하지 않습니다. 이 설정은 이전 버전과의 호환성을 유지하기 위해 남아 있을 뿐 더 이상 어떤 효과도 없습니다.
* 다른 플랫폼에서 수집된 값에 일치하도록 이제 `DayOfWeek`는 일요일에 1을 기준으로 시작됩니다.
* 라이프사이클 추적을 능률화하기 위해 TrackingHelper.js의 이벤트 리스너에 자동 구독이 추가되었습니다.

## 버전 3.0.2 {#section_CCFAE5A29FB14DAD9A9F14FE8EE09B75}

릴리스 날짜: **2012년 11월**

* 이제 C#, C++ 및 HTML5/WinJS 플랫폼에 대해 화면 해상도가 정확히 수집됩니다.
* `ADMS_Churn` class is now internal. 응용 프로그램 라이프사이클 추적에 대한 우수 사례를 사용하려면 다음 호출을 사용하십시오.

   ```
   public void ADMS_Measurement.StartSession(); 
   public void ADMS_Measurement.StopSession();
   ```

* `public double maxSessionLength` 이전 사용자 세션에 대한 최대 세션 길이를 설정할 수 있도록 변수를에 `ADMS_Measurement` 추가했습니다. 등록된 세션 길이가 최대값을 초과할 경우 최대 세션 길이가 전송됩니다. Default `maxSessionLength` is 3600 (seconds).
* 앱 시작이 새 세션으로 간주하기 전 앱이 시작되는 사이 경과해야 하는 시간(초)을 지정할 수 있게 해주는 `lifecycleSessionTimeout` 구성 변수가 추가되었습니다.
* 라이프사이클 지표에 새로운 이전 세션 길이 지표가 추가되었습니다.
* 명확성을 위해 TrackingHelper를 업데이트했습니다.
* 미디어 모듈 버그를 수정했습니다.

## 버전 3.0.1 {#section_EA2E5F8550C348BDB948A9236BD35619}

**2012년 10월 일**

초기 릴리스.
