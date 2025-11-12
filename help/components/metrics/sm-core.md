---
title: Streaming Media 서비스 핵심 지표
description: 보고서 세트에 대해 [!UICONTROL 미디어 코어]을(를) 사용하도록 설정할 때 사용 가능한 지표입니다.
feature: Metrics
exl-id: f4ff5f84-18b6-4e67-b808-133faeaf8605
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# Streaming Media 서비스 핵심 지표

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 코어]을(를) 사용할 때 사용할 수 있는 지표를 설명합니다. 사용 가능한 차원은 [Streaming Media 서비스 핵심 차원](../dimensions/sm-core.md)을 참조하십시오.*

스트리밍 미디어 서비스 핵심 지표는 스트리밍 미디어 서비스 컬렉션 라이브러리를 통해 수집된 데이터에 기본 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [미디어 코어](/help/admin/tools/manage-rs/edit-settings/media-management.md)을(를) 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 | XDM 필드 |
| --- | --- | --- | --- | --- |
| **[!UICONTROL 평균 분당 시청 대상자]** | 특정 콘텐츠에 소요된 총 시간을 모든 해당 재생 세션의 해당 길이로 나눈 값입니다.<br>`[Time spent] / [Media length]` | 미디어 닫기 | `a.media.`<br>`averageMinuteAudience` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`averageMinuteAudience` |
| **[!UICONTROL 컨텐츠 완료]** | 콘텐츠 조각이 완료되면 트리거됩니다. 이 지표는 반드시 전체 콘텐츠를 본다는 의미는 아닙니다. 앞으로 건너뛸 수도 있습니다. 이는 콘텐츠의 끝에 도달했음을 의미할 뿐입니다. | | `a.media.complete` | `xdm.mediaReporting.`<br>`sessionDetails.isCompleted` |
| **[!UICONTROL 일시 중지된 영향을 받은 스트림]** | 컨텐츠 재생 중에 하나 이상의 일시 중지가 발생했는지 여부를 트리거하는 부울입니다. | 미디어 닫기 | `a.media.pause` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`hasPauseImpactedStreams` |
| **[!UICONTROL 이벤트 일시 중지]** | 재생 세션 도중 발생한 일시 중지 수입니다. | 미디어 닫기 | `a.media.pauseCount` | `xdm.mediaReporting.`<br>`sessionDetails.pauseCount` |
| **[!UICONTROL 총 일시 중단 기간]** | 모든 일시 중지 이벤트의 총 기간(초)입니다. | 미디어 닫기 | `a.media.pauseTime` | `xdm.mediaReporting.`<br>`sessionDetails.pauseTime` |
| **[!UICONTROL 콘텐츠 시작]** | 미디어의 첫 번째 프레임이 사용됩니다. 광고 또는 버퍼링 중에 사용자가 그만두면 이 이벤트가 트리거되지 않습니다. | 미디어 닫기 | `a.media.play` | `xdm.mediaReporting.`<br>`sessionDetails.isPlayed` |
| **[!UICONTROL 10% 진행률 마커]**<br>**[!UICONTROL 25% 진행률 마커]**<br>**[!UICONTROL 50% 진행률 마커]**<br>**[!UICONTROL 75% 진행률 마커]**<br>**[!UICONTROL 95% 진행률 마커]** | 플레이헤드는 길이에 따라 컨텐츠의 표시된 마커를 전달합니다. 각 마커는 뒤로 검색하는 경우에도 한 번만 카운트됩니다. 앞으로 검색하는 경우 건너뛴 마커는 카운트되지 않습니다. | 미디어 닫기 | `a.media.progress10`<br>`a.media.progress25`<br>`a.media.progress50`<br>`a.media.progress75`<br>`a.media.progress95` | `xdm.mediaReporting.`<br>`sessionDetails.hasProgress10`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress25`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress50`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress75`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress95` |
| **[!UICONTROL 콘텐츠 다시 시작]** | 버퍼, 일시 중지 또는 지연 기간이 30분 이상 지난 후 콘텐츠가 다시 시작될 때 트리거되는 부울입니다. 또한 플레이어가 VideoInfo trackPlay에 설정한 경우 트리거됩니다. | 미디어 닫기 | `a.media.resume` | `xdm.mediaCollection.`<br>`sessionDetails.hasResume`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasResume` |
| **[!UICONTROL 콘텐츠 세그먼트 보기]** | 본 세그먼트의 첫 번째 프레임에서 트리거되는 부울입니다. | 미디어 닫기 | `a.media.segmentView` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`hasSegmentView` |
| **[!UICONTROL 미디어 시작]** | 미디어가 처음 로드될 때 트리거되는 부울입니다. 이 이벤트에는 광고, 버퍼링 및 오류가 포함됩니다. | 미디어 시작 | `a.media.view` | `xdm.mediaReporting.`<br>`sessionDetails.isViewed` |
| **[!UICONTROL 콘텐츠 체류 시간]** | 기본 컨텐츠에서 재생 유형의 모든 이벤트에 대한 총 이벤트 기간(초)입니다. | 미디어 닫기 | `a.media.timePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.timePlayed` |
| **[!UICONTROL 재생된 고유 시간]** | 고유 콘텐츠가 재생되는 총 시간(초)입니다. 이 지표는 뒤로 검색하는 것과 같이 반복 콘텐츠를 볼 때 재생되는 시간을 제외합니다. | 미디어 닫기 | `a.media.`<br>`uniqueTimePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`uniqueTimePlayed` |
