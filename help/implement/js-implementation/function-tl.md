---
description: JavaScript용 AppMeasurement 파일에 설정된 매개 변수를 기반으로 파일 다운로드 및 종료 링크를 자동으로 추적할 수 있습니다.
keywords: Analytics 구현
seo-description: JavaScript용 AppMeasurement 파일에 설정된 매개 변수를 기반으로 파일 다운로드 및 종료 링크를 자동으로 추적할 수 있습니다.
seo-title: s.tl() 함수 - 링크 추적
solution: Analytics
subtopic: 링크 추적
title: s.tl() 함수 - 링크 추적
topic: 개발자 및 구현
uuid: F 28 F 071 A -8820-4 F 74-89 CD-FD 2333 A 21 F 22
translation-type: tm+mt
source-git-commit: acaea784c977d7ff438f84faf8af5a3c605e3cf5

---


# s.tl() 함수 - 링크 추적

File downloads and exit links can be automatically tracked based on parameters set in the [!DNL AppMeasurement] for JavaScript file.

## s.tl() 함수 - 링크 추적 {#concept_EA13689CB8EE4F308FC89A1293046D5E}

File downloads and exit links can be automatically tracked based on parameters set in the [!DNL AppMeasurement] for JavaScript file.

필요한 경우 아래에 설명했듯이 사용자 지정 링크 코드를 사용하여 이러한 유형의 링크를 수동으로 추적할 수 있습니다. 또한 사용자 지정 링크 코드를 사용하여 다양한 추적 및 보고 요구에 활용할 수 있는 일반 사용자 지정 링크를 추적할 수 있습니다.

## s.tl() 매개 변수 참조 {#section_DDF19EE3ACE24EFAB2D65CD4B0D7DBC4}

<!-- Meike, I converted a table within to table to this section. Please check against orginal file -Bob -->

**this**

첫 번째 인수는 항상 this(기본값)나 true로 설정해야 합니다. 이 인수는 클릭되는 개체를 참조하며, "this"로 설정되면 링크의 HREF 속성을 참조합니다.

HREF 속성이 없는 개체에 대한 링크 추적을 구현하는 경우 항상 이 인수를 "this." 로 설정해야 합니다.

보통 링크를 클릭하면 방문자가 현재 페이지를 나가기 때문에 500ms 지연을 사용하여 사용자가 페이지를 떠나기 전에 이미지 요청이 Adobe로 전송되도록 합니다. 이러한 지연은 페이지를 나갈 때만 필요하지만 일반적으로 s.tl() 함수를 호출할 때도 존재합니다. 지연을 사용하지 않으려면 s.tl() 함수를 호출할 때 키워드 'true'를 첫 번째 매개 변수로 전달하십시오.

**linkType**

`s.tl(this,linkType,linkName, variableOverrides, doneAction)`

linkType에는 캡처할 링크의 유형에 따라, 세 가지 가능한 값이 있습니다. 링크가 다운로드나 종료 링크가 아니라면, 사용자 지정 링크 옵션을 선택해야 합니다.

| 유형 | linkType 값 |
|--- |--- |
| 파일 다운로드 | 'd' |
| 종료 링크 | 'e' |
| 사용자 지정 링크 | 'o' |

**linkName**

이것은 최대 100자를 사용하는 어떤 사용자 지정 값도 될 수 있습니다. 이 값은 링크가 해당 보고서에 어떻게 표시되는지를 결정합니다.

**variableOverrides**

(선택 사항. 사용하지 않을 경우 null 전달) 이 변수를 사용하면 이러한 단일 호출에 대한 변수 값을 변경할 수 있습니다. 다른 [!DNL AppMeasurement] 라이브러리와 유사합니다.

**useForcedLinkTracking**

이 플래그는 일부 브라우저에 대한 강제 링크 추적을 비활성화하는 데 사용됩니다. 강제 링크 추적은 FireFox 20 이상과 WebKit 브라우저에 대해 기본적으로 활성화됩니다.

기본값 = true

예: `s.useForcedLinkTracking& = false`

**forcedLinkTrackingTimeout**

