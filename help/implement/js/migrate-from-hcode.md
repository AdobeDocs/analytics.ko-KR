---
title: JavaScript용 AppMeasurement로의 마이그레이션
description: H 코드의 구현을 마이그레이션하는 데 필요한 사항을 결정합니다.
translation-type: tm+mt
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb

---


# JavaScript용 AppMeasurement로의 마이그레이션

구현에서 여전히 H 코드를 사용하는 경우 최신 버전의 AppMeasurement로 마이그레이션하는 것이 좋습니다. [Adobe Experience Platform Launch](../launch/overview.md)를 통해 Analytics를 구현하는 것이 좋지만 업데이트된 JavaScript 구현을 사용할 수 있습니다.

H 코드와 비교할 때 AppMeasurement에 다음의 주목할 만한 변경 사항이 있습니다.

* H 코드보다 3~7배 더 빠릅니다.
* H 코드보다 가벼움 - 21kb 비압축과 H 코드(33kb 비압축) 비교
* 라이브러리와 페이지 코드는 `<head>` 태그 내에 배포할 수 있습니다.
* 기존 페이지 수준 H 코드는 AppMeasurement와 호환됩니다.
* 라이브러리에서는 쿼리 매개 변수를 가져오고, 쿠키를 읽고 쓰고, 고급 링크 추적을 수행하는 기본 유틸리티를 제공합니다.
* 라이브러리가 동적 계정 구성 변수(`dynamicAccountSelection`, `dynamicAccountMatch` 및 `dynamicAccountList` 포함)를 지원하지 않습니다.
* 설문 조사 모듈은 지원되지 않습니다.

다음 절차는 일반적인 마이그레이션 워크플로우에 대한 개요입니다.

1. **새 AppMeasurement 파일 다운로드**: Adobe Analytics에 로그인한 다음, 관리 > 코드 관리자로 이동하여 새 파일에 액세스합니다. 다운로드한 압축 파일에는 미디어 및 통합 모듈과 함께 축소된 `AppMeasurement.js` 파일이 포함되어 있습니다.
1. **`s_code.js`사용자 지정 사항을`AppMeasurement.js`**에 복사:`s_code.js`의`DO NOT ALTER ANYTHING BELOW THIS LINE`섹션 앞에 있는 모든 코드를`AppMeasurement.js`의 시작 부분으로 이동합니다.
1. **모든 플러그인 업데이트**: `s_code.js` 파일에 나열된 각 플러그인의 최신 버전을 사용하고 있는지 확인하십시오. 여기에는 미디어 및 통합 모듈이 포함됩니다.
1. **AppMeasurement.js 파일 배포**: 웹 서버에 `AppMeasurement.js` 파일을 업로드합니다.
1. **스크립트 참조를 업데이트하여`AppMeasurement.js`**가리키기: 모든 페이지가`s_code.js`대신`AppMeasurement.js`를 참조하는지 확인합니다.

## Appmeasurement 코드 예

일반적인 `AppMeasurement.js` 파일. 구성 변수가 `doPlugins` 함수 위에 설정되어 있는지 확인하십시오.

```js
// Initialize AppMeasurement
var s = s_gi("examplersid");

/******** VISITOR ID SERVICE CONFIG - REQUIRES VisitorAPI.js ********/;
s.visitor=Visitor.getInstance("INSERT-MCORG-ID-HERE");

/************************** CONFIG SECTION **************************/;
/* You may add or alter any code config here. */
s.trackDownloadLinks = true;
s.trackExternalLinks = true;
s.trackInlineStats = true;
s.linkDownloadFileTypes = "exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx";
s.linkInternalFilters = "javascript:,example.com";

s.usePlugins = true;
function s_doPlugins(s) {

// Use implementation plug-ins that are defined below in this section

}
s.doPlugins = s_doPlugins;

/* WARNING: Changing any of the below variables will cause drastic
changes to how your visitor data is collected.  Changes should only be
made when instructed to do so by your account manager.*/
s.trackingServer="example.sc.omtrdc.net";

/************************** PLUGINS SECTION *************************/

// Copy and paste implementation plug-ins here. Plug-ins can then be used in the s_doPlugins(s) function above

/****************************** MODULES *****************************/

// Copy and paste implementation modules (Media, Integrate) here.

/* ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! ===============  */
```

## 예제 페이지 코드

각 페이지에 로드되는 일반적인 코드.

```html
<script src="AppMeasurement.js"></script>
<script language="JavaScript" type="text/javascript">
s.pageName = "Example page name";
s.eVar1 = "Example eVar value";
s.events = "event1";
s.t();
</script>
```

각 페이지의 `AppMeasurement.js` 및 `VisitorAPI.js`에도 참조를 포함해야 합니다. 자세한 내용은 [JavaScript 구현](/help/implement/js/overview.md)을 참조하십시오.
