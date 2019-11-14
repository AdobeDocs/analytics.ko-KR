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



# 이벤트

 변수는 일반적인 장바구니 성공 이벤트와 사용자 지정 성공 이벤트를 기록하는 데 사용됩니다.

<!-- 

events.xml

 -->

<table id="table_9EB9D08C80544CD68C4B1A2012440472"> 
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
   <td> 제한 없음 </td> 
   <td> events </td> 
   <td> <p>장바구니 이벤트 </p> <p>사용자 지정 이벤트 </p> </td> 
   <td> N/A </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL 이벤트]는 사이트 내에서 중대한 이벤트로 간주되어야 합니다. 성공 이벤트는 대개 등록 프로세스나 뉴스레터 가입과 같이, 프로세스의 최종 확인 페이지에서 채워집니다. 사용자 지정 이벤트는 아래의 가능한 값 섹션에 정의된 문자 값으로 events 변수를 채우는 방식으로 정의됩니다.

기본적으로, 성공 이벤트는 *카운터* 이벤트로 구성됩니다. 카운터 이벤트는 성공 이벤트가 설정되는 횟수(x+1)를 카운트합니다. 이벤트는 *숫자* 이벤트로도 구성됩니다. 숫자 이벤트를 사용하면 숫자를 증분으로 지정할 수 있습니다(내부 검색에서 반환되는 결과 수와 같이, 동적 또는 임의의 값을 카운트할 때 필요할 수 있기 때문에).

최종 이벤트 유형인 *통화*&#x200B;를 사용하면 추가되는 금액을 정의할 수 있습니다(숫자 이벤트와 유사). 하지만 통화는 보고서에서 통화로 표시되며,  *`currencyCode`*&#x200B;값과 보고서 세트에 대한 기본 통화 설정을 기반으로 통화 전환이 가능합니다. 숫자 및 통화 이벤트 사용에 대한 자세한 내용은 [제품](/help/implement/js-implementation/c-variables/page-variables.md)을 참조하십시오.

**변수 구성** {#section_9195286C34C54B02B2598E2B856492C3}

[!UICONTROL s.events] 변수는 모든 구현에 대해 기본적으로 활성화되어 있습니다. 7개의 사전 구성된 전환 이벤트는 모든 새 보고서 세트에 대해 자동으로 활성화됩니다. 새로운 사용자 지정 이벤트(event1- [event100 또는 event1000](/help/implement/js-implementation/c-variables/page-variables.md))는 관리 콘솔을 사용하여 모든 관리 수준 사용자가 활성화할 수 있습니다.

**가능한 값** {#section_18395A3BEFEB4E9F8D7B2ED0001FBE4E}

다음은 events 변수에 가능한 값의 목록입니다.

| 이벤트 | 설명 | 채워진 보고서 |
|---|---|---|
| prodView | 제품 보기 | 제품 |
| scOpen | 새 장바구니 열기/초기화 | 장바구니 |
| scAdd | 장바구니에 항목 추가 | 장바구니 추가 |
| scRemove | 장바구니에서 항목 제거 | 장바구니 제거 |
| scView | 장바구니 보기 | 장바구니 보기 |
| scCheckout | 체크아웃 프로세스의 시작 | 체크아웃 |
| purchase | 구매(주문) 완료 | 주문 |
| event1~event1000(포인트 제품의 경우 event100) | 사용자 지정 이벤트 | 사용자 지정 이벤트 |

**구문 및 예** {#section_45A159DF00114066B8551DDEB15E084C}

카운터 이벤트는 [!UICONTROL s.events] 변수에서, 쉼표로 구분된 목록(여러 이벤트를 전달해야 하는 경우)으로 원하는 이벤트를 삽입하여 설정합니다.

```js
s.events="scAdd"
```

```js
s.events="scAdd,event1,event7"
```

```js
s.events="event5"
```

```js
s.events="purchase,event10"
```

H23 이상의 코드인 경우, 카운터 이벤트에 2 이상의 정수가 지정되어 있을 수 있습니다.

```js
s.events="event1=10"
```

```js
s.events="scRemove=3,event6,event2=4"
```

지정된 정수 값이 있는 카운터 이벤트를 구현하면 이벤트가 이미지 요청 내에서 여러 번 실행되는 것처럼 취급됩니다. 카운터 이벤트에서는 소수를 허용하지 않으므로, 이 기능이 필요할 경우에는 숫자 이벤트를 대신 사용하는 것이 좋습니다.
보통 숫자 및 통화 이벤트가 [!UICONTROL s.products] 변수에서 숫자 값(예: 24.99)을 받기는 하지만, 이 이벤트들은 [!UICONTROL s.events] 변수에 포함되어야 합니다. 이렇게 하면 특정 숫자 및 통화 값을 개별 제품 항목에 연결할 수 있습니다.

**이벤트 정리** {#section_A89488EF4471405AAFC4D6DD05E77621}

기본적으로, 이벤트는 사이트에서 이벤트가 설정될 때마다 카운트됩니다.

자세한 내용은 [이벤트 정리](/help/implement/js-implementation/event-serialization.md)를 참조하십시오.

**구문** {#section_8559D42D3F344AF3BB3C0125F78C4989}

```js
s.events="event1:3167fhjkah"
```

**예** {#section_7B5B5728A59648ADB3E2548CDAD2C9D4}

```js
s.events="scAdd:003717174"
```

```js
s.events="scAdd:user228197,event1:577247280,event7:P7fhF8571"
```
