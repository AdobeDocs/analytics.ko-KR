---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# zip

변수  및  은(는) 전환 변수입니다.

<!-- 

zip.xml

 -->

이벤트를 캡처한다는 점은 eVar와 비슷하지만 지속되지 않는다는 점은 eVar와 다릅니다. The *`zip`* 및 *`state`* 변수는 즉시 만료되는 eVar와 같습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 50바이트 | zip | 전환 &gt; 방문자 프로필 &gt; Zip/우편 번호 | "" |

Since the *`state`* and *`zip`* variables expire immediately, the only events associated with them are events fired on the same page that are populated. 예를 들어 *`zip`*&#x200B;를 사용하여 우편번호별 전환율을 비교하려면 체크아웃 프로세스의 모든 페이지에서 *`zip`*&#x200B;을 채워야 합니다. 청구 주소를 우편번호에 대한 소스로 사용하는 것이 좋습니다. 대신 배송 주소를 사용하도록 선택할 수도 있습니다(주문에 대해 배송 주소가 하나만 있다고 가정할 경우). 미디어 사이트는 등록이나 광고 클릭스루  추적에 *`zip`* 및 *`state`*&#x200B;를 사용하도록 선택할 수 있습니다.

**구문 및 가능한 값** {#section_5EDCFCAC8FC241D1B4CC777996858CD7}

```js
s.zip="zip_code"
```

*`zip`* 변수에는 값 또는 형식 제한이 적용되지 않습니다. *`zip`*&#x200B;에는 표준 변수 제한 외에는 제한이 없습니다.

**예** {#section_F25C0D0CC3C04B81892A662CD605C593}

```js
s.zip="92806"
```

```js
s.zip="92806-4115"
```

**구성 설정** {#section_7987084EECC34DD38B643B94F82385CA}

없음

**함정, 질문 및 팁** {#section_E86774D5CE8B40EFA36353CDEE3A84D0}

* 관련 이벤트를 실행하는 모든 페이지(예: 체크아웃 프로세스의 각 페이지)에서 [!UICONTROL zip]을 채우십시오(체크아웃 프로세스의 각 페이지).
* *`zip`* 및 *`state`* 변수는 페이지 보기에서 만료되는 eVar처럼 작동합니다.

