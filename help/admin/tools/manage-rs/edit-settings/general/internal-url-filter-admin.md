---
description: 내부 URL 필터는 사이트 내부로 간주되는 참조를 식별합니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.
title: 내부 URL 필터
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 31%

---


# 내부 URL 필터

내부 URL 필터를 사용하면 사이트 내부로 간주하는 레퍼러를 식별할 수 있습니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.

**[!UICONTROL Analytics]** > **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 내부 URL 필터]**

참조 또는 참조 페이지는 일반적으로 방문자가 해당 페이지로부터 사용자의 사이트에 들어가게 되는 페이지입니다. 데이터 왜곡을 막기 위해 내부 참조를 필터링할 수 있습니다. 내부 URL 필터에 의존하는 차원에는 [레퍼러](/help/components/dimensions/referrer.md), [참조 도메인](/help/components/dimensions/referring-domain.md), [마케팅 채널](/help/components/dimensions/marketing-channel.md) 및 기타 트래픽 소스 차원이 포함됩니다.

[마케팅 채널 처리 규칙](../marketing-channels/c-rules.md)은(는) 가능한 규칙 기준으로 &quot;[!UICONTROL 내부 URL 필터와 일치]&quot;을 제공합니다.

>[!IMPORTANT]
>
>일부 보고서 세트에는 기본적으로 구성된 기간(`.`)의 내부 URL 필터가 있습니다. 이 필터가 존재하면 모든 트래픽은 내부로 분류됩니다. 레퍼러 보고서는 이 필터를 제거하고 하나 이상의 원하는 내부 도메인으로 바꿀 때까지 작동하지 않습니다.

* **[!UICONTROL 현재 필터]** 섹션에서 기존 필터를 모두 봅니다.
* **[!UICONTROL 필터 추가]** 섹션 아래의 텍스트 상자를 사용하여 필터를 추가한 다음 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

필터는 전체 URL에 대해 **contains** 논리를 사용하여 작동합니다. Adobe에서는 별도의 하위 도메인의 트래픽을 외부 트래픽으로 원하지 않는 경우 필터를 만들 때 프로토콜(`https://`) 및 하위 도메인을 생략하는 것이 좋습니다.