`s.tl`로 전달된 doneAction을 수행하기 전에 완료할 수 있도록 추적을 기다리는 최대 밀리초 수입니다. 이 값은 최대 대기 시간을 지정합니다. 이 시간 초과 전에 추적 링크 호출이 완료되면 doneAction이 즉시 실행됩니다. 추적 링크 호출이 완료되지 않고 있다는 것을 확인한 경우 이 시간 초과를 늘려야 할 수도 있습니다.

기본값 = 250

예: `s.forcedLinkTrackingTimeout&nbsp;=&nbsp;500`

**doneAction**

useForcedLinkTracking이 활성화되면 추적 링크 호출이 완료된 후 탐색 작업을 지정하여 실행하는 선택 매개 변수입니다.

구문:

`s.tl(linkObject,linkType,linkName,variableOverrides,doneAction)`

 doneAction  : (선택 사항) 링크 추적 호출이 전송되거나 시간 초과된 후에 다음 코드로 지정된 값을 기반으로 취할 동작을 지정합니다.

`s.forcedLinkTrackingTimeout`

doneAction 변수는 문자열 navigate가 될 수 있으며, 이는 메서드가 `document.location`을 linkObject의 href 특성으로 설정하는 원인이 됩니다. 또한 doneAction 변수는 고급 사용자 지정을 허용하는 함수가 될 수 있습니다.

앵커 onclick 이벤트에 doneAction에 대한 값을 제공하는 경우, 기본 브라우저 탐색을 방지할 수 있도록 `s.tl` 호출 후에 false를 반환해야 합니다.

기본 동작을 미러링하고 href 특성에 의해 지정된 URL을 따르려면 navigate의 문자열을 doneAction으로 제공해야 합니다.

선택 사항으로, doneAction으로 이 함수를 전달하여 탐색 이벤트를 처리하도록 자체 함수를 제공할 수 있습니다 .

예:

```js
<a href="..." onclick="s.tl(this,'o','MyLink',null,'navigate');return false">Click Here</a> <a href="#" onclick="s.tl(this,'o','MyLink',null,function(){if(confirm('Proceed?'))document.location=...});return false">Click Here</a>
```

**예**

다음의 [!UICONTROL s.tl()] 함수 호출 예에서는 기본값 500ms 지연을 사용하여, 페이지를 나가기 전에 데이터가 수집되도록 합니다.

```js
s.tl(this,'o','link name');
```

다음 예에서는 사용자가 페이지를 나가지 않을 예정인 경우 또는 클릭되는 개체에 HREF가 없을 때마다 500ms 지연을 비활성화합니다.

```js
s.tl(true,'o','link name');
```

500ms 지연이 최대 길이입니다. 요청을 받은 이미지가 500ms 이내에 반환되면, 지연이 즉시 중단됩니다. 이렇게 되면 방문자는 다음 페이지나 페이지 내 다음 동작으로 이동할 수 있습니다.

다음 예는 WebKit 브라우저에서의 사용자 지정 링크 처리에 대한 것입니다.

```js
<a href="..." onclick="s.tl(this,'o','MyLink',null,'navigate');return false">Click Here</a>
```

```js
<a href="#"  onclick="s.tl(this,'o','MyLink',null,  
function(){if(confirm('Proceed?'))document.location=...});return false">Click Here</a>
```

>[!NOTE]
>
>사용자 지정 링크 코드의 사용은 웹 사이트 및 보고 요구 사항에 따라 달라지는 경우가 많습니다. 사용자 지정 링크 코드를 구현하기 전에 Adobe 컨설턴트나 고객 지원에 문의하여 사용할 수 있는 기능과 비즈니스 요구를 기준으로 이 기능을 이용하는 최선의 방법을 이해할 수 있습니다.

사용자 지정 링크 코드를 사용하여 링크를 추적하는 기본 코드가 다음 예제에 나와 있습니다.

```js
<a href="index.html" onClick="s.tl(this,'o','Link Name')">My Page</a>
```

>[!NOTE]
>
>[!UICONTROL s_ gi] 함수는 보고서 세트 ID를 함수 매개 변수로 포함해야 합니다. [!DNL rsid]를 고유한 보고서 세트 ID로 바꾸십시오.

>[!NOTE]
>
>링크 이름 매개 변수가 정의되지 않은 경우 링크의 URL ("this" 개체에서 결정됨) 이 링크 이름으로 사용됩니다.

