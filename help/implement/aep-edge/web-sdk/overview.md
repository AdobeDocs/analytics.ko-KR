---
title: Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현
description: 웹 SDK을 사용하여 Adobe Analytics으로 데이터를 전송합니다.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
feature: Implementation Basics
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/4pS-q3F3W7D1ojdMkCzgUyZkO3LDt1DpFfxqcTtZXLQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 42%

---

# Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현

[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/web-sdk/home.html?lang=ko)를 사용하여 데이터를 Adobe Analytics로 전송할 수 있습니다. 웹 SDK을 구현하는 기본 방법에는 두 가지가 있으며, 각 방법에는 두 가지 구현 유형이 있습니다.

| | **AppMeasurement에서 마이그레이션** | **웹 SDK 구현 정리** |
| --- | --- | --- |
| **태그 사용** | [Analytics 확장에서 웹 SDK 확장으로 마이그레이션](analytics-extension-to-web-sdk.md) | [Web SDK 확장을 사용하여 Adobe Analytics에 데이터 보내기](web-sdk-tag-extension.md) |
| **JavaScript 사용** | [AppMeasurement에서 웹 SDK JavaScript 라이브러리로 마이그레이션](appmeasurement-to-web-sdk.md) | [웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics에 데이터 보내기](web-sdk-javascript-library.md) |

조직에서 새 웹 SDK 구현을 필요로 하고 향후 Customer Journey Analytics을 사용할 계획이라면, Adobe은 자체 스키마를 사용하여 깔끔한 웹 SDK 구현을 권장합니다. Customer Journey Analytics 사용 안내서에서 [Adobe Experience Platform Web SDK을 통해 데이터 수집](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk)을 참조하십시오.

## 추가 리소스

태그는 높은 자유도로 사용자 정의할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

- [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ko-KR#): 인터페이스의 작동 방식과 이요 가능한 확장 유형에 대해 알아봅니다.

- [Adobe Experience Platform 웹 SDK 설명서](https://experienceleague.adobe.com/docs/web-sdk.html?lang=ko-KR)
