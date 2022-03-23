---
title: 대량 데이터 삽입 API
description: 대량 데이터 삽입 API(BDIA)는 AppMeasurement와 같은 클라이언트측 라이브러리를 사용하지 않고 서버 호출 데이터를 파일 배치에 업로드할 수 있는 Adobe Analytics 기능입니다. 이러한 배치 파일의 서버 호출은 현재(라이브) 데이터 또는 내역 데이터일 수 있습니다. 이는 이전 버전의 Adobe Analytics API보다 확장성이 훨씬 좋은 대량 데이터 삽입 API의 연계 버전입니다.
solution: Analytics
feature: API
exl-id: c9d23fae-2800-42bb-8f8d-adf915cadc62
source-git-commit: b1ebf6e3548ef73217ffff1cbfb66af82e38fb8f
workflow-type: ht
source-wordcount: '231'
ht-degree: 100%

---

# 대량 데이터 삽입 API

대량 데이터 삽입은 다음과 같은 몇몇 사용 사례를 해결합니다.

* 이전 분석 시스템에서의 내역 데이터 수집

* AppMeasurement 사용을 어렵게 하는 내부 분석 수집 시스템 추출-변환-로드(ETL) 프로세스를 사용하여 데이터를 배치 파일로 가져온 다음 BDIA를 사용하여 가져온 데이터를 Adobe Analytics에 업로드할 수 있습니다.

* 인터넷 연결이 간헐적으로 끊어지는 디바이스에서의 데이터 수집 이러한 디바이스는 연결을 수신할 때까지 상호 작용을 보관합니다. 그런 다음 BDIA를 통해 모든 데이터를 한 번에 업로드할 수 있습니다.

데이터 삽입 API 및 [대량 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)는 모두 서버측 수집 데이터를 Adobe Analytics에 제출하는 방법입니다. 데이터 삽입 API 호출은 한 번에 하나의 이벤트로 수행됩니다. 대량 데이터 삽입 API는 한 행에 한 이벤트씩, 이벤트 데이터를 포함하는 CSV 형식의 파일을 수락합니다. 새로운 서버측 컬렉션 구현 작업을 수행하는 경우에는 대량 데이터 삽입 API를 사용하는 것이 좋습니다.
