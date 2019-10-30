---
description: 지정한 쿼리 문자열 매개 변수가 현재 페이지 URL이나 제공된 문자열에 있는 경우 그 값을 반환합니다.
keywords: Analytics 구현
seo-description: 지정한 쿼리 문자열 매개 변수가 현재 페이지 URL이나 제공된 문자열에 있는 경우 그 값을 반환합니다.
seo-title: Util.getQueryParam
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Util.getQueryParam
topic: 개발자 및 구현
uuid: 1fecd148-3e52-46f2-a73f-003563f7a62c
translation-type: ht
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Util.getQueryParam

지정한 쿼리 문자열 매개 변수가 현재 페이지 URL이나 제공된 문자열에 있는 경우 그 값을 반환합니다.

페이지의 쿼리 문자열에서 중요한 데이터(캠페인 추적 코드, 내부 검색 키워드 등)를 사용할 수 있기 때문에 getQueryParam은 Analytics 변수에서 데이터를 캡처하는 데 유용합니다.

이 유틸리티는 [getQueryParam](../../implement/js-implementation/plugins/getqueryparam.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF) 플러그인을 대체합니다.

**구문:**

```
s.Util.getQueryParam(key, [url], [delim])
```

>[!NOTE]
>
>유틸리티의 구문은 플러그인의 구문과 다릅니다.

**매개 변수:**

| 매개 변수 | 설명 |
|---|---|
| key | (필수) 받으려는 쿼리 문자열 매개 변수의 이름 이 매개 변수는 대소문자를 구분합니다. |
| url | (선택 사항) 기본 url은 `s.pageURL` 또는 `window.location`입니다. 이 매개 변수의 값을 지정하면 쿼리 매개 변수를 검색한 URL을 무시하고 지정된 값을 사용합니다. |
| delim | (선택 사항) URL에 있는 매개 변수 구분 기호 기본 구분 기호는 "&amp;"입니다. ";"과 같은 대체 쿼리 문자열 구분 기호를 지정할 수 있도록 해줍니다. |

**반환:**

제공된 키가 없거나 URL 옵션이 없거나 URL에 키가 없는 경우 이 함수는 빈 문자열 ""을 반환합니다. 단편 구분 기호 #이 URL에 있는 경우 단편 구분 기호 다음에 오는 모든 것이 고려되지 않습니다. 키가 있고 값에 할당되면 해당 값은 URL 디코딩되어 반환됩니다.

**예:**

```js
s.doPlugins = function(s) { 
  s.campaign = s.Util.getQueryParam("cid"); 
};
```

