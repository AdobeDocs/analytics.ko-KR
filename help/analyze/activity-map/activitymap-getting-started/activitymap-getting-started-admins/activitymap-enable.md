---
description: '[!DNL Activity Map] 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 Analytics 관리자가 완료해야 하는 단계를 설명합니다.'
seo-description: '[!DNL Activity Map] 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 Analytics 관리자가 완료해야 하는 단계를 설명합니다.'
seo-title: '[!DNL Activity Map] 활성화'
solution: Analytics
title: '[!DNL Activity Map] 활성화'
topic: Activity Map
uuid: 3043319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: ae18932eda59c059e2aa635cc30f233b88840031

---


# 활성화 [!DNL Activity Map]{#enable-activity-map}

Explains the steps the Analytics Admin needs to complete to enable [!DNL Activity Map] link collection and user download.

## 1단계. Update Your AppMeasurement (Javascript) Code to v1.6 (or higher) {#section_5D1586289DF2489289B1B6C1C80C300D}

The [!DNL Activity Map] module is part of the AppMeasurement.js file (located at the top of the file). The AppMeasurement library will load the [!DNL Activity Map] module when instantiated.

[!DNL Activity Map]이 버전(또는 이상)의 AppMeasurement로 업데이트해야만 데이터를 수집할 수 있습니다.

1. Download the latest AppMeasurement code (AppMeasurement_Javascript-1.6.zip) by going to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Code Manager]** and [implement it](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html).

   Adobe에서는 모듈을 포함하여 코드에 수행한 변경 작업을 시각화하는 데 도움이 되기 위해 [샘플 구현 코드](../../../../analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md#concept_EC27DA8A62F5411EBED51284CB7E1734)를 일부 포함했습니다.[!DNL Activity Map]

1. 구현의 유효성을 검사합니다:

   1. 클릭 가능한 요소를 클릭하면, 데이터가 s_sq라는 쿠키에 저장됩니다.
   1. The [!DNL Activity Map] data can be seen in the query-string on the tracking call. 예:

      ```
      …&c.&a.&[!DNL Activity Map].&link=My%20Link&region=My%20Region&page=My%20Page&.[!DNL Activity Map]&.a&.c&...
      ```

1. Break this report down by **[!UICONTROL [!DNL Activity Map]Link by Region]** to see the link/region for that page:  ![](assets/am_breakdown.png){width="400px"}

## 2단계. 보고서 [!DNL Activity Map] 활성화 {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

First, you need to enable [!DNL Activity Map] reports at a report-suite level.

1. Log in to Adobe Analytics and navigate to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin &gt; Report Suites &gt;[select report suite]&gt; Edit Settings &gt;[!DNL Activity Map]]** &gt; **[!UICONTROL [!DNL Activity Map]Reporting]** .
1. [!DNL Activity Map] 보고서에서 링크 데이터를 [!DNL Activity Map] 수집합니다. For the activation to happen, you must first activate the variables by clicking **[!UICONTROL Enable[!DNL Activity Map]Reports]**.

   이 단계에서는 데이터를 수집하는 데 필요한 모든 Analytics 차원이 추가됩니다.

1. After about an hour, check the [[!DNL Activity Map] Page report](/help/analyze/activity-map/activitymap-reporting-analytics.md), which shows all the pages where users clicked on a link.

## 3단계. Add users to [!DNL Activity Map] access group {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. **[!UICONTROL 그룹에 사용자 추가를 클릭합니다]**.

   이렇게 하면 관리 콘솔에 그룹 관리 페이지가 표시됩니다.

1. [이 그룹에](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) 사용자를 추가하고 그룹을 **[!UICONTROL 저장합니다]**.

1. This allow your Admin users to download [!DNL Activity Map] from  **[!UICONTROL Adobe Analytics]** &gt; **[!UICONTROL Tools]** &gt; **[!UICONTROL ActivityMap]** .

> [!NOTE] 관리자가 아닌 사용자가 다운로드하도록 하려면 [!DNL Activity Map]'도구' 및 '레거시 ClickMap 설치'에 대한 권한을 제공하는 새 사용자 그룹을 만드십시오. 액세스 권한과 함께 이 수준의 권한을 [!DNL Activity Map] 통해 도구를 다운로드하고 사용할 수 있습니다.
