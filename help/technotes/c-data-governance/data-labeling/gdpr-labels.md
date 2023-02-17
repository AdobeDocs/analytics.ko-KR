---
description: Adobe Analytics 변수에 대한 데이터 개인정보 레이블의 예
title: Analytics 변수의 데이터 개인정보 보호 레이블
feature: Data Governance
exl-id: b8c2143a-6e8e-465a-979b-aa8176e8d4e8
source-git-commit: 1ca7040156f7f2105a9625f921de3d90b4175056
workflow-type: tm+mt
source-wordcount: '3585'
ht-degree: 80%

---

# Analytics 변수의 데이터 개인정보 보호 레이블

## 데이터에 레이블을 지정하는 이유 {#why-label}

Adobe 고객은 데이터 통제자로서 GDPR 및 CCPA와 같은 해당 데이터 개인 정보 보호 법을 준수할 책임이 있습니다. 고객은 자신의 법률 팀과 협력하여 데이터 개인 정보 보호 법을 준수하도록 데이터를 처리하는 방법을 결정해야 합니다. Adobe은 각 고객이 개인 정보 보호와 관련된 고유한 요구 사항을 알고 있으며, 이러한 이유로 Adobe은 고객이 데이터 개인 정보 보호 데이터 처리에 대해 원하는 설정을 사용자 지정할 수 있도록 합니다. 그러면 각 고유 고객이 자신의 브랜드 및 고유 데이터 세트에 가장 적합한 방식으로 데이터 개인정보 보호 요청을 처리할 수 있습니다.

Adobe Analytics는 그 민감도 및 계약 제한 사항에 따라 데이터를 라벨링하는 도구를 제공합니다. 레이블은 다음과 같은 중요한 단계입니다. (1) 데이터 주체 식별, 액세스 요청의 일부로 반환할 데이터 결정 및 삭제 요청의 일부로 삭제되어야 하는 데이터 필드를 식별하는 (2)

어떤 변수/필드에 어떤 레이블을 적용해야 하는지 파악하려면 먼저 Analytics 데이터에서 캡처 중인 [ID를 파악하고](/help/technotes/c-data-governance/data-labeling/gdpr-analytics-ids.md) 데이터 개인정보 보호 요청에 사용할 ID를 결정해야 합니다.

Adobe Analytics 데이터 개인정보 보호 구현은 ID 데이터, 중요 데이터 및 데이터 거버넌스에 대해 다음 레이블을 지원합니다.

## ID 데이터 레이블 {#identity-data-labels}

ID 데이터의 “I” 레이블은 특정 개인을 식별하거나 특정 개인에게 연락할 수 있는 데이터를 범주화하는 데 사용됩니다.

| 레이블 | 정의 | 기타 요구 사항 |
| --- | --- | --- |
| I1 | 직접 식별 가능: 이름 또는 이메일 주소처럼 개인을 식별할 수 있거나 개인과 직접 연락할 수 있는 데이터입니다. | <ul><li>이벤트에 대해 설정할 수 없음</li><li>머천다이징 eVars에 대해 설정할 수 없음</li></ul> |
| I2 | 간접 식별 가능: 다른 데이터와의 조합에 사용하여 개인 또는 디바이스를 식별하거나 개인 또는 디바이스와 직접 연결할 수 있는 데이터입니다.  개인을 자체적으로 식별할 수는 없지만 다른 정보 (소유하고 있거나 소유하고 있지 않은 정보)와 결합하여 누군가를 식별할 수 있습니다. 예를 들어 고객 충성도 번호 또는 회사의 CRM 시스템에서 사용되며 각 고객에 대해 고유한 ID가 있습니다. | <ul><li>이벤트에 대해 설정할 수 없음</li><li>머천다이징 eVars에 대해 설정할 수 없음</li></ul> |

{style=&quot;table-layout:auto&quot;}

## 중요 데이터 레이블 {#sensitive-data-labels}

중요 데이터 &quot;S&quot; 레이블은 지리 데이터와 같은 중요 데이터를 범주화하는 데 사용됩니다. 추가적인 중요 데이터 레이블은 다른 유형의 중요 정보를 식별하기 위해 나중에 도입됩니다.

