---
title: 다이내믹 변수
description: 이미지 요청 길이를 늘리지 않고 변수를 복사합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 다이내믹 변수

동적 변수를 사용하면 이미지 요청 길이를 늘리지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다. 이 변수는 여러 변수에서 동일한 데이터를 캡처할 때 유용합니다.

이전 버전의 Analytics에서는 데이터가 잘리지 않도록 하는 데 이미지 요청 길이가 중요했습니다. AppMeasurement의 향상된 기능을 사용하면 이미지 요청 쿼리 문자열이 훨씬 길어질 수 있으므로 동적 변수가 일반적으로 필요하지 않습니다.

동적 변수는 이미지 요청에서 쿼리 문자열 매개 변수 또는 HTTP 헤더를 지원합니다. 참조할 수 있는 매개 변수의 전체 목록이 필요하면 [데이터 수집 쿼리 매개 변수](../../validate/query-parameters.md)를 참조하십시오. 참조할 수 있는 HTTP 요청 필드의 전체 목록이 필요하면 위키백과의 [표준 요청 필드](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields#Request_fields)를 참조하십시오.

Adobe는 동적 변수 접두사를 인식하면 보고서 세트의 쿼리 문자열 또는 HTTP 헤더 값을 자동으로 복사합니다. 이 작업은 처리 규칙 및 VISTA 규칙을 포함한 다른 처리 전에 수행됩니다.

>[!TIP] 변수를 복사할 때에는 최대 문자 제한을 고려해야 합니다. 예를 들어 `eVar1`을 `prop1`에 복사하는 경우 `prop1`은 100바이트 제한이 있으므로 값이 잘릴 수 있습니다(반면에 `eVar1`에는 255바이트 제한이 있음).

## Adobe Experience Platform Launch의 동적 변수

문자열을 허용하는 차원 필드에서 동적 변수를 사용할 수 있습니다. 차원 값은 일반적으로 Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 설정됩니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. 원하는 차원 값을 찾습니다.

텍스트 필드에 동적 변수 접두사를 배치하고 참조할 쿼리 문자열 매개 변수나 HTTP 헤더를 추가합니다. 기본적으로 동적 변수 접두사는 `D=`입니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 동적 변수

동적 변수는 다른 변수에 지정된 텍스트 문자열입니다. 기본 동적 변수 접두사는 `D=`입니다. 동적 변수는 대/소문자를 구분합니다.

```js
// Copy eVar1 into eVar2. The query string parameter of eVar1 is v1.
s.eVar1 = "Example value";
s.eVar2 = "D=v1";

// Take the user agent string found in the image request HTTP header and place it in eVar1.
s.eVar1 = "D=User-Agent";

// Copy the page URL and place it in eVar1. The query string parameter of page URL is g.
s.eVar1 = "D=g";
```

>[!NOTE] 동적 변수는 구현을 디버깅할 때 문자열로 나타납니다. 값은 Adobe 데이터 수집 서버에 의해 서버측에서 복사됩니다.
