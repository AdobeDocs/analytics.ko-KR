---
description: 'null'
seo-description: 'null'
seo-title: Windows Phone 8
solution: Analytics, Marketing Cloud
subtopic: 릴리스 노트
title: Windows Phone 8
topic: 개발자 및 구현
uuid: 7378969 A-D 219-42 BF -9750-141 ACC 9 E 4 B 7 D
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Windows Phone 8{#windows-phone}

>[!NOTE]
>
>현재 라이브러리 버전을 찾으려면 디버그 로깅을 켭니다.

Mobile library [downloads](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) are available on [!DNL Developer Connection].

>[!NOTE]
>
>[!DNL Windows] Phone 8 SDK는 [Windows 8.1 Universal App Store](../appmeasurement-release-notes/c-release-notes-winu.md) SDK로 대체됩니다. 이 SDK에 대한 추가 개발 예정은 없습니다.

## 버전 3.0.4 {#section_51A8A53CDFB24F6F9D882E9C30ECDB49}

릴리스 날짜: **2013년 8월 21일**

* 이제 컨텍스트 데이터 키에 밑줄을 사용할 수 있습니다.

## 버전 3.0.5 {#section_DFE58939E33C447FBBF8B04E612A96B5}

릴리스 날짜: **2013년 5월 22일**

* 버그 수정 및 성능 향상

## 버전 3.0.4 {#section_F303B6E5955248CF8BDA6C7CB994BAD5}

릴리스 날짜: **2013년 4월 18일**

* 이전 세션 길이를 종종 잘못 계산되도록 하던 문제를 해결했습니다.

## 버전 3.0.3 {#section_0159586C3EC94865A485A8E586862DF6}

릴리스 날짜: **2013년 3월 21일**

* `DateTime` 개체의 현지화 문제를 해결했습니다.

## 버전 3.0.2 {#section_296C375729EA4474BDF3FD6ADD4BEAFB}

릴리스 날짜: **2013년 2월 26일**

* `ADMS_Measurement.visitorID` 기본값이 기본값으로 미리 채워집니다.
* 캐시에서 자동 응답이 종종 수행되던 문제를 해결했습니다.

## 버전 3.0.1 {#section_5865E881249441ADBB03A9637548650F}

릴리스 날짜: **2013년 2월 21일**

* 설정으로서 가치가 떨어진 `offlineThrottleDelay`는 스레드 최적화로 인해 더 이상 필요하지 않습니다. 이 설정은 이전 버전과의 호환성을 유지하기 위해 남아 있을 뿐 더 이상 어떤 효과도 없습니다.
* 다른 플랫폼에서 수집된 값에 일치하도록 이제 `DayOfWeek`는 일요일에 1을 기준으로 시작됩니다.
* 가끔 앱 충돌을 일으키는 오프라인 스토리지 문제를 수정했습니다.

