---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 8c06a54ccd652f3f915af3af040e9cc69f01d0c1

---


# s.useForcedLinkTracking


 변수는 데이터를 저장 및 보고하는 보고서 세트를 결정합니다.

여러 보고서 세트(다중 세트 태깅)로 전송하는 경우 `s.account`는 쉼표로 구분된 값 목록일 수 있습니다. 보고서 세트 ID는 Adobe에 의해 결정됩니다.

## 매개 변수

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| 40바이트 | URL 경로에서 | N/A | N/A |

각 보고서 세트 ID는 [!DNL Admin Console]에서 생성한 값과 일치해야 합니다. 각 보고서 세트 ID는 40바이트 이하여야 하지만 모든 보고서 세트의 집계 정보(쉼표로 구분된 목록 전체)에는 제한이 없습니다.

보고서 세트는 보고에서 세그먼테이션의 가장 기본적인 수준입니다. 계약에서 허용하는 만큼 많은 보고서 세트를 설정할 수 있습니다. 각 보고서 세트는 Adobe의 수집 서버에서 채워지는 전용 테이블을 참조하십시오. 보고서 세트는 JavaScript 코드의 `s_account`변수로 식별됩니다. 

[!DNL Analytics] 내에서, 보고서의 왼쪽 상단에 있는 사이트 드롭다운 상자에는 현재 보고서 세트가 표시됩니다. 각 보고서 세트에는 보고서 세트 ID라는 고유 식별자가 있습니다. 변수 `s_account` 변수에는 데이터가 전송되는 하나 이상의 보고서 세트 ID가 포함되어 있습니다. [!DNL Analytics] 사용자에게 보이지 않는 보고서 세트 ID 값은 사용하기 전에 Adobe에서 제공 또는 승인 받아야 합니다. 모든 보고서 세트 ID에는 [!DNL Admin Console]의 보고서 세트 섹션에서 변경할 수 있는 연결된 "친숙한 이름"이 있습니다.

`s_account` 변수는 일반적으로 JavaScript 파일(s_code.js) 내에 선언됩니다. HTML 페이지에서 `s_account` 변수를 선언할 수 있습니다. 이 변수는 일반적으로 `s_account` 값이 페이지 간에 변경될 수 있을 때 사용합니다. `s_account` 변수는 범위가 전역적이기 때문에 Adobe의 JavaScript 파일을 포함하기 전에 바로 선언해야 합니다. JavaScript 파일이 로드될 때 `s_account`에 값이 없으면 데이터가 [!DNL Analytics]로 전송되지 않습니다.

Adobe의 [!DNL DigitalPulse Debugger]는 /b/ss/ 바로 뒤에 나오는 "Image"라는 단어 바로 아래에 표시되는 URL의 경로에 `s_account` 값을 표시합니다. 경우에 따라 `s_account` 값이 112.2o7.net 앞의 도메인에 표시됩니다. 경로의 값은 대상 보고서 세트를 결정하는 유일한 값입니다. 아래의 굵은 텍스트는 데이터를 전송 받는 보고서 세트가 디버거에 나타난 모습을 표시합니다. 자세한 내용은 [DigitalPulse Debugger](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/debugger.html).

```js
https://mycompany.112.207.net/b/ss/ 
<b>mycompanycom,mycompanysection</b>/1/H.1-pdv-2/s21553246810948?[AQB]
```

## 구문 및 가능한 값

보고서 세트 ID는 40바이트 길이 이하의 ASCII 영숫자 문자열입니다. 영숫자가 아닌 문자 중에서는 하이픈만 허용됩니다. 공백, 마침표, 쉼표 및 기타 구두점은 허용되지 않습니다. The `s_account` 에는 여러 보고서 세트가 포함될 수 있으며 이 모든 세트가 해당 페이지로부터 데이터를 받습니다.

```js
var s_account="reportsuitecom[,reportsuite2[,reportsuite3]]"
```

`s_account`의 모든 값은 Adobe가 제공하거나 승인해야 합니다.

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

* `s_account`가 비어 있거나, 선언되지 않았거나, 예기치 않은 값을 포함하는 경우 데이터가 수집되지 않습니다.
* `s_account` 변수가 쉼표로 구분된 목록(다중 세트 태그 지정)인 경우는 보고서 세트 ID 사이에 공백을 추가하지 마십시오.
* [!UICONTROL s.dynamicAccountSelection]이 *True*&#x200B;로 설정되면 URL을 사용하여 대상 보고서 세트를 결정합니다. [!DNL DigitalPulse Debugger]를 사용하여 수신처 보고서 세트를 결정하십시오.

* 일부 경우에, [!DNL VISTA]를 사용하여 수신처 보고서 세트를 변경할 수 있습니다. 자사 쿠키를 사용하거나 사이트에 활성 보고서 세트가 20개 이상 있는 경우, [!DNL VISTA]를 사용하여 데이터를 다시 전송하거나 다른 보고서 세트에 복사하는 것이 좋습니다.

* `s_account`는 항상 JS 파일 내부 또는 JS 파일을 포함하기 직전에 선언하십시오.