| 레이블 | 정의 |
| --- | --- |
| S1 | 디바이스의 정확한 위치를 판별하는 데 사용할 수 있는 위도 및 경도와 관련된 정확한 지리적 위치 데이터입니다(100m 이내). |
| S2 | 광범위하게 정의된 가상 울타리 영역을 판단하는 데 사용할 수 있는 지리적 위치 데이터입니다. |

{style=&quot;table-layout:auto&quot;}

## 데이터 거버넌스 레이블 (데이터 개인정보 보호) {#data-governance-labels}

데이터 거버넌스 레이블은 Adobe 고객이 규정 및 기업 정책을 계속 준수하도록 지원하기 위해 개인 정보 보호 관련 고려 사항 및 계약 조건을 반영하여 데이터를 분류하는 기능을 제공합니다.

### 데이터 개인정보 보호 액세스 레이블

| 레이블 | 정의 | 기타 요구 사항 |
| --- | --- | --- |
| 없음 | 이 변수에 데이터 개인 정보 보호 액세스 요청의 일부로 데이터 주체에게 반환되는 데이터에 포함해야 하는 데이터가 포함되지 않은 경우 이 옵션을 선택합니다. |  |
| ACC-ALL | 이 필드의 값은 모든 데이터 개인정보 보호 액세스 요청에 포함해야 합니다. 이 히트가 여러 개인이 공유한 디바이스에서 발생한 경우, 이 레이블을 적용하면 사용자가 데이터 컨트롤러로서 공유된 디바이스에 액세스한 개별 사용자와 이 필드의 데이터를 공유하는 것을 허용한다는 것을 나타냅니다. | 모든 데이터 개인정보 보호 요청에 대해 이 레이블이 있는 필드가 반환됩니다. |
| ACC-PERSON | 이 필드의 값은 ID-PERSON 필드의 값과 일치하는 데이터 개인 정보 보호 요청 ID에 의해 결정된 대로 데이터 주체에서 히트가 결정된다고 합리적으로 추정되는 경우 데이터 개인 정보 보호 액세스 요청용으로만 포함되어야 합니다. | 이 보고서 세트 내의 일부 변수에 ID-PERSON 레이블이 설정되어 있어야 하며 해당 ID를 사용하여 요청을 제출해야 합니다. 그렇지 않으면 이 레이블이 적용되지 않습니다. |

{style=&quot;table-layout:auto&quot;}

다른 레이블을 수신하는 변수는 거의 없는 반면 액세스 레이블은 많은 변수에 적용될 것입니다. 그러나 수집한 데이터를 데이터 주체와 공유해야 하는 것은 법무 팀과 협의하여 귀하의 책임입니다.

### 데이터 개인정보 보호 삭제 레이블

이러한 삭제 레이블은 다른 레이블과 달리 함께 사용할 수 있습니다. 둘 중 하나 또는 둘 다 선택하거나 아무것도 선택하지 않을 수 있습니다. [!UICONTROL 없음] 레이블은 삭제 옵션 중 하나를 선택하지 않음으로써 간단하게 [!UICONTROL 없음]이 표시되므로 별도로 필요하지 않습니다.

삭제 레이블은 히트가 데이터 주체와 연관될 수 있도록 하는 값(즉, 데이터 주체를 식별할 수 있는 값)이 포함된 필드에만 필요합니다. 기타 개인 정보(즐겨찾기, 탐색/구입 내역, 건강 상태 등)는 데이터 주체와의 연결이 끊기므로 을 삭제할 필요가 없습니다.

