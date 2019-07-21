---
description: 사용자 지정 방법을 구현하여 s.visitorID 변수를 설정함으로써 방문자를 식별할 수 있습니다.
keywords: Analytics 구현
seo-description: 사용자 지정 방법을 구현하여 s.visitorID 변수를 설정함으로써 방문자를 식별할 수 있습니다.
seo-title: 사용자 지정 방문자 ID
solution: Analytics
title: 사용자 지정 방문자 ID
topic: 개발자 및 구현
uuid: 49881 E 27-0418-4 ECF-A 092-DCC 3 DB 923 F 40
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 사용자 지정 방문자 ID

사용자 지정 방법을 구현하여 s.visitorID 변수를 설정함으로써 방문자를 식별할 수 있습니다.

방문자를 식별하는 고유한 방법이 있으면 사이트에서 사용자 지정 방문자 ID를 사용할 수 있습니다. 사용자가 사용자 이름과 암호를 사용하여 웹 사이트에 로그인할 때 생성되는 ID가 그 예입니다.

사용자의 [!UICONTROL 방문자 ID]를 추출하고 관리할 수 있을 경우, 다음 방법을 사용하여 ID를 설정할 수 있습니다.

| 메서드 | 설명 |
|---|---|
| [s.visitorID](/help/implement/js-implementation/c-variables/page-variables.md) 변수 | 브라우저에서 JavaScript를 사용하거나, 다른 AppMeasurement 라이브러리를 사용 중일 경우, 데이터 수집 변수에 방문자 ID를 설정할 수 있습니다. |
| 이미지 요청 시 쿼리 문자열 매개 변수 | 이 기능을 통해 [!UICONTROL 방문자 ID]를 하드 코딩된 이미지 요청에서 [!UICONTROL vid 쿼리 문자열] 매개 변수를 통해 Adobe로 전달할 수 있습니다. |
| 데이터 삽입 API | On devices using wireless protocols that don't accept JavaScript, you can send an XML post containing the `<visitorid/>` XML element to Adobe collection servers from your servers. |
| URL 다시 쓰기 및 VISTA | 일부 배포 아키텍처에서는 쿠키를 설정할 수 없는 경우 세션 상태를 유지할 수 있도록 URL 다시 쓰기를 지원합니다. 이와 같은 경우, Adobe 엔지니어링 서비스에서는 페이지의 URL에서 세션 값을 찾는 [!DNL VISTA] 규칙을 구현한 다음 형식을 지정하여 [!UICONTROL visid] 값에 삽입할 수 있습니다. |
>[!CAUTION]
>**사용자 지정 방문자 ID는 충분히 세부적이거나 고유해야 합니다. 사용자 지정 방문자 ID의 잘못된 구현은 잘못된 데이터와 낮은 보고 성능을 초래할 수 있습니다.** 사용자 지정 방문자 ID가 고유하거나 세부적이거나, 문자열 «null» 또는 «0» 와 같은 일반적인 기본값으로 잘못 설정된 경우, 여러 다른 방문자의 히트가 Adobe Analytics에서 단일 방문자로 표시됩니다. 이 경우 방문자 카운트가 너무 낮고 세그먼트가 해당 방문자에 대해 제대로 작동하지 않는 데이터가 잘못된 데이터로 표시됩니다. 또한 불충분한 사용자 지정 방문자 ID는 데이터가 Analytics 보고 클러스터의 노드 간에 적절하게 스프레드되지 않도록 합니다. 이 경우 한 노드가 과부하가 걸리며 적시에 보고서 요청을 처리할 수 없습니다. 결국 보고서 세트에 대한 모든 보고는 실패합니다. <br>Analytics가 종종 몇 달의 균형이 맞지 않는 데이터를 처리할 수 있기 때문에 잘못 구현된 사용자 지정 방문자 ID는 보고에 즉시 영향을 주지 않을 수 있습니다. 하지만 시간이 지나도 잘못 구현된 사용자 지정 방문자 ID 값이 Analytics가 영향을 받는 보고서 세트에 대한 처리를 비활성화하도록 요구하는 문제가 발생할 수 있습니다.</br><br>구현자는 단일 사용자 지정 방문자 ID 값이 보고서 세트의 트래픽의 1% 이상에 대해 신뢰되지 않도록 지침을 따라야 합니다. Although the 1% guideline is sufficient for most report suites, the actual limit that might cause reporting performance to be impacted may be lower than 1% for very large report suites.</br>
