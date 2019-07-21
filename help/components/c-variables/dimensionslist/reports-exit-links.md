---
description: 사이트 외부로 이동할 때 사람들이 클릭하는 가장 일반적인 링크를 표시합니다. 이러한 링크는 일반적으로 파트너 또는 제휴 사이트를 가리킵니다. 그러나 이러한 링크는 외부 링크를 구현한 모든 위치가 될 수 있습니다. 이 보고서를 사용하여 가장 인기 있는 제휴 링크를 보거나, 제공한 파트너 상태의 레퍼러 수를 확인하도록 지원할 수 있습니다.
seo-description: 사이트 외부로 이동할 때 사람들이 클릭하는 가장 일반적인 링크를 표시합니다. 이러한 링크는 일반적으로 파트너 또는 제휴 사이트를 가리킵니다. 그러나 이러한 링크는 외부 링크를 구현한 모든 위치가 될 수 있습니다. 이 보고서를 사용하여 가장 인기 있는 제휴 링크를 보거나, 제공한 파트너 상태의 레퍼러 수를 확인하도록 지원할 수 있습니다.
seo-title: 종료 링크
solution: Analytics
title: 종료 링크
topic: 보고서
uuid: E 1452 F 04-389 D -4 AA 3-8763-732880284302
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 종료 링크

사이트 외부로 이동할 때 사람들이 클릭하는 가장 일반적인 링크를 표시합니다. 이러한 링크는 일반적으로 파트너 또는 제휴 사이트를 가리킵니다. 그러나 이러한 링크는 외부 링크를 구현한 모든 위치가 될 수 있습니다. 이 보고서를 사용하여 가장 인기 있는 제휴 링크를 보거나, 제공한 파트너 상태의 레퍼러 수를 확인하도록 지원할 수 있습니다.

이 페이지가 정확하게 채워지려면 충족되어야 할 몇 가지 요구 사항이 있습니다.

* 수동 사용자 지정 링크 추적을 사용하는 경우 *`s.tl()`* 요청은 중간 매개 변수가 *e*&#x200B;로 설정된 상태에서 실행되어야 합니다.

* 자동 사용자 지정 링크 추적을 사용하는 경우 다음과 같은 요구 사항이 모두 충족되어야 합니다.
* 

   * [s.trackExternalLinks](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_trackexlinks)는 *참*&#x200B;으로 설정되어야 합니다.

   * 사용자가 클릭한 링크는 [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_linkinfilters) 변수 이내의 어떤 값과도 일치하면 안 됩니다.
   * [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_linkinfilters)가 구현된 경우 외부 링크는 이 변수에 설정된 값 중 적어도 1개와 일치해야 합니다.

* 위 요구 사항 중 어느 하나라도 충족하지 않는 경우 히트가 이 보고서에 채워지지 않습니다.

* 
* 모든 사용자 지정 링크 추적 히트와 같이 [s.pageName](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_pagename) 변수는 페이지 보기 인플레이션을 방지하기 위해 이미지 요청으로부터 제거됩니다.
* 이 보고서는 트렌드 형식과 등급 형식으로 볼 수 있습니다.
* 이 보고서에서 검색 필터를 사용하여 특정 라인 항목을 찾을 수 있습니다.
* You can create [관리 도구를 통해 다른 변수를](/help/analyze/reports-analytics/reports-customize/breakdowns.md) 분류합니다.
* [인스턴스](../../../components/c-variables/c-metrics/metrics-instance.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF)는 이 보고서 내에서 기본적으로 사용할 수 있는 유일한 지표이며, 종료 링크가 실행된 시간 수를 계산할 수 있습니다.
* 일일, 주별, 월별 및 분기별 방문자가 이 보고서에 대해 활성화될 수 있습니다. 단, Adobe 담당자만 추가 비용으로 이러한 방문자를 활성화할 수 있습니다. 모든 사용자 지정 링크 추적 변수에 대한 고유 방문자 수를 활성화하면 보고서 세트에 대한 지연이 크게 증가합니다.

