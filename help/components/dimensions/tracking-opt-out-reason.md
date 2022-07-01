---
title: 옵트아웃 이유 추적
description: 개인 정보 설정을 활성화하면 제외할 데이터를 미리 봅니다.
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
source-git-commit: b7209b914695423099266f5c507eaa34c2b98bc5
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 9%

---

# 옵트아웃 이유 추적

*이 페이지는 특정 보고서 세트 설정을 활성화하면 영향을 받을 수 있는 차원을 참조합니다. 와 관련이 없습니다 [Adobe Experience Cloud ID 옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=ko-KR).*

옵트아웃 이유 추적 차원은 개인 정보 설정을 활성화한 경우 제외되는 데이터에 대한 미리 보기 역할을 합니다. 이 차원은 주로 활성화한 경우 구현이 부정적인 영향을 받는지 확인하는 데 사용됩니다 [개인 정보 설정](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) 보고서 세트 설정에서 을 선택합니다.

일반 구현에서는 개인 정보 설정이 아직 활성화되어 있지 않은 경우 이 차원에 따른 전체 보고서 세트 트래픽의 1% 이상을 봅니다. 모든 트래픽의 1%보다 높은 백분율은 AppMeasurement가 자사 쿠키를 설정하지 못하도록 하는 잠재적 구현 문제를 제안합니다.

## 이 차원을 데이터로 채우기

이 차원은 아직 활성화되지 않은 모든 구현에 대해 즉시 작동합니다 [개인 정보 설정](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html). 조직에서 이미 을(를) 활성화한 경우 **[!UICONTROL 모든 쿠키를 차단한 사용자 제거]** 데스크톱 및 모바일 브라우저 모두에 대해 설정하면 이 차원에 데이터가 포함되어 있지 않습니다.

## 차원 항목

차원 항목은 `"Cookies disabled by Desktop Browser"` 및 `"Cookies disabled by Mobile Browser"`를 포함합니다.

* **데스크탑 브라우저가 쿠키를 비활성화했습니다.**: 방문자가 데스크톱 브라우저를 사용하여 쿠키를 차단했습니다. **[!UICONTROL 데스크톱 브라우저에서 모든 쿠키를 차단한 사용자 제거]** 이 비활성화되어 있습니다.
* **모바일 브라우저에 의해 쿠키가 비활성화됨**: 방문자가 모바일 브라우저를 사용하여 쿠키를 차단했습니다. **[!UICONTROL 모바일 브라우저에서 모든 쿠키를 차단한 사용자 제거]** 이 비활성화되어 있습니다.
