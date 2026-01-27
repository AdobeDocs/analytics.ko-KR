---
description: 시각적 오버레이로 링크 활동의 순위를 매겨 웹 페이지의 대상자 참여를 모니터링합니다.
title: Activity Map 개요
feature: Activity Map
role: User, Admin
exl-id: 30a800f7-e2c8-443e-b5d4-36834ef0ba20
source-git-commit: a7670fcda3e8e6af0c036c8b263746e142278255
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 100%

---

# Activity Map 개요

Adobe Analytics Activity Map은 웹 페이지 및 모바일 앱에서의 사용자 참여를 시각적으로 표현하는 Adobe Analytics의 기능입니다. 이를 통해 마케터와 분석가는 클릭 및 스크롤 동작과 같은 사용자 상호 작용을 추적하고 분석할 수 있습니다. Activity Map은 웹 페이지에서 가장 인기 있는 요소를 보여주는 히트맵과 오버레이 보고서를 생성하여 디지털 경험을 최적화하는 데 도움을 줍니다.

개념으로서의 Activity Map은 다음과 같은 몇 가지 중요한 구성 요소로 구성됩니다.

* **보고서 세트 설정**: 보고서 세트를 사용하려면 먼저 Activity Map을 활성화해야 합니다. 보고서 세트 설정에서 [Activity Map 보고](/help/admin/tools/manage-rs/edit-settings/activity-map.md)를 참조하십시오.
* **구현**: 대부분의 Activity Map 보고는 기본으로 사용할 수 있습니다. 그러나 일부 웹 사이트에서는 링크 추적을 최대한 활용하기 위해 추가 구현이 필요할 수 있습니다. 다음과 같은 구현 변수를 사용할 수 있습니다.
   * [`ActivityMap.linkExclusions`](/help/implement/vars/config-vars/activitymap-linkexclusions.md): 링크 이름별로 클릭 데이터를 필터링합니다.
   * [`ActivityMap.regionExclusions`](/help/implement/vars/config-vars/activitymap-regionexclusions.md): 지역 이름별로 클릭 데이터를 필터링합니다.
   * [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md): Activity Map 지역 차원을 채우는 속성을 변경합니다.
   * [`ActivityMap.link`](/help/implement/vars/functions/activitymap-link.md): Activity Map이 Activity Map 링크 차원을 채우기 위해 사용하는 논리를 사용자 정의합니다.
   * [`ActivityMap.region`](/help/implement/vars/functions/activitymap-region.md): Activity Map이 Activity Map 지역 차원을 채우기 위해 사용하는 논리를 사용자 정의합니다.
* **오버레이**: 웹 사이트에 오버레이된 클릭 데이터를 볼 수 있는 브라우저 확장 기능. 자세한 내용은 [Activity Map 확장 기능 인터페이스](overlay/overview.md)를 참조하십시오. 이 기능은 웹 SDK 구현에 사용할 수 없습니다.
* **차원**: Activity Map에서는 오버레이 확장 기능 외에도 Analysis Workspace에서 사용할 수 있는 여러 차원을 제공합니다.
   * [Activity Map 링크](/help/components/dimensions/activity-map-link.md): 클릭한 링크 이름.
   * [Activity Map 지역](/help/components/dimensions/activity-map-region.md): 클릭한 지역 이름.
   * [Activity Map 페이지](/help/components/dimensions/activity-map-page.md): 링크를 클릭한 시점의 페이지 이름.
   * [지역별 Activity Map 링크](/help/components/dimensions/activity-map-link-by-region.md): Activity Map 링크와 Activity Map 지역의 연결된 값.

## 기능 및 이점

* **사용자 참여 시각화**: Activity Map은 사용자 행동을 동적으로 시각화하여 사용자가 클릭하는 위치를 정확하게 확인할 수 있습니다. 이러한 시각적 데이터를 통해 패턴, 트렌드 및 관심도를 보다 쉽게 파악할 수 있습니다. 그러면 디자인, 콘텐츠 배치 및 사용자 흐름에 대해 정보에 입각한 결정을 내릴 수 있습니다.

* **히트맵**: Activity Map은 웹 페이지에서 가장 많이 클릭하거나 상호 작용한 영역을 표시하는 히트맵을 생성합니다. 히트맵은 색상 코딩을 사용하여 사용자 참여 수준을 표시하므로 핫스팟을 식별하고 우선적으로 영향이 큰 영역에 주의를 집중할 수 있습니다. 이 정보는 클릭 유도 버튼, 링크, 양식 또는 기타 대화형 요소를 최적화하는 데 유용할 수 있습니다.

* **오버레이 보고서**: Activity Map의 오버레이 보고서는 웹 페이지의 특정 요소에 대한 자세한 클릭 지표를 제공합니다. 개별 요소의 클릭스루 비율과 사용자 참여 수준을 이해함으로써 디자인 및 콘텐츠 전략을 미세 조정하여 사용자 경험을 향상시킵니다. 이 기능은 웹 SDK 구현에 사용할 수 없습니다.

* **세그먼트 분석**: 트래픽 소스, 인구 통계 또는 페르소나 등 다양한 세그먼트를 기반으로 사용자 동작을 분석할 수 있습니다. 데이터를 세분화함으로써 특정 사용자 그룹에 대한 귀중한 인사이트를 발견하여 개인화된 경험과 타기팅된 마케팅 전략을 구현할 수 있습니다.

## 실제 애플리케이션

* **웹 사이트 최적화**: Activity Map은 성과가 낮은 요소를 식별하고, 탐색 기능을 개선하고, 전반적인 사용자 경험을 향상시킴으로써 웹 사이트를 최적화하는 데 도움이 됩니다. 사용자 상호 작용을 분석함으로써 데이터 기반 의사 결정에 따라 사용자 흐름을 간소화하고 양식을 단순화하거나 콘텐츠 배치를 조정하여 효과를 극대화할 수 있습니다.

* **전환율 최적화**: 사용자 참여를 시각화하고 클릭스루 비율을 분석함으로써 Activity Map은 CRO 활동에 중요한 역할을 합니다. 다양한 디자인 변형을 통해 전환 및 실험을 방해하는 장애물을 식별하여 전환 단계, 랜딩 페이지와 체크아웃 프로세스를 최적화할 수 있습니다.

* **A/B 테스트**: Activity Map을 A/B 테스트와 결합하여 디자인 또는 콘텐츠 변경 내용이 미치는 영향을 측정할 수 있습니다. 다양한 웹 페이지 버전 간의 참여 지표를 비교함으로써 사용자 참여, 전환율 또는 매출을 높일 수 있는 변형을 결정할 수 있습니다.

