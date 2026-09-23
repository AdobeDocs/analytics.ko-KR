---
title: 영구적 쿠키 지원
description: 방문자가 영구 쿠키를 지원할 수 있는지 확인합니다.
feature: Dimensions
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
TQID: https://experienceleague.adobe.com/QmbTee9NoWeTmiRdFI3p24idNhzEzK66xb5RY-KKnQ4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
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
source-wordcount: '243'
ht-degree: 67%
---
# 영구적 쿠키 지원

&#39;영구 쿠키 지원&#39; [차원](overview.md)은 히트가 영구 소스에서 가져온 방문자 식별자를 사용했는지 여부를 보여 줍니다. 가장 일반적인 영구 소스는 쿠키이지만 모바일 헤더 및 기타 소스도 사용할 수 있습니다.

## 이 차원을 데이터로 채우기

Adobe은 히트의 방문자 식별자가 일반적으로 영구적인 소스(예: 쿠키)에서 유래되었는지 여부에 따라 이 차원 서버측을 결정합니다. 설정할 변수가 없으며 모든 구현에 대해 즉시 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(파생 서버측) |
| **웹 SDK/XDM 필드** | 없음(파생 서버측) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

* **`Enabled`**: 히트의 방문자 식별자가 일반적으로 영구적인 소스에서 가져온 것입니다. 가장 일반적인 예로는 `aid`, `fid` 또는 `mid` 쿼리 문자열 매개 변수가 있습니다. 이들 매개 변수는 쿠키에서 값을 가져오기 때문입니다.
* **`Disabled`**: 히트의 방문자 식별자가 Adobe가 영구적으로 인식하지 못하는 소스에서 가져온 것입니다(예: IP + 사용자 에이전트 문자열). 이 차원 항목에는 [`visitorID`](/help/implement/vars/config-vars/visitorid.md) 변수를 사용하는 사용자 지정 방문자 ID도 포함됩니다.

## “쿠키 지원”과 “영구적 쿠키 지원”의 차이점

* **쿠키 지원**: AppMeasurement는 일반 쿠키를 설정하려고 합니다. 차원 항목은 쿠키가 성공적으로 설정되었는지 여부를 기반으로 합니다.
* **영구적 쿠키 지원**: 차원 항목은 쿠키와 같은 영구적 소스에서 히트의 식별자를 가져왔는지 여부를 기반으로 합니다.
