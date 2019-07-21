---
description: s.sa() 함수를 사용하면 이미지 요청을 실행하기 전 또는 후에 페이지에서 언제든지 동적으로 보고서 세트를 변경할 수 있습니다.
keywords: Analytics 구현
seo-description: s.sa() 함수를 사용하면 이미지 요청을 실행하기 전 또는 후에 페이지에서 언제든지 동적으로 보고서 세트를 변경할 수 있습니다.
seo-title: s.sa() 함수
solution: Analytics
subtopic: 함수
title: s.sa() 함수
topic: 개발자 및 구현
uuid: A 6 aacd 10-2 A 5 B -448 B-B 3 B 7-BED 5590 B 71 D 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# s.sa() 함수

s.sa() 함수를 사용하면 이미지 요청을 실행하기 전 또는 후에 페이지에서 언제든지 동적으로 보고서 세트를 변경할 수 있습니다.

조직에서 페이지를 다시 로드하지 않고 데이터를 다른 보고서 세트로 보내려는 경우는 가능한 한 이 함수를 사용하는 것이 좋습니다.

이 정보는 보고와 구현 모두에 능숙한 고급 사용자에게 적합합니다. 발생할 수 있는 결과에 대해 충분히 이해하지 않은 상태에서 구현을 편집하지 마십시오. 구현 변경이 필요한 경우에는 조직의 계정 관리자에게 문의하십시오.

## 함수의 속성 {#section_E10CB41A0CF749F4A24C8377958E3671}

이 함수를 설정하면 이전에 정의한 변수를 모두 회수하여 다른 보고서 세트에 사용할 수 있습니다.

## 구현 예제 {#section_14B0B8C853244D5F82B08B995773640C}

비디오 데이터를 하나의 보고서 세트로 보내고 나머지를 다른 세트로 전송:

```js
// Set in the core JS file by default 
var s=s_gi('prodrsid'); 
 
// Define this when a user interacts with a video 
s.sa('videorsid'); 
s.t(); // Sends an image request
```

s.sa() 및 다중 세트 태깅 사용:

```js
// Set in the core JS file by default 
var s=s_gi('rsid1'); 
 
// Call the function when you wish to change report suites 
s.sa('rsid1,rsid2'); 
s.t();
```

