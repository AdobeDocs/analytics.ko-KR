---
title: 인스턴스
description: 변수가 설정된(지속되지 않음) 히트의 수입니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '129'
ht-degree: 100%

---


# 인스턴스

인스턴스 지표는 이미지 요청에서 차원이 명시적으로 정의된 횟수를 보여줍니다. [eVar](../dimensions/evar.md)와 같은 일부 차원은 이 차원이 설정된 히트 이후에 차원 항목을 유지합니다. 이 지표는 해당 값이 지속된 히트가 없는 상태에서 차원 항목이 설정된 횟수를 보려는 경우에 유용합니다.

## 이 지표의 계산 방법

보고서 세트의 모든 히트 중에서 이미지 요청에 차원 항목을 명시적으로 설정하는 히트만 포함하십시오. [eVar](../dimensions/evar.md)와 같은 일부 차원은 이 차원이 설정된 히트 이후에 유지됩니다. [페이지 보기 수](page-views.md) 및 [발생 횟수](occurrences.md)와 같은 지표는 초기 값과 지속되는 값을 모두 계산하지만, 이 지표는 지속되는 값을 계산하지 않습니다.