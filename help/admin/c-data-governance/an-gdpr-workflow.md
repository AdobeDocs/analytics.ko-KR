---
description: 'null'
seo-description: 'null'
seo-title: Adobe Analytics 데이터 개인 정보 보호 워크플로우
title: Adobe Analytics 데이터 개인 정보 보호 워크플로우
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# Adobe Analytics 데이터 개인 정보 보호 워크플로우

Adobe Analytics 및 데이터 개인 정보 보호 준비를 시작합니다. 이 워크플로우에서는 데이터 주체의 데이터 개인 정보 보호 액세스 및 삭제 권한을 지원하도록 Adobe Analytics를 구현하기 위해 수행해야 하는 단계를 간략하게 설명합니다.

<!--
<table id="table_0E561F62247A4D01B6E7180560082DC9"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Task Description </th> 
   <th colname="col3" class="entry"> Links to Instructions and More Information </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step1_icon.png" id="image_15849358972A4846A54FCB51997576D5" /> Ensure that any of your report suites that might contain Data Privacy-relevant data are mapped to your Experience Cloud (or IMS) organization. </p> <p>Data Privacy requests are submitted using an Experience Cloud Organization and will be applied to all report suites claimed by that Organization. Requests will not apply to report suites not mapped to that Organization, even if they are part of your login company. </p> </td> 
   <td colname="col3"> <p>Refer to <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html"> Map report suites to an organization</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step2_icon.png" id="image_372B2C65DFAD46E39AE4D715313ABD0E"/> Set your data retention policy. </p> </td> 
   <td colname="col3"> <p>A data retention policy needs to be in place in order for Adobe to service Data Privacy data access/delete requests. </p> <p>For more information, see this <a href="https://marketing.adobe.com/resources/help/en_US/reference/data-retention-client-table-faq.html"> Analytics Data Retention FAQ</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step3_icon.png" id="image_30DB956290CC4E64A7085B46364BE059" /> Familiarize yourself with DULE/Data Privacy labels, Adobe Analytics IDs, namespaces, and ID expansion. </p> </td> 
   <td colname="col3"> <p> Read these topics in this documentation set: 
     <ul> 
      <li><a href="/help/admin/c-data-governance/gdpr-labels.md"> Data Privacy Labels for Analytics Variables</a> </li> 
      <li><a href="/help/admin/c-data-governance/gdpr-analytics-ids.md"> Labeling Best Practices</a>--> </li>
    &lt;/ul&gt; &lt;/p&gt; &lt;/td&gt;
</tr> 
  <tr> 
   <td colname="col2"> <p><img  src="assets/step4_icon.png" id="image_FE2039B8345248BCA303B44C10B68EA1" placement="break" /> ID, 민감도 및 데이터 거버넌스 레이블을 보고서 세트의 각 변수에 지정합니다. </p> <p>참고: 새 보고서 세트를 작성할 때마다 또는 기존 보고서 세트 내에서 새 변수를 활성화하는 경우 레이블 지정을 검토해야 합니다. 또한, 새로운 솔루션 통합이 활성화된 경우 레이블 지정이 필요할 수 있는 새로운 변수를 노출할 수 있으므로 레이블 지정을 검토해야 할 수 있습니다. 모바일 앱 또는 웹 사이트를 재구현하면 기존 변수가 사용되는 방식이 변경될 수 있으며, 이로 인해 레이블 업데이트가 필요할 수도 있습니다. </p> </td> 
   <td colname="col3"> <p> <a href="/help/admin/c-data-governance/gdpr-setup-reportsuite.md">보고서 세트 데이터에 레이블 지정</a>의 지침을 따릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step5_icon.png" id="image_E9BEF83BF30F4528A030F23F71E5E5D8" /> Adobe 데이터 개인 정보 보호 API에 연결하고 액세스 및 삭제 요청을 제출합니다. </p> </td> 
   <td colname="col3"> <p>Adobe Analytics 고객의 경우 <a href="https://www.adobe.io/apis/cloudplatform/gdpr.html">Adobe Experience Cloud 데이터 개인 정보 보호 API를 호출하여 고객 데이터 액세스 및 삭제에 대한 개별 데이터 개인 정보 보호 요청을 제출할 수 있습니다</a>. </p> <p><a href="/help/admin/c-data-governance/gdpr-analytics-ids.md">레이블 지정 우수 사례</a> 섹션에 설명된 대로 Analytics 식별자를 해당 네임스페이스 ID(데이터 소스 ID)와 함께 요청에 제출할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step6_icon.png" id="image_5CF03706FECD4F8BBAE0D0C19F98B8BB" /> 보고서 세트의 데이터 개인 정보 보호 설정을 보고 관리합니다. </p> </td> 
   <td colname="col3"> <p><a href="/help/admin/c-data-governance/gdpr-view-settings.md">보고서 세트의 데이터 거버넌스 설정 보기</a>의 지침을 따릅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
