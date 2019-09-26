---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.fpCookieDomainPeriods

 변수는 구현에 타사 2o7.net 또는 omtrdc.net 도메인을 사용하는 경우에도 기본적으로 자사 쿠키인 JavaScript 설정 쿠키(s_sq, s_cc, plug-ins)에 사용됩니다.

The *`fpCookieDomainPeriods`* variable should never be dynamically set . 사용하는 *`cookieDomainPeriods`**`fpCookieDomainPeriods`* 경우 값을 지정하는 것도 좋습니다. *`fpCookieDomainPeriods`* 값을 상속합니다. *`cookieDomainPeriods`* Note that *`fpCookieDomainPeriods`* does not affect the domain on which the visitor ID cookie is set, even if your implementation treats this as a first-party cookie.

이름 " *`fpCookieDomainPeriods`*"은 마침표 수(".")를 나타냅니다. "www"로 시작되는 경우 도메인에 포함된 점(.) 수를 나타냅니다. For example, `www.mysite.com` contains two periods, while `www.mysite.co.jp` contains three periods. Another way to describe the variable is the number of sections in the main domain of the site (two for `mysite.com` and three for `mysite.co.jp`).

JavaScript [!DNL AppMeasurement] 파일용 *`fpCookieDomainPeriods`* 변수는 변수를 사용하여 [!UICONTROL 방문자 ID(s_vi) 쿠키 이외의 퍼스트 파티 쿠키를 설정할 도메인을] 결정합니다. There are at least two cookies affected by this variable, including `s_sq` and `s_cc` (used for visitor click map and cookie checking respectively). [!UICONTROL getValOnce]와 같은 플러그인에서 사용되는 쿠키도 영향을 받습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | cookieDomainPeriods |

## 쿠키 도메인 변수 설정을 위한 샘플 코드

```js
s.fpCookieDomainPeriods="2" 
var d=window.location.hostname 
if(d.indexOf('.co.uk')>-1||d.indexOf('.com.au')>-1) 
  s.fpCookieDomainPeriods="3" 
```

## 구문 및 가능한 값

The *`cookieDomainPeriods`* 변수는 아래와 같이, 문자열로 예상됩니다.

```js
s.fpCookieDomainPeriods="3"
```

## 예

```js
s.fpCookieDomainPeriods="3"
```

```js
s.fpCookieDomainPeriods="2"
```

## 구성 설정

없음