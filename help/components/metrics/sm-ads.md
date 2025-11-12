---
title: Streaming Media 서비스 광고 지표
description: 보고서 세트에 대해 [!UICONTROL 미디어 광고]를 사용하도록 설정하는 경우 사용 가능한 지표입니다.
feature: Metrics
exl-id: f0ddf3e0-ab55-4a05-a8ae-f040ba26e704
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 5%

---

# Streaming Media 서비스 광고 지표

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 광고]를 사용하도록 설정할 때 사용할 수 있는 지표를 설명합니다. 사용 가능한 차원은 [스트리밍 미디어 서비스 광고 차원](../dimensions/sm-ads.md)을 참조하십시오.*

Streaming Media 서비스 광고 지표는 Streaming Media 서비스 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [미디어 광고](/help/admin/tools/manage-rs/edit-settings/media-management.md)를 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 | XDM 필드 |
| --- | --- | --- | --- | --- |
| **[!UICONTROL 광고 완료]** | 비디오 광고가 완료될 때 트리거됩니다. | 광고 닫기 | `a.media.ad.complete` | `xdm.mediaReporting.`<br>`advertisingDetails.isCompleted` |
| **[!UICONTROL 광고 시작]** | 비디오 광고가 시작될 때 트리거됩니다. | 광고 시작 | `a.media.ad.view` | `xdm.mediaReporting.`<br>`advertisingDetails.isStarted` |
| **[!UICONTROL 광고 체류 시간]** | 광고를 시청하는 데 걸린 총 시간(초)입니다. | 광고 닫기 | `a.media.ad.timePlayed` | `xdm.mediaReporting.`<br>`advertisingDetails.timePlayed` |
| **[!UICONTROL 미디어 체류 시간]** | 모든 &#39;[!UICONTROL 재생]&#39; 이벤트(기본 콘텐츠와 광고 콘텐츠 모두)의 이벤트 기간(초)을 합합니다. | 미디어 닫기 | `a.media.totalTimePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.totalTimePlayed` |
