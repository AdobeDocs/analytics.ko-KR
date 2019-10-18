---
description: 'null'
seo-description: 'null'
seo-title: Adobe Analytics 데이터 개인 정보 보호 워크플로우
title: Adobe Analytics 데이터 개인 정보 보호 워크플로우
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
translation-type: tm+mt
source-git-commit: af95cc329414cfca68968c463206314aae1b8e18

---


# Adobe Analytics 데이터 개인 정보 보호 워크플로우

Adobe Analytics 및 데이터 개인 정보 보호 정책을 시작합니다! 이 워크플로우는 데이터 주체의 데이터 개인 정보 보호 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics 구현을 준비하는 데 필요한 단계를 간략하게 설명합니다.

<table id="table_0E561F62247A4D01B6E7180560082DC9"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> 작업 설명 </th> 
   <th colname="col3" class="entry"> 지침 및 추가 정보에 대한 링크 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step1_icon.png" id="image_15849358972A4846A54FCB51997576D5" /> 데이터 개인 정보 관련 데이터를 포함할 수 있는 보고서 세트가 Experience Cloud(또는 IMS) 조직에 매핑되는지 확인하십시오. </p> <p>데이터 개인정보 보호 요청은 Experience Cloud 조직을 사용하여 제출되며 해당 조직이 요청한 모든 보고서 세트에 적용됩니다. 보고서 세트가 로그인 회사의 일부인 경우에도 해당 조직에 매핑되지 않은 보고서 세트에는 요청이 적용되지 않습니다. </p> </td> 
   <td colname="col3"> <p>Refer to <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html" format="html" scope="external"> Map report suites to an organization.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step2_icon.png" id="image_372B2C65DFAD46E39AE4D715313ABD0E"/> 데이터 보존 정책을 설정합니다. </p> </td> 
   <td colname="col3"> <p>Adobe가 데이터 개인 정보 보호 데이터 액세스/삭제 요청을 처리하려면 데이터 보존 정책이 적용되어야 합니다. </p> <p>For more information, see this <a href="https://marketing.adobe.com/resources/help/en_US/reference/data-retention-client-table-faq.html" format="html" scope="external"> Analytics Data Retention FAQ.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step3_icon.png" id="image_30DB956290CC4E64A7085B46364BE059" /> DULE/Data Privacy 레이블, Adobe Analytics ID, 네임스페이스 및 ID 확장에 익숙해지십시오. </p> </td> 
   <td colname="col3"> <p> 다음 설명서 세트에서 이러한 주제를 읽어 보십시오. 
     <ul id="ul_F6E94B9281D446DB8F1F859F6056543B"> 
      <li id="li_6389D094B4B04CA181E5F077BF8C0F8E"><!--<a href="/help/admin/c-data-governance/gdpr-labels.md#concept_F4061E29353446B5B0A7CF248D54E6F2" format="dita" scope="local"> Data Privacy Labels for Analytics Variables</a>--> </li> 
      <li id="li_CEEF2106E37845A49E0EA1225D5CFF14">목록 항목 </li> 
      <li id="li_0B79CEBD074A4C68923EE9C9766D4B9D"><!--<a href="/help/admin/c-data-governance/gdpr-analytics-ids.md#concept_1BC4CA94B559481F8B08776DA100B23E" format="dita" scope="local"> Labeling Best Practices</a>--> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img  src="assets/step4_icon.png" id="image_FE2039B8345248BCA303B44C10B68EA1" placement="break" /> ID, 민감도 및 데이터 거버넌스 레이블을 보고서 세트의 각 변수에 지정합니다. </p> <p>참고: 새 보고서 세트를 작성할 때마다 또는 기존 보고서 세트 내에서 새 변수를 활성화하는 경우 레이블 지정을 검토해야 합니다. 또한, 새로운 솔루션 통합이 활성화된 경우 레이블 지정이 필요할 수 있는 새로운 변수를 노출할 수 있으므로 레이블 지정을 검토해야 할 수 있습니다. 모바일 앱 또는 웹 사이트를 재구현하면 기존 변수가 사용되는 방식이 변경될 수 있으며, 이로 인해 레이블 업데이트가 필요할 수도 있습니다. </p> </td> 
   <td colname="col3"> <p> 다음 <!--<a href="/help/admin/c-data-governance/gdpr-setup-reportsuite.md#concept_FAA948AD8CEA4BC38CB482EAF3648731" format="dita" scope="local"> Label Report Suite Data</a>-->. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step5_icon.png" id="image_E9BEF83BF30F4528A030F23F71E5E5D8" /> Adobe Data Privacy API에 연결하고 액세스 및 삭제 요청을 제출합니다. </p> </td> 
   <td colname="col3"> <p>As an Adobe Analytics customer, you can submit individual Data Privacy requests to access and delete customer data, by calling the <a href="https://www.adobe.io/apis/cloudplatform/gdpr.html" format="html" scope="external"> Adobe Experience Cloud Data Privacy API.</a> </p> <p>You can submit any Analytics identifiers (as described in the section <!--<a href="/help/admin/c-data-governance/gdpr-analytics-ids.md#concept_1BC4CA94B559481F8B08776DA100B23E" format="dita" scope="local"> Labeling Best Practices</a>-->) in the requests along with their respective namespace IDs (data source IDs). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step6_icon.png" id="image_5CF03706FECD4F8BBAE0D0C19F98B8BB" /> 보고서 세트의 데이터 개인 정보 설정을 보고 관리합니다. </p> </td> 
   <td colname="col3"> <p>다음 <!--<a href="/help/admin/c-data-governance/gdpr-view-settings.md#concept_7759BAD6F3174901A94116D189AEF80E" format="dita" scope="local"> View Report Suite's Data Governance Settings</a>-->. </p> </td> 
  </tr> 
 </tbody> 
