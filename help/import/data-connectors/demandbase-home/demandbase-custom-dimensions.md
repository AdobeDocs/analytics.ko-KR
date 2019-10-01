---
description: Adobe 통합 마법사의 4단계에서 지정할 수 있는 선택적 차원 식별자를 나열합니다.
seo-description: Adobe 통합 마법사의 4단계에서 지정할 수 있는 선택적 차원 식별자를 나열합니다.
seo-title: Demandbase 사용자 지정 차원
title: Demandbase 사용자 지정 차원
uuid: d1621046-3aa2-46b9-a536-4a8fb792b69f
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

---


# Demandbase 사용자 지정 차원{#demandbase-custom-dimensions}

Adobe 통합 마법사의 4단계에서 지정할 수 있는 선택적 차원 식별자를 나열합니다.

마법사에 들어갈 정확한 API ID를 잘 모르는 경우 Demandbase 담당자에게 문의하십시오.

>[!IMPORTANT]
>
>IP 주소를 사용자 지정 차원으로 포함하지 않는 것이 좋습니다. 고유 값이 너무 많으면 보고 시 성능 문제가 발생할 수 있습니다. 또한 IP 주소는 이미 Adobe 데이터 웨어하우스 보고를 통해 보고 옵션으로 제공됩니다.

<table id="table_3B44A18BE5FE45BC83389F89B48D9B97"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 차원 </th> 
   <th colname="col2" class="entry"> API ID </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ISP </td> 
   <td colname="col2"> isp </td> 
   <td colname="col3"> 식별된 조직이 ISP로 분류되는지 여부를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 마케팅 별칭 </td> 
   <td colname="col2"> marketing_alias </td> 
   <td colname="col3"> 광고, 메시지 또는 마케팅 카피에 사용할 조직명(32자 이하)을 정리했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 계정 감시 태그 </td> 
   <td colname="col2"> watch_list(사용자 정의) </td> 
   <td colname="col3">조직에서 API 응답 데이터에 추가할 수 있는 클라이언트가 정의한 태그의 무제한 집합. <p><b>예</b>:Q4 Target이라는 감시 태그가 있는 경우 API 필드는 </p> <code> watch_list_q4_target</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fortune 1000 </td> 
   <td colname="col2"> fortune_1000 </td> 
   <td colname="col3"> 조직이 포춘 1000 목록에 있는지 여부를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2000년 포브스 </td> 
   <td colname="col2"> forbes_2000 </td> 
   <td colname="col3"> 조직이 Forbes 2000 목록에 있는지 여부를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 직원 수 </td> 
   <td colname="col2"> employee_count </td> 
   <td colname="col3"> 조직에 고용된 사람의 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 연간 영업 </td> 
   <td colname="col2"> annual_sales </td> 
   <td colname="col3"> 공공 기관의 경우 연간 수익은 모든 위치의 글로벌 HQ에 대해 회사가 보고한 공개 기록을 기반으로 합니다. 민간 기업의 경우 연간 판매 수익에 대한 컨센서스를 기반으로 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 전화 번호 </td> 
   <td colname="col2"> 전화 </td> 
   <td colname="col3"> 식별된 조직의 전화 번호입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> street_address </td> 
   <td colname="col3"> 식별된 조직의 주소. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구/군/시 </td> 
   <td colname="col2"> city </td> 
   <td colname="col3"> 그 조직의 구/군/시가 확인되었다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주/도 </td> 
   <td colname="col2"> state </td> 
   <td colname="col3"> 식별된 조직의 상태입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 국가 코드 </td> 
   <td colname="col2"> country_code </td> 
   <td colname="col3"> 식별된 조직의 ISO 2문자 국가 코드입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 국가 이름 </td> 
   <td colname="col2"> country_name </td> 
   <td colname="col3"> 식별된 조직에 대한 국가의 문자열 값 국가 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zip </td> 
   <td colname="col2"> zip </td> 
   <td colname="col3"> 식별된 조직의 국가/주 우편번호입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 웹 사이트 </td> 
   <td colname="col2"> web_site </td> 
   <td colname="col3"> 식별된 조직에서 사용하는 URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주식 시세 </td> 
   <td colname="col2"> stock_ticker </td> 
   <td colname="col3"> 해당 단체가 공개적으로 거래되면 주식 시세는 악화될 것이다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본 SIC 코드 </td> 
   <td colname="col2"> primary_sic </td> 
   <td colname="col3"> 식별된 조직에 대해 지정된 합의 SIC 코드. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 위도 </td> 
   <td colname="col2"> latitude </td> 
   <td colname="col3"> 식별된 조직의 위치를 위한 위도. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 경도 </td> 
   <td colname="col2"> 경도 </td> 
   <td colname="col3"> 식별된 조직의 위치에 대한 경도입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 트래픽 </td> 
   <td colname="col2"> 트래픽 </td> 
   <td colname="col3"> 웹 사이트 트래픽이 낮거나, 보통 또는 높거나 매우 높을 것으로 예상되는 금액입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2B </td> 
   <td colname="col2"> b2b </td> 
   <td colname="col3"> 식별된 회사가 주로 다른 기업에 판매됨을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2C </td> 
   <td colname="col2"> b2c </td> 
   <td colname="col3"> 식별된 회사가 주로 소비자 또는 개인에게 판매됨을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Technology Insight </td> 
   <td colname="col2"> ??? </td> 
   <td colname="col3"> 광고, 메시지 또는 마케팅 카피를 타깃팅 및/또는 맞춤화하기 위해 카테고리, 공급업체 및 제품을 통해 고객이 정의한 최대 75개의 기술 카테고리 </td> 
  </tr> 
 </tbody> 
</table>

