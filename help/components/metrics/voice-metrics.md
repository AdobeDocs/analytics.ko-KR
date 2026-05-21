---
title: 음성 분석 지표
description: 음성 분석 지표
feature: Metrics
exl-id: 3c1b4e4e-d8d2-446f-9582-a2ce5580a8d3
TQID: https://experienceleague.adobe.com/snDtqM3TiX--cjPjKj8cGkaFxMIxRprvD4ia9OnBXJk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 21%

---

# 음성 분석 지표

[[!UICONTROL 응용 프로그램 보고]](/help/admin/tools/manage-rs/edit-settings/app-reporting.md)에서 [!UICONTROL 음성 및 챗봇]을 사용하도록 설정하면 다음 지표(및 [차원](../dimensions/voice-dimensions.md))가 만들어집니다. [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)을(를) 사용하여 컨텍스트 데이터 변수를 `1`(해당하는 경우 그 이상) 값으로 설정할 수 있습니다. 보고서 세트 설정에서 사용하도록 설정하면 음성 분석 지표를 연결된 컨텍스트 데이터 변수에 매핑하는 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)이 자동으로 만들어집니다.

| 지표 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| 음성 발언 | 음성 도우미에 명령이 실행되면 트리거됩니다. | `a.voiceutterances` |
| 음성 종료 세션 | 음성 앱이 닫히면 트리거됩니다. | `a.voiceendsession` |
| 음성 오류 | 음성 앱에 오류가 발생하면 트리거됩니다. | `a.voiceerror` |

{style="table-layout:auto"}
