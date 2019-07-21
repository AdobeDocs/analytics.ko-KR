---
description: s_objectID 변경을 사용하여 링크 ID를 사용자 지정하고, 영역을 사용자 지정하고, AppMeasurement ActivityMap 모듈 파일을 사용자 지정하여 링크를 차별화할 수 있습니다.
seo-description: s_objectID 변경을 사용하여 링크 ID를 사용자 지정하고, 영역을 사용자 지정하고, AppMeasurement ActivityMap 모듈 파일을 사용자 지정하여 링크를 차별화할 수 있습니다.
seo-title: 동일한 링크 ID 및 영역을 참조하는 링크 차별화
solution: Analytics
title: 동일한 링크 ID 및 영역을 참조하는 링크 차별화
topic: Activity Map
uuid: f 2 da 0 cda-a 33 b -4 a 12-8 d 99-1 f 58386 d 6 d 30
translation-type: tm+mt
source-git-commit: 4f313ae50c4d5a0f3bfec493c2d554bc8614aeef

---


# 동일한 링크 ID 및 영역을 참조하는 링크 차별화

s_objectID 변경을 사용하여 링크 ID를 사용자 지정하고, 영역을 사용자 지정하고, AppMeasurement ActivityMap 모듈 파일을 사용자 지정하여 링크를 차별화할 수 있습니다.

일례로, 동일한 링크 ID 및 영역에서 Activity Map으로 식별되는 여러 개의 "Buy" 링크가 있다고 하겠습니다.

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
    <code>&lt; div id = "recommendation panel" &gt; 
 &lt; div &gt; 
 &lt; a href = "product1.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a href = "product2.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a href = "product3.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; </code>
  </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p> <p> </p>Buy <p> </p> <p> </p> <p>Buy </p> <p> </p> <p> </p> <p>Buy </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p> <p> </p>recommendation Panel <p> </p> <p> </p> <p>recommendation Panel </p> <p> </p> <p> </p> <p>recommendation Panel </p> </td> 
  </tr> 
 </tbody> 
</table>

사용자는 어떻게 이러한 링크의 값을 차별화하는 웹 페이지와 태그 지정을 사용자 지정할 수 있습니까? 세 가지 옵션이 있습니다. 링크 ID를 사용자 지정하거나, 영역을 사용자 지정하거나, AppMeasurement ActivityMap 모듈 파일을 사용자 지정할 수 있습니다.

## s_objectID를 사용하여 링크 ID 사용자 지정 {#section_01B0D463397B4837B2D46F087A6E5937}

페이지의 링크 또는 링크 위치에 대한 고유 개체 ID를 작성함으로써 Activity Map 추적을 개선하거나 Activity Map을 사용하여, 링크 URL보다는 링크 유형 또는 위치에 대해 보고할 수 있습니다. s_objectID 변수에 대해 자세히 알려면 [여기](https://marketing.adobe.com/resources/help/en_US/sc/implement/s_objectID.html)를 클릭하십시오.

>[!IMPORTANT]
>
>Activity Map에서 s_ objectid를 사용할 때에는 후행 세미콜론 (;) 이 필요합니다.

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
    <code>&lt; div id = "recommendation panel" &gt; 
 &lt; div &gt; 
 &lt; a onclick = "s_ objectid =' product 1 '; " href = "product1.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a onclick = "s_ objectid =' product 2 '; " href = "product2.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a onclick = "s_ objectid =' product 3 '; " href = "product3.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; </code>
  </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p>Product1 <p> </p> <p> </p> <p>Product2 </p> <p> </p> <p> </p> <p>Product 3 </p> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p> <p>recommendation panel </p> <p> </p> <p> </p> <p>recommendation panel </p> <p> </p> <p> </p> <p>recommendation panel </p> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 영역 사용자 지정 {#section_6B1EF302573B445DBAF44176D0A12DB9}

각 "buy" 링크에 자체 영역이 정의되어 있도록 하여 영역을 사용자 지정할 수 있습니다. 이렇게 하려면, "id" 매개 변수를 각 "Buy" 앵커 태그의 상위 항목 중 하나에 추가하십시오.

>[!NOTE]
>
>영역 식별자로 "id" 매개 변수로 엄격하게 제한되지 않습니다. JavaScript 변수 "s. activitymap. regionidattribute" 를 사용하여 고유한 식별자를 설정할 수도 있습니다.

<table id="table_250DB52A869C466B942517BABA1C287B"> 
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
    <code>&lt; div id = "recommendation panel" &gt; 
 &lt; div id = "region a" &gt; 
 &lt; a href = "product1.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div id = "region b" &gt; 
 &lt; a href = "product2.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div id = "region c" &gt; 
 &lt; a href = "product3.html" &gt; buy &lt;/a &gt; 
 &lt;/div &gt; </code>
  </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p> <p>Buy </p> <p> </p> <p> </p> <p>Buy </p> <p> </p> <p> </p> <p>Buy </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p>region a <p> </p> <p> </p> <p>region b </p> <p> </p> <p> </p> <p>region c </p> </td> 
  </tr> 
 </tbody> 
</table>

## AppMeasurement ActivityMap 모듈 파일 사용자 지정 {#section_B933BB9F944E4D5389002908A5A881F8}

>[!CAUTION]
>
>수정된 코드를 테스트하여 제대로 작동하는지 확인합니다. Adobe는 수정된 코드가 어떻게 동작하는지에 대해 책임이 없습니다.

다음은 Appmeasurement. js 파일에 포함될 수 있는** 범용** 링크/영역 함수에 대한 두 가지 예입니다.

```
s.ActivityMap.link = function(ele,linkName){ 
if(linkName){ 
return linkName; 
} 
if(ele){ 
if(ele.tagName == 'A' && ele.href){ 
return ele.href; 
} 
} 
} 
```

s.tl 호출 동안 linkName이 전달됩니다.

```
s.ActivityMap.region = function(ele){ 
var className, 
classNames = { 
'header': 1, 
'navbar': 1, 
'left-content': 1, 
'main-content': 1, 
'footer': 1, 
}; 
  while( (ele && (ele = ele.parentNode))){ 
if( (className=ele.className) && classNames[className]){ 
return className; 
} 
} 
return "BODY"; 
} 
```

