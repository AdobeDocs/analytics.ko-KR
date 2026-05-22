---
description: Adobe CX Enterprise의 Admin Console으로 Analytics 사용자 ID 마이그레이션에 대해 알아야 할 사항.
title: Admin Console로 Analytics 사용자 마이그레이션
feature: Admin Tools
exl-id: f4bc0e92-af53-40db-8138-44d29e4b25fe
role: Admin
TQID: https://experienceleague.adobe.com/bCf6DWIpIVALcGPAi3tL8zlZ5V8lzPR-9XNCm4HuFnY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
  - id: d124af73-4061-4b84-9063-ae2b60f2c1f3
  - id: e499b847-6dc4-408a-9f0b-70d35ce9b711
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 2960
ht-degree: 58%

---

# Adobe Admin Console로 Analytics 사용자 마이그레이션{#analytics-user-migration-to-the-admin-console}

Adobe CX Enterprise의 Adobe Admin Console으로 Analytics 사용자 ID 마이그레이션에 대해 알아야 할 사항.

Analytics 마이그레이션과 관련이 없는 Adobe Admin Console 주제에 대한 일반적인 도움말은 [Admin Console 사용 안내서](https://helpx.adobe.com/kr/enterprise/administering/user-guide.html)를 참조하십시오.

마이그레이션한 후 Adobe Admin Console에서 [CX 엔터프라이즈 사용자 및 제품을 관리](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR)할 수 있습니다.

## Analytics 사용자 ID 마이그레이션이란 무엇입니까? {#section-adbe49aba10c4e62afa836a97894107c}

Analytics 사용자 ID 마이그레이션을 통해 관리자는 Analytics User Management에서 Adobe Admin Console로 사용자 계정을 쉽게 마이그레이션할 수 있습니다. 사용자가 마이그레이션되면 CX Enterprise에서 사용할 수 있는 솔루션 및 핵심 서비스에 액세스할 수 있습니다. 마이그레이션이 단계적으로 고객에게 배포되고 있습니다.

Adobe Admin Console 사용의 이점은 다음과 같습니다.

<table id="table_E4465796E224474680D750CAC5434ED3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이점 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>SSO (Single Sign-On) </p> </td> 
   <td colname="col2"> <p>Analytics 사용자는 Adobe ID 또는 Enterprise ID을 사용하여 CX Enterprise 및 모든 솔루션에 로그인할 수 있습니다. 이 로그인을 사용하면 CX Enterprise의 통합 솔루션 및 핵심 서비스에 액세스할 수 있습니다. </p> <p>마이그레이션 후 기존 로그인(<span class="filepath">my.omniture.com</span> 및 <span class="filepath">sc.omniture.com</span>)을 통해 로그인하려는 사용자는 <span class="filepath">experiencecloud.adobe.com</span>으로 리디렉션됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 ID 및 권한 관리 </p> </td> 
   <td colname="col2"> <p>Analytics 관리자는 <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console</a>에서만 사용자 및 권한을 관리할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 및 핵심 서비스 관리 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">새 사용자 초대 </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">제품 프로필 만들기 </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">특정 제품 및 서비스에 대한 사용자 권한 부여 </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Adobe CX Enterprise에서 사용 가능한 <a href="https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html?lang=ko-KR"> 교차 솔루션 핵심 서비스</a>에 대한 액세스 권한을 얻습니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 사용자 ID 마이그레이션 전 알아 두어야 할 사항(FAQ) {#section-b0fc7f0bbd4b488e95b0c8e77ff077a9}

마이그레이션 전에 발생할 수 있는 질문에 대한 답변입니다.

<table id="table_36FD7EF1DAB44D359F4FC186D93147E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문/작업 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analytics 관리자로서 마이그레이션 전 이메일을 받았습니다. 먼저 무엇을 해야 합니까? </p> </td> 
   <td colname="col2"> <p>Adobe ID이 있고 <a href="https://adminconsole.adobe.com/enterprise/"> CX Enterprise Admin Console</a>에 액세스할 수 있는지 확인하십시오. </p> <p>그렇지 않은 경우 <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>에 문의하십시오. (사용자를 적절한 조직에 초대할 수 있는 시스템 또는 제품 관리자에게 먼저 문의해야 합니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics와 AEM 통합 </p> </td> 
   <td colname="col2"> <p> Analytics와 통합한 AEM 사용자는 암호 대신 Analytics 공유 암호를 사용하도록 구성을 변경해야 합니다. </p> <p> 마이그레이션을 활성화하기 전에 이 작업을 수행해야 합니다. 마이그레이션이 비활성화되면 원래 구성된 암호가 더 이상 유효하지 않습니다. </p> <p><b>Analytics에서 공유 암호를 가져오려면</b> </p> <p> 공유 암호는 Analytics(<span class="uicontrol">Analytics</span> &gt; <span class="uicontrol">사용자 관리</span>)에서 확보할 수 있으며 서로 다릅니다. </p> <p><b>공유 암호로 AEM 구성을 업데이트하는 방법</b> </p> <p><a href="https://helpx.adobe.com/kr/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html">Adobe Analytics 연결 및 프레임워크 생성</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder 업데이트 </p> </td> 
   <td colname="col2"> <p> <p>중요: <a href="/help/analyze/report-builder/report-builder-setup.md">Report Builder</a>의 설치를 최신 버전으로 업데이트합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션은 언제 시작됩니까? </p> </td> 
   <td colname="col2"> <p>Adobe은 이메일을 통해 Analytics 관리자에게 마이그레이션이 시작되는 시기에 대한 지침을 알려줍니다. </p> <p>Adobe Admin Console로의 마이그레이션은 물결처럼 발생합니다. Adobe은 마이그레이션 당일 Analytics 관리자에게 알리고 마이그레이션 도구에 대한 액세스 권한을 부여합니다. 로그인 회사가 각 마이그레이션 물결에 대해 정의된 기준을 충족하면 Adobe에서는 다음 작업을 수행합니다. </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">회사 마이그레이션의 시작 날짜와 종료 날짜를 설정합니다. </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">회사의 현재 Analytics 관리자에게 마이그레이션 약 30일 전에 이메일 알림을 보냅니다. </li> 
     <li id="li_476265B24CE2404B995201170C75D674">관리자에게 마이그레이션 시작 날짜를 알려 주는 제품 내 알림을 표시합니다. </li> 
    </ul> <p> 이전의 권한 그룹은 마이그레이션 당일 자동으로 Adobe Admin Console에 복사됩니다. 더 이상 Analytics 관리 도구에서 새 사용자를 초대하거나 새 그룹을 만들 수 없게 됩니다. </p> <p>마이그레이션 후: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">관리자는 Adobe Admin Console을 사용하여 Analytics 사용자 및 권한을 관리합니다. (사용자 관리 인터페이스를 더 이상 Analytics &gt; 관리 &gt; 사용자 관리에서 사용하지 않습니다.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">사용자는 <span class="filepath"> my.omniture.com</span> 대신 CX Enterprise를 통해 Adobe 또는 Enterprise ID을 사용하여 Analytics에 액세스합니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 시작 날짜에 어떤 일이 발생합니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 시작 일자 오전 10시(UTC)에: </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Analytics의 기존 권한 그룹은 Adobe Admin Console에서 보고서 세트, 지표, 차원, Analytics 및 보고서 세트 도구에 대한 설명 및 세분화된 권한을 포함한 제품 프로필로서 자동으로 복제됩니다. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">현재 Analytics 사용자 중 Adobe Admin Console에서 생성된 사용자가 있는 경우(즉, 연결된 Adobe/Enterprise ID가 있는 경우) Adobe Admin Console의 해당 제품 프로필에 추가됩니다. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">Analytics의 [관리] 탭에 있는 [사용자 관리] 섹션은 <span class="term">읽기 전용</span>으로 설정됩니다. 여기에서는 새 사용자 또는 권한 그룹을 더 이상 만들 수 없으며 이 두 기능을 모두 Adobe Admin Console에서 수행해야 합니다. 자세한 내용은 <a href="/help/admin/tools/user-management/user-migration/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56">Adobe Admin Console에서 지원되지 않는 Analytics 기능</a>을 참조하십시오. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">관리자는 <a href="/help/admin/tools/user-management/user-migration/c-migration-tool.md">사용자 ID 마이그레이션 도구에 대한 액세스 권한을 부여 받습니다</a>. 또한 도움말 콘텐츠 및 FAQ 링크 외에 마이그레이션 종료 날짜(일반적으로 60일 후)가 포함된 제품 내 알림도 표시됩니다. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">Adobe Admin Console의 권한 탭에 대한 액세스 권한을 부여받아 Analytics에서 익숙한 모든 세분화된 옵션으로 제품 프로필을 만들 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 ID를 마이그레이션하려면 어떻게 해야 합니까? </p> </td> 
   <td colname="col2"> <p> 사용자 관리 아래의 관리 페이지에서 <a href="/help/admin/tools/user-management/user-migration/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9"> 사용자 ID 마이그레이션</a>을 클릭합니다. 도구를 사용하여 사용자를 Adobe Admin Console(Analytics의 권한 그룹에서 복제)의 제품 프로필에 추가합니다. 사용자 ID를 원하는 속도로 마이그레이션할 수 있습니다. </p> <p>관리 권한이 필요합니다. 마이그레이션이 완료되면 되돌릴 수 없습니다. </p> <p>마이그레이션 종료일이 되면 로그인 회사 내 사용자는 <span class="filepath">my.omniture.com</span>에 액세스할 수 없게 됩니다. 사용자(아직 마이그레이션되지 않은 사용자 포함)는 새 CX Enterprise URL(<span class="filepath"> experiencecloud.adobe.com</span>)을 통해 로그인하도록 리디렉션됩니다. </p> <p>참고: 마이그레이션하기 전에 사용자 및 그룹 감사를 수행하는 것이 좋습니다. 오래되고 사용되지 않는 계정 또는 더 이상 제품에 액세스하면 안 되는 계정(예: 더 이상 조직에 있지 않은 직원)은 삭제하십시오. </p> <p>관련 항목: <a href="/help/admin/tools/user-management/user-migration/migrate-enterprise.md"> Enterprise 및 Federated ID에 대한 Analytics 사용자 계정 마이그레이션</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션이 Analytics 구현에 영향을 주거나 데이터를 수집하는 방법에 영향을 줍니까? </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p>마이그레이션 도구는 Analytics 사용자 관리에서 <a href="https://adminconsole.adobe.com/enterprise/"> CX Enterprise Admin Console</a>(으)로 사용자 ID 및 권한을 전환하는 데 도움이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 프로세스는 얼마나 걸립니까? </p> </td> 
   <td colname="col2"> <p>현재 모든 Analytics 관리자는 마이그레이션 4주 전에 마이그레이션 전 알림 이메일을 받게 됩니다. (실제 시작 날짜가 Analytics 인터페이스에 표시됩니다.) </p> <p>마이그레이션이 시작되면 관리자는 프로세스를 완료하는 데 60일이 소요됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션을 신속하게 수행할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예. 하지만 마이그레이션을 시작하기 전에 시간을 가지고 다음 작업을 수행하는 것이 좋습니다. </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">귀하가 Adobe Admin Console에서 Analytics 제품 관리자인지 확인하십시오. </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">마이그레이션이 시작될 때 로그인 경험이 변경됨을 사용자 기반에 전달합니다. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">현재 사용자 및 권한을 감사하고 정리 활동을 수행합니다. </li> 
    </ul> <p>마이그레이션을 더 신속히 처리하려면 <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html"> Adobe 고객 지원 센터</a>의 Adobe 계정 팀에 연락하여 더 빠른 시작일에 대한 요청을 제출하세요. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 저는 Adobe Admin Console에 대한 액세스 권한이 없는 Analytics 관리자입니다. Adobe Admin Console에 대한 액세스 권한을 받는 데 누가 도와줄 수 있습니까? </p> </td> 
   <td colname="col2"> <p>조직의 Adobe Admin Console에 대한 액세스 권한이 있는 모든 시스템 또는 제품 관리자가 액세스 권한을 줄 수 있습니다. 조직 내 콘솔 관리자 권한을 가진 사람을 모르는 경우 <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>에 문의하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 시작 날짜를 연기할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예. <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>에 문의하십시오. </p><p>시작 날짜의 현재 Analytics 사용자 및 권한 관리에 대한 변경 사항 설명은 아래를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이제 내 회사가 Adobe Admin Console로 마이그레이션 중입니다. 마이그레이션 시작 날짜 전에는 새 사용자 및 권한 그룹을 어디에서 만듭니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 시작 날짜 전에는 Adobe Admin Console이나 Analytics &gt; 사용자 관리에서 사용자를 만들 수 있습니다. </p> <p>마이그레이션이 시작되면 Adobe Admin Console에서만 사용자와 권한 그룹을 만들 수 있습니다. </p><p>마이그레이션 시작 날짜에 발생하는 사항에 대한 자세한 내용은 아래 마이그레이션 섹션을 참조하십시오. </p>
   </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 언제 Federated ID를 사용하여 SSO(Single Sign-On)를 구현할 수 있습니까? </p> </td> 
   <td colname="col2"> <p> ID 유형을 Adobe ID에서 Federated ID로 변경할 수 있도록 해 주는 도구를 곧 Adobe Admin Console에서 사용할 수 있습니다. 마이그레이션하는 동안에는 사용자를 Federated ID로 마이그레이션할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 마이그레이션 시 알아야 할 사항(FAQ) {#section-d394524aa6d046d79025bbd7499792bc}

마이그레이션 프로세스와 이 프로세스가 현재 사용자 관리에 미치는 영향에 대한 중요 정보입니다.

<table id="table_0E37BB1DEA6143F0B5F4E861FCFA7189"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>권한 그룹은 Adobe Admin Console에 어떻게 복제됩니까? 내 사용자는 어떻습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션된 Analytics 그룹은 Adobe Admin Console에서 <i>제품 프로필</i>이라고 합니다. 원래 그룹에 대한 권한 설정은 마이그레이션 시 유지됩니다. 하지만 그룹에 할당된 사용자는 마이그레이션되지 않습니다. 해당 그룹에 속한 사용자가 마이그레이션 도구를 사용하여 마이그레이션되면 해당 사용자는 해당 제품 프로필에 지정됩니다. </p> <p>예를 들어 구성원에게 Report Builder 및 Analysis Workspace(특정 보고서 세트, 지표, 차원 사용)에 대한 자격을 부여한 West Coast Operations 권한 그룹은 West Coast Operations 제품 프로필이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 작업을 다른 관리자에게 위임할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션이 시작되면 CX Enterprise 를 통해 Analytics 인스턴스에 액세스하는 모든 관리자는 마이그레이션 도구를 사용하여 사용자 마이그레이션을 시작(또는 계속)할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션되지 않은 사용자의 권한 그룹 멤버십을 업데이트할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예. Analytics [사용자 관리] 섹션에서 마이그레이션되지 않은 사용자의 그룹 멤버십을 변경할 수 있습니다. </p><p>변경 작업이 수행된 위치에 대해서는 Ashok로부터 명확한 답변을 기다리는 중입니다. </p>
   </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션이 시작된 후에 Analytics에서 사용자 및 권한 그룹을 만든 다음 마이그레이션 도구를 사용하여 이를 Adobe Admin Console로 이동할 수 있습니까? </p> </td> 
   <td colname="col2"> <p> 아니요. 마이그레이션이 시작되면 Adobe Admin Console에서 모든 새 사용자 및 권한 그룹(Adobe Admin Console에서 제품 프로필이라고 함)을 만들어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 도구를 사용하여 마이그레이션하는 사용자에게 Analytics에서 수행한 권한과 동일한 권한이 할당됩니까? </p> </td> 
   <td colname="col2"> <p>예. 도구를 사용하여 마이그레이션된 사용자에게는 현재 Analytics에 있는 권한이 부여됩니다. 또한 CX Enterprise를 통해 Analytics에 액세스하면 Analytics 에셋(세그먼트, 프로젝트, 계산된 지표 등)에 대한 액세스 권한을 보유합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제가 Adobe Admin Console로 마이그레이션하는 사용자는 계속 <span class="filepath">my.omniture.com</span>을 사용하여 Analytics에 액세스합니까? </p> </td> 
   <td colname="col2"> <p>예. 마이그레이션된 사용자는 마이그레이션 도구를 통해 기존 로그인 액세스를 사용하지 않도록 지정하지 않는 한 마이그레이션 종료 날짜 전까지 <span class="filepath">my.omniture.com</span>을 통해 계속 기존 사용자 이름과 암호를 사용하여 Analytics에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>내 사용자 중 두 명 이상이 Analytics 레코드에 동일한 이메일 ID를 가지고 있습니다. 마이그레이션하면 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>Adobe Admin Console의 사용자 계정에는 고유한 이메일 ID가 필요하므로 이 사용자 중 둘 이상을 마이그레이션하려면 “중복 이메일 ID” 오류가 발생합니다. 마이그레이션을 다시 시도하기 전에 사용자 관리(기존) 섹션에서 마이그레이션되지 않은 사용자의 이메일 ID를 업데이트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 사용자를 마이그레이션한 후 어떻게 해야 합니까? </p> </td> 
   <td colname="col2"> <p><span class="filepath">my.omniture.com</span>에 대한 기존 로그인 액세스를 비활성화하십시오. 마이그레이션하지 않으면 기존 로그인을 끌 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 프로세스를 추적할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 도구에는 성공적으로 마이그레이션된 사용자 수와 기존 로그인이 비활성화된 사용자 수를 표시하는 대시보드가 포함되어 있습니다. </p> <p> 이상적으로는 사용자의 100%가 마이그레이션을 완료하고 기존 로그인의 사용을 중지한 경우 로그인 회사를 Adobe Admin Console에 성공적으로 마이그레이션하게 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션하는 동안 사용자 및 권한 관리를 수행해야 합니다. 이 작업을 수행하는 데 어떤 도구를 사용할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션이 시작되면 Adobe Admin Console을 사용하여 새 사용자 및 제품 프로필을 만들고 관리하게 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>도구를 사용하여 마이그레이션할 때 사용자의 경험은 어떻습니까? </p> </td> 
   <td colname="col2"> <p>CX Enterprise를 통해 Analytics에 액세스하는 새로운 방법을 알려 주고 Analytics 사용자 레코드에서 이메일 ID로 지정된 환영 이메일을 받게 됩니다. 기존 Adobe ID이 없는 경우 새로 만들라는 메시지가 표시된 후 Adobe ID을 사용하여 솔루션에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 도구를 사용하는 대신 API를 사용하여 사용자를 마이그레이션할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>아니요. 모든 기존 사용자가 Adobe Admin Console로 마이그레이션되었는지 확인하려면 마이그레이션 도구를 사용해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Admin Console에서 사용할 수 없는 Analytics 사용자 관리 기능은 무엇입니까? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">자산 이전 </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">사용자 만료 </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">사용자 로그 </li> 
    </ul> <p>이러한 기능은 Analytics 사용자 관리에서 계속 사용할 수 있습니다. </p> <p>자세한 내용은 <a href="/help/admin/tools/user-management/user-migration/c-migration-tool.md">Adobe Admin Console에서 지원되지 않는 Analytics 기능</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Admin Console에서 여러 구성을 만들고 이를 Analytics 권한 그룹에 매핑했습니다. 마이그레이션이 시작되면 이 구성은 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>Analytics 권한 그룹은 다른 모든 그룹과 마찬가지로 Adobe Admin Console에서 제품 프로필로 다시 만들어집니다. 즉, 본질적으로 중복된 권한이 있는 두 개의 제품 프로필이 콘솔에 표시됩니다. Adobe Admin Console에서 중복된 제품 프로필을 삭제할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자를 마이그레이션한 후 다음 단계는 무엇입니까? </p> </td> 
   <td colname="col2"> <p>사용자 또는 사용자 집합을 마이그레이션한 후 다음 단계는 <span class="filepath">my.omniture.com</span>을 통한 기존 로그인을 비활성화하는 것입니다. 마이그레이션 도구에서 이러한 사용자를 선택하고 화면 상단에 나타나는 상황에 맞는 “기존 로그인 비활성화” 옵션을 클릭하면 됩니다. 이 옵션은 모두 성공적으로 Adobe Admin Console로 마이그레이션된 사용자 또는 사용자 집합을 선택할 때에만 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 종료 당일에는 어떤 일이 일어납니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 종료일(마이그레이션 시작 후 60일) 이후 로그인 회사 내의 모든 사용자는 Adobe ID를 사용하여 CX 엔터프라이즈 로그인 페이지를 통해 로그인하도록 리디렉션됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 종료 날짜까지 모든 사용자를 마이그레이션하지 못했습니다. 마이그레이션되지 않은 사용자는 Analytics에 대한 액세스 권한을 잃게 됩니까? </p> </td> 
   <td colname="col2"> <p>종료 날짜까지 마이그레이션되지 않은 사용자는 CX 엔터프라이즈 로그인 페이지 (experiencecloud.adobe.com)로 리디렉션되고 Analytics에 액세스할 수 없습니다. 그러나 마이그레이션 도구에는 계속 액세스할 수 있으므로 해당 사용자를 찾아 마이그레이션하여 액세스 권한을 복원할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 마이그레이션 후 알아 두어야 할 사항(FAQ) {#section-9681baa01b8c41cdb9659b73b70b50ff}

<table id="table_F48CC9DFE3424AC9AD76A16882701C8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문/문제 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Admin Console에서 사용자 삭제 </p> </td> 
   <td colname="col2"> <p> Analytics에서 삭제된 사용자는 <span class="term">만료</span>로 설정되지만 계정은 계속 존재합니다. 계정을 보존하면 세그먼트, 계산된 지표, 예약된 보고서, 프로젝트 등과 같은 에셋을 전송할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계정 만료 </p> </td> 
   <td colname="col2"> <p> 관리자 도구의 Analytics에서 계정 만료 날짜를 수동으로 설정할 수 있습니다. 만료 날짜가 충족되면 사용자는 Analytics에 액세스할 수 없지만 실제 CX 엔터프라이즈 사용자 계정(예: Adobe ID, Enterprise ID, Federated ID 등)은 액세스할 수 있습니다. 만료되지 않습니다. CX Enterprise에 계속 로그인할 수 있지만 Analytics를 클릭할 수는 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Admin Console에서 지원되지 않는 Analytics 기능 {#section-928ffba27a0446e0af575b720434ef56}

>[!IMPORTANT]
>
>마이그레이션 중에 사용자에게 발생할 수 있는 다음 문제를 검토하십시오.

<table id="table_88E2FA03D5F241B79AB54D12F64B51DA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문/문제 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>다음으로 로그인 </p> </td> 
   <td colname="col2"> <p> Adobe Admin Console로 마이그레이션하는 관리자는 더 이상 “다른 계정으로 로그인” 기능을 사용하여 Adobe Admin Console로 마이그레이션된 비관리자 사용자 계정에 액세스할 수 없습니다. 이 기능은 중단되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 만료 및 에셋 이전 </p> </td> 
   <td colname="col2"> <p> Adobe Admin Console은 사용자 만료나 에셋 이전을 지원하지 않습니다. 관리자는 두 기능 모두에 대해 Analytics의 관리 도구에서 Analytics [사용자 및 에셋] 섹션을 사용하게 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마지막 액세스 (마지막 로그인) </p> </td> 
   <td colname="col2"> <p> 사용자의 마지막 로그인 날짜 및 시간에 대한 세부 정보는 Adobe Admin Console이 아닌 Analytics [사용자 및 에셋] 링크에서 사용할 수 있습니다. Analytics의 마지막 로그인 날짜는 사용자가 CX Enterprise 내에서 실제로 Analytics에 액세스한 시점에 해당하며 CX Enterprise에 로그인한 날짜/시간은 반영하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 관리 API <a href="https://helpx.adobe.com/kr/enterprise/help/identity.html">Adobe 지원 ID 유형</a> </p> </td> 
   <td colname="col2"> <p> Adobe Admin Console으로 마이그레이션하는 관리자는 Adobe Admin Console의 사용자 계정에 프로그래밍 방식으로 액세스하기 위해 Adobe Developer에서 제공되는 사용자 관리 API를 구성해야 합니다. </p> <p>마이그레이션에 대해 활성화되면 Analytics 권한 API가 꺼집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>웹 서비스 자격 증명 </p> </td> 
   <td colname="col2"> <p> 사용자의 웹 서비스 자격 증명(및 공유 암호)은 Adobe Admin Console에서 사용할 수 없으며 Analytics [사용자 및 에셋] 섹션에서 특정 사용자를 클릭하여 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSO(Single Sign-On) </p> </td> 
   <td colname="col2"> <p> 마이그레이션을 완료하면 Analytics SSO(Single Sign-On) 구성이 제거됩니다. 마이그레이션 중에도 활성 상태를 유지합니다. Analytics SSO(Single Sign-On)를 사용하는 고객은 <a href="https://helpx.adobe.com/kr/enterprise/help/identity.html">Adobe Federated ID</a>로 업그레이드해야 합니다. </p> <p>Analytics에서는 먼저 사용자를 Adobe ID로 마이그레이션하여 CX Enterprise 계정을 쉽게 만든 다음 이러한 계정을 Federated SSO(Single Sign) 사용자로 변환하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>권한 그룹 다운로드 </p> </td> 
   <td colname="col2"> <p> 권한 그룹 정보 다운로드는 Analytics 관리 도구 또는 Adobe Admin Console에서 더 이상 지원되지 않습니다. 고객은 adobe.io 사용자 관리 API 를 사용하여 권한 그룹 정보를 일괄적으로 받아야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계정 생성일 </p> </td> 
   <td colname="col2"> <p>계정 생성 날짜 정보는 Analytics 관리 도구 또는 Adobe Admin Console에서 더 이상 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>대량 이메일 </p> </td> 
   <td colname="col2"> <p>Analytics 관리 도구 또는 Adobe Admin Console에서는 사용자에게 보내는 대량 메일을 더 이상 지원하지 않습니다. 고객은 Adobe Admin Console에서 사용자의 이메일 주소를 대량으로 내보내고 원하는 이메일 클라이언트를 사용하여 이메일을 보낼 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
