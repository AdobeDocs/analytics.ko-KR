---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---



# s.linkInternalFilters

 변수는 사이트에서 어느 링크가 종료 링크인지를 확인하는 데 사용됩니다.

사이트에 속한 링크를 나타내는 필터들이 쉼표로 구분되어 있는 목록입니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 경로 &gt; 시작 및 종료 &gt; 종료 링크 |  |

> [!NOTE]이전에 linkInternalFilters를 Javascript로 설정할 것을 권장했습니다. 그러나 이로 인해 태그가 상주하는 현재 도메인을 포함하여 모든 도메인이 외부로 간주됩니다. 여러 도메인을 내부로 간주하려면 아래 예제에 표시된 것처럼 그러한 도메인을 추가할 수 있습니다.

*`linkInternalFilters`* 변수는 링크가 종료 링크인지 여부를 확인하는 데 사용됩니다. 종료 링크는 방문자를 사이트 외부로 보내는 링크입니다. 종료 링크의 대상 창이 팝업과 기존 창 중 어느 것인지는 종료 링크 보고서에 링크가 표시되는지 여부에 영향을 주지 않습니다. 종료 링크는 *`trackExternalLinks`* 가 `"true"`. DTM이 종료 링크를 처리하는 방법에 대한 자세한 내용은 동적 태그 관리 문서에서 [링크 추적](https://marketing.adobe.com/resources/help/en_US/dtm/link_tracking.html)을 참조하십시오. *`linkInternalFilters`*&#x200B;의 필터는 대/소문자를 구분하지 않습니다.

*`linkInternalFilters`*&#x200B;의 필터 목록은 기본적으로 모든 링크의 도메인 및 경로에 적용됩니다. *`linkLeaveQueryString`*&#x200B;이 `"true"`로 설정되면 필터가 전체 URL(도메인, 경로 및 쿼리 문자열)에 적용됩니다. 필터는 href 값에 상대 경로를 사용한 경우라도 항상 URL의 절대 경로에 적용됩니다.

사이트의 모든 도메인(및 사용자의 JavaScript 파일을 사용하는 모든 파트너)이 *`linkInternalFilters`*. 목록에 일부 도메인이 포함되지 않은 경우, 이러한 도메인으로 연결되거나 도메인에 있는 모든 링크가 종료 링크로 간주되어 전송되는 서버 호출을 증가시킵니다. 여러 도메인 또는 회사가 단일 JavaScript용 [!DNL AppMeasurement] 파일을 사용하려는 경우 페이지에서 *`linkInternalFilters`*&#x200B;를 채워서 JavaScript 파일에 지정된 값을 재정의하는 것을 고려할 수 있습니다. 주 도메인에 직접 연결되는 부속 도메인이 있는 경우에는 부속 도메인(vanity domain)을 목록에 포함시킬 필요가 없습니다.

다음 예에서는 이 변수의 사용 방법을 설명합니다. 이 예에서 페이지의 URL은 `https://www.mysite.com/index.html`입니다.

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

*`linkInternalFilters`* 변수는 쉼표로 구분된 ASCII 문자 목록입니다. 공백은 허용되지 않습니다.

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

* 필터 목록에서 JavaScript용 [!DNL AppMeasurement] 파일에 사용할 수 있는 모든 도메인을 포함하십시오.
* [!UICONTROL [경로]] &gt; [!UICONTROL [시작 및 종료]] &gt; [!UICONTROL [종료]] 링크 보고서에 있는 항목 중에서 잘못된 항목이 없는지 주기적으로 확인하십시오.

* 파트너 계약을 주기적으로 검토하여 파트너 계약에 링크 추적에 대한 제한 사항이 있는지 파악하십시오. 예를 들어 파트너 디스플레이 광고에 나타나는 링크를 추적하는 것이 금지되었을 수 있습니다. 도메인을 *`linkInternalFilters`*:

```js
s.linkInternalFilters="mysite.com,mysite.net,mypartner.net/adclick"
```
