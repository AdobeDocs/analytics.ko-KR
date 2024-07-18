---
description: 다중 통화 지원이 작동하도록 대상 통화 코드를 정의하는 방법을 설명합니다.
title: 다중 통화 지원
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: 99156dd9d898ce0abf214561cb0040c647d7e6ab
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 16%

---

# 다중 통화 지원

Adobe은 조직이 많은 보고서에서 원하는 통화를 달성할 수 있도록 여러 수준의 통화 변환을 제공합니다. 전환은 다음 세 가지 수준으로 수행됩니다.

## 페이지 수준

[`currencyCode`](/help/implement/vars/config-vars/currencycode.md) 변수를 사용하여 각 페이지에서 원하는 통화를 설정할 수 있습니다. 페이지의 통화가 대상 보고서 세트의 통화와 일치하지 않으면 Adobe은 현재 날짜의 환율을 기준으로 보고서 세트의 통화로 통화 변환을 수행합니다. 전환된 통화가 기록됩니다.

## 보고서 세트 수준

모든 보고서 세트에는 **기본 통화**&#x200B;가 있습니다. 이 통화는 모든 통화 지표의 컨텍스트를 나타냅니다(예: [매출](/help/components/metrics/revenue.md)). 저장된 모든 통화 데이터는 보고서 세트의 기본 통화로 표시됩니다.

