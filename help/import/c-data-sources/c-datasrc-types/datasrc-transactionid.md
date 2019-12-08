---
description: 범용(거래 ID) 카테고리를 선택하여 거래 ID를 통합할 수 있습니다.
subtopic: Data sources
title: 거래 ID
topic: Developer and implementation
uuid: f3370bb7-3f28-460b-a20d-c9e58d7301d4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 거래 ID

범용(거래 ID) 카테고리를 선택하여 거래 ID를 통합할 수 있습니다.

See [Integrating Offline Data](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

Data uploaded with *`transactionID`* automatically associates with the same marketing channel that processed the original server call that contained the *`transactionID`*.

**거래 ID 차원**

| 열 이름 | 설명 |
|--- |--- |
| 거래 ID | (필수) 오프라인 활동을 일으킨 온라인 거래를 나타내는 고유한 값. |
| 날짜 | MM/DD/YYYY/HH/mm/SS(예: 01/01/2015/06/00/00) 날짜 형식을 사용합니다. |
| 추적 코드 | 추적 코드 이름. |
| 카테고리 | 카테고리 이름.  카테고리를 지정하면 제품도 선택해야 합니다. |
| 채널 | 채널 이름. |
| eVarN | eVarN 이름. N의 유효한 값은 1 - 250의 정수입니다. |
| 제품 | 제품 이름. |
| 상태 | 상태 이름. |
| Zip | Zip 이름. |

<p class="head"> <b>거래 ID 지표</b> </p>



| 열 이름 | 설명 |
|--- |--- |
| 클릭스루 | 추적 코드 보기 수. |
| 장바구니 추가 | 장바구니 추가 수. |
| 장바구니 열기 | 장바구니 열기 횟수. |
| 장바구니 제거 | 장바구니 제거 수. |
| 장바구니 보기 | 장바구니 보기 수. |
| 체크아웃 | 체크아웃 수. |
| EventN | eventN이 발생한 횟수입니다. N의 유효한 값은 1 - 1000의 정수입니다.  보기 이벤트를 지정하면 해당 데이터 차원(eVar)도 지정해야 합니다. 예를 들어 eVar2 보기를 포함시키려면 값이 있는 eVar2를 나열해야 합니다. |
| eVarN 보기 | eVarN을 본 횟수입니다. N의 유효한 값은 1 - 250의 정수입니다. |
| 가격 | 제품 가격.  |
| 주문 | 발생한 주문 수. |
| 제품 보기 | 제품 보기 횟수. |
| 수량 | 판매 수량. |
