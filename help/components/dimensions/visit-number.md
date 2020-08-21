---
title: 방문 횟수
description: 방문자의 n번째 방문입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 59%

---


# 방문 횟수

방문 번호 차원은 현재 방문자가 있는 방문이 어느 것인지 보고합니다. 새 방문이 시작되면 이 차원 항목이 1씩 증가합니다. 이 차원은 사이트로 돌아올 때 방문자의 참여도를 이해하려 할 때 유용합니다. 방문 기반 차원으로서, 전체 방문에 대해 동일한 값을 포함하고 변경할 수 없음을 의미합니다. 프로젝트 날짜 범위와 상관없이 방문자의 라이프타임에 적용됩니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

Dimension items include the string `"Visit number"` followed by the numeric representation of the visit the visitor is currently on. For example, if the visitor has never been to your site before, their first visit belongs to the dimension item `"Visit number 1"`. If this is the visitor&#39;s 13th visit to your site, they belong to the dimension item `"Visit number 13"`.
