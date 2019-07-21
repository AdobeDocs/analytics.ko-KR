---
description: Adobe에서는 쿠키를 사용하여 고유한 브라우저/장치를 추적합니다.
keywords: Analytics 구현
seo-description: Adobe에서는 쿠키를 사용하여 고유한 브라우저/장치를 추적합니다.
seo-title: 고유 방문자 식별
solution: Analytics
subtopic: 방문자 수
title: 고유 방문자 식별
topic: 개발자 및 구현
uuid: ED 4 DEE 75-ECFB -4715-8122-461983 C 7 DD 8 F
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 고유 방문자 식별

Adobe에서는 쿠키를 사용하여 고유한 브라우저/장치를 추적합니다.

## Analytics 방문자 ID 순서 {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Adobe Analytics에서는 방문자를 식별하는 메커니즘을 몇 가지 제공합니다. 다음 표에는 Analytics에서 방문자를 식별할 수 있는 다양한 방법이 나열되어 있습니다(선호도 순).

| 사용된 순서 | 쿼리 매개 변수(컬렉션 방법) | 제공되는 경우 |
|---|---|---|
| ![](assets/step1_icon.png) | [vid (s.visitorID)](../../../implement/js-implementation/c-unique-visitors/visid-custom.md#concept_4A2000F4B6ED41E99CA6118A6D74ECE8) | s.visitorID가 설정된 경우 |
| ![](assets/step2_icon.png) | [aid (s_vi 쿠키)](../../../implement/js-implementation/c-unique-visitors/visid-analytics.md#concept_74F6B4B9B2FA415AB5D029A1F8F099BC) | 방문자는 방문자 ID 서비스를 배포하기 전에 기존 s_vi 쿠키가 있었거나 구성된 방문자 ID 유예 기간이 있습니다. |
| ![](assets/step3_icon.png) | [mid(Experience Cloud 방문자 ID 서비스에 의해 설정된 AMCV_ 쿠키)](https://marketing.adobe.com/resources/help/en_US/mcvid/) | 방문자의 브라우저가 쿠키를 수락하는 경우(퍼스트 파티) |
| ![](assets/step4_icon.png) | [fid(H.25.3 이상의 폴백 쿠키 또는 AppMeasurement for JavaScript)](../../../implement/js-implementation/c-unique-visitors/visid-fallback.md#concept_EBCBF9EB390E45A2BA20DB6BE931C505) | 방문자의 브라우저가 쿠키를 수락하는 경우(퍼스트 파티) |
| ![](assets/step5_icon.png) | [IP 주소, 사용자 에이전트, 게이트웨이 IP 주소](../../../implement/js-implementation/c-unique-visitors/visid-fallback.md#section_104819D74C594ECE879144FCC5DEF4BF) | 방문자의 브라우저가 쿠키를 승인하지 않습니다. |

많은 시나리오에서 2개나 3개의 서로 다른 ID가 같은 호출에 있는 경우를 볼 수도 있습니다. 하지만 Analytics에서는 해당 목록에 있는 첫 번째 ID를 공식 방문자 ID로 사용합니다. 예를 들어, 사용자 지정 방문자 ID("vid" 쿼리 매개 변수에 포함됨)를 설정하는 경우, 이 ID는 동일한 히트에 있을 수 있는 다른 ID보다 먼저 사용됩니다.

>[!NOTE]
>
>각 Analytics 방문자 ID는 Adobe 서버의 방문자 프로필과 연관되어 있습니다. 방문자 프로필은 모든 방문자 ID 쿠키 만료와 관계없이 비활성 기간 13달 후 삭제됩니다.
