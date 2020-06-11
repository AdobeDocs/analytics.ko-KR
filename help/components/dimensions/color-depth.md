---
title: 색상 깊이
description: 장치의 색상 깊이입니다.
translation-type: tm+mt
source-git-commit: a8dc233e962a49674a30ff3c9f0b5d0d45b09f24
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# 색상 깊이

&#39;색상 깊이&#39; 차원은 장치가 지원하는 색상의 수를 보고합니다. 이 차원은 1,600만 색상을 지원하지 않는 장치에서 트래픽이 발생하는 정도를 결정하는 데 유용합니다. 역사적으로, 이 보고서는 신생 모바일 웹이 처음 등장했을 때 귀중한 것이었다. 그러나 현재 사용 중인 대부분의 장치는 1,600만 색상(빨간색, 녹색 및 파란색의 경우 0-255)을 지원합니다. <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## 데이터로 이 차원 채우기

이 차원은 조회 테이블을 참조하며 비트 값을 보다 읽기 쉬운 형식으로 변환합니다. 이미지 요청의 [`c` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 수집합니다. AppMeasurement는 `screen.colorDepth` 변수를 사용하여 이미지 요청 쿼리 문자열을 채웁니다. AppMeasurement(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다. AppMeasurement 외부(예: API를 통해) 데이터 수집 메서드를 사용하는 경우 유효한 비트 값으로 각 히트에 `c` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 값

차원 값에는 장치에서 지원하는 색상 수가 포함됩니다. 예제 값에는 `"16 million (24-bit)"`, `"16 million (32-bit)"`및 `"65,536 (16-bit)"`. AppMeasurement에서 색상 심도를 확인할 수 없는 경우 색상 심도가 로 표시됩니다 `"None"`.

> [!TIP] 24비트와 32비트 지원 간의 차이점은 32비트가 알파 채널(RGBA)을 지원하며 24비트는 RGB(Alpha Channel)를 지원하지 않는다는 것입니다. 이 개념 [에 대한 자세한 내용은 Wikipedia의 색상 깊이를](https://en.wikipedia.org/wiki/Color_depth) 참조하십시오.
