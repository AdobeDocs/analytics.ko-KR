---
description: Adobe Experience Cloud에서 Admin Console로의 Analytics 사용자 ID 마이그레이션에 대해 알아야 할 사항.
title: Admin Console로 Analytics 사용자 마이그레이션
uuid: 7d020713-693b-4945-aa52-3669a631aacb
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# Admin Console로 Analytics 사용자 마이그레이션{#analytics-user-migration-to-the-admin-console}

Adobe Experience Cloud에서 Admin Console로의 Analytics 사용자 ID 마이그레이션에 대해 알아야 할 사항.

Analytics 마이그레이션과 관련이 없는 Admin Console 주제에 대한 일반적인 도움말은 [Admin Console 사용 안내서](https://helpx.adobe.com/kr/enterprise/administering/user-guide.html)를 참조하십시오.

마이그레이션한 후 관리 콘솔에서 Experience Cloud 사용자 및 제품을 [](https://docs.adobe.com/content/help/ko-KR/core-services/interface/manage-users-and-products/admin-getting-started.html) 관리할 수 있습니다.

## Analytics 사용자 ID 마이그레이션이란 무엇입니까? {#section-adbe49aba10c4e62afa836a97894107c}

관리자는 Analytics 사용자 ID 마이그레이션을 통해 Analytics 사용자 관리의 사용자 계정을 Adobe 관리 콘솔로 쉽게 마이그레이션할 수 있습니다. 사용자가 마이그레이션되면 Experience Cloud에서 사용할 수 있는 솔루션 및 핵심 서비스에 액세스할 수 있습니다. 마이그레이션은 단계별로 고객에게 롤아웃됩니다.

Admin Console을 사용하면 다음과 같은 이점이 있습니다.

<table id="table_E4465796E224474680D750CAC5434ED3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이점 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>단일 사인온 </p> </td> 
   <td colname="col2"> <p>Analytics 사용자는 Adobe ID 또는 Enterprise ID를 사용하여 Experience Cloud 및 모든 솔루션에 로그인할 수 있습니다. 이 로그인을 사용하면 Experience Cloud의 통합 솔루션 및 핵심 서비스에 액세스할 수 있습니다. </p> <p>마이그레이션 후 기존 로그인(<span class="filepath">my.omniture.com</span> 및 <span class="filepath">sc.omniture.com</span>)을 통해 로그인하려는 사용자는 <span class="filepath">experiencecloud.adobe.com</span>으로 리디렉션됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 ID 및 권한 관리 </p> </td> 
   <td colname="col2"> <p>Analytics 관리자는 <a href="http://adminconsole.adobe.com/enterprise/">Admin Console</a> (http://adminconsole.adobe.com/enterprise/) 에서 배타적으로 사용자 및 권한을 관리할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 및 핵심 서비스 관리 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">새 사용자 초대 </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">제품 프로필 만들기 </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">사용자에게 특정 제품 및 서비스에 대한 권한 부여 </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Adobe Experience Cloud에서 사용할 수 있는 <a href="https://docs.adobe.com/content/help/ko-KR/core-services/interface/experience-cloud.html">교차 솔루션 코어 서비스</a>에 대한 액세스 권한을 얻습니다. </li> 
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
   <td colname="col1"> <p>Analytics 관리자로서 사전 마이그레이션 이메일을 받았습니다. 먼저 뭘 해야 하죠? </p> </td> 
   <td colname="col2"> <p>Adobe ID가 있고 <a href="https://adminconsole.adobe.com/enterprise/">Experience Cloud Admin Console</a>에 액세스할 수 있는지 확인하십시오. </p> <p>그렇지 않은 경우 <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>에 문의하십시오. (사용자를 적절한 조직에 초대할 수 있는 시스템 또는 제품 관리자에게 먼저 문의해야 합니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics와 AEM 통합 </p> </td> 
   <td colname="col2"> <p> Analytics와 통합된 AEM 사용자는 암호 대신 Analytics 공유 암호를 사용하도록 구성을 변경해야 합니다. </p> <p> 이 작업은 마이그레이션이 활성화되기 전에 수행해야 합니다. 마이그레이션이 비활성화되면 원래 구성된 암호는 더 이상 유효하지 않습니다. </p> <p><b>Analytics에서 공유 암호를 가져오려면</b> </p> <p> 공유 암호는 Analytics(<span class="uicontrol">Analytics</span> &gt; <span class="uicontrol">사용자 관리</span>)에서 확보할 수 있으며 서로 다릅니다. </p> <p><b>공유 암호로 AEM 구성을 업데이트하는 방법</b> </p> <p><a href="https://helpx.adobe.com/kr/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html">Adobe Analytics 연결 및 프레임워크 생성</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder 업데이트 </p> </td> 
   <td colname="col2"> <p> <p>중요: <a href="https://marketing.adobe.com/resources/help/ko_KR/arb/t_install_arb.html">Report Builder</a>의 설치를 최신 버전으로 업데이트합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션은 언제 시작됩니까? </p> </td> 
   <td colname="col2"> <p>Adobe는 마이그레이션이 시작되는 시기에 대한 지침이 포함된 이메일을 통해 Analytics 관리자에게 알립니다. </p> <p>Admin Console로의 마이그레이션은 물결에서 발생합니다. 마이그레이션 당일 Adobe는 Analytics 관리자에게 알리고 마이그레이션 도구에 대한 액세스 권한을 부여합니다. 로그인 회사가 각 마이그레이션 웨이브에 대해 정의된 기준을 충족하면 Adobe는 다음 작업을 수행합니다. </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">회사 마이그레이션의 시작 날짜와 종료 날짜를 설정합니다. </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">마이그레이션 약 30일 전에 회사의 현재 Analytics 관리자에게 이메일 알림을 보냅니다. </li> 
     <li id="li_476265B24CE2404B995201170C75D674">관리자에게 마이그레이션 시작 날짜를 알려주는 제품 내 알림을 표시합니다. </li> 
    </ul> <p> 이전 권한 그룹은 마이그레이션이 진행되는 날 Admin Console에 자동으로 복사됩니다. 더 이상 Analytics 관리 도구에서 새 사용자를 초대하거나 새 그룹을 만들 수 없게 됩니다. </p> <p>마이그레이션 후: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">관리자는 관리 콘솔을 사용하여 Analytics 사용자 및 권한을 관리합니다. (Analytics &gt; 관리 &gt; 사용자 관리에서 더 이상 사용자 관리 인터페이스를 사용하지 않습니다.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">사용자는 <span class="filepath">my.omniture.com</span> 대신 Experience Cloud를 통해 Adobe 또는 Enterprise ID를 사용하여 Analytics에 액세스합니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 시작 날짜에 어떤 일이 발생합니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 시작 날짜의 오전 10시(UTC): </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Analytics의 기존 권한 그룹은 보고서 세트, 지표, 차원, 분석 및 보고서 세트 도구에서 설명 및 세부적인 권한을 포함하여 관리 콘솔에 제품 프로필로 자동으로 복제됩니다. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">현재 Analytics 사용자가 관리 콘솔에서 만들어진 경우(즉, 연결된 Adobe/Enterprise ID가 있음) 관리 콘솔의 해당 제품 프로필에 추가됩니다. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">Analytics의 관리 탭 아래에 있는 사용자 관리 섹션은 <span class="term"> 읽기 전용으로</span>설정됩니다. 여기에서는 새 사용자 또는 권한 그룹을 더 이상 만들 수 없으며 이 두 기능을 모두 Admin Console에서 수행해야 합니다. 자세한 내용은 <a href="/help/admin/user-management2/user-migration/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56">Admin Console에서 지원되지 않는 Analytics 기능</a>을 참조하십시오. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">관리자는 사용자 ID 마이그레이션 <a href="https://marketing.adobe.com/resources/help/ko_KR/experience-cloud/admin-console/analytics-migration/t_migrate-users.html">도구에</a>대한 액세스 권한이 부여됩니다. 또한, 도움말 컨텐츠 및 FAQ에 대한 링크와 함께 마이그레이션 종료 날짜(일반적으로 향후 60일)를 포함하는 제품 내 알림이 표시됩니다. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">Analytics에 익숙한 모든 세부 옵션을 사용하여 제품 프로필을 만들 수 있는 관리 콘솔의 권한 탭에 대한 액세스 권한이 부여됩니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 ID는 어떻게 마이그레이션합니까? </p> </td> 
   <td colname="col2"> <p> Click <a href="/help/admin/user-management2/user-migration/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9"> Migrate User IDs</a> on the Admin page, under User Management. 이 도구를 사용하여 관리 콘솔에서 제품 프로필에 사용자를 추가합니다(Analytics의 권한 그룹에서 복제). 사용자 ID를 원하는 속도로 마이그레이션할 수 있습니다. </p> <p>관리 권한이 필요합니다. 마이그레이션이 완료되면 되돌릴 수 없습니다. </p> <p>마이그레이션 종료일이 되면 로그인 회사 내 사용자는 <span class="filepath">my.omniture.com</span>에 액세스할 수 없게 됩니다. 사용자(아직 마이그레이션되지 않은 사용자 포함)는 새 Experience Cloud URL(<span class="filepath"> experiencecloud.adobe.com</span>)을 통해 로그인하도록 리디렉션됩니다. </p> <p>참고: 마이그레이션하기 전에 사용자 및 그룹 감사를 수행하는 것이 좋습니다. 오래되고 사용되지 않는 계정 또는 더 이상 제품에 액세스하면 안 되는 계정(예: 더 이상 조직에 있지 않은 직원)은 삭제하십시오. </p> <p>관련 항목: <a href="/help/admin/user-management2/user-migration/migrate-enterprise.md"> Enterprise 및 Federated ID에 대한 Analytics 사용자 계정 마이그레이션</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션이 Analytics 구현에 영향을 줍니까 또는 데이터가 어떻게 수집됩니까? </p> </td> 
   <td colname="col2"> <p>아니요. </p> <p>마이그레이션 도구는 Analytics 사용자 관리의 사용자 ID 및 권한을 <a href="https://adminconsole.adobe.com/enterprise/">Experience Cloud Admin Console</a>로 이전하는 것을 돕기 위한 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 프로세스는 얼마나 걸립니까? </p> </td> 
   <td colname="col2"> <p>현재 모든 Analytics 관리자는 마이그레이션 4주 전에 사전 마이그레이션 알림 이메일을 수신하게 됩니다. (실제 시작 날짜는 Analytics 인터페이스에 표시됩니다.) </p> <p>마이그레이션이 시작되면 관리자는 60일 동안 프로세스를 완료해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션을 신속하게 수행할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예. 그러나 Adobe에서는 마이그레이션이 시작되기 전에 다음 시간으로 지정하는 것이 좋습니다. </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">관리 콘솔에서 Analytics 제품 관리자인지 확인합니다. </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">마이그레이션이 시작되면 로그인 경험이 변경되도록 사용자 기반에 알립니다. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">현재 사용자 및 권한을 감사하고 정리 활동을 수행합니다. </li> 
    </ul> <p>마이그레이션을 더 신속히 처리하려면 <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>의 고객 성공 관리자에게 문의하여 더 빠른 시작일 요청을 제출하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 관리 콘솔에 액세스할 수 없는 Analytics 관리자입니다. Admin Console을 이용하는 데 도움이 되는 사용자는 누구입니까? </p> </td> 
   <td colname="col2"> <p>조직의 Admin Console에 대한 액세스 권한이 있는 모든 시스템 또는 제품 관리자가 액세스 권한을 줄 수 있습니다. 조직 내 콘솔 관리자 권한을 가진 사람을 모르는 경우 <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>에 문의하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 시작 날짜를 연기할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예. <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Adobe 고객 지원</a>에 문의하십시오. </p> 
    <draft-comment> 
     <p>시작 날짜의 현재 Analytics 사용자 및 권한 관리에 대한 변경 사항 설명은 아래를 참조하십시오. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이제 회사에서 Admin Console로 마이그레이션하고 있으므로 마이그레이션 시작 날짜 전에 새 사용자 및 권한 그룹을 어디에서 만들 수 있습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 시작 날짜 전에 관리 콘솔 또는 Analytics &gt; 사용자 관리에서 사용자를 만들 수 있습니다. </p> <p>마이그레이션이 시작되면 관리 콘솔에서 사용자 및 권한 그룹만 만들 수 있습니다. </p> 
    <draft-comment> 
     <p>마이그레이션 시작 날짜에 발생하는 사항에 대한 자세한 내용은 아래 마이그레이션 섹션을 참조하십시오. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Federated ID를 사용하여 SSO(Single Sign-On)를 언제 구현할 수 있습니까? </p> </td> 
   <td colname="col2"> <p> Admin Console에서 ID 유형을 Adobe ID에서 Federated ID로 변경할 수 있는 툴을 곧 사용할 수 있습니다. 마이그레이션 중에는 사용자를 Federated ID로 마이그레이션할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 마이그레이션 중 알아야 할 사항(FAQ) {#section-d394524aa6d046d79025bbd7499792bc}

마이그레이션 프로세스와 마이그레이션 프로세스가 현재 사용자 관리에 미치는 영향에 대한 중요한 정보입니다.

<table id="table_0E37BB1DEA6143F0B5F4E861FCFA7189"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>권한 그룹은 관리 콘솔에 어떻게 복제됩니까? 사용자는 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션된 Analytics 그룹은 관리 콘솔에서 <i>제품</i> 프로필이라고 합니다. 원래 그룹에 대한 권한 설정은 마이그레이션에서 유지됩니다. 하지만 그룹에 할당된 사용자는 마이그레이션되지 않습니다. 해당 그룹에 속한 사용자가 마이그레이션 도구를 사용하여 마이그레이션되면 해당 사용자가 해당 제품 프로필에 할당됩니다. </p> <p>예를 들어, 특정 보고서 세트, 지표, 차원이 있는 Report Builder 및 분석 작업 공간에 해당 멤버를 권한이 부여했던 West Coast Operations 권한 그룹은 West Coast Operations 제품 프로필이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다른 관리자에게 마이그레이션 작업을 위임할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션이 시작되면 Experience Cloud를 통해 Analytics 인스턴스에 액세스하는 모든 관리자가 마이그레이션 도구를 사용하여 사용자 마이그레이션을 시작하거나 계속할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션되지 않은 사용자의 권한 그룹 멤버십을 업데이트할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예. Analytics 사용자 관리 섹션에서 마이그레이션되지 않은 사용자의 그룹 구성원을 변경할 수 있습니다. </p> 
    <draft-comment> 
     <p>변경 작업이 수행된 위치에 대해서는 Ashok로부터 명확한 답변을 기다리는 중입니다.  </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션을 시작한 후 Analytics에서 사용자 및 권한 그룹을 만든 다음 마이그레이션 도구를 사용하여 관리 콘솔로 이동할 수 있습니까? </p> </td> 
   <td colname="col2"> <p> 아니요. 마이그레이션이 시작되면 모든 새 사용자 및 권한 그룹(관리 콘솔의 제품 프로필이라고 함)이 관리 콘솔에서 만들어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 도구를 사용하여 마이그레이션해야 하는 사용자에게 Analytics에 있었던 것과 동일한 권한이 할당됩니까? </p> </td> 
   <td colname="col2"> <p>예. 도구를 사용하여 마이그레이션된 사용자는 현재 Analytics에서 보유하고 있는 권한이 부여됩니다. 또한 Experience Cloud를 통해 Analytics에 액세스할 때 Analytics 자산(세그먼트, 프로젝트, 계산된 지표 등)에 대한 액세스 권한을 보유하게 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제가 Admin Console로 마이그레이션하는 사용자는 계속 <span class="filepath">my.omniture.com</span>을 사용하여 Analytics에 액세스합니까? </p> </td> 
   <td colname="col2"> <p>예. 마이그레이션된 사용자는 마이그레이션 도구를 통해 기존 로그인 액세스를 사용하지 않도록 지정하지 않는 한 마이그레이션 종료 날짜 전까지 <span class="filepath">my.omniture.com</span>을 통해 계속 기존 사용자 이름과 암호를 사용하여 Analytics에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>두 명 이상의 사용자가 Analytics 레코드에 동일한 이메일 ID가 있습니다. 마이그레이션하면 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>Admin Console의 사용자 계정에는 고유한 이메일 ID가 필요하므로 이러한 사용자 중 두 명 이상을 마이그레이션하려고 하면 "중복된 이메일 ID" 오류가 발생합니다. 마이그레이션을 다시 시도하기 전에 사용자 관리(레거시) 섹션에서 마이그레이션되지 않은 사용자의 이메일 ID를 업데이트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 사용자를 마이그레이션한 후 어떻게 해야 합니까? </p> </td> 
   <td colname="col2"> <p><span class="filepath">my.omniture.com</span>에 대한 기존 로그인 액세스를 비활성화하십시오. 마이그레이션되지 않으면 기존 로그인을 끌 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 프로세스를 추적할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 도구에는 성공적으로 마이그레이션된 사용자 수와 기존 로그인이 비활성화된 사용자 수가 표시되는 대시보드가 포함되어 있습니다. </p> <p> 사용자 중 100%가 마이그레이션을 완료하고 기존 로그인을 비활성화한 경우 로그인 회사를 Admin Console로 성공적으로 마이그레이션하게 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 중에 사용자 및 권한 관리를 수행해야 합니다. 이 작업을 수행하는 데 사용할 수 있는 도구는 무엇입니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션이 시작되면 Admin Console을 사용하여 새 사용자 및 제품 프로필을 만들고 관리할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이 도구를 사용하여 사용자를 마이그레이션할 때 사용자 환경은 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>이들은 Analytics 사용자 레코드의 이메일 ID로 주소가 지정된 환영 이메일을 수신하게 되며, Experience Cloud를 통해 Analytics에 액세스하는 새로운 방법을 알려 줍니다. 기존 Adobe ID가 없는 경우 Adobe ID를 만들라는 메시지가 표시되고, 그 후에는 Adobe ID를 사용하여 솔루션에 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 도구를 사용하는 대신 API를 사용하여 사용자를 마이그레이션할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>아니요. 마이그레이션 도구를 사용하여 모든 기존 사용자가 관리 콘솔로 마이그레이션되도록 해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>관리 콘솔에서 사용할 수 없는 Analytics 사용자 관리 기능은 무엇입니까? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">자산 전송 </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">사용자 만료 </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">사용자 로그 </li> 
    </ul> <p>Analytics 사용자 관리에서는 이러한 기능을 계속 사용할 수 있습니다. </p> <p>자세한 내용은 <a href="/help/admin/user-management2/user-migration/c-migration-tool.md">Admin Console에서 지원되지 않는 Analytics 기능</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>관리 콘솔에서 여러 구성을 만들고 Analytics 권한 그룹에 매핑했습니다. 마이그레이션이 시작되면 이러한 구성은 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>Analytics 권한 그룹은 다른 모든 그룹과 마찬가지로 관리 콘솔에서 제품 프로필로 다시 만들어집니다. 즉, 콘솔에 중복된 권한이 있는 두 개의 제품 프로필이 표시됩니다. 관리 콘솔에서 중복된 제품 프로필을 삭제할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자를 마이그레이션한 후 다음 단계는 무엇입니까? </p> </td> 
   <td colname="col2"> <p>사용자 또는 사용자 집합을 마이그레이션한 후 다음 단계는 <span class="filepath">my.omniture.com</span>을 통한 기존 로그인을 비활성화하는 것입니다. 마이그레이션 도구에서 이러한 사용자를 선택하고 화면 상단에 나타나는 컨텍스트 기반의 "기존 로그인 비활성화" 옵션을 클릭하면 됩니다. 이 옵션은 모두 관리 콘솔로 성공적으로 마이그레이션된 사용자 또는 사용자 집합을 선택하는 경우에만 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 종료 날짜는 어떻게 됩니까? </p> </td> 
   <td colname="col2"> <p>마이그레이션 종료 날짜(마이그레이션 시작일부터 60일) 이후 로그인 회사 내의 모든 사용자는 Adobe ID를 사용하여 Experience Cloud 로그인 페이지를 통해 로그인으로 리디렉션됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마이그레이션 종료 날짜까지 모든 사용자를 마이그레이션할 수 없습니다. 마이그레이션되지 않은 사용자는 Analytics에 액세스할 수 없습니까? </p> </td> 
   <td colname="col2"> <p>종료 날짜까지 마이그레이션되지 않은 사용자는 Experience Cloud 로그인 페이지(experiencecloud.adobe.com)로 리디렉션되고 Analytics에 액세스할 수 없습니다. 그러나 마이그레이션 도구에는 계속 액세스할 수 있으므로 해당 사용자를 찾아 마이그레이션하여 액세스 권한을 복원할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 마이그레이션 후 알아야 할 사항(FAQ) {#section-9681baa01b8c41cdb9659b73b70b50ff}

<table id="table_F48CC9DFE3424AC9AD76A16882701C8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문/문제 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>관리 콘솔에서 사용자 삭제 </p> </td> 
   <td colname="col2"> <p> Analytics에서 삭제된 사용자는 <span class="term"> 만료됨으로</span>설정되지만 계정은 계속 존재합니다. 계정을 보존하면 세그먼트, 계산된 지표, 예약된 보고서, 프로젝트 등과 같은 자산을 전송할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계정 만료 </p> </td> 
   <td colname="col2"> <p> 관리 도구의 Analytics에서 계정 만료 날짜를 수동으로 설정할 수 있습니다. 만료 날짜가 충족되면 사용자는 Analytics에 액세스할 수 없지만 실제 Experience Cloud 사용자 계정(예: Adobe ID, Enterprise ID, Federated ID 등)에 액세스할 수 있습니다. 만료되지 않습니다. Adobe Experience Cloud에 계속 로그인할 수 있지만 Analytics를 클릭하지 못할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Admin Console에서 지원되지 않는 Analytics 기능 {#section-928ffba27a0446e0af575b720434ef56}

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
   <td colname="col1"> <p>다른 이름으로 로그인 </p> </td> 
   <td colname="col2"> <p> Admin Console로 마이그레이션하는 관리자는 더 이상 "다른 이름으로 로그인" 기능을 사용하여 관리 콘솔로 마이그레이션된 비관리 사용자 계정에 액세스할 수 없습니다. 이 기능은 Analytics에서 더 이상 사용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 만료 및 자산 전송 </p> </td> 
   <td colname="col2"> <p> 관리 콘솔은 사용자 만료 또는 자산 전송을 지원하지 않습니다. 관리자는 Analytics의 관리 도구 아래에 있는 Analytics 사용자 및 자산 섹션을 두 기능에 모두 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마지막 액세스(마지막 로그인) </p> </td> 
   <td colname="col2"> <p> 사용자의 마지막 로그인 날짜와 시간에 대한 세부 사항은 관리 콘솔이 아니라 Analytics 사용자 및 자산 링크에서 사용할 수 있습니다. Analytics의 마지막 로그인 날짜는 사용자가 Experience Cloud 내에서 실제로 Analytics에 액세스한 시점에 해당하며 Experience Cloud에 로그인한 날짜/시간은 반영하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 관리 API <a href="https://helpx.adobe.com/kr/enterprise/help/identity.html">Adobe 지원 ID 유형</a> </p> </td> 
   <td colname="col2"> <p> Admin Console로 마이그레이션하는 관리자는 Admin Console의 사용자 계정에 프로그래밍 방식으로 액세스하기 위해 Adobe I/O에서 제공되는 <a href="https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html">사용자 관리 API</a>를 구성해야 합니다. </p> <p>마이그레이션을 활성화하면 Analytics 권한 API가 꺼집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>웹 서비스 자격 증명 </p> </td> 
   <td colname="col2"> <p> 사용자의 웹 서비스 자격 증명(및 해당 공유 암호)은 관리 콘솔에서 사용할 수 없으며 Analytics 사용자 및 자산 섹션에서 특정 사용자를 클릭하여 액세스할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>단일 사인온 </p> </td> 
   <td colname="col2"> <p> 마이그레이션을 완료하면 Analytics Single Sign-On 구성이 제거됩니다. 마이그레이션 중에는 활성 상태로 유지됩니다. Analytics 단일 사인온을 사용하는 고객은 <a href="https://helpx.adobe.com/kr/enterprise/help/identity.html">Adobe Federated ID</a>로 업그레이드해야 합니다. </p> <p>Adobe ID로 사용자를 마이그레이션하여 Experience Cloud 계정을 쉽게 만든 다음 이러한 계정을 Federated SSO 사용자로 전환하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>권한 그룹 다운로드 </p> </td> 
   <td colname="col2"> <p> Analytics 관리 도구 또는 Adobe 관리 콘솔에서 권한 그룹 정보 다운로드가 더 이상 지원되지 않습니다. 고객은 adobe.io 사용자 관리 API를 사용하여 권한 그룹 정보를 대량으로 가져와야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계정 생성 날짜 </p> </td> 
   <td colname="col2"> <p>계정 생성 날짜 정보는 더 이상 Analytics 관리 도구 또는 Adobe 관리 콘솔에서 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일괄 이메일 </p> </td> 
   <td colname="col2"> <p>Analytics 관리 콘솔 또는 Adobe 관리 콘솔에서 사용자에게 대량 전자 메일을 더 이상 지원하지 않습니다. 고객은 Adobe Admin Console에서 사용자의 이메일 주소를 일괄 내보내고 원하는 이메일 클라이언트를 사용하여 이메일을 보낼 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 마이그레이션에 대해 사용자에게 알리는 방법 {#section-f3b25f672a3a4d03b0559656fd99d20a}

이 마이그레이션 계획을 현재 사용자에게 적극적으로 알릴 수도 있습니다. 다음은 현재 모든 Analytics 사용자를 전송하도록 사용자 지정할 수 있는 템플릿입니다.

모든 사용자를 이메일로 전송하려면 > **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** 이메일 사용자로 [이동합니다](https://marketing.adobe.com/resources/help/ko_KR/reference/t_email_users.html).

**제목:** 예고 - Adobe Analytics 및 Adobe Experience Cloud에 로그인하는 새로운 방법

**본문:** Adobe Analytics 사용자 여러분 안녕하세요!

당사는 모든 Adobe Analytics 계정을[!DNL https://my.omniture.com/login/] 에서 Adobe Experience Cloud([experiencecloud.adobe.com](http://experiencecloud.adobe.com/))로 마이그레이션하는 작업을 시작할 예정입니다. 이 마이그레이션을 통해 Adobe Experience Cloud를 통해 Analytics에 액세스할 수 있도록 Adobe Analytics 계정이 업그레이드됩니다. Analytics에 액세스하는 방법이 변경되더라도 보고서 세트 및 도구에 대한 기존의 모든 권한이 유지됩니다.

**다음 단계:** 사용자 마이그레이션 시작 시기: **날짜를 삽입합니다**. Analytics 계정 아래에 나열된 이메일 ID로 새 로그인 주소가 지정된 시작 메시지를 확인하십시오. 이메일 주소에 연결된 Adobe [ID를](https://helpx.adobe.com/kr/x-productkb/global/adobe-id-account-change.html) 설정하지 않은 경우 계정을 설정하라는 메시지가 표시됩니다.

**유용한 리소스:**

[로그인 및 프로필 설정 관리](https://marketing.adobe.com/resources/help/ko_KR/mcloud/getting-started-experience-cloud.html).

[Experience Cloud의 클라우드, 핵심](https://marketing.adobe.com/resources/help/en_US/mcloud/solutions_capability_names.html) 서비스 및 솔루션 정보

질문이나 우려 사항이 있는 경우 Analytics 관리자에게 문의하십시오.

최고,

Analytics 관리
