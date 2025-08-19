---
title: Streaming Media 챕터 차원
description: 보고서 세트에 대해 [!UICONTROL 미디어 챕터]을(를) 사용하도록 설정하는 경우 사용할 수 있는 차원입니다.
feature: Dimensions
exl-id: cac66a0b-3f83-46a9-b35c-ba08e0eafb92
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 13%

---

# 스트리밍 미디어 서비스 챕터 차원

*이 페이지에서는 보고서 세트에 대해 [!UICONTROL 미디어 챕터]를 사용할 때 사용할 수 있는 차원을 설명합니다. 사용 가능한 지표는 [스트리밍 미디어 서비스 챕터 지표](../metrics/sm-chapters.md)를 참조하십시오.*

Streaming Media 서비스 챕터 차원은 Streaming Media 서비스 라이브러리를 통한 데이터 수집에 대한 보충 보고 기능을 제공합니다. 이 차원을 사용하려면 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 애드온]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

**[!UICONTROL 미디어 보고]**&#x200B;에서 [미디어 챕터](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md)을(를) 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

| 차원 이름 | 설명 | 전송 시점 | 컨텍스트 데이터 변수 |
| --- | --- | --- | --- |
| 챕터 | 자동으로 생성된 챕터 ID입니다. | 챕터 닫기 | `a.media.chapter.name` |

{style="table-layout:auto"}

위의 차원 외에도 Adobe은 자동으로 다음 분류 차원을 생성합니다. 이러한 차원을 사용하는 보고서를 보려면 분류 데이터를 업로드해야 합니다.

| 분류 이름 | 상위 차원 | 설명 |
| --- | --- | --- |
| 작성자 | [콘텐츠](sm-core.md) | 콘텐츠 작성자입니다. |
| 챕터 길이 | 챕터 | 챕터의 길이(초)입니다. |
| 챕터 이름 | 챕터 | 챕터의 알기 쉬운 이름. |
| 챕터 오프셋 | 챕터 | 처음부터 콘텐츠 내에 있는 챕터의 오프셋(초)입니다. |
| 챕터 위치 | 챕터 | 컨텐츠에서 챕터의 색인 위치입니다. |

{style="table-layout:auto"}
