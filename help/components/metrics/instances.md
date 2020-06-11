---
title: 인스턴스
description: 변수가 설정된 히트 수(지속되지 않음).
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---


# 인스턴스

&#39;인스턴스&#39; 지표는 이미지 요청에 차원이 명시적으로 정의된 횟수를 보여줍니다. eVar [와](../dimensions/evar.md)같은 일부 차원은 설정된 히트를 지나 차원 값을 유지합니다. 이 지표는 해당 값이 지속된 히트 없이 차원 값이 설정된 횟수를 보려는 경우에 유용합니다.

## 이 지표의 계산 방법

보고서 세트의 모든 히트 중에서 이미지 요청에 차원 값을 명시적으로 설정하는 히트만 포함합니다. eVar [와](../dimensions/evar.md)같은 일부 차원은 설정된 히트를 넘어서까지 지속됩니다. 페이지 [보기 횟수](page-views.md) 및 발생 횟수 [와 같은](occurrences.md) 지표는 초기 값과 지속적인 값을 모두 계산합니다. 이 지표는 지속적인 값을 계산하지 않습니다.