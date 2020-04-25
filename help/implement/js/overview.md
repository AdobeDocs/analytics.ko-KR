---
title: JavaScript용 AppMeasurement
description: 태그 관리 시스템 없이 JavaScript를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# JavaScript용 AppMeasurement

AppMeasurement for JavaScript는 지금까지 Adobe Analytics를 구현하는 일반적인 방법이었습니다. 그러나 Tag Management 시스템의 인기가 높아짐에 따라 [Adobe Experience Platform Launch](../launch/overview.md) 사용이 권장됩니다.

## JavaScript를 사용하여 데이터를 Adobe에 보내는 전반적인 워크플로우

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
   s.trackingServer = "example.omtrdc.net";
   ```

3. 사이트의 페이지 코드 내에서 페이지 수준 변수를 정의하십시오. 이 변수가 Adobe에 전송되는 특정 차원과 지표를 결정합니다. 정의할 수 있는 변수의 전체 목록이 필요하면 [페이지 변수](../vars/page-vars/page-variables.md)를 참조하십시오.

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. When all page-level variables are defined, send the data to Adobe using the `t()` method. 자세한 내용은 [t](../vars/functions/t-method.md)를 참조하십시오.

   ```js
   s.t();
   ```
