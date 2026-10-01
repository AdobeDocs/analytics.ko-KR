---
description: 사용자 정의 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 정의 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다. eVar은 방문을 기반으로 할 수 있으며 쿠키와 유사하게 작동합니다. eVar 변수로 전달된 값은 사전 결정된 기간 동안 사용자를 따릅니다.
keywords: eVar
title: 전환 변수(eVar)
feature: Admin Tools
role: Admin
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
TQID: https://experienceleague.adobe.com/rYLxVYB1oDyfEk8gQyesTSRRPHid-6zJ8QaqFG2b0Kc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ca917b867cd84b09b899ce7b72586f0b15003106
workflow-type: tm+mt
source-wordcount: '1726'
ht-degree: 34%
---
# 전환 변수(eVar)

사용자 정의 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 정의 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다. eVar은 방문을 기반으로 할 수 있으며 쿠키와 유사하게 작동합니다. eVar 변수로 전달된 값은 미리 정해진 기간 동안 사용자를 따라 유지됩니다.

**[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 변수]**

## 전환 변수(eVars) 개요

전환 변수에 대한 비디오 개요는 Analytics 자습서 안내서에서 [전환 변수 소개](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/dimensions/introduction-to-conversion-variables-evars)를 참조하십시오.

eVar가 방문자에 대한 값으로 설정될 때 Adobe는 값이 만료될 때까지 해당 값을 자동으로 기억합니다. eVar 값이 활성 상태인 동안 방문자가 발생하는 모든 성공 이벤트는 eVar 값에 대해 계산됩니다.

eVar는 다음과 같이 원인과 영향을 측정하는 데 가장 잘 사용됩니다.

* 매출에 영향을 준 내부 캠페인
* 어떤 배너 광고가 궁극적으로 등록을 초래합니까
* 주문하기 전에 내부 검색을 사용한 횟수

트래픽 측정 또는 경로 지정이 필요한 경우 트래픽 변수를 사용하는 것이 좋습니다.

>[!NOTE]
>
>단일 값만 이미지 요청 시 eVar에 저장할 수 있습니다. eVar 값에 여러 값을 사용하려는 경우 [목록 변수](/help/implement/vars/page-vars/page-variables.md)를 사용하십시오.

### 전환 변수 - 설명 {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

