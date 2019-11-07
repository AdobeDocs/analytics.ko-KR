---
description: '제출하는 ID가 Analytics에서 데이터 주체와 연결할 수 있는 모든 히트 데이터를 항상 포함하는 것은 아닙니다. Analytics에서는 연결된 데이터를 데이터 개인 정보 보호 요청에 포함하도록 확장된 ID 세트를 만들 수 있습니다. 제출한 각 데이터 개인 정보 보호 요청에 대해 선택적 매개 변수와 함께 이 옵션을 요청하여 JSON 요청에 추가할 수 있습니다. '
title: ID 확장
uuid: 2672d17d-c957-4e08-8dd9-16d54bf2be18
translation-type: tm+mt
source-git-commit: 12a7452337307ca019c005dc20e3b551d96e1289

---


# ID 확장

제출하는 ID가 Analytics에서 데이터 주체와 연결할 수 있는 모든 히트 데이터를 항상 포함하는 것은 아닙니다. Analytics에서는 연결된 데이터를 데이터 개인 정보 보호 요청에 포함하도록 확장된 ID 세트를 만들 수 있습니다. 제출한 각 데이터 개인 정보 보호 요청에 대해 선택적 매개 변수와 함께 이 옵션을 요청하여 JSON 요청에 추가할 수 있습니다.

```
"expandIds": true
```

