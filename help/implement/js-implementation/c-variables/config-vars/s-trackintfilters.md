---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---



# s.linkInternalFilters

 변수는 사이트에서 어느 링크가 종료 링크인지를 확인하는 데 사용됩니다.

사이트에 속한 링크를 나타내는 필터들이 쉼표로 구분되어 있는 목록입니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 경로 &gt; 시작 및 종료 &gt; 종료 링크 |  |

>[!NOTE]
>
>이전에는 linkInternalFilters를 javascript:. 그러나 이로 인해 태그가 상주하는 현재 도메인을 포함하여 모든 도메인이 외부로 간주됩니다. 여러 도메인을 내부로 간주하려면 아래 예제에 표시된 것처럼 그러한 도메인을 추가할 수 있습니다.

The *`linkInternalFilters`* variable is used to determine whether a link is an exit link, which is defined as any link that takes a visitor away from your site. 종료 링크의 대상 창이 팝업과 기존 창 중 어느 것인지는 종료 링크 보고서에 링크가 표시되는지 여부에 영향을 주지 않습니다. 종료 링크는 *`trackExternalLinks`* 가 `"true"`. DTM이 종료 링크를 처리하는 방법에 대한 자세한 내용은 동적 태그 관리 문서에서 [링크 추적](https://marketing.adobe.com/resources/help/en_US/dtm/link_tracking.html)을 참조하십시오. 의 필터는 대/소문자를 구분하지 *`linkInternalFilters`* 않습니다.

의 필터 목록은 기본적으로 모든 링크의 도메인 및 경로에 *`linkInternalFilters`* 적용됩니다. If *`linkLeaveQueryString`* is set to `"true"`, then the filters apply to the entire URL (domain, path, and query string). 필터는 href 값에 상대 경로를 사용한 경우라도 항상 URL의 절대 경로에 적용됩니다.

사이트의 모든 도메인(및 사용자의 JavaScript 파일을 사용하는 모든 파트너)이 *`linkInternalFilters`*. 목록에 일부 도메인이 포함되지 않은 경우, 이러한 도메인으로 연결되거나 도메인에 있는 모든 링크가 종료 링크로 간주되어 전송되는 서버 호출을 증가시킵니다. 여러 도메인 또는 회사가 JavaScript 파일에 대해 단일 항목을 사용하려는 경우 JavaScript 파일에 지정된 값을 재정의하여 [!DNL AppMeasurement] *`linkInternalFilters`* 페이지에 채우는 것이 좋습니다. 주 도메인에 직접 연결되는 부속 도메인이 있는 경우에는 부속 도메인(vanity domain)을 목록에 포함시킬 필요가 없습니다.

다음 예에서는 이 변수의 사용 방법을 설명합니다. In this example, the URL of the page is `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="mysite.com" 
s.linkExternalFilters="" 
s.linkLeaveQueryString=false 
... 
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Exit Link</a> 
<a href="https://www2.site1.com/partners/">Exit Link</a> 
```

## 구문 및 가능한 값

The *`linkInternalFilters`* variable is a comma-separated list of ASCII characters. 공백은 허용되지 않습니다.

```js
s.linkInternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

## 예

```js
s.linkInternalFilters="mysite.com"
```

```js
s.linkInternalFilters="mysite.com,mysite.net,vanity1.com"
```

## 구성 설정

없음

## 함정, 질문 및 팁

* Include all domains that the [!DNL AppMeasurement] for JavaScript file may be served under in the filter list.
* [!UICONTROL [경로]] &gt; [!UICONTROL [시작 및 종료]] &gt; [!UICONTROL [종료]] 링크 보고서에 있는 항목 중에서 잘못된 항목이 없는지 주기적으로 확인하십시오.

* 파트너 계약을 주기적으로 검토하여 파트너 계약에 링크 추적에 대한 제한 사항이 있는지 파악하십시오. 예를 들어 파트너 디스플레이 광고에 나타나는 링크를 추적하는 것이 금지되었을 수 있습니다. 도메인을 *`linkInternalFilters`*:

```js
s.linkInternalFilters="mysite.com,mysite.net,mypartner.net/adclick"
```
