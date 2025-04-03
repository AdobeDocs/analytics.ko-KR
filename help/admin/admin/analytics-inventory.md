---
description: Analytics 인벤토리 사용
title: Analytics 인벤토리
feature: Admin Tools
role: Admin
hide: true
hidefromtoc: true
exl-id: 9fc985c8-93d7-4838-9342-72a6268ef96f
source-git-commit: fceb28b7af480e6d87abf09c26f45a7afb2d3270
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 37%

---

# Analytics 인벤토리 {#analytics-inventory}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory"
>title="Analytics 인벤토리"
>abstract="이 페이지에서는 프로젝트 및 구성 요소 수, 보고서 세트, 사용자 등을 포함하여 Adobe Analytics 환경에 대한 포괄적인 개요를 제공합니다. 이 정보는 특히 Customer Journey Analytics로 업그레이드하기 위한 준비를 시작할 때 매우 유용합니다."

<!-- markdownlint-enable MD034 -->

Analytics 인벤토리는 프로젝트 및 구성 요소 수, 보고서 세트, 사용자 등을 포함하여 Adobe Analytics 환경에 대한 포괄적인 개요를 제공합니다. 이 정보는 특히 Customer Journey Analytics로 업그레이드하기 위한 준비를 시작할 때 매우 유용합니다.

이 애플리케이션의 목표는 다음 질문에 답변하는 데 도움이 됩니다.

* 조직의 경우 어떤 에셋(보고서 세트, 세그먼트, 사용자, 작업 공간 프로젝트, 데이터 피드 등)을 업그레이드해야 하며 어떤 에셋을 남겨둘 수 있습니까?

* 마이그레이션해야 하는 자산을 결정했으면 다음과 같이 하십시오.

   * 이 업그레이드 전에 에셋 정리를 수행해야 합니까?

   * 프로세스의 일부로 자산 통합을 수행해야 합니까?

   * 자산에 대한 업그레이드 시퀀스는 무엇입니까?

   * 먼저 업그레이드해야 하는 보고서 세트 그룹은 무엇입니까? 마지막으로?

## 권한

Analytics 인벤토리는 [Adobe Admin Console](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/admin-roles-in-analytics)에서 Adobe Analytics 제품 관리자 권한이 있는 사용자가 사용할 수 있습니다.

## Analytics 인벤토리 액세스

1. **[!UICONTROL 관리자]** 메뉴에서 **[!UICONTROL Analytics 인벤토리]**&#x200B;를 클릭합니다. 또는 **[!UICONTROL 모든 관리자]** > **[!UICONTROL Analytics 인벤토리]**(으)로 이동합니다.

![Analytics-Inventory-menu](assets/an-inventory-menu.png)

1. 기본 화면에는 Adobe Analytics 환경의 전체 인벤토리가 표시됩니다.

   ![기본 인벤토리 화면](assets/an_inventory.png)

>[!IMPORTANT]
>
>   이 초기 릴리스에서는 Workspace 프로젝트, 세그먼트, 계산된 지표, 고급(Media Analytics) 데이터 및 사용자에 대한 요약 번호를 볼 수 있습니다. 현재 실행 가능한 항목은 보고서 세트뿐입니다.


## 구성 요소 {#components}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-components"
>title="구성 요소"
>abstract="이 섹션에서는 Adobe Analytics 환경에 있는 프로젝트, 세그먼트 및 계산된 지표의 수를 보여 줍니다. 프로젝트와 구성 요소를 Customer Journey Analytics로 마이그레이션할 수 있습니다."

<!-- markdownlint-enable MD034 -->

이 초기 릴리스에서는 Workspace 프로젝트, 세그먼트 및 계산된 지표에 대한 요약 인벤토리 번호를 볼 수 있습니다. 후속 릴리스를 통해 이러한 구성 요소를 분석할 수 있습니다.

## 데이터 구성 및 수집 {#data-config}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-data-config"
>title="데이터 구성 및 수집"
>abstract="이 섹션에서는 Adobe Analytics 환경의 보고서 세트 수와 스트리밍 미디어에 대한 액세스 권한을 보여 줍니다. "

<!-- markdownlint-enable MD034 -->

### 보고서 세트 분석

1. 보고서 세트를 분석하고 마이그레이션할 보고서 세트를 결정하려면 **[!UICONTROL 데이터 구성 및 컬렉션]** > **[!UICONTROL 보고서 세트]**&#x200B;로 이동하고 **[!UICONTROL 분석]**&#x200B;을 클릭하십시오.

   ![보고서 세트 목록](assets/an_inv_rs.png)

   | 요소 | 설명 |
   | --- | --- |
   | 이름 | 보고서 세트의 이름 |
   | ID | 보고서 세트 ID(rsid)입니다. 영숫자만 포함한 고유 ID를 지정합니다. 이 ID는 생성하고 나면 변경할 수 없습니다. Adobe가 필수 ID 접두사를 설정하므로 어느 것도 변경할 수 없습니다. |
   | 발생 횟수 (최근 90일) |  |
   | 지표 | How |
   | 차원 |  |
   | A4T(Analytics for Target) 활성화됨 |  |
   | 마케팅 채널 활성화됨 |  |
   | Source 커넥터 활성화됨 | 팔로우 |
   | 캘린더 유형 | 자세한 내용은 [사용자 지정 달력](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/custom-calendar#)을 참조하세요. |

1. 주의:..

### CSV로 내보내기

1. 보고서 세트 목록을 .csv 파일로 내보내려면 **[!UICONTROL CSV로 내보내기]**&#x200B;를 클릭합니다.

1. 다운로드 폴더에 .csv 파일이 나타납니다.

1. 장치에서 스프레드시트 애플리케이션을 사용하여 열고 저장합니다.


## 사용자 관리 {#user-management}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-user-management"
>title="사용자 관리"
>abstract="이 섹션에서는 Adobe Analytics 환경의 사용자 수를 보여 줍니다."

<!-- markdownlint-enable MD034 -->

사용자 관리는 Analytics 인벤토리의 이후 릴리스에서 사용할 수 있습니다.