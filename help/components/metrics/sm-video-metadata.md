---
title: Streaming Media 비디오 메타데이터 지표
description: 보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]을(를) 사용하도록 설정할 때 사용 가능한 지표입니다.
feature: Metrics
exl-id: b2f60a34-e139-4498-bf71-74d291759ef2
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# Streaming Media 비디오 메타데이터 지표

*보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]을(를) 사용할 때 사용할 수 있는 지표에 대해 설명합니다. 사용 가능한 차원은 [스트리밍 미디어 비디오 메타데이터 차원](../dimensions/sm-video-metadata.md)을 참조하십시오.*

Streaming Media 비디오 메타데이터 지표는 스트리밍 미디어 컬렉션 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL Adobe 스트리밍 미디어 컬렉션]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

[미디어 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)에서 **[!UICONTROL 비디오 메타데이터]**&#x200B;을(를) 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 인증됨 | 사용자가 Adobe 인증을 통해 인증되면 트리거되는 부울입니다. | 미디어 시작, 미디어 종료 | `a.media.pass.auth` |

{style="table-layout:auto"}
