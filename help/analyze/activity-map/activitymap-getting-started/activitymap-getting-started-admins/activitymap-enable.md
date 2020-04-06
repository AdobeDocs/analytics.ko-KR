---
description: Analytics 관리자가 Activity Map 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 완료해야 하는 절차에 대해 설명합니다.
title: Activity Map 활성화
topic: Activity map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Activity Map 활성화{#enable-activity-map}

Analytics 관리자가 Activity Map 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 완료해야 하는 절차에 대해 설명합니다.

## 1단계. AppMeasurement(Javascript) 코드를 v1.6(또는 이상)으로 업데이트{#section_5D1586289DF2489289B1B6C1C80C300D}

Activity Map 모듈은 AppMeasurement.js 파일(파일의 맨 위에 있음)의 일부입니다. AppMeasurement 라이브러리는 인스턴스화될 때 Activity Map 모듈을 로드합니다.

이 버전(또는 이상)의 AppMeasurement로 업데이트하지 않으면 Activity Map 데이터를 수집할 수 없습니다.

1. Download the latest AppMeasurement code (AppMeasurement_Javascript-1.6.zip) by going to  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Code Manager]** and [implement it](https://marketing.adobe.com/resources/help/ko_KR/sc/implement/js_implementation.html).

   Activity Map 모듈을 포함하여 코드에 수행된 변경 사항을 시각화하는 데 도움이 되는 몇 가지 [샘플 구현 코드가](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) 포함되어 있습니다.

1. 구현의 유효성을 검사합니다.

   1. 클릭 가능한 요소를 클릭하면 데이터가 s_sq 쿠키에 저장됩니다.
   1. Activity Map 데이터는 추적 호출의 쿼리 문자열에서 볼 수 있습니다. 예:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Break this report down by **[!UICONTROL Activity Map Link by Region]** to see the link/region for that page:  ![](assets/am_breakdown.png){width=&quot;400px&quot;}

## 2단계. Activity Map 보고서 활성화 {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

먼저, 보고서 세트 수준에서 Activity Map 보고서를 활성화해야 합니다.

1. Log in to Adobe Analytics and navigate to  **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites >[select report suite]> Edit Settings > Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
1. Activity Map에서는 Activity Map 보고서에 있는 링크 데이터를 수집합니다. For the activation to happen, you must first activate the variables by clicking **[!UICONTROL Enable Activity Map Reports]**.

   이 단계에서는 데이터를 수집하는 데 필요한 모든 Analytics 차원을 추가합니다.

1. 약 1시간 후, 사용자가 링크를 [클릭한 모든 페이지를 보여주는 Activity Map 페이지 보고서를](/help/analyze/activity-map/activitymap-reporting-analytics.md)확인합니다.

## 3단계. Activity Map 액세스 그룹에 사용자 추가 {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. 클릭 **[!UICONTROL Add Users to Group]**.

   이렇게 하면 관리 콘솔에 그룹 관리 페이지가 표시됩니다.

1. [이 그룹에](https://marketing.adobe.com/resources/help/ko_KR/reference/groups.html) 사용자를 추가하고 **[!UICONTROL Save Group]**&#x200B;있습니다.

1. This allow your Admin users to download Activity Map from  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

>[!NOTE] 관리자가 아닌 사용자가 Activity Map을 다운로드하도록 하려면 &#39;도구&#39; 및 &#39;레거시 ClickMap 설치&#39;에 대한 권한을 제공하는 새 사용자 그룹을 만드십시오. 이 수준의 권한은 Activity Map 액세스와 함께 결합되어 도구를 다운로드하고 사용할 수 있는 권한을 제공합니다.
