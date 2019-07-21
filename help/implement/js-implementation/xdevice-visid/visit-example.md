---
description: 일반적인 고객 상호 작용에서 전송된 서버 호출의 샘플이 들어 있는 예
keywords: Analytics 구현
seo-description: 일반적인 고객 상호 작용에서 전송된 서버 호출의 샘플이 들어 있는 예
seo-title: 방문 예
solution: Analytics
subtopic: 방문자 수
title: 방문 예
topic: 개발자 및 구현
uuid: BC 5 F 8 F 56-52 E 3-42 D 8-AF 1 A -7 F 5 C 7 B 9496 C 0
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# 방문 예

>[!IMPORTANT]
>
>장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

일반적인 고객 상호 작용에서 전송된 서버 호출의 샘플이 들어 있는 예

| 서버 호출 | 작업 | 방문자 ID 쿠키 | 방문자 ID 변수 | 유효 방문자 ID | 방문 페이지 번호 | 방문 횟수 |
|--- |--- |--- |--- |--- |--- |--- |
| 1 | 방문자가 마케팅 이메일에 있는 링크를 클릭하고 집 컴퓨터에서 사이트를 방문합니다. 이 방문자는 과거에 사이트를 7번 더 방문했습니다. | 1 | - | 1 | 1 | 8 |
| 2-8 | 사이트에서 7개의 페이지를 더 방문합니다. | 1 | - | 1 | 2-8 | 8 |
| 9 | 집 컴퓨터를 인증합니다. | 1 | CID1 | CID1 | 9 <br>This is CID1's first hit ever, so it takes over and continues on the visitor profile from Visitor ID 1.</br> | 8 |
| 10 | 한 페이지를 더 방문합니다. | 1 | CID1 | CID1 | 10 | 8 |
| 11 | 사무실 랩톱에서 사이트를 엽니다. 이 방문자는 이 장치를 사용하기 전에는 여러분의 사이트를 방문한 적이 없습니다. | 2 | - | 2 | 1 | 1 |
| 12 | 랩톱을 인증합니다. | 2 | CID1 | CID1 | 1 | 9 |
| 13 | 한 페이지를 더 봅니다. | 2 | CID1 | CID1 | 2 | 9 |