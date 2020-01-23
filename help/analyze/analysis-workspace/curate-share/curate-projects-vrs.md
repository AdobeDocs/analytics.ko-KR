---
title: VRS 및 프로젝트 큐레이션
description: vrs 구성 요소 및 프로젝트 조정 방법 알아보기
translation-type: tm+mt
source-git-commit: 3a00162c5899ba2d5bb1b5aaed448b2abe93d56d

---


# VRS 및 프로젝트 큐레이션

프로젝트 또는 VRS(가상 보고서 세트)를 조정하는 경우 기본적으로 사용하려는 프로젝트/VRS 구성 요소(차원, 지표, 세그먼트, 날짜 범위)만 대상에게 표시되도록 구성 요소를 필터링합니다.

>[!N참고]
>제품 프로필은 사용자가 볼 수 있는 구성 요소를 제어하는 기본 메커니즘입니다. They are managed through the [Admin Console](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html#createproductprofiles). 큐레이션은 보조 필터입니다.

최근에 큐레이션 경험을 개선했습니다. 다음은 이미 사용 가능한 조정된 구성 요소 외에 조정된 다른 환경에서 권한 수준별로 **[!UICONTROL 모두 표시]**단추가 무엇을 나타내는지에 대해 간략히 설명한 것입니다.

| 큐레이션 유형 | 관리자 | 관리자가 아닌 프로젝트 소유자 | 비관리자 |
|---|---|---|---|
| 조정된 VRS | 조정되지 않은 모든 VRS 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 VRS 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 VRS 구성 요소 |
| 조정된 프로젝트 | 조정되지 않은 모든 프로젝트 구성 요소 | 조정되지 않은 모든 프로젝트 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 프로젝트 구성 요소 |
| 조정된 VRS에서 조정된 프로젝트 | 조정되지 않은 모든 구성 요소 **[!UICONTROL Non-Curated Project Components]**and**[!UICONTROL  Non-Curated VRS Components]** | 이 역할이 소유하거나 이 역할과 공유된 모든 조정되지 않은 모든 구성 요소와 조정되지 않은 프로젝트 구성 요소 | 이 역할이 소유하거나 함께 공유한 조정되지 않은 VRS 및 프로젝트 구성 요소 |

>[!IMPORTANT]
>VRS 조정은 프로젝트 조정 전에 항상 적용됩니다. 즉, 선별된 프로젝트에 특정 구성 요소가 포함되어 있더라도 선별된 VRS에 해당 구성 요소가 포함되어 있지 않으면 필터링됩니다.