[!DNL Analytics] 변수는 사용자 지정 링크 코드의 일부로 정의할 수 있습니다.

## 종료 링크 및 파일 다운로드 자동 추적 {#concept_DF078C5C1B004695B3B7C4536C99D4B2}

파일 다운로드 파일 형식 및 종료 링크를 정의하는 매개 변수를 기준으로 파일 다운로드 및 종료 링크를 자동으로 추적하도록 JavaScript를 구성할 수 있습니다.

<!-- 

link_automatic.xml

 -->

자동 추적을 제어하는 매개 변수는 다음과 같습니다.

```js
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,doc,pdf,xls" 
s.linkInternalFilters="javascript:,mysite.com,[more filters here]" 
s.linkLeaveQueryString=false 
```

매개변수 *`trackDownloadLinks`* 그리고 *`trackExternalLinks`* 자동 파일 다운로드 및 종료 링크 추적이 활성화되었는지 확인합니다. When enabled, any link with a file type matching one of the values in *`linkDownloadFileTypes`* is automatically tracked as a file download. Any link with a URL that does not contain one of the values in *`linkInternalFilters`* is automatically tracked as an exit link.

In JavaScript H.25.4 (released February 2013), automatic exit link tracking was updated to always ignore links with `HREF` attributes that start with `#`, `about:`, or `javascript:`.

## Example 1 {#section_504D163608E14B25A8B4CA9D615C6735}

The file types [!DNL jpg] and [!DNL aspx] are not included in *`linkDownloadFileTypes`* above, therefore no clicks on them are automatically tracked and reported as file downloads.

The parameter *`linkLeaveQueryString`* modifies the logic used to determine exit links. When *`linkLeaveQueryString`*=false, exit links are determined using only the domain, path, and file portion of the link URL. When *`linkLeaveQueryString`*=true, the query string portion of the link URL is also used to determine an exit link.

## Example 2 {#section_25660B64E28248A0BC982B2AF5603C0E}

다음과 같이 설정하면 아래 예제가 종료 링크로 카운트됩니다.

```js
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=false 
 
//HTML file 
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site!</a> 
```

## 예제 3 {#section_2A78D05162D640169844A7D1E9799BAA}

다음과 같이 설정하면 아래 링크가 종료 링크로 카운트되지 않습니다.

```js
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=true 
 
//HTML  
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site</a> 
```

>[!NOTE]
>
>단일 링크는 파일 다운로드 또는 종료 링크로만 추적할 수 있으며, 파일 다운로드의 우선 순위가 높습니다. If a link is both an exit link and file download based on the parameters *`linkDownloadFileTypes`* and *`linkInternalFilters`*, it is tracked and reported as a file download and not an exit link. 다음 표에 파일 다운로드 및 종료 링크에 대한 자동 추적이 요약되어 있습니다.

## 사용자 지정 링크 코드를 사용하여 수동으로 링크 추적{#concept_7113B5D037BE4622B6934554C6D18F96}에 추가했습니다 

자동 추적을 적용할 수 없거나 자동 추적이 불충분한 상황에서 사용자 지정 링크 코드를 사용하여 파일 다운로드, 종료 링크 및 사용자 지정 링크를 추적할 수 있습니다.

<!-- 

link_manual.xml

 -->

사용자 지정 링크 코드는 보통 [!UICONTROL onClick] 이벤트 핸들러를 링크에 추가하거나, 코드를 기존 루틴에 추가하여 구현합니다. 기본적으로 어떤 JavaScript 이벤트 핸들러나 함수에서든 구현할 수 있습니다.

Link Tracking consists of calling the [!DNL AppMeasurement] for JavaScript function whenever the user performs actions that generate data you want to capture. 함수 [!UICONTROL s.tl()]은 [!UICONTROL onClick]이나 [!UICONTROL onChange]와 같은 이벤트 핸들러에서 또는 별도의 함수에서 바로 호출됩니다. 이 [!UICONTROL s.tl()] 함수에는 5개의 인수가 있습니다. 처음 3개는 필수 인수입니다.

```js
s.tl(this,linkType,linkName, variableOverrides, doneAction)
```

