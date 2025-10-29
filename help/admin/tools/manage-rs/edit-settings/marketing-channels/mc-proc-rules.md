---
title: 마케팅 채널의 처리 규칙
description: 규칙을 사용하여 히트가 속한 마케팅 채널을 결정합니다.
feature: Marketing Channels
exl-id: 825f70a5-cce3-4b1c-bb42-828388348216
role: Admin
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 3%

---

# 마케팅 채널 처리 규칙

_이 페이지는 히트에 마케팅 채널을 할당하는 처리 규칙을 참조합니다. 데이터 수집 방법을 조정할 수 있는 기능에 대해서는 [처리 규칙](../general/processing-rules/pr-overview.md)을 참조하십시오._

마케팅 채널 처리 규칙을 사용하면 [마케팅 채널](/help/components/dimensions/marketing-channel.md) 및 [마케팅 채널 세부 정보](/help/components/dimensions/marketing-detail.md) 차원에 대한 값을 결정하는 논리를 만들 수 있습니다. [마케팅 채널 관리자](c-channels.md)를 사용하여 사용 중인 마케팅 채널을 확인한 다음 처리 규칙을 사용하여 각 채널이 설정되는 방법을 결정하십시오.

![마케팅 채널 버킷](assets/buckets_2.png)

**[!UICONTROL Analytics]** > **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 마케팅 채널]** > **[!UICONTROL 마케팅 채널 처리 규칙]**

[자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md)이 실행되면 설정 중에 생성된 각 채널에 대한 규칙이 만들어집니다.

![기본 규칙](assets/marketing_channel_rules.png)

여러 규칙을 사용하여 단일 마케팅 채널을 정의할 수 있습니다. 규칙 조건에 따라 채널 세부 사항을 다르게 설정하려는 경우 단일 채널에 대해 여러 규칙을 사용하는 것이 유용할 수 있습니다. 여러 조건을 사용하여 단일 규칙을 정의할 수도 있습니다.

## 규칙 정의

각 규칙에는 조건과 할당이 포함됩니다.

* **[!UICONTROL 다음 중 하나 또는 모두가 참인 경우]**: 하나의 규칙에 여러 조건을 추가하는 경우 모든 조건을 충족해야 하는지 또는 조건 중 하나를 충족해야 하는지 확인하여 채널 및 관련 값을 설정할 수 있습니다.
* **규칙 조건**: 충족해야 하는 규칙 조건을 하나 이상 지정합니다. 일반적으로 마케팅 채널에 적합하기 위해 히트가 일치해야 하는 차원을 지정합니다.
* **[!UICONTROL 다음 작업 수행]**: 규칙 조건이 일치하면 [마케팅 채널](/help/components/dimensions/marketing-channel.md)([!UICONTROL 채널을 다음으로 식별])과 [마케팅 채널 세부 정보](/help/components/dimensions/marketing-detail.md)([!UICONTROL 채널 값 설정])을 설정합니다.

## 규칙 조건

규칙 조건을 설정할 때 다음 옵션을 사용할 수 있습니다.

>[!NOTE]
>
>모든 텍스트 필드는 **대/소문자를 구분하지 않습니다**. 예를 들어 쿼리 문자열 매개 변수 `cmp`이(가) `abc123`인 규칙 조건을 사용하는 경우 쿼리 문자열 매개 변수와 값 모두 대문자와 소문자를 조합하여 사용할 수 있습니다.

**Adobe에서 검색한 조건**&#x200B;에 텍스트를 입력할 수 있는 옵션 또는 필드가 없습니다.

| Adobe 감지 조건 | 설명 |
|---|---|
| **[!UICONTROL 유료 검색 감지 규칙과 일치]** | 히트가 인식된 검색 엔진에서 시작되었으며 [유료 검색 감지 규칙](../general/paid-search-detection/paid-search-detection.md)과 일치합니다. |
| **[!UICONTROL 자연어 검색 검색 규칙과 일치]** | 히트가 인식된 검색 엔진에서 시작되었으며 유료 검색 감지 규칙과 일치하지 않습니다. |
| **[!UICONTROL 레퍼러가 내부 URL 필터와 일치함]** | 히트에 [내부 URL 필터](/help/components/dimensions/referrer.md)와 일치하는 [레퍼러](../general/internal-url-filter-admin.md)이(가) 포함되어 있습니다. |
| **[!UICONTROL 레퍼러가 내부 URL 필터와 일치하지 않음]** | 히트에 내부 URL 필터와 일치하지 않는 레퍼러가 포함되었습니다. |
| **[!UICONTROL 방문의 첫 번째 히트임]** | 방문에서 히트가 첫 번째였습니다. |
| **[!UICONTROL 레퍼러가 소셜 네트워크임]** | [레퍼러 유형](/help/components/dimensions/referrer-type.md)이(가) &quot;소셜 네트워크&quot;입니다. |
| **[!UICONTROL 레퍼러가 소셜 네트워크가 아닙니다]** | 레퍼러 유형이 &quot;소셜 네트워크&quot;가 아닙니다. |
| **[!UICONTROL 레퍼러가 대화형 AI입니다]** | 레퍼러 유형은 &quot;대화형 AI&quot;입니다. |
| **[!UICONTROL 레퍼러가 대화형 AI가 아닙니다]** | 레퍼러 유형이 &quot;대화형 AI&quot;가 아닙니다. |

