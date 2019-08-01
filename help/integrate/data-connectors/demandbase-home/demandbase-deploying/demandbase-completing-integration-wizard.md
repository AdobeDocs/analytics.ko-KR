---
description: 통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 구성 마법사를 완료해야 합니다.
seo-description: 통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 구성 마법사를 완료해야 합니다.
seo-title: Adobe 통합 마법사 완료
title: Adobe 통합 마법사 완료
uuid: 75260 b 92-a 6 f 5-44 b 6-b 3 ea-d 5945 fdd 1 ecb
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Completing the Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 구성 마법사를 완료해야 합니다.

1. Adobe Marketing Cloud 내의 데이터 커넥터 (이전 Genesis) 영역으로 이동합니다.
1. Demandbase 2.0 통합 마법사를 실행합니다.
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
   <td colname="col2"> Demandbase 담당자가 이를 얻을 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 사용자 지정 Demandbase Dimension # N </td> 
   <td colname="col2"> 이것은 8 개의 선택적 차원에 대한 ID 입니다. 자세한 내용은 Demandbase 사용자 정의 차원을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Target로 보내기 </td> 
   <td colname="col2">" true "인 경우 Demandbase 차원은 숨겨진 mbox를 사용하여 Adobe Target 에도 전송됩니다. <p>참고: 차원을 수집하려면 웹 페이지에서 구성된 mbox. js 파일을 구현해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 다음 변수 매핑 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | Demandbase Dimensions | 보고서 세트에서 사용 가능한 Evar 변수를 선택합니다. |
   | Demandbase 사용자 정의 차원 (선택 사항) | 보고서 세트에서 사용 가능한 Evar 변수를 선택합니다. |

1. 사용자 지정 차원에 대한 이름을 구성합니다 (해당하는 경우).

   1. 4 단계에서 사용자 지정 차원을 포함하도록 선택하고 5 단계에서 선택적 Evar를 매핑했다면 해당 차원에 대해 친숙한 이름을 제공해야 합니다. 예를 들어, 사용자 지정 차원 1로 «stock_ ticker» 를 입력하도록 선택한 경우 «dimension 1» 이 들어 있는 상자를 «Stock Ticker» 로 변경해야 합니다.
   1. Do **NOT** modify the names of the standard 8 dimensions (i.e. Demandbase SID, Company Name, Industry, etc.).

1. Demandbase Integration Dashboard를 자동으로 만들도록 상자를 선택합니다 (권장).
1. Review all configuration items and click **[!UICONTROL Activate Now]**.

