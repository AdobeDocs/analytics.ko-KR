---
description: Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트를 마이그레이션하는 방법에 대해 설명합니다.
title: Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션
feature: Admin Tools
exl-id: 49c7e47a-464b-4465-9b30-d77f886ca6dc
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 5%

---

# Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션

Adobe Analytics 관리자는 Adobe Analytics 프로젝트 및 관련 구성 요소를 Customer Journey Analytics로 마이그레이션할 수 있습니다.

마이그레이션 프로세스에 포함된 사항:

* Customer Journey Analytics에서 Adobe Analytics 프로젝트를 다시 생성합니다.

* Adobe Analytics 보고서 세트의 차원 및 지표를 Customer Journey Analytics 데이터 보기의 차원 및 지표에 매핑합니다.

  일부 차원 및 지표는 자동으로 매핑되며, 다른 차원은 마이그레이션 프로세스의 일부로 수동으로 매핑해야 합니다. 세그먼트도 마이그레이션되지만 마이그레이션 프로세스의 일부로 매핑할 필요는 없습니다.

  마이그레이션이 완료되면 마이그레이션된 모든 구성 요소가 마이그레이션 요약에 표시됩니다.

## 마이그레이션 준비

프로젝트를 Customer Journey Analytics으로 마이그레이션하기 전에 [Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션 준비](/help/admin/admin/component-migration/prepare-component-migration.md).

## Adobe Analytics 프로젝트를 Customer Journey Analytics으로 마이그레이션

>[!IMPORTANT]
>
>이 섹션에 설명된 대로 프로젝트를 Customer Journey Analytics으로 마이그레이션하기 전에 [Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션 준비](/help/admin/admin/component-migration/prepare-component-migration.md).
>
>매핑하는 모든 차원 또는 지표는 이 프로젝트 및 전체 IMS 조직 전체에서 마이그레이션되는 향후 모든 프로젝트에 대해 영구적입니다. 마이그레이션이 완료된 후에는 모든 매핑을 수정할 수 없습니다.

1. Adobe Analytics에서 [!UICONTROL **관리**] 탭을 선택한 다음 [!UICONTROL **모든 관리자**]&#x200B;를 선택합니다.

1. 아래 [!UICONTROL **데이터 구성 및 수집**], 선택 [!UICONTROL **구성 요소 마이그레이션**].

