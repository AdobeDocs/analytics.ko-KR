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


# purchaseID

보고서에서 주문이 여러 번 카운트되지 않도록 하는 데 사용됩니다.

<!-- 

purchaseID.xml

 -->

사이트에서 [!UICONTROL 구매] 이벤트가 사용될 때마다 *`purchaseID`* 변수를 사용해야 합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 20바이트 | purchaseID | 전환 &gt; 구매 &gt; 매출 전환 | "" |

방문자가 사이트에서 항목을 구매하면 *`purchaseID`*&#x200B;가, [!UICONTROL 구매] 이벤트가 실행된 같은 곳의 "감사합니다" 페이지에서 채워집니다. *`purchaseID`*&#x200B;가 채워지면, "감사합니다" 페이지의 제품이 *`purchaseID`*&#x200B;마다 한 번씩만 카운트됩니다. 사이트를 방문하는 많은 방문자들이 자신만의 목적을 위해 "감사합니다" 또는 "확인 페이지"를 저장하므로 이것은 매우 중요합니다. The *`purchaseID`* 는 페이지를 볼 때마다 구매를 카운트하지 않도록 해줍니다.

구매 데이터가 두 번 카운트되지 않도록 하는 것 외에도, 이 데이터를 *`purchaseID`*&#x200B;를 사용하면 모든 전환 데이터가 보고서에서 두 번 카운트되지 않습니다.

**구문 및 가능한 값** {#section_E352CE2370D54BA69A368E1F63A9C32D}

```js
s.purchaseID="unique_id"
```

*`purchaseID`*&#x200B;는 20자 이하여야 하며, 표준 ASCII를 사용해야 합니다.

**예** {#section_60A5C1EAF42F4611898CD6A4F4CF5A28}

```js
s.purchaseID="11223344" 
s.purchaseID="a8g784hjq1mnp3"
```

**구성 설정** {#section_1808631C96674380BF9C4A6D9A2C568E}

없음

**함정, 질문 및 팁** {#section_F5D010F234ED43F19AD1FCD2CD64E060}

*`purchaseID`* 변수를 사용하면 페이지의 모든 전환 변수를 보고서에서 한 번씩만 셀 수 있습니다.
