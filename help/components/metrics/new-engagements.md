---
title: 새 참여 횟수
description: 첫 번째 터치 채널이 설정되는 횟수입니다.
feature: Metrics
exl-id: a419d048-9715-4d7b-9c24-d34129755371
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: ht
source-wordcount: '148'
ht-degree: 100%

---

# 새 참여 횟수

새 참여 지표는 방문자가 참여하는 기간에 처음으로 마케팅 채널과 일치하는 횟수를 보여줍니다. 이 지표는 마케팅 채널 처리 규칙과 처음 일치하는 방문자와 차원을 비교하려는 경우 유용합니다.

## 이 지표의 계산 방법

데이터 처리 중, 모든 히트는 [마케팅 채널 처리 규칙](../c-marketing-channels/c-rules.md)을 통해 실행됩니다. 히트가 마케팅 채널 처리 규칙을 만족하고 방문자에게 아직 첫 번째 터치 채널이 없다면 히트는 새 참여입니다. 히트가 마케팅 채널 처리 규칙을 만족하지 않거나 방문자에게 이미 첫 번째 터치 채널이 있다면 히트는 새 참여가 아닙니다.

방문자가 자신의 방문자 참여 기간이 만료되도록 두는 경우 두 개 이상의 새 참여를 가질 수 있습니다.
