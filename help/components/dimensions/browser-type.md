---
title: 브라우저 유형
description: 브라우저를 만든 조직입니다.
translation-type: tm+mt
source-git-commit: 4a7b3a00bdbf557c219de530e3e692c2b2db4a84
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# 브라우저 유형

&#39;브라우저 유형&#39; 차원은 방문자가 사용하는 브라우저를 만든 조직을 나열합니다. 이 차원은 방문자가 사용하는 브라우저의 수준을 확인하려는 경우 유용합니다. 별도의 차원 값과 동일한 브라우저의 서로 다른 버전이 나열되지 않도록 &#39;브라우저&#39; 차원 위에 값을 제공합니다.

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 조회 테이블을 참조합니다. 조회 값은 이미지 요청의 `User-Agent` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다.

## 차원 값

차원 값에는 브라우저를 만드는 조직이 포함됩니다. 공통 차원 값에는 `"Google"` (작성자 [!DNL Chrome]), `"Apple"` (작성자 [!DNL Safari]), `"Microsoft"` (작성자 [!DNL Edge]) 및 `"Mozilla"` (작성자 [!DNL Firefox]),등이 포함됩니다.