| 요소 | 설명 |
| --- | --- |
| [!UICONTROL 상태] | eVar이 활성 상태인지 여부를 결정합니다.<ul><li>**[!UICONTROL 사용]**: eVar이 활성 상태입니다.</li><li>**[!UICONTROL 사용 안 함]**: eVar을 사용하지 않도록 설정하고 전환 변수 목록에서 제거합니다.</li></ul> |
| [!UICONTROL 설명] | eVar에 대한 선택적 설명. 이를 사용하여 eVar이 캡처하는 내용과 구현 방법을 문서화합니다. |
| [!UICONTROL 이름] | 전환 변수의 친숙한 차원 이름입니다. 일반적인 보고에서는 eVar을 참조합니다. |
| [!UICONTROL 할당] | 변수가 이벤트 이전에 여러 개의 값을 받을 경우 Analytics가 성공 이벤트에 대한 크레딧을 할당하는 방법을 결정합니다. 지원되는 값은 다음과 같습니다.<ul><li>**[!UICONTROL 가장 최근(마지막)]**: 마지막 eVar 값은 해당 eVar이 만료될 때까지 성공 이벤트에 대한 크레딧을 항상 받습니다.</li><li>**[!UICONTROL 원래 값(첫 번째)]**: 첫 번째 eVar은 해당 eVar이 만료될 때까지 성공 이벤트에 대한 크레딧을 항상 받습니다.</li><li>**[!UICONTROL 선형]**: 모든 eVar 값에 균일하게 성공 이벤트를 할당합니다. 선형 할당은 방문 내에만 값을 분배하므로 선형 할당은 eVar 방문 만료 또는 그 이전에 사용합니다. 이 옵션은 머천다이징 eVar에 사용할 수 없습니다.</li></ul>**중요**: Adobe에서는 [!UICONTROL 선형] 할당을 전환하지 않도록 권장합니다. 다시 전환할 때까지 보고 시 내역 데이터를 숨깁니다. 변경 기록이 많은 eVar에서 할당을 변경하려면 새 eVar을 대신 사용하는 것이 좋습니다. |
| [!UICONTROL 다음 시기 이후에 만료] | eVar 값이 만료되는 시기를 지정합니다(더 이상 성공 이벤트에 대한 크레딧을 받지 않음). eVar 만료 후 성공 이벤트가 발생하면 None 값이 해당 이벤트에 대한 크레딧을 받습니다(eVar가 활성 상태가 아니었음). 지원되는 값은 다음과 같습니다.<ul><li>**[!UICONTROL Visit]**: 값이 방문이 끝날 때 만료됩니다.</li><li>**[!UICONTROL 히트]**: 이 값은 설정된 히트에만 적용됩니다.</li><li>**[!UICONTROL 분]**, **[!UICONTROL 시간]**, **[!UICONTROL 일]**, **[!UICONTROL 주]**, **[!UICONTROL 월]**, **[!UICONTROL 분기]** 또는 **[!UICONTROL 연도]**: 값이 설정된 후 고정된 시간 후에 만료됩니다.<ul><li>분 = 60초</li><li>시간 = 3600초(60분)</li><li>일 = 86400초(24시간)</li><li>주 = 604800초(7일)</li><li>월 = 2678400초(31일)</li><li>분기 = 8035200초(93일 - 3개월 31일)</li><li>Year = 31536000초 (365일)</li></ul>예를 들어 eVar이 월요일 오전 7시 15분으로 설정된 경우 [!UICONTROL 일] 만료는 화요일 오전 7시 15분에 종료되고, [!UICONTROL 주] 만료는 다음 월요일 오전 7시 15분에 종료되며, [!UICONTROL 월] 만료는 31일 후 오전 7시 15분에 종료됩니다.</li><li>**[!UICONTROL 사용자 지정]**: 입력한 일 수(하루에 86400초)가 지나면 값이 만료됩니다.</li><li>**이벤트**([!UICONTROL 구매], [!UICONTROL 제품 보기], [!UICONTROL 장바구니 열기], [!UICONTROL 장바구니 체크아웃], [!UICONTROL 장바구니 추가], [!UICONTROL 장바구니 제거], [!UICONTROL 장바구니 보기] 또는 사용자 지정 이벤트): 선택한 이벤트가 발생하면 값이 만료됩니다. 이벤트가 발생하지 않으면 값이 만료되지 않습니다.</li><li>**[!UICONTROL 절대]**: 방문자가 동일한 식별자를 사용하는 한 eVar과 이벤트 간에 시간이 경과할 수 있습니다.</li></ul> |
| [!UICONTROL Type] | 변수 값 유형은 다음과 같습니다.<ul><li>**[!UICONTROL 텍스트 문자열]**: 텍스트 값을 캡처합니다. eVar의 가장 일반적인 유형이며 기본 설정입니다. 이는 다른 변수와 유사하게 작동하며, 변수 내 값은 정적 텍스트 문자열입니다. 내부 캠페인 또는 내부 검색 키워드와 같은 것을 추적하는 경우 이 설정이 권장됩니다.</li><li>**[!UICONTROL 카운터:]** 성공 이벤트 이전의 작업 발생 횟수를 카운트합니다. 예를 들어 성공 이벤트 전에 사용된 검색어에 관계없이 검색 횟수를 카운트할 수 있습니다.</li></ul> |
| [!UICONTROL 재설정] | 저장 시 머천다이징 제품 바인딩을 포함하여 모든 방문자에 대해 이 변수에 대한 서버측 지속 값이 모두 즉시 만료됩니다. 새 보고서에 이전 값을 혼합하지 않도록 eVar의 용도를 변경할 때 [!UICONTROL 재설정]을 사용합니다. **다시 설정하면 이전 데이터가 지워지지 않습니다.** |
| [!UICONTROL 머천다이징 사용] | 지원되는 값은 다음과 같습니다.<ul><li>**[!UICONTROL 사용 안 함]**: eVar에서 방문자에 대해 지속되는 값에 성공 이벤트를 크레딧합니다.</li><li>**[!UICONTROL 사용]**: eVar은 개별 제품에 값을 바인딩하는 머천다이징 eVar이 됩니다. 각 제품에 대한 성공 이벤트는 해당 제품에 바인딩된 값에 반영됩니다. 머천다이징을 사용하도록 설정하면 [!UICONTROL 머천다이징] 및 [!UICONTROL 머천다이징 바인딩 이벤트] 설정이 표시되고 [!UICONTROL 선형] 할당이 제거됩니다.</li></ul>제품을 발견하거나 구매하는 방법을 설명하는 eVar에 대해서만 머천다이징을 활성화합니다. 머천다이징 eVar은 더 이상 제품에 연결되지 않은 성공 이벤트를 크레딧하지 않습니다. [eVar(머천다이징)](/help/components/dimensions/evar-merchandising.md)을 참조하세요. |
| [!UICONTROL 머천다이징] | 제품에 바인딩할 값의 출처 결정:<ul><li>**[!UICONTROL 제품 구문]**: 값이 `products` 변수의 각 제품에 설정되어 있으며 해당 히트의 해당 제품에 바인딩됩니다. 각 제품은 다른 값을 가질 수 있습니다. 바인딩 이벤트가 사용되지 않으므로 [!UICONTROL 머천다이징 바인딩 이벤트]를 사용할 수 없습니다.</li><li>**[!UICONTROL 전환 변수 구문]**: 이 값은 eVar 자체에서 설정되고 스테이징된 값으로 유지되며 [!UICONTROL 할당]에 관계없이 전송된 가장 최근 값을 항상 반영합니다. 해당 히트에 선택한 [!UICONTROL 머천다이징 바인딩 이벤트]가 포함된 경우에만 값이 히트의 제품에 바인딩됩니다. 해당 히트의 모든 제품은 동일한 값을 받습니다.</li></ul>그에 따라 구현을 업데이트하지 않고 이 설정을 변경하면 데이터가 손실됩니다. 구현 세부 정보는 [eVar(머천다이징 변수)](/help/implement/vars/page-vars/evar-merchandising.md)을 참조하십시오. |
| [!UICONTROL 머천다이징 바인딩 이벤트] | [!UICONTROL 머천다이징]이 [!UICONTROL 전환 변수 구문]&#x200B;(으)로 설정된 경우에만 사용할 수 있습니다. eVar의 준비된 값을 동일한 히트의 제품에 바인딩하는 이벤트 또는 eVar를 결정합니다. 바인딩 이벤트를 선택하지 않으면 [!UICONTROL 모두]이 사용됩니다. 지원되는 값은 다음과 같습니다.<ul><li>**[!UICONTROL 모두]**: 히트의 다른 모든 이벤트 또는 eVar이 바인딩을 트리거합니다. 이 설정은 기본값입니다.</li><li>**[!UICONTROL 구매 이벤트]**, **[!UICONTROL 제품 보기 이벤트]**, **[!UICONTROL 장바구니 열기 이벤트]**, **[!UICONTROL 장바구니 체크아웃 이벤트]**, **[!UICONTROL 장바구니 추가 이벤트]**, **[!UICONTROL 장바구니 제거 이벤트]** 또는 **[!UICONTROL 장바구니 보기 이벤트]**: 선택한 이벤트가 포함된 히트에서 바인딩이 발생합니다.</li><li>**[!UICONTROL Campaign 이벤트]**: [추적 코드](/help/components/dimensions/tracking-code.md) 차원([`campaign`](/help/implement/vars/page-vars/campaign.md) 변수)의 인스턴스가 포함된 히트에서 바인딩이 발생합니다.</li><li>**사용자 지정 이벤트**: 선택한 사용자 지정 이벤트가 포함된 히트에서 바인딩이 발생합니다.</li><li>**사용자 지정 eVar**: 선택한 eVar을 설정하는 히트에서 바인딩이 발생합니다.</li></ul>Prop은 바인딩을 트리거할 수 없습니다. ctrl(Windows) 또는 cmd(Mac)를 누른 채로 목록에서 여러 항목을 클릭하여 여러 값을 선택합니다. eVar에 이미 바인딩된 특정 제품이 동일한 eVar을 사용하는 다른 바인딩을 수신하면 [!UICONTROL 할당]에서 보존되는 값을 결정합니다. |

