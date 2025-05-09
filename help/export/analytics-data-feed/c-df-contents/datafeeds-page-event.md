---
description: 테이블을 조회하여 페이지 이벤트를 기반으로 히트의 유형을 파악합니다.
keywords: 페이지;이벤트;page_event;post_page_event
title: 페이지 이벤트 조회
feature: Data Feeds
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
source-git-commit: e16b0d7b3fe585dc8e9274a77833ad5af3c63124
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 4%

---

# 페이지 이벤트 조회

테이블을 조회하여 `page_event` 값을 기준으로 히트의 유형을 확인합니다. [데이터 열 참조](datafeeds-reference.md)에 언급된 대로 `page_event` 및 `post_page_event` 열은 tinyint 부호 없습니다.

* AppMeasurement 및 웹 SDK에 대한 페이지 보기 호출 구현을 이해하려면 [`t()`](/help/implement/vars/functions/t-method.md)을(를) 참조하십시오.
* AppMeasurement 및 웹 SDK에 대한 링크 추적 호출 구현에 대해 이해하려면 [`tl()`](/help/implement/vars/functions/tl-method.md)을(를) 참조하십시오.
* Adobe Analytics에서 XDM 페이로드를 페이지 이벤트 유형으로 변환하는 방법에 대해 알아보려면 [Adobe Experience Platform Edge Network을 사용하여 Adobe Analytics 구현](/help/implement/aep-edge/overview.md)을 참조하십시오.

| `page_event` 값 | `post_page_event` 값 | 설명 |
| --- | --- | --- |
| `0` | `0` | 모든 표준 페이지 보기 호출. 대부분의 히트에 대한 기본값입니다. |
| `10` | `100` | 사용자 지정 링크. 링크 형식을 `o`(AppMeasurement) 또는 `xdm.web.webInteraction.type`을(를) `other`(웹 SDK 또는 모바일 SDK)로 설정합니다. |
| `11` | `101` | 다운로드 링크. 링크 형식을 `d`(AppMeasurement) 또는 `xdm.web.webInteraction.type`을(를) `download`(웹 SDK 또는 모바일 SDK)로 설정합니다. |
| `12` | `102` | 종료 링크. 링크 형식을 `e`(AppMeasurement) 또는 `xdm.web.webInteraction.type`을(를) `exit`(웹 SDK 또는 모바일 SDK)로 설정합니다. |
| `31` | `76` | 미디어 시작 |
| `32` | `77` | 미디어 업데이트(다른 변수 처리 안 함) |
| `33` | `78` | 미디어 업데이트(다른 변수 처리 시) |
| `40` | `80` | 설문 조사 |
| `50` | `50` | 스트리밍 미디어 시작 |
| `51` | `51` | 스트리밍 미디어 닫기 |
| `52` | `52` | 스트리밍 미디어 스크러빙 |
| `53` | `53` | 스트리밍 미디어 작동 유지 |
| `54` | `54` | 스트리밍 미디어 광고 시작 |
| `55` | `55` | Streaming Media 광고 닫기 |
| `56` | `56` | 스트리밍 미디어 광고 스크러빙 |
| `60` | `60` | Primetime 미디어 시작 |
| `61` | `61` | Primetime 미디어 닫기 |
| `62` | `62` | Primetime 미디어 삭제 |
| `63` | `63` | Primetime 미디어 작동 중지 |
| `64` | `64` | Primetime 미디어 광고 시작 |
| `65` | `65` | Primetime 미디어 광고 닫기 |
| `66` | `66` | Primetime 미디어 광고 삭제 |
| `70` | `70` | Target 활동 데이터 포함 |
