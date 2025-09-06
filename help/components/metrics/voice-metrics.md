---
title: 음성 분석 지표
description: 음성 분석 지표
feature: Metrics
exl-id: 3c1b4e4e-d8d2-446f-9582-a2ce5580a8d3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 21%

---

# 음성 분석 지표

[!UICONTROL 응용 프로그램 보고]에서 [[!UICONTROL 음성 및 챗봇]](/help/admin/tools/manage-rs/edit-settings/app-reporting.md)을 사용하도록 설정하면 다음 지표(및 [차원](../dimensions/voice-dimensions.md))가 만들어집니다. [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)을(를) 사용하여 컨텍스트 데이터 변수를 `1`(해당하는 경우 그 이상) 값으로 설정할 수 있습니다. 보고서 세트 설정에서 사용하도록 설정하면 음성 분석 지표를 연결된 컨텍스트 데이터 변수에 매핑하는 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)이 자동으로 만들어집니다.

| 지표 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| 음성 발언 | 음성 도우미에 명령이 실행되면 트리거됩니다. | `a.voiceutterances` |
| 음성 종료 세션 | 음성 앱이 닫히면 트리거됩니다. | `a.voiceendsession` |
| 음성 오류 | 음성 앱에 오류가 발생하면 트리거됩니다. | `a.voiceerror` |

{style="table-layout:auto"}
