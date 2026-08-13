---
description: Adobe Analytics 서버 호출 사용 기능에 대한 개요.
title: 서버 호출 사용량 개요
feature: Server Call Usage
exl-id: d3d64f1e-f01b-4b9e-9aee-c14e574fc40b
role: Admin
TQID: https://experienceleague.adobe.com/-IIz9r-K-flZq85Dz3lhYuo9-Ko0zt0KoJJ7DtI5Mz4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 93678f75cac9b513282a1e4d61276d7617fc933e
workflow-type: tm+mt
source-wordcount: 887
ht-degree: 42%

---

# 서버 호출 사용량

Adobe Analytics 서버 호출 사용량은 브라우저 및 모바일 서버 호출 사용량 데이터 모두에 대한 투명성 요청을 해결합니다. 여기에서 다음에 액세스할 수 있습니다.

* 서버 호출 사용량 데이터를 추적하고 이를 계약 한도와 비교하는 서버 호출 사용량 대시보드. (Adobe Analytics에서 > [!UICONTROL **관리자**] > [!UICONTROL **서버 호출 사용량**]&#x200B;을 선택합니다.)
* 초과 사용을 방지하기 위해 경고를 설정할 수 있는 경고 빌더의 서버 호출 사용량 경고 유형(Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **경고**] 선택)

서버 호출 사용의 주요 이점은 다음과 같습니다.

* 계약 서버 호출 사용량 한도에 따른 모바일 사용을 포함하여 서버 호출 사용량 및 약정 데이터에 대한 **가시성**.
* **경고**&#x200B;를 통해 초과 사용의 위험이나 발생을 알리고 초과 사용이 발생할 가능성에 대비하고 조치를 취합니다.

## 사전 요구 사항 {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **권한:** Adobe Analytics 관리자 액세스 권한 또는 Adobe Admin Console의 [서버 호출 사용량](/help/admin/admin-console/permissions/analytics-tools.md) 권한 항목이 있어야 합니다. 관리자는 제품 프로필을 통해 관리자가 아닌 사용자에게 이 권한 항목을 할당할 수 있습니다.

## 중요한 용어 {#terminology}

다음 용어는 서버 호출 사용을 이해하는 데 중요합니다.

