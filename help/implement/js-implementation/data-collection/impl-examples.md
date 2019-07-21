---
description: adobe.com을 예로 사용하면, 여기 설명된 구현은 동일한 visid 쿠키를 참조합니다.
keywords: Analytics 구현
seo-description: adobe.com을 예로 사용하면, 여기 설명된 구현은 동일한 visid 쿠키를 참조합니다.
seo-title: 구현 예
solution: Analytics
title: 구현 예
topic: 개발자 및 구현
uuid: 17 D 8 D 2 B 2-2303-495 A-B 0 F 9-D 8 D 3 C 05 F 3893
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 구현 예

adobe.com을 예로 사용하면, 여기 설명된 구현은 동일한 visid 쿠키를 참조합니다.

**Javascript:**

```js
var s_account="omniturecom" 
s.visitorNamespace="omniture" 
s.trackingServer="omniture.112.2o7.net"
```

**하드 코딩된 이미지 요청:**

```
<img border="0" alt="" src="https://omniture.112.2o7.net/b/ss/omniturecom/5?ns=omniture" width="1" height="1" /> 
```

**Appmeasurement:**

```js
s.account="omniturecom"; 
s.visitorNamespace="omniture"; 
s.trackingServer="omniture.112.2o7.net";
```

또한 자사 쿠키를 활용하는 경우:

**Javascript:**

```js
var s_account="omniturecom" 
s.visitorNamespace"omniture" 
s.trackingServer="metrics.omniture.com"
```

**하드 코딩된 이미지 요청:**

```
<img border="0" alt="" src="https://metrics.omniture.com/b/ss/omniturecom/5" width="1" height="1" />
```

**Appmeasurement:**

```js
s.account="omniturecom"; 
s.visitorNamespace="omniture"; 
s.trackingServer="metrics.omniture.com";
```

