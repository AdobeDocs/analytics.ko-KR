---
description: 시각적 오버레이를 사용하여 링크 활동의 등급을 매겨 웹 페이지의 대상자 참여를 모니터링합니다.
title: Activity Map 개요
feature: Activity Map
role: User, Admin
exl-id: 30a800f7-e2c8-443e-b5d4-36834ef0ba20
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---

# Activity Map 개요

Adobe Analytics Activity Map은 웹 페이지 및 모바일 앱에서의 사용자 참여를 시각적으로 표현하는 Adobe Analytics의 기능입니다. 이를 통해 마케터와 분석가는 클릭 및 스크롤 동작과 같은 사용자 상호 작용을 추적하고 분석할 수 있습니다. Activity Map은 웹 페이지에서 가장 인기 있는 요소를 보여주는 히트 맵 및 오버레이 보고서를 생성하여 디지털 경험을 최적화하는 데 도움이 됩니다.

이 설명서 섹션에서는 Activity Map 오버레이에 중점을 둡니다. 그러나 Activity Map 사용에 있어 다른 중요한 부분이 있습니다.

* **보고서 세트 설정**: 보고서 세트에는 Activity Map이 활성화되어 있어야 합니다. 보고서 세트 설정에서 [Activity Map 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/activity-map.md)를 참조하십시오.
* **구현**: 대부분의 Activity Map 보고는 즉시 사용할 수 있습니다. 그러나 일부 웹 사이트에서는 링크 추적을 최대한 활용하기 위해 추가 구현이 필요할 수 있습니다. 다음 구현 변수를 사용할 수 있습니다.
   * [`ActivityMap.linkExclusions`](/help/implement/vars/config-vars/activitymap-linkexclusions.md): 링크 이름별로 클릭 데이터를 필터링합니다.
   * [`ActivityMap.regionExclusions`](/help/implement/vars/config-vars/activitymap-regionexclusions.md): 지역 이름별로 클릭 데이터를 필터링합니다.
   * [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md): Activity Map 영역 차원을 채우는 특성을 변경합니다.
   * [`ActivityMap.link`](/help/implement/vars/functions/activitymap-link.md): Activity Map이 Activity Map 링크 차원을 채우는 데 사용하는 논리를 사용자 지정합니다.
   * [`ActivityMap.region`](/help/implement/vars/functions/activitymap-region.md): Activity Map이 Activity Map 영역 차원을 채우는 데 사용하는 논리를 사용자 지정합니다.
* **Dimension**: Activity Map은 오버레이 확장 기능 외에도 Analysis Workspace에서 사용할 수 있는 여러 차원을 제공합니다.
   * [Activity Map 링크](/help/components/dimensions/activity-map-link.md): 클릭한 링크 이름입니다.
   * [Activity Map 지역](/help/components/dimensions/activity-map-region.md): 클릭한 지역 이름입니다.
   * [Activity Map 페이지](/help/components/dimensions/activity-map-page.md): 링크를 클릭한 시점의 페이지 이름입니다.
   * [지역별 Activity Map 링크](/help/components/dimensions/activity-map-link-by-region.md): Activity Map 링크와 Activity Map 영역의 연결된 값입니다.

## 기능 및 이점

* **Activity Map 참여 시각화**: 사용자는 사용자 행동을 동적으로 시각화하여 사용자가 클릭하는 위치를 정확하게 확인할 수 있습니다. 이러한 시각적 데이터를 통해 패턴, 트렌드 및 관심 영역을 보다 쉽게 식별할 수 있습니다. 그런 다음 디자인, 콘텐츠 배치 및 사용자 흐름에 대해 정보에 입각한 결정을 내릴 수 있습니다.

* **열 지도**: Activity Map은 웹 페이지에서 가장 많이 클릭하거나 상호 작용하는 영역을 표시하는 열 지도를 생성합니다. 히트맵은 색상 코딩을 사용하여 참여 수준을 나타내므로 핫스팟을 식별하고 영향력이 큰 영역에 주의를 기울일 수 있습니다. 이 정보는 콜 투 액션 버튼, 링크, 양식 또는 기타 대화형 요소를 최적화하는 데 유용할 수 있습니다.

* **오버레이 보고서**: Activity Map의 오버레이 보고서는 웹 페이지의 특정 요소에 대한 자세한 클릭 지표를 제공합니다. 개별 요소의 클릭스루 비율 및 참여 수준을 이해하여 디자인과 콘텐츠 전략을 세밀하게 조정하여 사용자 경험을 향상시킬 수 있습니다.

* **세그먼트 분석**: 트래픽 소스, 인구 통계 또는 가상 사용자 등 다양한 세그먼트를 기반으로 사용자 동작을 분석할 수 있습니다. 데이터를 세그먼트화하면 특정 사용자 그룹에 대한 중요한 통찰력을 발견할 수 있으므로 개인화된 경험과 타겟팅된 마케팅 전략을 사용할 수 있습니다.

## 실용적인 응용 프로그램

* **웹 사이트 최적화**: Activity Map을 사용하면 성과가 낮은 요소를 식별하고, 탐색을 개선하고, 전반적인 사용자 경험을 향상하여 웹 사이트를 최적화할 수 있습니다. 사용자 상호 작용을 분석하여 데이터 중심의 의사 결정을 통해 사용자 흐름을 간소화하고 양식을 단순화하거나 컨텐츠 배치를 조정하여 최대의 영향을 미칠 수 있습니다.

* **전환율 최적화**: Activity Map 참여를 시각화하고 클릭스루 비율을 분석함으로써 사용자는 CRO 활동에 중요한 역할을 합니다. 전환 장벽을 식별하고 다양한 디자인 변형을 실험하여 전환 단계, 랜딩 페이지 및 체크아웃 프로세스를 최적화할 수 있습니다.

* **A/B 테스트**: Activity Map을 A/B 테스트와 결합하여 디자인 또는 콘텐츠 변경의 영향을 측정할 수 있습니다. 다양한 버전의 웹 페이지 간 참여 지표를 비교하여 어떤 변형이 더 높은 사용자 참여, 전환율 또는 매출을 유도하는지 결정할 수 있습니다.

* **모바일 앱 최적화**: Activity Map은 웹 사이트로 제한되지 않으며 모바일 애플리케이션으로 기능도 확장합니다. 앱 내의 사용자 상호 작용에 대한 통찰력을 얻을 수 있으므로 유용성을 향상시키고 탐색을 향상시키며 기능을 개선하여 원활한 모바일 경험을 제공할 수 있습니다.
