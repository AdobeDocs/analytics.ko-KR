---
description: 범용(트랜잭션 ID) 카테고리를 선택하여 방문자 ID를 통합할 수 있습니다.
subtopic: Data sources
title: 방문자 ID
topic-fix: Developer and implementation
uuid: 4e9ce675-72c2-42a4-8f2e-25140df19539
exl-id: 940af1ba-0d12-4552-a21e-0ceb06427ab2
source-git-commit: a7a116ddc9eddc500a52111e9c002bdbee3e4a56
workflow-type: ht
source-wordcount: '224'
ht-degree: 100%

---

# VisitorID

[!UICONTROL 콜센터 데이터] 카테고리를 선택하여 방문자 ID를 통합할 수 있습니다.

[오프라인 데이터 통합](/help/import/c-data-sources/datasrc-integrating-offline-data.md)을 참조하십시오.

## VisitorID 차원

| 열 이름 | 설명 |
|--- |--- |
| [!UICONTROL VisitorID] | (필수) 온라인 및 오프라인 시스템 모두에서 고객을 나타내는 고유한 값 |
| [!UICONTROL 날짜] | 다음 날짜 형식을 사용하십시오. `MM/DD/YYYY/hh/mm/ss` (예: 07/14/2017/06/00/00) |
| [!UICONTROL 추적 코드] | 추적 코드 이름 |
| [!UICONTROL 카테고리] | 카테고리 이름 카테고리를 지정하면 제품도 선택해야 합니다. |
| [!UICONTROL Channel] | 채널 이름 |
| [!UICONTROL eVar ]*n* | eVar *n* 이름. *n*&#x200B;의 유효한 값은 1-75의 정수입니다. |
| [!UICONTROL 제품] | 제품 이름 |
| [!UICONTROL 주/도] | 상태 이름 |
| [!UICONTROL Zip] | Zip 이름 |

## 방문자 ID 지표

| 열 이름 | 설명 |
| --- | --- |
| [!UICONTROL 클릭스루] | 추적 코드 보기 수 |
| [!UICONTROL 장바구니 추가] | 장바구니 추가 수 |
| [!UICONTROL 장바구니 열기] | 장바구니 열기 횟수 |
| [!UICONTROL 장바구니 제거] | 장바구니 제거 수 |
| [!UICONTROL 장바구니 보기] | 장바구니 보기 수 |
| [!UICONTROL 체크아웃] | 체크아웃 수 |
| *이벤트 n* | 이벤트 *n* 발생 횟수 n의 유효한 값은 1-100의 정수입니다. [!UICONTROL 보기] 이벤트를 지정하는 경우 해당 데이터 차원(eVar)도 지정해야 합니다. 예를 들어 eVar2 보기를 포함시키려면 값이 있는 eVar2를 나열해야 합니다. |
| [!UICONTROL eVar ]*n* 뷰 수 | eVar *n*&#x200B;을(를) 본 횟수. *n*&#x200B;의 유효한 값은 1-75의 정수입니다. |
| [!UICONTROL 가격] | 제품 가격 |
| [!UICONTROL 주문] | 발생한 주문 수 |
| [!UICONTROL 제품 보기] | 제품 보기 횟수 |
| [!UICONTROL 수량] | 판매 수량 |
