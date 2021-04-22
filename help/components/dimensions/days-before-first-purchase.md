---
title: 첫 구매까지 소요된 일 수
description: 방문자의 첫 방문과 첫 번째 구매 사이의 일 수입니다.
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# 첫 구매까지 소요된 일 수

첫 구매까지 소요된 일 수 차원은 방문자가 처음 사이트에 도달하고 구매하기까지 경과되는 일 수를 보고합니다. 예를 들어 방문자가 처음 방문한 다음 하루 후에 구매한다면 그 이후의 모든 방문 또는 이벤트는 &quot;1일&quot; 차원 항목에 속합니다.

방문자는 처음 구매한 후 방문자의 남은 쿠키 수명 동안 동일한 차원 항목에 속합니다.

## 이 차원을 데이터로 채우기

Adobe에서는 구현의 [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) 이벤트를 기반으로 이 차원을 자동으로 채웁니다. 사이트에서 `purchase` 이벤트를 구현하는 경우 이 차원이 항상 작동합니다.

## 차원 항목

차원 항목에는 사이트에 대한 방문자의 첫 방문과 첫 번째 구매 사이의 일 수가 포함됩니다. 각 일 수는 방문자의 첫 번째 방문과 첫 번째 구매가 같은 날에 발생한 경우 &quot;같은 날&quot;이 발생하는 별도의 차원 항목입니다.
