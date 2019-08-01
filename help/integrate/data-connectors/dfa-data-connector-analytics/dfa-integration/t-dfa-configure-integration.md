---
description: DFA Data Connectors 통합을 단계별로 안내합니다.
seo-description: DFA Data Connectors 통합을 단계별로 안내합니다.
seo-title: DFA 통합 구성
title: DFA 통합 구성
uuid: 4 C 2 AC 58 A -87 C 6-46 F 3-9033-9404 BEB 18 C 39
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# DFA 통합 구성{#configure-the-dfa-integration}

DFA Data Connectors 통합을 단계별로 안내합니다.

이 구성 페이지는 자세한 정보에 대한 유용한 링크와 함께 통합 개요를 제공합니다. 이 통합과 관련된 Adobe와 DoubleClick 요금이 있습니다. 두 조직에 적합한 영업 담당자에게 연락하여 요금 구성을 확인합니다.

1. Log in to the [!DNL Adobe Analytics].
1. **[!UICONTROL 관리]** &gt; **[!UICONTROL 데이터 커넥터를 클릭합니다]**.

   ![](assets/data_connectors.png)

1. **[!UICONTROL Doubleclick DFA]**&#x200B;를 찾은 다음 새로 **[!UICONTROL 추가를 클릭합니다]**.

   ![단계 결과](assets/wizard-01.png)

   통합 마법사의 각 페이지에서 필요한 정보를 제공하고 **[!UICONTROL 다음을 클릭합니다]**. 다음 표는 마법사를 통해 통합을 완료하는 데 필요한 정보를 설명합니다.