</table>

| 작업 설명 | 지침 및 추가 정보에 대한 링크 |
|--- |--- |
| **1단계**: 데이터 개인 정보 관련 데이터를 포함할 수 있는 보고서 세트가 Experience Cloud(또는 IMS) 조직에 매핑되는지 확인하십시오.  데이터 개인정보 보호 요청은 Experience Cloud 조직을 사용하여 제출되며 해당 조직이 요청한 모든 보고서 세트에 적용됩니다. 보고서 세트가 로그인 회사의 일부인 경우에도 해당 조직에 매핑되지 않은 보고서 세트에는 요청이 적용되지 않습니다. | Refer to [Map report suites to an organization.](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/report-suite-mapping.html) |
| **2단계**: 데이터 보존 정책을 설정합니다. | Adobe가 데이터 개인 정보 보호 데이터 액세스/삭제 요청을 처리하려면 데이터 보존 정책이 적용되어야 합니다.  For more information, see this [Analytics Data Retention FAQ.](/help/technotes/data-retention.md) |
| **3단계**: DULE/Data Privacy 레이블, Adobe Analytics ID, 네임스페이스 및 ID 확장에 익숙해지십시오. | 다음 설명서 세트에서 이러한 주제를 읽어 보십시오.<ul><li>[Analytics 변수의 데이터 개인 정보 레이블](/help/admin/c-data-governance/gdpr-labels.md)</li><li>[레이블 지정 우수 사례](/help/admin/c-data-governance/gdpr-analytics-ids.md)</li></ul> |
| **4단계**: ID, 민감도 및 데이터 거버넌스 레이블을 보고서 세트의 각 변수에 지정합니다.  참고: 새 보고서 세트를 작성할 때마다 또는 기존 보고서 세트 내에서 새 변수를 활성화하는 경우 레이블 지정을 검토해야 합니다. 또한, 새로운 솔루션 통합이 활성화된 경우 레이블 지정이 필요할 수 있는 새로운 변수를 노출할 수 있으므로 레이블 지정을 검토해야 할 수 있습니다. 모바일 앱 또는 웹 사이트를 재구현하면 기존 변수가 사용되는 방식이 변경될 수 있으며, 이로 인해 레이블 업데이트가 필요할 수도 있습니다. | Follow the instructions in [Label Report Suite Data.](/help/admin/c-data-governance/gdpr-setup-reportsuite.md) |
| **5단계**: Adobe Data Privacy API에 연결하고 액세스 및 삭제 요청을 제출합니다. | As an Adobe Analytics customer, you can submit individual Data Privacy requests to access and delete customer data, by calling the [Adobe Experience Cloud Data Privacy API.](https://www.adobe.io/apis/experienceplatform/gdpr.html)[레이블 지정 우수 사례](/help/admin/c-data-governance/gdpr-analytics-ids.md) 섹션에 설명된 대로 Analytics 식별자를 해당 네임스페이스 ID(데이터 소스 ID)와 함께 요청에 제출할 수 있습니다. |
| **6단계**:보고서 세트의 데이터 개인 정보 설정을 보고 관리합니다. | Follow the instructions in [View Report Suite's Data Governance Settings.](/help/admin/c-data-governance/gdpr-view-settings.md) |
