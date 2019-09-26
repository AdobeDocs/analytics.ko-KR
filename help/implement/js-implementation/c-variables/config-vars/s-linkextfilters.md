---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.linkExternalFilters

사이트에 외부 사이트에 대한 링크가 많이 포함되어 있고 일부 종료 링크를 추적하지 않으려는 경우 를 사용하여 특정 종료 링크의 하위 세트에 대해 보고합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 경로 &gt; 시작 및 종료 &gt; 종료 링크 | "" |

The 변수는 *`linkExternalFilters`* *`linkInternalFilters`* 링크가 종료 링크인지 여부를 확인하는 데 함께 사용되는 선택 변수입니다. 종료 링크는 방문자를 사이트 외부로 보내는 링크로 정의됩니다. 종료 링크의 대상 창이 팝업과 기존 창 중 어느 것인지는 종료 링크 보고서에 링크가 표시되는지 여부에 영향을 주지 않습니다. 종료 링크는 *`trackExternalLinks`* is set to 'true.' 필터는 대/소문자를 구분하지 *`linkExternalFilters`* *`linkInternalFilters`* 않습니다.

>[!NOTE]
>
>If you don't want to use , delete it or set it to "".*`linkExternalFilters`*

필터 목록은 기본적으로 의 목록을 *`linkExternalFilters`* 포함하며 모든 링크의 도메인 및 경로에 *`linkInternalFilters`* 적용됩니다. 'true'로 *`linkLeaveQueryString`* 설정하면 필터가 전체 URL(도메인, 경로 및 쿼리 문자열)에 적용됩니다. 이러한 필터는 href 값에 상대 경로를 사용한 경우라도 항상 URL의 절대 경로에 적용됩니다.

대부분의 회사는 *`linkInternalFilters`* 가 종료 링크를 충분히 제어할 수 있도록 해주므로 *`linkExternalFilters`*. Using *`linkExternalFilters`* simply decreases the likelihood that an exit link is considered external. If *`linkExternalFilters`* has a value, then a link is considered only external if it does not match *`linkInternalFilters`* and does match *`linkExternalFilters`*.

다음 예에서는 이 변수의 사용 방법을 설명합니다. In this example, the URL of the page is `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="javascript:,mysite.com" 
s.linkExternalFilters="site1.com,site2.com,site3.com/partners" 
s.linkLeaveQueryString=false 
... 
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Not an Exit Link</a> 
<a href="https://www.site1.com">Exit Link</a> 
<a href="https://www2.site3.com/partners/offer.asp">Exit Link</a> 
```

## 구문 및 가능한 값

The *`linkExternalFilters`* variable is a comma-separated list of ASCII characters. 공백은 허용되지 않습니다.

```js
s.linkExternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

URL의 어떤 부분이든 *`linkExternalFilters`*, separated by commas.

## 예

```js
s.linkExternalFilters="partnersite.com,partnertwo.net/path/"
```

```js
s.linkExternalFilters=""
```

## 구성 설정

없음

## 함정, 질문 및 팁

* Using *`linkExternalFilters`* can result in fewer links on your site being exit links. 내부 링크가 종료 링크가 되도록 *`linkInternalFilters`* 강제하기 위해 이 변수를 대신 사용하지 마십시오.

* 링크의 쿼리 문자열에 *`linkExternalFilters`* 적용해야 하는 경우 *`linkLeaveQueryString`* 이 'true'로 설정되어 있는지 확인하십시오. See [linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html) before setting to `"true"`.

* To disable exit link tracking, set *`trackExternalLinks`* to `"false"`.
