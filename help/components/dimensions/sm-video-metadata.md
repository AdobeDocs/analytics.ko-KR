---
title: Streaming Media 서비스 비디오 메타데이터 차원
description: 보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]을(를) 사용하도록 설정하는 경우 사용할 수 있는 차원입니다.
feature: Dimensions
exl-id: e476c19a-9542-4a6f-9b79-5f801e2a7bf8
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 6%

---

# Streaming Media 서비스 비디오 메타데이터 차원

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]를 사용하도록 설정할 때 사용할 수 있는 차원을 설명합니다. 사용 가능한 지표는 [스트리밍 미디어 서비스 비디오 메타데이터 지표](../metrics/sm-video-metadata.md)를 참조하십시오.*

Streaming Media 서비스 및 차원은 Streaming Media 서비스 컬렉션 라이브러리를 통해 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 차원을 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 애드온]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [비디오 메타데이터](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)을(를) 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

| 차원 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 광고 로드 | 로드된 광고 유형. | TBD | `a.media.adLoad` |
| 방송 시간대 | 콘텐츠가 브로드캐스트 또는 재생되는 시간. 모든 문자열 값이 지원됩니다. | 미디어 시작, 미디어 종료 | `a.media.dayPart` |
| 에피소드 | 에피소드 번호. | 미디어 시작, 미디어 종료 | `a.media.episode` |
| 미디어 피드 유형 | 피드 유형. | 미디어 시작, 미디어 종료 | `a.media.feed` |
| 장르 | 콘텐츠 생성자가 정의한 콘텐츠 유형 또는 그룹입니다. 이 차원은 쉼표로 구분된 여러 값을 지원합니다. | 미디어 시작, 미디어 종료 | `a.media.genre` |
| MVPD | Adobe 인증에서 제공하는 MVPD. | 미디어 시작, 미디어 종료 | `a.media.pass.mvpd` |
| 네트워크 | 네트워크 또는 채널 이름 | 미디어 시작, 미디어 종료 | `a.media.network` |
| 시즌 | 시연이 포함된 시즌 번호입니다. | 미디어 시작, 미디어 종료 | `a.media.season` |
| 표시 | 프로그램 또는 시리즈 이름. | 미디어 시작, 미디어 종료 | `a.media.show` |
| 표시 유형 | 콘텐츠 유형을 나타내는 정수.<br>`0`: 전체 에피소드<br>`1`: 미리 보기 또는 예고편<br>`2`: 클립<br>`3`: 기타 | 미디어 시작, 미디어 종료 | `a.media.type` |

{style="table-layout:auto"}
