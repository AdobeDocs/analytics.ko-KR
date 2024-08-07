---
title: 발생 횟수
description: 변수가 설정되었거나 지속된 히트의 수입니다.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 100%

---

# 발생 횟수

“발생 횟수” [지표](overview.md)는 지정된 차원이 설정되거나 지속된 히트 수를 보여 줍니다. Workspace의 차원을 빈 캔버스로 드래그하면 이 지표가 프로젝트에 자동으로 적용됩니다.

## 이 지표의 계산 방법

보고서 세트의 모든 히트 중에서 차원 항목이 정의되어 있거나 지속되는 히트를 포함하십시오. [eVar](../dimensions/evar.md)와 같은 일부 차원은 이 차원이 설정된 히트 이후에 유지됩니다. 이 지표는 초기 값과 지속된 값을 모두 계산합니다.

## 유사한 지표와 비교

* **발생 횟수와 [인스턴스](instances.md)** 비교: 발생 횟수는 차원 항목이 설정되어 있거나 지속된 히트를 계산합니다. 인스턴스는 차원 항목이 지속되는 히트를 포함하지 않습니다.
* **발생 횟수와 [페이지 조회수](page-views.md)** 비교: 발생 횟수에는 페이지 조회수 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md)), 링크 추적 호출 ([`tl()`](/help/implement/vars/functions/tl-method.md)) 및 요약 [데이터 소스](/help/import/data-sources/overview.md)의 데이터를 포함하여 모든 히트 유형이 포함됩니다. 페이지 조회수 지표에는 페이지 조회수 추적 호출만 포함되며 링크 추적 호출 및 요약 데이터 소스는 제외됩니다.
