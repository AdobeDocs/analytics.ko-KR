---
title: Streaming Media 서비스 오디오 메타데이터 차원
description: 보고서 세트에 대해 [!UICONTROL 오디오 메타데이터]을(를) 사용하도록 설정하는 경우 사용할 수 있는 차원입니다.
feature: Dimensions
exl-id: 2e4dc1e9-267b-47a2-b791-23d1e754a2c1
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 4%

---

# Streaming Media 서비스 오디오 메타데이터 차원

Streaming Media 서비스 및 차원은 Streaming Media 서비스 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 차원을 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [오디오 메타데이터](/help/admin/tools/manage-rs/edit-settings/media-management.md)을(를) 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

| 차원 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 | XDM 필드 |
| --- | --- | --- | --- | --- |
| **[!UICONTROL 앨범]** | 앨범 이름. | 미디어 시작, 미디어 종료 | `a.media.album` | `xdm.mediaCollection.`<br>`sessionDetails.album`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.album` |
| **[!UICONTROL 아티스트]** | 아티스트의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.artist` | `xdm.mediaCollection.`<br>`sessionDetails.artist`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.artist` |
| **[!UICONTROL 작성자]** | 오디오북 작성자의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.author` | `xdm.mediaCollection.`<br>`sessionDetails.author`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.author` |
| **[!UICONTROL 레이블]** | 레코드 레이블의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.label` | `xdm.mediaCollection.`<br>`sessionDetails.label`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.label` |
| **[!UICONTROL 게시자]** | 오디오 콘텐츠 게시자의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.publisher` | `xdm.mediaCollection.`<br>`sessionDetails.publisher`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.publisher` |
| **[!UICONTROL 스테이션]** | 라디오 방송국의 이름 또는 ID. | 미디어 시작, 미디어 종료 | `a.media.station` | `xdm.mediaCollection.`<br>`sessionDetails.station`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.station` |
