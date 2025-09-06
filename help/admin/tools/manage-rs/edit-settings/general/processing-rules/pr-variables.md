---
description: 처리 규칙을 사용하여 읽고 쓸 수 있는 사용 가능한 차원 및 지표입니다.
subtopic: Processing rules
title: 처리 규칙에 사용 가능한 차원 및 지표
feature: Processing Rules
role: Admin
exl-id: ffd7a1d6-2c9d-41e7-9c75-9e47b6f9c283
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 10%

---

# 처리 규칙에 사용 가능한 차원 및 지표

처리 규칙을 사용하여 읽고 쓸 수 있는 사용 가능한 차원 및 지표입니다.

## 사용자 지정 값 및 컨텍스트 데이터

| 값 | 읽기/쓰기 상태 | 설명 |
| --- | --- | --- |
| **사용자 지정 값** | 읽기 전용 | 처리 규칙 동작 시 직접 입력된 사용자 지정 텍스트 또는 값. |
| **연결된 값** | 읽기 전용 | 두 값을 결합하여 생성되는 값입니다. 예를 들어 채널과 페이지 이름을 결합하여 하위 범주를 만들 수 있습니다. |

## 히트 속성

| 속성 | 읽기/쓰기 상태 | 설명 |
| --- | --- | --- |
| **페이지 URL** | 읽기 + 쓰기 | [페이지 URL](/help/components/dimensions/page-url.md) 차원. 링크 추적 히트는 처리 규칙에 도달하기 전에 이 차원을 제거합니다. 처리 규칙을 사용하여 페이지 URL 값을 다시 삽입하는 경우 히트는 [페이지 이벤트](/help/components/metrics/page-views.md)가 아닌 [페이지 보기](/help/components/metrics/page-events.md)로 간주됩니다. Adobe에서는 페이지 차원의 값을 수정하기 전에 해당 값을 확인하는 것이 좋습니다. |
| **페이지 이름** | 읽기 + 쓰기 | [페이지](/help/components/dimensions/page.md) 차원입니다. 링크 추적 히트는 처리 규칙에 도달하기 전에 이 차원을 제거합니다. 처리 규칙을 사용하여 페이지 값을 다시 삽입하는 경우 히트는 [페이지 이벤트](/help/components/metrics/page-views.md)가 아닌 [페이지 보기](/help/components/metrics/page-events.md)로 간주됩니다. Adobe에서는 페이지 차원의 값을 수정하기 전에 해당 값을 확인하는 것이 좋습니다. |
| **보고서 세트 ID** | 읽기 전용 | 처리 규칙이 실행되는 보고서 세트입니다. 이 보고서 세트는 VISTA 규칙을 사용할 때와 같이 AppMeasurement을 통해 원래 전송된 보고서 세트와 다를 수 있습니다. |
| **AppMeasurement 코드 버전** | 읽기 전용 | 이미지 요청을 생성하는 데 사용되는 AppMeasurement 라이브러리 버전입니다. |
| **IP 주소** | 읽기 전용 | 방문자의 IP 주소입니다. |
| **사용자 에이전트** | 읽기 전용 | 방문자의 사용자 에이전트입니다. |
| **레퍼러** | 읽기 전용 | [레퍼러](/help/components/dimensions/referrer.md) 차원. |
| **쿼리 문자열 매개 변수** | 읽기 전용 | 현재 URL에서 지정된 쿼리 문자열 매개 변수의 값입니다. |
| **쿼리 문자열 매개 변수 참조** | 읽기 전용 | 참조 URL에 지정된 쿼리 문자열 매개 변수의 값이거나, 존재하지 않는 경우 빈 문자열입니다. |
| **참조 도메인** | 읽기 전용 | 하위 도메인을 포함한 참조 URL의 페이지 도메인. |
| **참조 루트 도메인** | 읽기 전용 | 참조 URL의 페이지 도메인(하위 도메인 제외). |
| **페이지 쿼리 문자열** | 읽기 전용 | 모든 쿼리 문자열 매개 변수와 현재 URL의 해당 값. |
| **쿼리 문자열 참조** | 읽기 전용 | 모든 쿼리 문자열 매개 변수 및 참조 URL의 해당 값. |
| **페이지 경로** | 읽기 전용 | 현재 URL의 페이지 경로. 페이지 경로에 프로토콜, 도메인 또는 쿼리 문자열 매개 변수가 포함되어 있지 않습니다. |
| **페이지 도메인** | 읽기 전용 | 하위 도메인을 포함한 현재 URL의 페이지 도메인. 페이지 도메인에는 페이지 경로 또는 쿼리 문자열 매개 변수가 포함되지 않습니다. |
| **페이지 루트 도메인** | 읽기 전용 | 하위 도메인을 제외한 현재 URL의 페이지 도메인. |
| **고객 관점** | 읽기 + 쓰기 | 히트가 모바일 배경 히트인지 여부를 결정하는 플래그입니다. |

