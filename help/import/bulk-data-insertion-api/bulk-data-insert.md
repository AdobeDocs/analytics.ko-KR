---
title: 대량 데이터 삽입 API
description: BDIA(Bulk Data Insertion API)는 AppMeasurement와 같은 클라이언트 측 라이브러리를 사용하는 대신 파일 배치(batch)로 서버 호출 데이터를 업로드할 수 있는 Adobe Analytics 기능입니다. 이러한 배치 파일의 서버 호출은 현재(라이브) 데이터 또는 이전 데이터일 수 있습니다. 이전 버전의 Adobe Analytics API에서 데이터 삽입 API를 확장적으로 이어줍니다.
solution: Analytics
feature: API
source-git-commit: d8603ddd6cee2ccc930281003d9ff1befa15c95c
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 27%

---


# 대량 데이터 삽입 API

대량 데이터 삽입은 다음과 같은 몇 가지 사용 사례를 해결합니다.

* 이전 분석 시스템에서 이전 데이터 수집

* AppMeasurement를 사용할 수 없도록 하는 내부 분석 수집 시스템입니다. ETL(Extract-Transform-Load) 프로세스를 사용하여 데이터를 배치 파일에 입력한 다음 BDIA를 사용하여 Adobe Analytics에 업로드할 수 있습니다.

* 인터넷에 간헐적인 연결만 있는 장치에서 데이터를 수집합니다. 이러한 장치는 연결을 받을 때까지 상호 작용을 저장합니다. 그런 다음 장치가 BDIA를 통해 데이터를 한 번에 모두 업로드할 수 있습니다.

데이터 삽입 API 및 [대량 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)두 방법 모두 서버측 수집 데이터를 Adobe Analytics에 제출하는 방법입니다. 데이터 삽입 API 호출은 한 번에 하나의 이벤트로 수행됩니다. 대량 데이터 삽입 API는 한 행에 한 이벤트씩, 이벤트 데이터를 포함하는 CSV 형식의 파일을 수락합니다. 새로운 서버측 컬렉션 구현 작업을 수행하는 경우에는 대량 데이터 삽입 API를 사용하는 것이 좋습니다.