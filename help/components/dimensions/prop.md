---
title: Prop
description: 보고에 사용할 수 있는 사용자 지정 차원입니다.
translation-type: tm+mt
source-git-commit: 10e157e370367374b55ee9c87c0e5c7ca9e99c1a
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 28%

---


# Prop

*이 도움말 페이지에서는 prop이 차원으로 작동하는 방식을 설명합니다. For information on how to implement props, see[props](/help/implement/vars/page-vars/prop.md)in the Implement user guide.*

prop은 원하는 대로 사용할 수 있는 사용자 지정 변수입니다. 설정된 히트 이후로 지속되지 않습니다.

> [!TIP][ 대부분의 경우 eVar를 사용하는 것이 좋습니다. ](evar.md) 이전 버전의 Adobe Analytics에서는 prop 및 eVar가 서로 장단점이 있었습니다. 그러나 Adobe는 prop에 대한 거의 모든 사용 사례를 충족하도록 eVar를 개선했습니다.

솔루션 디자인 문서 [](/help/implement/prepare/solution-design.md)가 있는 경우 이러한 사용자 지정 차원을 조직 고유의 값에 할당할 수 있습니다. 사용 가능한 prop의 수는 Adobe와의 계약에 따라 달라집니다. Adobe와의 계약이 지원하는 경우 최대 75개의 prop을 사용할 수 있습니다.

## 데이터로 prop 채우기

각 prop은 이미지 요청의 [`c1` - `c75` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 수집합니다. 예를 들어 `c1` 쿼리 문자열 매개 변수는 prop1에 대한 데이터를 수집하는 반면 `c68` 쿼리 문자열 매개 변수는 prop68에 대한 데이터를 수집합니다.

JavaScript 변수를 데이터 수집에 대한 이미지 요청으로 컴파일하는 AppMeasurement는 변수 `prop1` -를 사용합니다 `prop75`. 구현 [가이드라인에](/help/implement/vars/page-vars/prop.md) 대해서는 구현 사용 안내서의 prop을 참조하십시오.

## 차원 값

Prop에는 구현에 사용자 지정 문자열이 포함되어 있으므로 조직은 각 prop에 대한 차원 값을 결정합니다. 각 prop의 용도와 일반적인 차원 값을 [솔루션 디자인 문서에 기록해야 합니다](/help/implement/prepare/solution-design.md).

## eVar에 대한 prop 값

대부분의 경우 eVar를 사용하는 것이 좋습니다. 이 문에 대한 예외는 다음과 같습니다.

* 실시간 보고서에서 prop을 사용할 수 있습니다. eVar가 보고에 나타나려면 최소 30분이 소요됩니다.
* prop은 동일한 히트에서 여러 값을 수락하는 목록 prop이 될 수 있습니다. 목록 변수는 별개의 변수이며 사용할 수 있는 목록 변수는 세 개뿐입니다.
* prop에 대한 경로 지정을 활성화하면 [시작](entry-dimensions.md) 및 [종료](exit-dimensions.md) 차원을 즉시 사용할 수 있게 됩니다. eVar에 대한 시작 및 종료 차원을 수동으로 만들 수 있습니다.

prop [과 eVar](evar.md) 간의 더 많은 비교는 eVar를 참조하십시오.
