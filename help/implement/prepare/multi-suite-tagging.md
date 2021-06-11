---
description: 다중 세트 태깅을 구현하여 이미지 요청을 여러 보고서 세트로 보내는 방법을 알아봅니다.
title: 다중 세트 태깅 구현
exl-id: null
source-git-commit: 81da9ff9b00a69c49c028fc7f006c161d8ff21d4
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 3%

---


# 다중 세트 태깅 구현

[다중 세트 ](/help/admin/c-manage-report-suites/rollup-report-suite.md) 태깅을 사용하면 글로벌 보고서 세트뿐만 아니라 개별 하위 보고서 세트에 이미지 요청을 전송할 수 있으므로 회사의 글로벌 보고서 세트 데이터의 하위 세트를 다른 최종 사용자에게 제공할 수 있습니다.

다중 세트 태깅을 구현하려면 글로벌 보고서 세트에 대한 RSID(보고서 세트 ID)와 웹 페이지 및 앱의 추적 코드에 적용 가능한 하위 보고서 세트에 대한 RSID를 포함해야 합니다.

* Adobe Experience Platform Launch 구현의 경우 [[!DNL Analytics] 확장](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html?lang=kr)에 대한 각 보고서 세트를 지정합니다.

* 기존 JavaScript 및 모바일 SDK 구현의 경우 RSID를 쉼표로(공백 없음) 구분하십시오(`rsid1,rsid2,rsid3` 등).

* 다른 구현 유형의 경우 필요한 구문을 사용하여 여러 RSID를 나열합니다.

>[!TIP]
>
> 가장 좋은 방법은 글로벌 보고서 세트 또는 보고서 세트 ID를 먼저 나열하는 것입니다.

다중 세트 태깅은 각 이미지 요청에 대해 여러 서버 호출을 발생시킵니다.글로벌 보고서 세트에 대한 기본 호출 및 각 하위 보고서 세트에 대한 보조 호출.

>[!NOTE]
>
> [다른 최종 사용자에게 회사의 글로벌 보고서 세트 데이터의 하위 세트를 제공할 수도 있는 가상 보고서 세트는](/help/components/vrs/vrs-about.md) 보조 서버 호출을 발생시키지 않습니다.

## 다중 세트 태깅 또는 가상 보고서 세트를 구현해야 합니까?

다중 세트 태깅 대신 가상 보고서 세트를 사용하는 것이 가장 좋은 방법이지만, 비즈니스 요구 사항에 따라 조직에 가장 적합한 보고서 세트 접근 방식이 결정됩니다.

가상 보고서 세트가 가장 적합한 방법인지 알려면 &quot;[가상 보고서 세트와 다중 세트 태깅 고려 사항](/help/components/vrs/vrs-considerations.md)&quot;을 참조하십시오. 다중 세트 태깅 및 가상 보고서 세트 기능을 비교하려면 &quot;[가상 보고서 세트와 다중 세트 태깅](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)&quot;을 참조하십시오.
