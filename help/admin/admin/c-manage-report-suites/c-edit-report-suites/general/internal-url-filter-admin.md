---
description: 내부 URL 필터는 사이트 내부로 간주되는 참조를 식별합니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.
title: 내부 URL 필터
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 5c2643a143e5c8e17fcf11cfa2da81183bc5c39a
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 31%

---


# 내부 URL 필터

내부 URL 필터를 사용하면 사이트 내부로 간주하는 레퍼러를 식별할 수 있습니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.

**[!UICONTROL 분석]** > **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 내부 URL 필터]**

참조 또는 참조 페이지는 일반적으로 방문자가 해당 페이지로부터 사용자의 사이트에 들어가게 되는 페이지입니다. 데이터 왜곡을 막기 위해 내부 참조를 필터링할 수 있습니다. 내부 URL 필터에 의존하는 Dimension은 다음과 같습니다 [레퍼러](/help/components/dimensions/referrer.md), [참조 도메인](/help/components/dimensions/referring-domain.md), [마케팅 채널](/help/components/dimensions/marketing-channel.md), 기타 트래픽 소스 차원.

[마케팅 채널 처리 규칙](../marketing-channels/c-rules.md) &quot;제공[!UICONTROL 내부 URL 필터와 일치]가능한 규칙 기준으로 &quot;를 사용하십시오.

>[!IMPORTANT]
>
>일부 보고서 세트에는 마침표()의 내부 URL 필터가 있습니다.`.`) 기본적으로 구성됩니다. 이 필터가 존재하면 모든 트래픽은 내부로 분류됩니다. 레퍼러 보고서는 이 필터를 제거하고 하나 이상의 원하는 내부 도메인으로 바꿀 때까지 작동하지 않습니다.

* 아래의 기존 필터 모두 보기 **[!UICONTROL 현재 필터]** 섹션.
* 아래 텍스트 상자를 사용하여 필터 추가 **[!UICONTROL 필터 추가]** 섹션을 클릭한 다음 **[!UICONTROL 추가]**.

필터는 다음을 사용하여 작동합니다. **다음 포함** 전체 URL에 대한 논리입니다. Adobe은 프로토콜을 생략하도록 권장합니다(`https://`별도의 하위 도메인의 트래픽이 외부 트래픽으로 필요한 경우가 아닌 경우 및 하위 도메인(필터를 만들 때)