## FireFox 및 WebKit 브라우저에서의 사용자 지정 링크 추적 {#section_F2B9A2A3CC1F4BB9A64456BC39FC50B9}

JavaScript H.25에는 WebKit 브라우저(Safari 및 Chrome)에서 링크 추적이 성공적으로 완료되도록 해주는 업데이트가 포함되어 있습니다. JavaScript H.26에는 FireFox 20 이상에서 링크 추적이 성공적으로 완료되도록 해주는 업데이트가 포함되어 있습니다.

이 업데이트 후에는 자동 추적되는([!DNL s.trackDownloadLinks] 및 [!DNL s.trackExternalLinks]로 판별됨)다운로드 및 종료 링크가 성공적으로 추적됩니다. 수동 JavaScript 요청을 사용하여 사용자 링크를 추적할 경우 이러한 요청이 작성되는 방식을 변경해야 합니다. 예를 들어, 종료 및 다운로드 링크는 종종 다음과 유사한 코드를 사용하여 추적됩니다.

```js
<a href="https://anothersite.com" onclick="s.tl(this,'e','AnotherSite',null)">
```

Internet Explorer는 추적 링크 호출을 실행하고 새 페이지를 엽니다. 다른 브라우저는 새 페이지가 열릴 때 추적 링크 호출 실행을 취소할 수 있습니다. 이렇게 되면 추적 링크 호출이 완료되지 않는 경우가 있습니다.

이 동작을 해결하기 위해 H.25(2012년 7월 발표)는 추적 링크 호출이 완료될 때까지 이러한 동작을 수행하는 브라우저가 대기하도록 하는 오버로드된 추적 링크 메서드([!DNL s.tl])를 포함합니다. 이 새 메서드는 기본 브라우저 작업을 사용하는 대신, 추적 링크 호출을 실행하고 탐색 이벤트를 처리합니다. 이 오버로드된 메서드에는 링크 추적 호출이 완료될 때 수행될 작업을 지정하는 [!UICONTROL doneAction]이라는 추가 매개 변수가 필요합니다.

이 새 메서드를 사용하려면 다음과 같이, 추가 [!DNL s.tl]doneAction[!UICONTROL  매개 변수로 ]에 대한 호출을 업데이트하십시오.

```js
<a href="https://anothersite.com"  
onclick="s.tl(this,'e','AnotherSite',null,'navigate');return false">
```

navigate를 [!UICONTROL doneAction]으로 전달하면 기본 브라우저 동작이 미러링되고 추적 호출이 완료될 때 href 특성으로 지정된 URL이 열립니다.

JavaScript H.25.4(2013년 2월 발표)에서는, `useForcedLinkTracking`이 활성화되면 추적되는 링크에 다음의 범위 제한을 추가했습니다. 자동 강제 링크 추적은 다음의 경우에만 적용됩니다.

* `<A>``<AREA>` 태그가 표시됩니다.
* 태그에 `HREF` 특성이 반드시 있어야 함.
* The `HREF` can't start with `#`, `about:`, or `javascript:`.
* `TARGET` 속성을 설정하면 안 됩니다. `TARGET` 또는 현재 창 `_self`(, `_top`또는의 `window.name`값) 를 참조해야 합니다.

## 이미지 요청을 사용한 링크 추적 {#concept_FF31C8D1B3DF483D853BF0A9D637F02F}

이미지 요청을 구성하면 s.tl() 함수를 호출하지 않고도 링크를 추적할 수 있습니다.

<!-- 

link_img.xml

 -->

이미지 요청은 "pe" 매개 변수를 다음과 같이 이미지 요청 src 매개 변수에 추가하여 하드 코딩됩니다.

```
pe=[type]
```

Where `[type]` is replaced with the type of link you want to track:

* lnk_d = download
* lnk_e = exit
* lnk_o = custom

또한 링크 URL은 다음과 같이 pev1 매개 변수에서 URL을 전달하여 지정할 수 있습니다.

```
pev1=mylink.com
```

링크 이름은 pev2 매개 변수에서 이름을 전달하여 지정할 수 있습니다.

```
pev2=My%20Link
```

예:

