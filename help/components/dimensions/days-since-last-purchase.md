---
title: 마지막 구매 이후 일 수
description: 현재 히트와 마지막 구매 사이의 일 수입니다.
exl-id: 6f0d9d79-cf40-4de3-9d9f-9b1bc57f97b6
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# 마지막 구매 이후 일 수

마지막 구매 이후 일 수 차원은 방문자의 현재 히트와 그 당시 가장 최근 구매 사이에 경과된 시간의 크기를 측정합니다. 이 차원은 방문자가 사용자의 사이트에서 구매를 한 후 취하는 동작을 이해하는 데 도움이 됩니다.

구매한 적이 없는 방문자는 이 차원에 포함되지 않습니다. 또한 방문자의 첫 구매 전에 실행된 히트도 포함되지 않습니다. 방문자의 첫 구매 후 히트만 포함됩니다.

## 이 차원을 데이터로 채우기

Adobe에서는 구현의 [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) 이벤트를 기반으로 이 차원을 자동으로 채웁니다. 사이트에서 `purchase` 이벤트를 구현하는 경우 이 차원이 항상 작동합니다.

## 차원 항목

차원 항목에는 방문자의 가장 최근 구매와 현재 히트 사이의 일 수가 포함됩니다. 각 일 수는 방문자의 가장 최근 구매와 현재 히트가 같은 날 발생한 경우 &quot;같은 날&quot; 발생하는 별도의 차원 항목입니다.
