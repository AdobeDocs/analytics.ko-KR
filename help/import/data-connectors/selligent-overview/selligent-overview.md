---
description: 'null'
seo-description: 'null'
seo-title: Adobe Analytics용 지능형 데이터 커넥터
solution: Analytics
title: Adobe Analytics용 지능형 데이터 커넥터
uuid: e16c3ca6-b131-44b1-a36c-e39697677a96
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Selligent Data Connector for Adobe Analytics{#selligent-data-connector-for-adobe-analytics}

이 통합에는 다음과 같은 주요 이점이 포함됩니다.

* 이메일 마케팅 및 분석 데이터를 하나의 보고 인터페이스로 통합할 수 있습니다.
* 전환율과 매출 및 사이트 성공률 기여도로 이메일 캠페인을 최적화할 수 있습니다.
* 다이내믹한 마케팅 세그먼트를 기반으로 주요 방문자 및 시장 세그먼트로 다시 마케팅합니다.

## 다이내믹 마케팅 세그먼트 {#section-a2216f3339304636bd5417249bd635a4}

이 이메일 통합은 다이내믹한 마케팅 세그먼트를 지원하여 비즈니스를 추진하는 데 도움이 됩니다. 이 통합은 즉시 다음과 같은 마케팅 세그먼트를 제공합니다.

| 세그먼트 | 설명 |
|---|---|
| **장바구니 포기 프로필** | 완전한 장바구니를 원하지 않는 고객을 위해 특별히 고안된 정교한 캠페인을 통해 방문자가 고객으로 전환할 수 있도록 지원합니다. |
| **구매 프로필** | 방문자 구매 패턴으로 타깃팅된 캠페인을 통해 반복 주문 및 평균 주문 가격을 높일 수 있습니다. |
| **제품/컨텐츠 보기 행동 프로필** | 제품 보기 및 컨텐츠 액세스 프로파일링을 기반으로 마케팅 세그먼트를 통해 잠재 고객에게 도달할 수 있습니다. |
| **사용자 지정 재마케팅 세그먼트** | 또한 고객은 사용자의 요구 사항에 맞는 맞춤형 재마케팅 세그먼트를 만들고 예약할 수 있습니다. |

## 이 통합을 활성화하기 전에{#before-you-activate-this-integration}

이 통합을 활성화하기 전에 Adobe Analytics 및 이메일 소프트웨어의 배포에 대해 다음 항목을 검토하십시오.

이렇게 하면 정품 인증 전에 적절한 모범 사례와 전제 조건을 갖출 수 있습니다. 이렇게 하면 최적의 통합이 성공적으로 이루어집니다.

## Adobe Analytics 사전 요구 사항{#prerequisites-for-adobe-analytics}

통합을 배포하기 전에 Adobe Analytics에서 수행해야 할 필요한 작업을 나열합니다.

| 전제 조건 | 참고 |
|---|---|
| 보고서 세트 선택 | 이 통합은 보고서 세트별로 다릅니다. 통합을 활성화하기 전에 원하는 보고서 세트를 선택했는지 확인합니다. |
| Analytics 변수 구성 | 이 통합에는 사용자 지정 이벤트 및 사용자 지정 eVar, 선택적으로 추가 이벤트 및 추가 eVar가 필요합니다. 지능적인 분석을 위한 분석 변수 구성을 참조하십시오. |
| 공인 대리인 | Adobe, Inc.와의 서비스 계약 또는 Adobe의 신뢰할 수 있는 파트너 중 하나와의 서비스 계약에 따라 이 통합을 활성화하면 귀사에서 비용을 발생시킬 수 있습니다. 이 통합을 활성화함으로써 귀하는 회사의 공인 대리인임을 명시합니다.따라서 귀사는 상기에 명시된 서비스 계약에 명시된 요금을 지불해야 합니다. |
| Adobe Data Warehouse™ 활성화 | 이 통합을 사용하려면 리마케팅 세그먼트를 생성하기 위해 데이터 웨어하우스를 활성화해야 합니다. Adobe 데이터 웨어하우스를 활성화하지 않은 경우 Adobe에 자세한 내용을 문의하십시오. |
| Recipient ID | 통합하려면 Analytics 변수(eVar) 내에서 "방문자 ID"를 캡처하고 저장해야 합니다. 방문자 ID("수신자 ID"라고도 함)는 지능형 시스템에서 이메일 주소를 인코딩하거나 숫자로 나타낸 것입니다. 이 "수신자 ID"는 사이트의 다운스트림 방문자 행동(장바구니 포기, 구매 등)과 연결됩니다. 즉, Sellligent 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. 설정 프로세스의 일부로 마법사에서 메시지가 표시되면 이러한 목적으로 eVar를 식별해야 합니다. |
| 외부 추적 | 현재 전송하는 각 이메일 캠페인에 대해 외부 추적을 활성화하는 우수 사례를 따르지 않는 경우, 성공적으로 통합되도록 해야 합니다. 자세한 내용은 아래 Selective 섹션을 참조하십시오. |
| 개인 정보 보호 규정 준수 | 수신자 또는 방문자 ID 추적을 활성화하면 이 기능이 사이트 방문자의 개인 식별 정보를 추적할 수 있음을 이해해야 합니다. 여기에는 사이트 방문자에 대한 통지, 동의 등 조직에서 적절한 절차를 구현해야 하는 개인 정보가 포함됩니다. |

## 지능적인 분석 변수 구성{#configure-analytics-variables-for-selligent}

이 통합을 사용하려면 각 보고서 세트 구현에 대해 2개의 eVar를 예약해야 합니다.

이러한 eVar 외에도 Analytics에서 보려는 Sellligent의 데이터에 따라 일부 이벤트가 예약될 수 있습니다. 이러한 eVar 및 이벤트는 다음과 같이 설명되어 있습니다.

<table id="table_2FFB865DBD80412F90DA8E224B12FB62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 유형 </th> 
   <th colname="col2" class="entry"> 변수 이름 </th> 
   <th colname="col3" class="entry"> 사용 방법 </th> 
   <th colname="col4" class="entry"> 설정 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> 개별 이메일 메시지 캠페인 ID를 캡처하려면 </td> 
   <td colname="col4"> <p><b>상태</b>:활성화됨 </p> <p><b>할당</b>:최근 </p> <p><b>만료 날짜</b>:"비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eV ar </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> 이메일 캠페인을 클릭한 고객의 익명 ID를 캡처하려면 </td> 
   <td colname="col4"> <p><b>상태</b>:활성화됨 </p> <p><b>할당</b>:최근 </p> <p><b>만료 날짜</b>:"비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 전송 </td> 
   <td colname="col3"> Selligent에서 보낸 이메일 수를 저장합니다. </td> 
   <td colname="col4"> <p><b>유형</b>:숫자 </p> <p><b>기여도</b>:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 배달됨 </td> 
   <td colname="col3"> 배달된 이메일 수를 저장합니다. </td> 
   <td colname="col4"> <p><b>유형</b>:숫자 </p> <p><b>기여도</b>:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 보기 횟수 </td> 
   <td colname="col3"> 본 고유 이메일 수를 저장합니다. </td> 
   <td colname="col4"> <p><b>유형</b>:숫자 </p> <p><b>기여도</b>:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 클릭 수 </td> 
   <td colname="col3"> 이메일을 클릭한 횟수를 저장하려면 </td> 
   <td colname="col4"> <p><b>유형</b>:숫자 </p> <p><b>기여도</b>:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 바운스됨 </td> 
   <td colname="col3"> 바운스된 이메일 수를 저장합니다. </td> 
   <td colname="col4"> <p><b>유형</b>:숫자 </p> <p><b>기여도</b>:활성화됨 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 지능적인 사전 요구 사항{#prerequisites-for-selligent}

통합을 배포하기 전에 Sellligent 계정에서 제공하는 데 필요한 정보를 나열합니다.

**유효한 고급 계정**

이 데이터 커넥터 통합을 사용하려면 유효한 지능적인 계정이 있어야 합니다.

**계정 정보**

이 통합 설정 중에 지능형 계정에 대한 다음 정보가 필요합니다.

* **Adobe 서비스 URL**:

   URL은 Sellligent Marketing 솔루션에 로그온하는 데 사용되는 URL에서 파생될 수 있습니다. url의 "/simweb/login.aspx" 부분을 "/automation/omniture.asmx"로 바꿉니다.

   E.g: `http://<client-specific install url>/automation/omniture.asmx`

* **** 쿼리 문자열 매개 변수:메시지 ID 및 수신자 ID(방문자 ID)에 대한 랜딩 페이지 URL에 추가됩니다. 메시지 ID와 수신자 ID의 경우 항상 MID 및 RID입니다.

* **통합 토큰** Simweb 내에서 Manager 도구를 실행하고 구성 **[!UICONTROL &gt; 시스템 설정]** **[!UICONTROL &gt; 일반]** 탭 &gt; **[!UICONTROL 시스템]** 설정으로 이동합니다 ****. 보안 **[!UICONTROL 아래에서]**&#x200B;통합 토큰을 찾을 수 있습니다.

   ![](assets/selligent-integration_token.png)
