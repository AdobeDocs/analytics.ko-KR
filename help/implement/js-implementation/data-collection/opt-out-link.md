---
description: 옵트아웃 링크를 지정하고 링크에 대한 브랜딩을 사용자 지정합니다. 웹 사이트 방문자는 데이터 수집 도메인의 옵트아웃 페이지를 방문하여 Adobe의 분석 제품에서 자신의 활동을 추적하지 않도록 선택할 수 있습니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Troubleshooting
title: 옵트아웃 링크 추가
topic: Developer and implementation
uuid: c12092be-3be7-4621-b838-d6b78d074f84
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 옵트아웃 링크 추가

옵트아웃 링크를 지정하고 링크에 대한 브랜딩을 사용자 지정합니다. 웹 사이트 방문자는 데이터 수집 도메인의 옵트아웃 페이지를 방문하여 Adobe의 분석 제품에서 자신의 활동을 추적하지 않도록 선택할 수 있습니다.

사용자가 추적되지 않도록 선택하고 옵트아웃 쿠키가 설정된 경우 JavaScript 파일이 계속해서 Adobe 서버로 데이터를 보내지만 데이터가 처리되거나 보고되지 않습니다.

URL 구조에서 collection_domain 섹션이 JavaScript 파일에서 사용되는 trackingServer입니다. Adobe Analytics 구현에 사용된 수집 도메인은 Adobe Analytics 테이블의 첫 번째 행에 있는 DigitalPulse 디버거에서 볼 수 있습니다. 이 행에서는 구현에 따라 "퍼스트 파티 쿠키" 또는 "타사 쿠키"로 레이블이 지정됩니다. 웹 사이트에 대한 컬렉션 도메인은 2o7.net, omtrdc.net 또는 metrics.example.com과 같은 웹 사이트 도메인을 포함할 수 있습니다.

방문자가 옵트아웃 페이지의 링크를 클릭하여 옵트아웃하면 브라우저에서 쿠키가 설정됩니다. 적용 가능한 추적 도메인에 대한 `omniture_optout` 쿠키가 있으면 사용자의 활동이 Adobe Analytics로 보고되지 않습니다. 옵트아웃 쿠키에 자체 링크를 제공하거나 아래 단계에 따라 옵트아웃 쿠키를 설정할 수 있습니다.

Adobe는 모든 구현 유형에 대해 옵트아웃을 제공합니다. 귀하는 자체 개인정보 보호정책과 서명한 약관 준수 유지에 대한 책임을 져야 합니다. 여기 설명한 것과 같이 옵트아웃 페이지에 대한 링크가 구현 유형을 기준으로 변화함을 확인하십시오.

Adobe Analytics 제품 및 서비스를 Adobe가 소유한 도메인(예: 207.net 또는 omtrdc.net)에 설정된 쿠키와 함께 구현하는 경우 Adobe Analytics 제품 및 서비스를 위해 Adobe 쿠키를 사용하는 모든 사이트에 대해 웹 사이트 방문자를 [Adobe Privacy Center](https://www.adobe.com/privacy/opt-out.html)에 제공된 옵트아웃 메커니즘으로 안내할 수 있습니다. Adobe 옵트아웃 메커니즘으로 직접 연결되는 링크는 `https:// *collection_domain* /optout.html`입니다.

More information about Adobe Analytics privacy practices can be found at [https://www.adobe.com/privacy/advertising-services.html](https://www.adobe.com/privacy/advertising-services.html).

* [옵트아웃 페이지 URL 구조](/help/implement/js-implementation/data-collection/opt-out-link.md#section_E0462428D2E440E7863E24D2F6DBF748)
* [옵트아웃 URL 예제](/help/implement/js-implementation/data-collection/opt-out-link.md#section_258DE5226AA0483CA790D2C9C5318B2E)
* [옵트아웃 URL 브랜딩](/help/implement/js-implementation/data-collection/opt-out-link.md#section_674AB62E810B414AB8F1615C0E3061F8)

## 옵트아웃 페이지 URL 구조 {#section_E0462428D2E440E7863E24D2F6DBF748}

옵트아웃 페이지는 다음 URL에 있습니다.

```
https://collection_domain/optout.html[?optional_parameters]
```

`optional_parameters`에는 다음이 포함되어 있습니다.

`locale=[code]`: 번역된 옵트아웃 페이지를 제공합니다. 지원되는 로케일:

* en_US(기본값)
* de_DE
* es_ES
* fr_FR
* jp_JP
* ko_KR
* zh_CN
* zh_TW

`popup=1`:페이지를 팝업으로 취급하고 "창 닫기" 단추를 제공합니다.

## 옵트아웃 URL 예제 {#section_258DE5226AA0483CA790D2C9C5318B2E}

클릭하면 방문자가 metrics.example.com에서 추적되지 않도록 하는 링크를 포함한 전체 창으로 열리는 영어 웹 페이지:

```
https://metrics.example.com/optout.html
```

클릭하면 방문자가 example.d3.sc.omtrdc.net에서 추적되지 않도록 하는 링크를 포함한 전체 창으로 열리는 프랑스어 웹 페이지:

```
https://example.d3.sc.omtrdc.net/optout.html?locale=fr_FR
```

클릭하면 방문자가 example.112.2o7.net에서 추적되지 않도록 하는 링크를 포함한 전체 창으로 열리는 독일어 웹 페이지:

```
https://example.112.2o7.net/optout.html?popup=1&locale=de_DE
```

## 옵트아웃 URL 브랜딩 {#section_674AB62E810B414AB8F1615C0E3061F8}

웹 사이트의 어딘가에서 다음과 같은 링크를 제공할 수 있습니다.

```
 <a href=" https://stats.adobe.com/optout.html?optout=1&confirm_change=1">
Click Here to Opt Out! </a>
```

  *`stats.adobe.com`*&#x200B;은 *`s.trackingServer`* 변수가 설정된 항목으로 대체됩니다.

또한 옵트인에 링크를 제공하려면 동일한 URL을 사용하되, `?optout=1`을 `?optin=1`로 바꾸고 `confirm_change=1`을 유지합니다.