```
<img src="https://collectiondomain.112.2o7.net/b/ss/reportsuite/1/H.25.3--NS/0?pe=lnk_e&pev1=othersite.com&pev2=Offsite%20Link" width="1" height="1" border="0" />
```

## 파일 다운로드, 종료 링크, 사용자 지정 링크에 대한 추가 변수 설정 {#concept_8DD06387D5234A52A6E361572FAA2DF6}

Two parameters (  and ) control which [!DNL Analytics] variables are set for file downloads, exit links, and custom links.

<!-- 

link_variables.xml

 -->

이 매개 변수들은 기본적으로 다음과 같이 JS 파일 내에 설정됩니다.

```js
s.linkTrackVars="None"
```

```js
s.linkTrackEvents="None"
```

the *`linkTrackVars`* 매개 변수에는 모든 파일 다운로드, 종료 링크 및 사용자 지정 링크와 함께 추적할 각 변수가 포함되어야 합니다. The *`linkTrackEvents`* parameter should include each event you want to track with every file download, exit link, and custom link. 이 링크 유형 중 하나가 발생하면, 식별된 각 변수의 현재 값이 추적됩니다.

예를 들어 모든 파일 다운로드, 종료 링크 및 사용자 지정 링크로 prop1, eVar1, event1을 추적하려는 경우, 글로벌 JS 파일에 다음과 같은 설정을 사용하십시오.

```js
s.linkTrackVars="prop1,eVar1,events"
```

```js
s.linkTrackEvents="event1"
```

>[!NOTE]
>
>The variable *`pageName`* cannot be set for a file download, exit link, or custom link, because each of the link types is not a page view and does not have an associated page name.

>[!NOTE]
>
>If *`linkTrackVars`* (or *`linkTrackEvents`*) is null (or an empty string), all [!DNL Analytics] variables (or events) that are defined for the current page are tracked. 이렇게 되면 각 변수의 인스턴스가 의도치 않게 부풀려지므로 이렇게 되지 않도록 해야 합니다.

## 우수 사례 {#section_DA3CA596792E4BD6B5FFE89BCE0E617D}

The settings for *`linkTrackVars`* and *`linkTrackEvents`* within the JS file affect every file download, exit link, and custom link. 변수(또는 이벤트)가 현재 페이지에 적용되지만 특정 파일 다운로드, 종료 링크 또는 사용자 지정 링크와 관계없는 경우 각 변수 및 이벤트 인스턴스가 부풀려질 수 있습니다.

적절한 변수가 사용자 지정 링크 코드로 설정되도록 하기 위해 다음과 같이, 사용자 지정 링크 코드 내에서  *`linkTrackVars`* and *`linkTrackEvents`* within the custom link code, as as:

```js
<a href="index.html" onClick=" 
var s=s_gi('rsid'); 
s.linkTrackVars='prop1,prop2,eVar1,eVar2,events'; 
s.linkTrackEvents='event1'; 
s.prop1='Custom Property of Link'; 
s.events='event1'; 
s.tl(this,'o','Link Name'); 
">My Page 
```

The values of *`linkTrackVars`* and *`linkTrackEvents`* override the settings in the JS file and ensure only the variables and events specified in the custom link code are set for the specific link.

>[!NOTE]
>
>위의 예에서, prop 1에 대한 값은 사용자 지정 링크 코드 자체 내에서 설정됩니다. prop2의 값은 페이지에 설정된 변수의 현재 값에서 가져옵니다.

## 사용자 지정 링크 코드와 함께 함수 호출 사용 {#concept_DB662C93B3ED415DB72C80270502BE5D}

사용자 지정 링크 코드의 복잡한 특성 때문에 내장된 JavaScript 함수(페이지 또는 링크된 JavaScript 파일에 정의됨)에 코드를 통합하여 [!UICONTROL onClick] 핸들러 내에 함수 호출을 지정할 수 있습니다.

<!-- 

link_functions.xml

 -->

For example, you could insert the following two functions in your `AppMeasurement.js` file, just below the `s_doPlugins()` function, and then use them throughout your site:

