---
description: JavaScript 없이 Analytics를 구현하기 위한 요구 사항과 구성이 더 있습니다.
keywords: Analytics 구현; 대/소문자 구분; 쿼리 매개 변수 인코딩; 잘못된 문자; 보안 이미지 요청; 최대 변수 길이; 참조; URL; 캐싱; namespace
seo-description: JavaScript 없이 Analytics를 구현하기 위한 요구 사항과 구성이 더 있습니다.
seo-title: JavaScript 지침 없이 구현
solution: Analytics
title: JavaScript 지침 없이 구현
topic: 개발자 및 구현
uuid: C 672 DD 63-1 C 74-4 F 66-8992-9257 C 5 A 75 E 36
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# JavaScript 지침 없이 구현

JavaScript 없이 Analytics를 구현하기 위한 요구 사항과 구성이 더 있습니다.

샘플 코드를 보면 구현을 더 잘 이해할 수 있습니다. 다음 정보는 추가 요구 사항 및 구성을 간략히 설명합니다.

<!--Meike, I converted this from a table. Table within a table was a mess, and I'm not sure I captured everything. Please check this content against the orginal. -Bob -->

**대/소문자 구분**

The parameter names (`pageName`, `purchaseID`, and so forth) are case-sensitive and will not properly record data unless they appear as designated in the table displayed in [Query Parameters](../../../implement/js-implementation/data-collection/query-parameters.md).

**쿼리 매개 변수 인코딩**

각 쿼리 문자열 매개 변수의 값은 URL로 인코딩되어야 합니다. URL encoding converts characters that are normally illegal when appearing in a query string, such as a space character, into an encoded character beginning with `%`. For example, a space character is converted into `%20`.

이 함수의 JavaScript 버전은 escape라고 합니다(디코딩은 escape 취소). Microsoft IIS Version 5.0에도 쿼리 문자열 인코딩을 위해 Escape와 Escape 취소 함수가 포함되어 있습니다. 다른 웹 서버 스크립팅 언어에서도 인코딩/디코딩 유틸리티를 제공합니다.

**최대 변수 길이**

각 변수에는 최대 길이가 있습니다. 이 길이는 [Analytics 변수](../../../implement/js-implementation/c-variables/sc-variables.md). 변수의 최대 길이를 초과하면 이 변수의 값이 저장소용으로 잘려서 Analytics에 표시됩니다.

**잘못된 문자**

십진수 128을 넘는 문자 코드를 사용하는 문자는 128 미만의 인쇄가 되지 않는 문자 코드와 마찬가지로 유효하지 않습니다. HTML 서식("&lt;h1&gt;")도 상표, 등록 상표 및 저작권 기호처럼 유효하지 않습니다.

**보안 (&lt; https: &gt; 비보안 (&lt; http: &gt;) 이미지 요청**

https(보안 프로토콜)를 통해 액세스하는 페이지에서, 이미지 요청의 URL 부분은 다른 데이터 수집 서버 세트를 수용하도록 변경됩니다.

다음 정보는 보안 및 비보안 이미지 요청에 사용된 서로 다른 URL를 보여줍니다.

* The `*` in the URL above denotes a data-center specific URL that is provided to you by your Adobe Consultant. Adobe에서는 몇 개의 데이터 센터를 사용하므로, 해당 조직이 지정된 올바른 URL을 구현해야 합니다. 회사 계정 내에서 관리 콘솔 외부에 다운로드한 모든 코드에는 올바른 데이터 센터가 자동으로 제공되어 있습니다. 외부 소스에서 제공된 코드는 올바른 데이터 센터를 가리키도록 수정해야 할 수 있습니다.
* 여러 보고서 세트를 사용하는 클라이언트의 경우, 아래에서 보듯이 디렉토리 섹션에만 나열되고 URL의 도메인 섹션에는 나열되면 안 됩니다.
* The `*` in the URL above denotes a data-center specific URL that is provided to you by your Adobe Consultant. Adobe에서는 몇 개의 데이터 센터를 사용하므로, 해당 조직이 지정된 올바른 URL을 구현해야 합니다.

**URL 및 참조 URL**

`g=` AND `r=` 변수의 서버에서 URL 및 참조 URL를 채울 수 있습니다. Use the Request ServerVariables (`HTTP\_REFERRER`) or Request ServerVariables `(URL) (IIS/ASP)`, or the appropriate variable for your server/scripting technology. The referring URL `( r=)` is extremely important for tracking referring URLs, domains, search engines, and search terms.

Pagename를 사용하지 않는 경우 현재 URL 필드를 고유하게 채워야 합니다. If neither pageName nor Current URL `(g=)` is populated, the record is invalid and is not processed. 최소한 레코드를 처리하기 위해서는 URL 필드를 반드시 채워야 합니다.

**캐시의 효과**

방문자와 컨텐츠를 제공하는 웹 사이트 사이에 있는 브라우저나 서버가 HTML과 다른 웹 페이지를 캐싱할 수 있습니다. 캐싱을 사용하면 "cache-busting" 기술이 사용되지 않는 한 페이지 보기 횟수 및 기타 이벤트가 정확하게 카운트되지 않습니다.

Adobe의 표준 JavaScript에는 페이지 및 이미지 캐시를 방지하도록 이미지 요청을 변경하는 동적 방법이 포함되어 있어서 페이지 보기의 수를 정확히 계산할 수 있습니다.

하지만 서버측 이미지 요청을 만들 때는 이러한 무작위 추출이 발생하지 않습니다. 페이지 다시 로드 및 캐시된 페이지(브라우저의 캐시와 프록시 서버 둘 중 하나에서)의 수는 서버측 이미지 요청 사용 시의 특정 경우 카운트되지 않습니다.

SSL (`https:`) pages are not, by definition, ever cached so this warning applies only to non-secure (`http:`) pages. Additionally, pages with parameters (`https://www.samplesite.com/page.asp?parameter=1`) or certain file extensions (`.asp`, `.jsp`, etc.) 캐시되지 않습니다.

아래의 예도 주로 이미지 요청 서버측을 만들고, 브라우저에서 무작위 숫자를 추적하는 최소한의 JavaScript 솔루션을 보여 줍니다. 이 메서드는 https를 통해 액세스한 정적 HTML 페이지에서 발생할 수 있는 캐싱을 극복합니다. 프로토콜.

**nameSpace 변수**

nameSpace 쿼리 문자열 매개 변수는 비JavaScript 구현에 필수입니다.

예: ns=nameSpace

Adobe 컨설턴트나 계정 관리자에게 연락하여 조직의 nameSpace 값을 받으십시오.
