---
description: 경고를 생성, 편집 또는 삭제합니다.
title: 경고 관리자 (Analysis Workspace)
feature: Alerts
role: User, Admin
exl-id: c33a9a30-f53f-443c-96b7-6a87d03573c7
source-git-commit: 58e1d3025b455de7fa07037b3b0659330c8324c7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 6%

---


# 경고 관리

경고 관리자에서 기존 경고를 관리할 수 있습니다. 태그 지정, 이름 변경, 삭제 등과 같은 경고에 대한 다양한 관리 작업을 수행할 수 있습니다.

경고 관리자는 다음과 매우 유사하게 구성되어 있습니다. [세그먼트 관리자](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=ko-KR) 및 [계산된 지표 관리자](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=ko-KR).

## 경고 만들기

경고 관리자에서 경고를 생성하려면 다음을 수행합니다.

1. 선택 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고]** Adobe Analytics의 경고 관리자에 액세스합니다.

   ![](assets/alert-manager.png)

1. 선택 [!UICONTROL **추가**] (또는 [!UICONTROL **새 경고 만들기**] 기존 경고가 없는 경우)입니다.

1. 생성하려는 경고에 해당하는 경고 유형을 선택합니다.

   * [!UICONTROL **Analytics 데이터 경고**]: 데이터에서 비정상 이벤트가 발생하는 경우 알려 주는 경고입니다.

     이 옵션을 선택하는 경우 다음을 계속합니다. [경고 만들기](/help/analyze/analysis-workspace/c-intelligent-alerts/alert-builder.md) 경고 만들기에 대한 자세한 내용은 을 참조하십시오.

   * [!UICONTROL **서버 호출 사용량 경고**]: 서버 호출 사용량 및 약정 데이터에서 초과의 위험 또는 발생을 알리는 경고입니다.

     이 옵션을 선택하는 경우 다음을 계속합니다. [서버 호출 사용량 경고](/help/admin/admin/c-server-call-usage/scu-alerts.md).

     >[!NOTE]
     >
     >서버 호출 사용량에 액세스하려면 Analytics 관리자이거나 서버 호출 사용 권한이 있는 사용자여야 합니다.




## 기존 경고 관리

경고 관리자에서 기존 경고를 관리하려면 다음 작업을 수행하십시오.

1. 선택 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고]** Adobe Analytics의 경고 관리자에 액세스합니다.

   ![](assets/alert-manager.png)

1. 관리할 경고를 하나 이상 선택합니다.

   ![](assets/alert-manager-tasks.png)

1. 작업 표시줄에서 다음 옵션 중 하나를 선택합니다.

   | 액션 | 함수 |
   |---------|----------|
   | [!UICONTROL **태그**] | 경고에 태그를 적용합니다. 이렇게 하면 쉽게 사용할 수 있도록 경고를 구성하는 데 도움이 됩니다. |
   | [!UICONTROL **삭제**] | 경고를 삭제합니다. |
   | [!UICONTROL **이름 변경**] | 경고 이름을 변경합니다. |
   | [!UICONTROL **승인**] | 경고를 승인됨으로 표시합니다. |
   | [!UICONTROL **복사**] | 경고의 사본(복제)을 만듭니다. |
   | [!UICONTROL **사용 안 함**] | 현재 활성화되어 있는 경고를 비활성화합니다. |
   | [!UICONTROL **활성화**] | 현재 비활성화된 경고를 활성화합니다. |
   | [!UICONTROL **갱신**] | 경고 만료일을 갱신합니다. 이렇게 하면 원래 만료 날짜와 상관없이 이 옵션을 선택한 날로부터 1년으로 만료 날짜가 연장됩니다. |
   | [!UICONTROL **CSV로 내보내기**] | 경고를 .CSV 파일로 내보냅니다. |
