---
title: VRS 및 프로젝트 큐레이션
description: vrs 구성 요소 및 프로젝트 조정 방법 알아보기
translation-type: tm+mt
source-git-commit: db983980a6ec3db4d60bbc8fc3ba57a4e1219287

---


# VRS 및 프로젝트 큐레이션

프로젝트 또는 VRS(가상 보고서 세트)를 조정하는 경우 기본적으로 사용하려는 프로젝트/VRS 구성 요소(차원, 지표, 세그먼트, 날짜 범위)만 대상에게 표시되도록 구성 요소를 필터링합니다.

>[!NOTE]
>
>제품 프로필은 사용자가 볼 수 있는 구성 요소를 관리하는 기본 메커니즘으로, [Admin Console](https://helpx.adobe.com/kr/enterprise/using/manage-products-and-profiles.html#createproductprofiles)을 통해 관리됩니다. 큐레이션은 보조 필터입니다.

최근에 큐레이션 경험을 개선했습니다. Here is an overview of what the **[!UICONTROL Show All]** button reveals, in addition to the curated components already available, in different curated experiences and by permission level:

| 큐레이션 유형 | 관리자 | 관리자가 아닌 프로젝트 소유자 | 비관리자 |
|---|---|---|---|
| 조정된 VRS | 조정되지 않은 모든 VRS 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 VRS 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 VRS 구성 요소 |
| 조정된 프로젝트 | 조정되지 않은 모든 프로젝트 구성 요소 | 조정되지 않은 모든 프로젝트 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 프로젝트 구성 요소 |
| 조정된 VRS에서 조정된 프로젝트 | All non-correcated components, shown under **[!UICONTROL Non-Curated Project Components]** 및 **[!UICONTROL Non-Curated VRS Components]** | 이 역할이 소유하거나 이 역할과 공유된 모든 조정되지 않은 모든 구성 요소와 조정되지 않은 프로젝트 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 VRS 및 프로젝트 구성 요소 |

>[!IMPORTANT]
>
>VRS 조정은 항상 프로젝트 조정 전에 적용됩니다. 즉, 조정된 프로젝트에 특정 구성 요소가 포함되어 있더라도 조정된 VRS에 해당 구성 요소가 포함되어 있지 않으면 필터링됩니다.