## 전환 변수

| 변수 | 읽기/쓰기 상태 | 설명 |
| --- | --- | --- |
| **eVar 1-250** | 읽기 + 쓰기 | [eVar](/help/components/dimensions/evar.md) 차원. |
| **Campaign** | 읽기 + 쓰기 | [추적 코드](/help/components/dimensions/tracking-code.md) 차원입니다. |
| **구매 ID** | 읽기 + 쓰기 | [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) 구현 변수입니다. |
| **주/도** | 읽기 + 쓰기 | (중단됨) [`state`](/help/implement/vars/page-vars/state.md) 구현 변수입니다. |
| **Zip** | 읽기 + 쓰기 | [우편 번호](/help/components/dimensions/zip-code.md) 차원. |
| **통화 코드** | 읽기 + 쓰기 | [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) 구현 변수입니다. 중요: 이 변수를 잘못된 값으로 설정하면 히트가 무시됩니다. |
| **거래 ID** | 읽기 + 쓰기 | [`transactionID`](/help/import/data-sources/transactionid.md) 구현 변수입니다. |

>[!NOTE]
>Adobe에서는 처리 규칙을 사용하여 [`products`](/help/implement/vars/page-vars/products.md) 구현 변수를 설정할 수 없습니다.

## 트래픽 변수

| 변수 | 읽기/쓰기 상태 | 설명 |
| --- | --- | --- |
| **Prop 1-75** | 읽기 + 쓰기 | [Prop](/help/components/dimensions/prop.md) 차원. |
| **계층 구조 1-5** | 읽기 + 쓰기 | (중단됨) [계층](/help/components/dimensions/hierarchy.md) 차원. |
| **서버** | 읽기 + 쓰기 | [서버](/help/components/dimensions/server.md) 차원. |
| **Channel** | 읽기 + 쓰기 | [사이트 섹션](/help/components/dimensions/site-section.md) 차원. |

## 컨텍스트 변수

이 보고서 세트에 지난 30일 동안 표시된 모든 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md). 사용 예는 [처리 규칙 사용 사례](pr-use-cases.md)를 참조하십시오.

>[!IMPORTANT]
>
>처리 규칙이 지정된 컨텍스트 데이터 변수를 다른 변수(예: prop 또는 eVar)에 매핑하지 않으면 컨텍스트 데이터 변수의 값이 영구적으로 손실됩니다.

## 성공 이벤트

처리 규칙은 이벤트를 설정할 수 있지만 조건으로 읽을 수는 없습니다. 규칙 작업 드롭다운을 **[!UICONTROL 이벤트 설정]**(으)로 설정하여 증가시킬 사용 가능한 지표를 확인합니다.

| 변수 | 읽기/쓰기 상태 | 설명 |
| --- | --- | --- |
| **주문** | 쓰기 전용 | [주문](/help/components/metrics/orders.md) 지표입니다. |
| **장바구니** | 쓰기 전용 | [장바구니](/help/components/metrics/carts.md) 지표. |
| **장바구니 보기 수** | 쓰기 전용 | [장바구니 보기 수](/help/components/metrics/cart-views.md) 지표. |
| **체크아웃** | 쓰기 전용 | [체크아웃](/help/components/metrics/checkouts.md) 지표입니다. |
| **장바구니 추가** | 쓰기 전용 | [장바구니 추가](/help/components/metrics/cart-additions.md) 지표. |
| **장바구니 제거 수** | 쓰기 전용 | [장바구니 제거](/help/components/metrics/cart-removals.md) 지표입니다. |
| **이벤트 1-1000** | 쓰기 전용 | [사용자 지정 이벤트](/help/components/metrics/custom-events.md). |
| **제품 보기** | 쓰기 전용 | [제품 보기](/help/components/metrics/product-views.md) 지표입니다. |
