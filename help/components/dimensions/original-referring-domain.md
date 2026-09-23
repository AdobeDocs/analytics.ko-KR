---
title: 최초 참조 도메인
description: 방문자가 사이트를 클릭스루하기 전에 있었던 첫 번째 참조 도메인입니다.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
TQID: https://experienceleague.adobe.com/G-se6LH33gMTt8ttrP5RBzL85m335ujtbiSm6EjLGuU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
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
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 72%
---
# 최초 참조 도메인

&#39;원래 참조 도메인&#39; [차원](overview.md)은(는) 방문자가 사이트에 도달하기 위해 클릭했던 첫 번째 참조 도메인을 보고합니다. 설정되면 해당 방문자 ID의 전체 라이프타임 동안 동일한 값을 포함합니다. 이 차원은 처음에 사이트로 트래픽을 유도하는 서드파티 사이트를 아는 데 유용합니다.

>[!IMPORTANT]
>
>이 차원을 사용하려면 보고서 세트의 [내부 URL 필터](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 도메인이 포함되거나 외부 도메인이 표시되지 않을 수 있습니다.

## 이 차원을 데이터로 채우기

Adobe은 방문자의 첫 번째 [레퍼러](referrer.md)에서 해당 레퍼러 URL의 도메인 부분을 사용하여 이 차원을 파생합니다. 설정할 변수가 없습니다. 보고서 세트의 [내부 URL 필터](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)를 구성해야 합니다. 구성하지 않으면 내부 도메인이 포함되거나 외부 도메인이 표시되지 않을 수 있습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(방문자의 첫 번째 레퍼러에서 파생) |
| **웹 SDK/XDM 필드** | 없음(방문자의 첫 번째 레퍼러에서 파생) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 방문자 |

방문자가 언제든지 나가서 다른 도메인의 링크를 클릭하는 경우 새 값이 기록되지 않습니다. 새 값을 보려면 [참조 도메인](referring-domain.md)을 참조하세요.

## 차원 항목

차원 항목에는 방문자가 사이트에 도달하기 위해 클릭한 도메인이 포함됩니다. 히트에 (설정되었거나 유지된) 레퍼러 데이터가 없으면 이 히트는 차원 항목 `"None"` 아래에 그룹화됩니다. 이 차원 항목은 방문자가 수동으로 브라우저 주소를 주소 표시줄에 입력하거나 책갈피를 클릭하는 등의 경우와 같이 레퍼러 값이 없음을 의미합니다.

## 참조 도메인과 최초 참조 도메인 비교

참조 도메인은 방문에 따라 달라질 수 있습니다. 예를 들어 방문자가 `google.com`을 통해 사용자의 사이트로 도착하고 1주일 후 `twitter.com`을 통해 사용자의 사이트에 도착합니다. 결국 이 방문자는 사용자의 사이트에서 구매를 합니다. 참조 도메인을 마지막 터치 속성이 있는 차원으로 사용하는 경우 `twitter.com`이 구매에 대한 크레딧을 받습니다. 최초 참조 도메인을 차원으로 사용하는 경우 속성 모델에 관계없이 `google.com`이 구매에 대한 크레딧을 받습니다.

최초 참조 도메인은 주어진 방문자 ID의 전체 라이프타임 동안 변경되지 않습니다.
