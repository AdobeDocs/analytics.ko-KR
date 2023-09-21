---
title: 옵트아웃 이유 추적
description: 개인 정보 설정을 활성화한 경우 제외되는 데이터를 미리 봅니다.
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 9%

---

# 옵트아웃 이유 추적

*이 페이지는 [차원](overview.md) 이를 통해 특정 보고서 세트 설정을 활성화함으로써 발생할 수 있는 데이터 영향을 확인할 수 있습니다. 와(과) 관련 없음 [Adobe Experience Cloud ID 옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=ko-KR).*

옵트아웃 이유 추적 차원은 개인 정보 설정을 활성화한 경우 제외되는 데이터에 대한 미리 보기 역할을 합니다. 이 차원은 주로 을 활성화한 경우 구현이 부정적인 영향을 받는지 확인하는 데 사용됩니다 [개인 정보 설정](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) 보고서 세트 설정에서 을 선택합니다.

일반적인 구현은 개인 정보 설정이 아직 활성화되지 않은 경우 이 차원에서 전체 보고서 세트 트래픽의 1% 이하를 봅니다. 모든 트래픽의 1%보다 높은 백분율은 AppMeasurement이 자사 쿠키를 설정하지 못하도록 하는 잠재적 구현 문제를 나타냅니다.

## 이 차원을 데이터로 채우기

이 차원은 아직 활성화되지 않은 모든 구현에 대해 즉시 작동합니다 [개인 정보 설정](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html). 조직에서 이미 다음을 활성화한 경우 **[!UICONTROL 모든 쿠키를 차단한 사용자 제거]** 데스크톱 및 모바일 브라우저 모두에 대해 설정하면 이 차원에는 데이터가 포함되지 않습니다.

## 차원 항목

차원 항목은 `"Cookies disabled by Desktop Browser"` 및 `"Cookies disabled by Mobile Browser"`를 포함합니다.

* **데스크탑 브라우저에서 쿠키를 비활성화함**: 방문자가 데스크탑 브라우저를 사용하여 쿠키를 차단했습니다. **[!UICONTROL 데스크톱 브라우저에서 모든 쿠키를 차단한 사용자 제거]** 이(가) 비활성화되었습니다.
* **모바일 브라우저에서 쿠키를 비활성화함**: 방문자가 모바일 브라우저를 사용하여 쿠키를 차단했습니다. **[!UICONTROL 모바일 브라우저에서 모든 쿠키를 차단한 사용자 제거]** 이(가) 비활성화되었습니다.
