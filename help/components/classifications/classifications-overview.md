---
title: 분류 개요
description: 차원 항목 그룹을 사용자 정의합니다.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: 1e209d4313c3d9d67f15a0c3a0939ceeb7a1ed31
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 87%

---

# 분류 개요

분류란 Analytics 변수 데이터를 카테고리별로 분류하여 보고서를 생성할 때 여러 다른 방법으로 데이터를 표시하는 방법입니다. 변수 값 및 해당 값과 관련된 메타데이터 간의 관계를 설정합니다. [추적 코드](/help/components/dimensions/tracking-code.md), [Prop](/help/components/dimensions/prop.md) 및 [eVar](/help/components/dimensions/evar.md)와 같은 대부분의 사용자 정의 차원에서 분류를 사용할 수 있습니다.

* **분류 집합**&#x200B;은(는) 데이터를 분류하는 기본 구성 요소입니다. [분류 세트](/help/components/classifications/sets/overview.md)를 사용하면 간소화된 단일 인터페이스에서 분류를 만들고 관리할 수 있습니다.

* **기존 분류**&#x200B;는 기존 분류 방법을 문서화하여 데이터를 분류합니다. 이 방법은 더 이상 사용되지 않으며 2026년 8월 31일 이후 더 이상 액세스할 수 없습니다.

   * [분류 규칙](/help/components/classifications/crb/classification-rule-builder.md): 분류 차원 항목에 주어진 차원 항목을 할당하는 규칙을 만듭니다. 이러한 데이터 분류 방법은 차원에 새 고유 값이 자주 발생하거나 빈번한 수동 분류가 부담이 되는 경우 가장 적합합니다.
   * [분류 가져오기 도구](/help/components/classifications/importer/c-working-with-saint.md): 각 행의 차원 항목이 포함된 템플릿 스프레드시트를 내보냅니다. 열은 차원에 대한 각 분류를 나타냅니다. 이러한 데이터 분류 방법은 모든 차원 항목이 알려진 경우 가장 적합하며, 자주 업데이트할 필요가 없습니다.

단일 차원에는 여러 분류 차원이 있을 수 있습니다. 예를 들어 제품 이름, 색상, 크기, 설명 및 SKU와 같은 추가 제품 속성을 사용하여 [!UICONTROL 제품 ID]를 분류할 수 있습니다. 이 속성 각각은 동일한 상위 차원에 속하는 별도의 분류 차원이 될 것입니다. 이러한 속성으로 보고서를 보강하면 보다 심층적이고 복잡한 보고 기회를 얻을 수 있습니다. 차원에 분류 데이터가 포함되면 분류 차원은 분류 차원 항목만 포함된 보고에 사용할 수 있습니다. 분류 값을 포함하지 않는 모든 상위 차원 항목은 [지정되지 않음](/help/technotes/unspecified.md) 아래에 그룹화됩니다.
