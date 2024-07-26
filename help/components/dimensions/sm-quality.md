---
title: 스트리밍 미디어 품질 차원
description: 보고서 세트에 대해 [!UICONTROL 미디어 품질]을(를) 사용하도록 설정하는 경우 사용 가능한 차원입니다.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---

# 스트리밍 미디어 품질 차원

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 품질]을(를) 사용할 때 사용할 수 있는 차원을 설명합니다. 사용 가능한 지표는 [스트리밍 미디어 품질 지표](../metrics/sm-quality.md)를 참조하십시오.*

Streaming Media 품질 차원은 방문자가 사용하는 콘텐츠의 품질과 관련된 보고를 제공합니다. 이 차원을 사용하려면 [!UICONTROL Adobe 스트리밍 미디어 컬렉션 추가 기능]이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

[미디어 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)에서 **[!UICONTROL 미디어 품질]**&#x200B;을(를) 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

| Dimension 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 평균 비트율 | 평균 비트율(100KBPS 버킷 간격). 지정된 재생 세션의 재생 기간과 관련하여 모든 비트율 값의 가중 평균으로 계산됩니다. | 미디어 닫기 | `a.media.qoe.bitrateAverageBucket` |
| 비트율 변경 | 재생 세션 도중 발생한 비트율 변경 횟수입니다. | 미디어 닫기 | `a.media.qoe.bitrateChangeCount` |
| 버퍼 이벤트 | 재생 세션 도중 미디어 플레이어가 버퍼 상태에 들어간 횟수입니다. | 미디어 닫기 | `a.media.qoe.bufferCount` |
| 총 버퍼 지속 시간 | 버퍼링에 소요된 총 시간(초)입니다. | 미디어 닫기 | `a.media.qoe.bufferTime` |
| 드롭된 프레임 | 재생 세션 도중 드롭된 총 프레임 수. | 미디어 닫기 | `a.media.qoe.droppedFrameCount` |
| 오류 | 재생 세션 도중 발생한 총 오류 수입니다. | 미디어 닫기 | `a.media.qoe.errorCount` |
| 외부 오류 ID | CDN 오류와 같은 외부 소스의 모든 고유 오류 ID. 원하는 오류 코드 또는 ID를 제공해야 합니다. 여러 오류 ID가 허용됩니다. | 미디어 닫기 | `a.media.qoe.externalErrors` |
| 플레이어 SDK 오류 ID | 콘텐츠 플레이어 SDK에서 생성한 모든 고유 오류 ID입니다. 원하는 오류 코드 또는 ID를 제공해야 합니다. 여러 오류 ID가 허용됩니다. | 미디어 닫기 | `a.media.qoe.playerSdkErrors` |
| 시작 시간 | 이 값은 QoSObject를 통해 설정되지 않은 경우 기본적으로 `0`입니다. 값을 밀리초 단위로 설정합니다. Analysis Workspace은 이 차원을 초 단위로 보고합니다. | 미디어 시작, 미디어 종료 | `a.media.qoe.timeToStart` |

{style="table-layout:auto"}
