---
title: Streaming Media 서비스 챕터 지표
description: 보고서 세트에 대해 [!UICONTROL 미디어 챕터]을(를) 사용하도록 설정할 때 사용 가능한 지표입니다.
feature: Metrics
exl-id: bef379d5-9dc9-404f-8197-1ba66d11299d
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 5%

---

# Streaming Media 서비스 챕터 지표

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 챕터]를 사용할 때 사용할 수 있는 지표를 설명합니다. 사용 가능한 차원은 [스트리밍 미디어 서비스 챕터 차원](../dimensions/sm-chapters.md)을 참조하십시오.*

스트리밍 미디어 서비스 챕터 지표는 스트리밍 미디어 서비스 컬렉션 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [미디어 챕터](/help/admin/tools/manage-rs/edit-settings/media-management.md)을(를) 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 | XDM 필드 |
| --- | --- | --- | --- | --- |
| **[!UICONTROL 챕터 완료]** | 챕터가 완료되면 트리거되는 부울입니다. | 챕터 닫기 | `a.media.chapter.complete` | `xdm.mediaReporting.`<br>`chapterDetails.isCompleted` |
| **[!UICONTROL 챕터 시작]** | 챕터가 시작될 때 트리거되는 부울입니다. | 챕터 시작 | `a.media.chapter.view` | `xdm.mediaReporting.`<br>`chapterDetails.isStarted` |
| **[!UICONTROL 챕터 체류 시간]** | 챕터에서 보낸 시간(초)입니다. | 챕터 닫기 | `a.media.chapter.timePlayed` | `xdm.mediaReporting.`<br>`chapterDetails.timePlayed` |
