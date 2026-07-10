---
title: Experience Cloud ID를 보유한 사용자
description: Experience Cloud ID를 가진 크로스 디바이스 분석 사용자의 수.
feature: Metrics
exl-id: 072e7d2b-3a08-49c6-a892-4cea2cc10159
TQID: https://experienceleague.adobe.com/w85poHKHnDYQ0iTItr2r26q1aRpN50AsdYzg6v82Jpk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 58%

---

# Experience Cloud ID를 보유한 사용자

&#39;Experience Cloud ID를 가진 사용자&#39;는 [방문자 ID 서비스](https://experienceleague.adobe.com/kr/docs/id-service/using/home) 또는 [Experience Platform ID 서비스](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/home)를 사용하여 Adobe에서 식별한 [사용자](people.md)의 수를 표시하는 [크로스 디바이스 분석](../cda/overview.md) 지표입니다.

## 이 지표의 계산 방법

각 [사용자](people.md)(확인되거나 미확인된)을 고려하여, 히트에 `mid` 쿼리 문자열이 포함된 경우 이 [지표](overview.md)이(가) 증가합니다([`s_ecid`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) 쿠키 기반).

ID 서비스를 사용하여 계산된 지표 `[People with ECID] ÷ [People]`을 만들어 사이트 방문자의 백분율을 구할 수 있습니다.

Experience Cloud ID 및 설정 디버깅의 중요성에 대한 자세한 내용은 이와 동등한 CDA가 아닌 지표인 [Experience Cloud ID를 가진 방문자](visitors-with-ecid.md)를 참조하십시오.
