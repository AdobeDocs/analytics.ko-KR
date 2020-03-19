---
title: JavaScript용 AppMeasurement
description: 태그 관리 시스템 없이 JavaScript를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# JavaScript용 AppMeasurement

JavaScript용 AppMeasurement는 지금까지 Adobe Analytics를 구현하는 일반적인 방법이었습니다. 그러나 태그 관리 시스템의 인기가 높아짐에 따라 Adobe Experience [Platform Launch를 사용하는 것이](../launch/overview.md) 좋습니다.

## JavaScript를 사용하여 데이터를 Adobe로 전송하는 전반적인 워크플로우

1. 파일을 `AppMeasurement.js` 로드합니다. 이 파일에는 데이터를 Adobe로 전송하는 데 필요한 라이브러리가 포함되어 있습니다.

   ```html
   <script src="AppMeasurement.js"></script>
   ```

2. 구성 변수를 정의할 수 `AppMeasurement.js`있습니다. Analytics 개체가 인스턴스화될 때 이러한 변수는 데이터 수집 설정이 올바른지 확인합니다. 정의할 [수 있는 변수의 전체 목록은 구성 변수를](../vars/config-vars/configuration-variables.md) 참조하십시오.

   ```js
   // Instantiate the Analytics tracking object with report suite ID
   var s_account = "examplersid";
   var s=s_gi(s_account);
   // Make sure data is sent to the correct location
   s.trackingServer = "example.omtrdc.net";
   ```

3. 사이트의 페이지 코드 내에서 페이지 수준 변수를 정의합니다. 이러한 변수는 Adobe로 전송된 특정 차원과 지표를 결정합니다. 정의할 [수 있는 변수의 전체 목록은 페이지 변수를](../vars/page-vars/page-variables.md) 참조하십시오.

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. 모든 페이지 수준 변수가 정의되면 `t()` 메서드를 사용하여 데이터를 Adobe로 보냅니다. 자세한 [내용은](../vars/functions/t-method.md) 을 참조하십시오.

   ```js
   s.t();
   ```
