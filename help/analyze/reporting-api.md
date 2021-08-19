---
description: 보고 API에 대한 리소스 및 링크입니다.
title: Analytics Reporting API
uuid: 68ec3490-6e47-4606-860d-dd5e89c574a1
feature: API
role: Developer
exl-id: 003a8b83-6ef0-4313-903a-b76078558d55
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 73%

---

# Analytics 보고 API

Adobe Analytics API에 대한 설명서는 [Adobe I/O](https://adobe.io/analytics-apis/docs)에 있습니다.

## Analytics API 비교

| **API 유형** | **완전히 처리됨** | **실시간** | **라이브 스트림** | **Data Warehouse** |
| --- | --- | --- | --- | --- |
| **설명** | 모든 Analytics 인터페이스에서 사용할 수 있는 완료된 데이터로, 완전히 처리되었습니다. | 컬렉션이 발생하면 바로 사용할 수 있는 제한된 지표로, 부분적으로 처리되었습니다. | 컬렉션이 발생하면 바로 사용할 수 있는 히트 데이터로, 부분적으로 처리되었습니다. | 가져온 대용량 데이터 내보내기에 사용되는 완료된 데이터로, 완전히 처리되었습니다. |
| [**지연**](/help/technotes/latency.md) | 30-90분 | 초 -10분 | 초 -10분 | 90분 이상 |
| **처리 완료** | 전체 | 부분 | 부분 | 전체 |
| **보고 인터페이스** | Analysis Workspace, Reports &amp; Analytics, Report Builder, API | Reports &amp; Analytics, Report Builder, 1.4 API의 실시간 보고서 | API 전용 | Data Warehouse, API |
| **데이터 세부기간** | 요약 | 요약 | 히트 수준 | 요약 |
| **방문자 프로필 처리** | 예 | 아니요 | 아니요 | 예 |
| **세그먼트 지원** | 예 | 아니요 | 아니요 | 부분 |
