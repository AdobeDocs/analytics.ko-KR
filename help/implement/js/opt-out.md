---
title: 옵트아웃 링크
description: 사이트 방문자를 위한 구현 옵트아웃 링크를 만드는 방법을 알아봅니다.
translation-type: ht
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# 구현 옵트아웃 링크

> [!IMPORTANT] 특히 GDPR 관련 조직의 경우 옵트인 서비스를 사용하는 것이 좋습니다. Experience Cloud ID 서비스 사용 안내서의 [옵트인 서비스 개요](https://docs.adobe.com/content/help/ko-KR/id-service/using/implementation/opt-in-service/optin-overview.html)를 참조하십시오.

웹 사이트의 일부 방문자는 데이터 세트에 자신의 검색 정보가 포함되지 않기를 바랍니다. Adobe에서는 웹 사이트 방문자가 정보 수집을 옵트아웃할 수 있는 기능을 제공합니다. 모든 구현 유형이 수용됩니다. 조직은 자체 개인정보 보호정책과 서명한 약관 준수 유지에 대한 책임을 져야 합니다.

방문자가 옵트아웃 URL에 도달하면 옵트아웃 쿠키를 설치하라는 메시지가 표시됩니다. 사용자가 추적되지 않도록 선택하고 옵트아웃 쿠키가 설정된 경우 JavaScript 파일이 계속해서 Adobe 서버에 데이터를 보냅니다. 하지만 이 데이터는 처리되거나 보고서에 포함되지 않습니다.

> [!TIP] 또한 Adobe에서는 보고서 세트별로 개인정보 설정을 제공합니다. 관리자 가이드의 [개인정보 설정](../../admin/admin/privacy-settings.md)을 참조하십시오.

## 옵트아웃 URL

조직에 대한 옵트아웃 페이지는 구현의 [`trackingServer`](../vars/config-vars/trackingserver.md) 변수 값에 따라 다릅니다.

* Adobe Experience Platform Launch에서:
   1. [launch.adobe.com](https://launch.adobe.com)에 로그인하고 원하는 속성을 클릭합니다.
   2. [!UICONTROL 확장] 탭을 클릭한 다음 Adobe Analytics 아래의 [!UICONTROL 구성]을 클릭합니다.
   3. [!UICONTROL 일반] 아코디언을 클릭하고 [!UICONTROL 추적 서버] 값을 확인합니다.

* JavaScript 구현에서:
   1. 웹 서버에서, 사이트에서 사용되는 AppMeasurement.js 파일을 코드 또는 텍스트 편집기에서 엽니다.
   2. `trackingServer` 변수 값을 확인합니다.

* [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/ko-KR/debugger/using/experience-cloud-debugger.html) 사용:
   1. Chrome 브라우저를 사용하여 사이트로 이동합니다.
   2. Experience Cloud Debugger를 열고 [!UICONTROL 네트워크 탭]으로 이동합니다.
   3. [!UICONTROL 요청 URL - 호스트 이름] 값을 확인합니다.

구현의 `trackingServer` 도메인을 찾으면 경로 `/optout.html`을 끝에 추가합니다. 예:

* 타사 쿠키: `https://example.sc.omtrdc.net/optout.html`
* 자사 쿠키: `https://stats.example.com/optout.html`

## 옵트아웃 쿼리 문자열 매개 변수

쿼리 문자열을 사용하여 이 페이지에 자동으로 로드할 수 있는 설정이 있습니다.

### 로케일

`locale` 쿼리 문자열 매개 변수를 포함하여 옵트아웃 페이지의 언어를 자동으로 전환하십시오. 이 쿼리 문자열 매개 변수는 다음 값 중 하나를 지정합니다.

* en_US(영어, 기본값)
* bg_BG(불가리아어)
* zh_CN(중국어 간체)
* zh_TW(중국어 번체)
* cs_CZ(체코어)
* da_NK(덴마크어)
* nl_NL(네덜란드어)
* et_EE(에스토니아어)
* fi_FI(핀란드어)
* fr_FR(프랑스어)
* de_DE(독일어)
* el_GR(그리스어)
* it_IT(이탈리아어)
* jp_JP(일본어)
* ko_KR(한국어)
* lv_LV(라트비아어)
* lt_LT(리투아니아어)
* nb_NO(노르웨이어)
* pl_PL(폴란드어)
* pt_BR(포르투갈어)
* sk_SK(슬로바키아어)
* es_ES(스페인어)

예를 들어 `https://example.sc.omtrdc.net/optout.html?locale=ko_KR`은 옵트아웃 페이지를 한국어로 로드합니다.

> [!TIP] 기본적으로 페이지가 영어로 로드되므로 `en_US` 쿼리 문자열 값은 필요하지 않습니다.

### 팝업

페이지에 &#39;창 닫기&#39; 단추를 추가하여 옵트아웃 페이지를 팝업 창으로 만들 수 있습니다. `popup` 쿼리 문자열 매개 변수를 사용하고 값을 `1`로 지정하십시오.

예를 들어 `https://example.sc.omtrdc.net/optout.html?popup=1`은 &#39;창 닫기&#39; 단추가 있는 옵트아웃 페이지를 로드합니다.

> [!NOTE] 이전에는 이 쿼리 문자열 매개 변수를 사용하여 팝업 창을 만들었습니다. 그러나 대부분의 최신 브라우저는 최종 사용자가 팝업을 제어할 수 있도록 합니다.

### 옵트아웃 한 번 클릭

이렇게 하면 사용자가 즉시 추적을 그만둘 수 있습니다(옵트아웃). 두 쿼리 문자열 매개 변수 `opt_out` 및 `confirm_change`를 추가하고 각각 값을 `1`로 지정합니다.

예를 들어 `https://example.sc.omtrdc.net/optout.html?opt_out=1&confirm_change=1`은 방문자의 페이지에 옵트아웃 쿠키를 즉시 설치합니다.

### 옵트인 한 번 클릭

이렇게 하면 사용자가 옵트아웃 쿠키를 삭제하여 즉시 추적을 다시 수행할 수 있습니다(옵트인). 두 쿼리 문자열 매개 변수 `opt_in` 및 `confirm_change`를 추가하고 각각 값을 `1`로 지정합니다.

예를 들어 `https://example.sc.omtrdc.net/optout.html?opt_in=1&confirm_change=1`은 방문자에 대한 옵트아웃 쿠키를 즉시 삭제합니다.
