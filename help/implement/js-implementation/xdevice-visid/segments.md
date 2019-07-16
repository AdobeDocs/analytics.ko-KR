---
description: 주어진 방문자 ID 쿠키에 대한 연관성이 생길 때마다 세그먼트를 만들 수 있습니다.
keywords: Analytics 구현
seo-description: 주어진 방문자 ID 쿠키에 대한 연관성이 생길 때마다 세그먼트를 만들 수 있습니다.
seo-title: 세그먼트 만들기
solution: Analytics
title: 세그먼트 만들기
topic: 개발자 및 구현
uuid: 476 A 4667-033 C -4 E 53-961 D-AD 67 E 7 C 2 B 045
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# 세그먼트 만들기

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

주어진 방문자 ID 쿠키에 대한 연관성이 생길 때마다 세그먼트를 만들 수 있습니다.

[이전 표를](../../../implement/js-implementation/xdevice-visid/visit-example.md#concept_E3B32B8E539F4FDC8E3FA872328B87BA)기준으로 방문 번호가 9 인 세그먼트를 만든 경우 서버가 12와 13 이라는 서버 호출을 포함합니다. 서버 호출 11이 엄밀히 말해 동일한 방문의 일부였다 하더라도, 해당 서버 호출에 대한 내역 데이터는 바뀌지 않으며 방문 번호는 변하지 않고 유지됩니다.
