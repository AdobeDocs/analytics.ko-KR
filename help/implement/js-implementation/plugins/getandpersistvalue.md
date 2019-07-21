---
description: getAndPersistValue 플러그인은 선택한 값을 가져와 결정된 기간 동안 Analytics 변수에 채웁니다. 가장 일반적인 용도는 클릭스루 후에 캠페인이 페이지 보기를 몇 개나 생성하는지 확인하여 각 캠페인에 가장 공통되는 페이지를 쉽게 확인할 수 있도록 하는 것입니다.
keywords: Analytics 구현
seo-description: getAndPersistValue 플러그인은 선택한 값을 가져와 결정된 기간 동안 Analytics 변수에 채웁니다. 가장 일반적인 용도는 클릭스루 후에 캠페인이 페이지 보기를 몇 개나 생성하는지 확인하여 각 캠페인에 가장 공통되는 페이지를 쉽게 확인할 수 있도록 하는 것입니다.
seo-title: getAndPersistValue
solution: Analytics
subtopic: 플러그인
title: getAndPersistValue
topic: 개발자 및 구현
uuid: ddeab 80 c -260 e -44 b 6-8483-8 b 8 b 369 ec 19 b
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getAndPersistValue

getAndPersistValue 플러그인은 선택한 값을 가져와 결정된 기간 동안 Analytics 변수에 채웁니다. 가장 일반적인 용도는 클릭스루 후에 캠페인이 페이지 보기를 몇 개나 생성하는지 확인하여 각 캠페인에 가장 공통되는 페이지를 쉽게 확인할 수 있도록 하는 것입니다.

>[!IMPORTANT]
>
>This plug-in has not been validated to be compatible with [AppMeasurement for JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8). [Appmeasurement 플러그인 지원을 참조하십시오](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A).

For example, you might use this plug-in to set a campaign tracking code from the *`campaign`* variable into a Custom Traffic ( *`s.prop`*) variable on each visitor's page view made for the next 30 days. 이 예를 활용하여 원래 클릭스루의 결과로 생성되는 추적 코드의 페이지 보기 수를 결정할 수 있습니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 및 구현 {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: 이 섹션은 변경할 필요가 없습니다.

**플러그인 구성**

다음 코드를 *`s_doPlugins()`* 함수는 Plugin Config 라는 *`s_code.js`* 레이블의 영역에 *있습니다*. 지속되는 값 데이터를 캡처하는 데 사용할 사용자 지정 트래픽(s.prop) 변수 또는 사용자 지정 전환(s.eVar) 변수 하나를 선택합니다. 관리 콘솔을 사용하여 활성화했지만 현재 다른 목적으로 사용하고 있지는 않은 변수여야 합니다. 다음 예를 사용하여 요구 사항에 맞게 업데이트할 수 있습니다.

`s.prop1=s.getAndPersistValue(s.campaign,'s_getval',30);`

*`s.getAndPersistValue`*&#x200B;에는 세 개의 인수가 있습니다.

1. Currently populated variable or value to persist ( *`s.campaign`* shown above).
1. Cookie name, used to store the value ( *`s_getval`* shown above).
1. 일 단위의 지속 기간. 위에 표시된 "30"은 다음 30일 동안 사용자가 생성하는 모든 페이지 보기에서 선택한 변수에 값을 채우게 만듭니다. 이 값을 생략하면 설정 기본값은 *session*&#x200B;이 됩니다.

**PLUGINS SECTION**: [!DNL s_code.js] 파일에서 PLUGINS SECTION이라는 레이블이 지정된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

```js
/* 
 * Plugin: getAndPersistValue 0.3 - get a value on every page 
 */ 
s.getAndPersistValue=new Function("v","c","e","" 
+"var s=this,a=new Date;e=e?e:0;a.setTime(a.getTime()+e*86400000);if(" 
+"v)s.c_w(c,v,e?a:0);return s.c_r(c);");
```

프로덕션 환경에 플러그인을 배포하기 전에 항상 플러그인 설치를 종합적으로 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