1. 마이그레이션할 프로젝트를 찾습니다. 프로젝트 목록을 필터링, 정렬 또는 검색할 수 있습니다.

   기본적으로 사용자와 공유되는 프로젝트만 표시됩니다. 조직의 모든 프로젝트를 보려면 **필터** 아이콘, 확장 [!UICONTROL **기타 필터**] 및 선택 [!UICONTROL **모두 표시**]. 프로젝트 목록 필터링, 정렬 및 검색에 대한 자세한 내용은 [프로젝트 목록 필터링, 정렬 및 검색](#filter-sort-and-search-the-list-of-projects).)

1. 마이그레이션할 프로젝트 위로 마우스를 가져간 다음 **마이그레이션** 아이콘 ![프로젝트 마이그레이션](assets/migrate.svg).

   또는

   마이그레이션할 프로젝트를 선택한 다음 를 선택합니다. [!UICONTROL **Customer Journey Analytics으로 마이그레이션**].

   한 번에 하나의 프로젝트만 선택하여 마이그레이션할 수 있습니다.

   다음 [!UICONTROL **project_name을 Customer Journey Analytics으로 마이그레이션**] 대화 상자가 표시됩니다.

   <!-- add screenshot -->

1. 다음에서 [!UICONTROL **프로젝트 소유자**] 필드에서 Customer Journey Analytics에서 프로젝트 소유자로 설정할 사용자의 이름을 입력한 다음 드롭다운 메뉴에서 이름을 선택합니다.

   지정한 소유자는 프로젝트에 대한 모든 관리 권한을 가집니다.

1. 다음에서 [!UICONTROL **보고서 세트에 대한 스키마 매핑**] 섹션에서 보고서 세트를 선택합니다.

1. 다음에서 [!UICONTROL **데이터 보기**] 드롭다운 메뉴에서 프로젝트 및 구성 요소를 마이그레이션할 Customer Journey Analytics 데이터 보기 를 선택합니다.

1. 선택 [!UICONTROL **스키마 매핑**].

1. 다음에서 [!UICONTROL **스키마 매핑**] 섹션을 확장합니다. [!UICONTROL **Dimension**] 및 [!UICONTROL **지표**] 섹션.

   Adobe Analytics의 일부 차원 및 지표는 Customer Journey Analytics의 차원 또는 지표에 자동으로 매핑됩니다. 다른 도메인은 수동으로 매핑해야 합니다.

   **차원 및 지표 자동 매핑**

   >[!NOTE]
   >
   >   WebSDK를 사용하여 데이터를 Adobe Experience Platform으로 수집한 경우 차원 및 지표를 자동으로 매핑할 수 없습니다. 자세한 내용은 [전제 조건](/help/admin/admin/component-migration/prepare-component-migration.md#prerequisites) 위치: [Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션 준비](/help/admin/admin/component-migration/prepare-component-migration.md).

   Adobe Analytics의 일부 차원 및 지표는 Customer Journey Analytics의 차원 또는 지표에 자동으로 매핑됩니다. 이러한 차원 및 지표에 대해 매핑 결정을 내릴 수 없습니다.

   예를 들어 **방문 횟수** Adobe Analytics의 지표는 **세션** Customer Journey Analytics의 지표.

   차원 또는 지표를 선택하여 연결된 ID를 볼 수 있습니다.

   <!-- update screenshot after I can see the Status column -->

   ![프로젝트 마이그레이션 스키마](assets/project-migration-schema.png)

   **수동으로 차원 및 지표 매핑**

   Adobe Analytics의 일부 차원 및 지표는 Customer Journey Analytics의 차원 또는 지표에 자동으로 매핑될 수 없습니다.

   차원 또는 지표를 자동으로 매핑할 수 없는 경우 [!UICONTROL **Dimension**] 또는 [!UICONTROL **지표**] 수동으로 매핑해야 하는 차원 또는 지표의 수를 나타내는 섹션 헤더입니다. 표에서 경고 아이콘 ![경고 아이콘](assets/schema-warning.png) 수동으로 매핑해야 하는 각 차원 또는 지표 옆에 가 표시됩니다.

   또한 [!UICONTROL **상태**] 열 메시지 [!UICONTROL **매핑되지 않음**].

   <!-- update screenshot after I can see the Status column -->

   ![마이그레이션 스키마 수동 맵](assets/schema-manual-map.png)

1. 차원 및 지표를 수동으로 매핑하려면 경고 아이콘이 포함된 차원 또는 지표를 선택합니다 ![경고 아이콘](assets/schema-warning.png), 그런 다음 [!UICONTROL **매핑된 Customer Journey Analytics 지표**] 필드(또는 [!UICONTROL **매핑된 Customer Journey Analytics 차원**] 필드 (차원을 매핑하는 경우) 선택한 차원 또는 지표에 매핑할 Customer Journey Analytics의 차원 또는 지표를 선택합니다.

   ![차원 및 지표 매핑](assets/schema-manual-map-drop-down.png)

   차원 또는 지표가 매핑되면 경고 아이콘이 사라지고 [!UICONTROL **상태**] 열 변경 [!UICONTROL **매핑됨**] 녹색 점이 있는. (상태: [!UICONTROL **매핑됨**] 회색 점이 있는 것은 차원 또는 지표가 이전 마이그레이션 중에 매핑되었음을 나타냅니다. 이전 매핑은 업데이트할 수 없습니다.)

   경고 아이콘이 포함된 각 차원 또는 지표에 대해 이 프로세스를 반복합니다.

   Adobe Analytics 보고서 세트의 모든 차원과 지표가 Customer Journey Analytics 데이터 보기의 차원 또는 지표에 매핑되면 녹색 확인 표시가 나타납니다 ![확인 표시](assets/report-suite-check.png) 의 보고서 세트 이름 옆에 표시됩니다. [!UICONTROL **보고서 세트에 대한 스키마 매핑**] 섹션.

1. (조건부) 마이그레이션하는 프로젝트에 둘 이상의 보고서 세트가 포함되어 있는 경우 [!UICONTROL **보고서 세트에 대한 스키마 매핑**] 섹션, 단계 6 - 단계 10을 반복합니다. <!-- double-check that the step numbers are still correct -->

1. 선택 [!UICONTROL **마이그레이션**].

   >[!WARNING]
   >
   >   을 선택하면 화면에 경고 메시지가 표시됩니다. [!UICONTROL **마이그레이션**]. 계속하기 전에 매핑하는 차원 또는 지표가 이 프로젝트와 전체 조직에서 마이그레이션되는 향후 모든 프로젝트에 대해 영구적이라는 것을 알고 있어야 합니다. 계속하면 만든 매핑을 수정할 수 없습니다.

   마이그레이션이 완료된 후 [!UICONTROL **마이그레이션 상태**] 페이지 는 마이그레이션된 항목에 대한 요약을 제공합니다.

   마이그레이션이 실패하면 [실패한 마이그레이션 다시 시도](#retry-a-failed-migration) 자세한 내용은 아래 섹션을 참조하십시오.

## 실패한 마이그레이션 다시 시도

마이그레이션이 실패하면 마이그레이션을 다시 시도할 수 있습니다.

실패한 마이그레이션을 다시 시도하기 전에 다음을 제거해야 합니다. [지원되지 않는 요소](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html#understand-unsupported-elements-that-cause-errors) 프로젝트에서 가져왔습니다.

>[!NOTE]
>
>마이그레이션을 다시 시도한 후에도 계속 실패하는 경우 프로젝트 ID를 사용하여 고객 지원 센터에 문의하십시오. 프로젝트 ID는 마이그레이션 상태 페이지에서 찾을 수 있습니다. <!-- when does this page display? How can they get there -->

실패한 마이그레이션을 다시 시도하려면 다음 작업을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **관리**] 탭을 선택한 다음 [!UICONTROL **모든 관리자**]&#x200B;를 선택합니다.

1. 아래 [!UICONTROL **데이터 구성 및 수집**], 선택 [!UICONTROL **구성 요소 마이그레이션**].

1. 선택 [!UICONTROL **실패**] 다음에서 [!UICONTROL **마이그레이션 상태**] 다시 시도할 프로젝트 옆에 있는 열입니다.

   ![마이그레이션 상태 열 실패](assets/migration-failed.png)

   다음 [!UICONTROL **마이그레이션 상태**] 페이지가 표시됩니다.

   또한 이 페이지는 섹션에 설명된 마이그레이션 단계를 완료한 직후에 표시됩니다 [Adobe Analytics 프로젝트를 Customer Journey Analytics으로 마이그레이션](#migrate-adobe-analytics-projects-to-customer-journey-analytics) 위.

1. 선택 [!UICONTROL **마이그레이션 다시 시도**].

## 프로젝트 목록 필터링, 정렬 및 검색

구성 요소 마이그레이션 페이지에서 프로젝트 목록을 필터링, 정렬 및 검색할 수 있습니다.

### 프로젝트 목록 필터링

다음 기준으로 필터링할 수 있습니다.

| 필터 | 설명 |
|---------|----------|
| [!UICONTROL **상태**] | 마이그레이션 상태: <ul><li>[!UICONTROL **시작되지 않음**]</li><li>[!UICONTROL **시작됨**]</li><li>[!UICONTROL **완료됨**]</li><li>[!UICONTROL **실패**]</li></ul>. |
| [!UICONTROL **태그**] | 태그 목록에서 태그를 선택합니다. 선택한 태그가 적용된 프로젝트만 표시됩니다. |
| [!UICONTROL **보고서 세트**] | 보고서 세트 목록에서 보고서 세트를 선택합니다. 선택한 보고서 세트를 사용하는 프로젝트만 표시됩니다. |
| [!UICONTROL **소유자**] | 소유자 목록에서 소유자를 선택합니다. 선택한 사용자가 소유한 프로젝트만 표시됩니다. |
| [!UICONTROL **기타 필터**] | 다음과 같은 추가 필터를 사용할 수 있습니다. <ul><li>[!UICONTROL **내**]: 자신이 소유자로 설정된 프로젝트만 표시합니다.</li><li>[!UICONTROL **나와 공유됨**]: 사용자와 공유된 프로젝트만 표시합니다.</li><li>[!UICONTROL **즐겨찾기**]: 즐겨찾기로 표시된 프로젝트만 표시합니다. (다음에서 프로젝트를 즐겨찾기로 표시할 수 있음) [프로젝트 랜딩 페이지](/help/analyze/landing.md).)</li><li>[!UICONTROL **월별**]</li><li>[!UICONTROL **연간**]</li></ul> |

{style="table-layout:auto"}

### 프로젝트 목록 정렬

모든 열을 기준으로 프로젝트 목록을 정렬할 수 있습니다.

프로젝트 목록을 정렬하려면

1. 정렬 기준으로 사용할 열의 열 머리글을 선택합니다.

1. (선택 사항) 정렬 순서를 반대로 하려면 동일한 열 헤더를 다시 선택합니다.

### 프로젝트 검색

구성 요소 마이그레이션 페이지에서 프로젝트 목록을 검색하여 마이그레이션하려는 프로젝트를 찾을 수 있습니다.

1. 구성 요소 마이그레이션 페이지 상단의 검색 필드에서 마이그레이션하려는 프로젝트의 이름을 입력하십시오.

1. 드롭다운 메뉴에 표시될 때 프로젝트를 선택합니다.

<!-- is there going to be a way to customize the columns that are displayed? -->
