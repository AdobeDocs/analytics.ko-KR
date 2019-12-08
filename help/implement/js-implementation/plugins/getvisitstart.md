---
description: 새 방문이 시작되고 있는지 확인합니다.
keywords: Analytics Implementation
title: getVisitStart
topic: Developer and implementation
uuid: 7dd3e51f-2f73-4452-a9fb-cac513cd28eb
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getVisitStart

새 방문이 시작되고 있는지 확인합니다.

**구성 변수**

없음

**매개 변수**

c = (문자열) 추적할 쿠키 이름

**반환**

(정수) 방문의 첫 번째 페이지에 있으면 1, 다른 경우에는 0.

**샘플 호출**

```
s.eVar50 = s.getVisitStart("s_visit");
```