### 만료

`eVars`는 지정되는 일정 기간 후 만료되며 만료된 후 eVar는 더 이상 성공 이벤트에 대한 크레딧을 받지 않습니다. eVar는 성공 이벤트 시 만료되도록 구성할 수도 있습니다. 예를 들어 방문이 끝날 때 만료되는 내부 판촉 행사가 있는 경우, 내부 판촉 행사는 활성화된 방문 중에 발생한 구매 또는 등록에 대해서만 크레딧을 받습니다.

eVar을 만료하는 방법에는 두 가지가 있습니다.

* 지정된 기간이나 이벤트 후 eVar가 만료되도록 설정할 수 있습니다.
* 재설정하여 eVar의 만료를 강제 적용할 수 있으며, 이는 변수를 다른 목적에 사용할 때 유용합니다.

예를 들어 eVar의 만료를 30일에서 90일로 변경하면 수집된 eVar 값은 새로 설정된 만료 기간(이 경우 90일) 동안 계속 유지됩니다. 시스템은 현재 만료 설정 및 수집된 eVar 값의 마지막 세트 타임스탬프를 보고 만료를 확인합니다. **[!UICONTROL 재설정]** 옵션만 값을 만료하고 즉시 만료됩니다.

다른 예: eVar를 내부 판촉 행사 반영을 위해 5월에 사용하고 21일 후 만료되며 6월에 내부 검색 키워드를 캡처하는 데 사용한다면 6월 1일에 변수를 강제로 만료하거나 재설정해야 합니다. 이렇게 하면 내부 판촉 행사 값을 6월의 보고서에서 빼는 데 유용합니다.

