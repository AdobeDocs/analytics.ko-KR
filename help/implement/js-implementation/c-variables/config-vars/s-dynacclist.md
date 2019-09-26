---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicAccountList

[!DNL AppMeasurement] for JavaScript는 데이터를 전송하는 보고서 세트를 동적으로 선택할 수 있습니다.  변수에는 대상 보고서 세트를 결정하는 데 사용할 규칙이 포함됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | "" |

이 변수는  and  variables. *`dynamicAccountSelection`**`dynamicAccountMatch`* The rules in  are applied if  is set to 'true,' and they apply to the section of the URL specified in .*`dynamicAccountList`**`dynamicAccountSelection`**`dynamicAccountMatch`*

If none of the rules in  matches the URL of the page, the report suite identified in  is used. *`dynamicAccountList`*`s_account` 이 변수에 나열된 규칙은 왼쪽에서 오른쪽 순서로 적용됩니다. 페이지 URL이 두 개 이상의 규칙에 일치하는 경우, 가장 왼쪽 규칙이 보고서 세트를 결정하는 데 사용됩니다. 그 결과, 더 일반적인 규칙이 목록의 오른쪽으로 이동합니다.

In the following examples, the page URL is  and  is set to true and  is set to `www.mycompany.com/path1/?prod_id=12345``dynamicAccountSelection`**`s_account``mysuitecom.`

| DynamicAccountList 값 | DynamicAccountMatch 값 | 데이터를 받는 보고서 세트 |
|---|---|---|
| `mysuite2=www2.mycompany.com;mysuite1=mycompany.com` | window.location.host | mysuite1 |
| "mysuite1=path4,path1;mysuite2=path2" | window.location.pathname | mysuite1, mysuite2 |
| "mysuite1=path5" | window.location.pathname | mysuitecom, mysuite1 |
| "myprodsuite=prod_id" | window.location.search?window.location.search:"?") | myprodsuite |

## 구문 및 가능한 값

The `dynamicAccountList`변수는 세미콜론으로 분리되는 이름=값 쌍(규칙) 목록입니다. 목록의 각 부분에는 다음 항목이 들어 있습니다.

* 하나 이상의 보고서 세트 ID(쉼표로 분리)
* 등호
* 하나 이상의 URL 필터(쉼표로 분리)

```js
s.dynamicAccountList=rs1[,rs2]=domain1.com[,domain2.com/path][;...]
```

문자열에는 공백 없이 표준 ASCII 문자만 사용해야 합니다.

## 예

```js
s.dynamicAccountList="mysuite2=www2.mycompany.com;mysuite1=mycompany.com"
```

```js
s.dynamicAccountList="ms1,ms2=site1.com;ms1,ms3=site3.com"
```

## 구성 설정

없음

## 함정, 질문 및 팁

* 다이내믹 계정 선택은 [JavaScript용 AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

* 페이지 URL이 여러 규칙을 만족하는 경우, 왼쪽 끝에 있는 규칙이 사용됩니다.
* 만족하는 규칙이 없을 경우에는 기본 보고서 세트가 사용됩니다.
* 페이지가 누군가의 하드 드라이브에 저장되거나 웹 기반 번역 엔진을 통해 번역되는 경우(Google의 번역된 페이지)에는, 동적 계정 선택 기능이 작동하지 않습니다. 더 정밀한 추적을 수행하려면, `s_account` 변수 서버측을 채우십시오.
* The `dynamicAccountSelection` rules apply only to the section of the URL specified in `dynamicAccountMatch`.

* When using dynamic account selection, be sure to update  every time you obtain a new domain.*`dynamicAccountList`*
* 대상 보고서 세트를 식별할 때 [!DNL DigitalPulse Debugger]를 사용하십시오. The `dynamicAccountSelection` variable always overrides the value of `s_account`.
