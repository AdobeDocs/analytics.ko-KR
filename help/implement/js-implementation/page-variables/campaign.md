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



# campaign

 변수는 사이트로 방문자를 유도하는 데 사용된 마케팅 캠페인을 식별합니다. 이 변수의 값은 대개 쿼리 문자열 매개 변수에서 가져옵니다.

<!-- 

campaign.xml

 -->

**매개 변수**

<table id="table_A35175678B6C4D3D86287199AFBE6803"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>255바이트 </p> </td> 
   <td> <p>v0 </p> </td> 
   <td> <p>전환 &gt; 캠페인 &gt; 추적 코드 </p> </td> 
   <td> <p>"" </p> </td> 
  </tr> 
 </tbody> 
</table>

마케팅 캠페인의 모든 요소에는 연관된 고유 추적 코드가 있습니다. 예를 들어 유료 검색 엔진 키워드에는 112233 추적 코드가 있습니다. 누군가 112233 추적 코드가 있는 키워드를 클릭하고 해당 웹 사이트로 연결되면 *`campaign`* 변수가 추적 코드를 기록합니다.

다음과 같이 *`campaign`* 변수를 채우는 두 가지 기본 방법이 있습니다.

* JavaScript 파일에서 사용되는 [!UICONTROL getQueryParam] 플러그인은 URL의 쿼리 문자열 매개 변수를 검색합니다. [!UICONTROL getQueryParam] 플러그인에 대한 자세한 내용은 [구현 플러그인](/help/implement/js-implementation/plugins/impl-plugins.md).

* 웹 페이지에서 HTML의 *`campaign`* 변수에 값을 지정합니다.

어느 방법으로 *`campaign`* 변수를 채우든 뒤로 단추 트래픽이 캠페인 요소에서 실제 클릭스루 수를 부풀릴 수 있습니다.

방문자가 유료 검색 키워드를 클릭하여 사이트에 들어올 때를 예로 들어봅시다. 방문자가 랜딩 페이지에 도착할 때 URL에는 해당 키워드의 추적 코드를 식별하는 쿼리 문자열 매개 변수가 들어 있습니다. 방문자가 다른 페이지로 가는 링크를 클릭하지만 즉시 [뒤로] 단추를 클릭하여 랜딩 페이지로 다시 돌아갑니다. 방문자가 랜딩 페이지에 두 번째로 도착할 때 쿼리 문자열 매개 변수가 포함된 URL이 추적 코드를 다시 식별합니다. 그리고 두 번째 클릭스루가 등록되고 그에 따라 클릭스루의 수가 잘못 부풀려집니다.

클릭스루가 이렇게 부풀려지지 않도록 하려면 [!UICONTROL getValOnce] 플러그인을 사용하여 각 캠페인 클릭스루가 세션당 한 번씩만 계산되도록 하는 것이 좋습니다. [!UICONTROL getValOnce] 플러그인에 대한 자세한 내용은 [구현 플러그인](/help/implement/js-implementation/plugins/impl-plugins.md).

**구문 및 가능한 값** {#section_91A141841A6D4711A1EE08A6145A301D}

```js
s.campaign="112233"
```

*`campaign`* 변수에는 다른 모든 변수와 동일한 제한 사항이 있습니다. 따라서 값을 표준 ASCII 문자로 제한하는 것이 좋습니다.

**대/소문자 구분** {#section_112A9A0F886148B6BEF9A7C94BE0A36F}

eVar는 대/소문자를 구분하지는 않지만 처음 사용한 대/소문자대로 표시됩니다. 예를 들어 eVar1을 처음 사용할 때 "Logged In"으로 설정되었지만, 그 이후의 모든 사용에서는 "logged in"으로 전달되는 경우, 보고서는 항상 "Logged In"을 eVar의 값으로 보여 줍니다.

**예** {#section_705A25D05F6848E29C78320247AECB5F}

```js
s.campaign="112233"
```

```js
s.campaign=s.getQueryParam('cid');
```

**구성 설정** {#section_4083F281968443169EAF8C0E8529D7BC}

각 캠페인 값은 한 사용자에 대해 활성화 상태로 유지되며, 만료되기 전까지 해당 사용자의 활동과 성공 이벤트에 대한 크레딧을 받습니다. 관리 콘솔에서 캠페인 변수의 만료를 변경할 수 있습니다.

**함정, 질문 및 팁** {#section_94B5C4BF9DE84BA3A16F9E9E9D197F0C}

* 클릭스루가 부풀려지지 않도록 하려면 [!UICONTROL getValOnce] 플러그인을 사용하여 캠페인 클릭스루가 세션당 한 번씩만 계산되도록 하십시오. [!UICONTROL getValOnce] 플러그인에 대한 자세한 내용은 [구현 플러그인](/help/implement/js-implementation/plugins/impl-plugins.md).

* 마케팅 캠페인 추적 및 키워드 구입에 대한 자세한 내용은 [캠페인](https://marketing.adobe.com/resources/help/en_US/reference/campaign.html)을 참조하십시오.
* [!DNL DigitalPulse Debugger]를 사용하여 캠페인의 실제 값(디버거의 v0)을 살펴 보십시오. v0이 디버거에 나타나지 않으면, 해당 페이지에 대해 캠페인 데이터가 기록되지 않습니다.