| 레이블 | 정의 | 기타 요구 사항 |
| --- | --- | --- |
| DEL-DEVICE | 데이터 개인정보 보호 삭제 요청의 경우, 이 필드의 값은 지정된 ID-DEVICE가 히트에 있는 요청에 대해서만 익명 처리되어야 합니다.  삭제되지 않는 다른 히트에서 동일한 값이 발생하면 해당 다른 인스턴스는 변경되지 않습니다. 이 경우 이 필드에서 고유 카운트를 계산하는 보고서의 카운트가 변경됩니다. 공유 장치에서 데이터 주체 외에 다른 개인의 식별자를 제거할 수 있습니다.  이 필드에 ID-DEVICE 레이블이 있고 이 필드의 값이 데이터 개인정보 보호 요청에 대한 ID로 사용된 경우에는 카운트가 변경되지 않습니다. | <ul><li>I1 또는 I2 또는 S1 레이블도 필요함</li><li>이벤트에 대해 설정할 수 없음</li><li>머천다이징 eVars에 대해 설정할 수 없음</li></li><li>분류에 대해 설정할 수 없음</li><li>ID-DEVICE를 사용하여 요청을 제출하거나 expandIDs를 true로 설정해야 합니다. 그렇지 않으면 이 레이블이 적용되지 않습니다.</li></ul> |
| DEL-PERSON | 데이터 개인정보 보호 삭제 요청의 경우, 이 필드의 값은 지정된 ID-PERSON이 히트에 있는 요청에 대해서만 익명 처리되어야 합니다.  삭제되지 않는 다른 히트에서 동일한 값이 발생하는 경우 다른 값은 변경되지 않습니다. 이렇게 하면 이 필드에서 고유한 카운트를 계산하는 보고서에 대한 카운트가 변경됩니다. 이 필드에 ID-PERSON 레이블이 있고 이 필드의 값이 데이터 개인정보 보호 요청에 대한 ID로 사용된 경우에는 카운트가 변경되지 않습니다. | <ul><li>I1 또는 I2 또는 S1 레이블도 필요함</li><li>이벤트에 대해 설정할 수 없음</li><li>머천다이징 eVars에 대해 설정할 수 없음</li></li><li>분류에 대해 설정할 수 없음</li><li>이 보고서 세트 내의 일부 변수에 대해 ID-PERSON 레이블 세트를 사용하여 요청을 제출하고 해당 ID를 사용하여 요청을 제출해야 합니다. 그렇지 않으면 이 레이블이 적용되지 않습니다.</li></ul> |

{style=&quot;table-layout:auto&quot;}

### 데이터 개인정보 보호 ID 레이블

| 레이블 | 정의 | 기타 요구 사항 |
| --- | --- | --- |
| 없음 | 이 변수는 데이터 개인정보 보호 요청에 사용될 ID를 포함하지 않습니다. | 이 필드에 [Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=ko-KR) 또는 UI를 통해 액세스 또는 삭제 요청을 제출할 때 사용할 ID가 포함된 경우에만 이러한 다른 레이블 중 하나를 설정해야 합니다. |
| ID-DEVICE | 이 필드에는 데이터 개인정보 보호 요청에 대해 디바이스를 식별하는 데 사용할 수 있는 ID가 포함되어 있지만 공유 디바이스의 서로 다른 사용자를 구별할 수 없습니다.  ID (I1/I2 레이블의 용도)가 포함된 모든 변수에 이 레이블을 지정할 필요는 없습니다. 이 변수에 저장된 ID를 사용하여 데이터 개인정보 보호 요청을 제출하고 이 변수에서 지정된 ID를 검색하려는 경우 이 레이블을 사용합니다. | I1 또는 I2 레이블도 필요함.<ul><li>이벤트에 대해 설정할 수 없음</li><li>머천다이징 eVars에 대해 설정할 수 없음</li><li>분류에 대해 설정할 수 없음</li></ul> |
| ID-PERSON | 이 필드에는 데이터 개인정보 보호 요청에 대해 인증된 사용자 (특정 사용자)를 식별하는 데 사용할 수 있는 ID가 포함됩니다.  ID (I1/I2 레이블의 용도)가 포함된 모든 변수에 이 레이블을 지정할 필요는 없습니다. 이 변수에 저장된 ID를 사용하여 데이터 개인정보 보호 요청을 제출하고 이 변수에서 지정된 ID를 검색하려는 경우 이 레이블을 사용합니다. | <ul><li>I1 또는 I2 레이블도 필요함.</li><li>이벤트에 대해 설정할 수 없음</li><li>머천다이징 eVars에 대해 설정할 수 없음</li><li>분류에 대해 설정할 수 없음</li></ul> |

{style=&quot;table-layout:auto&quot;}

## 변수에 ID-DEVICE 또는 ID-PERSON으로 레이블을 지정할 때 네임스페이스 제공 {#provide-namespace}

