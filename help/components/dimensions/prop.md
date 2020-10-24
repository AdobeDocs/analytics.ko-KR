---
title: Prop
description: 보고에 사용할 수 있는 사용자 지정 차원입니다.
translation-type: ht
source-git-commit: cd2225ec00190af6b616f313b419935c4f8dfafd
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---


# Prop

*이 도움말 페이지에서는 prop이 차원으로 작동하는 방식을 설명합니다. prop 구현 방법에 대한 자세한 내용은 구현 사용 안내서의 [prop](/help/implement/vars/page-vars/prop.md)을 참조하십시오.*

prop은 원하는 대로 사용할 수 있는 사용자 지정 변수입니다. prop이 설정된 히트 이후에는 지속되지 않습니다.

>[!TIP]
>
>대부분의 경우 [eVar](evar.md)를 사용하는 것이 좋습니다. 이전 버전의 Adobe Analytics에서는 prop 및 eVar가 서로 장단점이 있었습니다. 그러나 Adobe는 prop에 대한 거의 모든 사용 사례를 충족하도록 eVar를 개선했습니다.

[솔루션 설계 문서](/help/implement/prepare/solution-design.md)가 있는 경우 이러한 사용자 지정 차원을 조직 고유의 값에 할당할 수 있습니다. 사용 가능한 prop의 수는 Adobe와의 계약에 따라 달라집니다. Adobe와의 계약이 지원하는 경우 최대 75개의 prop을 사용할 수 있습니다.

## 데이터로 prop 채우기

각 prop은 이미지 요청의 [`c1` - `c75` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. 예를 들어 `c1` 쿼리 문자열 매개 변수는 prop1에 대한 데이터를 수집하는 반면 `c68` 쿼리 문자열 매개 변수는 prop68에 대한 데이터를 수집합니다.

JavaScript 변수를 데이터 수집을 위한 이미지 요청으로 컴파일하는 AppMeasurement는 변수 `prop1` - `prop75`을 사용합니다. 구현 지침이 필요하면 구현 사용 안내서의 [prop](/help/implement/vars/page-vars/prop.md)을 참조하십시오.

## 차원 항목

prop은 구현의 사용자 지정 문자열을 포함하므로 조직에서 각 prop에 대한 차원 항목을 결정합니다. [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 각 prop의 목적과 일반적인 차원 항목을 반드시 기록하십시오.

## 대/소문자 구분

기본적으로 Prop은 대/소문자를 구분하지 않습니다. 같은 값을 대소문자를 달리하여(예: `"DOG"` 및 `"Dog"`)에 보낼 경우, Analysis Workspace는 동일한 차원 항목으로 함께 그룹화합니다. 보고 월의 시작 부분에 표시되는 첫 번째 값의 대소문자가 사용됩니다. Data Warehouse는 요청 기간 동안 발생한 첫 번째 값을 표시합니다.

prop 대/소문자를 구분하도록 지정할 수 있습니다. 어떤 prop에 대해서든 대소문자 구분을 활성화한 후 비활성화할 수도 있습니다. 대/소문자 구분을 전환하려면 보고서 세트 ID와 원하는 변수를 사용하여 Adobe 고객 지원 센터에 문의하십시오.

>[!IMPORTANT]
>
>대/소문자 구분을 전환하면 차원 항목을 클리프할 수 있고, 세그먼트에 예기치 않은 결과가 발생하며, 필터에 문제가 발생합니다. 이 설정은 한 달 또는 1년의 시작과 같이 주요한 두 기간 간에 전환하는 것이 좋습니다.

## eVar에 대한 prop 값

대부분의 경우 eVar를 사용하는 것이 좋습니다. 이 문에 대한 예외는 다음과 같습니다.

* 실시간 보고서에서 prop을 사용할 수 있습니다. eVar가 보고에 나타나려면 최소 30분이 소요됩니다.
* prop은 동일한 히트에서 여러 값을 수락하는 목록 prop이 될 수 있습니다. 목록 변수는 별개의 변수이며 사용할 수 있는 목록 변수는 세 개뿐입니다.
* prop에 대한 경로 지정을 활성화하면 [시작](entry-dimensions.md) 및 [종료](exit-dimensions.md) 차원을 즉시 사용할 수 있게 됩니다. eVar에 대한 시작 및 종료 차원이 필요한 경우 수동으로 세그먼트를 만들 수 있습니다.

prop과 eVar 간의 비교 내용을 더 알려면 [eVar](evar.md)를 참조하십시오.
