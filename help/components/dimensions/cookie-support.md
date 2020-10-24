---
title: 쿠키 지원
description: 브라우저가 쿠키를 지원하는지 여부를 결정합니다.
translation-type: ht
source-git-commit: cd2225ec00190af6b616f313b419935c4f8dfafd
workflow-type: ht
source-wordcount: '187'
ht-degree: 100%

---


# 쿠키 지원

쿠키 지원 차원은 브라우저가 주어진 히트에 대한 쿠키를 지원하는지 여부를 보고합니다. 쿠키를 지원하는 브라우저를 사용하는 방문자와 쿠키를 의도적으로 비활성화하는 방문자의 비율을 파악하는 것이 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`k` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. AppMeasurement는 `s_cc`라는 쿠키를 설정한 다음 쿠키가 존재하는지 감지합니다. 그 결과가 쿼리 문자열 매개 변수 값 `Y`(브라우저가 지원하고 쿠키가 활성되어 있는 경우) 또는 `N`(브라우저에 쿠키가 비활성화되어 있는 경우)입니다. AppMeasurement를 사용하는 경우(Adobe Experience Platform Launch 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우(API 등을 통해)에는 값 `Y` 또는 `N`으로 각 히트에서 `k` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 항목

차원 항목은 `Enabled`, `Disabled` 및 `Unknown`을 포함합니다.

* **`Enabled`**: 브라우저가 쿠키를 지원하고 브라우저에 쿠키가 활성화되어 있습니다.
* **`Disabled`**: 브라우저가 쿠키를 지원하지 않거나 방문자가 쿠키를 비활성화했습니다.
* **`Unknown`**: AppMeasurement가 쿠키 지원을 확인할 수 없습니다. 이미지 요청에 `k` 쿼리 문자열이 없습니다.
