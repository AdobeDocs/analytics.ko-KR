---
title: '페이지 조회수 지표 설명 | Adobe Analytics '
description: Adobe Analytics에서 페이지 조회수 지표가 어떻게 작동하는지 알아보고 페이지 조회수와 방문수의 차이를 파악하십시오.
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '176'
ht-degree: 100%

---

# Adobe Analytics를 페이지 조회수에 대해 알아보기

페이지 보기 수 지표는 주어진 차원 항목이 페이지에 설정되거나 지속된 횟수를 보여 줍니다. 보고서에서 가장 일반적이고 기본적인 지표 중 하나입니다.

## 이 지표의 계산 방법

이 지표는 보고서 세트의 모든 페이지 보기 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md))을 계산합니다. 차원의 경우 차원 항목이 정의되거나 지속된 히트가 포함됩니다. 링크 추적 호출 ([`tl()`](/help/implement/vars/functions/tl-method.md))은 포함되지 않습니다.

## 유사한 지표와 비교

* **페이지 보기 수와 [방문 횟수](visits.md)**: 페이지 보기 수는 페이지를 본 횟수를 계산합니다. 방문 횟수는 방문자의 세션 수를 계산합니다. 한 번의 방문은 하나 이상의 페이지로 구성됩니다.
* **페이지 보기 수와 [페이지 이벤트](page-events.md)**: 페이지 보기 수는 페이지 보기 추적 호출의 수 (`t()`)를 계산하며, 링크 추적 호출 (`tl()`)을 제외합니다. 페이지 이벤트는 반대입니다. 링크 추적 호출 수를 계산하고 페이지 보기 수를 제외합니다.