변수에 ID-DEVICE 또는 ID-PERSON으로 레이블을 지정할 때 네임스페이스를 제공하라는 메시지가 표시됩니다. 이전에 정의된 네임스페이스를 사용하거나 새 네임스페이스를 정의할 수 있습니다.

### 이전에 정의한 네임스페이스 사용

로그인 회사의 모든 보고서 세트에 있는 다른 변수에 ID 레이블을 이전에 할당한 경우 이러한 기존 네임스페이스 중 하나를 선택할 수 있습니다. 이 변수에 이 네임스페이스로 이미 레이블이 지정된 다른 변수와 동일한 유형의 ID가 포함되어 있고 요청을 제출할 때 이 변수를 모두 검색하려면 네임스페이스를 다시 사용해야 합니다.

1. **[!UICONTROL 네임스페이스 선택]**&#x200B;을 클릭하고 기존 네임스페이스 중 하나를 선택합니다.
1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

![](assets/namespace.png)

### 새 네임스페이스 정의

새 네임스페이스를 정의할 수도 있습니다. 네임스페이스 문자열을 영숫자와 밑줄, 대시 및 공백으로 제한하는 것이 좋습니다. 이 문자열은 소문자로 변환됩니다.

1. **[!UICONTROL 네임스페이스 선택]**&#x200B;을 클릭하고 네임스페이스 제목을 입력합니다.

   ![](assets/namespace2.png)

1. **[!UICONTROL Enter]** 키를 눌러 이 네임스페이스를 추가합니다. 현재는 적용 버튼만 활성화됩니다.
1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

네임스페이스로 지정하는 문자열은 데이터 개인정보 보호 API를 통해 요청을 &quot;네임스페이스&quot; 매개변수 값으로 제출할 때 사용해야 하는 것과 동일한 문자열입니다. 그러면 요청이 발생하면 Adobe Analytics이 이 네임스페이스를 공유하는 모든 보고서 세트에서 요청과 함께 지정한 ID에 대한 모든 변수를 검색하게 됩니다.

ID (I1/I2 레이블의 용도)가 포함된 모든 변수에 ID-DEVICE 또는 ID-PERSON 레이블을 지정할 필요는 없습니다. 이 변수에 저장된 ID를 사용하여 데이터 개인정보 보호 요청을 제출하고 이 변수에서 지정된 ID를 검색하려는 경우 이 레이블을 사용합니다. 예를 들어 eVar1에 이메일 주소를 포함할 수 있고 eVar2에 로그인 사용자 이름을 포함할 수 있지만 사용자 이름만 사용하여 요청을 제출하는 경우 eVar1을 I1, ACC-PERSON, DEL-PERSON으로 레이블 지정할 수 있지만 eVar2는 &quot;user name&quot; 네임스페이스와 함께 I2, ACC-PERSON, DEL-PERSON, ID-PERSON으로 레이블 지정할 수 있습니다. 다음과 같은 사용자 섹션 JSON 블록과 함께 요청을 제출할 수 있습니다.

```
{
     "namespace": "user name",
     "type": "analytics",
     "value": "rocketman123"
}
```

동일한 보고서 세트 내의 다른 변수에 동일한 네임스페이스를 사용할 수 있습니다. 예를 들어 일부 사용자 정의 구현은 prop 및 eVar에 모두 CRM-ID를 저장합니다. CRM-ID가 항상 하나의(예: eVar)에서 발생하고, 다른 속성(prop)에서만 가끔 발생하고, eVar에도 없을 때 prop에서는 발생하지 않는 경우 Adobe은 해당 eVar에서만 ID를 검색할 수 있으므로 eVar은 ID 레이블과 네임스페이스가 필요하므로 됩니다. 그러나 CRM-ID가 한 변수에서 가끔 발생하고 다른 변수에서도 가끔 발생하면 두 변수 모두 동일한 네임스페이스를 가져야 하며, Adobe에서는 두 변수에서 이 네임스페이스와 함께 데이터 개인정보 보호 요청의 일부로 지정된 ID의 발생을 검색합니다. 이러한 모든 변수에는 DEL 레이블이 있어야 하므로 값이 어디에서 발생하더라도 익명이 아닙니다.

