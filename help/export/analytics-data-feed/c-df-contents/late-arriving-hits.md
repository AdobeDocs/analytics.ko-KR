---
title: Late-arriving hits
description: Learn how data feeds treat late-arriving hits.
feature: Data Feeds
exl-id: c99a702b-2aaa-47a6-958a-1e5ab66961ba
source-git-commit: 4d0007d1a23a81f0d5ba60541b4f7b9ac7b00ace
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 41%

---

# 늦게 도착하는 히트 {#late-arriving-hits}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_late_hits"
>title="늦게 도착하는 히트 허용"
>abstract="이 옵션을 선택하면 데이터 피드 작업이 완료된 후에 도착한 데이터를 설정된 보고 빈도(보통 일별 또는 시간별) 내에 포함합니다. 이 옵션이 활성화되면 데이터 피드에서 데이터를 처리할 때마다 데이터 피드는 늦게 도착하는 모든 히트를 조회하고 전송된 다음번 데이터 피드 파일과 함께 배치합니다."

<!-- markdownlint-enable MD034 -->

## Understand late-arriving hits

Historical data can arrive after a data feed job finishes processing for a given hour or day, such as through timestamped hits or data sources.

데이터 피드는 일반적으로 데이터를 처리할 때 보고 창 내에서만 데이터를 조회합니다 (일반적으로 가장 최근 시간 또는 일수). 피드에서 해당 보고 기간의 처리를 마친 후에 데이터가 도착하는 경우 해당 데이터는 데이터 피드에 포함되지 않습니다.

With late-arriving hits enabled, the processing method changes to include this data. 데이터 피드는 데이터를 처리할 때마다 도착한 모든 히트를 조회하고 전송된 다음 데이터 피드 파일에 데이터를 배치합니다.

## Enable late-arriving hits

Before enabling the option to allow late-arriving hits for a data feed, consider the following:

* Data for different days frequently appear in data feeds when late-arriving hits are enabled. 데이터 피드를 수집하는 데 사용하는 플랫폼이 동일한 파일 내에서 다른 요일의 데이터를 수용할 수 있는지 확인합니다.
* If a data feed file is reprocessed, the late-arriving hits that were included in the original file are included in the reprocessed file when reprocessing occurs within the first 5 days. After 5 days, late-arriving hits are not included in the reprocessed file.

You can enable late-arrive hits when creating or editing a data feed by enabling the option, **[!UICONTROL Allow late-arriving hits]**, as described in [Create a data feed](/help/export/analytics-data-feed/create-feed.md).
