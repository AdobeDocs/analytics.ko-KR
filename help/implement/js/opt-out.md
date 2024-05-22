---
title: 옵트아웃 링크
description: 사이트 방문자를 위한 구현 옵트아웃 링크를 만드는 방법을 알아봅니다.
feature: Implementation Basics
exl-id: 08b8c7cc-28c6-45e3-ab44-77471eea8ef1
hide: true
hidefromtoc: true
role: Developer
source-git-commit: 48f1974a0c379a4e619d9a04ae80e43cce9527c1
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 67%

---

# 구현 옵트아웃 링크

>[!IMPORTANT]
>
> 이 문서에서는 다음을 제공합니다 **Adobe Analytics을 구현할 (계획 중인) Adobe Analytics 고객** 웹 사이트에서 웹 사이트 사용자에게 옵트아웃 링크를 제공하는 방법에 대한 지침을 제공합니다. <p><p>
> 다음과 같은 경우 **Adobe Analytics을 구현한 웹 사이트 방문**, 옵트아웃하려는 경우 **<span style="color:red">이 문서는 귀하를 위한 것이 아닙니다.</span>**. 다음을 참조하십시오. [Adobe 개인 정보 보호 선택 사항](https://www.adobe.com/kr/privacy/opt-out.html) Adobe이 정보를 사용하는 방법을 제어합니다.

웹 사이트의 일부 방문자는 데이터 세트에 자신의 검색 정보가 포함되지 않기를 바랍니다. Adobe은 웹 사이트 방문자에게 분석 대상 정보를 옵트아웃할 수 있는 수단을 제공하는 기능을 제공합니다.

옵트아웃 링크는 웹 사이트 방문자가 Analytics 보고에서 데이터를 생략하도록 허용하는 방법입니다. 이러한 링크는 AppMeasurement 구현으로 제한됩니다. Adobe은 [Adobe Experience Cloud 옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=ko-KR) 대신, 옵트인 서비스는 보다 강력하며 Adobe Analytics 및 AppMeasurement을 포함한 여러 Adobe Experience Cloud 제품에서 작동합니다.

방문자가 옵트아웃 URL에 도달하면 옵트아웃 쿠키를 설치하라는 메시지가 표시됩니다. 사용자가 추적되지 않도록 선택하고 옵트아웃 쿠키가 설정된 경우 AppMeasurement은 Adobe에게 데이터를 계속 전송합니다. 하지만 이 데이터는 처리되거나 보고서에 포함되지 않습니다.

>[!TIP]
>
>또한 Adobe에서는 보고서 세트별로 개인정보 설정을 제공합니다. 관리자 안내서의 [개인정보 설정](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md)을 참조하십시오.

## 옵트아웃 URL

조직에 대한 옵트아웃 페이지는 구현의 [`trackingServer`](../vars/config-vars/trackingserver.md) 변수 값에 따라 다릅니다.

* Analytics 확장에서:
   1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
   1. 원하는 태그 속성을 클릭합니다.
   1. [!UICONTROL 확장] 탭을 클릭한 다음 Adobe Analytics 아래의 [!UICONTROL 구성]을 클릭합니다.
   1. [!UICONTROL 일반] 아코디언을 클릭하고 [!UICONTROL 추적 서버] 값을 확인합니다.

* JavaScript 구현에서:
   1. 웹 서버에서, 사이트에서 사용되는 AppMeasurement.js 파일을 코드 또는 텍스트 편집기에서 엽니다.
   1. `trackingServer` 변수 값을 확인합니다.

* [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/experience-platform/debugger/home.html) 사용:
   1. Chrome 브라우저를 사용하여 사이트로 이동합니다.
   1. Experience Cloud Debugger를 열고 [!UICONTROL 네트워크 탭]으로 이동합니다.
   1. [!UICONTROL 요청 URL - 호스트 이름] 값을 확인합니다.

구현의 `trackingServer` 도메인을 찾으면 경로 `/optout.html`을 끝에 추가합니다. 예:

* 서드파티 쿠키: `https://example.data.adobedc.net/optout.html`
* 자사 쿠키: `https://stats.example.com/optout.html`

## 옵트아웃 쿼리 문자열 매개 변수

쿼리 문자열을 사용하여 이 페이지에 자동으로 로드할 수 있는 설정이 있습니다.

### 로케일

`locale` 쿼리 문자열 매개 변수를 포함하여 옵트아웃 페이지의 언어를 자동으로 전환하십시오. 이 쿼리 문자열 매개 변수는 다음 값 중 하나를 지정합니다.

* `en_US` (영어, 기본값)
* `bg_BG` (불가리아어)
* `zh_CN` (중국어 간체)
* `zh_TW` (중국어 번체)
* `cs_CZ` (체코어)
* `da_NK` (덴마크어)
* `nl_NL` (네덜란드어)
* `et_EE` (에스토니아어)
* `fi_FI` (핀란드어)
* `fr_FR` (프랑스어)
* `de_DE` (독일어)
* `el_GR` (그리스어)
* `it_IT` (이탈리아어)
* `jp_JP` (일본어)
* `ko_KR` (한국어)
* `lv_LV` (라트비아어)
* `lt_LT` (리투아니아어)
* `nb_NO` (노르웨이어)
* `pl_PL` (폴란드어)
* `pt_BR` (포르투갈어)
* `sk_SK` (슬로바키아어)
* `es_ES` (스페인어)

예를 들어 `https://example.data.adobedc.net/optout.html?locale=ko_KR`은 옵트아웃 페이지를 한국어로 로드합니다.

### 팝업

페이지에 &#39;창 닫기&#39; 버튼을 추가하여 옵트아웃 페이지를 팝업 창으로 만들 수 있습니다. `popup` 쿼리 문자열 매개 변수를 사용하고 값을 `1`로 지정하십시오.

예를 들어 `https://example.data.adobedc.net/optout.html?popup=1`은 &#39;창 닫기&#39; 버튼이 있는 옵트아웃 페이지를 로드합니다.

>[!NOTE]
>
>이전에는 이 쿼리 문자열 매개 변수를 사용하여 팝업 창을 만들었습니다. 그러나 대부분의 최신 브라우저는 최종 사용자가 팝업을 제어할 수 있도록 합니다.

### 옵트아웃 한 번 클릭

이렇게 하면 사용자가 즉시 추적을 그만둘 수 있습니다(옵트아웃). 두 쿼리 문자열 매개 변수 `opt_out` 및 `confirm_change`를 추가하고 각각 값을 `1`로 지정합니다.

예를 들어 `https://example.data.adobedc.net/optout.html?opt_out=1&confirm_change=1`은 방문자의 페이지에 옵트아웃 쿠키를 즉시 설치합니다.

### 옵트인 한 번 클릭

이렇게 하면 사용자가 옵트아웃 쿠키를 삭제하여 즉시 추적을 다시 수행할 수 있습니다(옵트인). 두 쿼리 문자열 매개 변수 `opt_in` 및 `confirm_change`를 추가하고 각각 값을 `1`로 지정합니다.

예를 들어 `https://example.data.adobedc.net/optout.html?opt_in=1&confirm_change=1`은 방문자에 대한 옵트아웃 쿠키를 즉시 삭제합니다.
