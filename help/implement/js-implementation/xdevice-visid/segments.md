---
description: 주어진 방문자 ID 쿠키에 대한 연관성이 생길 때마다 세그먼트를 만들 수 있습니다.
keywords: Analytics Implementation
solution: Analytics
title: 세그먼트 만들기
topic: Developer and implementation
uuid: 476a4667-033c-4e53-961d-ad67e7c2b045
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 세그먼트 만들기

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Adobe Experience [Cloud Device Co-op 설명서를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/mcdc/).

주어진 방문자 ID 쿠키에 대한 연관성이 생길 때마다 세그먼트를 만들 수 있습니다.

[이전 테이블](/help/implement/js-implementation/xdevice-visid/visit-example.md)을 기준으로 할 때, 방문 번호가 9인 세그먼트를 만든 경우 여기에는 서버 호출 12와 13이 포함됩니다. 서버 호출 11이 엄밀히 말해 동일한 방문의 일부였다 하더라도, 해당 서버 호출에 대한 내역 데이터는 바뀌지 않으며 방문 번호는 변하지 않고 유지됩니다.
