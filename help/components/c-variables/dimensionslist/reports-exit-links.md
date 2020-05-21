---
title: 종료 링크
description: 사람들이 사이트를 떠나기 위해 클릭하는 가장 일반적인 링크에 대한 보고서입니다.
translation-type: ht
source-git-commit: be4c3ec95b9e93dda7603c0bdb178c0a54d800a0

---


# 종료 링크

사람들이 사이트를 떠나기 위해 클릭하는 가장 일반적인 링크를 표시합니다. 이러한 링크는 일반적으로 파트너 또는 제휴 사이트를 가리키지만, 외부 링크가 있는 위치가 될 수도 있습니다. 이 보고서를 사용하여 가장 인기 있는 제휴 링크를 보거나, 제공한 파트너 상태의 레퍼러 수를 확인하도록 지원할 수 있습니다.

이 페이지가 정확하게 채워지려면 충족되어야 할 몇 가지 요구 사항이 있습니다.
* 수동 사용자 지정 링크 추적을 사용하는 경우 중간 매개 변수를 `e`로 설정하여 `tl()` 요청을 실행해야 합니다.
* 자동 사용자 지정 링크 추적을 사용하는 경우 다음과 같은 요구 사항이 모두 충족되어야 합니다.
   * [trackExternalLinks](/help/implement/vars/config-vars/trackexternallinks.md) 변수를 활성화해야 합니다.
   * 사용자가 클릭한 링크는 [linkInternalFilters](/help/implement/vars/config-vars/linkinternalfilters.md) 변수 내에 있는 어떤 값과도 일치하면 안 됩니다.
   * [linkExternalFilters](/help/implement/vars/config-vars/linkexternalfilters.md) 변수가 있는 경우 외부 링크는 이 변수에 설정된 값 중 적어도 1개와 일치해야 합니다.
* 위 요구 사항 중 어느 하나라도 충족하지 않는 경우 히트가 이 보고서에 채워지지 않습니다.
* 모든 사용자 지정 링크 추적 히트와 마찬가지로 [pageName](/help/implement/vars/page-vars/pagename.md) 변수는 페이지 보기 지표에 대한 인플레이션을 방지하기 위해 이미지 요청에서 제거됩니다.
* 이 보고서는 트렌드 형식과 등급 형식으로 볼 수 있습니다.
* 이 보고서에서 검색 필터를 사용하여 특정 라인 항목을 찾을 수 있습니다.
*  다른 변수를 사용하여 [분류](/help/analyze/reports-analytics/reports-customize/breakdowns.md)할 수 있습니다.
