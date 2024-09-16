---
description: 경고 관리.
title: 경고 관리자 개요
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 2b8688da1400857b7f5093197d06c04681cd87ff
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 6%

---

# 경고 관리자

경고 관리자에서 기존 경고를 관리할 수 있습니다. 태그 지정, 이름 변경, 삭제 등과 같은 경고에 대한 다양한 관리 작업을 수행할 수 있습니다.

경고 관리자는 구조가 [세그먼트 관리자](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=ko-KR) 및 [계산된 지표 관리자](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=ko-KR)와 매우 유사합니다.

![](assets/alert-manager.png)

## 경고 만들기

경고 관리자에서 경고를 생성하려면 다음을 수행합니다.

1. Adobe Analytics의 경고 관리자에 액세스하려면 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고]**&#x200B;를 선택하십시오.

   ![](assets/alert-manager.png)

1. [!UICONTROL **추가**](또는 기존 경고가 없는 경우 [!UICONTROL **새 경고 만들기**])를 선택합니다.

1. 생성하려는 경고에 해당하는 경고 유형을 선택합니다.

   * [!UICONTROL **Analytics 데이터 경고**]: 데이터에서 비정상적인 이벤트가 발생하면 알려 주는 경고입니다.

     이 옵션을 선택하는 경우 경고 만들기에 대한 자세한 내용을 보려면 [경고 만들기](/help/components/c-alerts/alert-builder.md)를 계속하십시오.

   * [!UICONTROL **서버 호출 사용량 경고**]: 서버 호출 사용량 및 약정 데이터의 초과 사용 위험이나 발생을 알리는 경고입니다.

     이 옵션을 선택하는 경우 [서버 호출 사용량 경고](/help/admin/admin/c-server-call-usage/scu-alerts.md)를 사용하여 계속하십시오.

     >[!NOTE]
     >
     >서버 호출 사용량에 액세스하려면 Analytics 관리자이거나 서버 호출 사용 권한이 있는 사용자여야 합니다.

## 기존 경고 관리

기존 경고에 대해 태그 지정, 이름 변경, 삭제 등과 같은 다양한 작업을 수행할 수 있습니다.

경고 관리자에서 기존 경고를 관리하려면 다음 작업을 수행하십시오.

1. Adobe Analytics의 경고 관리자에 액세스하려면 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고]**&#x200B;를 선택하십시오.

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

## 경고 편집

기존 경고를 편집하려면:

1. Adobe Analytics의 경고 관리자에 액세스하려면 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고]**&#x200B;를 선택하십시오.

   ![](assets/alert-manager.png)

1. [!UICONTROL **제목 및 설명**] 열에서 경고 이름을 선택하십시오.

1. 원하는 대로 경고를 편집합니다.

   다음은 경고를 편집할 때 수행할 수 있는 몇 가지 작업입니다.

   * 다른 보고서 세트에 경고 추가
   * 소유자 변경
   * 필터 업데이트
   * 만료 날짜 업데이트

1. 경고를 편집한 다음 [!UICONTROL **저장**]&#x200B;을 선택합니다.

## 열 구성

표시되는 열을 구성하여 경고 관리자에서 각 경고에 대해 표시되는 정보를 구성할 수 있습니다.

경고 관리자에서 표시되는 열을 구성하려면 다음을 수행합니다.

1. Adobe Analytics에서 **[!UICONTROL 구성 요소]** 탭을 선택한 다음 **[!UICONTROL 경고]**&#x200B;를 선택합니다.

1. 경고 관리자에서 **열 사용자 지정** 아이콘 ![열 사용자 지정](assets/customize-columns-icon.png)을 선택한 다음 경고 관리자에 표시할 열을 선택합니다.

   다음 열을 사용할 수 있습니다.

   | 열 제목 | 설명 |
   |---|---|
   | 제목 및 설명 | 이러한 값은 경고 빌더에 제공됩니다. 제목 및 설명을 편집하려면 제목 링크를 선택하여 경고 빌더를 엽니다. |
   | 즐겨찾기 | 각 경고 옆에 별 아이콘을 표시하여 경고를 즐겨찾기로 표시할 수 있습니다. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | 유형 | 경고가 Analytics 데이터 경고인지 서버 호출 사용량 경고인지 여부를 표시합니다. |
   | 활성화됨 | 경고가 현재 활성화되었는지 또는 비활성화되었는지 여부를 표시합니다. |
   | 보고서 세트 | 경고가 마지막으로 저장된 보고서 세트를 나타냅니다. |
   | 소유자 | 경고를 소유하는 사람을 나타냅니다. 관리자가 아닌 경우 사용자가 소유하거나 사용자와 공유된 경고만 볼 수 있습니다. |
   | 태그 | 사용자 또는 사용자와 경고를 공유한 사람이 경고에 적용한 태그를 표시합니다. |
   | 만료 날짜 | 경고가 만료되도록 설정된 날짜와 시간을 표시합니다. |
   | 수정한 날짜 | 경고가 마지막으로 수정된 날짜를 나타냅니다. |

   {style="table-layout:auto"}

   <!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->


