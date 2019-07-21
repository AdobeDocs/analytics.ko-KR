---
description: 'null'
keywords: 데이터 피드; 작업; 방문자; Experience Cloud ID; Analytics 방문자 ID; 식별
seo-description: 'null'
seo-title: 방문자 식별
solution: Analytics
title: 방문자 식별
topic: Reports & Analytics
uuid: 2490 B 67 E-A 333-422 D -82 FA-CB 0670 EF 2 E 0 C
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 방문자 식별

Analytics에서는 방문자를 식별하는 몇 가지 메커니즘을 제공합니다([방문자 식별](../../../export/analytics-data-feed/c-df-contents/datafeeds-visid.md#concept_BE966BABA7D0475BB706BC6676B8FA11)에 나열됨). Regardless of the method used to identify a visitor, in data feeds the final visitor ID used by Analytics is split across the `post_visid_high` and `post_visid_low` columns, even when using the Identity Service.

**고유 방문자 식별:**

1. Exclude all rows where `exclude_hit > 0`.
1. Exclude all rows with `hit_source = 5,7,8,9`. 5,8 및 9는 데이터 소스를 사용하여 업로드된 요약 행입니다. 7은 방문 및 방문자 카운트에 포함되지 않아야 하는 거래 ID 데이터 소스 업로드를 나타냅니다. see [히트 출처 조회](../../../export/analytics-data-feed/c-df-contents/datafeeds-hit-source.md#concept_FE4C114F6A524F7593D5CAC944C36C42)
1. `post_visid_high``post_visid_low`와 결합. All hits across all dates that contain this combination of `post_visid_high` and `post_visid_low` can be considered as coming from same visitor.

방문자 ID 값을 결정(예: 쿠키 승인 계산을 위해)하는 데 사용된 메커니즘을 결정하려는 경우, `post_visid_type`에는 사용된 ID 메서드를 가리키는 조회 키가 들어 있습니다. 조회 키는 [아래 표](../../../export/analytics-data-feed/c-df-contents/datafeeds-visid.md#table_D267D36451F643D1BB68AF6FEAA6AD1A)에 방문자 ID 메커니즘과 함께 나열되어 있습니다.

## Experience Cloud ID {#section_1628ED37D31E4B0EB75632E397A06B29}

Experience Cloud ID는 별도의 열 `mcvisid`로 보고됩니다. 이 ID는 자체 열로 보고되므로, Analytics에서 이 ID나 다른 ID를 사용하여 방문자를 식별하는 경우 명백하지 않을 수 있습니다.

If the Experience Cloud ID was used to identify the visitor, the ID will be contained in the `post_visid_high` and `post_visid_low` columns and the `post_visid_type` will be set to 5. When calculating metrics, you should use the value from the `post_visid_high` and `post_visid_low` columns since these columns will always contain the final visitor ID.

>[!TIP]
>
> When using the Adobe Analytics visitor ID as a key for other systems, always use `post_visid_high` and `post_visid_low`. 이러한 필드는 데이터 피드에서 모든 행과 함께 값을 제공하는 유일한 방문자 ID 필드입니다.

## Analytics 방문자 ID {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Analytics에서 방문자를 식별할 수 있는 방법에는 몇 가지가 있습니다(다음 표에 선호도 순으로 나열됨).

| 사용된 순서 | 쿼리 매개 변수(컬렉션 메서드) | post_visid_type 열 값 | 존재할 때 |
|---|---|---|---|
| ![](assets/step1_icon.png) | [vid(s.visitorID)](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_custom) | 0 | s.visitorID가 설정되어 있습니다. |
| ![](assets/step2_icon.png) | [aid(s_vi 쿠키)](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_analytics) | 3 | 방문자 ID 서비스를 배포하기 전에 방문자에게 기본 s_vi 쿠키가 있었거나, 여러분에게 방문자 ID [유예 기간](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_grace_period)이 설정되어 있습니다. |
| ![](assets/step3_icon.png) | [mid (Identity Service에 의해 설정된 AMCV_ 쿠키)](https://marketing.adobe.com/resources/help/en_US/mcvid/) | 5 | 방문자의 브라우저가 쿠키를 승인하고 (퍼스트 파티) ID 서비스가 배포됩니다. |
| ![](assets/step4_icon.png) | [fid(H.25.3 이상 또는 AppMeasurement for JavaScript의 폴백 쿠키)](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_fallback) | 4 | 방문자의 브라우저가 쿠키를 승인합니다(퍼스트 파티). |
| ![](assets/step5_icon.png) | [HTTP 모바일 가입자 헤더](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_mobile) | 2 | 장치는 모바일 장치로 인식됩니다. |
| ![](assets/step6_icon.png) | [IP 주소, 사용자 에이전트, 게이트웨이 IP 주소](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_fallback) | 1 | 방문자의 브라우저가 쿠키를 승인하지 않습니다. |

많은 시나리오에서 2개나 3개의 서로 다른 ID가 한 호출에 있는 경우를 볼 수도 있습니다. 하지만 Analytics에서는 해당 목록에 있는 첫 번째 ID를 공식 방문자 ID로 사용하며, `post_visid_high` 및 `post_visid_low` 열에 이 값을 분할합니다. 예를 들어, 사용자 지정 방문자 ID("vid" 쿼리 매개 변수에 포함됨)를 설정하는 경우, 이 ID는 동일한 히트에 있을 수 있는 다른 ID보다 먼저 사용됩니다.
