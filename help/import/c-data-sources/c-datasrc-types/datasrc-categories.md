---
description: 데이터 소스 카테고리는 유사한 기능을 제공하는 다양한 데이터 소스 유형을 식별합니다.
seo-description: 데이터 소스 카테고리는 유사한 기능을 제공하는 다양한 데이터 소스 유형을 식별합니다.
seo-title: 데이터 유형 및 카테고리 개요
solution: Analytics
subtopic: Data Sources
title: 데이터 유형 및 카테고리 개요
topic: 개발자 및 구현
uuid: b 5004 cdc-b 68 a -4 a 82-a 159-a 7 cd 7 b 8 bfe 21
translation-type: tm+mt
source-git-commit: e3b1ac3139f26ca3a97f3d2228276e690ec4cb79

---


# 데이터 유형 및 카테고리 개요

데이터 소스 카테고리는 유사한 기능을 제공하는 다양한 데이터 소스 유형을 식별합니다.

카테고리를 사용하면 사용자의 관점에서 데이터 소스를 그룹화할 수 있습니다. 데이터 소스 UI를 통해 데이터 소스를 생성하는 경우 먼저 데이터 소스 카테고리를 선택한 후 특정 데이터 소스 유형을 선택합니다. 각 카테고리는 유사한 데이터 유형을 지원하는 데이터 소스 유형을 포함합니다. 데이터 소스에는 다음과 같은 데이터 소스 카테고리가 있습니다.

## 웹 사이트 사용 패턴 {#section_4BA8D97B6BA848518F21760AE49F41D1}