```js
/* Set Click Interaction values (with timeout - H25 code and higher*/ 

function trackClickInteraction(name){ 
    var s=s_gi('rsid'); 
    s.linkTrackVars='prop42,prop35'; 
    s.prop42=name; 
    s.prop35=s.pageName; 
    s.tl(true,'o','track interaction',null,'navigate'); 
}
```

```js
/* Set Click Interaction values (without timeout - pre H25 code*/ 
 
function trackClickInteraction(name){ 
    var s=s_gi('rsid'); 
    s.linkTrackVars='prop42,prop35'; 
    s.prop42=name; 
    s.prop35=s.pageName; 
    s.tl(true,'o','track interaction'); 
}
```

>[!NOTE]
>
>필요한 경우 링크 유형 및 링크 이름을 JavaScript 함수의 추가 매개 변수로 전달할 수 있습니다.

이러한 함수 호출을 위해 다음과 유사한 코드를 사용할 수 있습니다.

```
<a href=”https://www.your-site.com/some_page.php” onclick=”trackClickInteraction('this.href');”>Link Text</a>
```

## 중복 링크 카운트 방지 {#section_9C3F73DE758F4727943439DED110543C}

링크가 자동 파일 다운로드나 종료 링크 추적에 의해 정상적으로 링크가 캡처되는 상황에서 링크가 두 번 카운트될 가능성이 있습니다.

예를 들어 PDF 다운로드를 자동으로 추적하는 경우 다음 코드가 중복 다운로드 카운트를 일으킬 수 있습니다.

```js
function trackDownload(obj) { 
 var s=s_gi('rsid'); 
 s.linkTrackVars='None'; 
 s.linkTrackEvents='None'; 
 s.tl(obj,'d','PDF Document'); 
}
```

링크를 두 번 카운트하지 않도록 다음과 같이 수정한 JavaScript 함수를 사용하십시오:

```js
<script language=JavaScript> 
function linkCode(obj) { 
 var s=s_gi('rsid'); 
 s.linkTrackVars='None'; 
 s.linkTrackEvents='None'; 
 var lt=obj.href!=null?s.lt(obj.href):""; 
 if (lt=="") { s.tl(obj,'d','PDF Document'); } 
}
```

위 코드에서 마지막 두 행은 자동 추적 동작만이 발생하도록 사용자 지정 링크 코드의 동작을 수정하여, 두 번 카운트할 가능성을 제거합니다.

## useForcedLinkTracking이 있는 팝업 창 {#concept_0AC4BA3A64B84CCB8D9A6021A022D1C3}

When `useForcedLinkTracking` is enabled, [!DNL AppMeasurement] overrides the default link behavior on some browsers to prevent the track link call from being canceled when the new page opens. [!DNL AppMeasurement] 기본 브라우저 작업을 사용하는 대신 추적 링크 호출을 실행하고 탐색 이벤트를 수동으로 처리합니다.

<!-- 

link_popups.xml

 -->

When tracking some links that open a popup window, the Chrome built-in popup blocker might prevent [!DNL AppMeasurement] from opening a popup window that would normally be allowed. To avoid this, add a `target="_blank"` attribute to calls that open a window:

```
<a href="./popup.html" target="_blank" onClick="<a href="./popup.html" onclick="s.tl(this,'o','popup',null,'navigate');javascript:window.open('./popup.html','popup','width=550,height=450'); 
return false;">
```

그러면 예상대로 링크를 추적하고 팝업을 열 수 있습니다.

## URL 단축기의 링크 {#concept_CD792362A8E04448B452BE9A18772024}

URL 단축기 서비스의 링크(bit.ly 등)는 일반적으로 페이지 보기나 레퍼러로서 추적되지 않습니다. 이러한 서비스는 전체 URL을 사용하는 301/302 리디렉션을 웹 브라우저에 반환합니다. 이렇게 되면 웹 브라우저는 별도의 새 요청을 전체 URL로 보냅니다. 단축기가 더 이상 루프에 없고 리디렉션 서비스가 URL을 가져오는 데 사용되었음을 가리키는 내용이 요청에 없으므로 원래 레퍼러는 유지됩니다.

<!-- 

link_shortener.xml

 -->

다양한 서비스를 사용할 수 있으므로, 사이트에서 사용 중인 구체적인 시나리오를 테스트하여 서비스에 사용된 리디렉션 메커니즘을 결정하는 것이 좋습니다.

