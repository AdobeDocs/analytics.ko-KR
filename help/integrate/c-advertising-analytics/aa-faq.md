---
description: Advertising Analytics에 대해 자주 묻는 질문입니다.
title: Advertising Analytics에 대해 자주 묻는 질문
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 37%

---

# FAQ

## 액세스/권한 부여 {#access}

+++ 이 기능에 액세스하려면 Adobe Advertising Cloud 또는 AMO(Adobe Advertising Cloud) 고객이어야 합니까?

아니요. 이 기능은 Advertising Cloud 및 AMO를 사용하지 않는 고객도 사용할 수 있습니다.

AMO 고객은 기존의 Analytics-AMO 통합을 활용할 수 있으며, Ad Analytics를 사용할 수 없습니다.

+++

+++ Advertising Analytics 사용 권한을 부여하는 Adobe Analytics SKU는 무엇입니까?

Adobe Analytics에서 Advertising Analytics 사용 가능

* [선택](https://www.adobe.com/kr/data-analytics-cloud/analytics/select.html)

* [Prime](https://www.adobe.com/kr/data-analytics-cloud/analytics/prime.html)

* [Ultimate](https://www.adobe.com/kr/data-analytics-cloud/analytics/ultimate.html)

+++

+++ Advertising Analytics을 이용하려면 추가 요금을 내야 하나요?

아니요. 적절한 SKU 프로비저닝 Advertising Analytics 외에는 추가 비용이 발생하지 않습니다.

+++

+++ Advertising Analytics은 내 서버 호출 사용량에 따라 계산됩니까

아니요. Advertising Analytics에서는 서버 호출 비용이 발생하지 않는 특수 데이터 소스 유형을 사용합니다.

+++

+++ 이미 Advertising Cloud/AMO를 사용하고 있는 경우에도 Advertising Analytics 기능을 사용할 수 있습니까?

호환되는 검색 엔진 계정은 모두 Advertising Analytics으로 전달되고 읽기 전용으로 표시됩니다. 모든 편집 또는 업데이트는 Advertising Cloud/AMO에서 처리해야 합니다.

+++

+++ 올바른 SKU를 소유하고 있지만 Advertising Analytics에 액세스할 수 없습니다. 이유는 무엇입니까?

Advertising Analytics은 Adobe Analytics 관리자만 사용할 수 있습니다. 하지만 관리자는 관리자가 아닌 사용자에게 액세스 권한을 부여할 수 있습니다. 관리자에게 액세스 권한에 대해 문의하십시오.

+++

## Advertising Analytics 사용 {#using}

+++ Advertising Analytics에는 어떤 검색 엔진 계정이 포함됩니까?

검색 엔진 계정에는 Google Ads 및 Microsoft Advertising이 포함됩니다.

+++

+++ Advertising Analytics에 액세스하려면 어디로 이동합니까?

Adobe Analytics에 로그인한 후 [!UICONTROL 관리자]&#x200B;(으)로 이동합니다. 그런 다음 [!UICONTROL Advertising Analytics]을(를) 선택하여 검색 엔진 계정을 추가합니다.

+++

+++ 데이터를 수집하여 Analytics로 전달하는 방법은 무엇입니까?

Advertising Analytics은 일련의 사용자 지정 API를 사용하여 Adobe Advertising Cloud를 통해 검색 엔진의 데이터를 Analytics에 전달합니다.

+++

+++ 이 통합에서 얻을 수 있는 검색 데이터는 무엇입니까?

다음을 얻을 수 있습니다.

* 노출 횟수
* 클릭 수
* 비용
* 품질 점수입니다
* 검색 엔진에서 직접 평균 위치 및
* AMO ID 인스턴스(인스턴스 클릭).

+++

+++ 다른 Analytics 데이터(지표/차원)로 Advertising Analytics 데이터를 분류할 수 있습니까?

아니요. 원시 검색 데이터는 독립적인 데이터 세트로 제공됩니다. 하지만 다른 Analytics 데이터로 분류할 수 있는 클릭 데이터의 인스턴스 버전이 있습니다.

+++ 내 계정에 대한 여러 상태 표시기 의 정의는 무엇입니까 (보류 중, 활성, 일시 정지됨 등)? 이러한 각 상태 표시기는 각 검색 엔진 계정의 라이프사이클 단계를 식별합니다.

* [!UICONTROL 보류 중]
* [!UICONTROL 일시 정지됨]은 계정이 이전에 설정되었지만 비활성 상태에 있음을 의미합니다.
* [!UICONTROL 활성]은 계정이 완전히 설정되었으며, 검색 데이터를 가져오고 있음을 의미합니다.

+++

+++ Advertising Analytics 계정을 특정 보고서 세트에 매핑하려고 하지만 보고서 세트 모달에서는 사용할 수 없습니다. 왜일까요?

보고서 세트를 Advertising Analytics 계정에 할당하려면 먼저 원하는 보고서 세트를 [Advertising Analytics 보고용으로 프로비저닝](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md)해야 합니다.
이 작업은 별도 관리 페이지에서 수행합니다. 이 페이지는 관리 > 보고서 세트 > `[select report suite]` > 설정 편집 > Advertising Analytics 구성에서 액세스할 수 있습니다.

+++

+++ Advertising Analytics 계정에 가상 보고서 세트를 할당할 수 있습니까?

가상 보고서 세트는 데이터를 수집하지 않으므로 Advertising Analytics 계정을 가상 보고서 세트에 직접 매핑할 수 없습니다. 그러나 Advertising Analytics 계정을 데이터를 보려는 가상 보고서 세트의 상위 보고서 세트에 매핑할 수 있습니다. AMO ID(또는 해당 분류)를 기반으로 세그먼트 논리에 &quot;or&quot; 조건을 포함하지 않으면 검색 엔진 지표(클릭/비용/노출 수)가 가상 보고서 세트에 표시되지 않을 수 있습니다. 예: “AMO ID가 있는 모든 조회 수”를 추가하면 세그먼트에 검색 엔진 지표가 포함됩니다.

+++

+++ *마케팅 채널* 보고서에 Advertising Analytics 지표를 보고할 수 있습니까?

아니요. 마케팅 채널 보고서에는 이러한 지표가 포함되지 않습니다.

+++

+++ 검색 데이터를 언제 Analytics로 가져옵니까?

검색 데이터는 Analytics 데이터 센터의 시간대를 기준으로 하여 오전 6시(06:00)에 검색 엔진에서 가져옵니다. 이 때 AMO 데이터가 수집되고 보고서 세트에 삽입됩니다. 그런 다음 Analytics에 데이터를 삽입할 때 보고서 세트 시간대로 변환됩니다.

+++

+++ *클릭 전에 캡처할 수 있는 항목* 클릭하지 않더라도 노출 횟수, 비용, 평균 위치 등이 표시됩니까?

AMO ID는 검색 엔진 지표(노출 횟수, 비용, 클릭 수, 평균 위치 및 평균 품질 점수)를 캡처합니다. 클릭이 없지만 노출 횟수가 있는 경우 노출/위치/품질 점수 데이터가 계속 Analytics에 전송됩니다. 일반적으로 클릭이 없는 경우에는 비용도 없습니다.

+++

+++ 이 데이터는 어느 수준에서 캡처됩니까? *방문자? 히트?*

검색 엔진 지표는 히트 수준에서 캡처되며 AMO ID(및 해당 분류)에 연결됩니다. 요약 수준 데이터이며 방문 횟수/방문자 수에 연결되어 있지 않습니다. 따라서 검색 엔진 지표는 조회수 수준 범위에 있으며 AMO ID (또는 해당 분류)를 기반으로 하는 세그먼트에서만 사용할 수 있습니다.

또한 AMO ID는 방문 횟수/방문자 수에 연결된 해당 페이지 조회수의 랜딩 페이지에서 캡처되며 다른 Analytics 지표에 대한 크레딧을 가져오기 위해 (만료될 때까지 또는 새 AMO ID가 덮어쓸 때까지) 다운스트림을 유지합니다. 다른 eVar와 같이 데이터 세트에 완전히 통합되었습니다.

+++

+++ google.com 또는 *국가 버전*(google.co.uk, google.it, google.fr 또는 google.de)만 캡처합니까?

광고 플랫폼 분류는 &quot;Google Adwords&quot; 및 &quot;Bing Ads&quot; 값을 캡처합니다. 일반적인 우수 사례에는 캠페인 이름의 일부로 국가 코드가 포함됩니다. 그 이후에 필터링하거나 분류할 수 있습니다 (예: 모든 캠페인이 countrycode_로 시작하는 경우 캠페인 (AMO ID)이 &#39;UK_&#39;로 시작하는 세그먼트를 생성하여 영국에 대한 데이터만 제공).

+++

+++ 지표 &quot;AMO 비용&quot;은 검색 엔진에서 보고한 대로 각 키워드/광고에 대해 지불된 비용입니다. 이는 순비용 또는 총비용입니까?

&quot;AMO 비용&quot;은 검색 엔진에 지불된 비용입니다. 에이전시 또는 검색 최적화/관리 플랫폼 수수료는 포함되지 않습니다.

+++

+++ *디스플레이* 또는 *소셜*&#x200B;과 같은 다른 광고 채널을 포함할 계획이 있습니까?

아니요. 현재 로드맵에는 이러한 다른 채널에 대한 계획이 없습니다.

+++


## 자동 vs 수동 추적 {#section_7437C4698A6D482EB7ED94A948390119}

+++ 내 Advertising 계정을 설정할 때 *자동 추적*&#x200B;이 의도하지 않은 결과를 초래할 수 있다고 표시됩니다. 어떤 결과가 발생할 수 있습니까?

자동 모드에서는 URL 매개 변수를 올바른 형식으로 추적 템플릿/대상 URL의 끝에 추가하려고 합니다. 그러나 추가된 URL 매개 변수가 최종 랜딩 페이지에 올바르게 유지되는지는 사용자가 확인해야 합니다. 자동 모드는 랜딩 URL에 키워드를 삽입할 수 있으며, 웹 서버가 특수 문자가 있는 키워드를 지원하지 않을 수 있습니다.

+++

+++ 처음에 수동 또는 자동 추적을 설정한 경우 나중에 다른 추적 모드로 전환할 수 있습니까? 이 작업에 함축된 의미는 무엇입니까?

예, 추적 모드를 전환할 수 있지만 전환하기 전에 이전 추적 로직을 제거해야 합니다. 이로 인해 전환 시 추적이 다소 중단될 수 있습니다 (특히 수동에서 자동으로 이동하는 경우). 따라서 반드시 필요한 경우가 아니면 전환하지 않는 것이 좋습니다.

* 수동에서 자동으로 전환: 추적 템플릿에 대한 수동 추가 사항을 제거한 다음 Advertising Analytics UI의 토글을 수동에서 자동으로 전환하고 설정을 저장합니다. 시스템에서 자동 추적 코드를 채우는 데 몇 시간이 걸릴 수 있습니다.

* 자동에서 수동으로 전환: Advertising Analytics 설정 UI에서 수동에서 자동으로 토글을 업데이트한 다음 가능한 한 빨리 수동 추적 코드를 배포합니다. 수동 추적 코드를 배포하는 동안 검색 엔진 추적 템플릿에 자동 추적 코드가 표시되는 경우 해당 코드를 제거합니다.

+++
