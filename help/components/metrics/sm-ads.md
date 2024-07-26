---
title: 스트리밍 미디어 광고 지표
description: 보고서 세트에 대해 [!UICONTROL 미디어 광고]를 사용하도록 설정하는 경우 사용 가능한 지표입니다.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---

# 스트리밍 미디어 광고 지표

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 광고]를 사용하도록 설정할 때 사용할 수 있는 지표를 설명합니다. 사용 가능한 차원은 [스트리밍 미디어 광고 차원](../dimensions/sm-ads.md)을 참조하십시오.*

Streaming Media 광고 지표는 스트리밍 미디어 컬렉션 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL Adobe 스트리밍 미디어 컬렉션 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

[미디어 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)에서 **[!UICONTROL 미디어 광고]**&#x200B;를 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 광고 완료 | 비디오 광고가 완료될 때 트리거됩니다. | 광고 닫기 | `a.media.ad.complete` |
| 광고 시작 | 비디오 광고가 시작될 때 트리거됩니다. | 광고 시작 | `a.media.ad.view` |
| 광고 체류 시간 | 광고를 시청하는 데 걸린 총 시간(초)입니다. | 광고 닫기 | `a.media.ad.timePlayed` |
| 미디어 체류 시간 | 모든 재생 이벤트(기본 컨텐츠와 광고 컨텐츠 모두)에 대한 이벤트 기간(초)을 합합니다. | 미디어 닫기 | `a.media.totalTimePlayed` |

{style="table-layout:auto"}
