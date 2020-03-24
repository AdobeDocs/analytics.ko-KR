---
description: 통합을 통해 달성한 마케팅 효율성에 대해 설명합니다.
title: Adobe Analytics용 Lyris Data Connector
uuid: db213865-1296-4a93-a0a2-781c026b2be5
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Adobe Analytics용 Lyris Data Connector{#lyris-data-connector-for-adobe-analytics}

통합을 통해 달성한 마케팅 효율성에 대해 설명합니다.

Adobe® Data Connectors™ 이메일 통합은 Adobe Analytics의 행동 정보를 Lyris 이메일 마케팅과 결합하여 성공 측정 및 타겟 대상을 더 연관성 있는 메시징으로 재정의합니다.

이러한 시장 세그먼트에 관련 있는 이메일 메시지를 전달하면 완전히 새로운 수익 기회를 창출하여 신규 및 기존 이메일 캠페인에서 전환과 매출을 높일 수 있습니다. 예를 들어 방문 중에 본 제품이나 구매하지 않고 장바구니에 남겨진 제품을 기반으로 관련 있는 이메일 메시지를 전달하면 사용자의 사이트에서 이미 확보하고 있는 방문자를 활용하기 때문에 비용에 미치는 영향을 최소화하면서 매출에 큰 영향을 미치는 것으로 입증되었습니다.

이러한 마케팅 효율성 향상은 Adobe Analytics와 Lyris를 통합함으로써 얻을 수 있는 주요 이점 중 하나입니다. 또한 이 통합은 폐쇄 루프 보고를 위해 이메일 지표를 매시간 Adobe Analytics 데이터와 자동으로 동기화합니다.

## 주요 이점 및 기능{#key-benefits-and-features}

Lyris와 Adobe Marketing Reports and Analytics 통합의 주요 이점에 대해 설명합니다.

Lyris와 Adobe Analytics의 통합은 다음과 같은 주요 이점을 제공합니다.

* 이메일 마케팅 및 분석 데이터를 하나의 보고 인터페이스로 통합
* 매출 및 사이트 성공에 대한 전환과 기여로 이메일 캠페인 최적화
* 동적 마케팅 세그먼트를 기반으로 주요 방문자 및 시장 세그먼트를 리마케팅

### 동적 마케팅 세그먼트

이메일 통합은 동적 마케팅 세그먼트를 지원하여 비즈니스의 동력을 제공하는 데 도움이 됩니다. 이 통합은 다음과 같은 마케팅 세그먼트를 즉시 제공합니다.

* **장바구니 포기 프로필**: 장바구니에서 주문 완료를 망설이는 고객을 위해 특별히 고안된 정밀한 캠페인을 통해 방문자가 고객으로 전환될 수 있도록 지원
* **구매 프로필**: 방문자 구매 패턴별로 타겟팅한 캠페인을 통해 반복 주문 및 평균 주문 가격 증가
* **제품/컨텐츠 보기 행동 프로필**: 제품 보기 및 컨텐츠 액세스 프로파일링을 기반으로 하는 마케팅 세그먼트를 통해 잠재 고객에게 도달
* 또한 고객은 사용자의 요구 사항에 맞게 **사용자 지정 리마케팅 세그먼트**&#x200B;를 만들고 예약할 수 있습니다.

## 통합 사전 요구 사항{#integration-prerequisites}

성공적인 통합을 위한 사전 요구 사항을 설명합니다.

이 통합을 활성화하기 전에 Adobe Analytics 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.

이렇게 하면 활성화 전에 적절한 우수 사례와 사전 요구 사항이 준비되므로 최적화되고 성공적인 통합이 이루어지도록 할 수 있습니다.

### Adobe Analytics 사전 요구 사항 {#section-ddb9d4f3b283438ea33788f47f35e69a}

* **보고서 세트별**: 이 통합은 보고서 세트별로 다르므로 주의하십시오. 통합을 활성화하기 전에 원하는 보고서 세트를 선택했는지 확인합니다.
* **사용 가능하고 구성된 Analytics 변수**: 이 통합에는 사용자 지정 이벤트 및 사용자 지정 eVar, 선택적 추가 이벤트 및 추가 eVar가 필요합니다.

* **승인된 담당자**: 이 통합을 활성화하면 Adobe, Inc.와의 서비스 계약 또는 Adobe의 신뢰할 수 있는 파트너 중 하나와의 서비스 계약에 따라 귀사에 비용이 발생할 수 있습니다. 이러한 통합을 활성화함으로써 귀하는 귀사의 권한을 부여받은 대표자임을 명시하며, 이에 따라 귀사는 상기에 제시된 서비스 계약에 명시된 요금을 지불해야 합니다.
* **Adobe Analytics Data Warehouse**: 이 통합에서 리마케팅 세그먼트를 생성하려면 Adobe Analytics Data Warehouse를 활성화해야 합니다. Data Warehouse를 활성화하지 않은 경우 Adobe에 자세한 내용을 문의하십시오.
* **수신자 ID**: 통합하려면 Analytics 변수(eVar) 내에서 &quot;방문자 ID&quot;를 캡처하고 저장해야 합니다. 방문자 ID(종종 &quot;수신자 ID&quot;라고도 함)는 Lyris 시스템의 이메일 주소를 인코딩하거나 숫자로 표현한 것입니다. 이 &quot;수신자 ID&quot;는 사이트의 다운스트림 방문자 행동(장바구니 포기, 구매 등)과 관련되어 있어 Lyris 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. 설정 프로세스의 일부로 마법사에서 메시지가 표시되면 이 용도를 위해 eVar를 식별해야 합니다.
* **외부 추적**: 사용자가 현재 전송하는 각 이메일 캠페인에 대해 외부 추적을 활성화하는 우수 사례를 따르고 있지 않다면, 성공적인 통합을 위해 우수 사례를 따라야 합니다. 자세한 내용은 아래 Lyris 섹션을 참조하십시오.
* **개인정보 규정 준수**: 수신자 또는 방문자 ID 추적을 활성화하면 이 기능이 사이트 방문자의 개인 식별 정보를 추적할 수 있음을 이해해야 합니다. 따라서 조직에서는 사이트 방문자에게 통지하고 동의를 구하는 등과 같이 개인정보 보호를 위한 적절한 절차를 구현해야 합니다.

### Lyris EmailLabs 사전 요구 사항 {#section-84abae9401224a3699fed861f715ebde}

* **유효한 Lyris 계정**: 이 Data Connectors 통합을 사용하려면 유효한 Lyris 계정이 있어야 합니다.
* **계정 정보**: 이 통합 설정 중에 Lyris 계정에 대한 다음 정보가 필요합니다.

   * *Lyris API 키*: 데이터 채우기에 사용됨
   * *쿼리 문자열 매개 변수*: 메시지 ID 및 수신자 ID(방문자 ID)용 랜딩 페이지 URL에 추가됩니다.
   * *Lyris 서버/URL*: Lyris 시스템에서 사용하는 서버 값
   * *Lyris 사이트 ID*: &quot;고객 ID&quot;라고도 하는 이 값은 Lyris HQ 인스턴스에 대한 고유 값입니다. EmailLabs의 &quot;계정 홈&quot; 섹션에 있는 &quot;고객 정보&quot; 아래에 있습니다.

## Lyris에 대한 Adobe Analytics 변수 구성{#configure-adobe-analytics-variables-for-lyris}

각 보고서 세트 구현에 예약되는 eVar 및 이벤트에 대해 설명합니다.

이 통합을 위해서는 각 보고서 세트 구현에 대해 2개 이상의 eVar를 예약해야 합니다. 이러한 eVar 외에도 Analytics에서 보려는 Lyris 데이터에 따라 일부 이벤트가 예약될 수 있습니다. 이러한 eVar 및 이벤트는 아래 표에 설명되어 있습니다.

<table id="table_43E32344E9E54FED8491F28047249329"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 유형 </th> 
   <th colname="col2" class="entry"> 변수 이름 </th> 
   <th colname="col3" class="entry"> 변수 사용 방법 </th> 
   <th colname="col4" class="entry"> 설정 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> 개별 이메일 메시지 캠페인 ID를 캡처 </td> 
   <td colname="col4"> <p>상태: 활성화됨 </p> <p>할당: 가장 최근 </p> <p>다음 시기 이후에 만료: "비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> 이메일 수신자 ID </td> 
   <td colname="col3"> 이메일 캠페인을 클릭한 고객의 익명 ID 캡처 </td> 
   <td colname="col4"> <p>상태: 활성화됨 </p> <p>할당: 가장 최근 </p> <p>다음 시기 이후에 만료: "비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 보낸 이메일 </td> 
   <td colname="col3"> Lyris에서 보낸 이메일 개수 저장 </td> 
   <td colname="col4">유형: 숫자 <p>기여도: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 연 이메일 </td> 
   <td colname="col3"> 열어본 이메일 개수 저장 </td> 
   <td colname="col4">유형: 숫자 <p>기여도: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 열린 고유 이메일 </td> 
   <td colname="col3"> 열린 고유 이메일 개수 저장 </td> 
   <td colname="col4">유형: 숫자 <p>기여도: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 클릭스루 </td> 
   <td colname="col3"> 이메일을 클릭한 횟수 저장 </td> 
   <td colname="col4">유형: 숫자 <p>기여도: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 바운스 </td> 
   <td colname="col3"> 바운스된 이메일 개수 저장 </td> 
   <td colname="col4">유형: 숫자 <p>기여도: 활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 구독 취소 </td> 
   <td colname="col3"> 비활성화된 이메일 구독 개수 저장 </td> 
   <td colname="col4">유형: 숫자 <p>기여도: 활성화됨 </p> </td> 
  </tr> 
 </tbody> 
</table>
