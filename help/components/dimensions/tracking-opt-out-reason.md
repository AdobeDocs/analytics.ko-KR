---
title: 옵트아웃 이유 추적
description: 개인 정보 설정을 활성화한 경우 제외되는 데이터를 미리 봅니다.
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
TQID: https://experienceleague.adobe.com/mFYYrj4iBWBi87sErHnWTYXce3lUhV0pwUt63x3vfnY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 11%

---

# 옵트아웃 이유 추적

*이 페이지는 특정 보고서 세트 설정을 활성화함으로써 발생할 수 있는 데이터 영향을 확인할 수 있는 [차원](overview.md)을 참조합니다. [Adobe Experience Cloud ID 옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=ko-KR)와(과) 관련이 없습니다.*

옵트아웃 이유 추적 차원은 개인 정보 설정을 활성화한 경우 제외되는 데이터에 대한 미리 보기 역할을 합니다. 이 차원은 주로 보고서 세트 설정에서 [개인 정보 설정](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html?lang=ko)을 사용하도록 설정한 경우 구현이 부정적인 영향을 받는지 확인하는 데 사용됩니다.

일반적인 구현은 개인 정보 설정이 아직 활성화되지 않은 경우 이 차원에서 전체 보고서 세트 트래픽의 1% 이하를 봅니다. 모든 트래픽의 1%보다 높은 백분율은 AppMeasurement이 자사 쿠키를 설정하지 못하도록 하는 잠재적 구현 문제를 나타냅니다.

## 이 차원을 데이터로 채우기

이 차원은 아직 [개인 정보 설정](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html?lang=ko)을 활성화하지 않은 모든 구현에 대해 즉시 작동합니다. 조직이 데스크톱 및 모바일 브라우저 모두에 대해 **[!UICONTROL 모든 쿠키를 차단한 사용자 제거]** 설정을 이미 사용하도록 설정한 경우 이 차원에는 데이터가 포함되지 않습니다.

## 차원 항목

차원 항목은 `"Cookies disabled by Desktop Browser"` 및 `"Cookies disabled by Mobile Browser"`를 포함합니다.

* **데스크톱 브라우저에서 쿠키를 사용하지 않도록 설정**: 방문자가 데스크톱 브라우저를 사용하여 쿠키를 차단했으며 **[!UICONTROL 데스크톱 브라우저에서 모든 쿠키를 차단한 사용자 제거]**&#x200B;가 사용하지 않도록 설정되었습니다.
* **모바일 브라우저에서 쿠키가 비활성화됨**: 방문자가 모바일 브라우저를 사용하여 쿠키를 차단했으며 **[!UICONTROL 모바일 브라우저에서 모든 쿠키를 차단한 사용자 제거]**&#x200B;가 비활성화되었습니다.