### 대/소문자 구분

eVar는 대소문자를 구분하지 않습니다. 보고에 사용되는 대문자 또는 소문자는 백엔드 시스템이 등록하는 첫 번째 값을 기반으로 합니다. 이 값은 보고서 세트와 관련된 데이터의 다양성과 수량에 따라 지금까지 확인된 첫 번째 인스턴스일 수도 있고, 일정 기간(예: 매월)에 따라 달라질 수도 있습니다.

### 카운터

eVar는 대부분 문자열 값을 보관하는 데 사용되지만, 카운터로 작동하도록 구성할 수도 있습니다. eVar는 이벤트 전에 사용자가 취하는 동작의 수를 세려고 할 때 카운터로 유용합니다. 예를 들어 구매 전에 eVar를 사용하여 내부 검색 횟수를 캡처할 수 있습니다. 방문자가 검색할 때마다, eVar에는 &#39;+1&#39; 값이 포함되어야 합니다. 방문자가 구매 전에 검색을 네 번 수행하면, 각각 총 횟수는 1.00, 2.00, 3.00 및 4.00이 됩니다. 하지만 4.00만 구매 이벤트(주문 및 매출 지표)에 대한 크레딧을 받습니다. eVar 카운터의 값에는 양수만 사용할 수 있습니다.

## 전환 변수 추가 또는 편집

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. 보고서 세트 선택.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 변환]** > **[!UICONTROL 전환 변수]**&#x200B;를 클릭합니다.
1. [!UICONTROL 전환 변수] 페이지에서 수정할 전환 변수 옆에 있는 **[!UICONTROL 확장]** 아이콘 [+]를 클릭합니다.

   또는

   보고서 세트에 사용하지 않은 eVar를 추가하려면 **[!UICONTROL 새로 추가]**&#x200B;를 클릭합니다.
1. 수정할 전환 변수 필드를 선택합니다.

   [전환 변수 - 설명](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md#section_7C317BB0287A4B8EB0A1A4ECC40627BF)을 참조하세요. 일부 필드에는 직접 입력할 수 있습니다. 다른 옵션을 사용하면 지원되는 값의 드롭다운 목록에서 선택할 수 있습니다.
1. **[!UICONTROL 저장을]** 클릭합니다.
