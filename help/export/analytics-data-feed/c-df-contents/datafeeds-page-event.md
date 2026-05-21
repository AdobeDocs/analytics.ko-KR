---
description: 테이블을 조회하여 페이지 이벤트를 기준으로 히트의 유형을 파악합니다.
keywords: page;event;page_event;post_page_event
title: 페이지 이벤트 조회
feature: Data Feeds
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
TQID: https://experienceleague.adobe.com/QAGYKNnpMl2tM6BRux7BBL-YFpMTgUIXsHT-9bGKWnA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 100%

---

# 페이지 이벤트 조회

테이블을 조회하여 `page_event` 값을 기준으로 히트의 유형을 파악합니다. [데이터 열 참조](datafeeds-reference.md)에 언급된 바와 같이 `page_event` 및 `post_page_event` 열은 tinyint 부호가 없습니다.

* AppMeasurement 및 웹 SDK에 대한 페이지 조회수 호출 구현을 이해하려면 [`t()`](/help/implement/vars/functions/t-method.md)를 참조하십시오.
* AppMeasurement 및 웹 SDK에 대한 링크 추적 호출 구현에 대해 이해하려면 [`tl()`](/help/implement/vars/functions/tl-method.md)를 참조하십시오.
* [Adobe Experience Platform Edge Network를 사용하여 Adobe Analytics 구현](/help/implement/aep-edge/overview.md)을 참조하여 Adobe Analytics가 XDM 페이로드를 페이지 이벤트 유형으로 변환하는 방법을 이해합니다.

| `page_event` 값 | `post_page_event` 값 | 설명 |
| --- | --- | --- |
| `0` | `0` | 모든 표준 페이지 조회수 호출. 대부분의 히트에 대한 기본값입니다. |
| `10` | `100` | 사용자 정의 링크. 링크 유형을 `o`(AppMeasurement) 또는 `xdm.web.webInteraction.type`을 `other`(웹 SDK 또는 모바일 SDK)로 설정합니다. |
| `11` | `101` | 링크를 다운로드합니다. 링크 유형을 `d`(AppMeasurement) 또는 `xdm.web.webInteraction.type`을 `download`(웹 SDK 또는 모바일 SDK)로 설정합니다. |
| `12` | `102` | 링크를 종료합니다. 링크 유형을 `e`(AppMeasurement) 또는 `xdm.web.webInteraction.type`을 `exit`(웹 SDK 또는 모바일 SDK)로 설정합니다. |
| `31` | `76` | 미디어 시작 |
| `32` | `77` | 미디어 업데이트(다른 변수 처리 포함 안됨) |
| `33` | `78` | 미디어 업데이트(다른 변수 처리 포함) |
| `40` | `80` | 설문 조사 |
| `50` | `50` | 스트리밍 미디어 시작 |
| `51` | `51` | 스트리밍 미디어 닫기 |
| `52` | `52` | 스트리밍 미디어 스크러빙 |
| `53` | `53` | 스트리밍 미디어 keep alive |
| `54` | `54` | 스트리밍 미디어 광고 시작 |
| `55` | `55` | 스트리밍 미디어 광고 닫기 |
| `56` | `56` | 스트리밍 미디어 광고 스크러빙 |
| `60` | `60` | Primetime 미디어 시작 |
| `61` | `61` | Primetime 미디어 닫기 |
| `62` | `62` | Primetime 미디어 스크러빙 |
| `63` | `63` | Primetime 미디어 keep alive |
| `64` | `64` | Primetime 미디어 광고 시작 |
| `65` | `65` | Primetime 미디어 광고 닫기 |
| `66` | `66` | Primetime 미디어 광고 스크러빙 |
| `70` | `70` | Target 활동 데이터 포함 |