<table id="table_4E97F85F13344A2C962FA4FA5A51642E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 용어 </th> 
   <th colname="col2" class="entry"> 정의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>서버 호출 </p> </td> 
   <td colname="col2"> <p>서버 호출은 데이터를 처리할 수 있도록 Adobe 서버로 보내는 인스턴스로서, "히트" 또는 "이미지 요청"이라고도 합니다. 가장 일반적인 서버 호출 유형은 페이지 보기입니다. 페이지 보기는 방문자가 웹 사이트에서 페이지를 보고 Adobe로 서버 호출이 생성되며 정보를 수집, 처리한 후 보고서 지표에 포함할 때 발생합니다. </p> <p>종료 링크 및 파일 다운로드를 포함한 다른 유형의 서버 호출이 있으며, 이 서버 호출에서는 데이터를 Adobe으로 전송하여 처리하지만 새 페이지 보기로 기록되지는 않습니다. "제외된" 페이지 보기 횟수도 (예: IP 주소 범위를 구성하여 보고서에서 제외) Adobe에서 수신 및 처리하지만 보고서에는 표시되지 않기 때문에 호출로 취급됩니다. </p> <p><b>주 서버 호출</b>: 웹 사이트 방문자 브라우저 또는 데이터 삽입 API에서 직접 받은 요청입니다. 기본 방문 횟수 (페이지 보기 횟수), 기본 사용자 지정 이벤트, 기본 다운로드 이벤트 및 기본 종료 이벤트를 포함합니다. </p> <p><b>보조 서버 호출</b>: 다중 세트 태그로 만들었거나 VISTA 규칙으로 복사/이동한 주 서버 호출의 복사본입니다. 보조 서버 호출이 VISTA 규칙에 의해 다른 보고서 세트로 이동(복사되지 않음)된 경우 누적된 보조 호출은 기본 서버 호출에서 제외됩니다. </p> <p><b>모바일 기본 서버 호출 </b> </p> <p>Mobile SDK 중 하나에서 직접 받은 요청입니다. trackAction, trackState, trackApp Crashes, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease를 포함합니다.</p> <p><b>모바일 보조 서버 호출</b> </p> <p>다중 세트 태그로 만들었거나 VISTA 규칙으로 복사하고 이동한 주 서버 호출의 사본. 보조 서버 호출이 VISTA 규칙에 의해 다른 보고서 세트로 이동(복사되지 않음)된 경우 누적된 보조 호출은 기본 서버 호출에서 제외됩니다. </p> <p>참고: 계약에 따라 귀사에 모바일 서버 호출 (기본 또는 보조)에 대해서만 권한이 부여된 경우 웹과 모바일 특정 사용량은 모두 모바일 특정 약정에 따라 계산됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>청구 회사(청구 ID) </p> </td> 
   <td colname="col2"> <p>서버 호출에 대해 청구되는 법인입니다. 예: adobe.com. 각 청구 회사에는 청구 고객을 고유하게 식별하는 데 사용되는 청구 ID가 있습니다. 과금 ID는 여러 CX 엔터프라이즈 조직에 연결될 수 있으며 조직과 과금 ID 간에 항상 1:1 관계가 있는 것은 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그인 회사 </p> </td> 
   <td colname="col2"> <p>한 청구 회사에 <a href="https://helpx.adobe.com/kr/analytics/kb/multiple-login-companies.html">여러 로그인 회사</a>가 있을 수 있습니다. 로그인 회사는 조직에서 사용한 보고서 세트들의 컬렉션입니다. 일부 조직에는 조직의 여러 부분에 해당되는 여러 로그인 회사가 있습니다. 이 기능은 많은 보고서 세트를 회사의 다른 사용자에게 적용할 수 없는 다양한 비즈니스 단위를 처리하는 대규모 조직에 특히 유용합니다. </p> <p>종종 이들은 기업의 지역 자회사입니다. 다음 예에서는 로그인 회사 및 관련 보고서 세트를 보여 줍니다. </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.worldwide: RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us: RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in: RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de: RS4 </li> 
    </ul> <p>참고: 청구 회사 내의 <u>모든</u> 보고서 세트에 대한 서버 호출 사용량 데이터는 해당 <a href="/help/admin/admin-console/permissions/analytics-tools.md">권한</a>이 있는 모든 사용자가 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CX 엔터프라이즈 조직 </p> </td> 
   <td colname="col2"> <p>조직은 관리자가 그룹과 사용자를 구성하고, CX Enterprise에서 SSO(Single Sign-On)를 제어할 수 있도록 하는 항목입니다. 조직은 모든 CX 엔터프라이즈 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. </p> <p>대부분의 경우 조직은 회사 이름입니다. 그렇지만 한 회사에 여러 조직이 있을 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 호출 약정 </p> </td> 
   <td colname="col2"> <p>귀사가 Adobe와의 계약에 서명하면 Adobe Sales 팀은 귀사, 고객, 계약 기간 과정에 발생할 것으로 예상되는 서버 호출 유형 (기본, 보조, 모바일 기본, 모바일 보조) 및 수와 동일시합니다. 총 서버 호출 약정입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용 기간 </p> </td> 
   <td colname="col2"> <p>이 총 서버 호출 약정은 서버 호출 사용량을 모니터링하기 위해 더 작은 사용 기간(예: 3개월)으로 구분되므로 매년 비교하기가 쉽습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계약 기간 </p> </td> 
   <td colname="col2"> <p>계약 기간은 여러 해를 넘길 수 있습니다. 예를 들어 귀사에서 3년 계약 기간 동안 600만 번의 호출을 약속하는 서버 호출을 보유하고 있다고 가정해 보겠습니다. 서버 호출 사용량을 모니터링하기 위해 이 3년을 더 작은 사용 기간으로 구분하면 연차별로 쉽게 비교할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
