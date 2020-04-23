---
description: 방문자 위치에 대한 데이터를 표시합니다. 지리 특성 보고서에는 국가, 지역, 도시, 미국 주 및 미국 DMA(디지털 마케팅 영역)가 포함됩니다. 지리 특성 보고서는 모든 고객에 대해 활성화됩니다.
title: 지리 특성
topic: Reports
uuid: 66aa22c4-dcbc-491a-b23c-0c3d87444d23
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# 지리 특성

방문자 위치에 대한 데이터를 표시합니다. 지리 특성 보고서에는 국가, 지역, 도시, 미국 주 및 미국 DMA(디지털 마케팅 영역)가 포함됩니다. 지리 특성 보고서는 모든 고객에 대해 활성화됩니다.

보고 및 분석의 다른 곳에서 사용할 수 있는 모든 지표는 자동으로 국가, 지역, 도시, 미국 주 및 DMA 보고서에 포함됩니다.전환 및 방문 기반 지표와 계산된 지표를 참조하십시오. For more information, see this Adobe [blog](https://blogs.adobe.com/digitalmarketing/analytics/introducing-new-metrics-in-geosegmentation-and-more/) post.

<table id="table_566CFFC82E1149D8BAFE6641627FCF1F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 보고서 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 국가 </td> 
   <td colname="col2"> <p> 가장 큰 지리적 분할 대부분의 보고서에서 사용할 수 있는 표준 등급 및 트렌드 보기 외에도 총 트래픽에 대한 상대적 기여에 따라 주의 색상을 달리하는 "맵" 보기가 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지역 </td> 
   <td colname="col2"> <p> 국가보다 작지만 도시보다 큰 지리적 영역. 일부 국가에서는 지역이 주, 도 또는 현입니다. 다른 지역에서는 국가, 부서 또는 대도시 지역입니다. 표시된 각 영역의 오른쪽에 해당 지역의 국가도 괄호 안에 표시됩니다. </p> <p>테이블 세부 사항에서 이 지역에 대한 도시 보고서 실행(확대경)을 클릭하여 선택한 지역의 도시가 해당 지역의 다른 도시와 비교하여 어떻게 수행되었는지 보여주는 보고서를 실행합니다. </p> <p>See <a href="/help/components/c-variables/dimensionslist/reports-geosegmentation-reference.md"  > GeoSegmentation Regions and Postal Code usage by Country</a> to see which countries use regions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시 </td> 
   <td colname="col2"> <p> 가장 작은 지리적 분할 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 미국 주(州) </td> 
   <td colname="col2"> <p> 미국의 각 주에 대한 방문자를 보여주는 히트 맵. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 미국 DMA </td> 
   <td colname="col2"> <p> (디지털 마케팅 지역) 미국 전역의 라디오 및 TV를 위한 미디어 시장 분할 특정 상태 내의 마케팅 영역만 표시하도록 보고서를 필터링할 수 있습니다. 이 데이터는 Adobe와 Nielsen Media Research, Inc. 간의 파트너 관계를 통해 제공됩니다. </p> <p>참고: 미국 DMA 보고서의 지정되지 않음 항목은 특정 DMA와 관련 지을 수 없었던 방문자를 가리킵니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 보고서 정확도 </td> 
   <td colname="col2"> <p>Adobe는 선도적인 IP 인텔리전스 및 인증 솔루션 제공업체인 Digital Envoy와 파트너 관계를 맺고 최종 사용자의 IP 주소를 기반으로 지리적 측정 기능인 지리 특성 기능을 제공합니다. 개별 데이터 세트에 따른 정확도는 다를 수 있지만, 일반적으로 Digital Envoy는 국가 수준에서 99% 이상, 지역 수준에서 97% 이상, 도시 수준에서 90% 이상의 정확도를 제공합니다. </p> <p>Note: These numbers assume that <a href="/help/admin/admin/general-acct-settings-admin.md">the setting</a> to remove the last octet of the IP address is NOT enabled. </p> <p>IP 주소는 우편 번호에 매핑되고, 각 도시는 "지역 당국"이 그 도시의 일부로 정의한 우편 번호에 의해 정의됩니다. 예를 들어 베를린의 교외가 베를린 정의에 포함되지 않지만 각 도시는 별도로 나열되므로 IP 주소를 그러한 도시 중 하나의 우편 번호로 정확하게 매핑할 수 있다고 가정합니다. </p> <p>지리 특성 데이터에 영향을 줄 수 있는 몇 가지 요인은 다음과 같습니다. </p> 
    <ul id="ul_1B05024AD5174232A8DB8145753FB09B"> 
     <li id="li_C3A21E7C1186490EB9A236634DB45E7F">기업 프록시를 나타내는 IP 주소. 이러한 데이터는 사용자의 회사 네트워크를 통해 들어오는 트래픽으로 나타날 수 있으며, 이는 사용자가 원격으로 작업하는 경우 실제로 다른 위치가 될 수 있습니다. </li> 
     <li id="li_56FC36B3598C420F9246D4E8772822A7">모바일 IP 주소. 모바일 IP 타깃팅은 위치 및 네트워크에 따라 다양한 수준에서 작동합니다. 많은 통신 사업자는 중앙 또는 지역 POP를 통해 IP 트래픽을 역수송합니다. </li> 
     <li id="li_C1EED854AE584489BCBC2A7AA20B8EF1">위성 ISP 사용자에 속하는 IP 주소. 이러한 사용자의 특정 위치를 식별하기 어려운 것은 일반적으로 업링크 위치에서 오는 것처럼 보입니다. </li> 
     <li id="li_A735756F39554DF19E05D251CA614F02">군사 및 공공 기관 IP 이것은 종종 그들이 현재 주둔하고 있는 기지나 사무실이 아닌, 전 세계를 여행하고 그들의 집 위치를 통해 들어오는 사람들을 나타냅니다. </li> 
     <li id="li_ACFF1B8094684173B8325A44304CA32B">GeoSegmentation/IP 데이터는 타사 공급업체에서 제공하며 ISP 및 기타 네트워크 소스에서 제공하는 정보를 기반으로 정기적으로 업데이트됩니다. IP 조회는 전 세계적으로 자주 구매되고 판매되므로 본질적으로 불안정합니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

