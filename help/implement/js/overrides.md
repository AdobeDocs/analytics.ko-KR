---
title: 변수 무시
description: 변수 무시는 하나의 추적 또는 추적 링크 호출에 대한 변수 값을 변경할 수 있도록 해줍니다.
translation-type: tm+mt
source-git-commit: 1f0fd2dcb0454ad9bc2e0c2141b5e17470c6a5de

---


# 변수 무시

변수 무시를 사용하면 페이지의 기존 변수에 영향을 주지 않고 단일 히트에 대한 Analytics 값을 변경할 수 있습니다.

## 워크플로우

1. 새 JavaScript 개체를 만듭니다. 개체 이름은 원하는 대로 지정할 수 있습니다.

   ```js
   var y = new Object();
   ```

2. 이 개체에 유효한 Analytics 속성을 지정하십시오.

   ```js
   y.eVar1 = "New value";
   y.events = "event2";
   ```

3. 개체를 적절한 추적 호출 내에서 인수로 사용합니다.

   ```js
   // Use the override object in a standard page view call
   s.t(y);
   
   // Use the override object in a link tracking call
   s.tl(this,'o','Example override link',y);
   ```

추적 호출이 overrides 매개 변수에서 개체를 받으면 무시 개체의 모든 유효한 값이 표준 Analytics 개체의 값을 덮어씁니다. 기존 Analytics 개체에 이미 정의된 변수는 영향을 받지 않습니다.
