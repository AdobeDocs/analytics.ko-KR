---
description: 이 섹션은 Adobe Analytics 관리자용으로서, 새로운 링크 추적 매개 변수를 집중적으로 살펴보고, 이 매개 변수들이 여러 브라우저와 장치에서 링크 고유성 및 일관성을 보장하고 페이지에서 링크 위치 변경 처리를 개선하는 방식에 대해 살펴봅니다.
seo-description: 이 섹션은 Adobe Analytics 관리자용으로서, 새로운 링크 추적 매개 변수를 집중적으로 살펴보고, 이 매개 변수들이 여러 브라우저와 장치에서 링크 고유성 및 일관성을 보장하고 페이지에서 링크 위치 변경 처리를 개선하는 방식에 대해 살펴봅니다.
seo-title: 링크 추적 방법
solution: Analytics
title: 링크 추적 방법
topic: Activity Map
uuid: 67864 BF 9-33 CD -46 FA -89 A 8-4 D 83 D 3 B 81152
translation-type: tm+mt
source-git-commit: 4f313ae50c4d5a0f3bfec493c2d554bc8614aeef

---


# 링크 추적 방법

이 섹션은 Adobe Analytics 관리자용으로서, 새로운 링크 추적 매개 변수를 집중적으로 살펴보고, 이 매개 변수들이 여러 브라우저와 장치에서 링크 고유성 및 일관성을 보장하고 페이지에서 링크 위치 변경 처리를 개선하는 방식에 대해 살펴봅니다.

