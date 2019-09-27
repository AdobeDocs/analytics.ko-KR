---
description: 'null'
seo-description: 'null'
seo-title: Windows Silverlight, NET, IIS, XBOX
solution: Analytics
subtopic: 릴리스 노트
title: Windows Silverlight, NET, IIS, XBOX
topic: 개발자 및 구현
uuid: 15c20bca-4886-4d57-9957-fe99743851ea
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Windows Silverlight, NET, IIS, XBOX{#windows-silverlight-net-iis-xbox}

>[!IMPORTANT]
>
>These SDKs have been sunset and are no longer supported or distributed by Adobe.

>[!NOTE]
>
>To find the current library version, turn on debug logging.

## 버전 1.4.2 {#section_2B70F52C4D214A43844CCEC6B45037F0}

릴리스 날짜: **2014년 8월**

* Removed support for the . [!DNL Microsoft Silverlight Analytics Framework] Adobe is no longer supporting or distributing the [!DNL Microsoft Silverlight Analytics Framework] integration for [!DNL AppMeasurement].

* 예정된 기능을 지원하기 위한 내부 변경입니다.

## 버전 1.4.1 {#section_9134F77804BF472291DA7243FAC89C2B}

릴리스 날짜: **2013년 3월**

* Fixed exception with getting default referrer in [!DNL Silverlight] outside of a browser context and properly exposed SSL property in the [!DNL Microsoft Silverlight Analytics Framework] component.

## 버전 1.4 {#section_2F4ADA4628EC43B480177C3DDB3D1CFA}

릴리스 날짜: **2013년 2월**

* Adobe 데이터 수집 서버의 페이지 URL 필드 확장을 지원할 수 있도록 255바이트보다 긴 URL을 전송하는 지원이 추가되었습니다. Page URLs longer than 255 bytes are split, with the first 255 bytes appearing in the `g=` parameter, with the remaining bytes appearing later in the query sting in the `-g=` query parameter. 따라서 브라우저가 잘리는 경우 긴 URL이 다른 데이터보다 우선하는 경우를 방지하면서도 긴 URL을 여전히 캡처할 수 있습니다.

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

## 버전 1.3.8 {#section_03089199E2DE4199B32F6821DDAED7BD}

릴리스 날짜: **2012년 9월**

* 미디어 닫기 이벤트를 추적하는 사용자 지정 `media.monitor` 메서드를 사용하는 경우 비디오 완료 이벤트가 전송되지 않는 문제를 해결했습니다.

   ```
   If(media.event==”CLOSE”) { 
   … 
   } 
   ```

## 버전 1.3.7 {#section_32AA8AE0CED4495496D25BF9246AE8AB}

릴리스 날짜: **2012년 4월**

* Added support for [!DNL XBOX].

## 버전 1.3.6 {#section_9F2738FA31CD48C4877AB92281EC67A9}

릴리스 날짜: **2012년 2월**

* [!DNL iOS] Phone 7: offlineThrottleDelay가 제대로 적용되지 않는 문제를 수정했습니다.
* 추적 호출에 사용된 변수(trackLight)에 타임스탬프를 추가했습니다.

## 버전 1.3.5 {#section_28BBDE7D187547A4AACCA60E5154DCD2}

릴리스 날짜: **2012년 1월**

* 전체 비디오 보기 횟수를 추적하는 새로운 방법을 사용하여 비디오 추적을 업데이트했습니다. [Adobe Analytics에서 비디오 측정](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/index.html)을 참조하십시오.

## 버전 1.3.4 {#section_43788EE6B57E4B2DBEED68BE6954D9CA}

* New support and build for [!DNL iOS] Phone platform including offline tracking.
* 데이터 추적을 위해 요청이 전송되는 방법을 덮어쓸 수 있도록 doRequest 위임을 지원합니다.
* 서버측 처리 규칙을 유도하는 contextData를 지원합니다(v15만 해당).
* 라이트 서버 호출을 지원합니다(현재 베타 버전).
* 이벤트 목록에서 카운터 이벤트에 1이 아닌 값을 할당할 수 있도록 지원합니다.
* 전환 eVar 및 이벤트를 사용하여 비디오를 추적하는 새로운 메서드를 지원합니다(현재 베타 버전).

