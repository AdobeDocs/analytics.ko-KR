---
title: 스트리밍 미디어 서비스 플레이어 상태 추적 지표
description: 보고서 세트에 대해 [!UICONTROL 플레이어 상태 추적]을(를) 사용하도록 설정할 때 사용 가능한 지표입니다.
feature: Metrics
exl-id: 324936cc-0c7a-4710-a618-b24cc6a2c2cf
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# 스트리밍 미디어 서비스 플레이어 상태 추적 지표

Streaming Media 서비스 플레이어 상태 추적 지표는 Streaming Media 서비스 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [플레이어 상태 추적](/help/admin/tools/manage-rs/edit-settings/media-management.md)을 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 | XDM 필드 |
| --- | --- | --- | --- | --- |
| **[!UICONTROL 닫힌 캡션의 영향을 받은 스트림]** | 재생 세션 중에 하나 이상의 닫힌 캡션 상태가 발생하는 경우 트리거됩니다. | 미디어 닫기 | `a.media.states.`<br>`closedcaptioning.set` | `mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL 자막 개수]** | 비디오가 자막 상태에 들어간 횟수입니다. | 미디어 닫기 | `a.media.states.`<br>`closedcaptioning.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL 자막 총 기간]** | 비디오가 자막 상태에 있었던 시간(초)입니다. | 미디어 닫기 | `a.media.states.`<br>`closedcaptioning.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL 전체 화면의 영향을 받은 스트림]** | 재생 세션 중에 하나 이상의 전체 화면 상태가 발생하는 경우 트리거됩니다. | 미디어 닫기 | `a.media.states.`<br>`fullscreen.set` | `xdm.mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL 전체 화면 수]** | 비디오가 전체 화면 상태에 들어간 횟수입니다. | 미디어 닫기 | `a.media.states.`<br>`fullscreen.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL 전체 화면 총 기간]** | 비디오가 전체 화면 상태에 있었던 시간(초)입니다. | 미디어 닫기 | `a.media.states.`<br>`fullscreen.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL 초점의 영향을 받은 스트림]** | 재생 세션 중에 하나 이상의 초점 상태가 발생한 경우 트리거됩니다. | 미디어 닫기 | `a.media.states.`<br>`infocus.set` | `mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL 포커스 카운트]** | 비디오가 초점 상태에 들어간 횟수입니다. | 미디어 닫기 | `a.media.states.`<br>`infocus.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL 초점 총 기간]** | 비디오가 초점 상태에 있었던 시간(초)입니다. | 미디어 닫기 | `a.media.states.`<br>`infocus.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL 음소거의 영향을 받은 스트림]** | 재생 세션 중에 하나 이상의 음소거 상태가 발생한 경우 트리거됩니다. | 미디어 닫기 | `a.media.states.`<br>`mute.set` | `xdm.mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL 음소거 카운트]** | 비디오가 음소거 상태로 전환된 횟수입니다. | 미디어 닫기 | `a.media.states.`<br>`mute.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL 음소거 총 기간]** | 비디오가 음소거 상태에 있었던 시간(초)입니다. | 미디어 닫기 | `a.media.states.`<br>`mute.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL 화면 속 화면의 영향을 받은 스트림]** | 재생 세션 중에 화면 속 화면 상태가 하나 이상 발생한 경우 트리거됩니다. | 미디어 닫기 | `a.media.states.`<br>`pictureinpicture.set` | `mediaReporting.states.`<br>`[*].isSet` |
| **[!UICONTROL 화면 속 화면 수]** | 비디오가 화면 속 화면 상태를 입력한 횟수입니다. | 미디어 닫기 | `a.media.states.`<br>`pictureinpicture.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL 화면 속 화면 총 시간]** | 비디오가 화면 속 화면 상태에 있었던 시간(초)입니다. | 미디어 닫기 | `a.media.states.`<br>`pictureinpicture.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