<table id="table_2562E7A400214B8F9BB9177D210348F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>웹 서버 로그 파일 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-web-log.md#concept_E25D89C8B90A41FEB7DF4E936CACEE2B" type="concept" format="dita" scope="local"> 웹 로그 </a> </p> </td> 
   <td colname="col3"> <p>대부분의 웹 서버는 모든 서비스 제공 페이지를 기록하는 로그 파일을 생성합니다. 이 데이터 소스를 사용하면 대부분의 웹 서버 데이터의 로그 파일을 처리하고 이 데이터를 보고서에 추가할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Advertising Cloud 벌크 업로드 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>Advertising Cloud에서 수동 및 Excel 자동 벌크 업로드를 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사이트 수준 트래픽 데이터 소스 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC" type="concept" format="dita" scope="local"> 트래픽 </a> </p> </td> 
   <td colname="col3"> <p>전체 웹 사이트에 대한 트래픽 데이터를 가져옵니다. 예를 들어 페이지 뷰 수를 가져옵니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>트래픽 데이터 소스 분류 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC" type="concept" format="dita" scope="local"> 트래픽 </a> </p> </td> 
   <td colname="col3"> <p>다른 웹 사이트 변수로 분류된 트래픽 데이터를 가져옵니다. 예를 들어 제품별 페이지 뷰 수를 가져옵니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 광고 캠페인 {#section_9AE27E347CFC48F29E7C1134B6E928A6}

<table id="table_2A297A86CC3E4B1E8B72389AA148549A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>범용 광고 서버 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>광고 서버의 광고 서비스 활동에 대한 노출 횟수 및 기타 최상위 지표를 마케팅 보고서에 통합할 수 있습니다. 이는 범용 광고 서버 데이터 소스이며 특정 광고 서버가 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>범용 이메일 캠페인 서버 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>이메일 캠페인 서버의 지표를 마케팅 보고서에 통합할 수 있습니다. </p> <p>일반적으로 통합되는 지표로는 전송한 메시지 수, 배달된 메시지 수 및 읽은 메시지 수 등이 있습니다. 이는 범용 이메일 캠페인 데이터 소스이며 특정 이메일 캠페인 서버가 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>범용 클릭당 지불 서비스 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p> 노출 수, 클릭 수, 비용을 포함한 클릭당 지불 실적 데이터를 가져올 수 있습니다. </p> <p>이는 범용 클릭당 지불 데이터 소스이며 특정 클릭당 지불 서비스가 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 고객 관계 관리(CRM) {#section_013A1C5D3CAD4CCEAD22C2FDD26715A0}

<table id="table_5895659CAB2C415AB2AA59A2E6C75AD1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>범용 콜 센터 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>콜 센터 관련 정보를 마케팅 보고서에 통합할 수 있습니다. 일반적으로 가져오는 지표로는 통화 수, 통화 시간, 상담원, 총 매출액 등이 있습니다. </p> <p>이는 범용 콜 센터 데이터 소스이며 특정 콜 센터 소프트웨어가 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> <p>범용 고객 지원 </p> <p>응용 프로그램 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>고객 지원 소프트웨어의 정보를 마케팅 보고서에 통합할 수 있습니다. 여기에는 새 지원 건 수, 해결된 지원 건 수 및 지원에 소비된 시간 등의 지표가 포함됩니다. </p> <p>이는 범용 고객 지원 데이터 소스이며 특정 고객 서비스 응용 프로그램이 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 고객 만족 {#section_1058CA3860044630B0B06EEDA261DBA2}

<table id="table_3811CA1E2B7C45D7A0CBEC5CE44C11A8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>범용 조사 데이터 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>타사 도구를 통해 얻은 조사 결과를 마케팅 보고서에 통합하고, 이를 통해 고객이 사이트와의 상호 작용에서 느끼는 만족도를 파악할 수 있습니다. </p> <p>이는 범용 조사 데이터 소스이며 특정 조사 데이터 서비스가 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사이트 실적 {#section_3A7BECB0B4B247FB991DC59237ECFE1F}

<table id="table_7B623D08275E4FDEADDD85EA89A2B7C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>범용 사이트 다운로드 속도 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>다운로드 속도를 추적하는 응용 프로그램이나 서비스에서 얻은 데이터를 데이터에 통합할 수 있습니다. </p> <p>이는 범용 다운로드 속도 데이터 소스이며 특정 다운로드 속도 소프트웨어 또는 서비스가 지원되지 않는 경우에 사용해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 범용 {#section_9B9A2A9871894B6491032AE1E961629A}

<table id="table_D63A6A00C93A4CD48FEBE7BC24E5DA9F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> <p>범용 데이터 소스(요약 데이터만) </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>마케팅 보고 및 분석에 가져오려는 데이터 유형과 유사한 내용이 검색되지 않을 때 이 데이터 소스를 사용하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>범용 데이터 소스(전체 처리) </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#concept_975B1BB9981D49139B4EE09C78CDE6ED" type="concept" format="dita" scope="local"> 전체 처리 </a> </p> </td> 
   <td colname="col3"> <p>로그 파일 데이터를 가져올 수 있습니다. 이 데이터는 지정된 시간에 데이터 수집 서버에서 수신한 것처럼 처리됩니다(각 히트에서 타임스탬프 수신). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> <p>범용 데이터 소스(거래 ID) </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-transactionid.md#concept_A97302E9EC45468A8F30285FACE8C776" type="concept" format="dita" scope="local"> 거래 ID </a> </p> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-visitorid.md#concept_1CFAA61D57A84B22A41F7A8E0DFCAAB5" type="concept" format="dita" scope="local"> Visitor ID </a> </p> </td> 
   <td colname="col3"> <p>오프라인 이벤트를 온라인 이벤트에 연결할 수 있습니다. 거래 ID는 오프라인 이벤트와 온라인 이벤트 간의 키 역할을 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 온라인 구매 {#section_2B2D4DBB045548C3A5DC7DEF81BA56D1}

<table id="table_EE450D955D4C4264A40142AF6D74F1AA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>제품 반환 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>제품 반환 데이터를 가져와서 구매 ID와 연결하여 검색 엔진, 키워드, 캠페인, 그 외 반환을 일으킬 가능성이 높은 특성을 파악할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 비용 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>비용이나 수익을 개별 제품과 연결함으로써 웹 사이트에서 구매되어 배송된 제품의 실제 비용을 제공하여 웹 사이트에 대한 가장 수익성 있는 캠페인, 키워드 및 내부 프로모션을 정확히 보고할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주문 상태 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>지표를 사용하여 모든 주문의 상태(예: 취소된 주문, 배송된 주문, 완료된 주문 또는 부정 주문)를 나타낼 수 있습니다. </p> <p>주문 상태 보고를 사용하면 어떤 획득 방법이 주문 완료율을 가장 많이 높이는지를 파악할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 리드 및 견적 {#section_0B3EAA59BEC94244BE3EB3825D719DF6}

<table id="table_85B095414F6C4644A191A94AC0CAD13D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>데이터 소스 </p> </th> 
   <th colname="col2" class="entry"> <p>처리 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>리드 생성 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>실제 발생 매출을 포함하여 웹 사이트에서 생성된 모든 리드에 대한 리드 결과 정보를 업로드할 수 있습니다. </p> <p>매출이 실제로 리드 ID에 기여하면 수익이 가장 많이 나는 캠페인과 프로모션을 파악할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>온라인 견적 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>실제 발생 매출을 포함하여 웹 사이트에서 생성된 모든 리드에 대한 리드 결과 정보를 업로드할 수 있습니다. </p> <p>매출이 실제로 리드 ID에 기여하면 수익이 가장 많이 나는 캠페인과 프로모션을 파악할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>콜 센터 데이터 </p> </td> 
   <td colname="col2"> <p> <a href="../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0" type="concept" format="dita" scope="local"> 변환 </a> </p> </td> 
   <td colname="col3"> <p>콜 센터 거래를 업로드하여 고객이 전화를 하게 만든 방법(캠페인, 프로모션 등)을 파악할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

