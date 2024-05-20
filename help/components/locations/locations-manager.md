---
description: 분류 데이터를 업로드할 수 있는 클라우드 가져오기 계정 및 위치를 구성합니다.
keywords: Analysis Workspace
title: 위치 관리자
feature: Classifications
exl-id: ace70568-220a-44e8-8e5f-f73002b9e2a2
source-git-commit: 273fea86cde8880d9c9e03ac9c6a99b75f70f6cd
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 1%

---

# 위치 관리자

위치 관리자를 사용하여 계정 및 위치를 보거나, 만들거나, 편집하거나, 삭제할 수 있습니다. 다음 용도로 사용할 수 있습니다.

* 다음을 사용하여 파일 내보내기 [데이터 피드](/help/export/analytics-data-feed/create-feed.md)
* 를 사용하여 보고서 내보내기 [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* 을 사용하여 스키마 가져오기 [분류 세트](/help/components/classifications/sets/overview.md)

## 위치 보기, 필터링 및 검색

위치 관리자를 사용하여 생성한 모든 위치를 볼 수 있습니다. 시스템 관리자는 모든 사용자가 만든 위치를 볼 수 있습니다.

1. Adobe Analytics에서 위치 관리자에 액세스하려면 다음을 선택합니다. **[!UICONTROL 구성 요소]** > **[!UICONTROL 위치]**.

1. (조건부) 시스템 관리자인 경우 [!UICONTROL **모든 사용자의 위치 보기**] 조직의 모든 사용자가 만든 위치를 보는 옵션입니다. <!-- Maybe add a screenshot? This is new functionality -->

1. 위치 목록을 필터링하거나 검색합니다.

   * **필터:** 필터 아이콘을 선택하여 위치 목록을 필터링합니다.

     다음 기준으로 위치를 필터링할 수 있습니다. **[!UICONTROL 위치 유형]**, **[!UICONTROL 계정]**, 또는 **[!UICONTROL 작성자:]**.

     ![위치 필터](assets/locations-filters.png)

   * **검색:** 검색 필드에서 보려는 위치의 이름을 입력하십시오. 입력한 대로 결과가 필터링됩니다. 다음 열이 검색됩니다. **위치 이름**, **위치 유형**, **계정**, 및 **작성자:**.

1. (선택 사항) 위치가 1,000개를 초과하는 경우 처음 1,000개만 표시됩니다. 선택 [!UICONTROL **추가 로드**] 1,000개의 위치를 더 로드합니다.

## 위치 관리자에서 열 구성

위치 관리자에서 다음 열을 사용할 수 있습니다. 테이블에 표시되는 열을 사용자 정의하려면 **표 맞춤화** 아이콘 ![표 맞춤화 아이콘](assets/customize-table-icon.png).

* **[!UICONTROL 위치 이름]**: 위치 이름입니다. 위치 이름 옆에 있는 3점 메뉴를 선택하여 다음 중 하나를 수행합니다. [위치 편집](/help/components/locations/configure-import-locations.md) 또는 삭제합니다.
* **[!UICONTROL 위치 유형]**: 위치와 연결된 계정 유형입니다.
* **[!UICONTROL 계정]**: 위치와 연결된 특정 계정입니다.
* **애플리케이션**: 위치를 사용할 수 있는 애플리케이션 유형(예: 데이터 피드, Data Warehouse 또는 분류 세트)입니다.
* **[!UICONTROL 마지막으로 사용한 날짜]**: 위치를 마지막으로 사용한 날짜입니다.
* **[!UICONTROL 작성자:]**: 위치를 만든 사용자입니다.
* **[!UICONTROL 만든 날짜]**: 위치가 생성된 날짜입니다.

## 위치 만들기 및 관리

위치를 생성, 편집 및 삭제할 수 있습니다.

### 위치 만들기

위치를 만드는 방법에 대한 자세한 내용은 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md).

<!-- Do I need to add some steps here about how to create a location and then assign that location to be used with DF, DW, or Classifications sets? Need to hear back from Ron and team whether we are including this functionality -->

### 위치 편집

위치를 편집하는 방법에 대한 자세한 내용은 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md).

### 위치 삭제

>[!IMPORTANT]
>
>위치가 삭제되면 삭제된 위치와 연결된 데이터 피드 파일, Data Warehouse 보고서 또는 분류 세트 스키마를 다음에 사용할 때 실패합니다.
>
>위치를 삭제하면 다음과 같은 결과가 발생합니다 [데이터 피드 편집](/help/export/analytics-data-feed/create-feed.md), [Data Warehouse 보고서](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), 및 [분류 세트 스키마](/help/components/classifications/sets/manage/schema.md) 작동 중인 위치를 사용합니다.

Adobe Analytics에서 위치 관리자에서 위치를 삭제하려면 다음을 수행하십시오.

1. 선택 **[!UICONTROL 구성 요소]** > **[!UICONTROL 위치]**&#x200B;을(를) 선택한 다음 [!UICONTROL **위치**] 탭.

1. 에서 3점 메뉴를 선택합니다. [!UICONTROL **위치 이름**] 삭제할 위치에 대한 열입니다.

1. [!UICONTROL **삭제**]&#x200B;를 선택합니다.

## 계정 편집

1. Adobe Analytics의 위치 관리자에서 계정을 편집하려면 다음을 선택합니다. **[!UICONTROL 구성 요소]** > **[!UICONTROL 위치]**&#x200B;을(를) 선택한 다음 [!UICONTROL **위치 계정**] 탭.

1. (조건부) 시스템 관리자인 경우 [!UICONTROL **모든 사용자의 계정 보기**] 조직의 모든 사용자가 만든 위치를 보는 옵션입니다. <!-- Maybe add a screenshot? This is new functionality -->


1. 선택 [!UICONTROL **세부 정보 보기**] 편집할 계정에 대해 설명합니다.

1. 원하는 대로 변경한 다음, [!UICONTROL **저장**].

## 계정 키 보기

계정을 만든 후 해당 계정에 대해 연결된 계정 키를 볼 수 있습니다. 클라우드 공급자와의 계정 구성을 완료하지 않은 경우 이 정보를 확인해야 할 수 있습니다. [원래 구성된 계정](/help/components/locations/configure-import-accounts.md).

내보내기 계정과 연결된 키를 보려면 다음과 같이 하십시오.

1. Adobe Analytics에서 **[!UICONTROL 구성 요소]** > **[!UICONTROL 위치]**&#x200B;을(를) 선택한 다음 [!UICONTROL **위치 계정**] 탭.

1. 편집할 계정의 3점 아이콘을 선택한 다음 을 선택합니다 [!UICONTROL **계정 키**].

## 계정 삭제

1. Adobe Analytics에서 **[!UICONTROL 구성 요소]** > **[!UICONTROL 위치]**&#x200B;을(를) 선택한 다음 [!UICONTROL **위치 계정**] 탭.

1. 편집할 계정의 3점 아이콘을 선택한 다음 을 선택합니다 [!UICONTROL **계정 삭제**]
