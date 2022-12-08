---
description: 다중 세트 태그 지정을 구현하여 여러 보고서 세트에 이미지 요청을 보내는 방법에 대해 알아봅니다.
title: 다중 세트 태그 지정 구현
feature: Implementation Basics
exl-id: c7fb0478-97e1-4367-8742-e7539f6f82e7
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---

# 다중 세트 태그 지정 구현

[다중 세트 태그 지정](/help/admin/admin/c-manage-report-suites/rollup-report-suite.md)을 사용하면 글로벌 보고서 세트뿐만 아니라 개별 하위 보고서 세트에도 이미지 요청을 보낼 수 있으므로 회사 글로벌 보고서 세트 데이터의 하위 집합을 다른 최종 사용자에게 제공할 수 있습니다.

다중 세트 태그 지정을 구현하려면 글로벌 보고서 세트에 대한 RSID(보고서 세트 ID)와 웹 페이지 및 앱의 추적 코드에 해당 하위 보고서 세트에 대한 RSID를 포함해야 합니다.

* Adobe Experience Platform 태그 구현의 경우 [[!DNL Analytics] 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=ko-KR)에 대한 각 보고서 세트를 지정합니다.

* 레거시 JavaScript 및 모바일 SDK 구현의 경우 공백 없이 쉼표로 RSID를 구분하십시오(`rsid1,rsid2,rsid3` 등).

* 다른 구현 유형의 경우 필수 구문을 사용하여 여러 RSID를 나열합니다.

>[!TIP]
>
> 가장 좋은 방법은 글로벌 보고서 세트 또는 보고서 세트 ID를 먼저 나열하는 것입니다.

다중 세트 태그 지정은 글로벌 보고서 세트에 대한 기본 호출과 각 하위 보고서 세트에 대한 보조 호출 등 각 이미지 요청에 대해 여러 서버 호출을 발생시킵니다.

>[!NOTE]
>
> [가상 보고서 세트](/help/components/vrs/vrs-about.md)는 회사의 글로벌 보고서 세트 데이터의 하위 집합을 다른 최종 사용자에게 제공할 수도 있지만 보조 서버 호출은 발생하지 않습니다.

## 다중 세트 태그 지정 또는 가상 보고서 세트를 구현해야 합니까?

다중 세트 태그 지정 대신 가상 보고서 세트를 사용하는 것이 모범 사례인 경우가 많지만 조직에 가장 적합한 보고서 세트 접근 방식을 비즈니스 요구 사항에 의해 결정됩니다.

가상 보고서 세트가 최상의 접근 방식인지 파악하려면 “[가상 보고서 세트 및 다중 세트 태그 지정 고려 사항](/help/components/vrs/vrs-considerations.md)”을 참조하십시오. 다중 세트 태그 지정과 가상 보고서 세트 기능을 비교하려면 “[가상 보고서 세트 vs. 다중 세트 태그 지정](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)”도 참조하십시오.
