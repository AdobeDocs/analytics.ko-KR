---
title: 마지막 구매 이후 일 수
description: 현재 히트와 마지막으로 구매한 기간 사이의 일 수입니다.
translation-type: tm+mt
source-git-commit: c9e696201d0e9ec97dcdd6ff797ca72244dcf366
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# 마지막 구매 이후 일 수

&#39;마지막 구매 이후 일 수&#39; 차원은 방문자의 현재 히트와 해당 시간의 가장 최근 구매 간 경과된 시간을 측정합니다. 이 차원은 방문자가 사이트에서 항목을 구매한 후 만든 행동을 이해하는 데 도움이 됩니다.

구매한 적이 없는 방문자는 이 차원에 포함되지 않습니다. 또한 방문자의 첫 구매 전에 실행된 히트도 포함되지 않습니다. 방문자의 첫 구매 후에만 히트가 포함됩니다.

## 데이터로 이 차원 채우기

Adobe는 구현의 이벤트를 기반으로 이 차원을 자동으로 [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) 채웁니다. 사이트에서 `purchase` 이벤트를 구현하는 경우 이 차원은 항상 작동합니다.

## 차원 값

차원 값에는 방문자의 최근 구매와 현재 히트 사이의 일 수가 포함됩니다. 각 일 수는 방문자의 최근 구매와 현재 히트가 같은 날에 발생한 경우 &quot;같은 날&quot;이 발생하는 별도의 차원 값입니다.
