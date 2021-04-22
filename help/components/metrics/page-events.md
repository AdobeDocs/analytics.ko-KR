---
title: 페이지 이벤트
description: 트리거된 링크 추적 작업의 수입니다.
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '143'
ht-degree: 100%

---

# 페이지 이벤트

페이지 이벤트 지표는 링크 추적 호출이 수행된 횟수를 보여줍니다. 이 지표는 가장 매력적인 콘텐츠가 있는 페이지를 알려 할 때 유용합니다. 이 지표에 대한 측정은 방문자가 새 페이지로 이동하지 않고 페이지에서 작업을 수행할 수 있을 때 가장 중요합니다.

## 이 지표의 계산 방법

이 지표는 보고서 세트의 모든 링크 추적 호출 ([`tl()`](/help/implement/vars/functions/tl-method.md))을 계산합니다. 모든 링크 유형이 포함됩니다 (사용자 지정 링크, 다운로드 링크 및 종료 링크). 페이지 보기 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md))은 포함되지 않습니다.

## 유사한 지표와 비교

* **페이지 이벤트와 [페이지 보기 수](page-views.md)**: 페이지 이벤트는 링크 추적 호출 (`tl()`)의 수를 계산하며 페이지 보기 추적 호출 (`t()`)은 제외합니다. 페이지 보기는 반대입니다. 페이지 보기 추적 호출의 수를 계산하고 링크를 제외합니다.