요청에 이 옵션을 포함시키는 방법에 대한 예는 [샘플 JSON 요청](/help/admin/c-data-governance/gdpr-submit-access-delete.md#sample-json-request)을 참조하십시오. For more details, refer to the [Privacy Service API documentation](https://www.adobe.io/apis/experienceplatform/gdpr.html).

<table id="table_A10CA8DC8C1643CF84A4DF30A6740D51"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 유형 </th> 
   <th colname="col2" class="entry"> 고려 사항 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>쿠키 ID 확장 </p> </td> 
   <td colname="col2"> <p>원래 기존 <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_analytics.html">Analytics 쿠키</a>를 사용했던 많은 Analytics 고객이 지금은 이전에 MCID(Marketing Cloud ID Service)로 알려졌던 <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/">ECID(Identity Service)</a>를 사용합니다. 전환 후 처음 방문한 해당 웹 사이트 방문자의 경우 ECID만 존재합니다. 하지만 기존 쿠키만 사용할 수 있을 때 처음 방문하고 이후에 방문한 방문자의 경우에는 일부 데이터에 두 쿠키가 모두 있지만, 드문 경우, 이전 데이터에는 Analytics 쿠키만 있고 최신 데이터에는 ECID만 있을 수 있습니다. </p> <p>Analytics(방문자 ID) 쿠키 또는 ECID를 통해 식별된 방문자에 대한 모든 데이터를 찾으려고 합니다. 따라서 현재 ECID를 사용하고 이전에 Analytics 쿠키를 사용한 경우 두 가지 유형의 ID 중 하나를 사용하여 요청을 제출할 때마다 두 ID를 요청에 포함하거나 expandIds 옵션을 지정해야 합니다. expandIds를 지정하면 Adobe는 사용자가 제공한 쿠키 ID에 해당하는 다른 ECID 또는 Analytics 쿠키를 확인합니다. 새로 식별된 쿠키 ID를 포함하도록 요청이 자동으로 확장됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>쿠키 ID 확장에 대한 사용자 지정 ID </p> </td> 
   <td colname="col2"> <p>전자 상거래 웹 사이트에서는 방문자가 사이트에 로그인하기 전에 사이트를 탐색하고 장바구니에 항목을 추가한 후, 체크아웃 절차를 시작하는 일이 흔합니다. 데이터 개인 정보 보호 요청에 대해 사용자를 식별하는 데 사용된 ID가 사용자가 로그인한 경우에만 사용자 지정 변수에 저장되는 경우 이 사전 로그인 활동은 ID와 연관되지 않습니다. Analytics 쿠키 ID를 사용하면 쿠키 ID가 로그인하는 동안 유지되므로 고객이 로그인 전에 수행한 탐색과 로그인 후 구매한 항목을 연결하도록 선택할 수 있습니다. </p> <p>구현 시 사용자 지정 변수(prop 또는 eVar) 또는 사용자 정의 방문자 ID에 로그인 ID(CRM ID, 사용자 이름, 로열티 번호, 전자 메일 주소 등, 또는 이러한 값 중 하나의 해시)를 저장하고 데이터 개인 정보 보호 액세스 요청에 대해 이 ID를 사용한다고 가정해 봅시다. 데이터 주체는 탐색에 대한 모든 정보가 액세스 요청의 일부로 반환되지 않고, 특히 보긴 했지만 아직 구입하지 않은 항목으로 승격시킨 경우 반환되지 않는다는 점에 대해 의아해할 수 있습니다. </p> <p>따라서 Analytics 데이터 개인 정보 보호 처리에서는 ID 확장을 지원합니다. 그러면 Analytics에서 사용자 지정 ID와 동일한 히트에서 발생하는 모든 쿠키 ID를 찾아서 그러한 ID를 포함하도록 요청을 확장합니다. </p> <p>쿠키 네임스페이스 이외의 모든 네임스페이스와 함께 expandIDs가 지정된 경우, 요청은 지정된 ID를 포함하는 히트에 있는 모든 쿠키 ID(ECID 또는 Analytics 쿠키)를 포함하도록 확장됩니다. 위에서 설명한 대로 쿠키 ID 확장은 새로 발견된 모든 쿠키 ID에서 수행됩니다. </p> <p>expandIDs 옵션이 액세스 요청에 사용되고 지정된 ID에 ID-PERSON 레이블이 있는 경우 두 개의 파일 세트가 반환됩니다. 첫 번째 세트(개인 세트)는 지정된 ID가 발견된 히트의 데이터만 포함합니다. 두 번째 세트(장치 세트)는 지정된 ID가 없는 확장된 ID의 히트에서만 데이터를 포함합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

데이터 개인 정보 보호가 시행된 후 처음 몇 개월 동안 대부분의 Analytics 데이터 개인 정보 보호 요청이 ID 확장을 요청하지 않았지만 조직에 대한 적절한 값을 결정하는 것은 귀하의 책임입니다. 귀하가 사용 중인 ID의 데이터 및 Adobe Analytics에서 수집한 데이터에 ID 확장이 필요한지 여부는 귀하의 법률팀과 상의해야 합니다. 여러 사용자가 귀하의 사이트를 방문한 공유 장치에 대한 주요 고려 사항은 ID 확장을 사용하면 장치 파일의 액세스 요청에 의해 반환된 데이터에 장치의 다른 사용자가 히트한 데이터가 포함된다는 것입니다. 라벨 지정 시 모범 사례를 따랐더라도 방문한 페이지와 같은 개인 데이터가 장치 파일에 포함되지 않으면 장치 파일에는 방문한 페이지 수와 각 방문 시간이 포함됩니다. 방문자가 아닌 다른 사람과 이 정보를 공유해도 괜찮습니까?

ID 확장이 사용되지 않는 삭제 요청의 경우 쿠키가 아닌 ID(ECID 또는 Analytics 쿠키 이외의 ID)를 사용하여 삭제해야 하는 히트와 해당 ID에 ID-DEVICE 라벨이 있는 히트를 식별해야 하는 경우 쿠키 ID의 일부 인스턴스만 익명화되고 나머지는 변경되지 않으므로 보고서의 순 방문자 수는 변경됩니다. ID 확장을 지정하지 않는 경우 요청에 쿠키 ID를 사용하거나 ID-PERSON 레이블로 ID를 사용하는 것이 좋습니다.

Adobe는 ID 확장을 수행할 때 전체 데이터 스캔을 추가로 요구할 수 있습니다. 그런 경우, Adobe가 요청을 완료하는 데 걸리는 시간이 늘어나고 처리 시간에 일주일씩 추가되는 경우가 많습니다.

## 기타 데이터 개인 정보 보호 요청 플래그

다음 "expandIDs" 플래그 외에 Analytics에서는 데이터 개인 정보 보호 요청 일부로 전달될 수 있는 두 가지 다른 플래그를 지원합니다. 이러한 플래그 및 기본값은 다음과 같습니다.

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

향후에 "analyticsDeleteMethod"는 "anonymize"라는 기본값 외에 "purge"라는 값을 지원할 수 있습니다. 지원되면 DEL 레이블이 있는 히트 필드의 값을 단순히 업데이트하는 것이 아니라 전체 히트가 삭제됩니다.

기본값 외에 우선순위 필드는 "low" 값도 지원합니다. 데이터 주제 요청의 결과가 아닌 요청에 대해 이 값을 지정해야 하므로 30일 이내에 완료해야 할 법률상의 요구가 없습니다. Adobe에서는 데이터 주제가 요청을 시작했다는 것 외에 여러 이유로 데이터 개인 정보 보호 API의 사용을 막고 있습니다. 데이터 개인 정보 보호 API는 데이터 정리 또는 복구에 적합한 도구가 아니므로 의도하지 않은 결과가 발생합니다.

> [!NOTE][데이터 개인 정보 보호 API](https://www.adobe.io/apis/experienceplatform/gdpr.html)는 시간에 민감한 데이터 개인 정보 보호 요청을 이행하는 데 도움을 주기 위해 제공되었습니다. 이 API를 다른 용도로 사용하는 것은 Adobe에서 지원하지 않으며, Adobe가 다른 Adobe 고객을 위해 우선순위가 높은 사용자 주도 데이터 개인 정보 보호 요청을 시기적절하게 제공하는 기능에 영향을 줄 수 있습니다. 많은 방문자 그룹에 실수로 제출된 데이터 지우기와 같은 다른 용도로는 Privacy Service API를 사용하지 말아 주십시오.

또한 데이터 개인 정보 보호 삭제 요청으로 인해 히트가 삭제(업데이트 또는 익명 처리)된 방문자의 상태 정보는 재설정된다는 사실을 알고 있어야 합니다. 따라서 다음번에 방문자가 사용자의 웹 사이트로 돌아가면 새 방문자로 간주됩니다. 방문 수, 레퍼러, 방문한 첫 번째 페이지 등의 정보와 마찬가지로 모든 eVar 속성이 다시 시작됩니다. 이 부작용은 데이터 필드를 지우려는 경우 바람직하지 않으며, Privacy Service API가 이 사용에 대해 부적절한 이유 중 하나를 강조 표시합니다.

계정 관리자에게 문의(CSM)하여 PII 또는 데이터 문제를 없애는 데 필요한 노력을 더 자세히 검토하고 제공하도록 Engineering Architect(엔지니어링 설계) 컨설팅팀과 상의하십시오.

