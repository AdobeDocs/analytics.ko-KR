---
title: AMO 메타 광고 클릭 ID
description: Adobe Advertising 통합에 사용되는 Adobe Media Optimizer Meta 광고 클릭 ID.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 10%

---

# AMO 메타 광고 클릭 ID

**[!UICONTROL AMO Meta 광고 클릭 ID]**&#x200B;은(는) Adobe Advertising 통합에 사용되는 광고 클릭 식별자입니다. [Analytics for Advertising](https://experienceleague.adobe.com/ko/docs/advertising/integrations/analytics/overview) 통합을 사용하도록 설정하면 차원이 자동으로 만들어집니다. 주로 사람이 읽을 수 있는 보고 차원이 아닌 원시 추적 식별자로 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 여러 가지 방법으로 값을 수집합니다.

* 클릭스루 트래픽의 경우 일반적으로 광고 기반 트래픽이 사이트로 들어오는 페이지에서 `fbclid`페이지 URL[의 &#x200B;](page-url.md) 쿼리 문자열 매개 변수에서 데이터가 수집됩니다.
* URL에 추적 코드가 포함되어 있지 않지만 Adobe Advertising JavaScript이 이전 2분 내에 클릭을 감지하면 클릭스루 트래픽을 캡처할 수도 있습니다.

## 차원 항목

Dimension 항목에는 Meta(Facebook) 광고 네트워크에서 생성한 광고 클릭 식별자가 포함됩니다. 이러한 해시된 값의 길이는 다를 수 있지만, 일반적으로 수백 자의 길이입니다. 예(잘림) 값은 다음과 같습니다.

```text
IwY2xjawP0bVtleHRuA2FlbQIxMAB[...]AVp_aem_l5TPw-muraFjBGOq8l1w0g
PAb21jcAQB1LNleHRuA2FlbQIxMQB[...]PoFocE1FH44g_aem_FNMJG5EydJ_59aBwKIf4uA
```
