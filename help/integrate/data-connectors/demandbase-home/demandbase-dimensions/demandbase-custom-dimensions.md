---
description: Adobe 통합 마법사의 4 단계에서 지정할 수 있는 선택적 차원 식별자를 나열합니다.
seo-description: Adobe 통합 마법사의 4 단계에서 지정할 수 있는 선택적 차원 식별자를 나열합니다.
seo-title: Demandbase 사용자 정의 차원
title: Demandbase 사용자 정의 차원
uuid: D 1621046-3 AA 2-46 B 9-A 536-4 A 8 FB 792 B 69 F
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Demandbase Custom Dimensions{#demandbase-custom-dimensions}

Adobe 통합 마법사의 4 단계에서 지정할 수 있는 선택적 차원 식별자를 나열합니다.

마법사에 입력할 API ID를 정확히 모르는 경우 Demandbase 담당자에게 문의하십시오.

>[!IMPORTANT]
>
>IP 주소는 사용자 정의 차원으로 포함하지 않는 것이 좋습니다. 고유값이 너무 많으면 보고에 성능 문제가 발생할 수 있습니다. 또한, IP 주소는 Adobe 데이터 웨어하우스 보고를 통해 보고 옵션으로 이미 제공됩니다.

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
   <td colname="col2"> ISP </td> 
   <td colname="col3"> 식별된 조직이 ISP로 분류되는지 여부를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 마케팅 별칭 </td> 
   <td colname="col2"> marketing_ alias </td> 
   <td colname="col3"> 광고, 메시지 또는 마케팅 사본에 사용할 정리 및/또는 축약된 조직 이름 (32 자 이하) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 계정 감시 태그 </td> 
   <td colname="col2"> watch_ list (custom) </td> 
   <td colname="col3">조직별로 API 응답 데이터에 추가될 수 있는 클라이언트가 정의한 태그의 무제한 세트입니다. <p><b></b>예: Q 4 Target 이라는 감시 태그가 있는 경우 API 필드는 </p> <code> watch_ list_ q 4_ target</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fortune 1000 </td> 
   <td colname="col2"> Fortune_ 1000 </td> 
   <td colname="col3"> 조직이 Fortune 1000 목록에 속하는지 여부를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Forbes 2000 </td> 
   <td colname="col2"> Forbes_ 2000 </td> 
   <td colname="col3"> 조직이 Forbes 2000 목록에 있는지를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 직원 수 </td> 
   <td colname="col2"> employee_ count </td> 
   <td colname="col3"> 조직에 고용된 사람 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 연간 영업 </td> 
   <td colname="col2"> annual_ sales </td> 
   <td colname="col3"> 공공 기관의 경우 연간 수익은 모든 위치에서 글로벌 HQ에 대한 회사에서 보고한 공개 기록을 기반으로 합니다. 민간 기업의 경우 연간 영업 수익 번호에 대한 합의를 기반으로 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 전화 번호 </td> 
   <td colname="col2"> 전화 번호 </td> 
   <td colname="col3"> 식별된 조직의 전화 번호입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 주소 </td> 
   <td colname="col2"> street_ address </td> 
   <td colname="col3"> 식별된 조직의 주소. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구/군/시 </td> 
   <td colname="col2"> 구/군/시 </td> 
   <td colname="col3"> 식별된 조직의 구/군/시입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주/도 </td> 
   <td colname="col2"> state </td> 
   <td colname="col3"> 식별된 조직의 상태. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 국가 코드 </td> 
   <td colname="col2"> country_ code </td> 
   <td colname="col3"> 식별된 조직의 ISO 2 문자 국가 코드입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 국가 이름 </td> 
   <td colname="col2"> country_ name </td> 
   <td colname="col3"> 식별된 조직에 대한 국가의 문자열 값 국가 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zip </td> 
   <td colname="col2"> zip </td> 
   <td colname="col3"> 식별된 조직의 국가/주의 우편 번호. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 웹 사이트 </td> 
   <td colname="col2"> web_ site </td> 
   <td colname="col3"> 식별된 조직이 사용하는 URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주식 시세 </td> 
   <td colname="col2"> stock_ ticker </td> 
   <td colname="col3"> 식별된 조직이 공개적으로 거래되는 경우의 주식 주식 시세 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본 SIC 코드 </td> 
   <td colname="col2"> primary_ sic </td> 
   <td colname="col3"> 콘센트 SIC 코드는 식별된 조직에 대해 지정됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 위도 </td> 
   <td colname="col2"> 위도 </td> 
   <td colname="col3"> 위도는 식별된 조직의 위치입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 경도 </td> 
   <td colname="col2"> 경도 </td> 
   <td colname="col3"> 식별된 조직의 위치에 대한 경도입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 트래픽 </td> 
   <td colname="col2"> 트래픽 </td> 
   <td colname="col3"> 웹 사이트 트래픽 양이 낮음, 보통, 높음 또는 매우 높음 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2B </td> 
   <td colname="col2"> b2b </td> 
   <td colname="col3"> 식별된 회사가 주로 다른 비즈니스에 판매됨을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2C </td> 
   <td colname="col2"> b2c </td> 
   <td colname="col3"> 식별된 회사가 주로 소비자 또는 개인에게 판매됨을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기술 통찰력 </td> 
   <td colname="col2"> ??? </td> 
   <td colname="col3"> 카테고리, 공급업체 및 제품을 통해 고객이 정의하는 최대 75 개의 기술 카테고리로 광고, 메시지 또는 마케팅 카피를 타깃팅하거나 사용자 정의할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

