---
description: 검색할 수 있도록 하려는 각 ID에는 네임스페이스가 지정됩니다. 이 네임스페이스는 모든 보고서 세트에서 해당 ID가 사용되는 변수에 있는 각 ID를 식별하는 사용자 지정 문자열입니다.
seo-description: 검색할 수 있도록 하려는 각 ID에는 네임스페이스가 지정됩니다. 이 네임스페이스는 모든 보고서 세트에서 해당 ID가 사용되는 변수에 있는 각 ID를 식별하는 사용자 지정 문자열입니다.
seo-title: 네임스페이스
title: 네임스페이스
uuid: CAB 61844-3209-4980-B 14 C -6859 DE 777606
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 네임스페이스

검색할 수 있도록 하려는 각 ID에는 네임스페이스가 지정됩니다. 이 네임스페이스는 모든 보고서 세트에서 해당 ID가 사용되는 변수에 있는 각 ID를 식별하는 사용자 지정 문자열입니다.

네임스페이스 문자열은 ID를 GDPR 요청의 일부로 제공할 때 검색할 필드를 식별하는 데 사용됩니다. GDPR 요청이 제출되면 이 요청에는 요청에 사용할 데이터 주체 ID를 지정하는 JSON 섹션이 포함됩니다. 여러 개의 ID가 데이터 주체에 대한 단일 요청의 일부로 포함될 수 있습니다. JSON에는 다음이 포함됩니다.

* "namespace" 필드: 네임스페이스 문자열이 들어 있습니다.
* "type" 필드: 대부분의 Adobe Analytics 요청에 대해 "analytics" 값이 들어 있습니다.
* "value" 필드: Analytics가 각 보고서 세트의 연관된 네임스페이스 변수에서 검색해야 하는 ID가 들어 있습니다.

