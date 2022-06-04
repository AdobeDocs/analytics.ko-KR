---
title: JavaScript용 AppMeasurement를 사용하여 Adobe Analytics 구현
description: 태그 관리 시스템 없이 JavaScript를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
feature: Implementation Basics
exl-id: 25b9d768-c641-4f6c-a4ae-0d6c238c4776
source-git-commit: 99fc7814eaa12d0d9e8e478629a4c2134a577aaa
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# JavaScript용 AppMeasurement를 사용하여 Adobe Analytics 구현

AppMeasurement for JavaScript는 지금까지 Adobe Analytics를 구현하는 일반적인 방법이었습니다. 그러나 태그 관리 시스템의 인기가 높아짐에 따라 [Adobe Experience Platform의 태그](../launch/overview.md)를 사용하는 것이 권장됩니다.

## JavaScript를 사용하여 데이터를 Adobe에 보내는 전반적인 워크플로

1. `AppMeasurement.js` 파일을 로드합니다. 이 파일에는 데이터를 Adobe에 보내는 데 필요한 라이브러리가 포함되어 있습니다.

   ```html
   <script src="AppMeasurement.js"></script>
   ```

2. `AppMeasurement.js` 내에서 구성 변수를 정의하십시오. Analytics 개체가 인스턴스화될 때 이 변수가 데이터 수집 설정이 올바른지 확인합니다. 정의할 수 있는 변수의 전체 목록이 필요하면 [구성 변수](../vars/config-vars/configuration-variables.md)를 참조하십시오.

   ```js
   // Instantiate the Analytics tracking object with report suite ID
   var s_account = "examplersid";
   var s=s_gi(s_account);
   // Make sure data is sent to the correct location
   s.trackingServer = "example.data.adobedc.net";
   ```

3. 사이트의 페이지 코드 내에서 페이지 수준 변수를 정의하십시오. 이 변수가 Adobe에 전송되는 특정 차원과 지표를 결정합니다. 정의할 수 있는 변수의 전체 목록이 필요하면 [페이지 변수](../vars/page-vars/page-variables.md)를 참조하십시오.

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. 모든 페이지 수준 변수가 정의되면 `t()` 메서드를 사용하여 데이터를 Adobe에 보내십시오. 자세한 내용은 [t](../vars/functions/t-method.md)를 참조하십시오.

   ```js
   s.t();
   ```
