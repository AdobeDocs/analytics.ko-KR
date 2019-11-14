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


# s_objectID

이 변수는 링크의 [!UICONTROL onClick] 이벤트에서 설정해야 하는 전역 변수입니다.

<!-- 

s_objectID.xml

 -->

페이지의 링크 또는 링크 위치에 대한 고유 개체 ID를 작성함으로써 방문자 활동 추적을 개선하거나 [!UICONTROL Activity Map]을 사용하여 링크 URL보다는 링크 유형 또는 위치에 대해 보고할 수 있습니다.

> [!NOTE] s_objectID를 Activity Map에서 사용할 때는 후행 세미콜론(;)이 [필요합니다](https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/activitymap-link-tracking-use-case.html).

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | OID | [!UICONTROL Activity Map], [!UICONTROL ClickMap] | 클릭한 링크의 절대 URL |

다음 세 가지 일반적인 이유 *`s_objectID`*:

* 하루 동안 자주 변하는 방문자 활동을 집계하기 위해
* [!UICONTROL Activity Map]이 결합하는 링크 활동을 구분하기 위해
* [!UICONTROL Activity Map] 데이터 보고의 정확도를 개선하기 위해

**매우 동적인 링크에 대한 클릭 집계** {#section_BA730A0393B149DDBCAA272C3C23A1C5}

사이트가 동적이고 일부 페이지의 링크가 하루 종일 변경되는 경우 *`s_objectID`*&#x200B;를 사용하여 페이지에서 링크 위치를 식별할 수 있습니다. *`s_objectID`*&#x200B;가 예를 들어 페이지의 왼쪽 상단에 있는 첫 번째 링크를 나타내는 "top left 1" 또는 "top left 2"로 설정된 경우 해당 위치에 나타나는(또는 동일한 값으로 설정된 *`s_objectID`*) 모든 링크가 방문자 클릭 맵과 함께 보고됩니다. *`s_objectID`*&#x200B;를 사용하지 않는 경우에는 특정 링크를 클릭한 횟수가 표시되지만, 사이트 방문자가 해당 위치의 다른 모든 링크를 어떻게 사용했는지에 대한 통찰력은 잃게 됩니다.

**결합된 클릭 구분** {#section_1AE91FB8A2D3423CBE064ACF02FEEA47}

사이트의 *`pageName`* 변수가 방문자가 보고 있는 특정 페이지가 아니라 방문자가 보고 있는 섹션이나 템플릿을 표시하는 데 사용되는 경우 해당 페이지 템플릿의 여러 버전에 표시되는 링크를 구분하는 데 *`s_objectID`*&#x200B;를 사용할 수 있습니다. 예를 들어 사이트에 있는 모든 제품에 대한 템플릿 페이지가 있는 경우, 모든 페이지의 해당 템플릿에서 홈 페이지와 검색 상자에 연결된 링크가 있을 수 있습니다. 이러한 링크가 개별 제품 기반(템플릿 기반이 아닌)으로 어떻게 사용되는지를 알려면 *`s_objectID`*&#x200B;를 "prod 123789 home page" 또는 "prod 123789 search"와 같이, 제품별 값으로 채우면 됩니다. 완료되면 [!UICONTROL Activity Map]은 개별 제품 기반으로 해당 링크에 대해 보고합니다.

**[!UICONTROL Activity Map]정확도 개선** {#section_08B3406821294DCCABEEB99C90CF5C52}

경우에 따라 Internet Explorer, Firefox, Netscape, Opera 및 Safari 이외의 브라우저는 보고되지 않습니다. 이런 경우가 흔하지는 않지만, 일부 클릭 수와 기타 지표가 이 문제와 관련됩니다. 링크 내에서 *`s_objectID`*&#x200B;를 사용하면 이러한 문제를 고유하게 식별하고 브라우저 보고 문제를 해결합니다. 다음은 링크가 *`s_objectID`*:

```js
<a href="/art.jsp?id=559" onClick="s_objectID='top left 1';">Article 559</a> 
<a href="/home.jsp" onClick="s_objectID='prod 123789 home page';">Home</a> 
```

**구문 및 가능한 값** {#section_85841DF9F06A4680953D9B2A884A1A5A}

s_objectID에는 모든 텍스트 식별자가 들어 있을 수 있습니다.

```js
s_objectID="unique_id" 
```

*`s_objectID`*&#x200B;에는 표준 변수 제한 외에는 제한이 없습니다.

**예** {#section_33F119D532CA4ACAA3426253C42030BB}

```js
s_objectID="top left 2" 
```

```js
s_objectID="prod 123789 search"
```

**구성 설정** {#section_95396657D55B41ECB66B83D0534EA827}

없음
