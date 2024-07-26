---
title: Streaming Media 오디오 메타데이터 차원
description: 보고서 세트에 대해 [!UICONTROL 오디오 메타데이터]을(를) 사용하도록 설정하는 경우 사용할 수 있는 차원입니다.
feature: Dimensions
source-git-commit: 45b371bd20223b86d0f17d9bdb48cffb2de15468
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 8%

---

# Streaming Media 오디오 메타데이터 차원

Streaming Media 광고 차원은 스트리밍 미디어 컬렉션 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 차원을 사용하려면 **[!UICONTROL Adobe 스트리밍 미디어 컬렉션 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

[미디어 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)에서 **[!UICONTROL 오디오 메타데이터]**&#x200B;을(를) 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

| 차원 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 앨범 | 앨범 이름. | 미디어 시작, 미디어 종료 | `a.media.album` |
| 아티스트 | 아티스트의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.artist` |
| 작성자 | 오디오북 작성자의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.author` |
| 레이블 | 레코드 레이블의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.label` |
| 게시자 | 오디오 콘텐츠 게시자의 이름입니다. | 미디어 시작, 미디어 종료 | `a.media.publisher` |
| 방송국 | 라디오 방송국의 이름 또는 ID. | 미디어 시작, 미디어 종료 | `a.media.station` |

{style="table-layout:auto"}
