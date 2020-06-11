---
title: 쿠키 지원
description: 브라우저가 쿠키를 지원하는지 여부를 결정합니다.
translation-type: tm+mt
source-git-commit: a8dc233e962a49674a30ff3c9f0b5d0d45b09f24
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# 쿠키 지원

&#39;쿠키 지원&#39; 차원은 브라우저가 주어진 히트에 대한 쿠키를 지원하는 경우 보고합니다. 쿠키를 지원하는 브라우저를 사용하는 방문자와 쿠키를 의도적으로 비활성화하는 방문자의 비율을 결정하는 것이 유용합니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`k` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 수집합니다. AppMeasurement는 이름이 지정된 쿠키를 설정한 다음 쿠키 `s_cc`가 존재하는지 감지합니다. 그 결과 쿼리 문자열 매개 변수 값 `Y` (브라우저가 쿠키를 지원하고 활성화한 경우) 또는 `N` (브라우저에 쿠키가 비활성화된 경우)이 됩니다. AppMeasurement(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다. AppMeasurement 외부(예: API를 통해) 데이터 수집 메서드를 사용하는 경우 값 `k` 또는 `Y` `N`의 각 히트에 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 값

차원 값은 `Enabled`, `Disabled`및 `Unknown`를 포함합니다.

* **`Enabled`**: 브라우저는 쿠키를 지원하고 쿠키를 활성화합니다.
* **`Disabled`**: 브라우저가 쿠키를 지원하지 않거나 방문자가 쿠키를 비활성화했습니다.
* **`Unknown`**: AppMeasurement에서 쿠키 지원을 확인할 수 없습니다. 이미지 요청에 `k` 쿼리 문자열이 없습니다.
