---
title: 단일 페이지 방문 횟수
description: 방문이 하나의 페이지로 이루어졌음을 나타내는 플래그입니다.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 81%

---


# 단일 페이지 방문 횟수

*이 도움말 페이지에서는 &#39;단일 페이지 방문 횟수&#39;가 차원으로 작동하는 방식을 설명합니다. 자세한 내용은[단일 페이지 방문 횟수](../metrics/single-page-visits.md)지표를 참조하십시오.*

The &#39;Single page visits&#39; dimension reports the number of visits that consisted of a single unique [Page](page.md) dimension item. [단일 페이지 방문 횟수](../metrics/single-page-visits.md) 지표의 차원 양식입니다.

이 차원은 [세그멘테이션](../segmentation/seg-home.md) 내의 구성 요소로서 가장 일반적으로 사용됩니다. 일반적으로 보고서에서 차원으로 사용되지 않습니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

The only dimension item is `"Enabled"`. 방문이 하나의 페이지로 이루어진 경우 히트가 이 값으로 설정됩니다. 다른 모든 히트는 이 보고서에서 생략됩니다.
