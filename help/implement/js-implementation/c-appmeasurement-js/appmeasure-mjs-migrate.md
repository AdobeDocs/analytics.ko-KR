---
description: 다음 표에는 구현을 마이그레이션하기 위해 수행해야 하는 작업 목록이 나와 있습니다.
keywords: Analytics 구현; Appmeasurement; 마이그레이션; 마이그레이션; Javascript
seo-description: 다음 표에는 구현을 마이그레이션하기 위해 수행해야 하는 작업 목록이 나와 있습니다.
seo-title: JavaScript용 AppMeasurement로의 마이그레이션
solution: Analytics
subtopic: JavaScript AppMeasurement
title: JavaScript용 AppMeasurement로의 마이그레이션
topic: 개발자 및 구현
uuid: 5 BE 345 A 8-5 A 95-4176-A 2 E 6-97139 B 9 B 46 CE
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# JavaScript용 AppMeasurement로의 마이그레이션

다음 표에는 구현을 마이그레이션하기 위해 수행해야 하는 작업 목록이 나와 있습니다.

>[!NOTE]
>
>We recommend migrating to the [Identity Service](../../../implement/js-implementation/c-unique-visitors/visid-service.md#concept_230F8759826E47789EA8DEE08FA09B07) when you migrate to [!DNL AppMeasurement] for JavaScript.

![](assets/step1_icon.png) 플러그인 호환성 확인

위치: s\_ code. js

일부 플러그인은 더 이상 지원되지 않습니다. [Appmeasurement 플러그인 지원을](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A) 참조하십시오.

![](assets/step2_icon.png) 새 AppMeasurement 다운로드

위치: 관리 &gt; 코드 관리자

다운로드 zip에는 축소된 AppMeasurement.js 파일과, 미디어 및 통합 모듈용 Javascript 파일이 들어 있습니다.

![](assets/step3_icon.png) s\_ code. js 사용자 지정을에 복사합니다 `AppMeasurement.js`.

위치: s\_ code. js 및 appmeasurement. js

Move all code that appears before the `DO NOT ALTER ANYTHING BELOW THIS LINE` section in s\_code.js to the beginning of AppMeasurement.js.

![](assets/step4_icon.png) (선택 사항) 플러그인 업데이트

위치: Appmeasurement. js

If you are using the getQueryParam plug-in, update these calls to use the new utility, [Util.getQueryParam](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5).

![](assets/step5_icon.png) (선택 사항) 미디어 및 통합 모듈 업데이트

위치: Appmeasurement. js

If you are using either of these modules, copy and paste the code from AppMeasurement\_Module\_Media.js and/or AppMeasurement\_Module\_Integrate.js and paste it just before the `DO NOT ALTER ANYTHING BELOW THIS LINE` in AppMeasurement.js.

![](assets/step6_icon.png) 새 JavaScript 배포

위치: 웹 사이트

새로운 JavaScript 파일은 표준 프로세스에 따라 배포할 수 있습니다. 기존 페이지 코드는 이 버전과 호환됩니다.