---
description: 통합을 통해 달성한 마케팅 효율성에 대해 설명합니다.
seo-description: 통합을 통해 달성한 마케팅 효율성에 대해 설명합니다.
seo-title: Adobe Analytics용 Lyris Data Connector
solution: Analytics
title: Adobe Analytics용 Lyris Data Connector
uuid: db213865-1296-4a93-a0a2-781c026b2be5
translation-type: tm+mt
source-git-commit: 34b18e7769e0850283fd3840c2557818d5d742f0

---


# Lyris Data Connector for Adobe Analytics{#lyris-data-connector-for-adobe-analytics}

통합을 통해 달성한 마케팅 효율성에 대해 설명합니다.

Adobe® Data Connectors™ 이메일 통합은 Adobe Analytics의 행동 정보를 Lyris 이메일 마케팅과 결합하여 성공 측정 및 타겟 고객을 보다 연관성 있는 메시지로 재정의합니다.

이러한 시장 세그먼트에 관련 이메일 메시지를 전달하면 완전히 새로운 수익 기회를 창출하여 신규 및 기존 이메일 캠페인 간의 전환율과 매출을 높일 수 있습니다. 예를 들어 방문 중에 본 제품이나 중단된 장바구니에 남겨진 제품을 기반으로 관련 이메일 메시지를 전달하는 것은 매출에 큰 영향을 미치는 것으로 입증되었습니다. 이는 단순히 사이트에서 이미 사용하고 있는 방문자를 활용하는 것이므로 비용에 미치는 영향을 최소화했습니다.

이러한 마케팅 효율성 향상은 Adobe Analytics와 Lyris를 통합함으로써 얻을 수 있는 주요 이점 중 하나입니다. 또한 이 통합은 이메일 지표를 Adobe Analytics 데이터와 자동으로 동기화하여 폐쇄 루프형 보고를 위해 시간별 단위로 표시합니다.

## 주요 이점 및 기능{#key-benefits-and-features}

Lyris와 Adobe 마케팅 보고 및 분석 통합의 주요 이점에 대해 설명합니다.

Lyris와 Adobe Analytics의 통합은 다음과 같은 주요 이점을 제공합니다.

* 이메일 마케팅 및 분석 데이터를 하나의 보고 인터페이스로 통합
* 전환 및 매출 및 사이트 성공에 대한 기여도로 이메일 캠페인 최적화
* 다이내믹한 마케팅 세그먼트를 기반으로 주요 방문자 및 시장 세그먼트로 재마케팅

### 다이내믹 마케팅 세그먼트

이메일 통합은 다이내믹한 마케팅 세그먼트를 지원하여 비즈니스를 추진하는 데 도움이 됩니다. 이 통합은 즉시 다음과 같은 마케팅 세그먼트를 제공합니다.

* **장바구니 포기 프로필**:완전한 장바구니를 원하지 않는 고객을 위해 특별히 고안된 미세 조정 캠페인을 통해 방문자가 고객으로 전환할 수 있도록 지원
* **구매 프로필**:방문자 구매 패턴으로 타깃팅된 캠페인을 통해 반복 주문 및 평균 주문 가격 증가
* **제품/컨텐트 보기 행동 프로필**:제품 보기 및 컨텐츠 액세스 프로파일링을 기반으로 마케팅 세그먼트를 통해 잠재 고객에게 도달
* 또한 고객은 사용자의 요구 사항에 맞는 **맞춤형 재마케팅 세그먼트를** 만들고 예약할 수 있습니다.

## 통합 전제 조건{#integration-prerequisites}

성공적인 통합을 위한 전제 조건을 설명합니다.

이 통합을 활성화하기 전에 Adobe Analytics 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.

따라서 정품 인증 전에 적절한 모범 사례와 사전 이수 과정이 준비되므로 최적의 통합 상태로 유지할 수 있습니다.

### Adobe Analytics 사전 요구 사항 {#section-ddb9d4f3b283438ea33788f47f35e69a}

* **보고서 세트별**:이 통합은 보고서 세트별로 다릅니다. 통합을 활성화하기 전에 원하는 보고서 세트를 선택했는지 확인합니다
* **사용 가능하고 구성된 Analytics 변수**:이 통합에는 사용자 지정 이벤트 및 사용자 지정 eVar, 선택적으로 추가 이벤트 및 추가 eVar가 필요합니다.