다른 예로는 가끔 eVar1을 통해 전송되는 CRM ID와 가끔 prop7을 통해 전송되는 CRM ID가 있을 수 있습니다. 그런 경우 eVar1의 값 (있는 경우)을 eVar3에 복사하는 처리 규칙이 있습니다. 그렇지 않으면 prop7의 값을 eVar 3으로 복사합니다. 이 시나리오에서는 eVar3에 항상 CRM ID가 포함되므로 eVar3에만 ID-PERSON 레이블이 필요합니다.

>[!CAUTION]
>
>네임스페이스 &quot;visitorId&quot;와 &quot;customVisitorId&quot;는 Analytics 이전 추적 쿠키와 Analytics 고객 방문자 ID를 식별하기 위해 예약되어 있습니다. 사용자 정의 트래픽 또는 전환 변수에 이러한 네임스페이스를 사용하지 마십시오.

## 변수 유형 및 변수 유형이 지원하는 데이터 개인정보 보호 레이블 {#variable-types}

데이터 개인정보 보호 레이블을 지정하면 Analytics 변수의 네 가지 광범위한 클래스에 영향을 줍니다. 모든 변수가 모든 레이블을 지원하는 것은 아닙니다. 이 표는 어떤 레이블을 지원하거나 지원하지 않는 변수를 보여줍니다.

| 변수 유형 | 지원되는 레이블 | 지원되지 않는 레이블 |
|--- |--- |--- |
| <ul><li>사용자 정의 성공 이벤트</li><li>머천다이징 eVars</li><li>다중 값 변수 (mvVars)</li><li>계층 변수</li></ul> | <ul><li>S1/S2</li><li>ACC-ALL, ACC-PERSON</li></ul> | <ul><li>I1/I2</li>  <li>ID-DEVICE, ID-PERSON</li><li>DEL-DEVICE, DEL-PERSON</li></ul> |
| 분류 | <ul><li>I1/I2, S1/S2</li><li>ACC-ALL, ACC-PERSON</li></ul> | <ul><li>ID-DEVICE, ID-PERSON</li><li>DEL-DEVICE, DEL-PERSON</li></ul> |
| <ul><li>트래픽 변수 (Prop)</li><li>상거래 변수 (비머천다이징 eVar)</li></ul> | 모든 레이블 | - |
| 대부분의 다른 변수  (*예외 사항은 아래 표 참조*) | ACC-ALL, ACC-PERSON | <ul><li>I1/I2, S1/S2</li><li>ID-DEVICE, ID-PERSON</li><li>DEL-DEVICE, DEL-PERSON)</li></ul> |

{style=&quot;table-layout:auto&quot;}

## ACC-ALL/ACC-PERSON 이외의 레이블을 지정/수정할 수 있는 변수 {#variables}

