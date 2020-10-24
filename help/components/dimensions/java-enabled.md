---
title: Java 활성화
description: 브라우저에서 Java가 활성화되어 있는지 여부를 결정합니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '216'
ht-degree: 100%

---


# Java 활성화

Java 활성화 차원은 현재 브라우저에 Java가 활성화되어 있는지 여부를 결정합니다. 사이트에 Java 기반 기능을 도입하고 Java가 이미 활성화된 방문자의 수를 알고 싶은 경우 유용합니다. Java를 비활성화한 사용자를 위해 활성화 방법에 대한 지침이나 대안을 제공할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`v` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 브라우저에서 Java가 활성화되어 있는지 여부를 감지하여 이 데이터를 수집합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform Launch 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우(API 등을 통해)에는 이 차원을 사용하려면 &quot;Y&quot; 또는 &quot;N&quot;을 포함하는 `v` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 항목

차원 항목은 &quot;활성화됨&quot;, &quot;비활성화됨&quot; 및 &quot;알 수 없음&quot;을 포함합니다.

* **활성화됨**: 브라우저에 Java가 활성화되어 있습니다. `v` 쿼리 문자열이 값 &quot;Y&quot;를 포함했습니다.
* **비활성화됨**: 브라우저에 Java가 비활성화되어 있거나 Java가 지원되지 않습니다. `v` 쿼리 문자열이 값 &quot;N&quot;를 포함했습니다.
* **알 수 없음**: AppMeasurement에서 Java 지원을 확인할 수 없습니다. 이미지 요청에 `v` 쿼리 문자열이 없습니다.
