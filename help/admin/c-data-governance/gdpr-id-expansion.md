---
description: 제출하는 ID가 Analytics에서 데이터 주체와 연결할 수 있는 모든 히트 데이터를 항상 포함하는 것은 아닙니다. Analytics에서는 연결된 데이터를 데이터 개인정보 보호 요청에 포함하도록 확장된 ID 세트를 만들 수 있습니다. 제출한 각 데이터 개인정보 보호 요청에 대해 선택적 매개변수와 함께 이 옵션을 요청하여 JSON 요청에 추가할 수 있습니다.
title: ID 확장
feature: Data Governance
exl-id: 312a249f-e0e7-44da-bb3d-b19f1bb4c706
source-git-commit: e9fffe62d3e53ae075610b1feec9a9071d925433
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ID 확장

제출하는 ID가 Analytics에서 데이터 주체와 연결할 수 있는 모든 히트 데이터를 항상 포함하는 것은 아닙니다. Analytics에서는 연결된 데이터를 데이터 개인정보 보호 요청에 포함하도록 확장된 ID 세트를 만들 수 있습니다. 제출한 각 데이터 개인정보 보호 요청에 대해 선택적 매개변수와 함께 이 옵션을 요청하여 JSON 요청에 추가할 수 있습니다.

```
"expandIds": true
```

자세한 내용은 [개인정보 보호 서비스 API 문서](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html)를 참조하십시오.


| 유형 | 고려 사항 |
| --- | --- |
| 쿠키 ID 확장 | 원래 (이전)을 사용한 많은 Analytics 고객 [Analytics 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-privacy.html?lang=en)하지만 이제 [ECID(Experience Cloud Identity Service)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko-KR). 전환 후 처음 방문한 해당 웹 사이트 방문자의 경우 ECID만 존재합니다. 그러나 기존 쿠키만 사용할 수 있을 때 처음 방문한 후 방문한 다음 이후 방문한 사용자의 경우: 일부 데이터에 두 개의 쿠키가 있습니다. 하지만 이전 데이터에는 Analytics 쿠키만 있으며, 드물게 최신 데이터에는 ECID만 있을 수 있습니다.<p>Analytics(방문자 ID) 쿠키 또는 ECID를 통해 식별된 방문자의 모든 데이터를 찾으십시오. 현재 ECID를 사용하고 이전에 Analytics 쿠키를 사용한 경우, 두 가지 유형의 ID를 사용하여 요청을 제출할 때마다 요청에 두 ID를 포함하거나 를 지정해야 합니다 `expandIds` 선택 사항입니다. 지정한 경우 `expandIds`, Adobe은 제공하는 쿠키 ID에 해당하는 다른 ECID 또는 Analytics 쿠키가 있는지 확인합니다. 새로 식별된 이러한 쿠키 ID를 포함하도록 요청이 자동으로 확장됩니다. |
| 쿠키 ID 확장에 대한 사용자 정의 ID | 전자 상거래 웹 사이트에서는 방문자가 사이트에 로그인하기 전에 사이트를 탐색하고 장바구니에 항목을 추가한 후 체크아웃 절차를 시작하는 일이 흔합니다. 데이터 개인 정보 보호 요청에 대해 사용자를 식별하는 데 사용된 ID가 사용자가 로그인한 경우에만 사용자 지정 변수에 저장되는 경우 이 사전 로그인 활동은 ID와 연관되지 않습니다. Analytics 쿠키 ID를 사용하면 쿠키 ID가 로그인하는 동안 유지되므로 고객이 로그인 전에 수행한 탐색과 로그인 후 구매한 항목을 연결하도록 선택할 수 있습니다.<p>구현 시 사용자 정의 변수 (prop 또는 eVar) 또는 사용자 정의 방문자 ID에 로그인 ID(CRM ID, 사용자 이름, 로열티 번호, 이메일 주소 등, 또는 이러한 값 중 하나의 해시)를 저장하고 데이터 개인정보 보호 액세스 요청에 대해 이 ID를 사용한다고 가정해 봅시다. 데이터 주체는 탐색에 대한 모든 정보가 액세스 요청의 일부로 반환되지 않고, 특히 보긴 했지만 아직 구매하지 않은 항목을 프로모션한 경우 반환되지 않는다는 점에 대해 의아해할 수 있습니다. 따라서 Analytics 데이터 개인정보 보호 처리에서는 ID 확장을 지원합니다. 그러면 Analytics에서 사용자 정의 ID와 동일한 히트에서 발생하는 모든 쿠키 ID를 찾아서 그러한 ID를 포함하도록 요청을 확장합니다.<p>When `expandIDs` 는 쿠키 네임스페이스 이외의 네임스페이스와 함께 지정되며, 지정된 ID 중 하나를 포함하는 히트에 있는 모든 쿠키 ID(ECID 또는 Analytics 쿠키)를 포함하도록 요청이 확장됩니다. 위에 설명된 대로 쿠키 ID 확장은 새로 찾은 쿠키 ID에서 수행됩니다.<p>이 `expandIDs` 옵션이 액세스 요청에 사용되고 지정된 ID에 ID-PERSON 레이블이 있는 경우 두 파일 세트가 반환됩니다. 첫 번째 세트 (개인 세트)는 지정된 ID가 발견된 히트의 데이터만 포함합니다. 두 번째 세트 (디바이스 세트)는 지정된 ID가 없는 확장된 ID의 히트에서만 데이터를 포함합니다. |

