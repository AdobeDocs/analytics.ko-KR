---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.charSet

일반적으로 JavaScript 파일에서 설정되는 charSet 속성은 Analytics에서 저장 및 보고를 위해 들어오는 데이터를 UTF-8로 변환하는 데 사용됩니다.

>[!N] 참고:charSet 속성은 데이터를 2바이트 보고서 세트로 보낼 때 필요하며 표준 보고서 세트와 함께 사용해서는 안 됩니다. 표준 ISO 보고서 세트와 함께 charSet 속성을 사용하면 변수가 잘리거나 예기치 않는 문자 변환이 일어날 수 있습니다.

구문은 약간 다를 수 있어도 charSet 속성 값은 META 태그 또는 http 헤더 안의 웹 페이지 인코딩과 일치해야 합니다. META 태그는 인코딩에 별칭을 사용할 수 있지만 charSet 값은 인코딩의 기본(또는 정식) 이름을 사용해야 합니다.

다음 표에 일부 인코딩의 기본 이름과 별칭이 요약되어 있습니다.

| 기본 이름 | 별칭 |
|--- |--- |
| ISO-8859-1 | ISO_8859-1,CP819,latin1 |
| ISO-8859-2 | ISO_8859-2,latin2 |
| ISO-8859-5 | ISO_8859-5,cyrillic |
| Big5 | Big-5 |
| Shift_JIS | SJIS |

인코딩과 별칭이 많이 있으므로 위의 표에 나타나지 않는 경우 구현 컨설턴트 또는 Adobe 고객 지원 센터에 문의하여 올바른 charSet 값을 확인하십시오.

If a site has different web encodings on different pages, or a single JavaScript file is used for multiple sites, the charSet property can be set to a default value in the JavaScript file and then reset on specific pages as needed to override the default; for example, `s.charSet="UTF-8"` or `s.charSet="SJIS"`.

공백이 아닌 모든 charSet 매개 변수 값에 따라 데이터가 저장을 위해 UTF-8로 변환됩니다. 128-255 범위의 문자가 적절한 UTF-8 2바이트 시퀀스로 변환되어 저장됩니다. 이러한 문자는 표준 보고서 세트에서 올바로 표시되지 않습니다. 따라서 charSet 속성을 표준 보고서 세트와 함께 사용해서는 안 됩니다.

마찬가지로 공백인 charSet 매개 변수는 데이터 변환 프로세스를 무시하고 128-255 범위의 모든 문자를 1바이트로 저장합니다. 이러한 문자는 2바이트 보고서 세트에서 올바로 표시되지 않는데, 그 이유는 해당 문자의 1바이트 코드가 유효한 UTF-8이 아니기 때문입니다. 따라서 charSet 매개 변수는 항상 2바이트 보고서 세트와 함께 사용해야 합니다. 또한 웹 페이지 인코딩에 적합한 값을 사용해야 합니다.

If the *`charSet`* variable contains an incorrect value, the data in all other variables are translated incorrectly. If JavaScript variables on your pages (e.g. *`pageName`*, [!UICONTROL prop1], or *`channel`*) contain only ASCII characters, *`charSet`* does not need to be defined. 그러나 페이지의 변수에 비ASCII 문자가 포함되어 있으면 *`charSet`* 변수를 채워야 합니다.

## 매개 변수

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | CE | N/A | "" |

## 구문 및 가능한 값

```js
s.charSet="character_set"
```

## 예

```js
s.charSet="ISO-8859-1"
```

```js
s.charSet="SJIS"
```
