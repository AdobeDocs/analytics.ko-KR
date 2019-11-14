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


# eVarN

[!UICONTROL eVar] 변수는 사용자 지정 보고서를 작성하는 데 사용됩니다.

<!-- 

eVarN.xml

 -->

eVar가 방문자에 대한 값으로 설정되면 이 값은 만료되기 전까지 기억됩니다. eVar 값이 활성일 때 방문자가 발견하는 성공 이벤트는 eVar 값으로 카운트됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 255바이트 | V1-v75([또는 v100 또는 v250](/help/implement/js-implementation/c-variables/page-variables.md)) | 사용자 지정 전환 | "" |

**만료** {#section_6DB5882B960D4660AE248B91B76883C4}

[!UICONTROL eVar]은 지정되는 일정 시간 후 만료되며, 만료된 후 eVar는 더 이상 성공 이벤트에 대한 크레딧을 받지 않습니다. eVar를 성공 이벤트에 대해 만료되도록 구성할 수도 있습니다. 예를 들어 방문이 끝날 때 만료되는 내부 판촉 행사가 있을 경우, 이 내부 판촉 행사는 방문 중 발생하여 활성화되는 구매 또는 등록에 대해서만 크레딧을 받습니다.

다음과 같은 두 가지 eVar 만료 방법이 있습니다.

* 지정된 시간이나 이벤트 후 eVar가 만료되도록 설정할 수 있습니다.
* eVar의 강제 만료 기능을 사용할 수 있으며, 이 기능은 변수를 다른 목적에 사용할 때 유용합니다.

eVar를 내부 판촉 행사 반영을 위해 5월에 사용하고 6월에 내부 검색 키워드를 캡처하는 데 사용한다면, 6월 1일에 변수를 강제로 만료하거나 재설정해야 합니다. 이렇게 하면 내부 판촉 행사 값을 6월의 보고서에서 빼는 데 유용합니다.

**대/소문자 구분** {#section_6E9145B7FCC2438E95BB35AAE3857412}

eVar는 대/소문자를 구분하지는 않지만 처음 사용한 대/소문자대로 표시됩니다. 예를 들어 eVar1을 처음 사용할 때 "Logged In"으로 설정되었지만, 그 이후의 모든 사용에서는 "logged in"으로 전달되는 경우, 보고서는 항상 "Logged In"을 eVar의 값으로 보여 줍니다.

**카운터** {#section_D8403F0C175E4BC9BE4F2E794B1F4D33}

eVar는 대부분 문자열 값을 보관하는 데 사용되지만, 카운터로 작동하도록 구성할 수도 있습니다. eVar는 이벤트 전에 사용자가 취하는 동작의 수를 세려고 할 때 카운터로 유용합니다. 예를 들어 구매 전에 eVar를 사용하여 내부 검색 횟수를 캡처할 수 있습니다. 방문자가 검색할 때마다, eVar에는 '+1'의 값이 포함되어 있어야 합니다. 방문자가 구매 전에 검색을 네 번 수행하면, 각각 총 횟수는 1.00, 2.00, 3.00 및 4.00이 됩니다. 하지만 구매 이벤트에 대해서는 4.00만 크레딧을 받습니다(주문 및 매출 지표). eVar 카운터의 값으로는 양수만 허용됩니다.

**하위 관계** {#section_2BEABBBC735241F4BA42E74D19B5AEE0}

[!UICONTROL 사용자 지정 eVar] 보고서에 대한 일반적인 요구 사항은 하나의 [!UICONTROL 사용자 지정 eVar] 보고서를 다른 eVar로 분류하는 기능입니다. 예를 들어 한 eVar에 성별이 들어 있고 다른 eVar에 급료가 들어 있는 경우, 사이트의 여성 방문자 중에 '연간 $50,000 이상을 버는 여성이 얼마의 매출을 생성했는가'라는 질문을 할 수 있습니다. 전체 하위 관계인 모든 eVar는 보고서에서 이러한 유형의 분류를 허용합니다. 예를 들어 성별 eVar에 전체 하위 관계가 활성화되어 있는 경우, 모든 다른 사용자 지정 eVar 보고서는 성별로 분류할 수 있고 성별은 모든 다른 eVar로 분류할 수 있습니다. 두 보고서 간의 관계를 보기 위해서는, 이 중 하나의 전체 하위 관계만 활성화되어 있어야 합니다. 기본적으로 [!UICONTROL 캠페인], [!UICONTROL 제품] 및 [!UICONTROL 카테고리] 보고서의 경우 전체 하위 관계가 활성화되어 있습니다(모든 eVar는 캠페인이나 제품으로 분류할 수 있음).

**구문 및 가능한 값** {#section_BD46438B14F3488FB9AC42994C317B06}

eVar의 이름은 변경할 수 있지만 JavaScript 파일에서는 항상 eVarX로 참조되어야 합니다. 여기서 X는 1과 75 사이의 숫자([ 또는 100 또는 250](/help/implement/js-implementation/c-variables/page-variables.md))입니다.

```js
s.eVarX="value"
```

카운터로 사용하지 않는 eVar는 다른 모든 변수와 동일한 제한 사항을 가집니다. eVar가 "카운터"일 경우에는 "1" 또는 "2.5"와 같은 숫자 값을 받게 됩니다. 소수점 이하 자리 수가 세 자리 이상인 수가 지정되는 경우, eVar 카운터는 소수점 이하 두 자리로 반올림합니다. eVar 카운터에는 음수가 들어 있을 수 없습니다.

**예** {#section_B37F4B0D56734DA3AB02BB218825BA4E}

```js
s.eVar1="logged in"
```

```js
s.eVar23="internal spring promo 4"
```

**구성 설정** {#section_BD1FE63001C84D3DB69F3DEE243960B6}

eVar는 [!UICONTROL Analytics &gt; 관리자 &gt; 보고서 세트 &gt; 설정 편집 &gt; 전환 &gt; 전환 변수]에서 구성할 수 있습니다. 모든 eVar는 [!UICONTROL 이름], [!UICONTROL 유형], [!UICONTROL 할당], [!UICONTROL 설정 후 만료] 또는 [!UICONTROL 재설정]으로 구성할 수 있습니다. 각 구성 설정은 개별적으로 지정됩니다.

<table id="table_5C524B71520849FA8A9A6B79A3EE77C9"> 
 <thead> 
  <tr> 
   <th class="entry"> 설정 </th> 
   <th class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td>  이름  </td> 
   <td> <span class="keyword">Analytics</span> 내에서 eVar 보고서의 이름을 변경할 수 있도록 해줍니다. <p><span class="keyword">Analytics</span>에서 보고서에 어떤 이름이 지정되었는지에 관계없이 JavaScript 코드에서는 여전히 eVar를 s.eVarX로 참조해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> 유형 </td> 
   <td> eVar가 텍스트 문자열인지 아니면 카운터인지 표시할 수 있도록 해줍니다. </td> 
  </tr> 
  <tr> 
   <td> 할당 </td> 
   <td> eVar의 값 중 어느 값이 성공 이벤트에 대한 크레딧을 받는지를 구성하는 데 사용됩니다. <p>할당이 "가장 최근(마지막)"으로 설정되면, B가 크레딧을 받습니다. </p> <p>할당이 "원래 값(처음)"으로 설정되면, A가 크레딧을 받습니다. </p> <p>할당이 "선형"으로 설정되면, A와 B 모두가 구매 가치의 반에 대한 크레딧을 받습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> 다음 날짜 이후에 만료 </td> 
   <td> eVar가 구매와 같은 특정 이벤트 발생 시 만료되는지, 아니면 사용자 지정 또는 사전 정의된 시간 후 만료되는지를 결정할 수 있도록 해줍니다. </td> 
  </tr> 
  <tr> 
   <td> 재설정 </td> 
   <td> eVar에 대한 <span class="wintitle">재설정</span> 확인란을 선택하고 페이지 하단에 있는 <span class="wintitle">저장</span>을 클릭하면, 해당 eVar의 모든 값이 즉시 만료됩니다. 이렇게 되면 eVar의 새 값만 성공 이벤트에 대한 크레딧을 받습니다. </td> 
  </tr> 
 </tbody> 
</table>

**함정, 질문 및 팁** {#section_DA6912C802E445F986C6DE4234C6C737}

* [!UICONTROL prop] 변수와 달리, eVar 변수는 구분된 값 목록이 될 수 없습니다. 값 목록으로 eVar를 채우는 경우(예: "one,two,three") 이 문자열이 그대로 보고서에 나타납니다.
* eVar 카운터는 음수를 포함할 수 없습니다.
