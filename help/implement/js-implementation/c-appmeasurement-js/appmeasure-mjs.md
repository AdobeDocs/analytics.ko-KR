---
description: JavaScript 용 AppMeasurement는 s_code.js와 동일한 핵심 기능을 제공하면서도, 모바일 사이트와 데스크탑 사이트 모두에서 사용할 수 있는 보다 가볍고 빠른 새로운 라이브러리입니다.
keywords: appmeasurement;Analytics 구현;javascript;javascript에 대한 appmeasurement;초기화;appmeasurement 인스턴스 검색;clear vars;clearvars;appmeasurement 유틸리티;appmeasurement 인스턴스;appmeasurement 이점
seo-description: JavaScript 용 AppMeasurement는 s_code.js와 동일한 핵심 기능을 제공하면서도, 모바일 사이트와 데스크탑 사이트 모두에서 사용할 수 있는 보다 가볍고 빠른 새로운 라이브러리입니다.
seo-title: JavaScript용 AppMeasurement 정보
solution: Analytics
subtopic: JavaScript AppMeasurement
title: JavaScript용 AppMeasurement 정보
topic: 개발자 및 구현
uuid: dc71ad7a-92bd-40cd-8fab-707f6f8472e2
translation-type: ht
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# JavaScript용 AppMeasurement 정보

JavaScript 용 [!DNL AppMeasurement]는 s_code.js의 핵심 기능과 동일한 기능을 제공하면서도, 모바일 사이트와 데스크탑 사이트에서 모두 사용할 수 있는 보다 가볍고 빠른 새로운 라이브러리입니다.

## 마이그레이션하기 전에 알아야 할 사항 {#section_B8E7B39E8469468883BA0B41234F21C4}

다음은 새로운 [!DNL AppMeasurement] 버전으로 전환하기 전에 알고 있어야 하는 변경 사항입니다.

* 일부 플러그인은 더 이상 지원되지 않습니다. [AppMeasurement 플러그인 지원](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A)을 참조하십시오.
* 라이브러리는 동적 계정 선택([dynamicAccountList](/help/implement/js-implementation/c-variables/configuration-variables.md), [dynamicAccountMatch](/help/implement/js-implementation/c-variables/configuration-variables.md) 및 [dynamicAccountSelection](/help/implement/js-implementation/c-variables/configuration-variables.md))을 지원하지 않습니다.

* 라이브러리와 페이지 코드는 `<head>` 태그 내에 배포할 수 있습니다.
* 미디어 및 통합 모듈은 JavaScript [!DNL AppMeasurement] 다운로드 패키지에 있는 업데이트된 모듈 코드를 사용하여 지원됩니다. 설문 조사 모듈은 지원되지 않습니다.
* 기존 페이지 코드가 새 버전과 호환됩니다.
* 라이브러리에서는 쿼리 매개 변수를 가져오고, 쿠키를 읽고 쓰고, 고급 링크 추적을 수행하는 기본 유틸리티를 제공합니다.

## FAQ {#section_9BD41B08F7B54197B230937714B9357A}

성능, 비디오 추적, 모바일 등에 대한 자세한 내용은 [FAQ](../../../implement/faq.md#concept_9BBC230E01114318BE9C08724F2040D3)를 참조하십시오.

## 초기화 프로세스 {#section_F6D5680F6D134B6AB1F01C6235860635}

`s_gi()`를 호출하여 보고서 세트 ID를 전달함으로써 [!DNL AppMeasurement] 인스턴스를 초기화합니다.

```js
var s_account="INSERT-RSID-HERE"
var s=s_gi(s_account)
```

`s_gi`이 호출되면 [!DNL AppMeasurement] 인스턴스가 지정된 `s_account`에 없을 경우 새 인스턴스가 생성됩니다. 그렇지 않으면 기존 인스턴스가 반환됩니다. 이것은 동일 계정에 복제 개체를 만들지 않도록 하는 데 유용합니다.

## AppMeasurement 인스턴스 가져오기 {#section_6F05C96DCAB24C8C9B4B91C5739630A6}

코드 전체에서 전역 [s_gi() 함수](../../../implement/js-implementation/function-s-gi.md#concept_50EE6629F61A478BB67781408FBA04BD)를 호출하여 기존 [!DNL AppMeasurement] 인스턴스를 검색합니다.

## 유틸리티 {#section_0F47694DD0214645A24C94AB6A4142A0}

JavaScript [!DNL AppMeasurement]는 다음의 기본 제공 유틸리티를 제공합니다.

* [Util.cookieRead](../../../implement/js-implementation/util-cookieread.md#concept_33BD774A90504F2C8094DDC16D47440D)
* [Util.cookieWrite](../../../implement/js-implementation/util-cookiewrite.md#concept_9BE4F7D9CDAE4445B9AF3212BC7E61F2)
* [Util.getQueryParam](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5)

## Clear Vars {#section_597C411E7EDB42BC9A6A0508C9D57147}

새 `clearVars` 메서드는 인스턴스 개체에서 다음 값을 지우는 데 사용할 수 있습니다.

* `props`
* `eVars`
* `hier`
* `list`
* `events`
* `eventList`
* `products`
* `productsList`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

예:

```js
s.clearVars()
```

## 이점 {#section_091E5A28E89E438E8A54A95F55165743}

* H.25 코드보다 3~7배 더 빠릅니다.
* 21k만 압축 해제되어 있고 8k는 gzip이 사용되었습니다(H.25 코드는 33k 압축 해제되어 있고 13k gzip이 사용됨).
* 몇 가지 일반적인 플러그인()에 대한 기본 지원을 제공합니다.
* 모바일 사이트에서 사용할 수 있을 만큼 작고 빠르고 데스크톱 웹에서 사용할 수 있을 만큼 강력하므로, 모든 웹 환경에서 단일 라이브러리를 사용할 수 있습니다.

