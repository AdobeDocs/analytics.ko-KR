---
title: 마지막 터치 채널 세부 사항
description: 방문자의 참여 만료 내 가장 최근 마케팅 채널에 대한 세부 사항입니다.
feature: Dimensions
exl-id: def03267-f3e5-4772-a707-5678c45eba6d
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 80%

---

# 마지막 터치 채널 세부 사항

마지막 터치 채널 세부 사항&#39; [차원](overview.md)은(는) 해당 방문자의 참여 기간(기본적으로 30일) 동안 방문자가 일치하는 가장 최근 마케팅 채널에 대한 세부 사항을 보고합니다. 이 차원은 마케팅 채널과 일치하는 히트에 기여한 사항을 이해하는 데 유용합니다. 예를 들어 방문자가 사이트에 도달하고 &#39;유료 검색&#39; 마케팅 채널과 일치하는 경우 채널 세부 사항을 사용하여 사용한 검색 엔진 또는 검색한 키워드를 확인할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 다른 변수의 값을 복사합니다. 사용된 변수는 각 [마케팅 채널 처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md) 내의 채널 값을 참조합니다. 히트가 마케팅 채널 처리 규칙과 일치하면 [마지막 터치 채널](last-touch-channel.md) 차원이 채널 이름으로 설정되고 이 차원은 규칙에 설정된 채널 값으로 설정됩니다.

이 차원을 특정 값으로 설정하려면 다음 단계를 수행해야 합니다.

* 원하는 차원 항목이 히트 속성이나 사용자 지정 변수에 있는지 확인합니다.
* 히트에 대해 원하는 기준을 포함하는 마케팅 채널 처리 규칙을 설정합니다.
* 마케팅 채널 처리 규칙 내에서 [!UICONTROL 채널 값 설정]에서 원하는 드롭다운 값을 선택합니다.
* 사이트에 대한 방문자의 히트는 마케팅 채널 처리 규칙에 설명된 기준과 일치해야 합니다.

## 차원 항목

Dimension 항목은 해당 마케팅 채널 처리 규칙의 드롭다운 목록에 나열된 채널 값에 따라 다릅니다. 예를 들어 채널의 값을 &#39;페이지 URL&#39;로 설정하면 차원 항목에 사이트의 페이지 URL이 포함됩니다. 채널의 값을 참조 도메인으로 설정하면, 차원 항목에는 방문자가 사이트에 액세스하기 위해 클릭스루한 도메인이 포함됩니다. 이 차원은 차원 항목이 속한 채널에 관계없이 모든 세부 차원 값을 집계합니다.

채널 세부 정보에 대한 통찰력을 위해 마케팅 채널과 관련된 채널 값을 설정하는 것이 좋습니다.
