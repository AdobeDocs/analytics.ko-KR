---
title: Java 활성화
description: 브라우저에서 Java가 활성화되어 있는지 확인합니다.
translation-type: tm+mt
source-git-commit: 226c54b782651ea8c6f4b7bb8030a1513c440a1d
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 1%

---


# Java 활성화

&#39;Java 활성화&#39; 차원은 현재 브라우저에 Java가 활성화되어 있는지 여부를 결정합니다. 사이트에 Java 기반 기능을 도입하고 Java가 이미 활성화된 방문자 수를 알고 싶은 경우 유용합니다. Java를 비활성화한 사용자를 위해 활성화 방법에 대한 지침이나 대안을 제공할 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`v` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 브라우저에서 Java가 활성화되어 있는지 여부를 감지하여 이 데이터를 수집합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다. API를 통해 AppMeasurement 외부에 데이터 수집 메서드를 사용하는 경우 이 차원을 사용하려면 &quot;Y&quot; 또는 &quot;N&quot;을 포함하는 `v` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 값

차원 값에는 &quot;Enabled&quot;, &quot;Disabled&quot; 및 &quot;Unknown&quot;이 포함됩니다.

* **활성화됨**: 브라우저에서 Java가 활성화됩니다. 쿼리 문자열에 값 &quot;Y&quot;가 포함되어 있습니다. `v`
* **비활성화됨**: 브라우저에서 Java가 비활성화되거나 Java가 지원되지 않습니다. 쿼리 문자열에 값 &quot;N&quot;이 포함되어 있습니다. `v`
* **알 수 없음**: AppMeasurement에서 Java 지원을 확인할 수 없습니다. 이미지 요청에 `v` 쿼리 문자열이 없습니다.
