---
title: 페이지 조회수
description: 차원 항목이 Adobe Analytics에서 설정되거나 지속된 횟수입니다.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 51%

---

# 페이지 조회수

**[!UICONTROL 페이지 보기 수]** [지표](overview.md)은(는) 주어진 차원 항목이 페이지에 설정되거나 지속된 횟수를 보여줍니다. 보고서에서 가장 일반적이고 기본적인 지표 중 하나입니다.

## 이 지표의 계산 방법

이 지표는 보고서 세트의 모든 페이지 보기 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md))을 계산합니다. 차원의 경우 차원 항목이 설정되어 있거나 지속된 히트가 포함됩니다. 링크 추적 호출([`tl()`](/help/implement/vars/functions/tl-method.md))이나 [데이터 원본](/help/import/data-sources/overview.md)의 데이터는 포함되지 않습니다.

## 유사한 지표와 비교

* **페이지 보기 수와 [방문 횟수](visits.md)**: 페이지 보기 수는 페이지를 본 횟수를 계산합니다. 방문 횟수는 방문자의 세션 수를 계산합니다. 방문 횟수 1회는 1회 이상의 페이지 조회수로 구성됩니다.
* **페이지 보기 수와 [페이지 이벤트](page-events.md)**: 페이지 보기 수는 페이지 보기 추적 호출(`t()`)의 수를 계산하며, 링크 추적 호출(`tl()`)을 제외합니다. 이와 반대로 페이지 이벤트는 링크 추적 호출 수를 계산하며 페이지 조회수 추적 호출을 제외합니다.
