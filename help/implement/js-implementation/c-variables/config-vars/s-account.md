---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 4a6bac589d1d6d6caaf34dc5363c60bbfbb952d5

---


# s.account

 변수는 데이터를 저장 및 보고하는 보고서 세트를 결정합니다.

If sending to multiple report suites (multi-suite tagging), `s.account` may be a comma-separated list of values. 보고서 세트 ID는 Adobe에 의해 결정됩니다.

## 매개 변수

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| 40바이트 | URL 경로에서 | N/A | N/A |

Each report suite ID must match the value created in the [!DNL Admin Console]. 각 보고서 세트 ID는 40바이트 이하여야 하지만 모든 보고서 세트의 집계 정보(쉼표로 구분된 목록 전체)에는 제한이 없습니다.

보고서 세트는 보고에서 세그먼테이션의 가장 기본적인 수준입니다. 계약에서 허용하는 만큼 많은 보고서 세트를 설정할 수 있습니다. 각 보고서 세트는 Adobe의 수집 서버에서 채워지는 전용 테이블을 참조하십시오. 보고서 세트는 JavaScript 코드의 `s_account`변수로 식별됩니다. 

[!DNL Analytics] 내에서, 보고서의 왼쪽 상단에 있는 사이트 드롭다운 상자에는 현재 보고서 세트가 표시됩니다. 각 보고서 세트에는 보고서 세트 ID라는 고유 식별자가 있습니다. 변수 `s_account` 변수에는 데이터가 전송되는 하나 이상의 보고서 세트 ID가 포함되어 있습니다. [!DNL Analytics] 사용자에게 보이지 않는 보고서 세트 ID 값은 사용하기 전에 Adobe에서 제공 또는 승인 받아야 합니다. Every report suite ID has an associated "friendly name" that can be changed in the report suites section of the [!DNL Admin Console].

The `s_account` variable is normally declared inside the JavaScript file (s_code.js). HTML 페이지에서 `s_account` 변수를 선언할 수 있습니다. 이 방법은 값이 페이지에서 페이지로 변경될 `s_account` 수 있는 일반적인 방법입니다. Because the `s_account` variable has a global scope, it should be declared immediately before including Adobe's JavaScript file. If `s_account` does not have a value when the JavaScript file is loaded, no data is sent to [!DNL Analytics].

Adobe's [!DNL DigitalPulse Debugger] displays the value of `s_account` in the path of the URL that appears just below the word "Image," just after /b/ss/. 경우에 따라 의 값이 112.2o7.net 이전의 도메인에 `s_account` 표시됩니다. 경로의 값은 대상 보고서 세트를 결정하는 유일한 값입니다. 아래의 굵은 텍스트는 데이터를 전송 받는 보고서 세트가 디버거에 나타난 모습을 표시합니다. 자세한 내용은 [DigitalPulse Debugger](/help/implement/impl-testing/debugger.md).

```js
https://mycompany.112.207.net/b/ss/ 
<b>mycompanycom,mycompanysection</b>/1/H.1-pdv-2/s21553246810948?[AQB]
```

## 구문 및 가능한 값

보고서 세트 ID는 40바이트 길이 이하의 ASCII 영숫자 문자열입니다. 영숫자가 아닌 문자 중에서는 하이픈만 허용됩니다. 공백, 마침표, 쉼표 및 기타 구두점은 허용되지 않습니다. The `s_account` 에는 여러 보고서 세트가 포함될 수 있으며 이 모든 세트가 해당 페이지로부터 데이터를 받습니다.

```js
var s_account="reportsuitecom[,reportsuite2[,reportsuite3]]"
```

의 모든 값은 Adobe가 제공하거나 승인해야 `s_account` 합니다.

## 예

```js
var s_account="mycompanycom"
```

```js
var s_account="mycompanycom,mycompanysection"
```

## Analytics의 변수 구성

각 보고서 세트 ID와 연결된 친숙한 이름은 Adobe [!DNL Customer Care]에서 변경할 수 있습니다. 친숙한 이름은 [!DNL Analytics] 상단의 화면 왼쪽 섹션에 있는 사이트 드롭다운 상자에서 확인할 수 있습니다.

## 함정, 질문 및 팁

* If `s_account` is empty, not declared, or contains an unexpected value, no data is collected.
* When the `s_account` variable is a comma-separated list (multi-suite tagging), do not put spaces between report suite IDs.
* If [!UICONTROL s.dynamicAccountSelection] is set to *True* the URL is used to determine the destination report suite. [!DNL DigitalPulse Debugger]를 사용하여 수신처 보고서 세트를 결정하십시오.

* 일부 경우에, [!DNL VISTA]를 사용하여 수신처 보고서 세트를 변경할 수 있습니다. 자사 쿠키를 사용하거나 사이트에 활성 보고서 세트가 20개 이상 있는 경우, [!DNL VISTA]를 사용하여 데이터를 다시 전송하거나 다른 보고서 세트에 복사하는 것이 좋습니다.

* Always declare `s_account` inside the JS file or just before it is included.
