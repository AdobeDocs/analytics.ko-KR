---
title: 페이지를 찾을 수 없음
description: 사이트에서 오류를 반환하는 URL입니다.
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '214'
ht-degree: 100%

---

# 페이지를 찾을 수 없음

*이 도움말 페이지에서는 &#39;페이지를 찾을 수 없음&#39;이 차원으로 작동하는 방식을 설명합니다. 자세한 내용은 [페이지를 찾을 수 없음](../metrics/pages-not-found.md) 지표를 참조하십시오.*

페이지를 찾을 수 없음 차원은 오류가 포함된 URL을 보여줍니다. 이 차원은 방문자가 사이트에서 받은 오류의 수를 줄이려 할 때 유용합니다.

* [흐름 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)에서 이 차원을 사용하여 방문자가 어느 페이지를 클릭스루하여 오류에 도달하는지 확인할 수 있습니다. 확인이 되면 조직의 개발 팀과 협력하여 각 페이지에서 링크를 수정할 수 있습니다.
* [레퍼러](referrer.md) 차원과 함께 이 차원을 사용하면 방문자가 외부 링크에서 사이트에 도착하는 위치를 확인할 수 있습니다. 그런 다음 원하는 위치로의 리디렉션을 구현하거나, 타사와 협력하여 링크를 수정할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`pageType` 및 `g` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. `pageType` 쿼리 문자열이 `errorPage`인 경우 `g` 쿼리 문자열 (페이지 URL)이 기록됩니다. AppMeasurement는 [`pageType`](/help/implement/vars/page-vars/pagetype.md) 변수를 사용하여 이 데이터를 수집합니다. `pageType` 변수가 정의되지 않았거나 `errorPage`가 아닌 다른 변수로 설정되어 있으면 이 차원에 대한 데이터가 수집되지 않습니다.

## 차원 항목

차원 항목에는 오류가 발생한 사이트의 페이지 URL이 포함됩니다.
