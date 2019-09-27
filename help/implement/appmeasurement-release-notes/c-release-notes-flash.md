---
description: Flash에 대한 누적 릴리스 노트입니다. ActionScript를 사용하는 Flash 앱은 데스크탑과 웹에서 측정 가능합니다.
seo-description: Flash에 대한 누적 릴리스 노트입니다. ActionScript를 사용하는 Flash 앱은 데스크탑과 웹에서 측정 가능합니다.
seo-title: Flash-Flex
solution: Analytics
subtopic: 릴리스 노트
title: Flash-Flex
topic: 개발자 및 구현
uuid: 2ee7fb92-9b62-44d4-bd93-6dff26764b7f
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Flash-Flex{#flash-flex}

Flash에 대한 누적 릴리스 노트입니다. ActionScript를 사용하는 Flash 앱은 데스크탑과 웹에서 측정 가능합니다.

>[!NOTE]
>
>현재 라이브러리 버전을 찾으려면 디버그 로깅을 설정합니다.

<!-- 

https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=omtrcache&title=AppMeasurement+Change+Log

 -->

## April 20, 2017 {#section_8521EC2B68E24203A0F1B14A9D2652D2}

**버전 4.0.3 **

* 방문자 API 1.6.1 포함.

## 2016년 8월 18일 {#section_D72EF20672174249B864997905D7552A}

** 4.0.2 - 업데이트**

방문자 API 1.6.0 포함

## May 19, 2016 {#section_061305CFC1E040E69E3CDF4078C17AE4}

** 4.0.1 - 업데이트**

방문자 API 1.5.6 포함

## April 21, 2016 {#section_6EFC6DBEB9E1460DB344A8278F9FC696}

Adobe는 [보안 업데이트 APSB16-13](https://helpx.adobe.com/security/products/analytics/apsb16-13.html)을 발표했습니다. 해당 업데이트는 다음에 적용됩니다: [!DNL AppMeasurement] for Flash 라이브러리. 이 업데이트는 `debugTracking`이 사용되도록 설정될 때만 적용 가능하고 [DOM기반 XSS 공격](https://www.owasp.org/index.php/DOM_Based_XSS)을 수행하는 데 악용될 수 있는 라이브러리의 중요한 취약점을 해결합니다.

>[!IMPORTANT]
>
>This issue affects [!DNL AppMeasurement] for Flash only when `debugTracking` has been enabled ( `debugTracking` is disabled in the default configuration). **영향을 받는 경우에는`debugTracking`을 즉시 사용하지 않도록 설정하는 것이 좋습니다.** 다음은 일부 샘플 코드입니다.

```
public var s:AppMeasurement; 
s = new AppMeasurement(); 
s.debugTracking = false; // set to false or remove line 
                         // for default "disabled” behavior 
```

영향을 받는 버전은 모든 플랫폼의   for Flash version 4.0 and earlier on all platforms.[!DNL AppMeasurement]

>[!NOTE]
>
>Due to security reasons, we will no longer be distributing an AS2 version of [!DNL AppMeasurement] for Flash. 기존 AS2 기반 프로젝트의 데이터 수집은 계속 지원됩니다. 그렇지만 고객은 구현을 AS3로 업그레이드하고 [!DNL AppMeasurement] for Flash의 최신 보안 기능을 통합하는 것이 좋습니다.

[!DNL AppMeasurement] for Flash customers affected by this issue must rebuild projects with the updated library available for download from the [!DNL Analytics] Console [More…](https://help.adobe.com/en_US/Flex/4.0/UsingFlashBuilder/WS6f97d7caa66ef6eb1e63e3d11b6c4d0d21-7feb.html#WS6f97d7caa66ef6eb1e63e3d11b6c4d0d21-7f88) (AN-121780)

## November 5, 2015 {#section_18C1A1C82EA844E78A1D563E66DE3FCF}

버전 4.0 - 업데이트:

* 방문자 API 1.5.3 포함.

## September 17, 2015 {#section_319911C0F080452981F8C8BEA2880463}

버전 4.0 - 업데이트:

* 방문자 API 1.5.2 포함.

## 2015년 8월 20일 {#section_1BEA10285E9F4863B89B4B713DBB20DB}

Version 4.0 - Update:

* 방문자 API 1.5.1 포함.

## June 18, 2015 {#section_2ACB18A1693244D6A49B53F4E17F0C30}

버전 4.0 - 업데이트

* 방문자 API 1.5 포함.
* Visitor API 1.5+ getCustomerIDs 메서드를 사용하여 고객 ID 및 인증된 상태를 수집한 후 데이터 수집 요청과 함께 전송합니다(AN-102131).

## 2015년 5월 21일 {#section_F5EFCC451F13499F9AA53326AE5926F1}

버전 3.9.2 - 업데이트:

* 방문자 API 1.4 포함

## 2015년 2월 19일 {#section_95ADF1725CE7415D956944A28182E69B}

버전 3.9.2:

* 방문자 API 1.3.5 포함.
* 첫 번째 추적 호출 전에 *`s.referrer`*&#x200B;가 수동으로 설정되었을 때 두 번째, 세 번째 등의 추적 호출(일반적으로 링크 추적)에서 레퍼러가 두 번 계산되지 않도록 첫 번째 추적 호출 이후에 자동 레퍼러 추적을 수행하지 않도록 변경되었습니다. (AN-92647)
* Removal of deprecated [!UICONTROL Heartbeat] video tracking embedded in the Media module. The supported [!UICONTROL Heartbeat] video tracking has been moved to a separate Video [!DNL Analytics] library.

## September 18, 2014 {#section_80939868A2284961BF620851B000294F}

버전 3.9.1:

* Added cookie support testing to Flash (k = Y/N query-string variable) and pf=1 to query-string when cookie support test is possible (browser with [!DNL JavaScript] access).
* 방문자 ID 서비스 1.3.2의 새로운 기능에 대한 지원

## 2014년 8월 21일 {#section_F7CA56E42B6548D3BE5A0D020BCEE97A}

버전 3.9:

* 위도 및 경도 변수를 추가했습니다.
* 방문자 ID 서비스 1.3.1의 새로운 기능에 대한 지원

## 버전 3.8.1 {#section_29A2A0A20D9B43A1B57E5ED299C6EAF3}

릴리스 날짜: **2014년 6월 19일**

* Fixed handling of done and waiting flags for Visitor API fields such as the legacy [!DNL Analytics] Visitor ID, that was causing errors.
* 방문자 ID 서비스 1.3의 새로운 기능에 대한 지원

## 버전 3.8 {#section_3F75C4D0C9BE470B95838DDB2CDCA79F}

릴리스 날짜: **2014년 4월 17일**

* Support for the Experience Cloud Visitor ID service.[](https://marketing.adobe.com/resources/help/en_US/mcvid/)

## 버전 3.7.3 {#section_1159B2AB56F54903A6FBFB7047AEC1C5}

릴리스 날짜: **2014년 3월 13일**

* Multiple bug fixes to [!UICONTROL Heartbeat] video tracking.

## 버전 3.7.2 {#section_D6DCE5FE846A45F1A2CED237E8AAEFE9}

릴리스 날짜: **2014년 2월 6일**

* Multiple bug fixes to [!UICONTROL Heartbeat] video tracking.

## 버전 3.7.1 {#section_DC79F108AB5E42189A8EC7D87697AE0B}

릴리스 날짜: **2013년 11월 14일**

* Multiple bug fixes to [!UICONTROL Heartbeat] video tracking.

## 버전 3.7 {#section_7239878DCD724FD0B9BC900821A4DA96}

릴리스 날짜: **2013년 10월 17일**

* [하트비트 비디오 추적](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/) 지원
* [방문자 ID 서비스](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_service#.html)를 지원하기 위해 VisitorAPI.swc가 포함되었습니다.
* ActionScript 3이 있는 Flash player 9에 대한 지원이 삭제되었습니다. ActionScript 3용 최소 Flash Player 버전은 10입니다.

## 버전 3.6.2 {#section_57FB21568BDD48F7882F00AD630E6CE8}

릴리스 날짜: **2013년 9월 18일**

* 향후 베타 릴리스를 지원하기 위한 내부 변경입니다.

## 버전 3.5.5 {#section_149CAF8AF39741C2B9F6A015F7FB8C61}

릴리스 날짜: **2013년 8월 15일**

* 오프라인 추적이 비활성화될 때 실패한 요청을 대기열에 다시 추가하는 기능이 비활성화되었습니다.

## 버전 3.5.4 {#section_3429BD7DE2B64110BEE3A3850E58A0F7}

릴리스 날짜: **2013년 2월 21일**

* ActionScript 2의 URL 인코딩/디코딩 문제가 수정되었습니다.

## 버전 3.5.3 {#section_5192BC1C8BF547D1A5A92863686601DD}

릴리스 날짜: **2013년 1월 31일**

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

## 버전 3.5.2 {#section_77727E343EC14B869020358183DAB2DB}

릴리스 날짜: **2012년 11월 8일**

* Internal updates for  integration.[!DNL Audience Manager]

## 버전 3.5.1 {#section_F6345AC9F4994D6F97BBCF399B02BB21}

릴리스 날짜: **2012년 10월 22일**

* 항상 UTF-8을 사용하므로 `s.charSet`의 모든 설정을 무시할 수 있도록 ActionScript 3 빌드가 변경되었습니다.

## 버전 3.5 {#section_7DC183DD46CF42FE85F42E7AB8915D99}

Release Date: **September 13, 2012**
**Important change to variable binding**: In version 3.5, an option to disable variable binding was added for customers who need to start and end literal string values with curly braces. 중괄호를 사용한 변수 바인딩은 주로 XML 태그를 사용하는 OSMF 비디오 플레이어를 구성할 때 사용됩니다.

```
<autoTrackMediaName>{media.player.metadata(https://www.corp1.com/,episodeID)}</autoTrackMediaName>
```

XML 태그의 기본 동작을 덮어쓸 때 `autoBind`라고 하는 새로운 특성을 사용할 수 있습니다.

```
<autoTrackMediaName autoBind=false>{123}</autoTrackMediaName>
```

`autoBind`를 `false`로 설정하면 해당 값이 기본적인 문자열로 간주되고 변수 바인딩이 사용되지 않습니다. 이 특성이 `false`로 설정되지 않은 경우 XML 태그의 동작은 동일하게 유지됩니다.

**ActionScript Code에 대한 영향**

Though not commonly used, this syntax is also available to bind [!DNL AppMeasurement] variables in your ActionScript code. If you are unsure whether or not you are using variable binding, search your code for [!DNL AppMeasurement] variable values that start and end with curly braces. 예:

```
s.eVar1 = "{source}";
```

변수 바인딩을 사용하고 있는 경우 새로운 `bindVariable` 메서드를 사용하려면 이 코드를 변경해야 합니다.

```
s.bindVariable("eVar1","source");
```

선택적으로, 각 위치를 변경하는 대신에 `autoBindVariablesByValue`를 true로 설정함으로써 3.5 이전 버전의 동작으로 되돌릴 수 있습니다.

```
s.autoBindVariablesByValue = true;
```

**추가 수정 사항:**

* 미디어 닫기 이벤트를 추적하는 사용자 지정 `media.monitor` 메서드를 사용하는 경우 비디오 완료 이벤트가 전송되지 않는 문제를 해결했습니다.

   ```
   If(media.event==”CLOSE”) { 
   … 
   } 
   ```

## 버전 3.4.9 {#section_5F2566CF954242D0A7205DA0B257DABA}

릴리스 날짜: **2012년 7월 19일**

* Added a master-only meta policy, see [https://www.adobe.com/devnet/flashplayer/articles/fplayer9_security.html](https://www.adobe.com/devnet/flashplayer/articles/fplayer9_security.html).

## 버전 3.4.8 {#section_7501E04F6A854D50BFF0F287607A796F}

릴리스 날짜: **2012년 6월 21일**

* AS3 빌드에 항상 UTF-8을 사용하도록 변경되었습니다. 이를 통해 일부 멀티바이트 언어의 문자열 문제를 방지합니다.

## 버전 3.4.7 {#section_B26A014D13B14878816472E394FBAAA6}

릴리스 날짜: **2012년 4월 26일**

비디오 측정: Brightcove 플레이어의 오프셋 값이 일관되지 않은 문제를 수정했습니다. 이제 오프셋이 0으로 보고될 경우 전체적으로 길이를 오프셋으로 사용합니다. 이렇게 하면 오프셋 값을 사용하여 추적을 완료하는 새로운 방법에 관련된 문제가 해결됩니다.

## 버전 3.4.6 {#section_273B76A58745486E9715D9F5C2AEC433}

릴리스 날짜: **2012년 1월 19일**

* 전체 비디오 보기 횟수를 추적하는 새로운 방법을 사용하여 비디오 추적을 업데이트했습니다.

## 버전 3.4.5 {#section_DEDF0BEF6BF4458CA00896799E5BA67C}

릴리스 날짜: **2011년 9월 8일**

* 기본 제로 값 "0"을 포함하는 prop이 활성화되었습니다. 이전에는 기본 제로 값이 포함된 prop이 전송되지 않았습니다.

## 버전 3.4.3 {#section_6C930AA0E95045BCA9AD4096B63657C9}

릴리스 날짜: **2011년 5월**

* OSMF의 경우 OSMF 비디오 플레이어를 추적할 때 프록시 플러그인을 사용하는 경우 발생되는 문제를 수정했습니다. 이 문제 수정을 통해 OSMF ProxyElement가 프록시하는 요소가 추적되지 않을 때 OSMF ProxyElement를 추적할 수 있게 되었습니다.
* Flash Player 9.0.16에서 비디오 측정 오류의 원인이 되는 문제를 수정했습니다.

