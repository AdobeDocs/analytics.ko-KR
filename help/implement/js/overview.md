---
title: JavaScript용 AppMeasurement를 사용하여 Adobe Analytics 구현
description: 태그 관리 시스템 없이 JavaScript를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
feature: Implementation Basics
source-git-commit: 97e2cefbd8959f088d5f6e9923cad47b5414f38b
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 45%

---

# JavaScript용 AppMeasurement를 사용하여 Adobe Analytics 구현

AppMeasurement for JavaScript는 지금까지 Adobe Analytics를 구현하는 일반적인 방법이었습니다. 그러나 태그 관리 시스템의 인기가 높아짐에 따라 [Adobe Experience Platform의 태그](../launch/overview.md)를 사용하는 것이 권장됩니다.

구현 작업의 개요:

![AppMeasurement를 사용하여 Adobe 분석 구현 개요](../assets/appmeasurement-annotated.png)

<table>
<tr>
<td></td><td> <b>작업</b></td><td><b>추가 정보</b></td>
</tr>

<tr>
<td>1</td><td>다음을 확인하십시오 <b>보고서 세트 정의</b></td><td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">보고서 세트 관리자</a></td>
</tr>

<tr>
<td>2</td><td><b>AppMeasurement에 필요한 JavaScript 코드를 다운로드합니다</b> 코드 관리자에서. 파일의 압축을 해제합니다.</td><td><a href="../../admin/admin/code-manager-admin.md">코드 관리자</a></td>
</tr>

<tr>
<td>3</td><td><b>추가 <code>AppMeasurement.js</code> 웹 사이트의 템플릿 파일에 추가</b>. 이 코드에는 Adobe에 데이터를 전송하는 데 필요한 라이브러리가 포함되어 있습니다.

```html
<head>
  <script src="AppMeasurement.js"></script>
  …
</head>
```

</td><td></td>
</tr>

<tr>
<td>4</td><td><b><code>AppMeasurement.js</code></b> 내에서 구성 변수를 정의하십시오. Analytics 개체가 인스턴스화될 때 이 변수가 데이터 수집 설정이 올바른지 확인합니다.

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
<td>6</td><td><b>를 사용하여 데이터를 Adobe으로 보냅니다. <code>t()</code> 메서드</b>: 모든 페이지 변수가 정의된 경우

```js
s.t();
```

</td><td><a href="../vars/functions/t-method.md">t() 메서드</a></td>
</tr>

<tr>
<td>7</td><td><b>구현 확장 및 유효성 검사</b> 프로덕션에 투입하기 전에</b></td><td></td>
</tr>

</table>

## 추가 리소스

- [변수, 함수, 메서드 및 플러그인 개요](../vars/overview.md)
