---
title: 색상 깊이
description: 장치의 색상 깊이입니다.
exl-id: 0bde895d-6832-4110-b575-62ee5ddc1783
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '220'
ht-degree: 100%

---

# 색상 깊이

색상 깊이 차원은 장치가 지원하는 색상의 수를 보고합니다. 이 차원은 1,600만 색상을 지원하지 않는 장치에서 트래픽이 발생하는 정도를 파악하는 데 유용합니다. 이전에 신생 모바일 웹이 처음 등장했을 때는 이 보고서가 유용했지만, 현재 사용 중인 대부분의 장치가 1,600만 색상 (빨간색, 녹색 및 파란색에 대해 0-255)을 지원합니다. <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## 이 차원을 데이터로 채우기

이 차원은 조회 테이블을 참조하며 비트 값을 보다 읽기 쉬운 형식으로 변환하며 이미지 요청의 [`c` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 수집합니다. AppMeasurement는 `screen.colorDepth` 변수를 사용하여 이미지 요청 쿼리 문자열을 채웁니다. AppMeasurement를 사용하는 경우 (Adobe Experience Platform Launch 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우 (API 등을 통해)에는 유효한 비트 값으로 각 히트에서 `c` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 항목

차원 항목에는 장치에서 지원하는 색상 수가 포함됩니다. 값의 예로는 `"16 million (24-bit)"`, `"16 million (32-bit)"` 및 `"65,536 (16-bit)"`이 있습니다. AppMeasurement에서 색상 깊이를 파악할 수 없는 경우 이 차원은 `"None"`으로 표시됩니다.

>[!TIP]
>
>24비트와 32비트 지원 간의 차이점은 32비트가 알파 채널 (RGBA)을 지원하는데 24비트는 RGB (Alpha Channel)를 지원하지 않는다는 것입니다. 이 개념에 대한 자세한 내용은 Wikipedia의 [색상 깊이](https://en.wikipedia.org/wiki/Color_depth)를 참조하십시오.
