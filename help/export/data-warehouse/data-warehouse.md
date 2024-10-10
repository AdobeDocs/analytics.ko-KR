---
description: Data Warehouse는 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 정의 보고서에 대한 분석 데이터 사본을 의미합니다. 고유한 질문에 따라 원시 데이터의 고급 데이터 관계를 표시하는 보고서를 요청할 수 있습니다. Data Warehouse 보고서는 클라우드 스토리지 공급업체로 전송되거나 메일로 보내지며 처리하는 데 72시간까지 소요될 수 있습니다. 처리 시간은 쿼리의 복잡성과 요청된 데이터의 양에 따라 달라집니다.
title: Data Warehouse 개요
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
source-git-commit: 1e1a26b8595ca026fb049322125a6f91d9d5513c
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 100%

---

# Data Warehouse 개요

Data Warehouse를 사용하여 데이터를 필터링하여 실행할 수 있는 사용자 정의 보고서를 저장 및 만들기 위해 Adobe Analytics 데이터를 복사할 수 있습니다.

## 보고서 개요

Data Warehouse 보고서는 고유한 질문에 따라 원시 데이터의 고급 데이터 관계를 표시할 수 있습니다. (개별적으로 예약하고 다운로드한 보고서를) 한 번의 요청으로 행 수에 관계없이 포함할 수 있습니다.

>[!NOTE]
>
>Data Warehouse는 보고 기간에 발생한 첫 번째 값을 보고합니다.

>[!IMPORTANT]
>
>분류된 값을 구분하는 경우 Analysis Workspace 및 Data Warehouse는 &#39;지정되지 않음&#39; 값을 다르게 처리합니다. Workspace에서 &#39;지정되지 않음&#39;은 분류되지 않은 값을 나타내지만, Data Warehouse에서 &#39;지정되지 않음&#39;은 &#39;지정되지 않음&#39;으로 분류한 값을 나타냅니다.

## 게재 개요

Data Warehouse 보고서는 클라우드 스토리지 공급업체로 전송되거나 메일로 보내지며 처리하는 데 72시간까지 소요될 수 있습니다. 처리 시간은 쿼리의 복잡성과 요청된 데이터의 양에 따라 달라집니다.

Data Warehouse는 크기가 1MB를 초과하는 모든 파일을 자동으로 압축합니다. 최대 이메일 첨부 파일 크기는 10MB입니다.

## 액세스

Adobe는 관리자 수준 사용자에 대해서만 특정 보고서 세트에 대해 Data Warehouse를 사용할 수 있도록 합니다. (전체 및 하위 보고서 세트를 활성화할 수 있지만 롤업 보고서 세트는 활성화할 수 없습니다.) 관리자는 Data Warehouse에 대한 액세스 권한이 있는 그룹을 만든 다음 해당 그룹에 비관리자 수준의 사용자를 연결할 수 있습니다.

[Data Warehouse 권한 관리](/help/export/data-warehouse/t-dw-group.md)를 참조하십시오.

## Data Warehouse 요청 만들기

Data Warehouse 요청을 만드는 방법에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)를 참조하십시오.

## Data Warehouse 요청 관리

Data Warehouse 요청을 관리하는 방법에 대한 자세한 내용은 [Data Warehouse 요청 관리](/help/export/data-warehouse/data-warehouse-requests-manage.md)를 참조하십시오.