## doPlugins의 링크 추적 변수 {#concept_B5AC1D4372AA4A7D8C7871453A4F1215}

링크 추적을 관리할 수 있도록, `doPlugins` 함수가 실행되기 전에 다음 변수가 채워집니다.

<!-- 

util_linkhandler.xml

 -->

`doPlugins` 내부에서 다음 값들을 사용하여 링크 추적 행동을 수정할 수 있습니다. 예를 들어 추적을 취소하거나, 추적 요청에 변수를 더 추가할 수 있습니다.

<table id="table_55CCF4F2BF474FD3B703C926B896B392"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 영향 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> linkType </td> 
   <td colname="col2"> <p>자동으로 결정된 링크 유형이 들어 있습니다(있을 경우). 다음 중 하나로 설정할 수 있습니다. </p> 
    <ul id="ul_81ACB5D00D774E86AFD22C61AD4D0E2C"> 
     <li id="li_52B6F2B124024DEFB422D1E9E97254C0">d (다운로드) </li> 
     <li id="li_E842C2E64F034181A364C639C30451FD">e (종료) </li> 
     <li id="li_3263F378CE65407E81B6C5C597CED1E8">o (사용자 지정/기타) </li> 
    </ul> <p>이미지 요청의 <code>pe</code> 매개 변수입니다. </p> </td> 
   <td colname="col3"> <p><code>linkURL</code> 또는 <code>linkName</code>으로 설정하면, 서버 호출이 다운로드, 사용자 지정 또는 종료 링크로서 전송됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> linkName </td> 
   <td colname="col2"> <p>사용자 지정, 다운로드 또는 종료 링크 보고서에 나타날 이름. 100자에서 잘리며, 어떤 문자열로도 설정할 수 있습니다. </p> <p>이미지 요청의 <code>pev2</code> 매개 변수입니다. </p> </td> 
   <td colname="col3"> <p> <code>linkType</code>으로 설정하면, 이미지 요청이 다운로드, 사용자 지정 또는 종료 링크로서 전송됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> linkURL </td> 
   <td colname="col2"> <p>linkName이 없는 경우 이름 역할을 하는 링크의 URL입니다. 어떤 URL 문자열로도 설정할 수 있습니다. </p> <p>이미지 요청의 <code>pev1</code> 매개 변수입니다. </p> </td> 
   <td colname="col3"> <p><code>linkType</code>으로 설정하면, 이미지 요청이 다운로드, 사용자 지정 또는 종료 링크로서 전송됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> linkObject </td> 
   <td colname="col2"> <p>참조를 위해 클릭한 개체 읽기 전용입니다. </p> </td> 
   <td colname="col3"> <p>측정에 직접적인 영향이 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

```js
function s_doPlugins(s) { 
    if (s.linkType == "d" && s.linkURL.indexOf(".aspx?f=") { 
        //special tracking for .aspx file download script 
        s.eVar11 = s.linkURL.substring(s.linkURL.lastIndexOf("?f=") + 3, s.linkURL.length); 
    } 
  
    else if (s.linkType == "o" ) { 
        // note: linkType is set to "o" only if you make a custom call 
        // to s.tl() and set the link type to "o". Automatically tracked 
        // links are set to "d" or "e" only. 
        s.eVar10 = s.LinkURL; 
    } 
}
```

## 파일 다운로드, 종료 링크 및 사용자 지정 링크의 유효성 확인 {#concept_0B43AD582D3E470899FCCB58E44D3D49}

다운로드, 종료 및 사용자 지정 링크의 유효성을 철저히 확인하려면 패킷 분석기를 사용하여 링크를 실시간으로 검사할 것을 권장합니다.

<!-- 

downloads_validate.xml

 -->

파일 다운로드, 종료 링크 및 사용자 지정 링크는 페이지 보기가 아니므로 [!UICONTROL DigitalPulse Debugger] 도구를 사용하여 매개 변수 및 변수 설정을 확인할 수 없습니다. 추적 링크 데이터를 보려면 [패킷 분석기를](../../implement/impl-testing/packet-monitor.md#concept_490DF35E06D44234A91B5FC57C0BF258) 참조하십시오.
