---
title: Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현
description: Web SDK를 사용하여 데이터를 Adobe Analytics으로 전송합니다.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: d6c16d8841110e3382248f4c9ce3c2f2e32fe454
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 39%

---

# Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현

[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/web-sdk/home.html)를 사용하여 데이터를 Adobe Analytics로 전송할 수 있습니다. Web SDK를 구현하는 기본 메서드는 두 가지가 있으며, 각 메서드에는 두 가지 구현 유형이 있습니다.

| | **AppMeasurement에서 마이그레이션** | **웹 SDK 구현 정리** |
| --- | --- | --- |
| **태그 사용** | [Analytics 확장에서 웹 SDK 확장으로 마이그레이션](analytics-extension-to-web-sdk.md) | [Web SDK 확장을 사용하여 Adobe Analytics에 데이터 보내기](web-sdk-tag-extension.md) |
| **JavaScript 사용** | [AppMeasurement에서 Web SDK JavaScript 라이브러리로 마이그레이션](appmeasurement-to-web-sdk.md) | [Web SDK JavaScript 라이브러리를 사용하여 Adobe Analytics에 데이터 보내기](web-sdk-javascript-library.md) |

조직에서 새 웹 SDK 구현을 필요로 하고 차후에 Customer Journey Analytics을 사용할 계획이라면, Adobe은 자체 스키마를 사용하여 깔끔한 웹 SDK 구현을 권장합니다. Customer Journey Analytics 사용 안내서에서 [Adobe Experience Platform Web SDK를 통해 데이터 수집](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk)을 참조하십시오.

## 추가 리소스

태그는 높은 자유도로 사용자 정의할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

- [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ko-KR#): 인터페이스의 작동 방식과 이요 가능한 확장 유형에 대해 알아봅니다.

- [Adobe Experience Platform Web SDK 설명서](https://experienceleague.adobe.com/docs/web-sdk.html?lang=ko-KR)
