---
description: Data Connectors 통합 마법사는 Data Connectors 통합 프로세스를 단계별로 안내합니다.
title: Silverpop 통합
uuid: dc5e6a09-3238-412d-9980-4a105ce14819
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Silverpop 통합{#silverpop-integration}

Data Connectors 통합 마법사는 Data Connectors 통합 프로세스를 단계별로 안내합니다.

통합 구성 방법:

1. Adobe Experience Cloud의 제품 드롭다운 목록에서 Data Connectors™를 선택합니다.
1. **[!UICONTROL 새로 추가]**&#x200B;를 클릭하고 **[!UICONTROL 표시]** 드롭다운 목록에서 **[!UICONTROL 이름별]**&#x200B;을 선택합니다.
1. **Silverpop Engage 2.0** 아이콘을 찾아 Analytics 보고서 세트의 빈 플러그인 슬롯으로 끌어다 놓고 Data Connectors 통합 마법사를 시작합니다.
1. Silverpop 통합 소개 페이지에서 텍스트를 검토한 다음 확인란을 선택하여 통합과 관련된 비용을 수락합니다.
1. 이 통합에 사용할 보고서 세트를 선택합니다.
1. 이 통합을 식별하려면 친숙한 이름을 제공한 다음 **[!UICONTROL 이 통합 생성 및 구성]**&#x200B;을 클릭합니다.

   이 페이지는 자세한 정보에 대한 유용한 링크와 함께 통합 개요를 제공합니다. 이 통합과 관련된 Adobe와 Silverpop 요금이 있습니다. 두 조직의 영업 담당자에게 연락하여 요금 구성을 확인합니다.
1. Data Connectors 통합 마법사의 각 페이지에서 다음 표에 설명된 대로 필요한 정보를 제공합니다.

<table id="table_74EC1EEBE7A548AB878AA40187EBCD30"> 
 <thead> 
  <tr valign="top"> 
   <th colname="col2" class="entry"> <p> <b>필드</b> </p> </th> 
   <th colname="col03" valign="top" align="left" class="entry"> <p> <b>구성 섹션</b> </p> </th> 
   <th colname="col3" class="entry"> <p> <b>설명</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col2" valign="top" align="left"> <p>통합 이름 </p> </td> 
   <td colname="col03"> <p>(1) 통합 설정 </p> </td> 
   <td colname="col3"> <p>Data Connectors가 보고서 세트의 활성 통합 목록에 표시하는 통합 이름을 지정합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2" valign="top" align="left"> <p>파일 다운로드 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p> 파일 다운로드 리마케팅에 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p> 이메일 주소 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>알려진 Silverpop ID가 없는 방문자에 대한 리마케팅에 사용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>계정 ID </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>Silverpop 계정 ID(Silverpop에서 조직에 할당된 고유 식별자)를 지정한 다음 <b>다음</b>을 클릭하여 마법사의 3단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>양식 이름 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>양식 포기 리마케팅에 사용 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>메일링 ID </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Silverpop ID </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p> 바운스 수 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) 이메일 시스템에서 가져온 이메일 총 바운스 수 데이터를 저장하는 Analytics 이벤트를 지정합니다. </p> <p>총 바운스 수 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>클릭됨 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) 이메일 시스템에서 가져온 이메일 클릭 수 데이터를 저장하는 Analytics 이벤트를 지정합니다. </p> <p>클릭됨 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> 파일 다운로드됨 </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p> 파일 다운로드 리마케팅에 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> 양식 완료됨 </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>양식 포기 리마케팅에 사용 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> 양식 시작됨 </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>양식 포기 리마케팅에 사용 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>열림 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) 이메일 시스템에서 가져온 이메일 열림 데이터를 저장하는 Analytics 이벤트를 지정합니다. </p> <p>열림 이벤트를 사용하면 이메일 메시지를 연 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>보냄 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) 이메일 시스템에서 가져온 이메일 보냄 데이터를 저장하는 Analytics 이벤트를 지정합니다. </p> <p>보냄 이벤트를 사용하여 전송된 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>가입 해지됨 </p> </td> 
   <td colname="col03"> <p>(2) 변수 매핑 </p> </td> 
   <td colname="col3"> <p>(필수) 이메일 시스템에서 가져온 이메일 가입 해지됨 데이터를 저장하는 Analytics 이벤트를 지정합니다. </p> <p>가입 해지됨 이벤트를 사용하면 이메일 메시지를 열었지만 나중에 가입 해지 링크를 클릭하여 조직에서 발송하는 향후 이메일 메시지를 거부한 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>세그먼트 </p> </td> 
   <td colname="col03"> <p>(3) 데이터 설정 </p> </td> 
   <td colname="col3"> <p>이 통합은 파트너 세그먼트 섹션에 표시되는 파트너 정의 세그먼트를 만듭니다. </p> <p>또한 통합에 포함할 기존 보고서 세트 수준 세그먼트를 선택할 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>액세스 요청 </p> </td> 
   <td colname="col03"> <p>(3) 데이터 설정 </p> </td> 
   <td colname="col3"> <p> (필수) <span class="uicontrol">이 통합에서 제품 데이터를 다운로드하도록 허용합니다</span>를 활성화합니다. </p> <p>선택 사항: 이 통합에서 수익, 주문 및 판매량을 다운로드하도록 허용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>데이터 수집 </p> </td> 
   <td colname="col03"> <p>(3) 데이터 설정 </p> </td> 
   <td colname="col3"> <p>s_code.js 플러그인을 이 통합에 대한 수집 모델로 사용하려면 <b>JavaScript 플러그인</b>을 선택합니다(<a href="../silverpop-overview/silverpop-analytics-code.md"> Analytics 플러그인 코드</a> 참조). </p> <p>이 통합에 자동화된 수집 모델을 사용하려면 <b>자동화된 솔루션</b>을 선택한 다음 이 통합에 사용되는 고유 식별자를 지정합니다. </p> <p>이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다. </p> <p> <b>메시지 ID 쿼리 문자열 매개 변수</b>: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 메시지 ID를 나타냅니다. </p> <p> <b>수신인 ID 쿼리 문자열 매개 변수</b>: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 수신자 ID를 나타냅니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>대시보드 및 책갈피 생성 </p> </td> 
   <td colname="col03"> <p>(4) 보고서 설정 </p> </td> 
   <td colname="col3"> <p>통합에 사용할 대시보드 및 책갈피를 자동으로 생성합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

