---
description: 'null'
title: Adobe Analytics용 Selligent Data Connector
uuid: e16c3ca6-b131-44b1-a36c-e39697677a96
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Adobe Analytics용 Selligent Data Connector{#selligent-data-connector-for-adobe-analytics}

이 통합에는 다음과 같은 주요 이점이 포함됩니다.

* 이메일 마케팅 및 분석 데이터를 하나의 보고 인터페이스로 통합합니다.
* 매출 및 사이트 성공에 대한 전환과 기여로 이메일 캠페인을 최적화합니다.
* 동적 마케팅 세그먼트를 기반으로 주요 방문자 및 시장 세그먼트를 리마케팅합니다.

## 동적 마케팅 세그먼트{#section-a2216f3339304636bd5417249bd635a4}

이메일 통합은 동적 마케팅 세그먼트를 지원하여 비즈니스의 동력을 제공합니다. 이 통합은 다음과 같은 마케팅 세그먼트를 즉시 제공합니다.

| 세그먼트 | 설명 |
|---|---|
| **장바구니 포기 프로필** | 장바구니에서 주문 완료를 망설이는 고객을 위해 특별히 고안된 정밀한 캠페인을 통해 방문자가 고객으로 전환될 수 있도록 지원합니다. |
| **구매 프로필** | 방문자 구매 패턴별로 타깃팅한 캠페인을 통해 반복 주문 및 평균 주문 가격이 증가합니다. |
| **제품/컨텐츠 보기 행동 프로필** | 제품 보기 및 컨텐츠 액세스 프로파일링을 기반으로 마케팅 세그먼트를 통해 잠재 고객에게 도달할 수 있습니다. |
| **사용자 지정 리마케팅 세그먼트** | 또한 고객은 사용자의 요구 사항에 맞게 사용자 지정 리마케팅 세그먼트를 만들고 예약할 수 있습니다. |

## 이 통합을 활성화하기 전에{#before-you-activate-this-integration}

이 통합을 활성화하기 전에 Adobe Analytics 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.

이렇게 하면 활성화 전에 적절한 우수 사례와 전제 조건을 갖출 수 있습니다. 이를 통해 최적의 통합이 성공적으로 이루어집니다.

## Adobe Analytics 사전 요구 사항 {#prerequisites-for-adobe-analytics}

통합을 배포하기 전에 Adobe Analytics에서 수행해야 할 필수 작업을 나열합니다.

| 전제 조건 | 참고 |
|---|---|
| 보고서 세트 선택 | 이 통합은 보고서 세트별로 다르므로 주의하십시오. 통합을 활성화하기 전에 원하는 보고서 세트를 선택했는지 확인합니다. |
| Analytics 변수 구성 | 이 통합에는 사용자 지정 이벤트 및 사용자 지정 eVar, 선택적인 추가 이벤트 및 추가 eVar가 필요합니다. Selligent용 Analytics 변수 구성을 참조하십시오. |
| 공식 대리인 | 이 통합을 활성화하면 Adobe, Inc.와의 서비스 계약 또는 Adobe의 신뢰할 수 있는 파트너 중 하나와의 서비스 계약에 따라 귀사에 비용이 발생할 수 있습니다. 이러한 통합을 활성화함으로써 귀하는 귀사의 권한을 부여받은 대표자임을 명시하며, 이에 따라 귀사는 상기에 제시된 서비스 계약에 명시된 요금을 지불해야 합니다. |
| Adobe Data Warehouse™ 활성화 | 이 통합을 사용하려면 리마케팅 세그먼트를 생성하기 위해 Data Warehouse를 활성화해야 합니다. Adobe Data Warehouse를 활성화하지 않은 경우 Adobe에 자세한 내용을 문의하십시오. |
| 수신자 ID | 통합하려면 Analytics 변수(eVar) 내에서 &quot;방문자 ID&quot;를 캡처하고 저장해야 합니다. 방문자 ID(종종 &quot;수신자 ID&quot;라고도 함)는 Selligent 시스템의 이메일 주소를 인코딩하거나 숫자로 표현한 것입니다. 이 &quot;수신자 ID&quot;는 사이트의 다운스트림 방문자 행동(장바구니 포기, 구매 등)과 관련되어 있어 Selligent 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. 설정 프로세스의 일부로 마법사에서 메시지가 표시되면 이 용도를 위해 eVar를 식별해야 합니다. |
| 외부 추적 | 현재 전송하는 각 이메일 캠페인에 대해 외부 추적을 활성화하는 우수 사례를 따르고 있지 않다면, 성공적인 통합을 위해 우수 사례를 따라야 합니다. 자세한 내용은 아래 Selligent 섹션을 참조하십시오. |
| 개인정보 규정 준수 | 수신자 또는 방문자 ID 추적을 활성화하면 이 기능이 사이트 방문자의 개인 식별 정보를 추적할 수 있음을 이해해야 합니다. 따라서 조직에서는 사이트 방문자에게 통지하고 동의를 구하는 등과 같이 개인정보 보호를 위한 적절한 절차를 구현해야 합니다. |

## Selligent용 Analytics 변수 구성{#configure-analytics-variables-for-selligent}

이 통합을 위해서는 각 보고서 세트 구현에 대해 2개의 eVar를 예약해야 합니다.

이러한 eVar 외에도 Analytics에서 보려는 Selligent 데이터에 따라 일부 이벤트가 예약될 수 있습니다. 이러한 eVar 및 이벤트는 다음과 같이 설명되어 있습니다.

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
   <td colname="col3"> 개별 이메일 메시지 캠페인 ID를 캡처 </td> 
   <td colname="col4"> <p><b>상태</b>: 활성화됨 </p> <p><b>할당</b>: 가장 최근 </p> <p><b>다음 시기 이후에 만료</b>: "비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eV ar </td> 
   <td colname="col2"> 수신자 ID </td> 
   <td colname="col3"> 이메일 캠페인을 클릭한 고객의 익명 ID 캡처 </td> 
   <td colname="col4"> <p><b>상태</b>: 활성화됨 </p> <p><b>할당</b>: 가장 최근 </p> <p><b>다음 시기 이후에 만료</b>: "비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 보냄 </td> 
   <td colname="col3"> Selligent에서 보낸 이메일 수를 저장 </td> 
   <td colname="col4"> <p><b>유형</b>: 숫자 </p> <p><b>기여도</b>: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 배달됨 </td> 
   <td colname="col3"> 배달된 이메일 수를 저장 </td> 
   <td colname="col4"> <p><b>유형</b>: 숫자 </p> <p><b>기여도</b>: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 보기 횟수 </td> 
   <td colname="col3"> 조회된 고유 이메일 수를 저장 </td> 
   <td colname="col4"> <p><b>유형</b>: 숫자 </p> <p><b>기여도</b>: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 클릭 수 </td> 
   <td colname="col3"> 이메일을 클릭한 횟수를 저장 </td> 
   <td colname="col4"> <p><b>유형</b>: 숫자 </p> <p><b>기여도</b>: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 바운스됨 </td> 
   <td colname="col3"> 바운스된 이메일 수를 저장 </td> 
   <td colname="col4"> <p><b>유형</b>: 숫자 </p> <p><b>기여도</b>: 활성화됨 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Selligent 사전 요구 사항{#prerequisites-for-selligent}

통합을 배포하기 전에 Selligent 계정에서 제공하는 데 필요한 정보를 나열합니다.

**유효한 Selligent 계정**

이 Data Connectors 통합을 사용하려면 유효한 Selligent 계정이 있어야 합니다.

**계정 정보**

이 통합 설정 중에 Selligent 계정에 대한 다음 정보가 필요합니다.

* **Adobe 서비스 URL**:

   URL은 Selligent Marketing 솔루션에 로그온하는 데 사용되는 URL에서 파생될 수 있습니다. url의 &quot;/simweb/login.aspx&quot; 부분을 &quot;/automation/omniture.asmx&quot;로 바꿉니다.

   예: `http://<client-specific install url>/automation/omniture.asmx`

* **쿼리 문자열 매개 변수**: 메시지 ID 및 수신자 ID(방문자 ID)용 랜딩 페이지 URL에 추가됩니다. 메시지 ID와 수신자 ID에 대해 각각 항상 MID 및 RID입니다.

* **통합 토큰** Simweb 내에서 Manager 도구를 실행하고 **[!UICONTROL 구성]** > **[!UICONTROL 시스템 설정]** > **[!UICONTROL 일반]** 탭 > **[!UICONTROL 시스템]**&#x200B;으로 이동합니다. **[!UICONTROL 보안]** 아래에서 통합 토큰을 찾을 수 있습니다.

   ![](assets/selligent-integration_token.png)
