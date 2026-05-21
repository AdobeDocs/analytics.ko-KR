---
description: Data Warehouse에 대해 알아보고 데이터를 필터링하여 사용자 정의 보고서를 만들고 실행하는 방법에 대해 알아봅니다.
title: Data Warehouse 개요
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
TQID: https://experienceleague.adobe.com/Vkn9mWvBzaiIBf1KYIEUK8cRwTuzw41MT-v-thMBg38
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: e3e906cf-5493-4e0a-9a33-bf0ac37393d6id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 86%

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

Adobe는 관리자 수준 사용자에 대해서만 특정 보고서 세트에 대해 Data Warehouse를 사용할 수 있도록 합니다. 글로벌 및 하위 보고서 세트에 대해 활성화할 수 있지만, 롤업 보고서 세트에 대해서는 활성화할 수 없습니다. 관리자는 Data Warehouse에 액세스할 수 있는 그룹을 만든 다음 관리자가 아닌 수준 사용자를 해당 그룹에 연결할 수 있습니다.

[Data Warehouse 권한 관리](/help/export/data-warehouse/t-dw-group.md)를 참조하십시오.

## Data Warehouse 요청 만들기

Data Warehouse 요청을 만드는 방법에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)를 참조하십시오.

## Data Warehouse 요청 관리

Data Warehouse 요청을 관리하는 방법에 대한 자세한 내용은 [Data Warehouse 요청 관리](/help/export/data-warehouse/data-warehouse-requests-manage.md)를 참조하십시오.

