---
title: 운영 체제 유형
description: 버전에 관계없이 운영 체제.
translation-type: tm+mt
source-git-commit: ad206649488a1a2dead717cdfe53f4c630ba3f3b
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# 운영 체제 유형

&#39;운영 체제 유형&#39; 차원은 특정 버전에 관계없이 방문자가 사용한 상위 OS를 보여줍니다. 이 차원은 어떤 특정 운영 체제와 버전이 가장 일반적이지만 방문자가 사용하는 일반적인 OS 플랫폼을 파악하는 데 유용합니다.

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 조회 테이블을 참조합니다. 조회 값은 이미지 요청의 `User-Agent` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다.

## 차원 값

차원 값에는 사용된 운영 체제의 유형이 포함됩니다. Examples include `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"`, and `"Apple iOS"`.
