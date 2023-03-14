---
title: 해시 충돌
description: 해시 충돌의 정의와 해시 충돌이 어떻게 발현될 수 있는지에 대해 설명합니다.
feature: Validation
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 100%

---

# 해시 충돌

Adobe에서는 prop 및 eVar 값이 숫자이더라도 문자열로 처리합니다. 때로 이러한 문자열의 길이는 수백 자가 되기도 하고 때로는 짧기도 합니다. 공간을 절약하고, 성능을 개선하고, 모든 크기를 균일하게 만들려면 문자열을 처리에서 바로 사용하지 않습니다. 대신, 각 값에 대해 32비트나 64비트 해시가 계산됩니다. 모든 보고서는 이 해시 값에서 실행되며, 이때 각 해시는 원래 텍스트로 대체됩니다. 해시는 Analytics 보고서의 성능을 크게 향상시킵니다.

대부분의 필드의 경우, 문자열은 먼저 모두 소문자로 변환됩니다 (고유한 값의 수를 줄임). 값은 월 단위로 해시됩니다 (각 달에 값이 처음 나타날 때). 매월 두 개의 고유한 변수 값이 동일한 값으로 해시할 가능성은 작지만 존재합니다. 이 개념을 *해시 충돌*&#x200B;이라고 합니다.

해시 충돌은 다음과 같이 보고에서 나타날 수 있습니다.

* 값을 트렌드하고 있고, 한 달 동안 스파이크가 표시된다면 해당 변수에 대한 다른 값은 보고 있는 값과 동일한 값으로 해시되었을 수 있습니다.
* 특정 값에 대한 세그먼트들에 대해 동일한 일이 일어날 수 있습니다.

## 해시 충돌 예

해시 충돌 가능성은 차원 ()에 있는 고유한 값의 수가 증가할수록 증가합니다. 예를 들어 그 달의 말에 들어 오는 값들 중 하나가 그 달에 앞에 있었던 값과 동일한 해시 값을 받을 수 있습니다. 다음 예는 이것이 어떻게 세그먼트 결과의 변화를 초래할 수 있는지를 설명하는 데 도움이 될 수 있습니다. 가령 eVar62에서 2월 18일에 &quot;값 100&quot;을 받는다고 가정하십시오. Analytics에서는 다음과 같이 보일 수 있는 테이블을 유지 관리하게 됩니다.

<table id="table_6A49D1D5932E485DB2083154897E5074"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar62 문자열 값 </th> 
   <th colname="col2" class="entry"> 해시 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 값 99 </p> </td> 
   <td colname="col2"> <p> 111 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> 값 100</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 값 101 </p> </td> 
   <td colname="col2"> <p> 222 </p> </td> 
  </tr> 
 </tbody> 
</table>

eVar62=&quot;값 500&quot;인 방문을 찾는 세그먼트를 만들 경우, Analytics에서는 &quot;값 500&quot;에 해시가 들어 있는지 판단합니다. &quot;값 500&quot;이 존재하지 않으므로 Analytics에서는 방문 0회를 반환합니다. 그 후, 2월 23일에 eVar62에서 &quot;값 500&quot;을 받고 이 값에 대한 해시도 123입니다. 해당 테이블은 다음과 같이 표시됩니다.

<table id="table_5FCF0BCDA5E740CCA266A822D9084C49"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> eVar62 문자열 값 </th> 
   <th colname="col2" class="entry"> 해시 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 값 99 </p> </td> 
   <td colname="col2"> <p> 111 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> 값 100</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 값 101 </p> </td> 
   <td colname="col2"> <p> 222 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> 값 500</b> </p> </td> 
   <td colname="col2"> <p> <b> 123</b> </p> </td> 
  </tr> 
 </tbody> 
</table>

동일한 세그먼트가 다시 실행되면, &quot;값 500&quot;의 해시를 찾고, 123을 찾습니다. 그러면 보고서에서 해시 123이 들어 있는 모든 방문을 반환합니다. 이제, 2월 18일에 발생한 방문이 결과에 포함됩니다.

이 상황에서 Analytics를 사용하면 문제가 발생할 수 있습니다. Adobe에서는 차후의 이러한 해시 충돌의 가능성을 줄이는 방법을 계속 조사하고 있습니다. 이러한 상황을 피하기 위한 가능한 방법은 변수들 간에 고유한 값들을 분산할 방법을 찾거나, 처리 규칙에서 불필요한 값을 제거하거나, 그렇지 않으면 변수당 값의 개수를 줄이는 것입니다.
