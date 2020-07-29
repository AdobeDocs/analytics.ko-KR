---
title: eVar
description: 보고에 사용할 수 있는 사용자 지정 차원입니다.
translation-type: tm+mt
source-git-commit: 7c722e361978a3d7517e95c23442b703e7e25270
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 67%

---


# eVar

*이 도움말 페이지에서는 eVar가 차원으로 작동하는 방식을 설명합니다. eVar 구현 방법에 대한 자세한 내용은 구현 사용 안내서의[eVar](/help/implement/vars/page-vars/evar.md)를 참조하십시오.*

eVar는 원하는 대로 사용할 수 있는 사용자 지정 변수입니다. [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)가 있는 경우 조직 고유의 차원은 대부분 eVar로 끝납니다. 기본적으로 eVar는 설정된 히트를 넘어서까지 지속됩니다. You can customize their expiration and allocation under [Conversion variables](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in Report suite settings.

사용 가능한 eVar 수는 Adobe과의 계약에 따라 다릅니다. Adobe과의 계약이 지원하는 경우 최대 250개의 eVar를 사용할 수 있습니다.

eVar는 대소문자를 구분하지 않습니다. 같은 값을 다른 경우(예: `"DOG"` 및 `"Dog"`) 보낼 경우 Analysis Workspace은 같은 차원 항목으로 그룹화합니다. 보고 월의 시작 부분에 표시되는 첫 번째 값의 대/소문자가 사용됩니다. Data warehouse은 요청 기간 동안 발견된 첫 번째 값을 표시합니다.

## 데이터로 eVar 채우기

각 eVar은 이미지 요청의 [`v1` - `v250` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 수집합니다. 예를 들어 쿼리 `v1` 문자열 매개 변수는 eVar1에 대한 데이터를 수집하는 반면 `v222` 쿼리 문자열 매개 변수는 eVar222에 대한 데이터를 수집합니다.

JavaScript 변수를 데이터 수집에 대한 이미지 요청으로 컴파일하는 AppMeasurement는 변수 `eVar1` -를 사용합니다 `eVar250`. 구현 가이드라인에 대해서는 [구현](/help/implement/vars/page-vars/evar.md) 사용 안내서의 eVar을 참조하십시오.

## Dimension 항목

eVar에는 구현에 사용자 지정 문자열이 들어 있으므로 조직은 각 eVar에 대한 차원 항목을 결정합니다. 각 eVar 및 일반 차원 항목의 용도를 [솔루션 디자인 문서에 기록해야 합니다](/help/implement/prepare/solution-design.md).

## eVar 작동 방식

데이터를 Adobe Analytics로 보내면 데이터 수집 서버에서 히트를 수백 개의 열이 있는 단일 데이터 행으로 변환합니다. 두 개의 열이 각 eVar에 전용으로 사용됩니다. 하나는 직접 데이터 수집에 사용되고, 다른 하나는 지속 값에 사용됩니다.

* 표준 열에는 이미지 요청에서 Adobe로 전송된 데이터가 포함됩니다.
* 게시물 열에는 일관된 데이터가 들어 있으며, 이는 eVar의 만료 및 할당에 따라 달라집니다.

거의 모든 상황에서 `post_evar` 열은 보고서에 사용됩니다.

### eVar를 지표에 연결하는 방법

성공 이벤트와 eVar는 다른 이미지 요청에 자주 정의됩니다. `post_evar` 열에서 eVar 값을 이벤트에 연결하여 보고에 데이터를 표시할 수 있습니다. 예를 들어 다음 방문을 수행합니다.

1. 방문자가 홈 페이지의 사이트에 도달합니다.
2. 사이트의 내부 검색을 사용하여 &quot;cats&quot;를 검색합니다. 구현에서는 내부 검색에 eVar1을 사용합니다.
3. 제품을 보고 체크아웃 프로세스를 진행합니다.

원시 데이터의 간소화된 버전은 다음과 비슷합니다.

| `visitor_id` | `pagename` | `evar1` | `post_evar1` | `event_list` |
| --- | --- | --- | --- | --- |
| `examplevisitor_987` | `Home page` |  |  |  |
| `examplevisitor_987` | `Search results` | `cats` | `cats` | `event1` |
| `examplevisitor_987` | `Product page` |  | `cats` | `prodView` |
| `examplevisitor_987` | `Cart` |  | `cats` | `scAdd` |
| `examplevisitor_987` | `Checkout` |  | `cats` | `scCheckout` |
| `examplevisitor_987` | `Purchase confirmation` |  | `cats` | `purchase` |

* `visitor_id` 열은 히트를 동일한 방문자에게 연결합니다. 실제 원시 데이터에서 `visid_high`와 `visid_low`의 연결된 값이 방문자 ID를 결정합니다.
* `pagename` 열은 페이지 차원을 채웁니다.
* `evar` 열은 eVar1이 명시적으로 설정된 경우 히트 수를 결정합니다.
* `post_evar1`은 보고서 세트 설정에 있는 변수의 할당 및 만료 세트에 따라 이전 값을 전달합니다.
* `event_list` 열에는 모든 지표 데이터가 포함됩니다. 이 예제의 경우 `event1`은 &#39;검색&#39;이고, 다른 이벤트는 표준 장바구니 지표입니다. 실제 원시 데이터에서 `event_list`에 쉼표로 구분된 숫자 세트와 그러한 숫자들을 지표에 묶은 조회 테이블이 있습니다.

### 데이터 수집을 보고로 번역

Analysis Workspace와 같은 Adobe Analytics의 도구는 수집된 이러한 데이터에서 작동합니다. 예를 들어 eVar1을 차원으로 사용하고 주문을 지표로 사용하여 보고서를 가져오면 다음과 유사한 보고서가 표시됩니다.

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analysis Workspace에서 다음 논리를 사용하여 이 보고서를 가져옵니다.

* 모든 `event_list` 값을 찾은 다음 값에 `purchase`가 있는 모든 히트를 선택합니다.
* 그러한 히트 중에서 `post_evar1` 값을 표시합니다.

### 할당 및 만료의 중요성

할당 및 만료는 지속되는 값을 결정하므로 분석 구현에서 더 많은 가치를 창출하는 데 중요합니다. Adobe에서는 조직 내에서 각 eVar에 대한 여러 값을 처리하는 방법(할당)과 eVar가 데이터 유지를 중단하는 방법(만료)에 대해 논의할 것을 권장합니다.

* 기본적으로 eVar는 마지막 할당을 사용합니다. 새 값이 유지된 값을 덮어씁니다.
* 기본적으로 eVar는 방문 만료를 사용합니다. 방문이 종료되면 `post_evar` 열의 행에서 행으로 값 복사가 중지됩니다.

You can change eVar allocation and expiration under [Conversion variables](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in Report suite settings.

## prop보다 eVar의 값

대부분의 경우 다음을 통해 지원되는 eVar를 사용하는 것이 좋습니다.

* eVar는 보고서에서 255바이트 제한을 갖습니다. Prop에는 100바이트 제한이 있습니다.
* 기본적으로 prop은 prop이 설정된 히트 이후에 지속되지 않습니다. eVar에는 사용자 지정 만료가 있으므로, eVar가 후속 이벤트에 대한 크레딧을 더 이상 받지 않는 시기를 결정할 수 있습니다. 하지만 [보고서 시간 처리](/help/components/vrs/vrs-report-time-processing.md)를 사용하는 경우 속성과 eVar 모두 사용자 지정 속성 모델을 사용할 수 있습니다.
* Adobe은 최대 250개의 eVar를 지원하고 75개의 prop만 지원합니다.

prop과 eVar 간의 [더 많은 비교는 prop](prop.md) 을 참조하십시오.
