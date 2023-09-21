---
title: 계층
description: 보고에 사용할 수 있는 사용자 정의 차원입니다.
feature: Dimensions
exl-id: f9bd3ae1-3578-44c5-a540-ea93feac5bef
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 92%

---

# 계층

>[!IMPORTANT]
>
>이 차원은 사용이 중단되었으며 사용할 수 없습니다. [차원](overview.md) Analysis Workspace. Adobe에서는 대신 [eVar](evar.md) 및 분류를 사용하는 것이 좋습니다.

계층은 원하는 대로 사용할 수 있는 사용자 정의 변수입니다. prop이 설정된 히트 이후에는 지속되지 않습니다. Adobe와의 계약이 지원하는 경우 최대 5개의 계층을 사용할 수 있습니다.

## 데이터로 계층 채우기

각 계층은 이미지 요청의 [`h1` - `h5` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. 예를 들어 `h1` 쿼리 문자열 매개변수는 계층 1에 대한 데이터를 수집하는 반면 `h4` 쿼리 문자열 매개변수는 계층 4에 대한 데이터를 수집합니다.

JavaScript 변수를 데이터 수집을 위한 이미지 요청으로 컴파일하는 AppMeasurement는 변수 `hier1` - `hier5`을 사용합니다. 구현 지침이 필요하면 구현 사용 안내서의 [hier](/help/implement/vars/page-vars/hier.md)를 참조하십시오.

## 차원 항목

계층은 구현의 사용자 정의 문자열을 포함하므로 조직에서 각 계층에 대한 차원 항목을 결정합니다. [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 각 계층의 목적과 일반적인 차원 항목을 반드시 기록하십시오.
