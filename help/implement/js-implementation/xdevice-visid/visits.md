---
description: Analytics에서는 서버 호출이 방문 페이지 번호가 1인 채 발생할 때마다 방문을 계산합니다.
keywords: Analytics 구현
seo-description: Analytics에서는 서버 호출이 방문 페이지 번호가 1인 채 발생할 때마다 방문을 계산합니다.
seo-title: 방문 횟수
solution: Analytics
subtopic: 방문자 수
title: 방문 횟수
topic: 개발자 및 구현
uuid: 3035 BE 8 F -6 ADC -45 DF-A 3 F 2-5 DE 6 D 3 ED 99 CE
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# 방문 횟수

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Analytics에서는 서버 호출이 방문 페이지 번호가 1인 채 발생할 때마다 방문을 계산합니다.

[이전 표를](../../../implement/js-implementation/xdevice-visid/visit-example.md#concept_E3B32B8E539F4FDC8E3FA872328B87BA)보면 4 번 발생했습니다. 히트 1, 9, 11 및 12 에서. 유효한 [!UICONTROL 방문자 ID]에서의 변화로 인해 [!UICONTROL 방문 페이지 번호]가 1로 재설정되지 않으므로, 이 값은 방문자 수와 유사하게, 초기 연결 후 정상으로 돌아옵니다.
