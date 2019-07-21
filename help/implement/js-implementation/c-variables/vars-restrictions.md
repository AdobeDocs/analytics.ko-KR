---
description: JavaScript 변수에 허용되지 않는 문자 및 문자열
keywords: Analytics 구현
seo-description: JavaScript 변수에 허용되지 않는 문자 및 문자열
seo-title: 잘못된 JavaScript 문자
solution: Analytics
subtopic: 변수
title: 잘못된 JavaScript 문자
topic: 개발자 및 구현
uuid: 04 E 3 B 4 B 4-7 FF 5-4673-8060-34302 B 6 EE 545
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 잘못된 JavaScript 문자

JavaScript 변수에 허용되지 않는 문자 및 문자열

* 탭(0x09)
* 캐리지 리턴(0x0D)
* 줄바꿈 문자(0x0A)
* 127개 이상의 코드가 포함된 ASCII 문자(멀티바이트 문자가 활성화되지 않고 *`charSet`* 가 적절히 채워지지 않은 경우)
* HTML tags (e.g. <b></b> or &amp;#153)

특히 products, hierarchy 및 events와 같은 많은 변수에는 추가적인 제한 사항이나 구문 요구 사항이 있습니다. 개별 변수 제한 사항 및 구문 요구 사항을 보려면, *`s_account`* 변수 매개 변수에 해당하는 섹션을 참조하십시오.
