---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.cookieDomain

이 변수는 [!DNL Analytics] 쿠키 `s_cc` 및 `s_sq`를 설정할 도메인을 결정합니다.

Commonly, `s.cookieDomainPeriods` is used to generate `s.cookieDomain` from `window.location.hostname`. Instead of using `s.cookieDomainPeriods`, you can explicitly set `s.cookieDomain` to what you want to use in your implementation. 예를 들면 다음을 사용하여 정규화된 페이지 이름에 쿠키를 설정할 수 있습니다.

`s.cookieDomain = window.location.hostname;`
