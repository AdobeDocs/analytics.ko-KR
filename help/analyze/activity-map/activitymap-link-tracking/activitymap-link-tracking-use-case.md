---
description: s_objectID 변경을 사용하여 링크 ID를 사용자 지정하고, 영역을 사용자 지정하고, AppMeasurement ActivityMap 모듈 파일을 사용자 지정하여 링크를 차별화할 수 있습니다.
title: 동일한 링크 ID 및 영역을 참조하는 링크 차별화
uuid: f2da0cda-a33b-4a12-8d99-1f58386d6d30
feature: Activity Map
role: 비즈니스 전문가, 관리자
translation-type: tm+mt
source-git-commit: f9d9c7dbaf5fde5bd51c929d927d4cd3f61cb63b
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 61%

---


# 동일한 링크 ID 및 영역을 참조하는 링크 차별화

s_objectID 변경을 사용하여 링크 ID를 사용자 지정하고, 영역을 사용자 지정하고, AppMeasurement ActivityMap 모듈 파일을 사용자 지정하여 링크를 차별화할 수 있습니다.

일례로, 동일한 링크 ID 및 영역에서 Activity Map으로 식별되는 여러 개의 &quot;Buy&quot; 링크가 있다고 하겠습니다.

<table id="table_3020E2C0175D455C84E794CF51BE5A93">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 코드 샘플 </th>
   <th colname="col2" class="entry"> 링크 ID </th>
   <th colname="col3" class="entry"> 영역 </th>
  </tr>
 </thead>
  <tbody>
  <tr>
   <td colname="col1">
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td>
   <td colname="col2">
     <br/>
     <br/>
    구입<br/>
     <br/>
     <br/>
    구입<br/>
     <br/>
     <br/>
    구입<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    recommendation panel<br/>
     <br/>
     <br/>
    recommendation panel<br/>
     <br/>
     <br/>
    recommendation panel<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

사용자는 어떻게 이러한 링크의 값을 차별화하는 웹 페이지와 태그 지정을 사용자 지정할 수 있습니까? 세 가지 옵션이 있습니다. 링크 ID를 사용자 지정하거나, 영역을 사용자 지정하거나, AppMeasurement ActivityMap 모듈 파일을 사용자 지정할 수 있습니다.

## s_objectID를 사용하여 링크 ID 사용자 지정 {#section_01B0D463397B4837B2D46F087A6E5937}

페이지의 링크 또는 링크 위치에 대해 고유한 개체 ID `s_objectID`를 만들면 링크 URL이 아니라 Activity Map 추적을 개선하거나 Activity Map을 사용하여 링크 유형 또는 위치에 대해 보고할 수 있습니다.  변수에 대해 자세히 알려면 [여기](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/vars/page-vars/page-variables.html)를 클릭하십시오.`s_objectID`

>[!IMPORTANT]
>
>Activity Map에서 `s_objectID`을(를) 사용할 때는 후행 세미콜론(`;`)이 필요합니다.
<table id="table_9439A5F320304E439A19842CF3EBA456">
 <thead>
  <tr>
   <th colname="col02" class="entry"> 코드 샘플 </th>
   <th colname="col2" class="entry"> 링크 ID </th>
   <th colname="col3" class="entry"> 영역 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col02">
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product1';"&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt; </code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product2';"&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt; </code><br/>
    <code>&nbsp;&lt;div&gt; </code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product3';"&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td> 
   <td colname="col2">
     <br/>
     <br/>
    Product1<br/>
     <br/>
     <br/>
    Product2<br/>
     <br/>
     <br/>
    Product3<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    recommendation panel<br/>
     <br/>
     <br/>
    recommendation panel<br/>
     <br/>
     <br/>
    recommendation panel<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

## 영역 사용자 지정 {#section_6B1EF302573B445DBAF44176D0A12DB9}

각 &quot;구입&quot; 링크에 자체 영역이 정의되어 있도록 하여 영역을 사용자 지정할 수 있습니다. 이렇게 하려면 각 &quot;Buy&quot; 앵커 태그의 상위 항목 중 하나에 `"id"` 매개 변수를 추가합니다.

>[!NOTE]
>영역 식별자로 `"id"` 매개 변수에 제한되지 않습니다. JavaScript 변수 `"s.ActivityMap.regionIDAttribute"`을 사용하여 자체 식별자를 설정할 수도 있습니다.
>
>
><table id="table_250DB52A869C466B942517BABA1C287B">
 <thead>
  <tr>
   <th colname="col02" class="entry"> 코드 샘플 </th>
   <th colname="col2" class="entry"> 링크 ID </th>
   <th colname="col3" class="entry"> 영역 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col02">
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;a"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;b"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;c"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td> 
   <td colname="col2">
     <br/>
     <br/>
    구입<br/>
     <br/>
     <br/>
    구입<br/>
     <br/>
     <br/>
    구입<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    region a<br/>
     <br/>
     <br/>
    region b<br/>
     <br/>
     <br/>
    region c<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

## AppMeasurement ActivityMap 모듈 파일 사용자 지정 {#section_B933BB9F944E4D5389002908A5A881F8}

>[!CAUTION]
수정한 코드를 테스트하여 제대로 작동하는지 확인하십시오. Adobe는 수정된 코드가 어떻게 동작하는지에 대해 책임이 없습니다.

다음은 AppMeasurement.js 파일에 포함(수정된 형식으로)할 수 있는 **일반** 링크/영역 함수에 대한 두 가지 예입니다.

```
s.ActivityMap.link = function(ele, linkName) {
  if (linkName) {
    return linkName;
  }
  if (ele) {
    if (ele.tagName == 'A' && ele.href) {
      return ele.href;
    }
  }
}
```

`linkName`은(는) `s.tl()`에 대한 호출 중에 전달됩니다.

```
s.ActivityMap.region = function(ele) {
  var className,
  classNames = {
    'header': 1,
    'navbar': 1,
    'left-content': 1,
    'main-content': 1,
    'footer': 1,
  }; 
  while ((ele && (ele = ele.parentNode))) {
    if ((className=ele.className) && classNames[className]) {
      return className;
    }
  }
  return "BODY";
}
```
