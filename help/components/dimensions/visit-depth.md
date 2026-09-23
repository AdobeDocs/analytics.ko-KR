---
title: 방문 깊이
description: 방문의 깊이를 보고하는 방문 기반 차원입니다.
feature: Dimensions
exl-id: 3e9aca08-2255-46ca-9949-77334ee7120e
TQID: https://experienceleague.adobe.com/mT5dQzR6edNpvU6Fbf9LlLwQuxW6RA-ZCZJDaIFkyAw
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
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
    internal-label: Marketing Channels
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
source-wordcount: '209'
ht-degree: 68%
---
# 방문 깊이

&#39;방문 깊이&#39; [차원](overview.md)은(는) 방문자가 전체 방문에서 본 페이지 보기 횟수를 보고합니다. 방문 깊이는 히트가 페이지 보기이고 [페이지](page.md) 차원이 마지막 페이지 보기의 차원 항목과 같지 않은 경우에만 증가합니다. 방문 기반 차원이며, 전체 방문 동안 동일한 값을 포함합니다. 이 변수는 방문이 끝난 후 방문의 모든 히트에 대해 설정됩니다.

## 이 차원을 데이터로 채우기

Adobe은 각 방문의 페이지 보기에서 서버측에서 이 차원을 계산합니다. 설정할 변수가 없습니다. 모든 구현에 대해 즉시 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(Adobe에서 계산) |
| **웹 SDK/XDM 필드** | 없음(Adobe에서 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 방문 |

## 차원 항목

차원 항목에는 문자열 `"Pages per visit"`가 포함되며 그 뒤에는 방문에 있는 페이지의 수를 나타내는 숫자가 옵니다. 차원 항목 `"Pages per visit: 1"`은 단일 페이지 방문을 나타내는 반면 차원 항목 `"Pages per visit: 8"`은 8개의 페이지 보기 (및 임의 개수의 링크 추적 호출)가 있는 방문을 나타냅니다.

## 히트 깊이와 비교

차원 간의 비교가 필요하면 [히트 깊이](hit-depth.md)를 참조하십시오.
