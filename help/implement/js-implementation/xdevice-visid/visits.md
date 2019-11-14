---
description: Analytics에서는 서버 호출이 방문 페이지 번호가 1인 채 발생할 때마다 방문을 계산합니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Visitors
title: 방문 횟수
topic: Developer and implementation
uuid: 3035be8f-6adc-45df-a3f2-5de6d3ed99ce
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 방문 횟수

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Adobe Experience [Cloud Device Co-op 설명서를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Analytics에서는 서버 호출이 방문 페이지 번호가 1인 채 발생할 때마다 방문을 계산합니다.

[이전 테이블](/help/implement/js-implementation/xdevice-visid/visit-example.md)을 보면 네 번(히트 1, 9, 11, 12) 발생했습니다. 유효한 [!UICONTROL 방문자 ID]에서의 변화로 인해 [!UICONTROL 방문 페이지 번호]가 1로 재설정되지 않으므로, 이 값은 방문자 수와 유사하게, 초기 연결 후 정상으로 돌아옵니다.
