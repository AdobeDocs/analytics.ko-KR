---
title: JavaScript용 AppMeasurement를 사용하여 Adobe Analytics 구현
description: 태그 관리 시스템 없이 JavaScript를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
feature: Implementation Basics
source-git-commit: aef1d613437688b7eed704b227c41e4fbe4677dd
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 58%

---

# JavaScript용 AppMeasurement를 사용하여 Adobe Analytics 구현

AppMeasurement for JavaScript는 지금까지 Adobe Analytics를 구현하는 일반적인 방법이었습니다. 그러나 태그 관리 시스템의 인기가 높아짐에 따라 [Adobe Experience Platform의 태그](../launch/overview.md)를 사용하는 것이 권장됩니다.

구현 작업에 대한 개략적인 개요:

![AppMeasurement를 사용한 Adobe 분석 구현 개요](../assets/appmeasurement-annotated.png)

<table>

<tr>
<th style="width:5%"></th><th style="width:75%"><b>작업</b></th><th style="width:20%"><b>추가 정보</b></th>
</tr>

<tr>
<td>1</td><td><b>보고서 세트를 정의</b>했는지 확인합니다</td><td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">보고서 세트 관리자</a></td>
</tr>

<tr>
<td>2</td><td><b>AppMeasurement에 필요한 JavaScript 코드 다운로드</b> 코드 관리자에서. 파일의 압축을 풉니다.</td><td><a href="../../admin/admin/code-manager-admin.md">코드 관리자</a></td>
</tr>

<tr>
<td>3</td><td><b>추가 <code>AppMeasurement.js</code> 웹 사이트의 템플릿 파일에</b>. 이 코드에는 데이터를 Adobe에 보내는 데 필요한 라이브러리가 포함되어 있습니다.

```html
<head>
  <script src="AppMeasurement.js"></script>
  …
</head>
```

</td><td></td>
</tr>

<tr>
<td>4</td><td><b><code>AppMeasurement.js</code></b> 내에서 구성 변수를 정의하십시오. Analytics 개체가 인스턴스화될 때 이러한 변수는 데이터 수집 설정이 올바른지 확인합니다.

```JavaScript
// Instantiate the Analytics tracking object with report suite ID
var s_account = "examplersid";
var s=s_gi(s_account);
 
// Make sure data is sent to the correct tracking server
s.trackingServer = "example.data.adobedc.net";
```

</td><td><a href="../vars/config-vars/configuration-variables.md">구성 변수</a></td>
</tr>

<tr>
<td>5</td><td><b>사이트의 페이지 코드 내에서 페이지 수준 변수를 정의하십시오</b>. 이 변수가 Adobe에 전송되는 특정 차원과 지표를 결정합니다.

```js
s.pageName = "Example page";
s.eVar1 = "Example eVar";
s.events = "event1";
```

</td><td><a href="../vars/page-vars/page-variables.md">페이지 변수</a></td>
</tr>

<tr>
<td>6</td><td><b>다음을 사용하여 Adobe에 데이터 보내기 <code>t()</code> 방법</b>: 모든 페이지 변수가 정의된 경우입니다.

```js
s.t();
```

</td><td><a href="../vars/functions/t-method.md">t() 메서드</a></td>
</tr>

<tr>
<td>7</td><td>프로덕션으로 푸시하기 전에 <b>구현을 확장하고 유효성을 검사</b>합니다.</b></td><td></td>
</tr>

</table>

## 추가 리소스

- [변수, 함수, 메서드 및 플러그인 개요](../vars/overview.md)