자세한 내용은 [Experience Cloud GDPR API 설명서](https://www.adobe.io/apis/cloudplatform/gdpr/docs/alldocs.html#!api-specification/markdown/narrative/gdpr/use-cases/gdpr-api-overview.md)를 참조하십시오.

<!-- Meike, I converted this table to headings and text to fix a validation error. -Bob -->

## 쿠키 ID

Legacy Analytics Tracking Cookie 또한 Adobe Analytics ID(AAID)로 알려져 있습니다.

```
{
   namespace: "AAID",
   type: "standard",
   value: "2CCEEAE88503384F-1188000089CA"
}
```

값은 대시로 구분된 16진수 두 개로 지정해야 합니다. 영문자로 된 모든 16진수 숫자는 대문자를 사용하여 지정해야 합니다. 16진수 값에 선행하는 0이 없어야 합니다(앞자리에 0이 필수인 더 이상 사용되지 않는 형식에 지정된 동일한 값과의 차이점을 참고하십시오).

It is also acceptable to use `“namespaceId”: 10` instead of or in addition to `“namespace”: “AAID”` and you may see some other Adobe products use that form.

## Legacy Analytics Tracking Cookie: 사용되지 않는 형식

```
{
   "namespace": "visitorId",
   "type": "analytics",
   "value": "2cceeae88503384f-00001188000089ca"
}
```

사용되지 않는 형식:

이 값은 2개의 16자리 16진수 또는 2개의 19자리 십진수로 지정해야 합니다. 숫자는 대시, 밑줄 또는 콜론으로 구분해야 합니다. 숫자에 충분한 자리가 없는 경우 앞에 0을 추가해야 합니다.

## ID 서비스 쿠키

```
{
    namespace: "ECID",
    type: "standard",
    value: "00497781304058976192356650736267671594"
}
```

값은 38자리 10진수로 지정해야 합니다. 데이터 피드나 데이터 웨어하우스 보고서에서 두 개의 mcvisid\_ high/low 또는 post\_ msvisid\_ high/low 열에서 이 숫자를 가져오는 경우, 두 숫자 각각에 대해 19 자리 숫자로 구성된 패드를 만든 후 높은 값으로 먼저 연결해야 합니다.

It is also acceptable to use: `“namespaceId”: 4` instead of or in addition to `“namespace”: “ECID”` and you may see some other Adobe products use that form.

>[!NOTE]
>
>Experience Cloud ID (ECID) 는 이전에 MCID (Marketing Cloud ID) 로 알려져 있으며, 일부 기존 문서에서 해당 이름으로 여전히 언급됩니다.
>
>이러한 ID는 "analytics" 이외의 "type" 값을 사용하는 Analytics에서 지원하는 유일한 ID 입니다.

이러한 쿠키 ID의 값 부분 형식이 해당 ID에 대해 설명된 형식을 따르지 않는 경우, GDPR 요청은 실패하고 "값이 올바르게 형식화되지 않음" 오류가 발생합니다.

가장 일반적으로는 이러한 JSON ID에 관련 키/값 쌍을 모두 자동으로 제공하는 새 [개인 정보 JavaScript](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm)를 사용하여 이러한 쿠키 ID를 수집합니다.

이 JavaScript 코드는 위에 나열된 키/값 쌍(네임스페이스, 유형, 값) 외에도 다른 키/값 쌍으로 JSON을 채우지만, 위에 나열된 필드가 Analytics GDPR 처리에 가장 중요하며 일부 다른 방식으로 ID를 수집하는 경우 제공해야 하는 유일한 필드입니다.

## 사용자 지정 방문자 ID

```
{
     namespace: "customVisitorID",
     type: "analytics",
     value: "<ID>"
}
```

네임스페이스도 사용자 지정 방문자 ID에 대해 사전 정의되어 있습니다.

## 사용자 지정 변수의 ID

```
{
    namespace: "Email Address",
    type: "analytics", 
    value: "john@xyz.com" }, 
{
    namespace: "CRM ID", 
    type: "analytics", 
    value: "123456-ABCD" 
}
```

사용자 지정 트래픽 또는 전환 변수(props 또는 eVars)의 ID에 대해서는 해당 변수에 ID-DEVICE 또는 ID-PERSON 레이블을 지정한 다음 해당 유형의 ID에 고유한 네임스페이스 이름을 지정해야 합니다. [변수에 ID-DEVICE 또는 ID-PERSON으로 레이블을 지정할 때 네임스페이스 제공](../../admin/c-data-governance/gdpr-labels.md#section_F0A47AF8DA384A26BD56032D0ABFD2D7)을 참조하십시오.

이전에 다른 변수 또는 보고서 세트에 대해 정의한 네임스페이스를 보고 그러한 네임스페이스 중 하나를 재사용할 수도 있으므로, 해당 유형의 ID를 저장하는 모든 보고서 세트에 동일한 네임스페이스를 쉽게 사용할 수 있습니다. 또한 동일한 네임스페이스를 보고서 세트 내에 있는 여러 변수에 지정할 수 있습니다. 예를 들어 일부 고객이 트래픽 변수와 전환 변수에 CRM ID를 저장하고(페이지에 따라 트래픽 변수 또는 전환 변수 또는 둘 다에 있음), 네임스페이스 "CRM ID"를 두 변수에 모두 지정할 수 있습니다.

>[!NOTE]
>
>이 변수에 id-device 또는 id-person 레이블을 적용할 때 지정한 네임스페이스가 아니라면 변수 (보고 UI에 표시된 이름) 또는 변수 번호 (evar 12와 같이) 의 친숙한 이름을 GDPR API에 지정할 수 없습니다. 친숙한 이름 대신 네임스페이스를 사용하면 다음과 같은 경우 동일한 사용자 ID 블록에서 여러 보고서 세트에 대해 올바른 변수를 지정할 수 있습니다.

* ID가 일부 보고서 세트의 서로 다른 eVars에 있는 경우, 또는
* 친숙한 이름이 일치하지 않는 경우(예: 친숙한 이름이 특정 보고서 세트에 대해 현지화된 경우)

자세한 내용은 [변수에 ID-DEVICE 또는 ID-PERSON으로 레이블을 지정할 때 네임스페이스 제공](../../admin/c-data-governance/gdpr-labels.md#section_F0A47AF8DA384A26BD56032D0ABFD2D7)을 참조하십시오.
