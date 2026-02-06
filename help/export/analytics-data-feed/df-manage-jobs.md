---
title: 데이터 피드 작업 관리
description: 데이터 피드에서 개별 작업을 관리하는 방법을 알아봅니다. 인터페이스를 탐색하고 필터 및 검색을 사용하고 열 정의를 찾습니다.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
source-git-commit: d042bdb680504fdbf0ba346e5829713e529bd543
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 11%

---

# 데이터 피드 작업 관리

작업은 압축된 파일을 출력하는 개별 작업입니다. 피드에 의해 만들어지고 제어됩니다.

각 데이터 피드에 대한 작업 내역을 보거나, 작업을 다시 보내거나, 작업을 다시 처리할 수 있습니다.

## 데이터 피드에 대한 작업 내역 보기

각 작업에 대한 정보와 함께 주어진 데이터 피드에 대한 데이터 피드 작업 목록을 볼 수 있습니다.

데이터 피드에 대한 작업 기록을 보려면 다음 작업을 수행하십시오.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.

1. 오른쪽 상단에 있는 9제곱 아이콘을 선택한 다음 [!UICONTROL **Analytics**]&#x200B;을 선택합니다.

1. 맨 위 탐색 막대에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;로 이동합니다.

   액세스 권한이 있는 모든 보고서 세트에 대한 데이터 피드가 표시됩니다. 또는 구성된 피드가 없는 경우 페이지에 **[!UICONTROL 데이터 피드 만들기]** 단추가 표시됩니다.

   ![데이터 피드 관리자](assets/data-feed-manager.png)

1. 보려는 작업이 포함된 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **작업 기록**]&#x200B;을 선택합니다.

   사용 가능한 열에 각 작업에 대한 정보와 함께 데이터 피드 작업 내역이 표시됩니다.

1. (선택 사항) 테이블에 표시되는 열을 조정하려면 오른쪽 상단에서 열 아이콘 ![열 아이콘](assets/customize-columns-icon.png)을 선택한 다음 [테이블 사용자 지정] 대화 상자에서 보려는 각 열을 선택하고 숨기려는 각 열의 선택을 취소합니다.

   다음 열을 사용할 수 있습니다.

   * **[!UICONTROL 요청 기간 시작]**

   * **[!UICONTROL 요청 기간 종료]**

   * **[!UICONTROL 예약됨]**

   * **[!UICONTROL 시작]**

   * **[!UICONTROL 완료됨]**

   * **[!UICONTROL 실행 #]**

   * **[!UICONTROL 상태]**

   * **[!UICONTROL 오류 코드]**

   * **[!UICONTROL 오류 메시지]**

## 데이터 피드 작업 다시 보내기

데이터 피드 작업을 다시 보내면 파일이 원래 전송될 때와 동일한 데이터 및 처리로 데이터 피드 파일이 다시 전송됩니다. 또는 [데이터 피드 작업을 다시 처리](#reprocess-data-feed-jobs)할 수 있습니다.

하나 이상의 데이터 피드 작업을 다시 보내려면 다음을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 다시 전송할 작업이 포함된 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **작업 기록**]&#x200B;을 선택합니다.

1. 하나 이상의 데이터 피드 작업 옆의 확인란을 선택한 다음 **[!UICONTROL 다시 보내기]**&#x200B;를 선택합니다. <!-- What does the status need to be? Error, ... -->

   ![데이터 피드 작업 재처리](assets/data-feed-job-resend.png)

## 데이터 피드 작업 재처리

데이터 피드 작업을 재처리하면 데이터 피드 작업의 소스 데이터가 재처리되고 재처리된 데이터와 함께 다시 전송됩니다. 또는 [데이터 피드 작업을 다시 전송](#resend-data-feed-jobs)할 수 있습니다.

하나 이상의 데이터 피드 작업을 재처리하려면 다음을 수행하십시오.

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 다시 처리할 작업이 포함된 데이터 피드 옆의 확인란을 선택한 다음 [!UICONTROL **작업 기록**]&#x200B;을 선택합니다.

1. 하나 이상의 데이터 피드 작업 옆의 확인란을 선택한 다음 **[!UICONTROL 재처리]**&#x200B;를 선택합니다. <!-- What does the status need to be? Error, ... -->

   ![데이터 피드 작업 재처리](assets/data-feed-job-reprocess.png)
