---
title: 히트 깊이
description: 방문의 히트 수입니다.
feature: Dimensions
exl-id: 84c27e3f-4228-4455-95bf-0239928337b5
TQID: https://experienceleague.adobe.com/dH1ItdXZTw9vcqvej3VOQDM-J9FFA38f4bq8HTJbKMo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
    internal-label: Functions
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 63%
---
# 히트 깊이

&#39;히트 깊이&#39; [차원](overview.md)은(는) 주어진 히트가 방문까지 얼마나 진행되었는지 보고합니다. 이 차원은 방문자가 사이트에서 작업을 수행하는 시점이 방문 중 어느 정도인지 이해하는 데 유용합니다. 히트 깊이는 페이지 보기([`t()`](/help/implement/vars/functions/t-method.md))와 링크 추적 히트([`tl()`](/help/implement/vars/functions/tl-method.md))를 포함하여 모든 유형의 히트를 계산합니다.

## 이 차원을 데이터로 채우기

Adobe은 각 방문의 히트 시퀀스로부터 이 차원 서버측을 계산합니다. 설정할 변수가 없습니다. 모든 구현에 대해 즉시 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(Adobe에서 계산) |
| **웹 SDK/XDM 필드** | 없음(Adobe에서 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 문자열 `"Hit Depth"`가 포함되며 그 뒤에는 방문까지의 히트 수를 나타내는 숫자가 옵니다. `"Hit Depth 1"`이라는 차원 항목은 방문의 첫 번째 히트를 나타내고 차원 항목 `"Hit Depth 8"`은 방문의 8번째 히트를 나타냅니다.

>[!NOTE]
>
>Adobe Analytics은 두 번째 수준 정밀도에서만 타임스탬프를 기록합니다. 동일한 타임스탬프를 두 번째로 공유하는 히트의 경우 Adobe은 보고에 반영된 순서가 히트가 발생한 순서와 동일하다고 보장할 수 없습니다. 밀리초 수준의 정밀도가 조직의 우선 순위인 경우 Customer Journey Analytics 사용을 고려해 보십시오.

## 방문 깊이와 비교

히트 깊이는 페이지 조회수와 링크 추적 히트를 포함하여 모든 유형의 히트를 계산합니다. 방문 깊이는 페이지 보기 히트에 대해서만 증가&#x200B;_하며_ [페이지](page.md) 차원 항목은 이전 페이지의 값과 동일하지 않습니다. 방문 깊이는 또한 방문 기반 차원이므로 방문의 모든 히트에서 값이 동일합니다. 다음 테이블에서는 방문 예와 이 방문에서 히트 깊이 + 방문 깊이가 어떻게 고려되는지 설명합니다.

| 페이지 시퀀스 | 히트 깊이 | 방문 깊이에 포함됩니까? | 방문 깊이 |
| --- | --- | --- | --- |
| 홈 페이지 | 1 | 예 | 4 |
| 제품 페이지 | 2 | 예 | 4 |
| 홈 페이지 | 3 | 예 | 4 |
| 사용자 지정 링크 클릭 | 4 | 아니요 (사용자 지정 링크) | 4 |
| 사용자 지정 링크 클릭 | 5 | 아니요 (사용자 지정 링크) | 4 |
| 제품 페이지 | 6 | 예 | 4 |
| 사용자 지정 링크 클릭 | 7 | 아니요 (사용자 지정 링크) | 4 |
| 제품 페이지 | 8 | 아니요 (이전 페이지와 동일) | 4 |
