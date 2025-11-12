---
title: Streaming Media 서비스 비디오 메타데이터 지표
description: 보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]을(를) 사용하도록 설정할 때 사용 가능한 지표입니다.
feature: Metrics
exl-id: b2f60a34-e139-4498-bf71-74d291759ef2
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# Streaming Media 서비스 비디오 메타데이터 지표

*보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]을(를) 사용할 때 사용할 수 있는 지표에 대해 설명합니다. 사용 가능한 차원은 [스트리밍 미디어 서비스 비디오 메타데이터 차원](../dimensions/sm-video-metadata.md)을 참조하십시오.*

Streaming Media 서비스 비디오 메타데이터 지표는 Streaming Media 서비스 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [비디오 메타데이터](/help/admin/tools/manage-rs/edit-settings/media-management.md)을(를) 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 | XDM 필드 |
| --- | --- | --- | --- | --- |
| **[!UICONTROL 인증됨]** | 사용자가 Adobe 인증을 통해 인증되면 트리거되는 부울입니다. | 미디어 시작, 미디어 종료 | `a.media.pass.auth` | `xdm.mediaCollection.`<br>`sessionDetails.authorized`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.authorized` |
