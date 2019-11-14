---
description: 사전 정의된 이벤트 목록
keywords: Analytics Implementation;event
solution: Analytics
title: 사전 정의된 이벤트란?
topic: Developer and implementation
uuid: 4d0799ba-0f97-42c3-a620-36c03f9995da
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 사전 정의된 이벤트란?

사전 정의된 이벤트 목록

| prodView | 성공 이벤트는 방문자가 제품을 볼 때마다 발생합니다. |
|---|---|
| scView | 성공 이벤트는 장바구니를 볼 때마다 발생합니다. |
| scOpen | 성공 이벤트는 방문자가 장바구니를 처음으로 열었을 때 발생합니다. |
| scAdd | 성공 이벤트는 제품이 장바구니에 추가될 때마다 발생합니다. |
| scRemove | 성공 이벤트는 항목을 장바구니에서 제거할 때마다 발생합니다. |
| scCheckout | 성공 이벤트는 체크아웃의 첫 번째 페이지에서 발생합니다. |
| purchase | 성공 이벤트는 체크아웃의 마지막 페이지에서 발생합니다(매출, 주문 및 판매량 포함). |

위의 사전 정의된 이벤트 중 하나가 발생하면 이벤트 인스턴스가 증가합니다. 몇 가지 서로 다른 보고서에서 이벤트와 관련된 지표를 볼 수 있습니다. 사전 정의된 이벤트를 구성하는 데 사용되는 코드의 예가 필요하면 아래를 참조하십시오.

```js
s.events="scAdd"
```

```js
s.events="scOpen,scAdd"
```

* 위의 첫 번째 예에서 *`scAdd`* 는 이벤트 값입니다. 언제든지 장바구니에 항목을 추가하면 이벤트가 증가합니다.
* 두 번째 예에서는 두 값을 동시에 캡처합니다. 여러 성공 이벤트가 같은 페이지에서 발생하면 각 이벤트가 증가합니다.

