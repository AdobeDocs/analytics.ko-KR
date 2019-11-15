---
description: 지리 특성 데이터는 방문의 첫 번째 히트를 기반으로 기록되며, 사용된 장치에 상관없이 하나의 방문에 대해서는 변경되지 않습니다.
keywords: Analytics Implementation
solution: Analytics
title: 지리 특성 데이터
topic: Developer and implementation
uuid: 8449bf11-c367-4698-a73e-f6cb59f8c945
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 지리 특성 데이터

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Adobe Experience [Cloud Device Co-op 설명서를 참조하십시오](https://marketing.adobe.com/resources/help/en_US/mcdc/).

지리 특성 데이터는 방문의 첫 번째 히트를 기반으로 기록되며, 사용된 장치에 상관없이 하나의 방문에 대해서는 변경되지 않습니다.

고객이 자신의 집 컴퓨터에서 사이트를 탐색을 한 다음 30분 내에 모바일 장치에서 탐색하는 경우, 지리 특성 데이터는 변하지 않습니다. VISTA를 사용하여 지리 특성 데이터로 eVar를 채우는 경우에는 각 히트에서 IP 주소를 기반으로 합니다. 이렇게 하면 동일한 방문에 대해 IP 주소가 바뀌는 경우 지리 특성 데이터 값이 여러 개 생길 수 있습니다.
