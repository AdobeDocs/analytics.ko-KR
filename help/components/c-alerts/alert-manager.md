---
description: 경고 관리.
title: 경고 관리자 개요
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 49324ef7fd45adeef2c31167d0444a7e67041d6d
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 35%

---

# 경고 관리자

경고 관리자는 구조가 [세그먼트 관리자](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=ko-KR) 및 [계산된 지표 관리자](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=ko-KR)와 매우 유사합니다.

![](assets/alert-manager.png)

## 경고 관리자 액세스

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **경고**]&#x200B;를 선택합니다.

## 경고 관리자에서 사용 가능한 작업

경고 관리자에서 다음 작업을 수행할 수 있습니다.

* **[!UICONTROL + 추가]**&#x200B;를 클릭하여 경고 빌더에 액세스합니다.
* 경고에 태그 지정. 경고를 쉽게 사용할 수 있도록 구성할 수 있습니다.
* 경고 삭제
* 경고 이름 변경
* 경고 승인
* 경고 복사
* 경고 활성화/비활성화
* 경고 만료 날짜 **갱신**. 하나 이상의 경고를 선택한 경우 **[!UICONTROL 갱신]**&#x200B;을 클릭하여 갱신할 수 있습니다. 이렇게 하면 원래 만료 날짜와 상관없이 **[!UICONTROL 갱신]**&#x200B;을 클릭한 날로부터 1년으로 만료 날짜가 연장됩니다.
* 경고를 .CSV 파일로 내보내기
* 경고 제목을 더블 클릭하여 경고 편집
* 경고 검색
* 다른 보고서 세트에 경고 추가
* 경고 소유자 지정/변경
* 다른 필터 추가
* 경고 **만료 날짜** 정의

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


