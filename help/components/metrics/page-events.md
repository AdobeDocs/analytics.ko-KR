---
title: 페이지 이벤트
description: 트리거된 링크 추적 작업의 수입니다.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 205d86b13046bd17e321734904bf57435ef6e106
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 33%

---

# 페이지 이벤트

&#39;페이지 이벤트&#39; [지표](overview.md)은(는) 링크 추적 호출이 수행된 횟수를 보여줍니다. 이 지표는 가장 매력적인 콘텐츠가 있는 페이지를 알려 할 때 유용합니다. 이 지표에 대한 측정은 방문자가 새 페이지로 이동하지 않고 페이지에서 작업을 수행할 수 있을 때 가장 중요합니다.

예를 들어 전자 상거래 사이트의 일반적인 여정에서 방문자는 단일 페이지에서 여러 가지 상호 작용을 할 수 있습니다. 일반적인 Analytics 구현에는 이러한 상호 작용이 링크 추적([`tl()`](/help/implement/vars/functions/tl-method.md)) 호출로 구성된 반면, 페이지 보기([`t()`](/help/implement/vars/functions/t-method.md)) 호출은 초기 페이지 로드용으로 예약되어 있습니다. 이 구현 방법은 방문자가 여정을 계속하기 전에 발생하는 상호 작용에 대한 insight을 제공하는 보강된 이벤트 추적을 제공합니다.

## 이 지표의 계산 방법

이 지표는 보고서 세트의 모든 링크 추적 호출 ([`tl()`](/help/implement/vars/functions/tl-method.md))을 계산합니다. 모든 링크 유형이 이 지표에 포함됩니다. 특히 [사용자 지정 링크](../dimensions/custom-link.md), [다운로드 링크](../dimensions/download-link.md) 및 [종료 링크](../dimensions/exit-link.md)입니다. 페이지 보기 호출([`t()`](/help/implement/vars/functions/t-method.md))은 포함되지 않습니다.

## 유사한 지표와 비교

* **페이지 이벤트와 [페이지 보기 수](page-views.md)**: 페이지 이벤트는 링크 추적 호출([`tl()`](/help/implement/vars/functions/tl-method.md)) 수를 계산하며 페이지 보기 추적 호출([`t()`](/help/implement/vars/functions/t-method.md))을 제외합니다. 페이지 보기는 반대입니다. 페이지 보기 추적 호출의 수를 계산하고 링크를 제외합니다.
