---
description: 일반 웹 사이트에 대한 여러 가지 일반 변수 및 성공 이벤트를 구성합니다.
title: 기본 템플릿
feature: Report Suite Settings
uuid: edcf1b97-4ff2-4e98-b84c-199af2181d68
exl-id: 36aaded4-5c46-41af-a5c6-216bd2fcadb2
TQID: https://experienceleague.adobe.com/Tz2kROFW9n8apieb-bLIEPJ26LsZIhci5Azf1dvxRLI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2:
  - id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 80%

---

# 기본 템플릿

일반 웹 사이트에 대한 여러 가지 일반 변수 및 성공 이벤트를 구성합니다.

| 전환 변수 | 유형 | 하위 관계 | 할당 | 만료 | `s_code` 변수 |
|---|---|---|---|---|---|
| 내부 캠페인 | 문자열 | 기본 | 최근 (마지막) | 방문 | `evar1` |
| 내부 검색어 | 문자열 | 기본 | 최근 (마지막) | 방문 | `evar2` |
| Commerce 변수 3 | 문자열 | 기본 | 최근 (마지막) | 방문 | `evar3` |
| Commerce 변수 4 | 문자열 | 기본 | 최근 (마지막) | 방문 | `evar4` |

| 성공 이벤트 | 유형 | `s_code` 변수 |
|---|---|---|
| 등록 | 카운터 (하위 관계 없음) | `event1` |
| 이메일 등록 | 카운터 (하위 관계 없음) | `event2` |
| 구독 | 카운터 (하위 관계 없음) | `event3` |
| 페이지 조회수 | 카운터 (하위 관계 없음) | `event4` |
| 광고 노출 횟수 | 카운터 (하위 관계 없음) | `event5` |
| 광고 클릭수 | 카운터 (하위 관계 없음) | `event6` |

| 사용자 정의 인사이트 변수 | `s_code` 변수 |
|---|---|
| 트래픽 속성 1-5 | `prop1, prop2, prop3, prop4, prop5` |

다음 테이블은 표준 상거래 이벤트 목록을 포함합니다. 이러한 이벤트에 대한 초기 구성은 모든 보고서 세트 템플릿에서 동일합니다. s_code 변수가 N/A인 이벤트는 설정할 필요가 없으며 자동으로 제공됩니다.

| 표준 Commerce 이벤트 | 유형 | `s_code` 변수 |
|---|---|---|
| 매출 | 카운터 | `purchase` |
| 주문 | 카운터 | `purchase` |
| 판매량 | 카운터 | `purchase` |
| 장바구니 | 카운터 | `scOpen` |
| 장바구니 보기 | 카운터 | `scView` |
| 인스턴스 | 카운터 | 해당 사항 없음 |
| 체크아웃 | 카운터 | `scCheckout` |
| 장바구니 추가 | 카운터 | `scAdd` |
| 장바구니 제거 | 카운터 | `scRemove` |
| 방문 횟수 | 카운터 (하위 관계 없음) | 해당 사항 없음 |
| 페이지 조회수 | 카운터 (하위 관계 없음) | 해당 사항 없음 |
| 일별 고유 방문자 수 | 카운터 (하위 관계 없음) | 해당 사항 없음 |
| 고유 방문자 수 | 카운터 (하위 관계 없음) | 해당 사항 없음 |
