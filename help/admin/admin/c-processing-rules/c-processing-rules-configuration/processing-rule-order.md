---
description: 처리 규칙이 중요한 Analytics 데이터 파이프라인에 있는 경우.
subtopic: Processing rules
title: 처리 순서
feature: Processing Rules
exl-id: c7143527-017c-4550-b55e-09ea437d7c85
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 49%

---

# 처리 순서

처리 규칙을 효과적으로 사용하려면 데이터 수집 중에 규칙이 적용되는 시기를 이해하는 것이 중요합니다.

![처리 순서](assets/analytics_processing_order.png)

다음 표는 처리 규칙이 적용되기 전후에 일반적으로 사용할 수 있는 데이터를 나열합니다.

## 처리 규칙 이전

| 차원 | 설명 |
|--- |--- |
| [다이내믹 변수](/help/implement/vars/page-vars/dynamic-variables.md) | HTTP 헤더 또는 다른 변수에서 정보를 가져와서 동적으로 채우는 변수입니다. |
| [AppMeasurement](/help/implement/home.md) | AppMeasurement 라이브러리에서 사용되는 함수 및 플러그인은 브라우저 또는 클라이언트 애플리케이션에서 실행됩니다. |
| [태그 구현](/help/implement/launch/overview.md) | Adobe Experience Platform 데이터 수집 내의 Adobe Analytics 확장에 정의된 규칙입니다. |
| [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/analytics-overview.html) | 웹 SDK를 통해 수집된 데이터는 Adobe Experience Edge로 전송되고 원하는 보고서 세트로 전달됩니다. |
| [보트 규칙](/help/admin/admin/bot-removal/bot-rules.md) | 알려진 스파이더 및 보트에서 생성한 트래픽을 제거할 수 있습니다. |

## 처리 규칙 이후

| 차원 | 설명 |
|--- |--- |
| VISTA가 추가한 데이터 | 처리 규칙은 VISTA 이전에 적용됩니다. |
| 방문 페이지 번호 | 처리 규칙은 현재 히트에 포함된 데이터만 인식합니다. 방문 페이지 번호는 처리 규칙이 적용된 후 컴파일됩니다. |
| 클린 URL이 설정되지 않은 경우 페이지 이름으로 추가됩니다. | 처리 규칙 및 VISTA가 적용된 후, 설정된 페이지 이름이 없는 경우 클린 URL이 페이지 이름으로 추가됩니다. 이 로직은 처리 규칙이 적용된 후 발생하므로 Adobe은 페이지 이름이 비어 있는지 확인하기 위해 조건을 추가하는 것이 좋습니다.  를 실행하면 **[!UICONTROL 사이트 컨텐츠]** > **[!UICONTROL 페이지]** 보고서 및 페이지 이름에 대한 URL 값이 표시되면 페이지 이름 변수가 비어 있을 수 있습니다.  빈 페이지 이름을 테스트하거나 페이지 이름 또는 페이지 URL에 특정 값이 포함되어 있는지 테스트하는 조건을 설정할 수 있습니다. 그런 다음 필요에 따라 페이지 이름을 설정할 수 있습니다. |
| 마케팅 채널 처리 규칙 | 처리 규칙을 사용하여 [마케팅 채널 처리 규칙](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-rules.html)으로 처리할 데이터를 준비할 수 있습니다. |
| GEO 조회 | 방문자 주 및 방문자 ZIP/우편 번호 값을 포함합니다. |
| eVar 지속성 | 이전 히트에 포함된 evar는 규칙 처리 중에 각 히트에 지속되지 않습니다. 처리되는 현재 히트에서 설정된 eVar만 사용할 수 있습니다. |

## VISTA를 사용하여 히트를 복사할 때 처리 규칙이 적용되는 방식

히트를 다른 보고서 세트에 복사하도록 VISTA 규칙을 구성한 경우 히트가 다른 보고서 세트에 정의된 처리 규칙을 통해 전송됩니다.

원래 보고서 세트에 처리 규칙이 정의되어 있는 경우, 이러한 규칙은 엔지니어링 서비스에서 VISTA 규칙이 구성된 방식에 따라 적용되거나 적용되지 않을 수 있습니다. VISTA 규칙이 &quot;pre&quot; 또는 &quot;post&quot; 값을 추가 보고서 세트에 복사하는지 구현 전문가에게 물어볼 수 있습니다. &quot;pre&quot; 값이 복사되면 원래 보고서 세트에 정의된 처리 규칙은 적용되지 않습니다. &quot;post&quot; 값이 복사되면 히트가 복사되기 전에 처리 규칙이 적용됩니다.
