---
title: 데이터 피드 관리
description: 데이터 피드 인터페이스를 탐색하는 방법을 알아봅니다. 데이터 피드를 만들고, 편집하고, 보는 방법을 알아봅니다.
feature: Data Feeds
exl-id: 4d4f0062-e079-48ff-9464-940c6425ad54
source-git-commit: 5bf3f561c471410e4ce1ca576ba34ea3849b0325
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 21%

---

# 데이터 피드 관리

데이터 피드 관리자는 조직의 데이터 피드를 생성, 편집 및 삭제할 수 있도록 해 줍니다. 데이터 피드 관리자에 액세스할 수 있는 권한이 있으면 표시되는 모든 보고서 세트에 대한 데이터 피드를 관리할 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [데이터 피드 관리](https://video.tv.adobe.com/v/3428565?quality=12&learn=on&captions=kor){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]


## 데이터 피드 보기

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
1. 오른쪽 상단의 9제곱 아이콘을 선택한 다음 [!UICONTROL **Analytics**]&#x200B;을 선택합니다.
1. 상단 탐색 모음에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**] (으)로 이동합니다.

   액세스 권한이 있는 모든 보고서 세트에 대한 데이터 피드가 표시됩니다. 또는 구성된 피드가 없는 경우 페이지에 [!UICONTROL 새 데이터 피드 만들기] 단추가 표시됩니다.

   ![데이터 피드](assets/feeds.png)

## 데이터 피드 만들기

[!UICONTROL 추가] 단추를 사용하면 새 피드를 만들 수 있습니다. 자세한 내용은 [데이터 피드 만들기](create-feed.md)를 참조하십시오.

## 데이터 피드 편집

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 편집할 데이터 피드를 찾습니다. 데이터 피드를 찾으려면 [데이터 피드 목록을 필터링하고 검색](#filter-and-search-the-list-of-data-feeds)할 수 있습니다.

1. [!UICONTROL **피드 이름**] 열에서 데이터 피드를 선택하십시오.

1. 데이터 피드를 원하는 대로 변경합니다.

   편집 중인 데이터 피드에 대한 [!UICONTROL **대상**] 섹션을 업데이트할 때 [!UICONTROL **계정**] 및 [!UICONTROL **위치**] 드롭다운 필드에서 새 데이터 피드에 사용할 다른 계정 및 위치를 선택할 수 있습니다.

   [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 계정 및 위치를 편집할 수 있습니다. 계정 또는 위치를 편집하면 해당 계정 또는 위치와 연결된 모든 항목에 영향을 줍니다.

   이전 버전의 데이터 피드 관리자를 사용하면 FTP, SFTP, S3 및 Azure Blob 대상을 만들 수 있습니다. 이러한 이전 버전의 데이터 피드 관리자에서 생성된 대상은 편집하거나 복사할 수 없습니다.

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

## 데이터 피드 목록 필터링 및 검색

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 검색 또는 필터를 사용하여 특정 피드를 찾습니다.

   * 검색 필드에서 피드 이름을 입력하세요. 일치하는 피드만 사용 가능한 피드 목록에 표시됩니다.

   * 맨 왼쪽에서 필터 아이콘을 클릭하여 필터링 옵션을 표시하거나 숨깁니다. 필터는 범주별로 구성되어 있습니다. 필터링 범주를 축소하거나 확장할 수 있습니다. 적용할 필터 옆의 확인란을 선택합니다.

![필터](assets/filters.png)

## 데이터 피드 작업 보기

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 각 피드가 만드는 개별 작업을 보려면 [!UICONTROL **작업**] 탭을 선택하십시오.

   또는

   특정 데이터 피드에 대한 작업을 보려면 하나 이상의 데이터 피드 옆에 있는 확인란을 선택한 다음 [!UICONTROL **작업 기록**]&#x200B;을 선택하십시오.

   자세한 내용은 [데이터 피드 작업 관리](df-manage-jobs.md)를 참조하십시오.

## 데이터 피드 복사

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 복사할 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **복사**]&#x200B;를 선택합니다.

   현재 피드의 모든 설정을 사용하여 [새 피드를 만들기](create-feed.md)합니다. 두 개 이상의 데이터 피드를 선택한 경우에는 이 옵션이 표시되지 않습니다.

   복사하는 데이터 피드에 대한 [!UICONTROL **대상**] 섹션을 업데이트할 때 [!UICONTROL **계정**] 및 [!UICONTROL **위치**] 드롭다운 필드에서 새 데이터 피드에 사용할 다른 계정 및 위치를 선택할 수 있습니다.

   [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 계정 및 위치를 편집할 수 있습니다. 계정 또는 위치를 편집하면 해당 계정 또는 위치와 연결된 모든 항목에 영향을 줍니다.

   이전 버전의 데이터 피드 관리자를 사용하면 FTP, SFTP, S3 및 Azure Blob 대상을 만들 수 있습니다. 이러한 이전 버전의 데이터 피드 관리자에서 생성된 대상은 편집하거나 복사할 수 없습니다.

## 데이터 피드 일시 중지

데이터 피드를 일시 중지하면 피드 처리가 중지되어 피드 상태가 [!UICONTROL 비활성]&#x200B;(으)로 설정됩니다.

피드를 일시 중지한 후 다시 활성화하면 피드가 일시 중지된 시간 동안의 데이터가 채우기 피드에 대해서는 처리되지만 라이브 피드에 대해서는 처리되지 않습니다. 자세한 내용은 [데이터 피드 활성화](#activate-a-data-feed)를 참조하십시오.

데이터 피드를 일시 중지하려면 다음 작업을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 일시 중지할 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **일시 중지**]&#x200B;를 선택합니다.

## 데이터 피드 활성화

비활성 상태인 피드를 활성화할 수 있습니다.

피드가 다시 활성화되면 피드가 비활성 상태인 동안 데이터가 자동으로 처리되지 않을 수 있습니다. 데이터 처리 여부는 채우기 피드인지 라이브 피드인지에 따라 다릅니다.

* **피드 채우기**(내역 데이터만 처리하는 피드)에서 중지된 위치의 데이터 처리를 다시 시작하고 필요한 경우 날짜를 다시 채웁니다.

* **라이브 피드**&#x200B;가 활성화된 시점부터 데이터 처리를 다시 시작합니다. 즉, 피드가 일시 중지된 시간부터 활성화된 시간까지 데이터가 처리되지 않습니다. 이 기간 동안 데이터가 필요한 경우 채우기 작업을 설정해야 합니다.

데이터 피드를 활성화하려면 다음을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 활성화하려는 비활성 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **활성화**]&#x200B;를 선택합니다.

## 데이터 피드 삭제

데이터 피드를 삭제하면 해당 상태가 [!UICONTROL 삭제됨]&#x200B;(으)로 설정됩니다. 데이터 피드를 삭제하려면 먼저 데이터 피드 상태가 활성이어야 합니다.

데이터 피드를 삭제하려면

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 삭제할 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **삭제**]&#x200B;를 선택합니다.

