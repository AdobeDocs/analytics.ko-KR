---
title: 브라우저 유형
description: 브라우저를 만든 조직입니다.
feature: Dimensions
exl-id: 2a88ebc6-879e-4e5b-a8e5-40a32d54ac1b
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 67%

---

# 브라우저 유형

&#39;브라우저 유형&#39; [차원](overview.md)은(는) 방문자가 사용하는 브라우저를 만든 조직을 나열합니다. 이 차원은 방문자가 주로 사용하는 브라우저를 확인하려는 경우 유용합니다. 동일한 브라우저의 서로 다른 버전을 별도의 차원 항목으로 나열하지 않는다는 점에서 &#39;브라우저&#39; 차원보다 높은 가치를 제공합니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. Adobe은 사용자 에이전트와 브라우저 간 조회를 유지 관리하기 위해 [DeviceAtlas](https://deviceatlas.com/)와(과) 파트너 관계를 맺고 있습니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* Web SDK 구현의 경우 [데이터 스트림을 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko)할 때 [!UICONTROL 장치 조회]를 사용하도록 설정하십시오.

## 차원 항목

차원 항목에는 브라우저를 만드는 조직이 포함됩니다. 일반적인 차원 항목에는 `"Google"` ([!DNL Chrome] 작성자), `"Apple"` ([!DNL Safari] 작성자), `"Microsoft"` ([!DNL Edge] 작성자) 및 `"Mozilla"` ([!DNL Firefox] 작성자) 등이 포함됩니다.
