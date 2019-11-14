---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.linkExternalFilters

사이트에 외부 사이트에 대한 링크가 많이 포함되어 있으며 일부 종료 링크만 추적하려는 경우  를 사용하여 종료 링크의 특정 하위 집합에 대해 보고합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 경로 &gt; 시작 및 종료 &gt; 종료 링크 | "" |

The *`linkExternalFilters`* variable is an optional variable used in conjunction with *`linkInternalFilters`* to determine whether a link is an exit link. 종료 링크는 방문자를 사이트 외부로 보내는 링크로 정의됩니다. 종료 링크의 대상 창이 팝업과 기존 창 중 어느 것인지는 종료 링크 보고서에 링크가 표시되는지 여부에 영향을 주지 않습니다. 종료 링크는  *`trackExternalLinks`*&#x200B;가 'True'로 설정된 경우에만 추적됩니다. *`linkExternalFilters`* 및 *`linkInternalFilters`*&#x200B;의 필터는 대/소문자를 구분하지 않습니다.

> [!NOTE]*`linkExternalFilters`*&#x200B;를 사용하지 않으려면 삭제하거나 ""로 설정합니다.

*`linkExternalFilters`* 및 *`linkInternalFilters`*&#x200B;의 필터 목록은 기본적으로 모든 링크의 도메인 및 경로에 적용됩니다. *`linkLeaveQueryString`*&#x200B;이 'true'로 설정되면 필터가 전체 URL(도메인, 경로 및 쿼리 문자열)에 적용됩니다. 이러한 필터는 href 값에 상대 경로를 사용한 경우라도 항상 URL의 절대 경로에 적용됩니다.

대부분의 회사는 *`linkInternalFilters`* 가 종료 링크를 충분히 제어할 수 있도록 해주므로 *`linkExternalFilters`*. *`linkExternalFilters`*&#x200B;를 사용하기만 해도 종료 링크가 외부 링크로 간주될 가능성이 줄어듭니다. *`linkExternalFilters`*&#x200B;에 값이 있으면 *`linkInternalFilters`*&#x200B;와 일치하지 않고 *`linkExternalFilters`*&#x200B;와 일치할 경우에만 링크가 외부 링크로 간주됩니다.

다음 예에서는 이 변수의 사용 방법을 설명합니다. 이 예에서 페이지의 URL은 `https://www.mysite.com/index.html`입니다.

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

*`linkExternalFilters`* 변수는 쉼표로 구분된 ASCII 문자 목록입니다. 공백은 허용되지 않습니다.

```js
s.linkExternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

URL의 어떤 부분이든 *`linkExternalFilters`*&#x200B;에 쉼표로 구분하여 포함될 수 있습니다.

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

* *`linkExternalFilters`*&#x200B;를 사용하면 사이트에서 종료 링크가 되는 링크의 수가 줄어들 수 있습니다. 내부 링크를 종료 링크로 적용하기 위해 이 변수를 *`linkInternalFilters`* 대신 사용하지 마십시오.

* 링크의 쿼리 문자열에 *`linkExternalFilters`*&#x200B;를 적용해야 하는 경우 *`linkLeaveQueryString`*&#x200B;이 'true'로 설정되어 있는지 확인합니다. `"true"`로 설정하기 전에 [linkLeaveQueryString](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)을 참조하십시오.

* 종료 링크 추적을 비활성화하려면 *`trackExternalLinks`*&#x200B;를 `"false"`로 설정합니다.
