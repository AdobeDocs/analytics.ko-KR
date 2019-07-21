---
description: Ad Hoc Analysis의 단일 페이지 방문 지표와는 다릅니다. 단일 페이지 방문 보고서는 웹 사이트 방문자가 다른 페이지를 보는 단계를 수행하지 않고 시작 및 종료한 웹 페이지를 표시합니다.
seo-description: Ad Hoc Analysis의 단일 페이지 방문 지표와는 다릅니다. 단일 페이지 방문 보고서는 웹 사이트 방문자가 다른 페이지를 보는 단계를 수행하지 않고 시작 및 종료한 웹 페이지를 표시합니다.
seo-title: 단일 페이지 방문
solution: Analytics
title: 단일 페이지 방문
topic: 보고서
uuid: 5 CA 52 BE 8-C 7 F 5-464 A -8 A 06-55 E 8271760 B 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 단일 페이지 방문

Ad Hoc Analysis의 단일 페이지 방문 지표와는 다릅니다. 단일 페이지 방문 보고서는 웹 사이트 방문자가 다른 페이지를 보는 단계를 수행하지 않고 시작 및 종료한 웹 페이지를 표시합니다.

이 보고서는 [!UICONTROL 페이지] 보고서 컨텍스트에 가장 일반적으로 사용되지만 [!UICONTROL 경로 지정]이 활성화된 모든 트래픽 변수에서 볼 수 있습니다. 이 보고서를 사용하면 방문자의 사이트 추가 탐색을 유도할 가능성이 적은 시작 페이지를 식별하거나 단일 페이지를 구성하는 방문 수를 파악할 수 있습니다. 이 정보를 사용하면 컨텐츠를 최적화하여 그러한 페이지에서의 종료를 줄일 수 있습니다.

## 보고서의 속성 {#section_2D30F939FE0648EF983DD7C1BAB1181B}

* [!UICONTROL 페이지] 보고서를 표시하며 [!UICONTROL 단일 액세스]를 지표로 사용하면 동일한 보고서를 검색할 수 있습니다.

* 단일 페이지 방문은 단일 이미지 요청이 아닌 하나의 고유 값이 포함된 방문으로 간주됩니다.

   * In the context of a [페이지 보고서](../../../components/c-variables/dimensionslist/reports-pages.md#concept_0219136EA25745B58434D0C7E751D7D5) 컨텍스트에서는 방문 내에서 하나의 고유 페이지만 실행할 수 있습니다.
   *  [사이트 섹션 보고서](../../../components/c-variables/dimensionslist/reports-site-sections.md#concept_39E550D7A9E34C9580E81F5F9E12BDDD) 컨텍스트에서는 방문 내에서 하나의 고유 사이트 섹션만 실행됩니다.
   * 한편 [트래픽 변수](/help/admin/admin/c-traffic-variables/traffic-var.md) 컨텍스트에서는 단일 고유 값이 실행된 경우만 이 보고서에 방문이 표시됩니다.

* 보고서의 컨텍스트에서 변수에 단일 고유 값이 포함되어 있으면 단일 페이지 방문이 여러 이미지 요청으로 구성될 수 있습니다. 두 번째 고유 값을 채우면 방문은 더 이상 단일 페이지 방문으로 간주되지 않습니다.
* 이 보고서는 경로 지정 보고서 유형으로 간주됩니다. 기본적으로 [!UICONTROL 페이지] 변수에는 경로 지정이 활성화되어 있습니다. 모든 트래픽 변수는 이 기능도 가지고 있습니다. 추가 트래픽 변수에 대한 경로 지정 활성화에는 계약이 적용됩니다. 자세한 내용은 조직의 계정 관리자에게 문의하십시오.
* 이 보고서에서 검색 필터를 사용하여 특정 라인 항목을 찾을 수 있습니다.
* 이 보고서는 [트렌드](/help/components/c-variables/dimensionslist/reports-types.md) 및 [등급](/help/components/c-variables/dimensionslist/reports-types.md) 형식.

* 이 보고서에서는 상세 분류를 사용할 수 없습니다.
* 이 보고서에서는 [!UICONTROL 방문] 지표만 사용할 수 있습니다.

