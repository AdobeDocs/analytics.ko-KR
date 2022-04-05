---
title: 페이지 조회수
description: 차원 항목이 Adobe Analytics에서 설정되거나 지속된 횟수입니다.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 65f87bf4b5b3897c9ef68d091858332c08cbf699
workflow-type: ht
source-wordcount: '162'
ht-degree: 100%

---

# 페이지 조회수

페이지 보기 수 지표는 주어진 차원 항목이 페이지에 설정되거나 지속된 횟수를 보여 줍니다. 보고서에서 가장 일반적이고 기본적인 지표 중 하나입니다.

## 이 지표의 계산 방법

이 지표는 보고서 세트의 모든 페이지 보기 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md))을 계산합니다. 차원에는 차원 항목이 정의되거나 지속된 히트가 포함됩니다. 링크 추적 호출 ([`tl()`](/help/implement/vars/functions/tl-method.md))은 포함되지 않습니다.

## 유사한 지표와 비교

* **페이지 조회수 및 [방문 횟수](visits.md)**: 페이지 조회수는 페이지가 조회된 횟수를 계산합니다. 방문 횟수는 방문자의 세션 수를 계산합니다. 방문 횟수 1회는 1회 이상의 페이지 조회수로 구성됩니다.
* **페이지 조회수 및 [페이지 이벤트](page-events.md)**: 페이지 조회수는 페이지 조회수 추적 호출(`t()`) 수를 계산하며, 여기에서 링크 추적 호출(`tl()`)은 제외됩니다. 이와 반대로 페이지 이벤트는 링크 추적 호출 수를 계산하며 페이지 조회수 추적 호출을 제외합니다.
