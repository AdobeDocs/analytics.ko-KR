---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.linkTrackVars

 변수는 사용자 지정, 종료 및 다운로드 링크와 함께 전송되는, 쉼표로 구분되는 변수 목록입니다.

*`linkTrackVars`*&#x200B;가 ""로 설정되어 있으면 값이 있는 모든 변수가 링크 데이터와 함께 전송됩니다. 다른 변수와 연결된 인스턴스 또는 페이지 보기가 부풀려지지 않도록 링크 추적에 사용되는 링크의 [!UICONTROL onClick] 이벤트에서 *`linkTrackVars`*&#x200B;와 *`linkTrackEvents`*&#x200B;를 채우는 것이 좋습니다.

링크 데이터(사용자 지정, 종료 및 다운로드 링크)와 함께 보내야 하는 모든 변수는 *`linkTrackVars`*. *`linkTrackEvents`*&#x200B;를 사용하는 경우 *`linkTrackVars`*&#x200B;에 "events"를 포함해야 합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 임의 | "없음" |

When populating *`linkTrackVars`*, do not use the 's.' prefix for variables. 예를 들어 *`linkTrackVars`*&#x200B;를 "s.prop1"로 채우지 않고 "prop1"로 채워야 합니다. 다음 예제는 *`linkTrackVars`* 사용 방법을 보여줍니다.

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

google.com에 연결된 링크는 종료 링크(Google을 사용하지 않는 경우)이므로, event1과 eVar1이 종료 링크 데이터와 함께 보내져서, eVar1과 연결된 인스턴스와 event1이 실행되는 횟수를 증가시킵니다. [!DNL test.php]에 연결된 링크에서 [!UICONTROL eVar1]은 'value C' 값과 함께 전송됩니다. 이 값은 *`tl()`* 호출 시 [!UICONTROL eVar1]의 현재 값이기 때문입니다.

## 구문 및 가능한 값

*`linkTrackVars`* 변수는 개체 이름 접두사가 없고 대소문자를 구분하고 변수 이름을 쉼표로 구분하는 목록입니다. 's.eVar1' 대신 'eVar1'을 사용하십시오.

```js
s.linkTrackVars="variable_name[,variable_name[...]]"
```

The *`linkTrackVars`* 변수에는 [!DNL Analytics]에 전송된 변수, 즉 *`events`*, *`campaign`*, *`purchaseID`*, *`products`*, [!UICONTROL eVar1-75], [!UICONTROL prop1-75], [!UICONTROL hier1-5], *`channel`*, *`server`*, *`state`*, *`zip`* 및 *`pageType`* 변수만 포함될 수 있습니다.

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

* *`linkTrackVars`*&#x200B;가 비어 있으면 값이 있는 모든 변수가 모든 서버 호출과 함께 추적됩니다.
* *`linkTrackVars`*&#x200B;에 나열된 모든 변수는 모든 다운로드, 종료 또는 사용자 지정 링크 시 추적되는 값이 있습니다.
* *`linkTrackEvents`*&#x200B;를 사용하는 경우 *`linkTrackVars`*&#x200B;에 "events"를 포함해야 합니다.

* 변수에 "s." 또는 "s_objectname." 접두사를 사용하지 마십시오.