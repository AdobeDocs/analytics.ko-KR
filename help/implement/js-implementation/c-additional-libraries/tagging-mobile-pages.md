---
description: 모바일 추적 코드는 서버가 생성한 이미지 태그의 형태로 페이지에 삽입됩니다.
keywords: Analytics 구현; 모바일 추적; 모바일 프로토콜; 캐싱 방지; alt 태그; 기본 이미지 유형
seo-description: 모바일 추적 코드는 서버가 생성한 이미지 태그의 형태로 페이지에 삽입됩니다.
seo-title: 모바일 프로토콜에 대한 페이지 태깅
solution: Analytics
title: 모바일 프로토콜에 대한 페이지 태깅
topic: 개발자 및 구현
uuid: 5788 BEAF-F 309-4918-A 99 C-A 3 E 591668205
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 모바일 프로토콜에 대한 페이지 태깅

모바일 추적 코드는 서버가 생성한 이미지 태그의 형태로 페이지에 삽입됩니다.

모바일 추적 코드는 서버가 생성한 이미지 태그의 형태로 페이지에 삽입됩니다. JavaScript나 WMLScript 같은 스크립팅 언어는 일반적으로 모바일 장치 간에 지원되지 않으므로 스크립팅 언어를 통해 추적 비콘을 동적으로 생성할 수 없습니다.

· 모바일 비콘 이미지는 실제로 2x2 픽셀이지만 모든 모바일 장치 지원을 위해 높이와 폭 속성을 5로 설정해야 합니다. 예:

```
<img sr c="https://metric.mydomain.com/b/ss/<Report_Suite_Name>/5/<random_number>?pageName=" alt="" width="5" height="5"/>
```

## 무작위 번호를 사용한 캐시 방지 {#section_BF5C344A16034C439C8704632CF673A7}

Adobe 서버가 브라우저로 하여금 추적 비콘을 캐시하지 않도록 지시해도, 일부 브라우저는 이 지침을 따르지 않을 수 있습니다. 비콘의 캐시를 추가로 방지하려면, 웹 서버가 이미지 URL 경로에서 무작위 번호를 동적으로 생성하는 것이 좋습니다. 이렇게 하면 보고의 정확도가 높아집니다. 무작위 번호는 아래에서 보듯이 경로의 마지막 섹션에 있어야 합니다.

```js
<img src="https://rsid.112.2O7.net/b/ss/rsid/5/H.5--WAP/12345?pageName=" />.
```

## ALT 태그 포함 {#section_FBD8B2FD1EA0429580C2B933DA300B07}

일부 모바일 브라우저의 경우 모든 이미지는 이미지 태그에 alt 텍스트를 포함해야 합니다. 다음은 ALT 속성이 어떻게 이미지 태그에 나타나야 하는지를 보여 줍니다.

```js
<img src="https://rsid.112.2O7.net/b/ss/rsid/5/H.5--WAP/12345?pageName=" alt=""/>.
```

경로에 /5/가 항상 올바로 나타나는 것이 중요합니다. /5/는 Adobe 서버에서 모바일 장치를 식별하는 데 사용됩니다. 표준 /1/을 사용하는 경우, Adobe 서버는 모바일 장치에서 쿠키 설정을 시도합니다.

## 기본 이미지 형식 변경 {#section_2F969909010D4A64BF6E092A32ABADB7}

특정 장치에서 기본 이미지 형식이 지원되지 않는 경우 데이터가 반환되지 않습니다. 이를 방지하기 위해 강제로 Adobe 데이터 수집 서버가 해당 모바일 장치에서 지원되는 특정 그래픽 유형을 반환하도록 할 수 있습니다. 보고서 세트 이름 뒤의 코드가 이미지 형식을 지정합니다.

* `/5/` 기본 이미지 유형을 반환합니다.
* `/5.1/` 또는 `/1/` 항상 GIF 이미지를 반환합니다.

* `/5.5/` 항상 WBMP 이미지를 반환합니다.

See [Identifying Visitors using Mobile Protocols](../../../implement/js-implementation/c-unique-visitors/visid-mobile.md#concept_8C5557634014440AA3588FBB0CF6BB49).
