---
title: 스트리밍 미디어 품질 지표
description: 보고서 세트에 대해 [!UICONTROL 미디어 품질]을(를) 사용하도록 설정할 때 사용 가능한 지표입니다.
feature: Metrics
exl-id: a64829b5-d45b-44c6-80c3-5acf1a6d9919
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# 스트리밍 미디어 품질 지표

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 품질]을(를) 사용하도록 설정할 때 사용할 수 있는 지표를 설명합니다. 사용 가능한 차원은 [스트리밍 미디어 품질 차원](../dimensions/sm-quality.md)을 참조하십시오.*

Streaming Media 품질 지표는 스트리밍 미디어 컬렉션 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 지표를 사용하려면 **[!UICONTROL Adobe 스트리밍 미디어 컬렉션]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

[미디어 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)에서 **[!UICONTROL 미디어 품질]**&#x200B;을(를) 사용하도록 설정하면 다음 지표를 사용할 수 있습니다.

| 지표 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 평균 비트율 | 재생 세션의 재생 기간 동안 모든 비트율 값의 가중 평균. | 미디어 닫기 | `a.media.qoe.bitrateAverage` |
| 비트율 변경의 영향을 받는 스트림 | 재생 세션 중에 비트율이 한 번 이상 변경되는지 여부를 트리거하는 부울입니다. | 미디어 닫기 | `a.media.qoe.bitrateChange` |
| 비트율 변경 | 비트율이 변경된 횟수입니다. | 미디어 닫기 | `a.media.qoe.bitrateChangeCount` |
| 버퍼의 영향을 받는 스트림 | 비디오가 버퍼 상태에 한 번 이상 들어가는지 여부를 트리거하는 부울입니다. | 미디어 닫기 | `a.media.qoe.buffer` |
| 버퍼 이벤트 | 재생 세션 중에 비디오가 버퍼된 횟수입니다. | 미디어 닫기 | `a.media.qoe.bufferCount` |
| 총 버퍼 지속 시간 | 비디오가 모든 버퍼 이벤트에서 버퍼링에 소요된 시간(초)입니다. | 미디어 닫기 | `a.media.qoe.bufferTime` |
| 시작 전 드롭 | 비디오의 기본 컨텐츠가 시작되기 전에 사용자가 종료하면 트리거하는 부울입니다. | 미디어 닫기 | `a.media.qoe.dropBeforeStart` |
| 드롭된 프레임 | 재생 세션 도중 드롭된 총 프레임 수를 나타내는 정수입니다. | 미디어 닫기 | `a.media.qoe.droppedFrameCount` |
| 드롭된 프레임의 영향을 받는 스트림 | 재생 세션 중에 프레임이 드롭될 때 트리거하는 부울입니다. | 미디어 닫기 | `a.media.qoe.droppedFrames` |
| 오류의 영향을 받은 스트림 | 재생 세션 중에 비디오에 오류가 발생할 때 트리거하는 부울입니다. | 미디어 닫기 | `a.media.qoe.error` |
| 오류 이벤트 | 재생 세션 도중 발생한 총 오류 수를 나타내는 정수입니다. | 미디어 닫기 | `a.media.qoe.errorCount` |
| 시작 시간 | 비디오를 시작하는 데 걸린 시간(밀리초)입니다. Adobe은 이 값을 초 단위로 변환하여 저장합니다. | 미디어 닫기 | `a.media.qoe.timeToStart` |
