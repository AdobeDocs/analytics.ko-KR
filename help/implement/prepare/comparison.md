---
title: 구현 방법 비교
description: Adobe Analytics로 데이터를 전송하는 각 방법의 이점을 확인하십시오.
exl-id: 19353255-6356-4426-a2ef-5a2672a00eca
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: c476a1a19ae514f75fce8bd8e6d447d85de67a84
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 56%

---

# 구현 방법 비교

Adobe Analytics를 구현하는 각 방법을 서로 비교하는 방법을 확인하십시오. 이러한 테이블을 사용하여 조직에서 데이터를 Adobe에 보내는 가장 이상적인 방법을 결정할 수 있습니다. 자세한 내용을 보려면 각 열을 클릭합니다.

## 웹

| | [AppMeasurement](/help/implement/js/overview.md) | [Adobe Analytics 확장](/help/implement/launch/overview.md) | [웹 SDK](/help/implement/aep-edge/web-sdk/overview.md#web-sdk) | [Web SDK 확장](/help/implement/aep-edge/web-sdk/overview.md#web-sdk-extension) |
| --- | --- | --- | --- | --- |
| 구현 요구 사항 | 참조 `AppMeasurement.js` 각 페이지에서 변수를 정의하고 다음을 사용하여 데이터를 전송합니다. `s.t()` Adobe Analytics으로 | 각 페이지의 태그 로더를 참조하려면 데이터 수집 UI를 사용하여 변수를 정의하고 데이터를 Adobe Analytics으로 전송합니다 | 참조 `Alloy.js` 각 페이지에서 `alloy("sendEvent",{})` Edge Network를 사용하여 XDM 개체를 작성하고 원하는 데이터를 Adobe Analytics으로 보내려면 | 각 페이지에서 태그 로더를 참조하려면 데이터 수집 UI를 사용하여 XDM 개체를 구성하고 Edge Network를 사용하여 원하는 데이터를 Adobe Analytics으로 전송합니다 |
| 데이터 대상 | Adobe Analytics로 직접 전송 | Adobe Analytics로 직접 전송 | Adobe Experience Platform Edge로 전송, 데이터를 Adobe Analytics로 전달 | Adobe Experience Platform Edge로 전송, 데이터를 Adobe Analytics로 전달 |
| 구현 조정의 어려움 | 모든 구현 변경에 대해 웹 사이트 코드에 대한 액세스 권한이 필요합니다. | 로더 태그를 설치하려면 웹 사이트 코드를 한 번 변경합니다. 모든 추가 구현 업데이트는 데이터 수집 UI에서 수행할 수 있습니다. | 모든 구현 변경에 대해 웹 사이트 코드에 대한 액세스 권한이 필요합니다. | 로더 태그를 설치하려면 웹 사이트 코드를 한 번 변경합니다. 모든 추가 구현 업데이트는 데이터 수집 UI에서 수행할 수 있습니다. |
| A4T 처리 방법 | A4T 호출은 Adobe로 전송된 히트에 포함됩니다. | A4T 호출은 Adobe로 전송된 히트에 포함됩니다. | A4T 호출은 별도의 히트로 전송됩니다. | A4T 호출은 별도의 히트로 전송됩니다. |
| 컨텍스트 데이터 | `s.contextData` 사용. | 사용자 지정 코드 블록에서 `s.contextData` 사용 | 매핑되지 않은 모든 필드는 자동으로 `a.x.*` 컨텍스트 데이터 변수로 전송됩니다. | 매핑되지 않은 모든 필드는 자동으로 `a.x.*` 컨텍스트 데이터 변수로 전송됩니다. |

{style="table-layout:auto"}

## 모바일 및 기타

>[!CAUTION]
>
>버전 4 Mobile SDK에 대한 지원은 2021년 8월 31일에 종료되었습니다. 다음을 참조하십시오 [Adobe Mobile Services 사용 종료 FAQ](https://experienceleague.adobe.com/docs/discontinued/using/mobile-services.html) 추가 정보.


| | [Mobile SDK](/help/implement/aep-edge/mobile-sdk/overview.md) | [서버 API](/help/implement/aep-edge/server-api/overview.md) |
| --- | --- | --- |
| 구현 요구 사항 | 앱에서 태그 로더를 참조한 다음 데이터 수집 UI에서 직접 API 호출 또는 규칙을 사용하여 XDM 개체를 구성하고 Edge Network를 사용하여 원하는 데이터를 Adobe Analytics으로 전송합니다 | Edge Network Server API를 사용하여 XDM 개체를 구성하고 Edge Network를 사용하여 원하는 데이터를 Adobe Analytics으로 전송합니다 |
| 데이터 대상 | Adobe Experience Platform Edge로 전송, 데이터를 Adobe Analytics로 전달 | Adobe Experience Platform Edge로 전송, 데이터를 Adobe Analytics로 전달 |
| 구현 조정의 어려움 | 직접 API 호출이 수행되는 앱 코드를 변경하거나 데이터 수집 UI에서 변경합니다 | 모든 구현 변경에 대해 앱 코드에 액세스해야 함 |
| A4T 처리 방법 | A4T 호출은 별도의 히트로 전송됩니다. | A4T 호출은 별도의 히트로 전송됩니다. |
| 컨텍스트 데이터 | 매핑되지 않은 모든 필드는 자동으로 `a.x.*` 컨텍스트 데이터 변수로 전송됩니다. | 매핑되지 않은 모든 필드는 자동으로 다음으로 전송됩니다. `a.x.*` 컨텍스트 데이터 변수 |

{style="table-layout:auto"}