## 데이터 피드 관리자에서 열 구성

만들어진 각 피드에는 피드에 대한 정보를 제공하는 몇 개의 열이 표시됩니다. 오름차순으로 정렬하려면 열 헤더를 선택하십시오. 내림차순으로 정렬하려면 열 헤더를 다시 선택하십시오. 특정 열이 표시되지 않으면 오른쪽 상단의 열 아이콘을 클릭합니다.

![열 아이콘](assets/cols.jpg)

다음 열을 사용할 수 있습니다.

* **피드 이름**: 필수 열입니다. 피드 이름을 표시합니다.
* **피드 ID**: 고유 식별자인 피드 ID를 표시합니다.
* **보고서 세트**: 피드가 데이터를 참조하는 보고서 세트입니다.
* **보고서 세트 ID**: 보고서 세트의 고유 식별자입니다.
* **데이터 열**: 피드에 대해 활성화된 데이터 열입니다. 대부분의 경우 이 형식으로 표시할 열이 너무 많습니다.
* **간격**: 피드가 시간별인지 또는 일별인지를 나타냅니다.
* **대상 유형**: 피드의 대상 유형입니다. 예를 들어 Amazon S3, GCP 또는 Azure가 있습니다.
* **대상 호스트**: 파일이 있는 위치입니다.
* **소유자**: 피드를 만든 사용자 계정입니다.
* **상태**: 피드의 상태입니다.
   * 활성: 피드가 작동 중입니다.
   * 승인 보류: 일부 상황에서 피드가 작업 생성을 시작할 수 있으려면 먼저 Adobe에서 피드를 승인해야 합니다.
   * 삭제됨: 피드가 삭제되었습니다.
   * 완료: 피드의 처리가 완료되었습니다. 완료된 피드를 편집하거나, 보류하거나, 취소할 수 있습니다.
   * 보류 중: 피드가 만들어졌지만 아직 활성 상태가 아닙니다. 피드가 짧은 전환 시간 동안 이 상태로 유지됩니다.
   * 비활성: &#39;일시 중지됨&#39; 또는 &#39;보류 중&#39; 상태에 해당합니다. 비활성 피드가 다시 활성화될 때 채우기 피드 및 라이브 피드에 발생하는 사항에 대한 자세한 내용은 [데이터 피드 활성화](#activate-a-data-feed)를 참조하십시오.
* **마지막 수정 날짜**: 피드가 마지막으로 수정된 날짜입니다. 날짜 및 시간은 보고서 세트의 시간대에서 GMT 오프셋을 사용하여 표시됩니다.
* **시작 날짜**: 이 피드에 대한 첫 번째 작업의 날짜입니다. 날짜 및 시간은 보고서 세트의 시간대에서 GMT 오프셋을 사용하여 표시됩니다.
* **종료 날짜**: 이 피드에 대한 마지막 작업의 날짜입니다. 진행 중인 데이터 피드에는 종료 날짜가 없습니다.

