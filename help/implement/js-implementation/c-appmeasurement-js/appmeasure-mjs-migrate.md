---
description: 다음 표에는 구현을 마이그레이션하기 위해 수행해야 하는 작업 목록이 나와 있습니다.
keywords: Analytics 구현;appmeasurement;마이그레이션;마이그레이션;javascript
seo-description: 다음 표에는 구현을 마이그레이션하기 위해 수행해야 하는 작업 목록이 나와 있습니다.
seo-title: JavaScript용 AppMeasurement로의 마이그레이션
solution: Analytics
subtopic: JavaScript AppMeasurement
title: JavaScript용 AppMeasurement로의 마이그레이션
topic: 개발자 및 구현
uuid: 5be345a8-5a95-4176-a2e6-97139b9b46ce
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# JavaScript용 AppMeasurement로의 마이그레이션

다음 표에는 구현을 마이그레이션하기 위해 수행해야 하는 작업 목록이 나와 있습니다.

> [!NOTE] JavaScript용 [으로 마이그레이션할 때 ](../../../implement/js-implementation/c-unique-visitors/visid-service.md#concept_230F8759826E47789EA8DEE08FA09B07)ID 서비스[!DNL AppMeasurement]로 마이그레이션하는 것이 좋습니다.

![](assets/step1_icon.png) 플러그인 호환성 확인

위치: s\_code.js

일부 플러그인은 더 이상 지원되지 않습니다. [AppMeasurement 플러그인 지원](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A)을 참조하십시오.

![](assets/step2_icon.png) 새 AppMeasurement 다운로드

위치: 관리자 &gt; 코드 관리자

다운로드 zip에는 축소된 AppMeasurement.js 파일과, 미디어 및 통합 모듈용 Javascript 파일이 들어 있습니다.

![](assets/step3_icon.png) s\_code.js 사용자 지정을 `AppMeasurement.js`에 복사합니다.

위치: s\_code.js 및 AppMeasurement.js

s\_code.js의 `DO NOT ALTER ANYTHING BELOW THIS LINE` 섹션 앞에 표시되는 모든 코드를 AppMeasurement.js의 시작 부분으로 이동합니다.

![](assets/step4_icon.png) (선택 사항) 플러그인 업데이트

위치: AppMeasurement.js

getQueryParam 플러그인을 사용하는 경우 새 유틸리티인 [Util.getQueryParam](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5)을 사용하도록 이러한 호출을 업데이트합니다.

![](assets/step5_icon.png) (선택 사항) 미디어 및 통합 모듈 업데이트

위치: AppMeasurement.js

이러한 모듈 중 하나를 사용하는 경우 AppMeasurement\_Module\_Media.js 및/또는 AppMeasurement\_Module\_Integrate.js에서 코드를 복사하여 AppMeasurement.js의 `DO NOT ALTER ANYTHING BELOW THIS LINE` 바로 앞에 붙여넣으십시오.

![](assets/step6_icon.png) 새 JavaScript 배포

위치: 사용자의 웹 사이트

새로운 JavaScript 파일은 표준 프로세스에 따라 배포할 수 있습니다. 기존 페이지 코드는 이 버전과 호환됩니다.