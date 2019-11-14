---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# visitorNamespace

 변수는 쿠키가 설정된 도메인을 식별하는 데 사용됩니다.

<!-- 

visitorNamespace.xml

 -->

*`visitorNamespace`*&#x200B;를 JavaScript 파일에서 사용한 경우 삭제하거나 바꾸지 마십시오. *`visitorNamespace`*&#x200B;가 변경되면 Analytics에 보고된 모든 방문자가 새 방문자가 될 수 있습니다. 방문자 내역은 현재 및 미래 트래픽에서 연결성이 없어집니다. 따라서 Adobe 담당자의 승인 없이 이 변수를 바꾸지 마십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | ns | N/A | "" |

Analytics는 쿠키를 사용하여 사이트 방문자를 고유하게 식별합니다. *`visitorNamespace`*&#x200B;를 사용하지 않으면 쿠키가 2o7.net에 연결됩니다. *`visitorNamespace`*&#x200B;를 사용하면 쿠키가 2o7.net의 하위 도메인에 연결됩니다. 사이트의 모든 방문자는 같은 도메인 또는 하위 도메인에 쿠키를 연결해야 합니다.

The reason of use the *`visitorNamespace`*&#x200B;변수를 사용하는 이유는 브라우저의 쿠키 제한을 초과하지 않도록 하기 위한 것입니다. Internet Explorer에서는 도메인당 쿠키를 20개로 제한하고 있습니다. JavaScript를 *`visitorNamespace`* 변수를 사용하면, 다른 회사의 Analytics 쿠키가 사이트 방문자의 쿠키와 충돌하지 않게 됩니다.

**구문 및 가능한 값** {#section_EE247FE371784CA4B6058182181F3EA1}

*`visitorNamespace`*&#x200B;의 값은 Adobe가 제공해야 하며, 쉼표, 마침표, 공백 또는 특수 문자가 포함되지 않은 ASCII 문자로 이루어진 문자열이어야 합니다.

```js
s.visitorNamespace="company_specific_value"
```

**보고서 세트 간 방문자 식별** {#section_7AC5A97FC8C045DD8850245A62BB09F4}

`visitorNamespace`를 지정하지 않는 경우 회사에 있는 각 보고서 세트는 `s_vi_[random string]`로 작성된 자체 방문자 ID 쿠키를 받습니다. `visitorNamespace`를 지정하는 경우에는, 지정된 `s_vi`에 데이터를 보내는 모든 보고서 세트에 대해 동일한 `trackingServer` 쿠키가 사용됩니다. 다중 세트 태깅을 구현한 경우에는 반드시 각 보고서 세트에서 동일한 쿠키를 사용하도록 방문자 네임스페이스를 지정하십시오.

**예** {#section_89A95852AB9446E794AD3283B8800B09}

```js
s.visitorNamespace="company_name"
```

```js
s.visitorNamespace="Adobe"
```

**구성 설정** {#section_1128A2531ECC43DFA6749ECC21F050A2}

없음
