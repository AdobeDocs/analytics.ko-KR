---
title: H 코드 JavaScript 구현 개요
description: 사이트에서 H 코드를 구현하는 워크플로우에 대해 알아봅니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# H 코드 JavaScript 구현 개요

>[!IMPORTANT] 이 버전의 데이터 수집은 더 이상 지원되지 않습니다. [Adobe Experience Platform Launch](../../launch/overview.md)나 [AppMeasurement for JavaScript](../overview.md)로 업그레이드하십시오.

데이터를 수집하기 위해 코드가 있는 페이지를 성공적으로 구현하려면 호스팅 서버에 액세스할 수 있어야 합니다. 다음은 기초 Analytics H 코드 구현 단계입니다.

>[!NOTE] 이 지침을 따르려면 이미 `s_code.js`의 기존 복사본을 가지고 있어야 합니다. Adobe는 더 이상 코드 관리자에서 H 코드를 다운로드할 수 있는 옵션을 제공하지 않습니다.

1. **코어 JS 파일 변수 업데이트**: `s_code.js` 파일을 편집하고 다음 변수가 업데이트되었는지 확인합니다.
   * `s_account`에는 전송하는 데이터를 받을 보고서 세트 ID가 포함되어 있습니다. 참조
   * `s.trackingServer`에는 위치 쿠키가 저장되어 있습니다. [trackingServer](../../vars/config-vars/trackingserver.md)를 참조하십시오.
2. **사이트에서`s_code.js`파일 호스팅**: 이 파일은 일반적으로 웹 서버에 다른 스크립트와 함께 있습니다.
3. **모든 페이지에서`s_code.js`참조**: 모든 개별 페이지가 코어 JavaScript 파일을 호출하고 HTML `<body>` 태그(`<head>` 태그 아님) 내에서 호출하는지 확인하십시오.
   > [!TIP] H 코드를 사용하려면 `s_code.js` 스크립트가 `<body>` 태그 내에 호출되어 있어야 합니다. 이는 다른 구현 메서드와 다르며, 대부분은 스크립트 참조가 `<head>` 태그에 있어야 합니다.
4. **각 페이지에서 페이지별 변수 정의**: 각 페이지에는 페이지 이름이나 eVar와 같은 개별 변수가 정의되어 있어야 합니다. 개별 변수는 일반적으로 각 페이지에서 인라인 `<script>` 태그로 정의됩니다.
5. **디버거를 사용하여 데이터 수집 확인**: [Experience Cloud Debugger](../../validate/debugger.md)를 다운로드하고 설치하여 데이터가 Adobe에 전송되고 페이지 변수가 올바로 정의되어 있는지 확인합니다.

## 캐시

JavaScript 파일은 처음에 로드된 후 방문자의 브라우저에 캐싱되며 일반적으로 세션당 한 번 이상 다운로드되지 않습니다. 이 파일은 사이트의 모든 페이지에서 사용되더라도 각 페이지에서 다운로드되지 않습니다. 대부분의 웹 사이트에서 사용자는 평균적으로 세션당 여러 번 페이지를 보기 때문에 여러 번 사용되는 JavaScript를 이 파일로 전송하면 다운로드되는 전체 데이터가 줄어들 수 있습니다.

## H 코드 압축

`s_code.js` 파일의 다운로드 크기가 걱정되는 경우 GZIP을 사용하여 `s_code.js` 파일을 압축하는 것이 좋습니다. GZIP은 모든 주요 브라우저에서 지원되며 JavaScript 압축보다 성능이 더 좋습니다. Apache 설명서의 [Apache 모듈 mod_deflate](http://httpd.apache.org/docs/current/mod/mod_deflate.html)를 참조하십시오.
