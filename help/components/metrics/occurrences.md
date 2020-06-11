---
title: 발생 횟수
description: 변수가 설정되거나 지속된 히트 수.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 발생 횟수

&#39;발생 횟수&#39; 지표는 주어진 차원이 설정되거나 지속된 히트 수를 보여줍니다. 작업 공간의 차원을 빈 캔버스로 드래그하면 Adobe는 이 지표를 프로젝트에 자동으로 적용합니다.

## 이 지표의 계산 방법

보고서 세트의 모든 히트 중에서 차원 값이 정의되거나 지속되는 히트를 포함합니다. eVar [와](../dimensions/evar.md)같은 일부 차원은 설정된 히트를 넘어서까지 지속됩니다. 페이지 [보기 횟수](page-views.md) 및 발생 횟수 [와 같은](occurrences.md) 지표는 초기 값과 지속적인 값을 모두 계산합니다. 이 지표는 지속적인 값을 계산하지 않습니다.

## 유사한 지표와 비교

* **발생과 인스턴스[비교](instances.md)**: 발생 횟수: 차원 값이 설정되거나 지속된 히트. 인스턴스는 차원 값이 지속되는 히트를 포함하지 않습니다.
* **발생과[페이지 보기](page-views.md)**: 발생에는 페이지 보기 추적 호출([`t()`](/help/implement/vars/functions/t-method.md)) 및 링크 추적 호출([`tl()`](/help/implement/vars/functions/tl-method.md))을 비롯한 모든 히트 유형이 포함됩니다. 페이지 보기 지표에는 페이지 보기 추적 호출만 포함되며 링크 추적 호출은 제외됩니다.