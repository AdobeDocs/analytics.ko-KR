---
title: 스트리밍 미디어 비디오 메타데이터 차원
description: 보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]을(를) 사용하도록 설정하는 경우 사용할 수 있는 차원입니다.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 7%

---

# 스트리밍 미디어 비디오 메타데이터 차원

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 비디오 메타데이터]를 사용하도록 설정할 때 사용할 수 있는 차원을 설명합니다. 사용 가능한 지표는 [스트리밍 미디어 비디오 메타데이터 지표](../metrics/sm-video-metadata.md)를 참조하십시오.*

Streaming Media 광고 차원은 스트리밍 미디어 컬렉션 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 차원을 사용하려면 **[!UICONTROL Adobe 스트리밍 미디어 컬렉션 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

[미디어 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)에서 **[!UICONTROL 비디오 메타데이터]**&#x200B;을(를) 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

| 차원 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 광고 로드 | 로드된 광고 유형. | TBD | `a.media.adLoad` |
| 방송 시간대 | 콘텐츠가 브로드캐스트 또는 재생되는 시간. 모든 문자열 값이 지원됩니다. | 미디어 시작, 미디어 종료 | `a.media.dayPart` |
| 에피소드 | 에피소드 번호. | 미디어 시작, 미디어 종료 | `a.media.episode` |
| 미디어 피드 유형 | 피드 유형. | 미디어 시작, 미디어 종료 | `a.media.feed` |
| 장르 | 콘텐츠 생성자가 정의한 콘텐츠 유형 또는 그룹입니다. 이 차원은 쉼표로 구분된 여러 값을 지원합니다. | 미디어 시작, 미디어 종료 | `a.media.genre` |
| MVPD | Adobe 인증에서 제공한 MVPD입니다. | 미디어 시작, 미디어 종료 | `a.media.pass.mvpd` |
| 네트워크 | 네트워크 또는 채널 이름 | 미디어 시작, 미디어 종료 | `a.media.network` |
| 시즌 | 시연이 포함된 시즌 번호입니다. | 미디어 시작, 미디어 종료 | `a.media.season` |
| 표시 | 프로그램 또는 시리즈 이름. | 미디어 시작, 미디어 종료 | `a.media.show` |
| 표시 유형 | 콘텐츠 유형을 나타내는 정수.<br>`0`: 전체 에피소드<br>`1`: 미리 보기 또는 예고편<br>`2`: 클립<br>`3`: 기타 | 미디어 시작, 미디어 종료 | `a.media.type` |

{style="table-layout:auto"}
