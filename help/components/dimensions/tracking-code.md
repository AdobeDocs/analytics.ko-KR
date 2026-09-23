---
title: 추적 코드
description: 추적 코드 또는 캠페인의 이름입니다.
feature: Dimensions
exl-id: e4f70552-6946-4974-a9e2-928faf563ecd
TQID: https://experienceleague.adobe.com/8e9126PxGCNXJqo4a3XYTgXwrcHdf34FVwygpHXm5JI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 88%
---
# 추적 코드

“추적 코드” [차원](overview.md)은 사이트에 있는 추적 코드의 이름을 나열합니다. 인터넷의 서로 다른 위치에 서로 다른 쿼리 문자열 매개변수 값이 있는 링크를 배치할 수 있습니다. 이 차원을 통해 사이트로 트래픽을 유도하는 데 가장 성공적인 링크가 무엇인지 더 잘 이해할 수 있습니다.

추적 코드 쿼리 문자열 추가는 조직에서 사용하는 이메일, 광고, 소셜 미디어 게시물 및 기타 마케팅 활동에서 일반적입니다.

## 이 차원을 데이터로 채우기

AppMeasurement는 [`campaign`](/help/implement/vars/page-vars/campaign.md) 변수를 사용하여 이 데이터를 수집합니다. 조직에서 설정 방법을 정확히 결정하지만 이 변수는 일반적으로 [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md) 유틸리티 메서드를 사용하여 쿼리 문자열에서 값을 가져옵니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`campaign`](/help/implement/vars/page-vars/campaign.md) |
| **웹 SDK/XDM 필드** | [`marketing.trackingCode`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/campaign-marketing-details) |
| **쿼리 매개 변수** | [`v0`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<campaign>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 255바이트 |
| **지속성** | 구성 가능 |

## 차원 항목

차원 항목에는 사이트의 추적 코드 이름이 포함됩니다. 조직은 사용자가 사용하려는 특정 차원 항목을 파악합니다. 자세한 내용은 [캠페인 추적](/help/implement/use-cases/campaign-tracking.md)을 참조하십시오.

## 추적 코드 차원을 추적 코드를 수집하는 마케팅 채널과 비교

마케팅 채널 처리 규칙을 설정하는 일부 사용자는 추적 코드 차원에 사용된 모든 값을 가져오는 규칙을 구성합니다. 이는 훌륭한 방법이지만, 고유한 처리 및 아키텍처 차이로 인해 서로 다릅니다. 이 두 가지 방법이 한눈에 보기엔 비슷하지만, 기여도 동작을 변경할 수 있는 이유를 다음 목록에서 설명합니다.

### 처리 규칙의 이전 채널

목록의 상위에 있는 마케팅 채널 처리 규칙은 히트가 추적 코드 마케팅 채널에 귀속되지 않도록 할 수 있습니다. 예:

1. 소셜 네트워크를 첫 번째 규칙으로 설정하고 추적 코드를 두 번째 규칙으로 설정했습니다.
2. 사용자가 소셜 미디어 사이트에서 추적 코드가 들어 있는 여러분의 사이트에 대한 링크를 게시하고, 여러 친구들이 이 사이트에 대한 해당 링크를 클릭합니다.

소셜 네트워크가 첫 번째 마케팅 채널 처리 규칙이므로 이러한 사용자는 &#39;소셜 네트워크&#39; 마케팅 채널에 귀속되고 추적 코드 마케팅 채널에는 귀속되지 않습니다.

### 다른 마케팅 채널은 마지막 터치를 통해 속성을 가져올 수 있음

표준 추적 코드 차원을 처리할 때에는 사이트의 다른 부분이 기여도를 가로채는 것에 대해 걱정하지 않아도 됩니다. 그러나 마케팅 채널을 사용하면 사용자가 다른 규칙을 일치시켜 다른 속성을 제공할 수 있습니다. 예:

1. 첫 번째 채널로 &#39;추적 코드&#39;를 사용하고 두 번째 채널로 &#39;직접&#39;을 사용하고 있습니다.
2. 사용자가 처음에는 추적 코드를 통해 사이트에 도착하지만 이후 사이트를 나갑니다.
3. 다음날, 주소 표시줄에 URL을 입력한 다음 구입합니다.

이 예제에서는 추적 코드 마케팅 채널은 해당 구매에 대한 마지막 터치 크레딧을 받지 않습니다. 대신 “직접” 마케팅 채널로 이동합니다.


### 만료 차이

채널을 터치했는지 여부에 상관없이 마케팅 채널에는 연속 30일 방문자 참여 만료가 적용됩니다. 추적 코드는 변수가 설정된 시점을 기준으로 만료됩니다. 예:

1. 방문자 참여도 만료가 30일이며 추적 코드 차원도 30일 후에 만료되도록 구성했습니다.
2. 사용자가 추적 코드를 통해 사이트에 도달합니다. 그리고 사이트를 탐색한 다음 떠납니다.
3. 3주 후, 추적 코드나 마케팅 채널 없이 돌아왔다가 다시 떠납니다.
4. 다른 2주 후 (첫 방문 후 5주), 추적 코드나 마케팅 채널 없이 돌아왔다가 구매합니다.

사용자는 결국 30일 이상 지나서 구매했지만 30일 이상 동안 활동이 없는 상태는 아니었습니다. 이 경우, 수익은 추적 코드 마케팅 채널에 귀속되지만 추적 코드 차원 자체에는 귀속되지 않습니다.



