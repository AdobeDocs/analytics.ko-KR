---
description: 다음 표는 올바른 코드와 잘못된 코드 실수 간의 차이점을 보여 줍니다.
keywords: Analytics 구현
seo-description: 다음 표는 올바른 코드와 잘못된 코드 실수 간의 차이점을 보여 줍니다.
seo-title: 일반적인 구문 실수
solution: Analytics
subtopic: 문제 해결
title: 일반적인 구문 실수
topic: 개발자 및 구현
uuid: 9845 DCB 9-9 F 10-4 F 65-A 43 D -2 AF 41 EDAA 122
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 일반적인 구문 실수

다음 표는 올바른 코드와 잘못된 코드 실수 간의 차이점을 보여 줍니다.

| 잘못된 코드 | 올바른 코드 |
|---|---|
| prop1 | s.prop1 ("s."를 사용합니다.) |
| s.evar1 | s.eVar1 (대문자를 올바로 사용합니다.) |
| s.pagetype='errorpage'; | s.pageType='errorPage'; (대문자를 올바로 사용합니다.) |
| s.tl(this,o,pageA) | s.tl(this,'o','pageA'); (작은 따옴표의 올바른 사용) |
| s.events='event1'; s.events='event2'; | s.events='event1,event2'; (올바른 형식) |
| s.pageName="John" (둥근 따옴표 켬) | s.pageName="John" (둥근 따옴표 끔) |
| s.products="shoes,UX4879,1,19.99" | s.products="shoes;UX4879;1;19.99" (쉼표가 아니라 세미콜론을 사용합니다.) |
| s.products=";MacBook Air;1;$1999.99" | s.products=";MacBook Air;1;1999.99" (달러 기호를 사용하지 않습니다.) |
| s.products=";Nikon SB-600 Speedlight Flash for Nikon Digital SLR Cameras;1;229.9489183" | s.products=";Nikon SB-600 Speedlight Flash for Nikon Digital SLR Cameras;1;229.95" (긴 가격을 반올림하거나 자릅니다.) |
| var s_account="rsid1, rsid2" | var s_account="rsid1,rsid2" (다중 세트에 태깅할 때 보고서 세트 ID 간 공백 없음) |
| s.events="event1, event2" | s.events="event1,event2" (여러 이벤트에 태깅할 때 이벤트 ID 간 공백 없음) |
| s.products="product name" | s.products=";product name" (나열된 제품 카테고리가 없을 때 세미콜론을 사용함) |

## 추가 참고 사항 {#section_E2B6A9C966AD40A09578DD0F784DCAB9}

Adobe 코드의 맨 끝에 끝나는 HTML 주석을 유지하십시오(스크립트의 NOSCRIPT 부분을 사용하고 있더라도).
