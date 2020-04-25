---
description: Data Connectors 통합 마법사는 Data Connectors 통합 프로세스를 단계별로 안내합니다.
title: Data Connectors 통합 마법사 실행
uuid: 714417f7-c1df-4e61-a07f-d319f6581c9c
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Data Connectors 통합 마법사 실행{#running-the-data-connectors-integration-wizard}

Data Connectors 통합 마법사는 Data Connectors 통합 프로세스를 단계별로 안내합니다.

통합 구성 방법:

1. Experience Cloud에 로그인합니다.
1. Adobe Analytics 홈페이지의 핀휠이나 도구 모음에서 Data Connectors™ 아이콘을 클릭합니다.
1. Data Connectors 페이지에서 통합을 구성할 보고서 세트를 선택합니다.

   >[!NOTE]
   >
   >Data Connectors 페이지의 왼쪽 위 모서리에 있는 **보고서 세트** 드롭다운 목록에서 원하는 보고서 세트를 선택해야 합니다.

1. Data Connectors UI의 왼쪽 측면에 있는 **파트너 목록** 맨 위에서 **알파벳** 탭을 클릭한 다음 **Datran** 아이콘을 찾습니다.
1. **Datran** 아이콘을 Adobe Analytics 보고서 세트의 빈 플러그인 슬롯으로 끌어다 놓고 Data Connectors 통합 마법사를 시작합니다.

1. Datran 통합 소개 페이지에서 텍스트를 검토한 **다음** 확인란을 선택하여 통합과 관련된 비용을 수락합니다.

   이 페이지는 자세한 정보에 대한 유용한 링크와 함께 통합 개요를 제공합니다. 이 통합과 관련된 Adobe와 Datran 요금이 있습니다. 두 조직의 영업 담당자에게 연락하여 요금 구성을 확인합니다.
1. Data Connectors 통합 마법사의 각 페이지에서 다음 표에 설명된 대로 필요한 정보를 제공합니다.

<table id="table_74EC1EEBE7A548AB878AA40187EBCD30"> 
 <thead> 
  <tr valign="top"> 
   <th colname="col1" valign="top" align="left" class="entry"> <p><b>마법사 페이지 번호</b> </p> </th> 
   <th colname="col2" class="entry"> <p><b>필드</b> </p> </th> 
   <th colname="col3" class="entry"> <p><b>설명</b> </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2" valign="top" align="left"> <p>통합 이름 </p> </td> 
   <td colname="col3"> <p>Data Connectors가 보고서 세트의 활성 통합 목록에 표시하는 통합 이름을 지정합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>통합 이메일 주소 </p> </td> 
   <td colname="col3"> <p>이 통합과 관련된 모든 알림을 받는 이메일 주소를 지정한 다음 <b>다음</b>을 클릭하여 마법사의 2단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>계정 ID </p> </td> 
   <td colname="col3"> <p>Datran 계정 ID(Datran에서 조직에 할당된 고유 식별자)를 지정한 다음 <b>다음</b>을 클릭하여 마법사의 3단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>메시지 ID </p> </td> 
   <td colname="col3"> <p>이메일 메시지 ID를 추적하는 데 사용되는 Adobe Analytics eVar를 식별합니다. </p> <p>메시지 ID는 마케팅/리마케팅 캠페인에 사용됩니다. 메시지 ID를 "추적 코드"라고도 합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>수신자 ID </p> </td> 
   <td colname="col3"> <p>이메일 수신자 ID를 추적하는 데 사용되는 Adobe Analytics eVar를 식별합니다. </p> <p>수신자 ID는 마케팅/리마케팅 캠페인에 사용됩니다. 메시지 ID를 "방문자 코드"라고도 합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>수락 확인란 </p> </td> 
   <td colname="col3"> <p>수락 확인란 옆에 표시되는 정보를 검토합니다. </p> <p><i>"수신자 ID" 추적을 활성화하면 이 기능이 사이트 방문자의 개인 식별 정보를 추적할 수 있음을 이해합니다. 따라서 조직에서는 사이트 방문자에게 통지하고 동의를 구하는 등과 같이 개인정보 보호를 위한 적절한 절차를 구현해야 합니다.</i> </p> <p>수락 문구에 동의하는 경우 확인란을 선택하고 <b>다음</b>을 클릭하여 마법사의 4단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>고객 정의 보고서 세트 수준 세그먼트 </p> </td> 
   <td colname="col3"> <p>이 통합은 통합 마법사의 통합 세그먼트 페이지 왼쪽에 표시되는 파트너 정의 세그먼트를 만듭니다. </p> <p>또한 통합에 포함할 기존 보고서 세트 수준 세그먼트를 선택할 수 있습니다. </p> <p>페이지 오른쪽에서 원하는 세그먼트를 선택한 다음 <b>다음</b>을 클릭하여 마법사의 5단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>클릭됨 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 클릭 수 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>클릭됨 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>열림 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 열림 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>열림 이벤트를 사용하면 이메일 메시지를 연 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>보냄 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 보냄 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>클릭됨 이벤트를 사용하여 전송된 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>총 바운스 수 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 총 바운스 수 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>총 바운스 수 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>가입 해지됨 </p> </td> 
   <td colname="col3"> <p>이메일 시스템에서 가져온 이메일 가입 해지됨 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. </p> <p>가입 해지됨 이벤트를 사용하면 이메일 메시지를 열었지만 나중에 가입 해지 링크를 클릭하여 조직에서 발송하는 향후 이메일 메시지를 거부한 방문자 수를 볼 수 있습니다. </p> <p>다음을 클릭하여 마법사의 6단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p>데이터 수집: JavaScript 플러그인 </p> </td> 
   <td colname="col3"> <p>이 통합을 위해 플러그인을 수집 모델로 사용하려면 <b>JavaScript</b> 플러그인을 선택하고 <b>다음</b>을 클릭하여 마법사의 7단계로 진행합니다. </p> <p> <p>참고:  자동화된 솔루션이 기본 선택입니다. </p> </p> <p>이 통합에 사용되는 JavaScript 플러그인 사본을 얻으려면 Adobe 컨설턴트에게 문의하십시오. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p>데이터 수집: 자동화된 솔루션 </p> </td> 
   <td colname="col3"> <p>이 통합에 자동화된 수집 모델을 사용하려면 <b>자동화된 솔루션</b>을 선택한 다음 이 통합에 사용되는 고유 식별자를 지정합니다. </p> <p> <p>참고:  자동화된 솔루션이 기본 선택입니다. </p> </p> <p>이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다. </p> <p><b>메시지 ID 쿼리 문자열 매개 변수</b>: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 메시지 ID를 나타냅니다. </p> <p><b>수신인 ID 쿼리 문자열 매개 변수</b>: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 수신자 ID를 나타냅니다. </p> <p><b>다음</b>을 클릭하여 마법사의 7단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>통합 요약 </p> </td> 
   <td colname="col3"> <p>각 카테고리 옆에 있는 더하기(+) 기호를 클릭하여 통합 매개 변수를 확인한 다음 <b>저장</b>을 클릭하여 마법사의 8단계로 진행합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p>통합 완료 </p> </td> 
   <td colname="col3"> <p><b>완료</b>를 클릭하여 통합을 완료합니다. </p> <p><b>중요:</b> Adobe Analytics에서는 <b>마침</b>을 클릭할 때까지 통합 설정을 저장하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
