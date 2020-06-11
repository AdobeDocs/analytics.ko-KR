---
title: 운영 체제
description: 방문자의 운영 체제입니다.
translation-type: tm+mt
source-git-commit: ad206649488a1a2dead717cdfe53f4c630ba3f3b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# 운영 체제

&#39;운영 체제&#39; 차원은 방문자가 사용한 운영 체제와 버전을 보여 줍니다. 웹 속성에 OS별 기능이 있는 경우 이 차원을 통해 가장 일반적인 운영 체제를 파악할 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 조회 테이블을 참조합니다. 조회 값은 이미지 요청의 `User-Agent` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다.

## 차원 값

차원 값에는 방문자가 사용하는 운영 체제가 포함됩니다. Examples include `"Windows 10"`, `"OS X 10.15"`, and `"Android 9"`.