<table id="table_8F6F7F304C36431DA5FD6E5D54F60FC0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 마법사 페이지 # </th> 
   <th colname="col2" class="entry"> 필드 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> 통합 이름 </td> 
   <td colname="col3"> Genesis가 보고서 세트의 활성 통합 목록에 표시하는 통합 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> 통합 이메일 주소 </td> 
   <td colname="col3"> 이 통합과 관련된 모든 알림을 수신하는 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> 사용자 이름 </td> 
   <td colname="col3"> 이 통합에서 사용하는 DFA API 사용자 이름입니다. API 로그인을 위해 사용자를 활성화하려면 DFA 인터페이스에서 API 속성을 선택합니다. API 로그인을 활성화하면 사용자 암호를 제공하는 암호 필드가 표시됩니다. 인증할 마법사에 사용자 이름과 함께 이 암호를 입력합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> 암호 </td> 
   <td colname="col3"> DFA API 암호입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> 광고주 ID </td> 
   <td colname="col3"> <p>DFA 광고주 ID 또는 상위 Floodlight 구성 ID입니다. Data Connectors는 이 ID를 사용하여 추적할 DFA 광고주를 식별합니다(통합 버전 1.5). 이 광고주 ID는 통합의 버전 2.0에서 사용되지 않습니다. 상위 Floodlight 구성 ID가 조회 및 사용됩니다. 화면의 지침 참조 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3 </td> 
   <td colname="col2"> DFA 광고 변수 </td> 
   <td colname="col3"> DFA 캠페인 속성, 노출 횟수 및 클릭 수 데이터를 받는 Analytics eVar입니다. 일반적으로 추적 코드 eVar( <span class="varname"> s. campaign </span>) 를 사용하지만 사용 가능한 evar를 선택할 수 있습니다. Data Connectors는 다음 DFA 관련 분류를 선택한 eVar에도 추가합니다. <p><b>캠페인</b>: 일반 메시지를 전달하는 여러 사이트에 게재된 광고 모음입니다. </p> <p><b>사이트 이름</b>: 광고가 게재된 사이트입니다. </p> <p><b>광고 이름</b>: DFA 계정에 정의된 광고 이름입니다. </p> <p><b>사이트 게재위치 이름</b>: 광고가 게재된 웹 사이트 및 페이지입니다. </p> <p><b>배달 도구</b>: 광고주용 DoubleClick입니다. </p> <p><b>채널</b>: 배너 광고입니다. </p> <p><b>비용 구성</b>: 광고 비용 구성에 따라 CPM, CPC 또는 고정입니다. </p> <p><b>광고 소재 이름</b>: 광고/게재위치/광고 ID와 관련된 광고 소재 이름입니다. </p> <p><b>DFA &gt; SearchCenter 중복 제거</b>: DFA는 DFA 클릭스루 또는 뷰스루가 발생하는 Searchcenter 변수에 값을 배치하도록 지정합니다. 자세한 내용은 <a href="../../dfa-data-connector-analytics/dfa-integration-features.md#concept-ff93289d1662410e98f62c200394b3e3" format="dita" scope="local">SearchCenter 중복 제거</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> 노출 횟수 </td> 
   <td colname="col3"> DFA 노출 횟수 지표 데이터를 받는 사용자 지정 이벤트입니다. 노출 횟수는 광고가 게재된 횟수를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> 클릭 수 </td> 
   <td colname="col3"> DFA 클릭 수 지표 데이터를 받는 사용자 지정 이벤트를 선택합니다. 클릭 수는 DFA의 리디렉션에서 측정한 방문자의 광고 클릭 횟수를 나타냅니다. 클릭 수 지표는 Analytics 클릭스루 지표와 상관 관계가 있습니다. <p>참고: 데이터 수집 방식의 차이로 인해 DFA 클릭 수 및 Analytics 클릭스루가 정확하게 일치하지 않을 수 있습니다. For more information, see <a href="../../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies/dfa-metric-definitions.md#concept-2d5cd5ddd2594bb386a16a2764f30982" format="dita" scope="local"> Metric Definitions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> 뷰스루 변수 </td> 
   <td colname="col3"> <p>DFA 뷰스루 데이터를 받는 Analytics eVar입니다. 뷰스루 변수를 통해 뷰스루가 사이트의 전환율에 어떻게 영향을 주는지 알 수 있습니다. </p> <p>Data Connectors는 DFA 광고 변수에 추가할 때와 같은 동일한 DFA 관련 분류를 이 eVar에 추가합니다(위 참조). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> 마지막으로 본 이후의 시간(뷰스루 시간 버킷 변수) </td> 
   <td colname="col3"> 데이터를 마지막으로 본 이후의 DFA 시간을 받는 Analytics eVar입니다. 마지막으로 본 이후의 시간은 마지막 광고 뷰스루 이후 경과된 시간을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> 뷰스루 </td> 
   <td colname="col3"> DFA 뷰스루 지표 데이터를 받는 사용자 지정 이벤트입니다. 뷰스루 변수와 함께 뷰스루 이벤트를 사용하여 직접 클릭스루에 영향을 주진 않았지만 이후 시간에 사이트에 트래픽을 유도하는 역할을 했을 수 있는 캠페인을 확인할 수 있습니다. <p>Data Connectors는 선택한 사용자 지정 이벤트 이름을 “뷰스루”로 변경합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> DFA 쿼리 오류 </td> 
   <td colname="col3"> (선택 사항) 보고한 DFA 쿼리 오류 메시지 코드를 받는 Analytics eVar입니다. 가능한 DFA 메시지 코드는 다음과 같습니다. 
    <ul id="ul_85FC7FB19F7F4ADF83ABCA6DDB44CE19"> 
     <li id="li_0A3181DED5A149588A0D3F1584E2FE8B"><b>nc</b>: DoubleClick 쿠키가 없습니다. </li> 
     <li id="li_D397AA73AD5E4086A18B87F271E4EC14"><b>oo</b>: 사용자가 선택 해제했습니다. </li> 
     <li id="li_5AC1D0C8049340B4AD857D88E275CBD6"><b>nh</b>: 캠페인 내역이 없습니다. </li> 
     <li id="li_73A8C5E905C54E2BB531A1FCDBC6AA1A"><b>qe</b>: 쿼리 오류(시간 초과, 서버 중지 등)입니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> 시간 초과 이벤트 </td> 
   <td colname="col3"> <p>각 <span class="varname"> s. maxdelay </span> 타이머가 만료되고 DFA 서버에서 응답이 수신되지 않았습니다. Use this event to configure the <span class="varname"> s.maxDelay </span> variable (see <a href="../../dfa-data-connector-analytics/dfa-integration/dfa-tuning-s-maxlelay.md#concept-6deb28eee18e414db220d6009d449f0d" format="dita" scope="local"> Tuning s.maxDelay </a>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

