---
description: 데이터 커넥터 통합 마법사는 데이터 커넥터 통합 프로세스를 단계별로 안내합니다.
seo-description: 데이터 커넥터 통합 마법사는 데이터 커넥터 통합 프로세스를 단계별로 안내합니다.
seo-title: 데이터 커넥터 통합 마법사 실행
title: 데이터 커넥터 통합 마법사 실행
uuid: 714417 f 7-c 1 df -4 e 61-a 07 f-d 319 f 6581 c 9 c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d55b23a5baf5be1d7afb708cc6ef94851eac3e77

---


# Running the Data Connectors Integration Wizard{#running-the-data-connectors-integration-wizard}

데이터 커넥터 통합 마법사는 데이터 커넥터 통합 프로세스를 단계별로 안내합니다.

통합을 구성하려면 다음을 수행하십시오.

1. Marketing Cloud에 로그인합니다.
1. Adobe Analytics 홈 페이지에서 핀휠 또는 도구 모음의 데이터 커넥터™ 아이콘을 클릭합니다.
1. 데이터 커넥터 페이지에서 통합을 구성할 보고서 세트를 선택합니다.

   >[!NOTE]
   >
   >Make sure that you select the desired report suite from the **Report Suite** drop-down list in the upper-left corner of the Data Connectors page.

1. Click the **Alphabetical** tab at the top of the **Partner List** on the left side of the Data Connectors UI, then locate the **Datran** icon.
1. Drag the **Datran** icon to an empty plug-in slot in your Adobe Analytics report suite to launch the Data Connectors Integration Wizard.

1. On the Datran Integration introduction page, review the text, then select the check box to accept the fees associated with the integration, then click **Next**.

   이 페이지는 자세한 정보에 대한 유용한 링크와 함께 통합 개요를 제공합니다. 이 통합과 연관된 Adobe 및 Datran 요금이 모두 있습니다. 두 조직에 적합한 영업 담당자에게 연락하여 요금 구성을 확인합니다.
1. 다음 표에 설명된 대로 데이터 커넥터 통합 마법사의 각 페이지에서 필요한 정보를 제공합니다.

<table id="table_74EC1EEBE7A548AB878AA40187EBCD30"> 
 <thead> 
  <tr valign="top"> 
   <th colname="col1" valign="top" align="left" class="entry"> <p><b>마법사 페이지 #</b> </p> </th> 
   <th colname="col2" class="entry"> <p><b>field</b> </p> </th> 
   <th colname="col3" class="entry"> <p><b>description</b> </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2" valign="top" align="left"> <p>통합 이름 </p> </td> 
   <td colname="col3"> <p>보고서 세트의 활성 통합 목록에 데이터 커넥터가 표시되는 통합 이름을 지정합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>통합 이메일 주소 </p> </td> 
   <td colname="col3"> <p>Specify the email address that receives all notifications related to this integration, then click <b>Next</b> to proceed to Step 2 of the Wizard. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>계정 ID </p> </td> 
   <td colname="col3"> <p>Specify your Datran Account ID (the unique identifier assigned to your organization by Datran), then click <b>Next</b> to proceed to Step 3 of the Wizard. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>메시지 ID </p> </td> 
   <td colname="col3"> <p>이메일 메시지 ID를 추적하는 데 사용되는 Adobe Analytics evar를 식별합니다. </p> <p>메시지 ID는 마케팅/리마케팅 캠페인에 사용됩니다. 메시지 ID를 "추적 코드" 라고도 합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Recipient ID </p> </td> 
   <td colname="col3"> <p>이메일 수신자 ID를 추적하는 데 사용되는 Adobe Analytics evar를 식별합니다. </p> <p>수신자 ID는 마케팅/리마케팅 캠페인에 사용됩니다. 메시지 ID는 종종 "방문자 코드" 라고도 합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>수락 확인란 </p> </td> 
   <td colname="col3"> <p>수락 확인란 옆에 표시되는 정보를 검토합니다. </p> <p><i>" 수신자 ID "추적을 활성화함으로써 이 기능은 사이트 방문자의 개인 식별 정보를 추적할 수 있다는 것을 이해합니다. This has privacy implications requiring the implementation of appropriate procedures by my organization, such as providing notice to, and consent of, our site visitors. </i> </p> <p>If you agree to the acceptance statement, select the check box, then click <b>Next</b> to proceed to Step 4 of the Wizard. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>클라이언트가 정의한 보고서 세트 수준 세그먼트 </p> </td> 
   <td colname="col3"> <p>이 통합은 통합 마법사의 통합 세그먼트 페이지 왼쪽에 파트너 정의된 세그먼트를 만듭니다. </p> <p>또한, 통합에 포함할 기존 보고서 세트 수준 세그먼트를 선택할 수 있습니다. </p> <p>Select the desired segments on the right side of the page, then click <b>Next</b> to proceed to Step 5 of the Wizard. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>클릭함 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 클릭된 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>클릭한 이벤트를 통해 이메일 메시지를 클릭한 방문자 수를 확인할 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>열림 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 데이터를 이메일로 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>열린 이벤트를 통해 이메일 메시지를 연 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sent </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>클릭한 이벤트를 통해 전송된 이메일 메시지 수를 확인할 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>총 바운스 수 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 토탈 바운스 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>Total-Bounces 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>가입 해지 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 구독 취소 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>가입 취소된 이벤트는 이메일 메시지를 연 다음, 조직의 향후 이메일 메시지를 옵트아웃하는 구독 취소 링크를 클릭한 방문자 수를 볼 수 있도록 해줍니다. </p> <p>다음을 클릭하여 마법사의 6 단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p>데이터 수집: JavaScript 플러그인 </p> </td> 
   <td colname="col3"> <p>Select <b>JavaScript Plug-in</b> if you want to use the plug-in as the collection model for this integration, then click <b>Next</b> to proceed to Step 7 of the Wizard. </p> <p> <p>참고: 자동화된 솔루션이 기본 선택입니다. </p> </p> <p>이 통합에 사용되는 JavaScript 플러그인 사본을 다운로드하려면 Adobe 컨설턴트에게 문의하십시오. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p>데이터 수집: 자동화된 솔루션 </p> </td> 
   <td colname="col3"> <p>Select <b>Automated Solution</b> if you want to use an automated collection model for this integration, then specify the unique identifiers used for this integration. </p> <p> <p>참고: 자동화된 솔루션이 기본 선택입니다. </p> </p> <p>이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다. </p> <p><b>메시지 ID 쿼리 문자열 매개 변수:</b>이 값은 이메일 파트너가 랜딩 페이지 URL에 첨부한 메시지 ID를 나타냅니다. </p> <p><b>수신자 ID 쿼리 문자열 매개 변수:</b> 이 값은 이메일 파트너가 랜딩 페이지 URL에 첨부한 수신자 ID를 나타냅니다. </p> <p>Click <b>Next</b> to proceed to Step 7 of the Wizard. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>통합 요약 </p> </td> 
   <td colname="col3"> <p>Verify the integration parameters by clicking the plus sign (+) next to each category, then click <b>Save</b> to proceed to Step 8 of the Wizard. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p>통합 완료 </p> </td> 
   <td colname="col3"> <p><b>마침을</b> 클릭하여 통합을 완료합니다. </p> <p><b>중요:</b> Adobe Analytics 에서는 <b>[마침</b>] 를 클릭할 때까지 통합 설정을 저장하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

