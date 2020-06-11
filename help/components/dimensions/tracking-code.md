---
title: 추적 코드
description: 추적 코드 또는 캠페인의 이름입니다.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# 추적 코드

&#39;추적 코드&#39; 차원은 사이트에 있는 추적 코드의 이름을 나열합니다. 이 차원은 일반적으로 쿼리 문자열 매개 변수를 사용하여 수집됩니다. 인터넷의 여러 위치에 서로 다른 쿼리 문자열 매개 변수 값이 있는 링크를 배치할 수 있습니다. 이 차원은 사이트로 트래픽을 유도하는데 가장 성공한 링크를 보고합니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`v0` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 변수를 사용하여 이 데이터를 [`campaign`](/help/implement/vars/page-vars/campaign.md) 수집합니다.

## 차원 값

차원 값에는 사이트의 추적 코드 이름이 포함됩니다. 조직에서 사용할 특정 차원 값을 결정합니다.
