---
description: 통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 구성 마법사를 완료해야 합니다.
seo-description: 통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 구성 마법사를 완료해야 합니다.
seo-title: Adobe 통합 마법사 완료
title: Adobe 통합 마법사 완료
uuid: 75260b92-a6f5-44b6-b3ea-d5945fdd1ecb
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Adobe 통합 마법사 완료{#completing-the-adobe-integration-wizard}

통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 구성 마법사를 완료해야 합니다.

1. Adobe Experience Cloud 내에서 데이터 커넥터(이전 Genesis) 영역으로 이동합니다.
1. Demandbase 2.0 통합 마법사를 시작합니다.
1. 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. 다음 항목을 구성합니다.

<table id="table_8D60DC7C48C144DC9934749E7F9F65FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 항목 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이메일 주소 </td> 
   <td colname="col2"> 기본 연락처의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> (선택 사항) 이 통합 설정에 대한 설명입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Demandbase API 키 </td> 
   <td colname="col2"> Demandbase 담당자로부터 받을 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 사용자 지정 Demandbase 차원 #N </td> 
   <td colname="col2"> 8개의 선택적 차원에 대한 ID입니다. 자세한 내용은 Demandbase 사용자 지정 차원을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Target으로 보내기 </td> 
   <td colname="col2">"true"이면 숨겨진 mbox를 사용하여 Demandbase 차원도 Adobe Target으로 전송됩니다. <p>참고: 차원을 수집하려면 구성된 mbox.js 파일을 웹 페이지에 구현해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 다음 변수 매핑 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | Demandbase 차원 | 보고서 세트에서 사용 가능한 eVar 변수를 선택합니다. |
   | Demandbase 사용자 지정 차원(선택 사항) | 보고서 세트에서 사용 가능한 eVar 변수를 선택합니다. |

1. 사용자 지정 차원의 이름을 구성합니다(해당하는 경우).

   1. 4단계에서 사용자 지정 차원을 포함시키고 5단계에서 선택적 eVar를 매핑하도록 선택한 경우 해당 차원에 대해 친숙한 이름을 제공해야 합니다. 예를 들어 "stock_ticker"를 사용자 지정 차원 1로 입력하도록 선택한 경우 "Dimension 1"이 포함된 상자를 "Stock Ticker"로 변경해야 합니다.
   1. 표준 **8** 차원의 이름(즉, Demandbase SID, Company Name, Industry 등)은 수정하지 마십시오.

1. Demandbase 통합 대시보드를 자동으로 만들려면 이 확인란을 선택합니다(권장).
1. 모든 구성 항목을 검토하고 지금 **[!UICONTROL 활성화를 클릭합니다]**.

