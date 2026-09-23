---
title: 종료 링크
description: 종료 링크의 이름입니다.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
TQID: https://experienceleague.adobe.com/lGKBkR5e2arJxGmfIE4qN84oGtYJ2zkfn6luqxEUJ-w
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 22%
---
# 종료 링크

&#39;종료 링크&#39; [차원](overview.md)은(는) 사이트에 구현된 종료 링크의 이름을 보고합니다. 종료 링크는 방문자를 현재 도메인에서 멀리 이동하는 아웃바운드 클릭을 추적합니다. 이 차원은 가장 자주 클릭하는 아웃바운드 링크를 이해하려 할 때 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 [링크 추적 호출(`tl()`)](/help/implement/vars/functions/tl-method.md)로 채워집니다. 설정할 전용 변수가 없습니다. 대신 링크 형식 인수가 `"e"`인 `tl()` 이미지 요청을 보내고 링크 이름 인수를 원하는 값으로 설정하십시오. `pe` 쿼리 문자열은 링크 이름을 올바른 링크 차원으로 라우팅합니다([사용자 지정 링크](custom-link.md)의 경우 `lnk_o`, [다운로드 링크](download-link.md)의 경우 `lnk_d`, [종료 링크](exit-link.md)의 경우 `lnk_e`). 링크 이름이 제공되지 않으면 링크 URL이 차원 값으로 대신 사용되며 URL에서 파생된 값은 바이트 제한의 적용을 받지 않습니다.

```js
s.tl(true,"e","Example exit link");
```

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`tl()`](/help/implement/vars/functions/tl-method.md) |
| **웹 SDK/XDM 필드** | 없음 |
| **쿼리 매개 변수** | [`pev2`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<linkName>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 100바이트 |
| **지속성** | 히트 |

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다. 링크 이름이 제공되지 않으면 차원 항목이 원시 URL로 대신 표시됩니다. 이러한 원시 URL은 보고서에서 해석하기가 더 어려우므로 가능한 한 수사적 링크 이름을 제공합니다.
