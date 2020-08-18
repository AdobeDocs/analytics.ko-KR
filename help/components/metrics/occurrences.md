---
title: 발생 횟수
description: 변수가 설정되었거나 지속된 히트의 수입니다.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 67%

---


# 발생 횟수

발생 횟수 지표는 주어진 차원이 설정되거나 지속된 히트의 수를 보여줍니다. Workspace의 차원을 빈 캔버스로 드래그하면 이 지표가 프로젝트에 자동으로 적용됩니다.

## 이 지표의 계산 방법

보고서 세트의 모든 히트 중에서 차원 항목이 정의되거나 지속되는 히트를 포함합니다. [eVar](../dimensions/evar.md)와 같은 일부 차원은 이 차원이 설정된 히트 이후에 유지됩니다. 이 지표는 초기 값과 지속적인 값을 모두 계산합니다.

## 유사한 지표와 비교

* **발생과 인스턴스[비교](instances.md)**:발생 횟수: 차원 항목이 설정되거나 지속된 히트. 인스턴스는 차원 항목이 지속되는 히트를 포함하지 않습니다.
* **발생 횟수와[페이지 보기 수](page-views.md)** 비교: 발생 횟수에는 페이지 보기 추적 호출([`t()`](/help/implement/vars/functions/t-method.md))과 링크 추적 호출([`tl()`](/help/implement/vars/functions/tl-method.md))을 포함하여 모든 히트 유형이 포함됩니다. 페이지 보기 수 지표에는 페이지 보기 추적 호출만 포함되며 링크 추적 호출은 제외됩니다.
