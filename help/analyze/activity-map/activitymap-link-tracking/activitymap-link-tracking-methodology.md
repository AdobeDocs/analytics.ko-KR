---
description: 이 섹션은 Adobe Analytics 관리자용으로서, 새로운 링크 추적 매개 변수를 집중적으로 살펴보고, 이 매개 변수들이 여러 브라우저와 장치에서 링크 고유성 및 일관성을 보장하고 페이지에서 링크 위치 변경 처리를 개선하는 방식에 대해 살펴봅니다.
title: 링크 추적 방식
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Activity Map
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
source-git-commit: a6b38c6e7a34c876524ebe15514ac205898549d0
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 95%

---

# 링크 추적 방식

이 섹션은 Adobe Analytics 관리자용으로서, 새로운 링크 추적 매개 변수를 집중적으로 살펴보고, 이 매개 변수들이 여러 브라우저와 장치에서 링크 고유성 및 일관성을 보장하고 페이지에서 링크 위치 변경 처리를 개선하는 방식에 대해 살펴봅니다.

>[!IMPORTANT]
>
>텍스트(href 아님)에 개인 식별 정보(PII)를 포함할 수 있는 모든 링크는 [s_objectID](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html?lang=ko-KR)를 사용하거나 [s.ActivityMap.linkExclusions 또는 s.ActivityMap.regionExclusions](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#configuration-vars)로 ActivityMap 링크 컬렉션을 제외하여 명시적으로 구현해야 합니다. Activity Map이 PII 데이터를 수집하는 방법에 대한 자세한 내용은 [여기](/help/analyze/activity-map/lnk-tracking-overview.md)에서 확인하십시오.

Activity Map은 다음 두 ID를 기반으로 링크를 추적합니다.

* 기본 ID: 링크의 인식 가능한 매개 변수입니다.
* 링크 영역: 사용자가 페이지나 영역에서 전체 링크 구역을 나타내는 문자열을 지정할 수 있는 보조 매개 변수입니다. 이 매개 변수는 사용자가 제공하지 않는 경우 자동으로 생성될 수 있습니다.

## 기본 ID {#section_E8705CC1BDBC47FB8A4FE02293BACFE6}

HTML에 s_objectid가 있다면, 기본 ID의 기본값은 s_objectid로 지정됩니다. 그렇지 않은 경우에는 다음의 매개 변수가 기본 ID로 사용됩니다(아래 나열된 순서대로).

* Innertext
* Alttext
* 직함
* Src
* 작업

## InnerText 사용과 링크 동작(URL) 사용 {#section_70C3573E22274522A8CC035BF18EC468}

링크 동작은 링크를 클릭할 때 웹 페이지(일반적으로 링크를 클릭한 후 방문하는 URL)가 취하는 동작입니다. 링크 동작을 사용할 때 다음과 같은 문제가 발생할 수 있습니다.

* ID가 동일한 서로 다른 링크가 두 개 이상 생기는 문제
* 링크의 가독성 문제
* 한 링크가 여러 동작(링크를 볼 때 사용하는 장치에 따라 다름)을 하는 문제

따라서 Adobe에서는 링크 동작(URL)을 사용할 때와 비교해서 다음과 같은 이점이 있는 InnerText를 사용합니다.

* 링크 ID의 좋은 표현입니다. 동일한 텍스트의 여러 링크가 생기는 일이 흔하지 않아서 기본 ID 중복이 크게 줄어들었습니다.
* 여러 장치와 여러 종류의 브라우저에서 기본 ID의 일관성을 보장합니다.
* 페이지에서 링크 위치 변경으로 인한 영향을 받지 않습니다.
* 가독성이 개선되므로, 사용자는 Activity Map 외부에서 링크 추적 보고서에 대한 분석을 시작할 수 있습니다.

## 링크 영역 {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

이 새로운 속성을 사용하면 링크가 있는 페이지 영역을 나타내는 문자열을 지정할 수 있습니다.

예를 들어, 웹 페이지의 메뉴 섹션에 있는 &quot;담당자에게 문의&quot; 링크에 대해 사용자는 &quot;메뉴&quot; 영역 매개 변수를 전달할 수 있습니다. 유사하게, 웹 페이지의 바닥글에 있는 &quot;문의하기&quot; 링크의 경우에는 영역 매개 변수를 &quot;footer&quot;로 설정할 수 있습니다.

링크 영역 값은 링크 자체에 설정되지 않지만, 해당 영역을 둘러싸는 DOM HTML 트리 위의 한 HTML 요소에 설정됩니다.
링크 영역을 사용하면 다음과 같은 이점이 있습니다.

* 동일한 기본 ID로 링크를 차별화하는 데 도움이 됩니다.
* 영역에서의 트렌드는 웹 페이지의 다이내믹한 측면이 주는 영향을 덜 받습니다.
* 사용자는 영역 내에서 상위 실적 링크를 볼 수 있습니다. 영역을 앵커로 사용하면, 페이지에 현재 표시되지 않는 링크들의 오버레이를 보여줄 수 있습니다(Ajax, Targeting).
* 한 영역은 많은 웹 페이지에서 사용될 수 있기 때문에 영역이 여러 페이지를 대체할 수 있습니다. 이것은 &quot;내 &#39;제공 제품&#39; 영역이 &#39;여성용&#39; 랜딩 페이지나 &#39;남성용&#39; 랜딩 페이지에서 최고의 성과를 올리나요?&quot;와 같은 질문에 답하는 데에 도움이 됩니다.
* 본질적으로, 영역은 매우 다이내믹한 웹 페이지를 분석하는 데 적절한 차원입니다. 이것은 계속해서 변화하는 링크로 인한 노이즈를 제거하기 때문입니다. 예를 들어 CNN 랜딩 페이지의 &quot;Latest News&quot; 영역에는 변화하는 링크가 많이 있을 수 있습니다. 하지만 이 영역은 항상 같은 위치에 있게 됩니다. 따라서 여러 날에 걸쳐 영역 수준에서 트렌드를 찾는 것은 흥미로울 수 있습니다.

**사용자 지정된 영역 추적**

링크에 대한 영역 매개 변수를 사용자 지정할 수 있습니다(기본값은 링크ID). 태그를 &quot;ID&quot;로 설정하면 &quot;id&quot; 매개 변수를 가진 모든 HTML 요소를 영역으로 사용합니다. 따라서, 영역 태그를 &quot;id&quot;로 설정하면 서로 다른 많은 영역이 반환됩니다(페이지에 있는 서로 다른 &quot;ID&quot;의 수만큼). 또는 구현을 더 많이 사용자 지정하려는 경우, 영역 태그를 &quot;region_id&quot;와 같이 더 구체적으로 설정할 수 있습니다. 

아래에서는 기본 영역 ID 속성 &quot;id&quot;를 사용하는 샘플 HTML을 볼 수 있습니다.

```
<div id="content">
  <div id="breaking_news">
    <a href="breaking-news.html">...</a>
  </div>
  <div id="todays_top_headlines">
    <a href="breaking-news.html">...</a>
  </div>
```

원할 경우, 이 경우 &quot;lpos&quot;와 같이 임의의 문자열 식별자가 있는 요소에 태그를 지정한 다음, &quot;lpos&quot;라는 이름의 속성을 추가할 수 있습니다.

```
<script language="JavaScript" type="text/javascript">
s.ActivityMap.regionIDAttribute = "lpos";
</script>
<div id="nav" lpos="navbar">
  <ul>
    <li>Menu Category A
      <ul>
        <li><a href="">Menu Item A 1</a>
        <li><a href="">Menu Item A 2</a>
      </ul>
    </li>
    <li>Menu Category B
      <ul>
        <li><a href="">Menu Item B 1</a>
        <li><a href="">Menu Item B 2</a>
      </ul>
    </li>
  </ul>
</div> 
  
<div id="content">
  <div id="breaking_news" lpos="breaking_news>
    <a href="breaking-news.html">...</a>
  </div>
  <div id="todays_top_headlines">
    <a href="breaking-news.html">...</a>
  </div>
```

## 구성 변수 {#configuration-vars}

다음 변수들은 참조용으로만 제공됩니다. Activity Map은 설치 즉시 적절하게 구성되지만, 다음 변수들을 사용하여 구현을 사용자 지정할 수 있습니다.

### `s.ActivityMap.regionIDAttribute`

의 일부 상위 요소(parent, parent.parent, ...) 요소에서 지역 ID로 사용할 태그 속성을 식별하는 문자열입니다 `s.linkObject`예, **클릭한 요소**.

**예**

기본값을 &quot;id&quot; 매개 변수로 지정합니다. 이 변수를 다른 매개 변수로 설정할 수 있습니다.

### `s.ActivityMap.link`

클릭한 항목을 수신하는 함수 `HTMLElement` 및 는 클릭한 링크를 나타내는 문자열 값을 반환해야 합니다. 반환 값이 false일 경우(null, 정의되지 않음, 빈 문자열, 0), 링크가 추적되지 않습니다.

**예**

```
// only ever use "title" attributes from A tags
function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

### `s.ActivityMap.region`

클릭한 HTMLElement를 받고, **클릭했을 때 링크가 있었던 영역을 나타내는 문자열 값을 반환해야 하는 함수.** 반환 값이 false일 경우(null, 정의되지 않음, 빈 문자열, 0), 링크가 추적되지 않습니다.

**예**

```
// only ever use lowercase version of tag name concatenated with first className as the region
function(clickedElement) {
  var regionId, className;
  while (clickedElement && (clickedElement = clickedElement.parentNode)) {
    regionId = clickedElement.tagName;
    if (regionId) {
      return regionId.toLowerCase();
    }
  }
}
```

### `s.ActivityMap.linkExclusions`

링크 텍스트에서 검색할 문자열의 쉼표 구분 목록을 받는 문자열입니다. 검색되면, 링크는 Activity Map에 의해 추적되지 않도록 제외됩니다. 설정되지 않은 경우에는 Activity Map에 의한 링크 추적을 중지하기 위한 시도가 수행되지 않습니다.

**예**

```
// Exclude links tagged with a special linkExcluded CSS class
<style>
.linkExcluded {
  display: block;
  height: 1px;
  left: -9999px;
  overflow: hidden;
  position: absolute;
  width: 1px;
}
</style>
<a href="next-page.html">
  Link is tracked because link does not have hidden text matching the filter. 
</a>
<a href="next-page.html">
  Link not tracked because s.ActivityMap.linkExclusions is set and this link has hidden text matching the filter.
  <span class="linkExcluded">exclude-link1</span>
</a>
<a href="next-page.html">
  Link not tracked because s.ActivityMap.linkExclusions is set and this link has hidden text matching the filter.
  <span class="linkExcluded">exclude-link2</span>
</a>
<script>
  var s = s_gi('samplersid');
  s.ActivityMap.linkExclusions = 'exclude-link1,exclude-link2';
</script>
```

### `s.ActivityMap.regionExclusions`

영역 텍스트에서 검색할 문자열의 쉼표 구분 목록을 받는 문자열입니다. 검색되면, 링크는 Activity Map에 의해 추적되지 않도록 제외됩니다. 설정되지 않은 경우에는 Activity Map에 의한 링크 추적을 중지하기 위한 시도가 수행되지 않습니다.

**예**

```
// Exclude regions on the page from its links being trackable by ActivityMap
<div id="links-included">
  <a href="next-page.html">
    Link is tracked because s.ActivityMap.regionExclusions is set but does not match the filter.
  </a>
</div>
<div id="links-excluded"> 
  <a href="next-page.html">
    Link not tracked because s.ActivityMap.regionExclusions is set and this link matches the filter.
  </a>
</div>
<script>
  var s = s_gi('samplersid');
  s.ActivityMap.regionExclusions = 'links-excluded';
</script>
```
