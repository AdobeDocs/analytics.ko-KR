---
description: 다중 통화 지원이 작동하도록 대상 통화 코드를 정의하는 방법을 설명합니다.
title: 다중 통화 지원
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: f659d1bde361550928528c7f2a70531e3ac88047
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 10%

---

# 다중 통화 지원

Adobe은 조직이 많은 보고서에서 원하는 통화를 달성할 수 있도록 여러 수준의 통화 전환을 제공합니다. 다음과 같은 세 가지 수준에서 전환이 발생합니다.

## 페이지 수준

를 사용할 수 있습니다 [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) 변수를 사용하여 각 페이지에서 원하는 통화를 설정할 수 있습니다. 페이지의 통화가 대상 보고서 세트의 통화와 일치하지 않으면 Adobe이 현재 날짜의 환율을 기준으로 보고서 세트의 통화로 통화 변환을 수행합니다. 변환된 통화가 기록됩니다.

## 보고서 세트 수준

모든 보고서 세트에는 **기본 통화**. 이 통화는 모든 통화 지표의 컨텍스트(예: [매출](/help/components/metrics/revenue.md)). 저장된 모든 통화 데이터는 보고서 세트의 기본 통화로 표시됩니다.

## 사용자 수준

Reports &amp; Analytics의 경우 사용자는 아래의 보고서 세트의 기본 통화와 다른 통화를 설정할 수 있습니다 [보고서 설정](/help/analyze/reports-analytics/report-settings.md). 이 설정은 원본에 영향을 주지 않으므로 원본에 영향을 주지 않습니다. 대신, 기본 통화 전환을 오늘의 환율을 기준으로 본 모든 보고서에 적용합니다. 다른 날짜에 동일한 보고서를 보는 경우 다른 일별 환율로 인해 숫자가 변경될 수 있습니다.

Analysis Workspace은 현재 사용자 수준 통화 변환을 제공하지 않습니다.
