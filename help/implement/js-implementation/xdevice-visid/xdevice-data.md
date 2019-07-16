---
description: 상호 장치 방문자 식별 기능을 활성화하는 것이 보고서에 표시되는 데이터에 어떻게 영향을 미치는지에 대한 개요
keywords: Analytics 구현
seo-description: 상호 장치 방문자 식별 기능을 활성화하는 것이 보고서에 표시되는 데이터에 어떻게 영향을 미치는지에 대한 개요
seo-title: 장치 간 방문자 식별의 데이터 영향
solution: Analytics
subtopic: 방문자 수
title: 장치 간 방문자 식별의 데이터 영향
topic: 개발자 및 구현
uuid: 1 DB 4 D 149-CD 50-4 B 41-A 850-988901 F 25051
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# 장치 간 방문자 식별의 데이터 영향

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

상호 장치 방문자 식별 기능을 활성화하는 것이 보고서에 표시되는 데이터에 어떻게 영향을 미치는지에 대한 개요

이 기능이 어떻게 데이터 수집에 영향을 주는지 이해하려면, 방문자 프로필에서 방문자 데이터 필드를 이해하는 것이 유용합니다.

| 데이터 필드 | 설명 |
|---|---|
| 방문자 ID 쿠키 | 장치나 브라우저에서 첫 번째 방문 시 자동으로 생성되어 `s_vi` 쿠키에 저장된 ID |
| 방문자 ID 변수 | [!UICONTROL  변수를 사용하여 설정된 선택 사항인 ]방문자 ID`s.visitorID`. 이 값은 사용자 인증 후 채워지며, 회사가 여러 디지털 마케팅 채널에 걸쳐 사용자를 추적하는 데 사용하는 ID와 일치할 수 있습니다. |
| 유효 방문자 ID | 유효 [!UICONTROL 방문자 ID]는 사용자 프로필에 사용하는 실제 ID입니다. 이 값은 [!UICONTROL 방문자 ID] 쿠키로 설정되거나, [!UICONTROL 방문자 ID] 변수가 제공될 경우 이 변수로 설정됩니다. |

