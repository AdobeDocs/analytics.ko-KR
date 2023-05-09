---
title: 보트 발생 횟수
description: 보트 규칙과 일치하는 히트의 수입니다.
exl-id: 3b6cbe94-98db-4ba4-aab2-ce59cdbc420a
hide: true
hidefromtoc: true
source-git-commit: 017559d2b909deb4bf87fb5fe41db8250f2ca2ac
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 보트 발생 횟수

보트 발생 횟수 지표는 일치하는 히트의 수를 보여줍니다 [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

보트 보고는 나머지 보고서 세트 데이터와 구분되므로 이 지표는 다음 차원에서만 작동합니다.

* [보트 이름](../dimensions/bot-name.md)
* [페이지](../dimensions/page.md)
* 시간 기반 차원(예: [일](../dimensions/day.md), [주](../dimensions/week.md), 또는 [월](../dimensions/month.md))

이 지표와 함께 다른 차원을 사용하면 데이터가 반환되지 않습니다.

## 이 지표의 계산 방법

Adobe은 모든 히트를 확인하여 조직이 구성한 보트 규칙과 일치하는지 확인합니다. 주어진 히트가 보트 규칙과 일치하는 경우 히트가 보고에서 제외되고 이 지표가 1씩 증가합니다. 이 지표에는 두 페이지 보기([`t()`](/help/implement/vars/functions/t-method.md)) 및 링크 추적 히트( )[`tl()`](/help/implement/vars/functions/tl-method.md)) [보트 페이지 보기](bot-page-views.md) 링크 추적 히트는 포함하지 마십시오.