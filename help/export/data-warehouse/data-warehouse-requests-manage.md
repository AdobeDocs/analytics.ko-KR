---
description: 요청 관리자에서 요청을 보고, 복제하고, 요청의 우선순위를 변경할 수 있습니다.
title: Data Warehouse 요청 관리
feature: Data Warehouse
uuid: cdeb764f-56f9-43ec-9228-8ed5a2b58909
exl-id: a399d366-8402-4f4f-9b9f-14b218cd074a
source-git-commit: 8507ce3f7e4d09956ad88c2be5335b68c8e3b8a0
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 18%

---

# Data Warehouse 요청 관리

{{release-limited-testing}}

>[!NOTE]
>
>모든 고객이 곧 사용할 수 있는 새로운 Data Warehouse 경험이 조직에 아직 없는 경우 의 정보를 사용하십시오. [Data Warehouse 요청 관리(이전 경험)](#manage-data-warehouse-requests-old-experience)


수행한 Data Warehouse 요청을 관리할 수 있습니다. 다음 섹션에서는 요청을 관리할 때 수행할 수 있는 활동에 대해 설명합니다. <!-- just those you have made? I think you can see other people's requests (you can filter by them). What can you do with other people's requests? Just view them?-->

## 요청 보기

1. Adobe Analytics에서 [!UICONTROL **도구**] > [!UICONTROL **Data Warehouse**].

   Data Warehouse 페이지에는 수행한 모든 요청이 표시됩니다. <!-- just those you have made? -->데이터는 각 열에 표시됩니다. 다음을 수행할 수 있습니다. [열 구성](#configure-columns) 표시됩니다.

   <!-- add screenshot of main page -->

<!-- describe columns? -->

1. (선택 사항) 다음 정보를 표시하는 대화 상자를 보려면 요청 이름을 클릭합니다. <!-- Check this -->

   * 요청 처리가 시작된 시기

   * 제한적 평가: 조직에서 실행 중인 Data Warehouse 요청이 너무 많습니다. 다른 데이터 요청이 완료될 때까지 요청이 일시 중지됩니다.

## 요청 편집

요청을 편집할 때 다음 사항을 고려하십시오.

* 일정에 따라 실행되도록 구성된 요청만 편집할 수 있습니다.

* 요청과 연결된 일부 필드는 편집할 수 없습니다. 편집할 수 없는 필드는 흐리게 표시됩니다.

예약된 요청을 편집하려면:

1. Adobe Analytics에서 [!UICONTROL **도구**] > [!UICONTROL **Data Warehouse**].

1. Data Warehouse 페이지에서 편집할 요청을 선택합니다.

   ![요청 관리](assets/dw-manage-request.png)

1. 선택 [!UICONTROL **편집**].

1. 원하는 대로 요청을 편집합니다. 흐리게 표시된 구성 옵션은 편집할 수 없습니다.

   각 구성 옵션에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. 선택 [!UICONTROL **변경 내용 저장**].

## 요청 내역 보기

실행된 보고서의 내역을 볼 수 있습니다.

1. Adobe Analytics에서 [!UICONTROL **도구**] > [!UICONTROL **Data Warehouse**].

1. Data Warehouse 페이지에서 내역을 보려는 요청을 선택합니다.

   ![요청 관리](assets/dw-manage-request.png)

1. 선택 [!UICONTROL **내역 보기**].

## 요청 복사

요청을 복사하면 모든 구성 옵션이 원래 요청에서 복사됩니다.

1. Adobe Analytics에서 [!UICONTROL **도구**] > [!UICONTROL **Data Warehouse**].

1. Data Warehouse 페이지에서 복사할 요청을 선택합니다.

   ![요청 관리](assets/dw-manage-request.png)

1. 선택 [!UICONTROL **복사**].

   Data Warehouse 요청 복사 페이지가 표시됩니다. 모든 구성 옵션이 원래 요청에서 복사됩니다.

1. 요청과 연결된 모든 구성 옵션을 업데이트합니다.

   각 구성 옵션에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. 선택 [!UICONTROL **변경 내용 저장**].

## 요청 취소

일정에 따라 실행되도록 구성된 요청만 취소할 수 있습니다.

예약된 요청을 취소하려면 다음 작업을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **도구**] > [!UICONTROL **Data Warehouse**].

1. Data Warehouse 페이지에서 편집할 요청을 선택합니다.

   ![요청 관리](assets/dw-manage-request.png)

1. 선택 [!UICONTROL **취소**].

   예약된 시간에 요청이 더 이상 실행되지 않습니다.

## 열 구성

열을 추가하거나 제거하여 각 요청에 대해 표시되는 정보를 구성할 수 있습니다.

1. 다음 항목 선택 **열 구성** Data Warehouse 페이지의 오른쪽 상단에 있는 아이콘입니다.

   ![열 구성](assets/dw-configure-columns.png)

   다음 열을 사용할 수 있습니다.

   | 사용 가능한 열 | 설명 |
   |---------|----------|
   | 요청 이름 | 요청을 만든 사람의 이름입니다. |
   | 보고서 세트 | 요청과 연결된 보고서 세트입니다. |
   | 요청자 | 요청을 만든 사용자입니다. |
   | 요청 일자 | 요청이 수행된 날짜. |
   | 상태 | 다음 상태를 사용할 수 있습니다.<ul><li><p>**완료됨**: 요청이 정상적으로 실행되었습니다.</p></li><li><p>**취소됨**: 사용자가 요청을 취소했습니다.</p></li><li><p>**예약됨**: 요청이 일정에 따라 실행되도록 구성되었습니다.</p></li><!-- Are there other statuses? Failed? --> |

   {style="table-layout:auto"}

1. 표시할 열이 선택되어 있는지 확인합니다. 선택한 열이 Data Warehouse 페이지에 나타나고 관련 정보가 표시됩니다.

## 요청 필터링 및 정렬

1. 다음 항목 선택 **필터** 아이콘: Data Warehouse 페이지의 왼쪽 레일에 있습니다.

   ![요청 필터링](assets/dw-filter.png)

1. 확장 [!UICONTROL **보고서 세트**], [!UICONTROL **소유자**], 또는 [!UICONTROL **상태**] 섹션을 선택한 다음 요청을 필터링하는 방법을 선택합니다.

## 요청 검색

1. Data Warehouse 페이지 상단의 검색 필드에서 보려는 요청 이름을 지정합니다.

   요청은 사용자가 입력하는 대로 필터링됩니다.

## Data Warehouse 요청 관리(이전 경험)

>[!NOTE]
>
>다음 정보는 조직에 모든 Analytics 고객이 곧 사용할 수 있는 새로운 Data Warehouse 경험이 아직 없는 경우에만 적용됩니다.


요청 관리자에서 요청을 보고, 복제하고, 요청의 우선순위를 변경할 수 있습니다.

Data Warehouse에서 **[!UICONTROL 요청 관리자]** 탭을 선택합니다.

이 탭에서 작업할 때 가능한 사항

* 보고서 이름, 적용된 세그먼트, 요청자, 요청 날짜 및 상태별로 최근 보고서 요청 보기.
* 요청 복제. 요청 옆에 있는 **[!UICONTROL 복제]**&#x200B;를 클릭합니다.

  >[!NOTE]
  >
  >이 작업에서는 일정이나 배달 세부 정보는 복제되지 않고 요청만 복제됩니다.

* 보고서 이름이나 요청자의 로그인 이름을 사용한 보고서 검색.
* 큐 내의 새 위치로 보고서를 드래그해다 놓는 방법으로 보고서 우선 순위 변경.
* 요청 처리가 언제 시작되었는지 보려면 예약된 요청 ID를 클릭하고 열리는 팝업을 확인합니다.

해당 작업에 대한 개별 요청을 보려면 작업을 클릭합니다.

* 제한적 평가: 조직에서 실행 중인 Data Warehouse 요청이 너무 많습니다. 다른 데이터 요청이 완료될 때까지 요청이 일시 중지됩니다.