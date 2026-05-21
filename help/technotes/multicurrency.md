---
description: 다중 통화 지원이 작동하도록 대상 통화 코드를 정의하는 방법을 설명합니다.
title: 다중 통화 지원
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
TQID: https://experienceleague.adobe.com/-t0JAIvbmUmzTCTznOWcjVmvtJbmQNV5MIrbQBvhv6M
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 18%

---

# 다중 통화 지원

Adobe에서는 조직이 많은 보고서에서 원하는 통화를 달성할 수 있도록 여러 수준의 통화 변환을 제공합니다. 전환은 다음 세 가지 수준으로 수행됩니다.

## 페이지 수준

[`currencyCode`](/help/implement/vars/config-vars/currencycode.md) 변수를 사용하여 각 페이지에서 원하는 통화를 설정할 수 있습니다. 페이지의 통화가 대상 보고서 세트의 통화와 일치하지 않으면 Adobe은 현재 날짜의 환율을 기준으로 보고서 세트의 통화로 통화 변환을 수행합니다. 전환된 통화가 기록됩니다.

## 보고서 세트 수준

모든 보고서 세트에는 **기본 통화**&#x200B;가 있습니다. 이 통화는 모든 통화 지표의 컨텍스트를 나타냅니다(예: [매출](/help/components/metrics/revenue.md)). 저장된 모든 통화 데이터는 보고서 세트의 기본 통화로 표시됩니다.

