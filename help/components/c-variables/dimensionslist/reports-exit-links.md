---
title: '종료 링크 '
description: 사람들이 사이트를 떠나기 위해 클릭하는 가장 일반적인 링크에 대한 보고서를 표시합니다.
translation-type: tm+mt
source-git-commit: be4c3ec95b9e93dda7603c0bdb178c0a54d800a0

---


# 종료 링크 

사용자가 사이트를 떠나기 위해 클릭하는 가장 일반적인 링크를 표시합니다. 이러한 링크는 일반적으로 파트너 또는 제휴 사이트를 가리킵니다.그러나 외부 링크가 있는 모든 위치가 될 수 있습니다. 이 보고서를 사용하여 가장 인기 있는 제휴 링크를 보거나, 제공한 파트너 상태의 레퍼러 수를 확인하도록 지원할 수 있습니다.

이 페이지가 정확하게 채워지려면 충족되어야 할 몇 가지 요구 사항이 있습니다.
* 수동 사용자 지정 링크 추적을 사용하는 경우 중간 매개 변수를 로 설정하여 `tl()` 요청을 실행해야 합니다 `e`.
* 자동 사용자 지정 링크 추적을 사용하는 경우 다음과 같은 요구 사항이 모두 충족되어야 합니다.
   * trackExternalLinks [변수를](/help/implement/vars/config-vars/trackexternallinks.md) 활성화해야 합니다.
   * The link the user clicked on must not match any values within the [linkInternalFilters](/help/implement/vars/config-vars/linkinternalfilters.md) variable.
   * If the [linkExternalFilters](/help/implement/vars/config-vars/linkexternalfilters.md) variable exists, the external link must match at least one of the values set in this variable.
* 위의 요구 사항 중 하나가 충족되지 않으면 히트가 이 보고서를 채우지 않습니다.
* 모든 사용자 지정 링크 추적 히트와 마찬가지로 [pageName](/help/implement/vars/page-vars/pagename.md) 변수는 페이지 보기 지표로 인한 인플레이션을 방지하기 위해 이미지 요청에서 제거됩니다.
* 이 보고서는 트렌드 형식과 등급 형식으로 볼 수 있습니다.
* 이 보고서에서 검색 필터를 사용하여 특정 라인 항목을 찾을 수 있습니다.
* You can create 다른 변수와 [분류를](/help/analyze/reports-analytics/reports-customize/breakdowns.md) 참조하십시오.
