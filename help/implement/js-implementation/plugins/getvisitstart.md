---
description: 새 방문이 시작되고 있는지 확인합니다.
keywords: Analytics 구현
seo-description: 새 방문이 시작되고 있는지 확인합니다.
seo-title: getVisitStart
solution: Analytics
title: getVisitStart
topic: 개발자 및 구현
uuid: 7 DD 3 E 51 F -2 F 73-4452-A 9 FB-CAC 513 CD 28 EB
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

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

