---
description: JavaScript 용 AppMeasurement는 s_code.js와 동일한 핵심 기능을 제공하면서도, 모바일 사이트와 데스크탑 사이트 모두에서 사용할 수 있는 보다 가볍고 빠른 새로운 라이브러리입니다.
keywords: Appmeasurement; Analytics 구현; Javascript; Javascript 용 appmeasurement; 초기화; Appmeasurement 인스턴스 검색; var 지우기; Clearvars; Appmeasurement Utilities; Appmeasurement 인스턴스; Appmeasurement 이점
seo-description: JavaScript 용 AppMeasurement는 s_code.js와 동일한 핵심 기능을 제공하면서도, 모바일 사이트와 데스크탑 사이트 모두에서 사용할 수 있는 보다 가볍고 빠른 새로운 라이브러리입니다.
seo-title: JavaScript용 AppMeasurement 정보
solution: Analytics
subtopic: JavaScript AppMeasurement
title: JavaScript용 AppMeasurement 정보
topic: 개발자 및 구현
uuid: dc 71 ad 7 a -92 bd -40 cd -8 fab -707 f 6 f 8472 e 2
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# JavaScript용 AppMeasurement 정보

[!DNL AppMeasurement] JavaScript는 s_ code. js의 동일한 핵심 기능을 제공하면서도 모바일 사이트와 데스크탑 사이트 모두에서 사용할 수 있는 보다 가볍고 빠른 새 라이브러리입니다.

## 마이그레이션하기 전에 알아야 할 사항 {#section_B8E7B39E8469468883BA0B41234F21C4}

The following list contains changes you need to understand before switching to this new [!DNL AppMeasurement] version:

* 일부 플러그인은 더 이상 지원되지 않습니다. [Appmeasurement 플러그인 지원을 참조하십시오](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A).
* The library does not support dynamic account selection ([dynamicAccountList](/help/implement/js-implementation/c-variables/configuration-variables.md), [dynamicAccountMatch](/help/implement/js-implementation/c-variables/configuration-variables.md), and [dynamicAccountSelection](/help/implement/js-implementation/c-variables/configuration-variables.md)).

* The library and page code can be deployed inside the `<head>` tag.
* The Media and Integrate modules are supported using updated module code that is in the JavaScript [!DNL AppMeasurement] download package. 설문 조사 모듈은 지원되지 않습니다.
* 기존 페이지 코드가 새 버전과 호환됩니다.
* 라이브러리에서는 쿼리 매개 변수를 가져오고, 쿠키를 읽고 쓰고, 고급 링크 추적을 수행하는 기본 유틸리티를 제공합니다.

## FAQ {#section_9BD41B08F7B54197B230937714B9357A}

See the [FAQ](../../../implement/faq.md#concept_9BBC230E01114318BE9C08724F2040D3) for information about performance, video tracking, mobile, and more.

## 초기화 프로세스 {#section_F6D5680F6D134B6AB1F01C6235860635}

Call `s_gi()`, passing the report suite ID to initialize an [!DNL AppMeasurement] instance:

```js
var s_account="INSERT-RSID-HERE"
var s=s_gi(s_account)
```

When `s_gi` is called, if an [!DNL AppMeasurement] instance does not exist for the specified `s_account`, a new instance is created. 그렇지 않으면 기존 인스턴스가 반환됩니다. 이것은 동일 계정에 복제 개체를 만들지 않도록 하는 데 유용합니다.

## AppMeasurement 인스턴스 가져오기 {#section_6F05C96DCAB24C8C9B4B91C5739630A6}

Throughout your code, call the global [s_gi() function](../../../implement/js-implementation/function-s-gi.md#concept_50EE6629F61A478BB67781408FBA04BD) to retrieve an existing [!DNL AppMeasurement] instance.

## 유틸리티 {#section_0F47694DD0214645A24C94AB6A4142A0}

JavaScript [!DNL AppMeasurement] provides the following built-in utilities:

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

