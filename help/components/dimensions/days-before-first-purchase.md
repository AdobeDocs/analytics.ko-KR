---
title: 첫 구매까지 소요된 일 수
description: 방문자의 첫 방문과 첫 번째 구매 사이의 일 수입니다.
translation-type: tm+mt
source-git-commit: a8dc233e962a49674a30ff3c9f0b5d0d45b09f24
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# 첫 구매까지 소요된 일 수

&#39;첫 구매까지 소요된 일 수&#39; 차원은 방문자가 사이트에 처음 도달하고 구매하기까지 경과된 일 수를 보고합니다. 예를 들어 방문자가 처음 방문한 다음 하루 후에 구매를 하는 경우 그 이후의 모든 방문 또는 이벤트는 &quot;1일&quot; 차원 값에 속합니다.

방문자가 처음 구매한 후 방문자의 남은 쿠키 수명 동안 동일한 차원 값에 속합니다.

## 데이터로 이 차원 채우기

Adobe는 구현의 이벤트를 기반으로 이 차원을 자동으로 [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) 채웁니다. 사이트에서 `purchase` 이벤트를 구현하는 경우 이 차원은 항상 작동합니다.

## 차원 값

차원 값에는 방문자가 사이트를 처음 방문하고 첫 번째 구매를 하기 전의 일 수가 포함됩니다. 각 일 수는 방문자의 첫 번째 방문과 첫 번째 구매가 같은 날에 발생한 경우 &quot;같은 날&quot;이 발생하는 별도의 차원 값입니다.
