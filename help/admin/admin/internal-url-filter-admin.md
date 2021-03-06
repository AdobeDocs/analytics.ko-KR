---
description: 내부 URL 필터는 사이트 내부로 간주되는 참조를 식별합니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.
title: 내부 URL 필터
feature: 관리 도구
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 95%

---


# 내부 URL 필터

내부 URL 필터는 사이트 내부로 간주되는 참조를 식별합니다. 이 필터들은 트래픽 소스 보고서가 데이터를 채우도록 하고 내부 트래픽을 필터링하는 데 도움이 됩니다.

**[!UICONTROL 관리자]**  >  **[!UICONTROL 보고서 세트]**  >  **[!UICONTROL 설정 편집]**  >  **[!UICONTROL 일반]**  >  **[!UICONTROL 내부 URL 필터]**

참조 또는 참조 페이지는 일반적으로 방문자가 해당 페이지로부터 사용자의 사이트에 들어가게 되는 페이지입니다. 데이터 왜곡을 막기 위해 내부 참조를 필터링할 수 있습니다. 보고서는 필터링된 참조를 [레퍼러](/help/components/dimensions/referrer.md) 차원, [참조 도메인](/help/components/dimensions/referring-domain.md) 차원 및 기타 트래픽 소스 차원.

트래픽 소스 보고서가 데이터를 채우지 않는 가장 일반적인 원인은 내부 URL 필터 목록이 정의되지 않은 것입니다. 어느 내부 URL 필터가 보고서 세트에서 설정되었는지 확인하려면, 다음 절차를 따르십시오. 이를 방지하려면 필터로서 마침표(.)를 나열하는 규칙을 제거하고 자신의 사이트를 추가하십시오.

마침표가 기본 내부 URL 필터인 이유는 페이지 보고서에서 데이터를 수집할 수 있도록 허용하기 위한 것입니다. 조회수가 내부 URL 필터와 일치하지 않는 경우, 모든 페이지는 기타로 표시됩니다. 마침표는 항상 URL의 어딘가에 있으며, 이렇게 되면 페이지 보고서가 채워집니다.
