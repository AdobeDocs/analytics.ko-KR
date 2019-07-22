---
description: Appmeasurement. js에 설정된 구성 변수.
keywords: Analytics 구현
seo-description: Adobe Analytics 용 appmeasurement. js에 설정된 구성 변수
seo-title: 구성 변수
solution: Analytics
subtopic: 변수
title: 구성 변수
topic: 개발자 및 구현
uuid: A 19484 B 6-E 350-4 C 12-B 4 D 6-A 31 C 79 A 42 DB 0
translation-type: tm+mt
source-git-commit: 72f2b06f53c6a3c1cae965a1a9b030b0123bfca1

---


# 구성 변수

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 일반적으로 기본 전역 JavaScript appmeasurement. js에 설정되는 가장 일반적인 구성 변수입니다. 이러한 변수는 적절한 경우 Analytics 페이지 수준 코드와 링크 내에서 설정할 수 있습니다.

**[!UICONTROL 관리 도구]** &gt; **[!UICONTROL 코드 관리자를 통해 코드를 생성할 때 이 모든 변수가 기본적으로 코드에 나타나지]**&#x200B;않습니다. 이러한 구성 변수 중 일부는 사이트의 구현 요구에 적용할 수 없을 수도 있습니다.

이러한 구성 변수를 사용하는 몇 가지 목적은 다음과 같습니다.

* 여러 사이트/도메인 추적
* 구매 시 임의 통화 사용
* 다양한 언어로 데이터 캡처
* 링크 추적(다운로드한 파일의 수, 외부 사이트에 대한 링크)
* 고유한 목적으로 사용자 지정 링크 추적

>[!NOTE]
>
>[!DNL AppMeasurement] 모든 구성 변수가 추적 함수 초기 호출 전에 설정되어야 `t()`합니다. If configuration variables are set after the call to `t()`, unexpected results may occur. To ensure proper data collection, all configuration variables must be above the `doPlugins` function.

## s.account {#concept_685A5C832A6C40619ACB5920925785DC}

<!--
s_account.xml
-->

 변수는 데이터를 저장 및 보고하는 보고서 세트를 결정합니다.

If sending to multiple report suites (multi-suite tagging), `s.account` may be a comma-separated list of values. 보고서 세트 ID는 Adobe에 의해 결정됩니다.

**매개 변수**

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| 40바이트 | URL 경로에서 | N/A | N/A |

Each report suite ID must match the value created in the [!DNL Admin Console]. 각 보고서 세트 ID는 40바이트 이하여야 하지만 모든 보고서 세트의 집계 정보(쉼표로 구분된 목록 전체)에는 제한이 없습니다.

보고서 세트는 보고에서 세그먼테이션의 가장 기본적인 수준입니다. 계약에서 허용하는 만큼 많은 보고서 세트를 설정할 수 있습니다. 각 보고서 세트는 Adobe의 수집 서버에서 채워지는 전용 테이블을 참조하십시오. 보고서 세트는 JavaScript 코드의 `s_account`변수로 식별됩니다. 

[!DNL Analytics] 내에서, 보고서의 왼쪽 상단에 있는 사이트 드롭다운 상자에는 현재 보고서 세트가 표시됩니다. 각 보고서 세트에는 보고서 세트 ID라는 고유 식별자가 있습니다. 변수 `s_account` 변수에는 데이터가 전송되는 하나 이상의 보고서 세트 ID가 포함되어 있습니다. [!DNL Analytics] 사용자에게 보이지 않는 보고서 세트 ID 값은 사용하기 전에 Adobe에서 제공 또는 승인 받아야 합니다. Every report suite ID has an associated "friendly name" that can be changed in the report suites section of the [!DNL Admin Console].

`s_account` 이 변수는 일반적으로 JavaScript 파일 (s_ code. js) 내에서 선언됩니다. You can declare the `s_account` variable on the HTML page, which is a common practice when the value of `s_account` may change from page to page. `s_account` 변수에 전역 범위가 있으므로 Adobe의 JavaScript 파일을 포함하기 직전에 선언해야 합니다. If `s_account` does not have a value when the JavaScript file is loaded, no data is sent to [!DNL Analytics].

Adobe's [!DNL DigitalPulse Debugger] displays the value of `s_account` in the path of the URL that appears just below the word "Image," just after /b/ss/. In some cases, the value of `s_account` also appears in the domain, before 112.2o7.net. 경로의 값은 대상 보고서 세트를 결정하는 유일한 값입니다. 아래의 굵은 텍스트는 데이터를 전송 받는 보고서 세트가 디버거에 나타난 모습을 표시합니다. see [DigitalPulse Debugger](../../../implement/impl-testing/debugger.md#concept_B26FFE005EDD4E0FACB3117AE3E95AA2).

```js
https://mycompany.112.207.net/b/ss/ 
<b>mycompanycom,mycompanysection</b>/1/H.1-pdv-2/s21553246810948?[AQB]
```