>[!IMPORTANT]
>
>Any link where the text (not the href) may contain PII (Personally Identifiable Information) should be implemented explicitly using [s_objectID](https://marketing.adobe.com/resources/help/en_US/sc/implement/s_objectID.html) or by excluding ActivityMap link collection with [s.ActivityMap.linkExclusions or s.ActivityMap.regionExclusions](../../../analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#section_634197EACD404AC086DF9A03B813C8C3). Activity Map이 PII 데이터를 수집하는 방법에 대한 자세한 내용은 [여기](../../../analyze/activity-map/lnk-tracking-overview.md#section_A9F016E64F33446F8916855D8C69A7C6)에서 확인하십시오.

Activity Map은 다음 두 ID를 기반으로 링크를 추적합니다.

* 기본 ID: 링크의 인식 가능한 매개 변수입니다.
* 링크 영역: 사용자가 페이지나 영역에서 전체 링크 구역을 나타내는 문자열을 지정할 수 있는 보조 매개 변수입니다. 이 매개 변수는 사용자가 제공하지 않는 경우 자동으로 생성될 수 있습니다.

## 기본 ID {#section_E8705CC1BDBC47FB8A4FE02293BACFE6}

HTML에 s_objectid가 있다면, 기본 ID의 기본값은 s_objectid로 지정됩니다. 그렇지 않은 경우에는 다음의 매개 변수가 기본 ID로 사용됩니다(아래 나열된 순서대로).

* Innertext
* Alttext
* Title
* Src
* Action

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

## Link region {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

이 새로운 속성을 사용하면 링크가 있는 페이지 영역을 나타내는 문자열을 지정할 수 있습니다.

예를 들어, 웹 페이지의 메뉴 섹션에 있는 "담당자에게 문의" 링크에 대해 사용자는 "메뉴" 영역 매개 변수를 전달할 수 있습니다. 유사하게, 웹 페이지의 바닥글에 있는 "문의하기" 링크의 경우에는 영역 매개 변수를 "footer"로 설정할 수 있습니다.

링크 영역 값은 링크 자체에 설정되지 않지만, 해당 영역을 둘러싸는 DOM HTML 트리 위의 한 HTML 요소에 설정됩니다.
링크 영역을 사용하면 다음과 같은 이점이 있습니다.

* 동일한 기본 ID로 링크를 차별화하는 데 도움이 됩니다.
* 영역에서의 트렌드는 웹 페이지의 다이내믹한 측면이 주는 영향을 덜 받습니다.
* 사용자는 영역 내에서 상위 실적 링크를 볼 수 있습니다. 영역을 앵커로 사용하면, 페이지에 현재 표시되지 않는 링크들의 오버레이를 보여줄 수 있습니다(Ajax, Targeting).
* 한 영역은 많은 웹 페이지에서 사용될 수 있기 때문에 영역이 여러 페이지를 대체할 수 있습니다. 이것은 "내 '제공 제품' 영역이 '여성용' 랜딩 페이지나 '남성용' 랜딩 페이지에서 최고의 성과를 올리나요?"와 같은 질문에 답하는 데에 도움이 됩니다.
* 본질적으로, 영역은 매우 다이내믹한 웹 페이지를 분석하는 데 적절한 차원입니다. 이것은 계속해서 변화하는 링크로 인한 노이즈를 제거하기 때문입니다. 예를 들어 CNN 랜딩 페이지의 "Latest News" 영역에는 변화하는 링크가 많이 있을 수 있습니다. 하지만 이 영역은 항상 같은 위치에 있게 됩니다. 따라서 여러 날에 걸쳐 영역 수준에서 트렌드를 찾는 것은 흥미로울 수 있습니다.

**사용자 지정된 영역 추적**

링크에 대한 영역 매개 변수를 사용자 지정할 수 있습니다(기본값은 링크ID). 태그를 "ID"로 설정하면 "id" 매개 변수를 가진 모든 HTML 요소를 영역으로 사용합니다. 따라서, 영역 태그를 "id"로 설정하면 서로 다른 많은 영역이 반환됩니다(페이지에 있는 서로 다른 "ID"의 수만큼). 또는 구현을 더 많이 사용자 지정하려는 경우, 영역 태그를 "region_id"와 같이 더 구체적으로 설정할 수 있습니다. 

아래에서는 기본 영역 ID 속성 "id"를 사용하는 샘플 HTML을 볼 수 있습니다.

```
<div id="content"> 
  <div id="breaking_news"> 
      <a href="breaking-news.html">...</a> 
   </div> 
 <div id="todays_top_headlines"> 
      <a href="breaking-news.html">...</a> 
   </div> 
```

원할 경우, 이 경우 "lpos"와 같이 임의의 문자열 식별자가 있는 요소에 태그를 지정한 다음, "lpos"라는 이름의 속성을 추가할 수 있습니다.

```
s.ActivityMap.regionIDAttribute="lpos"; 
   
<div id="nav" lpos="navbar"> 
  <ul> 
     <li> Menu Category A 
    <ul> 
      <li><a href="">Menu Item A 1</a> 
      <li><a href="">Menu Item A 2</a> 
     </ul> 
    </li> 
     <li> Menu Category B 
     <ul> 
      <li><a href="">Menu Item B 1</a>  
      <li><a href="">Menu Item B 2</a> 
  
   </ul> 
</ul> 
</div> 
  
<div id="content" > 
  <div id="breaking_news" lpos="breaking_news> 
      <a href="breaking-news.html">...</a> 
   </div> 
 <div id="todays_top_headlines"> 
      <a href="breaking-news.html">...</a> 
   </div> 
</div>
```

## Configuration variables {#section_634197EACD404AC086DF9A03B813C8C3}

다음 변수들은 참조용으로만 제공됩니다. Activity Map은 설치 즉시 적절하게 구성되지만, 다음 변수들을 사용하여 구현을 사용자 지정할 수 있습니다.

<table id="table_7BC8DC3F35CF49288D94BA707F06B283"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 이름 </th> 
   <th colname="col2" class="entry"> 예 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> s. activitymap. regionidattribute </td> 
   <td colname="col2"> 기본값을 "id" 매개 변수로 지정합니다. 이 변수를 다른 매개 변수로 설정할 수 있습니다. </td> 
   <td colname="col3"> s.linkObject의 일부 상위(parent, parent.parent, ...) 요소, 즉 <b>클릭한 요소</b>의 영역 ID로 사용할 태그 속성을 식별하는 문자열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s. activitymap. link </td> 
   <td colname="col2"> 
    <code>// 는 태그 함수 (Clickedelement) {var linkid 에서 "title" 속성만 사용합니다. if (clickedelement &amp; &amp; clickedelement. tagname. touppercase () = = =' a ') {linkid = clickedelement. getattribute (' title '); } return linkid; } </code>
  </td> 
   <td colname="col3"> 클릭한 HTMLElement를 받고, <b>클릭한 링크</b>를 나타내는 문자열 값을 반환해야 하는 함수. <p>반환 값이 false일 경우(null, 정의되지 않음, 빈 문자열, 0), 링크가 추적되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s. activitymap. region </td> 
   <td colname="col2"> 
    <code>// 은 영역 함수 (Clickedelement) {var regionid, classname로 첫 번째 클래스 이름과 연결된 소문자 버전의 태그 이름만 사용합니다. while (clickedelement &amp; &amp; (clickedelement = clickedelement. parentnode)) {regionid = clickedelement. tagname; if (regionid) {return regionid. tolowercase (); }}}}}} </code>
  </td> 
   <td colname="col3"> 클릭한 HTMLElement를 받고, <b>클릭했을 때 링크가 있었던 영역</b>을 나타내는 문자열 값을 반환해야 하는 함수. <p>반환 값이 false일 경우(null, 정의되지 않음, 빈 문자열, 0), 링크가 추적되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.linkExclusions </td> 
   <td colname="col2"> 
    <code>// 특수 Linkexcludes CSS 클래스 &lt; style &gt;. linkexcludes {display: 블록; 높이: 1 px; 왼쪽: -9999 px; 오버플로우: 숨김; 위치: 절대; 너비: 1 px; } &lt;/style &gt; &lt; a href = "next-page.html" &gt; 링크에 필터와 일치하는 숨겨진 텍스트가 없기 때문에 링크가 추적됩니다.&lt;/a &gt; &lt; a href = "next-page.html" &gt; 링크가 s. activitymap. linkexclusions 가 설정되어 있고 이 링크에 필터와 일치하는 텍스트가 숨겨져 있으므로 링크가 추적되지 않았습니다. &lt; span class = "linkexcluded" &gt; exclude-link 1 &lt;/span &gt; &lt;/a &gt; &lt; a href = "next-page.html" &gt; 링크는 s. activitymap. linkexclusions 가 설정되어 있고 이 링크에 필터와 일치하는 텍스트가 있으므로 추적되지 않습니다.  &lt;span class="linkExcluded"&gt;exclude-link2&lt;/span&gt; &lt;/a&gt; &lt;script&gt;   var s = s_gi('samplersid');   s.ActivityMap.linkExclusions = 'exclude-link1,exclude-link2'; &lt;/script&gt; 
    </code> </td> 
   <td colname="col3"> <p>링크 텍스트에서 검색할 문자열의 쉼표 구분 목록을 받는 문자열입니다. 검색되면, 링크는 Activity Map에 의해 추적되지 않도록 제외됩니다. 설정되지 않은 경우에는 Activity Map에 의한 링크 추적을 중지하기 위한 시도가 수행되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.regionExclusions </td> 
   <td colname="col2"> 
    <code>// 이 페이지에서 추적 가능한 링크의 페이지 제외 영역이 Activitymap &lt; div id = "links-included" &gt; &lt; a href = "next-page.html" &gt; 링크가 추적됩니다.&lt;/a &gt; &lt;/div &gt; &lt; div id = "links-excluded" &gt; &lt; a href = "next-page.html" &gt; 링크는 s. activitymap. regionexclusion 이 설정되어 있고 이 링크가 필터와 일치하므로 추적되지 않습니다.&lt;/a&gt; &lt;/div&gt; &lt;script&gt;   var s = s_gi('samplersid');   s.ActivityMap.regionExclusions = 'links-excluded'; &lt;/script&gt;
    </code> </td> 
   <td colname="col3"> <p>영역 텍스트에서 검색할 문자열의 쉼표 구분 목록을 받는 문자열입니다. 검색되면, 링크는 Activity Map에 의해 추적되지 않도록 제외됩니다. 설정되지 않은 경우에는 Activity Map에 의한 링크 추적을 중지하기 위한 시도가 수행되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
