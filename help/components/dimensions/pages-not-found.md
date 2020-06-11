---
title: 페이지를 찾을 수 없음
description: 사이트에서 오류를 반환하는 URL.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 2%

---


# 페이지를 찾을 수 없음

*이 도움말 페이지에서는 &#39;페이지를 찾을 수 없음&#39;이 차원으로 작동하는 방식을 설명합니다. 자세한 내용은[페이지를 찾을](../metrics/pages-not-found.md)수 없음 지표를 참조하십시오.*

&#39;페이지를 찾을 수 없음&#39; 차원은 오류가 포함된 URL을 표시합니다. 이 차원은 방문자가 사이트에서 얻는 오류 수를 줄이려는 경우 유용합니다.

* 흐름 시각화에서 이 [차원을 사용하여](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) 방문자가 어떤 페이지를 클릭스루하여 오류를 범하는지 확인할 수 있습니다. 그런 다음 조직의 개발 팀과 협력하여 각 페이지의 링크를 수정할 수 있습니다.
* &#39;레퍼러&#39; 차원과 함께 이 차원 [을](referrer.md) 사용하여 방문자가 외부 링크에서 사이트에 도착하는 위치를 확인할 수 있습니다. 그런 다음 원하는 위치로 리디렉션을 구현하거나, 제3자와 작업하여 링크를 수정할 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`pageType` 및 `g` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. 쿼리 `pageType` 문자열이 같은 `errorPage`경우 `g` 쿼리 문자열(페이지 URL)이 기록됩니다. AppMeasurement는 변수를 사용하여 이 데이터를 [`pageType`](/help/implement/vars/page-vars/pagetype.md) 수집합니다. 변수가 `pageType` 정의되지 않았거나 다른 변수로 설정되어 `errorPage`있으면 이 차원에 대한 데이터가 수집되지 않습니다.

## 차원 값

차원 값에는 오류가 발생한 사이트의 페이지 URL이 포함됩니다.