**구문 및 가능한 값** {#section_3BE913DF26D848AEB4CB5B0A6CE7F0CA}

보고서 세트 ID는 40바이트 길이 이하의 ASCII 영숫자 문자열입니다. 영숫자가 아닌 문자 중에서는 하이픈만 허용됩니다. 공백, 마침표, 쉼표 및 기타 구두점은 허용되지 않습니다. the `s_account` 에는 여러 보고서 세트가 포함될 수 있으며 이 모든 세트가 해당 페이지로부터 데이터를 받습니다.

```js
var s_account="reportsuitecom[,reportsuite2[,reportsuite3]]"
```

All values of `s_account` must be provided or approved by Adobe.

**예** {#section_16580A9101B64560A58C7745397FB42F}

```js
var s_account="mycompanycom"
```

```js
var s_account="mycompanycom,mycompanysection"
```

**Analytics**&#x200B;의 변수 구성 {#section_7DFB2CCF02F045AFB1AD4F376638393B}

각 보고서 세트 ID와 연결된 친숙한 이름은 Adobe [!DNL Customer Care]에서 변경할 수 있습니다. 친숙한 이름은 [!DNL Analytics] 상단의 화면 왼쪽 섹션에 있는 사이트 드롭다운 상자에서 확인할 수 있습니다.

**함정, 질문 및 팁** {#section_BFFDA5C0AF31442494B0E02F0925CF93}

* If `s_account` is empty, not declared, or contains an unexpected value, no data is collected.
* `s_account` 변수가 쉼표로 구분된 목록 (다중 세트 태그 지정) 인 경우 보고서 세트 ID 사이에 공백을 넣지 마십시오.
* [!UICONTROL s. dynamicaccountselection] 이 true로 *설정되면 URL* 이 대상 보고서 세트를 결정하는 데 사용됩니다. [!DNL DigitalPulse Debugger]를 사용하여 수신처 보고서 세트를 결정하십시오.

* 일부 경우에, [!DNL VISTA]를 사용하여 수신처 보고서 세트를 변경할 수 있습니다. 자사 쿠키를 사용하거나 사이트에 활성 보고서 세트가 20개 이상 있는 경우, [!DNL VISTA]를 사용하여 데이터를 다시 전송하거나 다른 보고서 세트에 복사하는 것이 좋습니다.

* Always declare `s_account` inside the JS file or just before it is included.

## s.dynamicAccountSelection {#concept_FAD499DB357148DB8BD74F08093D3E35}

 변수를 사용하면 각 페이지의 URL을 기반으로 보고서 세트를 동적으로 선택할 수 있습니다.

>[!NOTE]
>
>`dynamicAccountSelection` 은 사용자 지정 링크 추적 시 작동하지 않습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | False |

>[!NOTE]
>
>Both `dynamicAccountList` and `dynamicAccountMatch` are ignored if the `dynamicAccountSelection` variable is not declared or set to 'false.'

**구문 및 가능한 값** {#section_36E5D0E2170345F5A652B44CE85DFED1}

```js
s.dynamicAccountSelection=[true|false]
```

Only 'true' and 'false' are allowed as values of *`dynamicAccountSelection`*.

**예** {#section_E8CE8BA62C7545889531495E2521663D}

```js
s.dynamicAccountSelection=true
```

```js
s.dynamicAccountSelection=false
```

**구성 설정** {#section_F052FA38144B4F84B015A263A8E711CF}

없음

**함정, 질문 및 팁** {#section_62F0B0895BC84A05840AEEED0643DE60}

* Dynamic account selection is not supported by [AppMeasurement for JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8).
* 각 페이지의 데이터를 받는 보고서 세트를 결정하려면 항상 [!DNL DigitalPulse Debugger]를 사용하십시오.

## s.dynamicAccountList {#concept_19715BA0AD4D41748E0C4A4A6B71AB51}

<!-- 
dynamicAccountList.xml
-->

[!DNL AppMeasurement] JavaScript의 경우 데이터를 보내는 보고서 세트를 동적으로 선택할 수 있습니다.  변수에는 대상 보고서 세트를 결정하는 데 사용할 규칙이 포함됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | "" |

이 변수는 *`dynamicAccountSelection`**`dynamicAccountMatch`* 변수를 참조하십시오. The rules in *`dynamicAccountList`* are applied if *`dynamicAccountSelection`* is set to 'true,' and they apply to the section of the URL specified in *`dynamicAccountMatch`*.

If none of the rules in *`dynamicAccountList`* matches the URL of the page, the report suite identified in `s_account` is used. 이 변수에 나열된 규칙은 왼쪽에서 오른쪽 순서로 적용됩니다. 페이지 URL이 두 개 이상의 규칙에 일치하는 경우, 가장 왼쪽 규칙이 보고서 세트를 결정하는 데 사용됩니다. 그 결과, 더 일반적인 규칙이 목록의 오른쪽으로 이동합니다.

In the following examples, the page URL is `www.mycompany.com/path1/?prod_id=12345` and `dynamicAccountSelection` is set to *true* and `s_account` is set to `mysuitecom.`

| DynamicAccountList 값 | DynamicAccountMatch 값 | 데이터를 받는 보고서 세트 |
|---|---|---|
| `mysuite2=www2.mycompany.com;mysuite1=mycompany.com` | window.location.host | mysuite1 |
| "mysuite1=path4,path1;mysuite2=path2" | window.location.pathname | mysuite1, mysuite2 |
| "mysuite1=path5" | window.location.pathname | mysuitecom, mysuite1 |
| "myprodsuite=prod_id" | window.location.search?window.location.search:"?") | myprodsuite |

**구문 및 가능한 값** {#section_7360E4354ED345E8BAAE210DBD58A7EC}

`dynamicAccountList` 변수는 세미콜론으로 구분된 이름 = 값 쌍 (규칙) 입니다. 목록의 각 부분에는 다음 항목이 들어 있습니다.

* 하나 이상의 보고서 세트 ID(쉼표로 분리)
* 등호
* 하나 이상의 URL 필터(쉼표로 분리)

```js
s.dynamicAccountList=rs1[,rs2]=domain1.com[,domain2.com/path][;...]
```

문자열에는 공백 없이 표준 ASCII 문자만 사용해야 합니다.

**예** {#section_49936D14EF6D45859B666C9E7A4CBA9E}

```js
s.dynamicAccountList="mysuite2=www2.mycompany.com;mysuite1=mycompany.com"
```

```js
s.dynamicAccountList="ms1,ms2=site1.com;ms1,ms3=site3.com"
```

**구성 설정** {#section_9F99CD741BC7449B8CCC108094B2EB85}

없음

**함정, 질문 및 팁** {#section_3E10534FCC05457AB67147BB480C8BB3}

* Dynamic account selection is not supported by [AppMeasurement for JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8).
* 페이지 URL이 여러 규칙을 만족하는 경우, 왼쪽 끝에 있는 규칙이 사용됩니다.
* 만족하는 규칙이 없을 경우에는 기본 보고서 세트가 사용됩니다.
* 페이지가 누군가의 하드 드라이브에 저장되거나 웹 기반 번역 엔진을 통해 번역되는 경우(Google의 번역된 페이지)에는, 동적 계정 선택 기능이 작동하지 않습니다. 더 정밀한 추적을 수행하려면, `s_account` 변수 서버측을 채우십시오.
* The `dynamicAccountSelection` rules apply only to the section of the URL specified in `dynamicAccountMatch`.

* When using dynamic account selection, be sure to update *`dynamicAccountList`* every time you obtain a new domain.
* 대상 보고서 세트를 식별할 때 [!DNL DigitalPulse Debugger]를 사용하십시오. `dynamicAccountSelection` 변수는 항상의 값을 무시합니다 `s_account`.

## s.dynamicAccountMatch {#concept_718171E602214CCC9905C749708BBE52}

<!-- 
dynamicAccountMatch.xml
-->

변수는 DOM 개체를 사용하여의 모든 규칙이 적용되는 URL 섹션을 검색합니다.

This variable is only valid when *`dynamicAccountSelection`* is set to 'True.' 기본값이 [!DNL window.location.host]이므로, 이 값은 [!UICONTROL 동적 계정 선택] 기능이 작동하는 데 필요하지 않습니다. For additional information, see [dynamicAccountList](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_19715BA0AD4D41748E0C4A4A6B71AB51).

The rules found in `dynamicAccountList` are applied to the value of `dynamicAccountMatch`. If `dynamicAccountMatch` only contains [!DNL window.location.host] (default), the rules in `dynamicAccountList` apply only to the domain of the page.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | window.location.host |

**구문 및 가능한 값** {#section_95CD81972C22419B80A921CA137D3841}

`dynamicAccountMatch` 이 변수는 보통 JavaScript 용 appmeasurement 파일을 제공하는 Adobe 컨설턴트가 채웁니다. 하지만 아래 목록의 값들은 언제든지 적용할 수 있습니다.

```js
s.dynamicAccountMatch=[DOM object]
```

| 설명 | 값 |
|---|---|
| 도메인(기본값) | window.location.host |
| 경로 | window.location.pathname |
| 쿼리 문자열 | (window.location.search?window.location.search:"?") |
| 도메인 및 경로 | window.location.host+window.location.pathname |
| 경로 및 쿼리 문자열 | window.location.pathname+(window.location.search?window.location.search:"?") |
| 전체 URL | window.location.href |

**예** {#section_924687CCE255421AA2223A3D4B8B6A30}

```js
s.dynamicAccountMatch=window.location.pathname
```

```js
s.dynamicAccountMatch=window.location.host+window.location.pathname
```

**구성 설정** {#**section_43BCE13B1ADD4D418DF7CBB9DD7A6472}

없음

**함정, 질문 및 팁** {#section_EF9B2977BC21497D8C5EEB9BAD731E17}

* Dynamic account selection is not supported by [AppMeasurement for JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8).
* When pages are saved to a hard drive, [!DNL window.location.host] is empty, causing those page views to be sent to the default report suite (in `s_account`).

* 페이지가 Google과 같은 웹 기반 번역 엔진을 통해 번역되는 경우, [!UICONTROL 동적 계정 선택] 기능이 설계대로 작동하지 않습니다. 더 정밀한 추적을 수행하려면, [!UICONTROL s_account ]변수 서버측을 채우십시오.

## s.dynamicVariablePrefix {#concept_38C1F2452DDB47FCA8F458BE1398E276}

<!-- 
dynamicVariablePrefix.xml
-->

 변수를 사용하면 배포 시 변수에 플래그를 지정하는데 이것은 동적으로 채워집니다.

쿠키, 요청 헤더 및 이미지 쿼리 문자열 매개 변수는 동적으로 채울 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | D= | 임의 | D= |

**구문 및 가능한 값** {#section_D0669899567F46B6A081C7661362BA81}

```js
s.prop1="D=User-Agent”
```

또는 동적 변수에 대한 사용자 지정 플래그 사용

```js
s.dynamicVariablePrefix=".."
```

**예** {#section_DD148560F9E8416EBCF159194FA427AC}

```js
s.prop1="D=User-Agent”
```

또는 동적 변수에 대한 사용자 지정 플래그 사용

```js
s.dynamicVariablePrefix=".."
```

```js
s.prop1="..User-Agent"
```

**함정, 질문 및 팁** {#section_6889908FBD78488D955F67DDB17617B1}

* 동적 변수를 사용하면 값을 다른 변수에 복사하여 URL의 전체 길이를 크게 줄일 수 있습니다.
* 동적 변수는 별도로 데이터 수집에 사용할 수 없는 헤더와 쿠키의 데이터를 모으는 데 사용할 수 있습니다.

## s.charSet {#concept_E65B9A8F75C3482C87D0D455805F89BD}

<!-- 
charset.xml
-->

Javascript 파일에서 일반적으로 설정되는 charset 속성은 Analytics에서 저장 및 보고를 위해 들어오는 데이터를 UTF -8로 변환하는 데 사용됩니다.

>[!NOTE:] Charset 속성은 데이터를 2 바이트 보고서 세트로 전송할 때 필요하며 표준 보고서 세트와 함께 사용해서는 안 됩니다. 표준 ISO 보고서 세트와 함께 charSet 속성을 사용하면 변수가 잘리거나 예기치 않는 문자 변환이 일어날 수 있습니다.

구문은 약간 다를 수 있어도 charSet 속성 값은 META 태그 또는 http 헤더 안의 웹 페이지 인코딩과 일치해야 합니다. META 태그는 인코딩에 별칭을 사용할 수 있지만 charSet 값은 인코딩의 기본(또는 정식) 이름을 사용해야 합니다.

다음 표에 일부 인코딩의 기본 이름과 별칭이 요약되어 있습니다.

| 기본 이름 | 별칭 |
|--- |--- |
| ISO-8859-1 | ISO_8859-1,CP819,latin1 |
| ISO-8859-2 | ISO_8859-2,latin2 |
| ISO-8859-5 | ISO_8859-5,cyrillic |
| Big5 | Big-5 |
| Shift_JIS | SJIS |

다양한 인코딩과 별칭이 존재하므로 위 표에 나타나지 않는 경우 구현 컨설턴트 또는 Adobe 고객 지원 팀에 문의하여 charset에 대한 올바른 값을 확인해야 합니다.

If a site has different web encodings on different pages, or a single JavaScript file is used for multiple sites, the charSet property can be set to a default value in the JavaScript file and then reset on specific pages as needed to override the default; for example, `s.charSet="UTF-8"` or `s.charSet="SJIS"`.

공백이 아닌 모든 charSet 매개 변수 값에 따라 데이터가 저장을 위해 UTF-8로 변환됩니다. 128-255 범위의 문자가 적절한 UTF-8 2바이트 시퀀스로 변환되어 저장됩니다. 이러한 문자는 표준 보고서 세트에서 올바로 표시되지 않습니다. 따라서 charSet 속성을 표준 보고서 세트와 함께 사용해서는 안 됩니다.

마찬가지로 공백인 charSet 매개 변수는 데이터 변환 프로세스를 무시하고 128-255 범위의 모든 문자를 1바이트로 저장합니다. 이러한 문자는 2바이트 보고서 세트에서 올바로 표시되지 않는데, 그 이유는 해당 문자의 1바이트 코드가 유효한 UTF-8이 아니기 때문입니다. 따라서 charSet 매개 변수는 항상 2바이트 보고서 세트와 함께 사용해야 합니다. 또한 웹 페이지 인코딩에 적합한 값을 사용해야 합니다.

*`charSet`* 변수에 잘못된 값이 포함되어 있으면 다른 모든 변수의 데이터가 잘못 변환됩니다. If JavaScript variables on your pages (e.g. *`pageName`*, [!UICONTROL prop1], or *`channel`*) contain only ASCII characters, *`charSet`* does not need to be defined. However, if the variables on your pages contain non-ASCII characters, the *`charSet`* variable must be populated.

**매개 변수**

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | CE | N/A | "" |

**구문 및 가능한 값** {#section_EBC2176067A04D9E814CF78A86DC80FA}

```js
s.charSet="character_set"
```

**예** {#section_406DE0A2B58441DB8512F5B3BE5D9CB5}

```js
s.charSet="ISO-8859-1"
```

```js
s.charSet="SJIS"
```

## s.currencyCode {#concept_CE216F1610E2499D8178DB9A8EB97C63}

<!-- 
currencycode.xml
-->

 변수는 매출에 적용할 전환율을 결정합니다.

모든 금액은 선택한 통화로 저장됩니다. 이 통화가 *`currencyCode`*&#x200B;또는 *`currencyCode`* 비어 있으면 전환이 적용되지 않습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | cc | 전환 &gt; 구매 &gt; 매출 매출이나 통화 가치를 보여 주는 모든 전환 보고서 | "USD" |

사이트에서 방문자가 여러 통화로 구매할 수 있는 경우, *`currencyCode`* 변수를 사용하여 매출이 적절한 통화로 저장되었는지 확인해야 합니다. For example, if the base currency for your report suite is USD, and you sell an item for 40 Euros, you should populate the *`currencyCode`* with "EUR" on the HTML page. 데이터 수집에서는 데이터를 받자마자 현재 전환율을 사용하여 40유로를 해당 USD로 전환합니다.

여러 통화로 판매하는 경우에는 JavaScript 파일 대신 HTML 페이지에서 *`currencyCode`* 변수를 채우는 것이 좋습니다. If you want to use your own conversion rates rather than the conversion rates used by Adobe, set the *`currencyCode`* to equal the base currency of your report suite. 그런 다음 모든 매출을 [!DNL Analytics]로 보내기 전에 전환합니다.

통화 전환은 매출과 모든 통화 이벤트 모두에 적용됩니다. 이러한 이벤트들은 세금이나 배송과 같이, 매출과 유사한 값들을 합하는 데 사용되는 이벤트입니다. 매출 및 통화 이벤트는 제품 문자열에서 지정됩니다. 제품에 대한 자세한 내용은 [events](../../../implement/js-implementation/c-variables/page-variables.md#concept_FFD115543D54401B98FE683BD7D5B3FE). 통화를 관리하는 방법에 대한 자세한 내용은 [복수 통화 지원](https://marketing.adobe.com/resources/help/en_US/whitepapers/currency/)을 참조하십시오.

**구문 및 가능한 값** {#section_7CD68F08AB4848EE9B0D19DCC3F1BECE}

```js
s.currencyCode="currency_code"
```

[복수 통화 지원](https://marketing.adobe.com/resources/help/en_US/whitepapers/currency/)에 나온 통화 코드만 허용됩니다.

**예** {#section_D55ED45369544C8AAA02B3193752636C}

```js
s.currencyCode="GBP"
```

```js
s.currencyCode="EUR"
```

**구성 설정** {#section_D05E29F545A04958B1C0A82248BCA1B0}

Adobe [!DNL Customer Care]에서는 보고서 세트에 대한 기본 통화 설정을 변경할 수 있습니다. 보고서 세트에 대한 기본 통화를 변경할 경우, 시스템에 있는 기존 매출은 전환되지 않습니다. 모든 새 매출액은 변경된 설정에 따라 전환됩니다.

**함정, 질문 및 팁** {#section_08A80A87B54A4861905953A6FA61FF8F}

* If you notice surprisingly large amounts of revenue in reports, ensure that the *`currencyCode`* variable and base currency of the report suite are set correctly.
* *`currencyCode`* 변수는 지속적이지 않으며, 이것은 매출 또는 기타 통화 관련 지표와 동일한 이미지 요청에서 변수를 전달해야 함을 의미합니다.
* 통화 이벤트는 비통화 목적으로는 사용하면 안 됩니다. 통화가 아닌 임의의 또는 동적인 값을 계산해야 하는 경우에는 [!UICONTROL 숫자] 이벤트 유형을 사용하십시오.
* when the *`currencyCode`* 변수가 비어 있으면, 전환이 적용되지 않습니다.

## s.cookieDomain {#concept_6164C39CF8BE4737A7EF1DE5A8376C1B}

<!-- 
cookiedomain.xml
-->

The  variable determines the domain on which the [!DNL Analytics] cookies `s_cc` and `s_sq` are set.

Commonly, `s.cookieDomainPeriods` is used to generate `s.cookieDomain` from `window.location.hostnam`e. Instead of using `s.cookieDomainPeriods`, you can explicitly set `s.cookieDomain` to what you want to use in your implementation. 예를 들면 다음을 사용하여 정규화된 페이지 이름에 쿠키를 설정할 수 있습니다.

`s.cookieDomain = window.location.hostname;`

## s.cookieDomainPeriods {#concept_F17A59C7D8F54F5897AD40980B6725EB}

<!-- 
cookiedomainperiods.xml
-->

The  variable determines the domain on which the [!DNL Analytics] cookies `s_cc` and `s_sq` are set by determining the number of periods in the domain of the page URL. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다.

The default value for *`cookieDomainPeriods`* is "2". This is the value that is used if *`cookieDomainPeriods`* is omitted. For example, using the domain `www.mysite.com`, *`cookieDomainPeriods`* should be "2". For `www.mysite.co.jp`, *`cookieDomainPeriods`* should be "3".

If *`cookieDomainPeriods`* is set to "2" but the domain contains three periods, the JavaScript file attempts to set cookies on the domain suffix.

For example, if setting *`cookieDomainPeriods`* to "2" on the domain `www.mysite.co.jp`, the `s_cc` and `s_sq` cookies are created on the domain `co.jp`. `co.jp`가 잘못된 도메인이므로 거의 모든 브라우저는 이 쿠키를 거부하게 됩니다. 그 결과, 방문자 클릭 맵 데이터가 유실되고, [!UICONTROL 방문자 프로필] &gt; [!UICONTROL 기술] &gt; [!UICONTROL 쿠키] 보고서는 거의 100%의 방문자가 쿠키를 거부한다고 나타냅니다.

If *`cookieDomainPeriods`* is set to "3" but the domain contains only two periods, the JavaScript file sets the cookies on the subdomain of the site. For example, if setting *`cookieDomainPeriods`* to "3" on the domain `www2.mysite.com`, the `s_cc` and `s_sq` cookies are created on the domain `www2.mysite.com`. When a visitor goes to another subdomain of your site (such as `www4.mysite.com`), all cookies set with `www2.mysite.com` cannot be read.

>[!NOTE]
>
>Do not include additional subdomains as part of *`cookieDomainPeriods`*. For example, `store.toys.mysite.com` would still have *`cookieDomainPeriods`* set to "2". 이 변수 정의는 루트 도메인 [!DNL mysite.com]에 대한 쿠키를 올바로 설정합니다. Setting *`cookieDomainPeriods`* to "3" in this example would set cookies on the domain [!DNL toys.mysite.com], which has the same implications as the prior example.

[s. fpcookiedomainperiods](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_0A25BD152B0744989E7C662A95448274)를 참조하십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | CDP | 여러 보고서에서 방문자 ID의 저장 및 처리 방식을 제어하는 데 영향을 줍니다. | "2" |

>[!NOTE]
>
>일부 클라우드 컴퓨팅 서비스는 쿠키를 작성할 수 없는 최상위 도메인으로 간주됩니다. (For example, `compute.amazonaws.com`, `*.herokuapp.com`, `*.googlecode.com`, and so on.) 이러한 서비스에 구현하는 경우 사용자 고유의 도메인이 설정되어 있지 않으면 모든 쿠키를 차단한 사용자를 제거하는 Analytics 개인 정보 보호 설정의 영향을 받을 수 있습니다(예: 구현을 테스트하는 경우). 이 경우 쿠키가 비활성화되었거나, 작동하지 않거나, 액세스할 수 없는 것으로 확인된 히트는 옵트아웃되므로, 보고에서 제외됩니다.

**예** {#section_4218BE29FA5E49F58975A2094329B268}

수동 변수 설정:

```js
s.cookieDomainPeriods = "3";
```

코어 Javascript 파일이 두 유형을 모두 호스팅하는 경우 이 변수를 동적으로 설정하는 몇 가지 예:

```js
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```

```js
s.cookieDomainPeriods = "2"; 
var d=window.location.hostname; 
if(d.indexOf(".co.uk") > 0 || d.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

```js
s.cookieDomainPeriods = "2"; 
if(window.location.indexOf(".co.jp") > 0 || window.location.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

**함정, 질문 및 팁** {#section_F3BE3F039E5C4359B694DBB61369822C}

* If you notice that visitor click map data is absent, or that the [!UICONTROL Traffic] &gt; [!UICONTROL Technology] &gt; [!UICONTROL Cookies] report shows a large percentage of visitors who reject cookies, check that the value of *`cookieDomainPeriods`* is correct.

* If *`cookieDomainPeriods`* is higher than the number of sections in the domain, cookies will be set with the full domain. 이로 인해 방문자가 하위 도메인 간을 전환하면 데이터 손실이 발생할 수 있습니다.
* the *`cookieDomainPeriods`* 변수는 방문자 ID 쿠키를 설정하기 전에 더 이상 사용되지 않는 *`trackingServer`* 구현에서 사용되었습니다. Though only present in outdated code, failure to correctly define *`cookieDomainPeriods`* in this circumstance puts your implementation at risk of data loss.

## s.fpCookieDomainPeriods {#concept_0A25BD152B0744989E7C662A95448274}

<!-- 
fpCookieDomainPeriods.xml
-->

 변수는 구현에 타사 2o7.net 또는 omtrdc.net 도메인을 사용하는 경우에도 기본적으로 자사 쿠키인 JavaScript 설정 쿠키(s_sq, s_cc, plug-ins)에 사용됩니다.

*`fpCookieDomainPeriods`* 변수를 동적으로 설정하면 안 됩니다. If you use *`cookieDomainPeriods`*, it is good practice to specify a value for *`fpCookieDomainPeriods`* as well. *`fpCookieDomainPeriods`**`cookieDomainPeriods`* 값을 상속합니다. Note that *`fpCookieDomainPeriods`* does not affect the domain on which the visitor ID cookie is set, even if your implementation treats this as a first-party cookie.

The name " *`fpCookieDomainPeriods`*" refers to the number of periods (".") "www"로 시작되는 경우 도메인에 포함된 점(.) 수를 나타냅니다. For example, `www.mysite.com` contains two periods, while `www.mysite.co.jp` contains three periods. Another way to describe the variable is the number of sections in the main domain of the site (two for `mysite.com` and three for `mysite.co.jp`).

The [!DNL AppMeasurement] for JavaScript file uses the *`fpCookieDomainPeriods`* variable to determine the domain with which to set first-party cookies other than the [!UICONTROL visitor ID] (s_vi) cookie. s_sq 및 s_cc(각각 방문자 클릭 맵과 쿠키 확인에 사용)를 포함한 두 개 이상의 쿠키가 이 변수의 영향을 받습니다. [!UICONTROL getValOnce]와 같은 플러그인에서 사용되는 쿠키도 영향을 받습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | cookieDomainPeriods |

**쿠키 도메인 변수 설정을 위한 샘플 코드** {#section_5200A92D40384C82998606E800B69E13}

```js
s.fpCookieDomainPeriods="2" 
var d=window.location.hostname 
if(d.indexOf('.co.uk')>-1||d.indexOf('.com.au')>-1) 
  s.fpCookieDomainPeriods="3" 
```

**구문 및 가능한 값** {#section_87923F4C12E74AF99CC9AFC0FFD77D49}

*`cookieDomainPeriods`* 이 변수는 아래와 같이 문자열이 될 것으로 예상됩니다.

```js
s.fpCookieDomainPeriods="3"
```

**예** {#section_EF7355718AD849BF963EE9F6F9F79891}

```js
s.fpCookieDomainPeriods="3"
```

```js
s.fpCookieDomainPeriods="2"
```

**구성 설정** {#section_DB65D9BC4F3048C8AD08F9A7CD8FCFC0}

없음

## s.cookieLifetime {#concept_8347C6648B0E4D4996E2F223C34B9A3D}

<!-- 
cookielifetime.xml
-->

 변수는 쿠키의 수명을 결정할 때 JavaScript와 데이터 수집 서버 모두에서 사용됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | cl | 트래픽 &gt; 기술 &gt; 쿠키. 모든 방문자 관련 보고서 | "" |

만약 *`cookieLifetime`* 이 설정되면, 이 값은 아래 설명된 한 가지 예외를 제외하고 JavaScript와 데이터 수집 서버 모두에 대한 다른 쿠키 만료를 무시합니다. The *`cookieLifetime`* variable can have one of three values:

* [!DNL Analytics] 쿠키
* 쿠키
* JavaScript 설정 및 플러그인

**구문 및 가능한 값** {#section_09D4D122451B45FAB2C9398600EC66F1}

```js
s.cookieLifetime="value"
```

가능한 값은 다음과 같습니다.

* ""
* "NONE"
* "SESSION"
* 만료까지의 시간을 초 단위로 나타낸 정수

**예** {#section_91499F70C8B14D3292FCF1B60F04E30A}

```js
s.cookieLifetime="SESSION"
```

```js
s.cookieLifetime="86400" // one day in seconds
```

**구성 설정** {#section_7BDAD4CFE8414C9BA5717A8C8B1BDD34}

없음

**함정, 질문 및 팁** {#section_23E24877F6554E0D9F8C8B7A9C2994B2}

*`cookieLifetime`* 추적에 영향을 [!DNL Analytics] 줍니다. If, for example, *`cookieLifetime`* is two days, then monthly, quarterly, and yearly unique visitor reports will be incorrect. 따라서 *`cookieLifetime`*.

## s.doPlugins {#concept_676EAE4FAFCF4B018876390FC874EFDA}

<!-- 
doPlugins.xml
-->

 변수는 함수 참조로서, 이 변수를 사용하면 JavaScript 파일 내의 적절한 위치에서 함수를 호출할 수 있습니다.

The *`s_doPlugins`* function is called each time any of the following occurs:

* *`t()`* 함수가
* *`tl()`* 함수가
* 종료 또는 다운로드 링크를 클릭할 때
* 방문자 클릭 맵이 추적하는 페이지 요소를 클릭할 때

the *`doPlugins`*&#x200B;함수는 데이터를 모으거나 바꾸는 사용자 지정 루틴을 실행하는 데 사용됩니다. If you are using an object name other than "s," make sure that the *`s_doPlugins`* is renamed appropriately. For example, if your object name is s_mc, the *`s_doPlugins`* function should be called s_mc_doPlugins.

**구문 및 가능한 값** {#section_5CFB94598521455E80947964A306EA89}

*`s_doPlugins`* 함수는 따옴표 안에 있으면 안 되며 *`doPlugins`**`s_doPlugins`* 함수의 정확한 이름 (함수 이름이 변경된 경우) 에 항상 지정해야 합니다.

```js
s.doPlugins=s_doPlugins;
```

**예** {#section_A5CF0054C56745268A1313CCC7730022}

```js
s.doPlugins=s_doPlugins;
```

```js
s_mc.doPlugins=s_mc_doPlugins;
```

**구성 설정** {#section_641F0EC55E3349E5A3F8671446797074}

없음

**함정, 질문 및 팁** {#section_0C7FB61CF0C946EF8A7D1B686D36E6ED}

* 개체 이름을 변경(s에서 s_mc으로 변경하는 등)하는 유일한 이유는 컨텐츠를 다른 고객과 공유하거나 다른 고객의 컨텐츠를 가져오는 경우입니다. 이름 바꾸기 *`s_doPlugins`* 함수를 [!UICONTROL s_ mc_ doplugins] 로 설정하면 다른 클라이언트의 JavaScript 파일이 사용자의 *`doPlugins`* 함수를 덮어쓰지 않습니다.

* If you unexpectedly start pulling in content from another Adobe customer, and your *`s_doPlugins`* function is being overwritten, it is possible to simply rename the *`s_doPlugins`* function without changing the object name. 같은 페이지에서 다른 JavaScript 파일이 아닌 다른 개체 이름을 사용하는 것이 최고의 솔루션일 경우에는 그렇게 할 필요가 없습니다.

## s. registerpretrackcallback 및 s. registerposttrackcallback

이 함수들은 매개 변수로서 콜백(기능)을 사용하고 해당 기능에 대한 매개 변수를 사용합니다. 예:

```
s.registerPreTrackCallback(function(requestUrl,a,b,c) { 
    console.log("pre track callback"); 
    console.dir(requestUrl); // Request URL 
    console.dir(a); // param1 
    console.dir(b); // param2 
    console.dir(c); // param3 
}, "param1", "param2", "param3");
```

콜백은 콜백을 등록할 때 전달되는 모든 매개 변수와 `requestUrl`과 함께 호출됩니다. 이러한 일은 콜백을 등록하는 데 사용되는 메서드에 따라 추적 호출 전 또는 후에 발생합니다.

이러한 콜백이 호출되는 순서는 보장되지 않습니다. 사전 함수에 등록된 콜백은 최종 추적 URL이 생성된 후 호출됩니다. 사후 콜백은 추적 호출 성공 시 호출됩니다(추적 호출이 실패하는 경우에는 이 함수들이 호출되지 않습니다). `registerPreTrackCallback`과 함께 등록된 모든 콜백은 추적 호출에 영향을 주지 않습니다. 또한, 등록된 임의의 콜백에서는 추적 메서드를 호출하지 않는 것이 좋으며, 호출하는 경우 무한 루프가 발생할 수 있습니다.

## s.trackDownLoadLinks {#concept_0A7AEAB3172A4BEA8B2E8B1A3A8F596C}

<!-- 
trackDownloadLinks.xml
-->

사이트에서 다운로드 가능한 파일에 대한 링크를 추적하려면'true'로 설정합니다.

If *`trackDownloadLinks`* is 'true,' *`linkDownloadFileTypes`* is used to determine which links are downloadable files.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | True |

사이트의 다운로드 가능 파일에 대한 링크가 없거나, 다운로드 가능 파일을 클릭한 횟수를 추적하는 데 관심이 없을 경우에만 *`trackDownloadLinks`*&#x200B;변수를 'false'로 설정해야 합니다. If *`trackDownloadLinks`* is 'true,' when a file download link is clicked, data is immediately sent to [!DNL Analytics]. 다운로드 링크와 함께 전송되는 데이터에는 링크 다운로드 URL과 해당 링크의 방문자 클릭 맵 데이터가 포함됩니다. if *`trackDownloadLinks`* 가'false'이면 사이트에서 다운로드 가능한 파일에 대한 링크의 방문자 클릭 맵 데이터가 제대로 보고되지 않을 수 있습니다.

**구문 및 가능한 값** {#section_828492CC2A144BC68D18C30CF397EEFC}

*`trackDownloadLinks`변수는 'true' 또는 'false'입니다.*

**예** {#section_BE2FA1873EBD4C5CA95E98B922B10280}

```
js
s.trackDownloadLinks=true 
```

```
js
s.trackDownloadLinks=false
```

**구성 설정** {#section_9A5F69966BAF433A8DA2BCF655A652D1}

없음

**함정, 질문 및 팁** {#section_B3764520D81143968F96CB69AADD457F}

* When *`trackDownloadLinks`* is 'false,' links that people use to download files on your site are likely to be under reported in visitor click map.
* When *`trackDownloadLinks`* is 'true,' data is sent each time a visitor clicks a file download link.

## s.trackExternalLinks {#concept_E1321318696841648A54CF77F6C4A7AF}

<!-- 
trackExternalLinks.xml
-->

가'true'이면 클릭된 링크가 종료 링크인지를 판별하는 데 사용됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | True |

사이트의 다운로드 가능 파일에 대한 링크가 없거나, 다운로드 가능 파일을 클릭한 횟수를 추적하는 데 관심이 없을 경우에만 *`trackExternalLinks`*&#x200B;변수를 'false'로 설정해야 합니다. 종료 링크는 방문자를 사이트 외부로 보내는 모든 링크입니다. if *`trackExternalLinks`* 가'true'이면 종료 링크를 클릭하면 추적 데이터가 즉시 전송됩니다. 종료 링크와 함께 전송되는 데이터에는 링크 URL, 링크 이름, 및 해당 링크의 방문자 클릭 맵 데이터가 포함됩니다. if *`trackExternalLinks`* 가'false'이면 사이트의 종료 링크에 대한 방문자 클릭 맵 데이터가 보고되지 않을 수 있습니다.

**구문 및 가능한 값** {#section_267748949A7544658E1D838AAEF964B2}

*`trackExternalLinks`변수는 'true' 또는 'false'입니다.*

```
js
s.trackExternalLinks=true|false
```

**예** {#section_EF18DB05884240F5B5062631E68E10A7}

```
js
s.trackExternalLinks=true 
```

```
js
s.trackExternalLinks=false
```

**구성 설정** {#section_C8748CFE36324FAFB14C23E3E1FB5082}

없음

**함정, 질문 및 팁** {#section_FE2C3AF17DA24EA8A944BF1D394FB5BC}

* When *`trackExternalLinks`* is 'false,' links that take people away from your site are likely to be under reported in visitor click map.
* When *`trackExternalLinks`* is 'true,' data is sent each time a visitor clicks on an exit link (before link target loads).

## s.trackInlineStats {#concept_E3A811D9761E4917935F6CD9059C7FCC}

<!-- 
trackInlineStats.xml
-->

 변수는 ClickMap 데이터가 수집되는지 여부를 결정합니다. 

If *`trackInlineStats`* is 'true,' data about the page and link clicked are stored in a cookie called s_sq. If 'false,' s_sq will have a value of "[[B]]," which is considered null.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | ClickMap | False |

**구문 및 가능한 값** {#section_46B2C1DD0D104A01A9C239929420CD90}

```
js
s.trackInlineStats=true|false
```

*`trackInlineStats`변수는 'true' 또는 'false'입니다.*

**예** {#section_F146770917A3493AB8007626913CD6AB}

```js
s.trackInlineStats=true
```

```js
s.trackInlineStats=false
```

**구성 설정** {#section_FB2CDB07CDCE454786D96A66E4D8EDCD}

없음

## s.linkDownloadFileTypes {#concept_06CC14C69DFD4887A5E6967A157A9E05}

<!-- 
linkDownloadFileTypes.xml
-->

 변수는 쉼표로 구분된 확장자 목록입니다.

사이트에 이러한 확장자를 가진 파일에 대한 링크가 포함된 경우 해당 링크의 URL이 [!UICONTROL 파일 다운로드] 보고서에 나타납니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | N/A | 트래픽 &gt; 사이트 트래픽 &gt; 파일 다운로드 | "exe, zip, wav, mp3, mov, mpg, avi, wmv, doc, pdf, xls" |

the *`linkDownloadFileTypes`* 변수는'true'로 설정된 경우에만 *`trackDownloadLinks`* 관련 있습니다.

링크를 마우스 왼쪽 단추로 클릭해야만 [!UICONTROL 파일 다운로드] 보고서에서 계산됩니다. 페이지가 로드될 때 자동으로 시작되거나, 리디렉션 후에만 다운로드되는 모든 파일 다운로드는 [!UICONTROL 파일 다운로드] 보고서에서 계산되지 않습니다. 파일을 마우스 오른쪽 단추로 클릭하고 "다른 이름으로 대상 저장..." 옵션을 선택하면, [!UICONTROL 파일 다운로드] 보고서에서 계산되지 않습니다.

the *`linkDownloadFileTypes`*&#x200B;변수를 사용하여 RSS 피드 클릭을 추적할 수 있습니다. If you have links to RSS feeds with a .xml or other extension, appending ",xml" to the *`linkDownloadFileTypes`* list allows you to see how often each RSS link is clicked.

**구문 및 가능한 값** {#section_E0B3F3817BBF4B11AFAABEF8BB951E5A}

파일 확장자만 포함(공백 없음).

```js
s.linkDownloadFileTypes="type1[,type2[,type3[...]]]"
```

모든 확장자를 목록에 포함할 수 있습니다. htm 또는 aspx와 같은 일반적인 파일 확장자가 *`linkDownloadFileTypes`*. 클릭할 때마다 추가 이미지 요청이 전송되어 주 서버 호출로 청구될 수 있습니다.

**예** {#section_C53F1AF768434CEBA65F3D255BC470AD}

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls"
```

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls,xml"
```

**구성 설정** {#section_CE24D5852E4D441A958A4EDDB82382A7}

없음

**함정, 질문 및 팁** {#section_786CF22D5553429EB6524B13774793BC}

* 다운로드 파일을 마우스 왼쪽 단추로 클릭한 경우에만 [!UICONTROL 파일 다운로드 보고서]에 URL이 나타납니다.
* 일반 파일 확장자를 *`linkDownloadFileTypes`* 에 포함하면 Adobe 서버로 전송되는 전체 서버 호출이 심각하게 증가할 수 있습니다.
* 파일 확장자가 *`linkDownloadFileTypes`*.
* JavaScript를 사용하는 링크(즉, javascript:openLink( ))는 파일 다운로드에서 카운트되지 않습니다.

## s.linkInternalFilters {#concept_D53C1186762E4AAE82451712B0801CAD}

<!-- 
linkInternalFilters.xml
-->

 변수는 사이트에서 어느 링크가 종료 링크인지를 확인하는 데 사용됩니다.

사이트에 속한 링크를 나타내는 필터들이 쉼표로 구분되어 있는 목록입니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 경로 &gt; 시작 및 종료 &gt; 종료 링크 |  |

>[!NOTE]
>
>이전에는 Linkinternalfilters를 javascript로 설정하는 것을 제안했습니다. 그러나 이로 인해 태그가 상주하는 현재 도메인을 포함하여 모든 도메인이 외부로 간주됩니다. 여러 도메인을 내부로 간주하려면 아래 예제에 표시된 것처럼 그러한 도메인을 추가할 수 있습니다.

*`linkInternalFilters`* 변수는 링크가 종료 링크인지 확인하는 데 사용됩니다. 종료 링크는 방문자를 사이트에서 보내는 링크로 정의됩니다. 종료 링크의 대상 창이 팝업과 기존 창 중 어느 것인지는 종료 링크 보고서에 링크가 표시되는지 여부에 영향을 주지 않습니다. 종료 링크는 *`trackExternalLinks`* 가 `"true"`. DTM이 종료 링크를 처리하는 방법에 대한 자세한 내용은 동적 태그 관리 문서에서 [링크 추적](https://marketing.adobe.com/resources/help/en_US/dtm/link_tracking.html)을 참조하십시오. The filters in *`linkInternalFilters`* are not case-sensitive.

The list of filters in *`linkInternalFilters`* applies to the domain and path of any link by default. If *`linkLeaveQueryString`* is set to `"true"`, then the filters apply to the entire URL (domain, path, and query string). 필터는 href 값에 상대 경로를 사용한 경우라도 항상 URL의 절대 경로에 적용됩니다.

사이트의 모든 도메인(및 사용자의 JavaScript 파일을 사용하는 모든 파트너)이 *`linkInternalFilters`*. 목록에 일부 도메인이 포함되지 않은 경우, 이러한 도메인으로 연결되거나 도메인에 있는 모든 링크가 종료 링크로 간주되어 전송되는 서버 호출을 증가시킵니다. If you would like multiple domains or companies to use a single [!DNL AppMeasurement] for JavaScript file, you may consider populating *`linkInternalFilters`* on the page, overriding the value specified in the JavaScript file. 주 도메인에 직접 연결되는 부속 도메인이 있는 경우에는 부속 도메인(vanity domain)을 목록에 포함시킬 필요가 없습니다.

다음 예에서는 이 변수의 사용 방법을 설명합니다. In this example, the URL of the page is `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="mysite.com" 
s.linkExternalFilters="" 
s.linkLeaveQueryString=false 
... 
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Exit Link</a> 
<a href="https://www2.site1.com/partners/">Exit Link</a> 
```

**구문 및 가능한 값** {#section_810966F09912415B96EA9C2EDAE0CEA0}

*`linkInternalFilters`* 변수는 쉼표로 구분된 ASCII 문자 목록입니다. 공백은 허용되지 않습니다.

```js
s.linkInternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

**예** {#section_491F48556DC247889D54C66FC431B4EC}

```js
s.linkInternalFilters="mysite.com"
```

```js
s.linkInternalFilters="mysite.com,mysite.net,vanity1.com"
```

**구성 설정** {#section_546AC1FACB664ABFBCF312990097C987}

없음

**함정, 질문 및 팁** {#section_E83A6F8B6EE44D51A2800D83F8BB264F}

* Include all domains that the [!DNL AppMeasurement] for JavaScript file may be served under in the filter list.
* [!UICONTROL [경로]] &gt; [!UICONTROL [시작 및 종료]] &gt; [!UICONTROL [종료]] 링크 보고서에 있는 항목 중에서 잘못된 항목이 없는지 주기적으로 확인하십시오.

* 파트너 계약을 주기적으로 검토하여 파트너 계약에 링크 추적에 대한 제한 사항이 있는지 파악하십시오. 예를 들어 파트너 디스플레이 광고에 나타나는 링크를 추적하는 것이 금지되었을 수 있습니다. 도메인을 *`linkInternalFilters`*:

```js
s.linkInternalFilters="mysite.com,mysite.net,mypartner.net/adclick"
```

## s.linkLeaveQueryString {#concept_118C280E29394DB5A16DBBF41EB4D742}

<!-- 
linkLeaveQueryString.xml
-->

기본적으로 쿼리 문자열은 모든 보고서에서 제외됩니다.

일부 종료 링크 및 다운로드 링크의 경우 다음 샘플 URL에서와 같이 URL의 중요한 부분이 쿼리 문자열에 있을 수도 있습니다.

```js
https://www.mycompany.com/download.asp?filename=myfile.exe
```

다운로드 파일 이름은 쿼리 문자열에서 정의할 수 있으므로, [!UICONTROL 파일 다운로드] 보고서를 더 정확하게 만들려면 쿼리 문자열이 필요합니다.

the *`linkLeaveQueryString`* 변수는 [!UICONTROL 종료 링크] 및 [!UICONTROL 파일 다운로드] 보고서에 쿼리 문자열을 포함해야 하는지 여부를 결정합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | N/A | 종료 링크 파일 다운로드 | false |

>[!NOTE]
>
>Setting `linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.

**구문** {#section_C40CF036B71A496D92574C6E46DE8302}

```js
s.linkLeaveQueryString=[false/true]
```

**예** {#section_E42CEC8DDE624A4B979F4F6C8094A7F9}

```js
s.linkLeaveQueryString=false
```

**가능한 값** {#section_E13211451B664B909B1BFDD050472F18}

```js
s.linkLeaveQueryString=false
```

```js
s.linkLeaveQueryString=true
```

**구성 설정** {#section_835FD74D3CA9425A9D091CACF88A6F1F}

이 변수에는 구성이 필요하지 않습니다.

**함정, 질문 및 팁** {#section_085E79D1A7F74F5D95F82D34FB82AEC4}

* Setting `s.linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.
* `linkLeaveQueryString` 이 변수는 기록된 페이지 URL, 방문자 클릭 맵 또는 [!UICONTROL 경로] 보고서에 영향을 주지 않습니다.

## s.linkTrackVars {#concept_A6B117826C15402EBD0781A94C8065B9}

<!-- 
linkTrackVars.xml
-->

 변수는 사용자 지정, 종료 및 다운로드 링크와 함께 전송되는, 쉼표로 구분되는 변수 목록입니다.

If *`linkTrackVars`* is set to "", all variables that have values are sent with link data. To avoid inflation of instances or page views associated with other variables, Adobe recommends populating *`linkTrackVars`* and *`linkTrackEvents`* in the [!UICONTROL onClick] event of a link that is used for link tracking.

링크 데이터(사용자 지정, 종료 및 다운로드 링크)와 함께 보내야 하는 모든 변수는 *`linkTrackVars`*. If *`linkTrackEvents`* is used, *`linkTrackVars`* should contain "events."

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 임의 | "없음" |

채울 때 *`linkTrackVars`*&#x200B;매개 변수에's.' 접두사를 사용하지 마십시오. For example, instead of populating *`linkTrackVars`* with "s.prop1," you should populate it with "prop1." The following example illustrates how *`linkTrackVars`* should be used.

```js
s.linkTrackVars="eVar1,events" 
s.linkTrackEvents="event1" 
s.events="event1" 
s.eVar1="value A" 
s.eVar2="value B" 
s.t() // eVar1, event1 and event2 are recorded 
<a href="https://google.com">event1 and eVar1 are recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.eVar1='value C';s.events='';s.tl(this,'o')">eVar1 is recorded</a> 
```

google.com에 연결된 링크는 종료 링크(Google을 사용하지 않는 경우)이므로, event1과 eVar1이 종료 링크 데이터와 함께 보내져서, eVar1과 연결된 인스턴스와 event1이 실행되는 횟수를 증가시킵니다. In the link to [!DNL test.php], [!UICONTROL eVar1] is sent with a value of 'value C' because that is the current value of [!UICONTROL eVar1] at the time that *`tl()`* is called.

**구문 및 가능한 값** {#section_DCC239F5CFE74959856764DAB1862BA7}

*`linkTrackVars`* 변수는 개체 이름 접두사가 없는 대소문자를 구분하는 쉼표로 구분된 변수 이름 목록입니다. 's.eVar1' 대신 'eVar1'을 사용하십시오.

```js
s.linkTrackVars="variable_name[,variable_name[...]]"
```

the *`linkTrackVars`* 변수에는 [!DNL Analytics]*`events`**`campaign`**`purchaseID`,**`products`* Evar 1-75[!UICONTROL , ]prop 1-75[!UICONTROL , ]hier 1-5*`channel`**`server`**`state`,**`zip`및**`pageType`.*

**예** {#section_546BAAC7373A41BF8583B280EAAB607C}

```js
s.linkTrackVars="events,prop1,eVar49"
```

```js
s.linkTrackVars="products"
```

**구성 설정** {#section_E387604B8A434A7F89A82A886649A89D}

없음

**함정, 질문 및 팁** {#section_99E0783A608C4462945F35D21AB4AC2B}

* If *`linkTrackVars`* is blank, all variables that have values are tracked with all server calls.
* Any variable listed in *`linkTrackVars`* that has a value at the time of any download, exit, or custom link, are tracked.
* If *`linkTrackEvents`* is used, *`linkTrackVars`* must contain "events."

* 변수에 "s." 또는 "s_objectname." 접두사를 사용하지 마십시오.

## s.linkTrackEvents {#concept_34D029097A674D0A97690C9569590EF5}

<!-- 
linkTrackEvents.xml
-->

The  variable is a comma-separated list of events that are sent with a [!UICONTROL custom], [!UICONTROL exit], or [!UICONTROL download] link.

If an event is not in *`linkTrackEvents`*, it is not sent to [!DNL Analytics], even if it is populated in the [!UICONTROL onClick] event of a link, as shown in the following example:

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

[!DNL help.php]에 연결된 첫 번째 링크를 보면 이벤트 변수가 링크를 누르기 전에 설정되었던 값을 유지함을 알 수 있습니다. 이렇게 되면 사용자 지정 링크로 event1을 보낼 수 있습니다. 두 번째 예인 [!DNL test.php]에 연결된 링크에서는 event2가 *`linkTrackEvents`*.

To avoid confusion and potential problems, Adobe recommends populating *`linkTrackVars`* and *`linkTrackEvents`* in the [!UICONTROL onClick] event of a link that is used for link tracking.

The *`linkTrackEvents`* variable contains the events that should be sent with [!UICONTROL custom], [!UICONTROL download], and [!UICONTROL exit] links. This variable is only considered if *`linkTrackVars`* contains "events."

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 전환 | "없음" |

**구문 및 가능한 값** {#section_89BA2425FBDC400A8C8B7FCDE7D67D63}

*`linkTrackEvents`* 변수는 쉼표로 구분된 이벤트 목록 (공백 없음) 입니다.

```js
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

 *`linkTrackEvents`*. These events are listed in [Events](../../../implement/js-implementation/c-variables/page-variables.md#concept_FFD115543D54401B98FE683BD7D5B3FE). 이벤트 이름의 앞이나 뒤에 공백이 있으면, 이벤트를 링크 이미지 요청으로 보낼 수 없습니다.

**예** {#section_AB7F952E522A4DCC92944EBF74C26BDD}

```js
s.linkTrackEvents="purchase,event1"
```

```js
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

**구성 설정** {#section_D938A47346D94A0C9E98FB327F2EF349}

없음

**함정, 질문 및 팁** {#section_DBB68BECC9D44380816113DB2566C38C}

* The JavaScript file only uses *`linkTrackEvents`* if *`linkTrackVars`* contains the "events" variable. "events" should be included in *`linkTrackVars`* only when *`linkTrackEvents`* is defined.

* 페이지에서 이벤트가 실행되어 *`linkTrackEvents`*. That event is recorded again with any [!UICONTROL exit], [!UICONTROL download], or [!UICONTROL custom] links unless the events variable is reset prior to that event (in the [!UICONTROL onClick] of a link or after the call to the *`t()`* function).

* If *`linkTrackEvents`* contains spaces between event names, the events are not recorded.

## s.linkExternalFilters {#concept_92A59169DCE443EBAE81A373B27BB6DD}

<!-- 
linkExternalFilters.xml
-->

사이트에 외부 사이트에 대한 링크가 많이 포함되어 있으며 일부 종료 링크만 추적하려는 경우, 특정 일부 종료 링크에 대해 보고하는 데 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 경로 &gt; 시작 및 종료 &gt; 종료 링크 | "" |

the *`linkExternalFilters`* 변수는 링크가 종료 링크인지 여부를 결정하기 *`linkInternalFilters`* 위해 함께 사용되는 선택적 변수입니다. 종료 링크는 방문자를 사이트 외부로 보내는 링크로 정의됩니다. 종료 링크의 대상 창이 팝업과 기존 창 중 어느 것인지는 종료 링크 보고서에 링크가 표시되는지 여부에 영향을 주지 않습니다. 종료 링크는 *`trackExternalLinks`* 가'true'로 설정되어 있어야 합니다. The filters in *`linkExternalFilters`* and *`linkInternalFilters`* are case insensitive.

>[!NOTE]
>
>If you don't want to use *`linkExternalFilters`*, delete it or set it to "".

The filters list in *`linkExternalFilters`* and *`linkInternalFilters`* apply to the domain and path of any link by default. If *`linkLeaveQueryString`* is set to 'true,' the filters apply to the entire URL (domain, path, and query string). 이러한 필터는 href 값에 상대 경로를 사용한 경우라도 항상 URL의 절대 경로에 적용됩니다.

대부분의 회사는 *`linkInternalFilters`* 가 종료 링크를 충분히 제어할 수 있도록 해주므로 *`linkExternalFilters`*. Using *`linkExternalFilters`* simply decreases the likelihood that an exit link is considered external. If *`linkExternalFilters`* has a value, then a link is considered only external if it does not match *`linkInternalFilters`* and does match *`linkExternalFilters`*.

다음 예에서는 이 변수의 사용 방법을 설명합니다. In this example, the URL of the page is `https://www.mysite.com/index.html`.

```js
s.trackExternalLinks=true 
s.linkInternalFilters="javascript:,mysite.com" 
s.linkExternalFilters="site1.com,site2.com,site3.com/partners" 
s.linkLeaveQueryString=false 
... 
<a href="https://www.mysite.com">Not an Exit Link</a> 
<a href="/careers/job_list.html">Not an Exit Link</a> 
<a href="https://www2.site3.com">Not an Exit Link</a> 
<a href="https://www.site1.com">Exit Link</a> 
<a href="https://www2.site3.com/partners/offer.asp">Exit Link</a> 
```

**구문 및 가능한 값** {#section_E35DAAAE8BDE44CEB8F6763EF1344693}

*`linkExternalFilters`* 변수는 쉼표로 구분된 ASCII 문자 목록입니다. 공백은 허용되지 않습니다.

```js
s.linkExternalFilters="site1.com[,site2.com[,site3.net[...]]]"
```

URL의 어떤 부분이든 *`linkExternalFilters`*&#x200B;를 쉼표로 구분하여 구분합니다.

**예** {#section_1D2F13EEC28942868C2F4207ADF2DDE0}

```js
s.linkExternalFilters="partnersite.com,partnertwo.net/path/"
```

```js
s.linkExternalFilters=""
```

**구성 설정** {#section_2D0CA911855B4B3698145FC18D5021C3}

없음

**함정, 질문 및 팁** {#section_8B40E6F539E3473B934A8DB7C5086D73}

* Using *`linkExternalFilters`* can result in fewer links on your site being exit links. Do not use this variable in place of *`linkInternalFilters`* to force internal links to become exit links.

* If *`linkExternalFilters`* should be applied to the query string of a link, make sure *`linkLeaveQueryString`* is set to 'true.' See [linkLeaveQueryString](../../../implement/js-implementation/c-variables/configuration-variables.md#concept_118C280E29394DB5A16DBBF41EB4D742) before setting to `"true"`.

* To disable exit link tracking, set *`trackExternalLinks`* to `"false"`.

## s.usePlugins {#concept_81836470A25C41228CE04084565F667D}

<!-- 
s_usePlugins.xml
-->

If the  function is available and contains useful code, [!UICONTROL s_usePlugins] should be set to 'true.'

[!UICONTROL Useplugins] 가'true'이면 이 함수는 *`s_doPlugins`* 각 이미지 요청에 앞서 호출됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | True |

**구문 및 가능한 값** {#section_BAD0F150047A4B7FB1214491B939A1FC}

```js
s.usePlugins=true|false
```

[!UICONTROL usePlugins] 변수는 'true' 또는 'false'입니다.

**예** {#section_1423CC3026384B1A9F78B272166B1DF5}

```js
s.usePlugins=true
```

```js
s.usePlugins=false
```

The [!UICONTROL usePlugins] variable should only be false (or not declared) if the *`s_doPlugins`* function is not declared in your JavaScript file.

**구성 설정** {#section_DFD41717134147E988B6AFC7DE5BB9E3}

없음