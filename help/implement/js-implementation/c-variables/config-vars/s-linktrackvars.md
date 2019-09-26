---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.linkTrackVars

 변수는 사용자 지정, 종료 및 다운로드 링크와 함께 전송되는, 쉼표로 구분되는 변수 목록입니다.

If *`linkTrackVars`* is set to "", all variables that have values are sent with link data. 다른 변수와 연결된 인스턴스 또는 페이지 보기가 부풀려지지 않도록 링크 추적에 사용되는 링크의 *`linkTrackVars`* onClick *`linkTrackEvents`*  이벤트에 채우는 것이 좋습니다.

링크 데이터(사용자 지정, 종료 및 다운로드 링크)와 함께 보내야 하는 모든 변수는 *`linkTrackVars`*. 이 *`linkTrackEvents`* 사용될 경우 "events"를 *`linkTrackVars`* 포함해야 합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 임의 | "없음" |

When *`linkTrackVars`*, do not use the 's.' prefix for variables. 예를 들어 "s.prop1" *`linkTrackVars`* 로 채우는 대신 "prop1"로 채워야 합니다. 다음 예는 *`linkTrackVars`* 사용해야 하는 방법을 보여줍니다.

```js
s.linkTrackVars="eVar1,events" 
s.linkTrackEvents="event1" 
s.events="event1" 
s.eVar1="value A" 
s.eVar2="value B" 
s.t() // eVar1, event1 and event2 are recorded 
<a href="https://google.com">event1 and eVar1 are recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.eVar1='value C';s.events='';s.tl(this,'o')">eVar1 is recorded</a> 
```

google.com에 연결된 링크는 종료 링크(Google을 사용하지 않는 경우)이므로, event1과 eVar1이 종료 링크 데이터와 함께 보내져서, eVar1과 연결된 인스턴스와 event1이 실행되는 횟수를 증가시킵니다. In the link to [!DNL test.php], [!UICONTROL eVar1] is sent with a value of 'value C' because that is the current value of [!UICONTROL eVar1] at the time that *`tl()`* is called.

## 구문 및 가능한 값

The *`linkTrackVars`* variable is a case-sensitive, comma-separated list of variable names, without the object name prefix. 's.eVar1' 대신 'eVar1'을 사용하십시오.

```js
s.linkTrackVars="variable_name[,variable_name[...]]"
```

The *`linkTrackVars`* 변수에는 전송된 변수만 포함될 수 있습니다. [!DNL Analytics]즉, 다음과 같습니다. *`events`**`campaign`*, *`purchaseID`*, *`products`* eVar1-75 [!UICONTROL ,]prop1-75 [!UICONTROL , hightroom1-5]er-51, er-51,,,,,,,, 및 구를 *`channel`**`server`**`state`**`zip`**`pageType`*&#x200B;사용합니다.

## 예

```js
s.linkTrackVars="events,prop1,eVar49"
```

```js
s.linkTrackVars="products"
```

## 구성 설정

없음

## 함정, 질문 및 팁

* If *`linkTrackVars`* is blank, all variables that have values are tracked with all server calls.
* Any variable listed in *`linkTrackVars`* that has a value at the time of any download, exit, or custom link, are tracked.
* 이 *`linkTrackEvents`* 사용될 경우 "events"를 *`linkTrackVars`* 포함해야 합니다.

* 변수에 "s." 또는 "s_objectname." 접두사를 사용하지 마십시오.