--&gt;

| 작업 설명 | 지침 및 추가 정보에 대한 링크 |
|--- |--- |
| **1단계**: 데이터 개인 정보 보호 관련 데이터가 포함될 수 있는 모든 보고서 세트가 Experience Cloud(또는 IMS) 조직에 매핑되어 있는지 확인합니다.  데이터 개인 정보 보호 요청은 Experience Cloud 조직을 사용하여 제출되며, 해당 조직에서 요구하는 모든 보고서 세트에 적용됩니다. 보고서 세트가 로그인 회사의 일부인 경우에도 해당 조직에 매핑되지 않은 보고서 세트에는 요청이 적용되지 않습니다. | [조직에 보고서 세트 매핑](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/report-suite-mapping.html)을 참조하십시오. |
| **2단계**:데이터 유지 정책을 설정합니다. | Adobe에서 데이터 개인 정보 보호 데이터 액세스/삭제 요청을 처리하려면 데이터 보존 정책이 적용되어 있어야 합니다.  자세한 내용은 이 [Analytics 데이터 유지 FAQ](/help/technotes/data-retention.md)를 참조하십시오. |
| **3단계**: DULE/데이터 개인 정보 보호 레이블, Adobe Analytics ID, 네임스페이스 및 ID 확장에 대해 숙지하십시오. | 다음 설명서 세트에서 이러한 주제를 읽어 보십시오.<ul><li>[Analytics 변수의 데이터 개인 정보 보호 레이블](/help/admin/c-data-governance/gdpr-labels.md)</li><li>[레이블 지정 우수 사례](/help/admin/c-data-governance/gdpr-analytics-ids.md)</li></ul> |
| **4단계**: ID, 민감도 및 데이터 거버넌스 레이블을 보고서 세트의 각 변수에 지정합니다.  참고: 새 보고서 세트를 작성할 때마다 또는 기존 보고서 세트 내에서 새 변수를 활성화하는 경우 레이블 지정을 검토해야 합니다. 또한, 새로운 솔루션 통합이 활성화된 경우 레이블 지정이 필요할 수 있는 새로운 변수를 노출할 수 있으므로 레이블 지정을 검토해야 할 수 있습니다. 모바일 앱 또는 웹 사이트를 재구현하면 기존 변수가 사용되는 방식이 변경될 수 있으며, 이로 인해 레이블 업데이트가 필요할 수도 있습니다. | [보고서 세트 데이터에 레이블 지정](/help/admin/c-data-governance/gdpr-setup-reportsuite.md)의 지침을 따릅니다. |
| **5단계**: Adobe 데이터 개인 정보 보호 API에 연결하고 액세스 및 삭제 요청을 제출합니다. | Adobe Analytics 고객의 경우 [Adobe Experience Cloud 데이터 개인 정보 보호 API를 호출하여 고객 데이터 액세스 및 삭제에 대한 개별 데이터 개인 정보 보호 요청을 제출할 수 있습니다.](https://www.adobe.io/apis/experienceplatform/gdpr.html)[레이블 지정 우수 사례](/help/admin/c-data-governance/gdpr-analytics-ids.md) 섹션에 설명된 대로 Analytics 식별자를 해당 네임스페이스 ID(데이터 소스 ID)와 함께 요청에 제출할 수 있습니다. |
| **6단계**: 보고서 세트의 데이터 개인 정보 보호 설정을 보고 관리합니다. | [보고서 세트의 데이터 거버넌스 설정 보기](/help/admin/c-data-governance/gdpr-view-settings.md)의 지침을 따릅니다. |