{style=&quot;table-layout:auto&quot;}

## ID 확장을 사용해야 하는 경우

데이터 개인 정보 보호가 시행된 후 처음 몇 개월 동안 대부분의 Analytics 데이터 개인 정보 보호 요청이 ID 확장을 요청하지 않았습니다. 그러나 조직에 대한 적절한 값을 결정하는 것은 귀하의 책임입니다. 사용 중인 ID와 Adobe Analytics 내에서 수집하는 데이터로 ID 확장이 필요한지 여부에 대해서는 법무팀에 문의해야 합니다.

기본적인 고려 사항은 다음과 같습니다. 여러 사용자가 사이트를 방문한 공유 장치에서, ID 확장을 사용하면 장치의 다른 사용자 히트의 데이터가 액세스 요청에 의해 반환된 데이터(장치 파일)에 포함됩니다. 레이블 지정에 대한 우수 사례를 따랐더라도(예를 들어 방문한 페이지 등 장치 파일에 개인 데이터가 포함되지 않음) 장치 파일에는 방문한 페이지 수와 이러한 각 방문 횟수가 포함됩니다. 자신에게 물어보세요: 이 정보를 방문자가 아닐 수 있는 사람과 공유해도 괜찮습니까?

ID 확장이 *not* 삭제 요청에 사용됨: 쿠키가 아닌 ID(ECID 또는 Analytics 쿠키가 아닌 모든 ID)를 사용하여 삭제해야 할 히트를 식별하고 해당 ID에 ID-DEVICE 레이블이 있는 경우 보고서의 고유 방문자 수가 변경됩니다. 이는 쿠키 ID의 일부 인스턴스만 익명으로 처리되지만, 다른 인스턴스는 변경되지 않기 때문입니다. ID 확장을 지정하지 않는 경우 요청에 쿠키 ID를 사용하거나 ID-PERSON 레이블이 있는 ID를 사용하는 것이 좋습니다.

Adobe에서 ID 확장을 수행할 때 추가 전체 데이터 검사가 필요할 수 있습니다. 이를 통해 요청을 완료하는 데 Adobe이 걸리는 시간을 늘리며, 종종 처리 시간에 1주를 추가합니다.

## 기타 데이터 개인정보 보호 요청 플래그

다음 &quot;expandIDs&quot; 플래그 외에 Analytics에서는 데이터 개인정보 보호 요청 일부로 전달될 수 있는 두 가지 다른 플래그를 지원합니다. 이러한 플래그 및 기본값은 다음과 같습니다.

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

미래에는 `analyticsDeleteMethod` &quot;anonymize&quot;라는 기본값 외에 &quot;purge&quot;라는 값을 지원할 수 있습니다. 지원되면 DEL 레이블이 있는 히트 필드의 값을 단순히 업데이트하는 것이 아니라 전체 히트가 삭제됩니다.

기본값 외에 `priority` 필드는 &quot;low&quot; 값도 지원합니다. 데이터 주제 요청의 결과가 아닌 요청에 대해 이 값을 지정해야 하므로 30일 이내에 완료해야 할 법률상의 요구가 없습니다.

## Privacy Service API 사용

>[!IMPORTANT]
>
>Adobe은 [Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html) data-subject-initiated 요청 이외의 이유로. 데이터 개인정보 보호 API는 데이터 정리 또는 복구에 적합한 도구가 아니므로 의도하지 않은 결과가 발생합니다. Privacy Service API는 시간에 민감한 데이터 개인 정보 보호 요청을 이행하는 데 도움을 주기 위해 제공되었습니다. 이 API를 다른 용도로 사용하는 것은 Adobe에서 지원하지 않으며, Adobe가 다른 Adobe 고객을 위해 우선순위가 높은 사용자 주도 데이터 개인정보 보호 요청을 시기적절하게 제공하는 기능에 영향을 줄 수 있습니다. 많은 방문자 그룹에 실수로 제출된 데이터 지우기와 같은 다른 용도로는 Privacy Service API를 사용하지 마십시오.

또한 데이터 개인정보 보호 삭제 요청으로 인해 히트가 삭제 (업데이트 또는 익명 처리)된 방문자의 상태 정보는 재설정된다는 사실을 알고 있어야 합니다. 따라서 다음번에 방문자가 사용자의 웹 사이트로 돌아가면 새 방문자로 간주됩니다. 방문 수, 레퍼러, 방문한 첫 번째 페이지 등의 정보와 마찬가지로 모든 eVar 속성이 다시 시작됩니다. 이 부작용은 데이터 필드를 지우려는 경우 바람직하지 않으며, Privacy Service API가 이 사용에 대해 부적절한 이유 중 하나를 강조 표시합니다.

계정 관리자에게 문의(CSM)하여 PII 또는 데이터 문제를 없애는 데 필요한 노력을 더 자세히 검토하고 제공하도록 Engineering Architect(엔지니어링 설계) 컨설팅팀과 상의하십시오.
