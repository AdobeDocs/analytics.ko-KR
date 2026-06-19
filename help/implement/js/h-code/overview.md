---
title: H 코드 JavaScript 구현 개요
description: 사이트에서 H 코드를 구현하는 워크플로에 대해 알아봅니다.
feature: Implementation Basics
exl-id: cf83d8fe-a3b1-4e65-a86a-7eeaf555651b
role: Developer
TQID: 'https://experienceleague.adobe.com/-d3QyBm0RW5arsRHNHY4ov7YJxVFZrNdvXhVIuU6Ih4'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 385
ht-degree: 77%

---

# H 코드 JavaScript 구현 개요

>[!IMPORTANT]
>
>이 버전의 데이터 수집은 더 이상 지원되지 않습니다. [Adobe Experience Platform의 태그](../../launch/overview.md) 또는 [JavaScript용 AppMeasurement](../overview.md)로 업그레이드하십시오.

데이터를 수집하기 위해 코드가 있는 페이지를 성공적으로 구현하려면 호스팅 서버에 액세스할 수 있어야 합니다. 다음은 기초 Analytics H 코드 구현 단계입니다.

>[!NOTE]
>
>이 지침을 따르려면 이미 `s_code.js`의 기존 복사본을 가지고 있어야 합니다. Adobe는 더 이상 코드 관리자에서 H 코드를 다운로드할 수 있는 옵션을 제공하지 않습니다.

1. **코어 JS 파일 변수 업데이트**: `s_code.js` 파일을 편집하고 다음 변수가 업데이트되었는지 확인합니다.
   * `s_account`에는 전송하는 데이터를 받을 보고서 세트 ID가 포함되어 있습니다.
   * `s.trackingServerSecure`에는 위치 쿠키가 저장되어 있습니다.
1. **사이트에서 `s_code.js` 파일 호스팅**: 이 파일은 일반적으로 웹 서버에 다른 스크립트와 함께 있습니다.
1. **모든 페이지에서 `s_code.js` 참조**: 모든 개별 페이지가 코어 JavaScript 파일을 호출하고 HTML `<body>` 태그 (`<head>` 태그 아님) 내에서 호출하는지 확인하십시오.

   >[!TIP]
   >
   >H 코드를 사용하려면 `s_code.js` 스크립트가 `<body>` 태그 내에 호출되어 있어야 합니다. 이는 다른 구현 메서드와 다르며, 대부분은 스크립트 참조가 `<head>` 태그에 있어야 합니다.
1. **각 페이지에서 페이지별 변수 정의**: 각 페이지에는 페이지 이름이나 eVar와 같은 개별 변수가 정의되어 있어야 합니다. 개별 변수는 일반적으로 각 페이지에서 인라인 `<script>` 태그로 정의됩니다.
1. **디버거를 사용하여 데이터 수집을 확인**: [CX Enterprise 디버거를 다운로드하여 설치](../../validate/debugger.md)하여 데이터가 Adobe으로 전송되고 페이지 변수가 올바르게 정의되었는지 확인하십시오.

## 캐싱

JavaScript 파일은 처음에 로드된 후 방문자의 브라우저에 캐시되며, 일반적으로 세션당 두 번 이상 다운로드되지 않습니다. 이 파일은 사이트의 모든 페이지에서 사용되더라도 각 페이지에서 다운로드되지 않습니다. 대부분의 웹 사이트에서 사용자는 평균적으로 세션당 몇 번 이상의 페이지 보기를 가지므로 여러 번 사용되는 JavaScript을 이 파일로 전송하면 다운로드되는 전체 데이터가 줄어들 수 있습니다.

## H 코드 압축

`s_code.js` 파일의 다운로드 크기가 걱정되는 경우 GZIP을 사용하여 `s_code.js` 파일을 압축하는 것이 좋습니다. GZIP은 모든 주요 브라우저에서 지원되며 JavaScript 압축보다 성능이 더 좋습니다. Apache 설명서의 [Apache 모듈 mod_deflate](https://httpd.apache.org/docs/current/mod/mod_deflate.html)를 참조하십시오.
