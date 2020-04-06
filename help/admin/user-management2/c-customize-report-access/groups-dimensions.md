---
description: eVar, 트래픽 보고서, 솔루션 보고서 및 경로 지정 보고서를 포함하여 세분된 수준에서 사용자 액세스를 사용자 지정합니다.
keywords: groups;permissions
subtopic: Users and groups
title: 차원 권한 사용자 지정
topic: Admin tools
uuid: aaf164ad-3863-4129-864e-39ec71c6a8eb
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 차원 권한 사용자 지정

>[!IMPORTANT] 사용자 및 제품 관리를 [Admin Console](https://helpx.adobe.com/kr/enterprise/using/admin-console.html)로 이동 중입니다. Adobe는 사용자를 마이그레이션할 때가 되면 통지합니다. After all customers have migrated, help content for **[!UICONTROL Analytics]** > **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** will be retired.

eVar, 트래픽 보고서, 솔루션 보고서 및 경로 지정 보고서를 포함하여 세분된 수준에서 사용자 액세스를 사용자 지정합니다.

**[!UICONTROL User Management]** > **[!UICONTROL Groups]** > **[!UICONTROL Report Access]** > **[!UICONTROL Dimensions]** > **[!UICONTROL Customize]**

>[!IMPORTANT] 현재 일부 차원은 허용되지 않습니다. 이러한 차원은 다음과 같습니다.모바일 책갈피 길이;모바일 장치 번호;모바일 DRM;모바일 정보 서비스;모바일 Java VM;모바일 메일 데코레이션;모바일 네트 프로토콜;모바일 OS;모바일 중심의 커뮤니케이션
>
>이러한 차원은 다른 권한에 상관없이 모든 사용자에 대해 사용할 수 있습니다.

이 페이지의 설정은 [!UICONTROL Define User Groups] 페이지에서 선택한 보고서 세트와 관련이 있습니다.

![](assets/permissions-dimensions.png)

권한에 대한 차원 카테고리에 대한 다음 정보를 이해합니다.

* eVar 1-250은 개별적으로 권한을 가집니다.
* 모든 트래픽 보고서는 차원입니다.
* 비디오 및 모바일 보고서는 다른 Analytics 솔루션 보고서(Experience Manager, Advertising Cloud, Social 등)일 뿐만 아니라 차원입니다.
* 경로 지정 보고서는 사용자가 상위 차원에 액세스할 수 있는 경우에 사용할 수 있습니다.
* 사용자 지정 그룹 내의 모든 현재 차원 및 지표는 자동으로 새 카테고리로 마이그레이션되었습니다. 기존 그룹에 지표가 활성화되어 있을 경우, 기본적으로 모든 새로 허용할 수 있는 측정 기준(eVar 및 콘텐츠 인식) 및 지표가 주어집니다.
* 분류 가져오기(이전 SAINT) 권한: 분류에 대한 액세스 권한은 분류가 기준으로 사용하는 [변수](https://marketing.adobe.com/resources/help/ko_KR/reference/c_classifications.html)에 대한 액세스 권한으로 결정됩니다. 

자세한 내용은 권한 변경에 [대한 FAQ를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/reference/permissions_faq.html).

**차원 사용자 정의**

다음 항목은 사용자가 허용할 수 있는 차원입니다.

<table id="table_F37D74A1619A4560A5F5651E855DAF1C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="/help/admin/admin/conversion-var-admin/conversion-var-admin.md"> eVar </a> </p> </td> 
   <td colname="col2"> <p>eVar 1-250은 개별적으로 권한을 가집니다. eVar는 사용자 지정 보고서에서 전환 성공 지표를 세그먼트화하는 데 사용하는 사용자 지정 전환 변수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/ko_KR/sc/implement/props_eVars.html"> Prop </a> </p> </td> 
   <td colname="col2"> <p>Prop는 사용자 지정 트래픽 변수입니다. </p> <p>분석 구현에서 <a href="https://marketing.adobe.com/resources/help/ko_KR/sc/implement/props_eVars.html">트래픽 prop 및 전환 eVar</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/ko_KR/sc/implement/hierN.html"> 계층 </a> </p> </td> 
   <td colname="col2"> <p> 계층(hierN) 변수는 사이트의 계층 또는 페이지 구조에서 페이지의 위치를 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/ko_KR/sc/implement/listN.html"> Listvar </a> </p> </td> 
   <td colname="col2"> <p> 목록 Prop의 기능과 마찬가지로 목록 변수를 사용하면 동일한 이미지 요청 내에서 여러 값을 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>표준 </p> </td> 
   <td colname="col2"> <p>Analytics에서 표준(즉시 사용) 차원을 참조합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/em/"> AEM </a> </p> </td> 
   <td colname="col2"> <p>Adobe Experience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/media-optimizer/"> AMO </a> </p> </td> 
   <td colname="col2"> <p>Adobe Advertising Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/ko_KR/analytics/activitymap/"> Activity Map </a> </p> </td> 
   <td colname="col2"> <p> Activity Map 보고 차원: Activity Map 페이지, Activity Map 링크, Activity Map 영역, 지역별 Activity Map 링크, Activity Map XY </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/ko_KR/mobile/"> 모바일 </a> </p> </td> 
   <td colname="col2"> <p>Adobe Mobile Services </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Comscore </p> </td> 
   <td colname="col2"> <p>이 파트너 통합은 더 이상 활성화되어 있지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/ko_KR/sc/appmeasurement/hbvideo/nielsen-partnership.html"> Nielsen </a> </p> </td> 
   <td colname="col2"> <p>이 파트너 통합은 더 이상 활성화되어 있지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 소셜 </p> </td> 
   <td colname="col2"> <p>사용되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
