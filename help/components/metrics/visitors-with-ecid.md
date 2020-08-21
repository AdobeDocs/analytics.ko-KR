---
title: Experience Cloud ID를 가진 방문자
description: Adobe Experience Cloud ID 서비스를 사용하는 고유 방문자의 수입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 95%

---


# Experience Cloud ID를 가진 방문자

Experience Cloud ID를 가진 방문자 지표는 [Experience Cloud ID 서비스](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 사용하여 Adobe가 식별한 고유 방문자 수를 보여줍니다. 이 차원은 사이트 방문자의 대다수가 이 ID 서비스를 사용하도록 하기 위해 [고유 방문자 수](unique-visitors.md) 지표와 비교하는 데 유용합니다. 방문자의 상당수가 이 ID 서비스 쿠키를 사용하지 않다면 구현 내의 문제를 나타낼 수 있습니다.

>[!NOTE]
>
>이 지표는 Adobe Target 또는 Adobe Audience Manager과 같은 여러 Experience Cloud 서비스를 사용하는 경우 디버깅에 특히 중요합니다. Experience Cloud 제품 간에 공유된 세그먼트에는 Experience Cloud ID가 없는 방문자가 포함되지 않습니다.

## 이 지표의 계산 방법

이 지표는 [고유 방문자 수](unique-visitors.md) 지표를 기반으로 합니다. 단, [`s_ecid`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키 기반 `mid` 쿼리 문자열을 사용하여 식별된 개인만 포함합니다.

## Experience Cloud ID 설정 디버깅

Experience Cloud ID를 가진 방문자 지표는 Experience Cloud 통합 문제 해결이나 ID 서비스가 배포되지 않은 사이트 영역 식별에 유용합니다.

Experience Cloud ID를 가진 방문자를 고유 방문자 수와 나란하도록 드래그하여 비교할 수 있습니다.

![고유 방문자 비교](assets/metric-mcvid1.png)

이 예에서 각 페이지의 &#39;고유 방문자 수&#39;는 &#39;Experience Cloud ID를 가진 방문자&#39; 수와 동일하지만 고유 방문자의 총 수는 Experience Cloud ID를 가진 방문자의 총 수보다 큽니다. ID 서비스를 설정하지 않는 페이지를 찾기 위해 [계산된 지표](../c-calcmetrics/cm-overview.md)를 만들 수 있습니다. 다음 정의를 사용할 수 있습니다.

![계산된 지표 정의](assets/metric-mcvid2.png)

보고서에 계산된 지표를 추가하면 MCID가 없는 방문자 수가 가장 많은 페이지를 표시하도록 페이지 보고서를 정렬할 수 있습니다.

![ID 서비스가 없는 페이지](assets/metric-mcvid3.png)

&quot;제품 빠른 보기&quot; 차원 항목이 ID 서비스와 함께 제대로 구현되지 않습니다. 조직 내의 적절한 팀과 함께 이러한 페이지를 가능한 한 빨리 업데이트할 수 있습니다. [브라우저 유형](../dimensions/browser-type.md), [사이트 섹션](../dimensions/site-section.md) 또는 [eVar](../dimensions/evar.md)와 같은 차원 유형으로 유사한 보고서를 만들 수 있습니다.
