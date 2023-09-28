---
description: Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트를 마이그레이션하는 방법에 대해 설명합니다.
title: Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션
feature: Admin Tools
source-git-commit: 73cbfbbad4d8e7bb3107ee08861a6342aba85e84
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 9%

---

# Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션

Adobe Analytics 관리자는 Adobe Analytics 구성 요소 및 프로젝트를 Customer Journey Analytics으로 마이그레이션할 수 있습니다.

마이그레이션 프로세스에는 다음이 포함됩니다.

* Customer Journey Analytics에서 Adobe Analytics 프로젝트 다시 만들기

* Adobe Analytics 보고서 세트의 차원과 지표를 Customer Journey Analytics 데이터 보기의 차원과 지표에 일치시킵니다.

  일부 차원과 지표는 자동으로 일치합니다. 다른 차원과 지표는 마이그레이션 프로세스의 일부로 수동으로 일치해야 합니다.

## 마이그레이션 준비

### 사전 요구 사항

프로젝트와 관련 차원 및 지표를 마이그레이션할 준비가 되기 전에 먼저 다음을 수행해야 합니다.

* Analytics 소스 커넥터를 사용하여 Customer Journey Analytics에서 Adobe Analytics 보고서 세트 데이터를 볼 수 있습니다. 이를 위해서는 다음을 수행해야 합니다.

   * [Adobe Experience Platform 및 Customer Journey Analytics에 수집하기 위한 보고서 세트 설정](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

   * [데이터 수집 및 사용](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html?lang=ko-KR)

* Customer Journey Analytics의 사용자가 데이터가 일치하는 데이터 보기에 프로비저닝되었는지 확인합니다.

  자세한 내용은 [Admin Console에서 권한 Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) 위치: [Customer Journey Analytics 액세스 제어](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  권한 탭은 Admin Console 각 제품 프로필의 일부입니다. 특정 제품 프로필에 사용자를 추가할 수 있습니다. 그 다음 특정 데이터 보기에 대한 권한을 할당하고 제품 프로필의 사용자에게 부여할 권한을 지정합니다.

* 아래 섹션에 설명된 대로 마이그레이션 계획을 만듭니다. [조직으로 마이그레이션 계획 만들기](#create-a-migration-plan-as-an-organization).

### 마이그레이션에 포함된 내용 이해

다음 표에서는 마이그레이션에 포함된 프로젝트 및 구성 요소의 요소를 간략하게 설명합니다.


|  | 프로젝트 | Dimension 및 지표 |
|---------|----------|---------|
| **날짜 범위** | 예 | 해당 사항 없음 |
| **세그먼트** | 예 | 해당 사항 없음 |
| **빠른 세그먼트** | 예 | 해당 사항 없음 |
| **패널** | 예 | 해당 사항 없음 |
| **시각화** | 예 | 해당 사항 없음 |
| **소유자** | (마이그레이션을 수행하는 사용자에 의해 정의됨) | ? |
| **큐레이션** | 아니요 | 해당 없음 |
| **공유(프로젝트 역할)** | 아니요 | 아니요 |
| **주석** | 아니요 | 해당 없음 |
| **폴더 구조** | 아니요 | 해당 없음 |
| **설명** | 예 | ? |
| **태그** | ? | ? |
| **일정** | ? | 해당 사항 없음 |
| **속성(차원)** | 해당 사항 없음 | ? |
| **예외 항목 탐지** | ? | 해당 사항 없음 |
| **기여도 분석** | ? | 해당 사항 없음 |
| **경고** | ? | 해당 사항 없음 |

{style="table-layout:auto"}

### 조직으로 마이그레이션 계획 만들기

주어진 프로젝트 마이그레이션에 대해 일치하는 모든 구성 요소는 향후 전체 조직의 프로젝트 마이그레이션에 적용되므로 조직에서 모든 프로젝트 마이그레이션을 미리 계획하는 것이 중요합니다.

조직에서는 프로젝트 마이그레이션 시 개별 관리자가 사일로에서 결정을 내리지 않도록 일치하는 항목과 일치하는 차원 및 지표를 결정해야 합니다.

## Adobe Analytics 프로젝트를 Customer Journey Analytics으로 마이그레이션

>[!IMPORTANT]
>
>이 섹션에 설명된 대로 프로젝트를 Customer Journey Analytics으로 마이그레이션하기 전에 [마이그레이션 계획](#plan-the-migration) 위의 섹션.
>
>일치하는 모든 차원 또는 지표는 이 프로젝트와 전체 조직에서 마이그레이션되는 향후 모든 프로젝트에 대해 영구적입니다. 일치하는 항목은 수정할 수 없습니다.



1. Adobe Analytics에서 [!UICONTROL **관리자**] 탭을 선택한 다음 를 선택합니다 [!UICONTROL **모든 관리자**].

1. 아래 [!UICONTROL **데이터 구성 및 수집**], 선택 [!UICONTROL **구성 요소 마이그레이션**].

1. (조건부) 마이그레이션할 프로젝트를 빨리 찾으려면 다음 중 하나를 수행할 수 있습니다.

   * 필터 아이콘을 선택하여 프로젝트 목록을 필터링합니다.

     다음 기준으로 필터링할 수 있습니다.

      * 상태

      * 태그

      * 보고서 세트

      * 소유자

      * 기타 필터

   * 검색 필드를 사용하여 마이그레이션할 프로젝트를 검색합니다.

1. 마이그레이션할 프로젝트 위로 마우스를 가져간 다음 **마이그레이션** 아이콘 ![프로젝트 마이그레이션](assets/migrate.svg).

   또는

   마이그레이션할 프로젝트를 선택한 다음 를 선택합니다. [!UICONTROL **Customer Journey Analytics으로 마이그레이션**].

   한 번에 하나의 프로젝트만 선택하여 마이그레이션할 수 있습니다.

   다음 [!UICONTROL **project_name을 Customer Journey Analytics으로 마이그레이션**] 대화 상자가 표시됩니다.

   <!-- add screenshot -->

1. 다음에서 [!UICONTROL **프로젝트 소유자**] 필드에서 Customer Journey Analytics에서 프로젝트 소유자로 설정할 사용자의 이름을 입력한 다음 드롭다운 메뉴에서 이름을 선택합니다.

   지정한 소유자는 프로젝트에 대한 모든 관리 권한을 가집니다.

1. 다음에서 [!UICONTROL **보고서 세트에 대한 일치 스키마**] 섹션에서 보고서 세트를 선택합니다.

1. 다음에서 [!UICONTROL **데이터 보기**] 드롭다운 메뉴에서 프로젝트 및 구성 요소를 마이그레이션할 Customer Journey Analytics 데이터 보기 를 선택합니다.

1. 선택 [!UICONTROL **스키마 일치**].

1. 다음에서 [!UICONTROL **스키마 일치**] 섹션을 확장합니다. [!UICONTROL **Dimension**] 및 [!UICONTROL **지표**] 섹션.

   Adobe Analytics의 일부 차원 및 지표는 Customer Journey Analytics의 차원 또는 지표에 자동으로 일치합니다. 다른 항목은 수동으로 일치시켜야 합니다.

   **자동으로 일치하는 차원 및 지표**

   Adobe Analytics의 일부 차원 및 지표는 Customer Journey Analytics의 차원 또는 지표에 자동으로 일치합니다. 이러한 차원 및 지표에 대해 일치하는 결정을 내릴 수 없습니다.

   예를 들어 **방문 횟수** Adobe Analytics의 지표는 **세션** Customer Journey Analytics의 지표.

   차원 또는 지표를 선택하여 연결된 ID를 볼 수 있습니다.

   <!-- update screenshot after I can see the Status column -->

   ![프로젝트 마이그레이션 스키마](assets/project-migration-schema.png)

   **수동으로 차원 및 지표 일치**

   Adobe Analytics의 다른 차원 및 지표는 Customer Journey Analytics의 차원 또는 지표와 자동으로 일치할 수 없습니다.

   차원 또는 지표를 자동으로 일치시킬 수 없는 경우 [!UICONTROL **Dimension**] 또는 [!UICONTROL **지표**] 수동으로 일치시켜야 하는 차원 또는 지표의 수를 나타내는 섹션 헤더입니다. 표에서 경고 아이콘 ![경고 아이콘](assets/schema-warning.png) 수동으로 일치시켜야 하는 각 차원 또는 지표 옆에 이 표시됩니다.

   <!-- update screenshot after I can see the Status column -->

   ![마이그레이션 스키마 수동 일치](assets/schema-manual-map.png)

1. 차원 및 지표를 수동으로 일치시키려면 경고 아이콘이 포함된 차원 또는 지표를 선택합니다 ![경고 아이콘](assets/schema-warning.png), 그런 다음 [!UICONTROL **일치하는 Customer Journey Analytics 지표**] 필드(또는 [!UICONTROL **일치하는 Customer Journey Analytics 차원**] Customer Journey Analytics과 일치하는 경우) 선택한 차원 또는 지표와 일치시킬 차원 또는 지표를 차원에서 선택합니다.

   ![차원 및 지표 일치](assets/schema-manual-map-drop-down.png)

   경고 아이콘이 포함된 각 차원 또는 지표에 대해 이 프로세스를 반복합니다.

   Adobe Analytics 보고서 세트의 모든 차원 및 지표가 Customer Journey Analytics 데이터 보기의 차원 또는 지표와 일치하면 녹색 확인 표시가 나타납니다 ![확인 표시](assets/report-suite-check.png) 의 보고서 세트 이름 옆에 표시됩니다. [!UICONTROL **보고서 세트에 대한 일치 스키마**] 섹션.

1. (조건부) 마이그레이션하는 프로젝트에 둘 이상의 보고서 세트가 포함되어 있는 경우 [!UICONTROL **보고서 세트에 대한 일치 스키마**] 섹션, 단계 6 - 단계 10을 반복합니다. <!-- double-check that the step numbers are still correct -->

1. 선택 [!UICONTROL **마이그레이션**].

   >[!WARNING]
   >
   >   을 선택하면 화면에 경고 메시지가 표시됩니다. [!UICONTROL **마이그레이션**]. 계속하기 전에, 이 프로젝트와 전체 조직에 걸쳐 마이그레이션되는 향후 모든 프로젝트에 대해 일치하는 모든 차원 또는 지표가 영구적이라는 것을 이해하십시오. 계속하면 일치하는 항목을 수정할 수 없습니다.
