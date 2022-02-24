---
title: Experience Cloud ID를 가진 사용자
description: Experience Cloud ID를 가진 크로스 디바이스 분석 사용자의 수.
feature: Metrics
exl-id: 072e7d2b-3a08-49c6-a892-4cea2cc10159
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: ht
source-wordcount: '130'
ht-degree: 100%

---

# Experience Cloud ID를 가진 사용자

‘Experience Cloud ID를 가진 사용자’는 [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko-KR)를 사용하여 Adobe가 확인한 [사용자](people.md) 수를 보여 주는 [크로스 디바이스 분석](../cda/overview.md) 지표입니다.

## 이 지표의 계산 방법

히트에 `mid` 쿼리 문자열이 포함된 경우 각 [사용자](people.md)(확인되거나 미확인된)를 고려하여 해당 지표는 증가합니다([`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=ko-KR) 쿠키에 따라).

ID 서비스를 사용하여 계산된 지표 `[People with ECID] ÷ [People]`을 만들어 사이트 방문자의 백분율을 구할 수 있습니다.

Experience Cloud ID 및 설정 디버깅의 중요성에 대한 자세한 내용은 이와 동등한 CDA가 아닌 지표인 [Experience Cloud ID를 가진 방문자](visitors-with-ecid.md)를 참조하십시오.