**히트 특성**&#x200B;을(를) 사용하면 차원, 일치하는 연산자 및 찾을 값을 지정할 수 있습니다.

| 히트 속성 조건 | 설명 |
|---|---|
| **[!UICONTROL 페이지]** | [페이지](/help/components/dimensions/page.md) 차원. |
| **[!UICONTROL 페이지 도메인]** | URL의 도메인입니다. (예: `products.example.com`) |
| **[!UICONTROL 페이지 도메인 및 경로]** | URL의 도메인 및 경로입니다. (예: `products.example.com/mens/pants/overview.html`) |
| **[!UICONTROL 페이지 루트 도메인]** | URL의 루트 도메인입니다. (예: `example.co.uk`) |
| **[!UICONTROL 페이지 URL]** | 전체 페이지 URL. |
| **[!UICONTROL 쿼리 문자열 매개 변수]** | 페이지 URL의 개별 쿼리 문자열 매개 변수입니다. 규칙 조건당 하나의 쿼리 문자열 매개 변수를 사용합니다. 규칙에 여러 쿼리 문자열 매개 변수를 포함하려면 여러 규칙 조건을 사용하십시오. |
| **[!UICONTROL 레퍼러]** | [레퍼러](/help/components/dimensions/referrer.md) 차원. |
| **[!UICONTROL 참조 도메인]** | [참조 도메인](/help/components/dimensions/referring-domain.md) 차원. |
| **[!UICONTROL 참조 도메인 및 경로]** | 참조 도메인과 레퍼러의 URL 경로의 연결. 예: `www.example.com/products/id/12345` 또는 `ad.example.com/foo`. |
| **[!UICONTROL 참조 매개 변수]** | 레퍼러 내의 쿼리 문자열 매개 변수입니다. |
| **[!UICONTROL 참조 루트 도메인]** | 참조 루트 도메인. |
| **[!UICONTROL 검색 엔진]** | [검색 엔진](/help/components/dimensions/search-engine.md) 차원. |
| **[!UICONTROL 검색 키워드]** | [검색 키워드](/help/components/dimensions/search-keyword.md) 차원. |
| **[!UICONTROL 검색 엔진 + 검색 키워드]** | 검색 엔진과 검색 키워드의 연결. |
| **[!UICONTROL AMO ID]** | Adobe Advertising 및 Advertising Analytics 통합에서 사용하는 기본 추적 코드. 이러한 통합 중 하나가 활성화되면 추적 코드 접두사를 사용하여 Advertising 특정 채널을 식별할 수 있습니다. &quot;AL&quot;로 시작하는 값은 검색 및 소셜에 사용됩니다. &quot;AC&quot;로 시작하는 값은 표시용입니다. AMO ID를 마케팅 채널에서 사용하면 클릭/비용/노출 지표가 올바른 채널에 귀속될 수 있습니다. |
| **[!UICONTROL AMO EF ID]** | Adobe Advertising에서 사용하는 보조 추적 코드. Advertising으로 데이터를 다시 전송하는 키 역할을 합니다. 디스플레이 클릭스루와 디스플레이 뷰스루를 두 개의 개별 마케팅 채널로 식별하는 데 사용할 수 있습니다. 이렇게 하려면 디스플레이 클릭스루의 경우 &quot;AMO EF ID&quot;가 `:d`(으)로 끝나거나 디스플레이 뷰스루의 경우 &quot;AMO EF ID&quot;가 `:i`(으)로 끝나도록 마케팅 채널 논리를 설정합니다. 디스플레이를 두 개의 채널로 분할하지 않으려면 AMO ID 차원을 대신 사용하십시오. |

**전환 변수**&#x200B;를 사용하면 사용자 지정 eVar, 일치하는 연산자 및 찾을 값을 지정할 수 있습니다.

| 전환 변수 조건 | 설명 |
|---|---|
| **eVar 1-250** | 연결된 [eVar](/help/components/dimensions/evar.md) 차원입니다. |
