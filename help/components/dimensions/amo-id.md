---
title: AMO ID
description: Adobe Advertising 통합에 사용되는 Adobe Media Optimizer ID.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 3%

---

# AMO ID

**[!UICONTROL AMO ID]**&#x200B;은(는) Adobe Advertising 통합에서 사용되는 연결된 식별자의 컬렉션입니다. 이 차원에 저장된 값은 Analytics 보고에서 사용하기 위해 사람이 인식할 수 있는 별도의 분류 차원으로 자동 구성됩니다. [Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview) 통합을 사용하도록 설정하면 차원이 자동으로 만들어집니다.

## 이 차원을 데이터로 채우기

이 차원은 여러 가지 방법으로 값을 수집합니다.

* 클릭스루 트래픽의 경우 일반적으로 광고 기반 트래픽이 사이트로 들어오는 페이지에서 `s_kwcid`페이지 URL[의 &#x200B;](page-url.md) 쿼리 문자열 매개 변수에서 데이터가 수집됩니다.
* URL에 추적 코드가 포함되어 있지 않지만 Adobe Advertising JavaScript이 이전 2분 내에 클릭을 감지하면 클릭스루 트래픽을 캡처할 수도 있습니다.
* 지원되는 뷰스루 트래픽의 경우 Adobe Advertising에서 보충 ID(`SDID`)를 사용하여 백엔드의 값을 보완합니다.

## 차원 항목

Dimension 항목에는 `s_kwcid` 값이라고도 하는 AMO ID가 포함되어 있습니다. 정확한 형식은 트래픽이 DSP에서 시작되었는지 또는 검색, 소셜 및 Commerce에서 시작되었는지에 따라 다릅니다. AMO ID는 EF ID보다 세분화되지 않으며 주로 Analytics에서 Adobe Advertising 지표를 분류하고 수집하는 데 사용됩니다.

### DSP

```text
AC!{ad key}!{placement key}
```

* **`AC`**: 표시 채널을 나타냅니다.
* **`ad key`**: 광고에 대해 Adobe Advertising에서 생성한 영숫자 식별자입니다.
* **`placement key`**: 배치에 대해 Adobe Advertising에서 생성한 영숫자 식별자입니다.

예제 값:

```text
AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7
```

### 검색, 소셜 및 Commerce 광고

검색, 소셜 및 Commerce AMO ID는 `AL`(으)로 시작하고 광고주 사용자 ID, 광고 네트워크 계정 ID, 네트워크별 식별자가 그 뒤에 옵니다. 공유 광고 네트워크 계정 ID는 다음과 같습니다.

* **`3`**: Google 광고
* **`10`**: Microsoft Advertising
* **`45`**: Meta
* **`86`**: Yahoo! 네트워크 표시
* **`87`**: 네이버
* **`88`**: Baidu
* **`90`**: Yandex
* **`94`**: Yahoo! 일본 광고
* **`105`**: Yahoo 네이티브(더 이상 사용되지 않음)
* **`106`**: Pinterest(더 이상 사용되지 않음)

#### Google Ads

Google Ads는 두 가지 관련 형식을 사용합니다. 최신 계정에는 성과 최대 및 초안/실험 캠페인에 대한 캠페인 및 광고 그룹 수준 보고를 지원하는 캠페인 ID와 광고 그룹 ID가 포함될 수 있습니다.

```text
AL!{user}!3!{creative}!{matchtype}!{placement}!{network}!{product partition}!{keyword}[!{campaign id}!{ad group id}]
```

* **`creative`**: Google Ads 광고 크리에이티브 ID.
* **`matchtype`**: 키워드 일치 유형(`e` 정확한 경우, `p` 구, `b` 광범위한 경우).
* **`placement`**: 광고를 클릭한 도메인입니다.
* **`network`**: 클릭이 발생한 네트워크(Google 검색의 경우 `g`, 검색 파트너의 경우 `s`, 표시의 경우 `d`).
* **`product partition`**: 제품 광고에 대한 제품 그룹 ID입니다.
* **`keyword`**: 검색 사이트에서 키워드를 트리거하거나 컨텐츠 사이트에서 일치하는 키워드를 트리거합니다.
* **`campaign id`**: Google 광고 캠페인 ID(있는 경우).
* **`ad group id`**: Google 광고 그룹 ID(있는 경우).

동적 검색 광고의 경우 키워드 필드가 자동 타겟으로 채워집니다.

예:

```text
AL!1234!3!569345525675!e!!g!!adobe express!15557590691!136734402131
```

#### Microsoft Advertising

```text
AL!{user}!10!{ad id}!!!!{keyword/order item id}!!{campaign id}!{ad group id}
```

* **`ad id`**: Microsoft Advertising 광고 ID.
* **`keyword/order item id`**: Microsoft Advertising 키워드 ID.
* **`campaign id`**: Microsoft Advertising 캠페인 ID.
* **`ad group id`**: Microsoft Advertising 광고 그룹 ID.

일부 마이그레이션되지 않은 계정에 대해 이전 Microsoft 형식이 계속 존재할 수 있습니다.

예:

```text
AL!1234!10!79577297926903!!!!79577437127536!!291647087!1273234845019564
```

#### 바이두

```text
AL!{user}!88!{creative}!{placement}!{keyword id}
```

* **`creative`**: Baidu Creative ID입니다.
* **`placement`**: 광고를 클릭한 웹 사이트입니다.
* **`keyword id`**: Baidu 키워드 ID입니다.

#### Yahoo! 일본 광고

```text
AL!{user}!94!{creative}!{matchtype}!{network}!{keyword}
```

* **`creative`**: Yahoo! Japan Ads 광고 ID.
* **`matchtype`**: 키워드 일치 유형(`be` exact, `bp` phrase, `bb` broad).
* **`network`**: 클릭이 발생한 네트워크(`n` 기본, `s` 검색).
* **`keyword`**: 키워드를 트리거하는 중입니다.

#### 얀덱스

```text
AL!{user}!90!{ad id}!{source type}!!!{phrase id}
```

* **`ad id`**: Yandex 광고 ID.
* **`source type`**: 광고가 표시된 사이트 유형(`b` 검색, `c` 컨텍스트/콘텐츠, `ct` 범주).
* **`phrase id`**: Yandex 키워드 ID.

## 분류

[Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview) 통합을 사용하도록 설정하면 다음 분류가 자동으로 만들어집니다. 분류 값은 통합에 의해 자동으로 유지 관리됩니다.

| 분류 | 설명 | DSP | 검색,<br>소셜, 및<br>Commerce |
| --- | --- | :---: | :---: |
| **[!UICONTROL 계정]** | 계정 이름. | &check; | &check; |
| **[!UICONTROL 광고 표시 URL]** | 광고에 표시되는 URL. | | &check; |
| **[!UICONTROL 광고 설명]** | 광고 설명(DSP) 또는 광고 본문(검색, 소셜 및 Commerce)입니다. | &check; | &check; |
| **[!UICONTROL 광고 대상 URL]** | 광고의 대상 URL입니다. | | &check; |
| **[!UICONTROL 광고 그룹]** | 광고 그룹 이름입니다. | | &check; |
| **[!UICONTROL 광고 플랫폼]** | 광고 DSP 또는 검색 엔진 이름. | &check; | &check; |
| **[!UICONTROL 광고 제목]** | 광고 유형(DSP) 또는 광고 제목(검색, 소셜 및 Commerce)입니다. | &check; | &check; |
| **[!UICONTROL 광고 유형]** | 광고 유형(예: `text`, `video`, `display` 또는 `native`). | &check; | &check; |
| **[!UICONTROL AdCloud 특성 1]** -<br>**[!UICONTROL AdCloud 특성 5 &#x200B;]** | 향후 사용자 지정 속성에 예약된 자리 표시자 분류. 현재 사용되지 않습니다. | | |
| **[!UICONTROL Campaign]** | 캠페인 이름. | &check; | &check; |
| **[!UICONTROL Creative 경험 이름]** | 테스트 또는 개인화에 사용된 크리에이티브 변형 그룹을 나타내는 광고 상호 작용과 연관된 크리에이티브 경험의 이름입니다. | &check; | |
| **[!UICONTROL Creative 분기 이름]** | 크리에이티브 실험의 특정 변형 또는 경로를 나타내는 크리에이티브 경험 내의 분기 이름. | &check; | |
| **[!UICONTROL Creative 분기 ID]** | 크리에이티브 경험 내의 크리에이티브 분기에 할당된 고유 식별자. | &check; | |
| **[!UICONTROL Creative 이름]** | 사용자에게 제공된 특정 광고 크리에이티브 에셋의 이름입니다. | &check; | |
| **[!UICONTROL Creative 변형 이름]** | 크리에이티브 경험 또는 분기 내에서 사용되는 크리에이티브의 특정 변형 이름. | &check; | |
| **[!UICONTROL 키워드]** | 키워드. | | &check; |
| **[!UICONTROL 키워드 일치 유형]** | 키워드 및 일치 유형입니다. | | &check; |
| **[!UICONTROL 랜딩 유형]** | 랜딩 페이지 항목이 뷰스루인지 또는 클릭스루인지 여부를 나타냅니다. | &check; | &check; |
| **[!UICONTROL 일치 유형]** | 검색 일치 유형입니다. | | &check; |
| **[!UICONTROL 네트워크]** | RTB(DSP) 또는 광고 네트워크 이름(검색, 소셜 및 Commerce)입니다. | &check; | &check; |
| **[!UICONTROL 최적화]** | 패키지 이름(DSP) 또는 포트폴리오 이름(검색, 소셜 및 Commerce)입니다. | &check; | &check; |
| **[!UICONTROL 배치]** | 배치 이름입니다. | &check; | |
| **[!UICONTROL 제품 대상]** | 제품 목록 광고에 대한 제품 타겟. | | &check; |
