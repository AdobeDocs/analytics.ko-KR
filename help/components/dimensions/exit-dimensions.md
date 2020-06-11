---
title: 차원 종료
description: 종료 차원 및 해당 사용을 나열합니다.
keywords: exit page, exit site section, exit server, exit custom insight
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# 차원 종료

*이 도움말 페이지에서는 종료가 차원으로 작동하는 방식을 설명합니다. 종료가 지표로 작동하는 방법에 대한 자세한 내용은 종료[지표를](../metrics/exits.md)참조하십시오.*

종료 차원은 마지막 차원 값을 기록하고 방문의 모든 히트에 소급하여 적용합니다. 종료 차원은 보고서 세트 설정의 트래픽 변수 아래에서 경로 지정이 활성화된 모든 [변수에](/help/admin/admin/c-traffic-variables/traffic-var.md) 사용할 수 있습니다.

## 데이터로 종료 차원 채우기

지정된 종료 차원은 연결된 트래픽 변수를 기반으로 합니다. 비종료 변수에 데이터가 있으면 연결된 종료 차원에도 데이터가 포함됩니다. 트래픽 변수에 데이터가 포함된 경우 종료 차원에 대해 구현 변경이 필요하지 않습니다.

## 차원 값

종료 변수는 일반적으로 구현의 사용자 지정 문자열을 기반으로 하므로 조직에서 차원 값이 무엇인지 결정합니다. 지정된 종료 차원의 값은 연결된 비종료 차원의 차원 값과 일치합니다. 예를 들어 &#39;종료 페이지&#39; 차원의 차원 값에는 &#39;페이지&#39; 차원의 비슷한 차원 값이 포함됩니다.
