---
description: 범용(거래 ID) 카테고리를 선택하여 방문자 ID를 통합할 수 있습니다.
seo-description: 범용(트랜잭션 ID) 카테고리를 선택하여 방문자 ID를 통합할 수 있습니다.
seo-title: 방문자 ID
solution: Analytics
subtopic: Data Sources
title: 방문자 ID
topic: 개발자 및 구현
uuid: 4 E 9 CE 675-72 C 2-42 A 4-8 F 2 E -25140 DF 19539
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 방문자 ID

범용(거래 ID) 카테고리를 선택하여 방문자 ID를 통합할 수 있습니다.

See [Integrate Offline Data](../../../import/c-data-sources/datasrc-integrating-offline-data.md#concept_B5C576220F1548B5A3A57112AA3960C6).

<p class="head"> <b>방문자 ID 차원</b> </p>

| 열 이름 | 설명 |
|--- |--- |
| 방문자 ID | (필수) 온라인 및 오프라인 시스템 모두에서 고객을 나타내는 고유한 값. |
| 날짜 | MM/DD/YYYY/hh/mm/ss(예: 07/14/2017/06/00/00) 날짜 형식을 사용합니다. |
| 추적 코드 | 추적 코드 이름. |
| 카테고리 | 카테고리 이름.  카테고리를 지정하면 제품도 선택해야 합니다. |
| 채널 | 채널 이름. |
| Evarn | Evarn 이름. n의 유효한 값은 1-75의 정수입니다. |
| 제품 | 제품 이름. |
| 상태 | 상태 이름. |
| Zip | Zip 이름. |

**방문자 ID 지표**

| 열 이름 | 설명 |
|--- |--- |
| 클릭스루 | 추적 코드 보기 수. |
| 장바구니 추가 | 장바구니 추가 수. |
| 장바구니 열기 | 장바구니 열기 횟수. |
| 장바구니 제거 | 장바구니 제거 수. |
| 장바구니 보기 | 장바구니 보기 수. |
| 체크아웃 | 체크아웃 수. |
| 이벤트 n | 이벤트 n의 발생 횟수. n의 유효한 값은 1-100의 정수입니다.  보기 이벤트를 지정하면 해당 데이터 차원(eVar)도 지정해야 합니다. 예를 들어 eVar2 보기를 포함시키려면 값이 있는 eVar2를 나열해야 합니다. |
| Evarn 뷰 수 | eVarn을(를) 본 횟수. n의 유효한 값은 1-75의 정수입니다. |
| 가격 | 제품 가격.  |
| 주문 | 발생한 주문 수. |
| 제품 보기 횟수 | 제품 보기 횟수. |
| 수량 | 판매 수량. |