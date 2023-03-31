---
description: 내부 URL 필터는 사이트 내부로 간주되는 참조를 식별합니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.
title: 내부 URL 필터
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 2beb4cd38fc8b48e2b34468a4570f7168aeacb78
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 30%

---


# 내부 URL 필터

내부 URL 필터를 사용하여 사이트 내부로 간주하는 레퍼러를 식별할 수 있습니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.

참조 또는 참조 페이지는 일반적으로 방문자가 해당 페이지로부터 사용자의 사이트에 들어가게 되는 페이지입니다. 데이터 왜곡을 막기 위해 내부 참조를 필터링할 수 있습니다. 보고서는 필터링된 참조를 [레퍼러](/help/components/dimensions/referrer.md) 차원, [참조 도메인](/help/components/dimensions/referring-domain.md) 차원 및 기타 트래픽 소스 차원.

## 기존 내부 URL 필터 보기

>[!NOTE]
>
>일부 보고서 세트에는 마침표(.)의 내부 URL 필터가 있습니다. 기본적으로 구성되어 있습니다. 이 필터가 있으면 모든 트래픽은 내부로 분류됩니다. 레퍼러 보고서는 기간(.)이 될 때까지 작동하지 않습니다 필터가 제거됩니다.

보고서 세트에 대해 구성된 내부 URL 필터를 확인하려면: <!-- I don't see the period in my instance? Is the following information valid? "To avoid this, remove the rule listing a period (.) as a filter, and add your own site. The reason why a period is the default internal URL filter is to allow data to be collected in the Pages report. If hits do not match internal URL filters, all pages come up as Other. A period is always somewhere in the URL, which guarantees the Pages report is populated.")-->

1. 선택 **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** 보고서 세트 관리자에 액세스합니다.

1. 구성할 내부 URL 필터를 확인할 보고서 세트를 선택한 다음 을 선택합니다 **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 내부 URL 필터]**.

   모든 기존 필터는 [!UICONTROL **현재 필터**] 섹션을 참조하십시오.

## 보고서 세트에 내부 URL 필터 추가

1. 선택 **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** 보고서 세트 관리자에 액세스합니다.

1. 내부 URL 필터를 추가할 보고서 세트를 선택한 다음 을 선택합니다 **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 내부 URL 필터]**.

1. 필터 추가 섹션의 제공된 필드에서 필터링하려는 페이지의 URL을 입력한 다음 을 선택합니다 [!UICONTROL **추가**].

   추가한 URL이 이제 [!UICONTROL **현재 필터**] 섹션을 참조하십시오.
