---
title: Experience Cloud ID를 가진 사용자
description: Experience Cloud ID가 있는 교차 장치 분석에 있는 사람 수입니다.
source-git-commit: eaf0c3b751a5fbdc70ad6bef501dbf9e8400339c
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 21%

---

# Experience Cloud ID를 가진 사용자

&#39;Experience Cloud ID를 가진 사람&#39;은 [교차 장치 분석](../cda/overview.md) 지표로서, [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko-KR)를 사용하여 Adobe에서 식별한 [People](people.md) 수를 보여줍니다.

## 이 지표의 계산 방법

각 [People](people.md)(식별되거나 식별되지 않음)을 고려할 때, 히트에 `mid` 쿼리 문자열([`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=ko-KR) 쿠키 기반)이 포함되어 있으면 이 지표가 증가합니다.

계산된 지표 `[People with ECID] ÷ [People]`를 만들어 ID 서비스를 사용하여 사이트 방문자의 비율을 구할 수 있습니다.

Experience Cloud ID의 중요성과 설정 디버깅에 대한 자세한 내용은 CDA 이외 지표 [Experience Cloud ID가 있는 방문자](visitors-with-ecid.md)를 참조하십시오.