<table id="table_0972910DB2D7473588F23EA47988381D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 그룹 </th> 
   <th colname="col2" class="entry"> 변수 </th> 
   <th colname="col3" class="entry"> 수정 가능한 레이블 </th> 
   <th colname="col4" class="entry"> 댓글 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_62FA1BAA3B9245909509566D8C03F900"> 
     <li id="li_38F7C4E18ECB42C292370713F502B8EB">전환 차원 </li> 
     <li id="li_41CB61F927CB4402AAB4A62E219CD153">사용자 정의 트래픽 차원 </li> 
    </ul> </td> 
   <td colname="col2"> <p>분류를 제외한 모든 변수 </p> </td> 
   <td colname="col3"> <p>모두 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>분류 </p> </td> 
   <td colname="col3"> <p>없음/I1/I2 </p> <p>없음/S1/S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>전환 이벤트 </p> </td> 
   <td colname="col2"> <p>모두 </p> </td> 
   <td colname="col3"> <p>없음/S1/S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>솔루션 차원 및 이벤트 </p> </td> 
   <td colname="col2"> <p>Activity Map 링크, </p> <p>Activity Map 페이지 </p> </td> 
   <td colname="col3"> <p>없음/I1/I2 </p> <p>없음/DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>변수에는 직접 또는 간접적으로 식별 가능한 데이터가 포함될 수 있는 URL 매개변수가 포함될 수 있습니다. 구현에서 이러한 변수에 있는 직접 또는 간접적으로 식별 가능한 데이터를 수집하지 않는 경우 ID 또는 삭제 레이블이 필요하지 않습니다. </p> <p>삭제하면 URL 매개변수가 지워지지만 기본 URL은 그대로 유지됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 처리 차원 </p> </td> 
   <td colname="col2"> <p>사용자 정의 방문자 ID </p> </td> 
   <td colname="col3"> <p>ID-DEVICE/ID-PERSON </p> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>ID 또는 DEL 레이블 (없음으로 설정됨)을 제거할 수 없지만 사용자 정의 ID 구현에 따라 DEVICE 또는 PERSON 변형으로 변경할 수 있습니다. </p> <p>사용자 지정 방문자 ID를 사용하지 않는 경우에는 설정이 중요하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_5EB0193732D44A20AEA08CE9DFE01DBD"> 
     <li id="li_F70D969F83314A94BD8567449968EE2F">표준 차원 </li> 
     <li id="li_6046764B19FF4679B51E55671C2C0ADB">데이터 처리 차원 </li> 
    </ul> </td> 
   <td colname="col2"> <p>IP 주소 </p> <p>IP 주소 2 </p> </td> 
   <td colname="col3"> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>DEL 레이블은 제거할 수 없지만 DEL-DEVICE 또는 DEL-PERSON 또는 둘 다로 변경할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>ClickMap 작업 (기존) </p> <p>ClickMap 컨텍스트 (기존) </p> <p>페이지, </p> <p>페이지 URL, </p> <p>원래 시작 페이지 URL, </p> <p>레퍼러, </p> <p>시작 페이지 URL 방문 </p> </td> 
   <td colname="col3"> <p>없음/I1/I2 </p> <p>없음/DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>변수에는 직접 또는 간접적으로 식별 가능한 데이터가 포함될 수 있는 URL 매개변수가 포함될 수 있습니다. 구현에서 이러한 변수에 있는 직접 또는 간접적으로 식별 가능한 데이터를 수집하지 않는 경우 ID 또는 삭제 레이블이 필요하지 않습니다. </p> <p>삭제하면 URL 매개변수가 지워지지만 기본 URL은 그대로 유지됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 삭제 처리 {#deletion}

데이터 개인정보 보호 삭제 요청에 대한 Adobe Analytics 지원은 보고에 미치는 영향을 최소화하도록 설계되었습니다. 대부분의 경우 보고서에 표시된 지표는 변경되지 않아야 합니다. 데이터 개인정보 보호 삭제 전에 실행된 기록 보고서는 삭제가 수행된 후 실행된 동일한 보고서와 일치합니다. 이 작업은 보고된 값이 일관되게 유지될 수 있도록 식별할 수 없는 데이터를 그대로 두면서 데이터 주체에서 삭제된 데이터를 완전히 분리하여 수행됩니다.

다음 표는 다양한 변수가 &quot;삭제&quot;되는 방법을 설명합니다. 이는 완전한 목록이 아닙니다.

| 변수 | 삭제 방법 |
| --- | --- |
| <ul><li>트래픽 변수 (Prop)</li><li>상거래 변수 (eVar)</li></ul> | 기존 값은 “데이터 개인정보 보호-356396D55C4F9C7AB3FBB2F2FA223482” 형식의 새 값으로 대체됩니다. 여기서 “개인정보 보호-” 접두사 다음의 32자리 16진수 값은 암호학적으로 강력한 128비트 의사 난수입니다.<p>기본적으로 임의의 문자열로 대체되기 때문에 이 새 값에서 원래 값을 결정할 방법이 없으며 원래 값을 판별하는 새 값을 도출하는 방법이 없습니다.  지정된 변수의 경우, 대체되는 값과 동일한 값이 동일한 데이터 개인정보 보호 요청의 일부로 삭제되는 다른 히트 내에 있으면 해당 값의 모든 인스턴스가 동일한 새 값으로 대체됩니다.<p>값의 일부 인스턴스가 하나의 삭제 요청으로 대체되고 이후 요청이 원래 값의 다른 (새) 인스턴스를 삭제하는 경우 새 대체 값은 원래 대체 값과 달라집니다. |
| 구매 ID | 기존 값은 &quot;G-7588FCD8642718EC50&quot; 형식의 새 값으로 대체됩니다. 여기서 &quot;G-&quot; 접두사 다음의 18자리 16진수는 암호학적으로 강력한 128비트 의사 난수의 처음 18자리입니다. 트래픽 및 상거래 변수의 삭제에 적용되는 모든 댓글도 여기에 적용됩니다.<p>구매 ID는 트랜잭션 ID로, 누군가가 구매 확인 페이지를 새로 고침하는 경우와 같이 구매가 두 번 결제되지 않도록 하는 것이 주 목적입니다. ID 자체는 구매가 기록된 자신의 DB 행에 구매를 연결할 수 있습니다. 대부분의 경우 이 ID를 삭제할 필요가 없으므로 기본적으로 삭제되지 않습니다.<p>사용자 고유의 데이터에 대한 데이터 개인정보 보호 삭제 요청 후에도 구매를 다시 사용자에게 연결할 수 있는 경우 이 방문자의 Analytics 데이터를 구매자에게 다시 연결할 수 없도록 이 필드를 삭제해야 할 수 있습니다. |
| 방문자 ID | 값은 128비트 정수이며 암호화적으로 강력한 128비트 의사 난수 값으로 대체됩니다. |
| <ul><li>MCID</li><li>사용자 정의 방문자 ID</li><li>IP 주소</li><li>IP 주소 2 | 값이 지워졌습니다 (변수 유형에 따라 빈 문자열 또는 0으로 설정). |
| <ul><li>ClickMap 작업 (기존)</li><li>ClickMap 컨텍스트 (기존)</li><li>페이지</li><li>페이지 URL</li><li>원래 시작 페이지 URL</li><li>레퍼러</li><li>시작 페이지 URL 방문</li></ul> | URL 매개변수는 삭제/제거됩니다. 값이 URL과 유사하지 않으면 값은 지워집니다 (빈 문자열로 설정됨). |
| <ul><li>위도</li><li>경도</li></ul> | 정밀도는 1km 정도로 감소합니다. |

{style=&quot;table-layout:auto&quot;}

## 예상 삭제 레이블을 지원하지 않을 수 있는 변수 {#no-delete-support}

이 섹션은 삭제를 지원하지 않을 수 있는 Analytics 변수에 대한 정보를 명확하게 확인하기 위한 것입니다. 간혹 변수에 포함된 데이터 유형을 이해하지 못하고 변수 이름을 기반으로 가정을 하는 비 Analytics 사용자(예: 법률 팀)가 이러한 변수를 삭제하는 경우가 있습니다.

레이블 지정 또는 삭제를 결정하기 전에 각 변수에 포함된 데이터 유형을 이해하고 변수 이름만 의존하지 않는 것이 중요합니다. 다음은 이러한 변수 중 일부 목록이며 삭제가 필요하지 않은 이유 또는 특정 삭제 레이블이 필요하지 않은 이유입니다.

| 변수 | 댓글 |
| --- | --- |
| [!UICONTROL 새 방문자 ID] | 새 방문자 ID는 주어진 방문자 ID를 처음 볼 때 true인 부울입니다. 방문자 ID가 익명 처리되면 삭제할 필요가 없습니다. 익명 처리 후에는 이 익명 ID를 처음 표시된 순간과 일치하게 됩니다. |
| [!UICONTROL 우편번호]<p>[!UICONTROL 지역 우편번호] | 우편번호는 미국에서 시작되는 히트에 대해서만 설정됩니다. EU에서 발생한 히트에 대해서는 설정되지 않습니다. 설정되더라도 데이터 주체를 다시 식별하기 어렵게 하는 광범위한 지리적 영역만 제공합니다. |
| [!UICONTROL 지역 위도]<p>[!UICONTROL 지역 경도] | 이는 IP 주소에서 파생된 대략적인 위치를 제공합니다. 정확성은 일반적으로 실제 위치의 수십 킬로미터 내에 있는 우편번호 정확성과 비슷합니다. |
| [!UICONTROL 사용자 에이전트] | 사용자 에이전트는 사용된 브라우저의 버전을 식별합니다. |
| [!UICONTROL 사용자 ID] | 데이터를 포함하는 Analytics 보고서 세트를 (숫자로) 지정합니다. |
| [!UICONTROL 보고서 세트 ID] | 데이터를 포함하는 Analytics 보고서 세트의 이름을 지정합니다. |
| [!UICONTROL 방문자 ID]<p>[!UICONTROL MCID] / [!UICONTROL ECID] | 이러한 ID에는 DEL-DEVICE 레이블이 있지만 DEL-PERSON 레이블을 추가할 수 없습니다. 각 요청에 [!UICONTROL ID 확장]을 지정하는 경우 ID-PERSON을 사용하는 모든 삭제 요청에 대해 이러한 ID가 자동으로 삭제됩니다.<p>ID 확장을 사용하지 않고 이러한 쿠키 ID가 Prop 또는 eVar에 일치하는 ID가 포함된 히트에 익명으로 표시되도록 하려면 실제로 사람을 식별하는 경우에도 Prop 또는 eVar에 ID-DEVICE 레이블을 지정하여 이 라벨링 제한을 해결할 수 있습니다 (모든 DEL-PERSON 레이블도 DEL-DEVICE 레이블로 변경해야 함). 이 경우 방문자 ID 또는 ECID의 일부 인스턴스만 익명으로 처리되므로 고유 방문자 수가 기록 보고에서 변경됩니다. |
| [!UICONTROL AMO ID] | Adobe Advertising Cloud ID는 수정할 수 없는 [!UICONTROL DEL-DEVICE] 레이블이 있는 솔루션 변수입니다. 방문자 ID 및 MCID와 마찬가지로 쿠키에서 채워집니다. 다른 ID가 삭제될 때마다 히트에서 삭제해야 합니다. 자세한 내용은 해당 변수에 대한 설명을 참조하십시오. |

{style=&quot;table-layout:auto&quot;}

## 액세스 요청에 대한 날짜 필드 {#access-requests}

타임스탬프를 포함하는 다음과 같은 5개의 표준 변수가 있습니다.

| 타임스탬프 | 정의 |
| --- | --- |
| Hit Time UTC | Adobe Analytics가 히트를 받는 시간입니다. |
| Custom Hit Time UTC | 일부 모바일 애플리케이션 및 기타 구현에서 발생한 히트가 수신된 시간보다 이전일 수 있습니다. 예를 들어 히트가 수신되었을 때 네트워크 연결을 사용할 수 없는 경우에는 애플리케이션이 히트를 보유하고 연결을 사용할 수 있게 되면 해당 히트를 보낼 수 있습니다. |
| Date Time | Custom Hit Time UTC와 동일한 값이지만 GMT가 아닌 보고서 제품군의 시간대에 있습니다. |
| First Hit Time GMT | 첫 번째 히트의 Custom Hit Time UTC 값은 이 히트의 방문자 ID 값에 대해 수신된 첫 번째 히트입니다. |
| Visit Start Time UTC | 첫 번째 히트의 Custom Hit Time UTC 값은 이 방문자 ID의 현재 방문에 대해 수신된 첫 번째 히트입니다. |

{style=&quot;table-layout:auto&quot;}

데이터 개인정보 보호 액세스 요청에 대해 반환되는 파일을 생성하는 코드는 처음 세 개의 타임스탬프 변수 중 하나 이상이 액세스 요청에 포함되어야 합니다 (요청 유형에 적용되는 ACC 레이블 있음). 이러한 항목이 포함되지 않은 경우 Custom Hit Time UTC는 ACC-ALL 레이블이 있는 것처럼 처리됩니다.

데이터 개인정보 보호 액세스 요청에 대해 반환된 히트 레벨 CSV 파일은 unix 타임스탬프에서 이러한 필드의 값을 YYYY-MM-DD HH:MM:SS 형식의 날짜/시간 필드로 변환합니다(예: 2018-05-01 13:49:22). 요약 HTML 파일에서 이러한 타임스탬프 값은 이러한 필드에 대해 발생하는 고유한 값의 수를 줄이기 위해 날짜 YYYY-MM-DD만 포함하도록 잘립니다.