* **공인 담당자**:Adobe, Inc.와의 서비스 계약 또는 Adobe의 신뢰할 수 있는 파트너 중 하나와의 서비스 계약에 따라 이 통합을 활성화하면 귀사에서 비용을 발생시킬 수 있습니다. 이 통합을 활성화함으로써 귀하는 회사의 공인 대리인임을 명시합니다.따라서 귀사는 상기에 명시된 서비스 계약에 명시된 요금을 지불해야 합니다.
* **Adobe Analytics 데이터 웨어하우스**:이 통합을 사용하려면 재마케팅 세그먼트를 생성하기 위해 Adobe Analytics 데이터 웨어하우스를 활성화해야 합니다. 데이터 웨어하우스를 활성화하지 않은 경우 Adobe에 자세한 내용을 문의하십시오.
* **수신자 ID**:통합하려면 Analytics 변수(eVar) 내에서 "방문자 ID"를 캡처하고 저장해야 합니다. 방문자 ID(종종 "수신자 ID"라고도 함)는 Lyris 시스템에서 보낸 이메일 주소의 인코딩 또는 숫자 표현입니다. 이 "수신자 ID"는 사이트의 다운스트림 방문자 행동(장바구니 포기, 구매 등)과 연결됩니다. Liris 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. 설정 프로세스의 일부로 마법사에서 메시지가 표시되면 이러한 목적으로 eVar를 식별해야 합니다.
* **외부 추적**:현재 전송하는 각 이메일 캠페인에 대해 외부 추적을 활성화하는 우수 사례를 따르지 않는 경우, 성공적으로 통합되도록 해야 합니다. 자세한 내용은 아래 Lyris 섹션을 참조하십시오.
* **개인 정보 보호 규정 준수**:수신자 또는 방문자 ID 추적을 활성화하면 이 기능이 사이트 방문자의 개인 식별 정보를 추적할 수 있음을 이해해야 합니다. 여기에는 사이트 방문자에 대한 통지, 동의 등 조직에서 적절한 절차를 구현해야 하는 개인정보 보호문제가 있습니다.

### Lyris EmailLabs를 위한 사전 요구 사항 {#section-84abae9401224a3699fed861f715ebde}

* **유효한 Lyris 계정**:이 데이터 커넥터 통합을 사용하려면 유효한 Lyris 계정이 있어야 합니다.
* **계정 정보**:이 통합 설정 중에 Lyris 계정에 대한 다음 정보가 필요합니다.

   * *Lyris API 키*:데이터 모집단 사용
   * *쿼리 문자열 매개 변수*:메시지 ID 및 수신자 ID(방문자 ID)에 대한 랜딩 페이지 URL에 추가됩니다.
   * *Lyris 서버/URL*:Lyris 시스템에서 사용하는 서버 값
   * *Lyris 사이트 ID*:"고객 ID"라고도 하는 이 값은 Lyris HQ 인스턴스에 대한 고유 값입니다. EmailLabs의 "계정 홈" 섹션에 있는 "고객 정보" 아래에 있습니다.

## Lyris에 대한 Adobe Analytics 변수 구성{#configure-adobe-analytics-variables-for-lyris}

각 보고서 세트 구현에 예약되는 eVar 및 이벤트에 대해 설명합니다.

이 통합을 사용하려면 각 보고서 세트 구현에 대해 2개 이상의 eVar를 예약해야 합니다. 이러한 eVar 외에도 Analytics에서 보려는 Lyris 데이터에 따라 일부 이벤트가 예약될 수 있습니다. 이러한 eVar 및 이벤트는 아래 표에 설명되어 있습니다.

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
   <td colname="col3"> 개별 이메일 메시지 캠페인 ID를 캡처하려면 </td> 
   <td colname="col4"> <p>상태:활성화됨 </p> <p>할당:최근 </p> <p>만료 날짜:"비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Email Recipient ID </td> 
   <td colname="col3"> 이메일 캠페인을 클릭한 고객의 익명 ID를 캡처하려면 </td> 
   <td colname="col4"> <p>상태:활성화됨 </p> <p>할당:최근 </p> <p>만료 날짜:"비즈니스 결정" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 보낸 이메일 </td> 
   <td colname="col3"> 아니요. Liris에서 보낸 이메일 </td> 
   <td colname="col4">유형:숫자 <p>기여도:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 열린 이메일 </td> 
   <td colname="col3"> 아니요. 열어본 이메일의 </td> 
   <td colname="col4">유형:숫자 <p>기여도:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 연 고유 이메일 </td> 
   <td colname="col3"> 아니요. 열었던 고유한 이메일 </td> 
   <td colname="col4">유형:숫자 <p>기여도:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 클릭스루 </td> 
   <td colname="col3"> 아니요. 를 클릭합니다. </td> 
   <td colname="col4">유형:숫자 <p>기여도:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 바운스 </td> 
   <td colname="col3"> no를 저장합니다. 바운스된 이메일 </td> 
   <td colname="col4">유형:숫자 <p>기여도:활성화됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lys - 이메일 구독 취소 </td> 
   <td colname="col3"> no를 저장합니다. 비활성화된 이메일 구독 </td> 
   <td colname="col4">유형:숫자 <p>기여도:활성화됨 </p> </td> 
  </tr> 
 </tbody> 
</table>
