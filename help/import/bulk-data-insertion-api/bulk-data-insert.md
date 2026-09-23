---
title: 대량 데이터 삽입 API
description: 대량 데이터 삽입 API(BDIA)는 AppMeasurement과 같은 클라이언트측 라이브러리를 사용하지 않고 서버 호출 데이터를 파일 배치에 업로드할 수 있는 Adobe Analytics 기능입니다.
solution: Analytics
feature: API
exl-id: c9d23fae-2800-42bb-8f8d-adf915cadc62
role: Admin
TQID: 'https://experienceleague.adobe.com/TVa-LtTWKi6lQKGQKhH2bu5UcKsSJ2-KVqlfU5tQROQ'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: f46a60da-b0b2-4ca3-bd91-271173f4123d
    internal-label: Data sources
role_v2:
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
source-wordcount: '228'
ht-degree: 53%
---
# 대량 데이터 삽입 API

대량 데이터 삽입은 다음과 같은 몇몇 사용 사례를 해결합니다.

* 이전 분석 시스템에서의 내역 데이터 수집

* AppMeasurement 사용을 어렵게 하는 내부 분석 수집 시스템 추출-변환-로드(ETL) 프로세스를 사용하여 데이터를 배치 파일로 가져온 다음 BDIA를 사용하여 가져온 데이터를 Adobe Analytics에 업로드할 수 있습니다.

* 인터넷 연결이 간헐적으로 끊어지는 디바이스에서의 데이터 수집 이러한 디바이스는 연결을 수신할 때까지 상호 작용을 보관합니다. 그런 다음 BDIA를 통해 모든 데이터를 한 번에 업로드할 수 있습니다.

Data Insertion API 및 [Bulk Data Insertion API](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/)는 모두 서버측 컬렉션 데이터를 Adobe Analytics에 제출하는 방법입니다. 데이터 삽입 API 호출은 한 번에 하나의 이벤트씩 수행됩니다. 대량 데이터 삽입 API는 한 행에 한 이벤트씩, 이벤트 데이터를 포함하는 CSV 형식의 파일을 수락합니다. 새로운 서버측 컬렉션 구현 작업을 수행하는 경우에는 대량 데이터 삽입 API를 사용하는 것이 좋습니다.

인증, 끝점, 파일 형식, 열 참조 및 문제 해결에 대해서는 Adobe Developer에서 [대량 데이터 삽입 API](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/) 설명서를 참조하십시오.
