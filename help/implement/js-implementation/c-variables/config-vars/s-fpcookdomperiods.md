---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.fpCookieDomainPeriods

 변수는 구현에 타사 2o7.net 또는 omtrdc.net 도메인을 사용하는 경우에도 기본적으로 자사 쿠키인 JavaScript 설정 쿠키(s_sq, s_cc, plug-ins)에 사용됩니다.

*`fpCookieDomainPeriods`* 동적으로 설정하면 안 됩니다. *`cookieDomainPeriods`*&#x200B;를 사용하는 경우 *`fpCookieDomainPeriods`*&#x200B;에 대한 값도 지정하는 것이 좋습니다. *`fpCookieDomainPeriods`*&#x200B;는 *`cookieDomainPeriods`* 값을 상속합니다. *`fpCookieDomainPeriods`*&#x200B;가 방문자 ID 쿠키가 설정된 도메인에 영향을 주지 않으며, 이는 구현에서 쿠키를 자사 쿠키로 취급하는 경우에도 마찬가지입니다.

*`fpCookieDomainPeriods`*&#x200B;는 점(".") 수를 말합니다. www로 시작되는 경우 도메인에 포함된 점(.) 수를 나타냅니다. 예를 들어 `www.mysite.com`에는 점이 두 개 있고, `www.mysite.co.jp`에는 점이 세 개 있습니다. 변수를 설명하는 또 다른 방법은 사이트의 주 도메인에 있는 섹션의 수입니다(`mysite.com`의 경우 2, `mysite.co.jp`의 경우 3).

JavaScript용 [!DNL AppMeasurement] 파일은 *`fpCookieDomainPeriods`* 변수를 사용하여 [!UICONTROL 방문자 ID](s_vi) 쿠키 이외의 자사 쿠키를 설정할 도메인을 결정합니다. There are at least two cookies affected by this variable, including `s_sq` and `s_cc` (used for visitor click map and cookie checking respectively). [!UICONTROL getValOnce]와 같은 플러그인에서 사용되는 쿠키도 영향을 받습니다.

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

*`cookieDomainPeriods`* 변수는 아래와 같이 문자열이어야 합니다.

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
