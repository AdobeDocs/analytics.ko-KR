---
description: 사용자 특성에 대한 Analytics FAQ 및 사용자 특성 보고서 실행 방법.
seo-description: 사용자 특성에 대한 Analytics FAQ 및 사용자 특성 보고서 실행 방법.
seo-title: 고객 속성
solution: Marketing Cloud, Analytics
title: 고객 속성
uuid: 94721265-BA 23-45 D 5-8807-76 F 81 B 0 B 8 A 30
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 고객 속성

사용자 특성에 대한 Analytics FAQ 및 사용자 특성 보고서 실행 방법.

**[!UICONTROL 보고서]** **[!UICONTROL &gt; 방문자 프로필]** &gt; **[!UICONTROL 고객 속성]**

CRM(고객 관계 관리) 데이터베이스에서 엔터프라이즈 고객 데이터를 캡처하는 경우, 이 데이터를 Experience Cloud의 고객 속성 데이터 소스에 업로드할 수 있습니다. 데이터가 업로드된 후 Reports &amp; Analytics에서 사용자 특성 보고서를 실행할 수 있습니다.

* [Analytics의 사용자 특성 및 보고 지표](../../../components/c-variables/dimensionslist/reports-customer-attributes.md#section_EF343662146B460A882D3DF772ADD86D)
* [FAQ - Analytics의 사용자 특성](../../../components/c-variables/dimensionslist/reports-customer-attributes.md#section_E29641D1F3D649C1AC9EA5231921F038)

사용자 특성 데이터 업로드에 대한 자세한 내용은 Experience Cloud 도움말의 [사용자 특성](https://marketing.adobe.com/resources/help/en_US/mcloud/index.html?f=attributes)을 참조하십시오.

## Analytics의 사용자 특성 및 보고 지표 {#section_EF343662146B460A882D3DF772ADD86D}

After you upload customer attributes and validate the schema (in the Experience Cloud), the system creates metrics based on the friendly names (like *`age`* or *`gender`*) that you map to the attribute strings and integers. These metrics appear in **[!UICONTROL Visitor Profile]** &gt; **[!UICONTROL Customer Attributes]** reports.

예:

**[!UICONTROL 방문자 프로필]** &gt; **[!UICONTROL 고객 속성]** &gt; **[!UICONTROL 연령]**

![](assets/report_age.png)

**예 - 연령 지표**

문자열을 *`age`*&#x200B;로 설정되면 시스템이 다음 지표 및 차원을 생성합니다.

* 연령 측정기준: 연령 특성을 기반으로 보고서를 실행할 수 있도록 해줍니다.
* 연령 지표: 고유 방문자 수 보고서와 같이 보고서에 추가할 수 있는 지표입니다.
* 연령 카운트 지표: 예를 들어 방문자가 양식에 *`age`* 값을 지정한 경우 이해할 수 있도록 해줍니다.

Because metrics are sums in a report table, you should [create a calculated metric](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/) that tells you the average age. The formula for this metric is `Age / Count of Age`.

## FAQ - Analytics의 사용자 특성 {#section_E29641D1F3D649C1AC9EA5231921F038}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Prop 또는 evar에 고객 ID를 채우는 대신 ID 서비스를 사용하여 고객 ID를 설정하는 것이 더 좋은 이유는 무엇입니까? </p> </td> 
   <td colname="col2"> <p>ID 서비스를 사용하면 다음과 같은 다양한 이점이 있습니다. </p> 
    <ul id="ul_5D3659604D43419F9CA5920B4F93728E"> 
     <li id="li_BA2EF0715C5A47EFAFA7191CFAD088A4">ID 서비스로 고객 ID를 설정하지 않은 경우 고객 레코드는 Adobe Analytics 에서만 사용할 수 있습니다. 실시간 타깃팅을 위해 고객 기록을 사용하려면 ID 서비스를 사용해야 합니다. </li> 
     <li id="li_228358684E474A298E39578D427BF932">ID 서비스를 사용하여 고객 ID를 설정하면 ID를 Experience Cloud와 동기화하는 데 걸리는 시간이 줄어듭니다. Prop 또는 eVar에 고객 ID를 입력하면 일괄로 발생하는 백엔드 서버 동기화를 통해 고객 ID가 Experience Cloud로 전송됩니다. ID 서비스는 고객 ID를 Experience Cloud와 즉시 동기화합니다. </li> 
     <li id="li_BCF28219E4014FCF9F747C3D8D270526"> prop 또는 evar 대신 ID 서비스를 사용하면 해당 prop 또는 evar가 다른 용도로 활성화됩니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이미 Prop 또는 eVar에 고객 ID를 저장하고 있는데 내 Prop 또는 eVar을 CRM 특성으로 분류하는 대신 이 새로운 기능을 사용해야 하는 이유가 무엇입니까? </p> </td> 
   <td colname="col2"> <p>Prop 및 eVar는 [고유 수가 초과되었습니다] 제한 사항에 따라 달라집니다. 이 기능을 사용하면 무제한의 고객 ID 개수에 대해 특성 데이터를 가져올 수 있습니다. 또한 Prop/eVar 접근 방식을 사용하면 CRM 정보가 Analytics로 제한됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>내 CRM 특성은 어떻게 Adobe Analytics에 표시됩니까? </p> </td> 
   <td colname="col2"> <p>CRM 특성은 Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis, 보고 API 및 Report Builder에서 매니페스트됩니다. 텍스트 특성은 보고서/측정기준으로 나타납니다. 숫자 속성은 측정기준 및 지표로 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CRM 데이터를 Data Warehouse와 데이터 피드에서 사용할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>CRM 데이터는 현재 Data Warehouse와 Analytics 데이터 피드에서 사용할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

