---
title: 통합 모듈
seo-title: Adobe Analytics 용 통합 모듈
description: Adobe 파트너는 통합 모듈을 사용하여 데이터 수집 활동을 조직과 통합할 수 있습니다.
seo-description: Adobe 파트너는 통합 모듈을 사용하여 데이터 수집 활동을 조직과 통합할 수 있습니다.
translation-type: tm+mt
source-git-commit: dae73042ace20eded9d0caf690a14203827f903a

---


# 통합 모듈

Adobe 파트너는 통합 모듈을 사용하여 데이터 수집 활동을 조직과 통합할 수 있습니다. 이 통합은 양방향 데이터 연결을 위한 기회를 제공합니다. 일반적으로 통합 모듈의 사용은 Adobe 파트너에 의해 이루어집니다.

> [!NOTE] 구현에서 파트너 데이터를 요청하면 페이지 로드 및 Adobe 데이터 수집 서버로 전송된 데이터 간의 지연 시간이 증가할 수 있습니다. 방문자가 데이터를 보내기 전에 새 페이지를 로드하는 경우 해당 페이지가 기록되지 않습니다.

## 통합 모듈 워크플로우

1. A visitor to your site loads a page that initiates a `get` request for partner data.
2. The Adobe partner receives the `get` request and packages the appropriate variables in a JSON object. JSON 개체가 반환됩니다.
3. Your site receives the JSON object and calls `setVars` to assign the information contained in the JSON object to Adobe Analytics variables
4. 이미지 요청이 Adobe 데이터 수집 서버로 전송됩니다.

## 통합 모듈 구현

Adobe 파트너와 협력하는 조직은 이러한 단계를 사용하여 통합 모듈 사용을 성공적으로 시작할 수 있습니다.

### 통합 모듈 코드 가져오기

모듈 코드를 입수하려면 제품 관리자 액세스 권한이 있거나 코드 관리자에 액세스할 수 있는 제품 프로필에 속해 있어야 합니다. 모듈 코드를 얻는 방법은 Adobe Experience Platform Launch를 포함한 모든 구현 방법에서 동일합니다.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
1. 오른쪽 상단의 9 개 사각형 아이콘을 클릭한 다음 컬러 분석 로고를 클릭합니다.
1. In the top navigation, click [!UICONTROL Admin] &gt; [!UICONTROL Code Manager].
1. 최신 JavaScript appmeasurement 라이브러리를 다운로드합니다.
1. Once downloaded, unzip the file and locate `AppMeasurement_Module_Integrate.js`.

### 구현에 통합 모듈 배치

사이트에서 통합 모듈을 구현하려면 Adobe Experience Platform Launch에 액세스해야 합니다. 기존 JavaScript 구현을 사용하는 경우 조직의 웹 사이트 소스 코드에 액세스할 수 있어야 합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your Adobe ID credentials.
2. 편집할 론치 속성을 클릭합니다.
3. 확장 탭을 클릭한 다음 Adobe Analytics 아래에서 구성을 클릭합니다.
4. ' 사용자 지정 코드 사용'아코디언을 연 다음 ' &lt;/&gt; 편집기 열기'를 클릭합니다.
5. 통합 모듈 코드를 코드 모달 창에 붙여넣습니다. 완료되면 저장을 클릭합니다.

## 통합 모듈 메서드

통합 모듈이 구현되면 이러한 방법을 사용하여 원하는 Adobe 파트너의 데이터를 보내고 받도록 구성합니다.

### 추가

The `add` method instantiates a partner object, which serves as an intermediate store of variable data when sharing data between partner systems and your implementation. 이 방법은 모든 통합에 필요합니다. 단일 구현에 여러 파트너가 사용되는 경우 각 고유 파트너에 대해 별도의 파트너 개체를 사용해야 합니다.

```JavaScript
s.Integrate.add("<partner_name>");
```

조직은 일반적으로 파트너 이름의 값을 결정하기 위해 Adobe 파트너와 협력합니다.

### 비콘

`beacon` 이 메서드는 이미지 요청을 만들어 지정된 URL로 가리킵니다. 이러한 이미지 요청은 표준 이미지 요청과 다릅니다. 비콘 메서드는 일반적으로 Adobe 데이터 수집 서버 대신 Adobe 파트너에게 데이터를 보냅니다.

```JavaScript
p.beacon("<partner_url>/track?qs1=value1&qs2=value2");
```

조직은 일반적으로 파트너 이름의 값을 결정하기 위해 Adobe 파트너와 협력합니다. URL에 포함된 쿼리 문자열은 선택 사항이며 파트너에 종속적입니다. 통합 모듈에는 브라우저 캐싱을 방지하기 위해 무작위 숫자가 포함된 쿼리 문자열이 자동으로 포함됩니다.

### 지연

Adobe는 내부적으로 팀과 협력하여 이 방법을 문서화하고 있습니다.

### get

The `get` method lets a client import partner variables and store them in the partner object. 파트너 개체에 데이터가 있으면 Analytics 변수에 할당되고 이미지 요청으로 전송할 수 있습니다. 이 메서드는 원하는 데이터를 포함하는 JSON 개체를 가리키는 URL를 호출합니다.

```JavaScript
s.Integrate.<partner_name>.get("<url_to_json_object>?pid=value1&pid2=value2");
```

* **파트너 이름:** 조직은 일반적으로 파트너 이름의 값을 결정하기 위해 Adobe 파트너와 협력합니다.
* **JSON 개체에 대한 URL:** 이미지 요청에 통합할 파트너 변수를 포함하는 JSON 개체의 URL 입니다.
* **쿼리 문자열 매개 변수:** 파트너 시스템에서 조직을 식별하는 파트너 계정 정보입니다. Adobe 파트너는 이 정보를 사용하여 데이터 세트를 식별합니다.

통합 모듈은 URL에 더 많은 쿼리 문자열을 자동으로 추가합니다. var 쿼리 문자열은 모듈에서 반환할 JSON 개체의 이름을 지정합니다. 브라우저 캐싱을 방지하기 위해 무작위 숫자가 추가됩니다.

### ready

Adobe는 내부적으로 팀과 협력하여 이 방법을 문서화하고 있습니다.

### Usevar

`useVars` 이 방법을 사용하면 클라이언트가 Adobe 파트너와 변수 값을 공유할 수 있습니다.

```JavaScript
s.Integrate.<partner_name>.useVars = function (s,p) {
    p.<partner_var1> = s.eVar1;
    p.<partner_var2> = s.eVar2;
}
```

조직은 일반적으로 파트너 이름과 파트너가 사용하는 변수에 대한 값을 결정하기 위해 Adobe 파트너와 협력합니다.

### Setvars

`setVars` 클라이언트는 이 방법을 사용하여 검색한 파트너 데이터를 사용하여 Analytics 변수를 채울 수 있습니다. Partner data can be the result of a `get` method, a static assignment, or any other mechanism that populates the partner object with data.

```JavaScript
s.Integrate.<partner_name>.setVars = function (s,p) {
    s.eVar1 = p.<partner_var1>;
    s.eVar2 = p.<partner_var2>;
}
```

조직은 일반적으로 파트너 이름과 파트너가 사용하는 변수에 대한 값을 결정하기 위해 Adobe 파트너와 협력합니다.

### 스크립트

`script` 이 방법을 사용하면 특정 조건이 충족되는 경우 (예: 캠페인 변수가 설정된 경우) Adobe 파트너가 파트너 사이트에서 추가 JavaScript를 호출할 수 있습니다.

```JavaScript
p.script("<partner_url>/script?qs1=value1&qs2=value2");
```

조직은 일반적으로 파트너 이름의 값을 결정하기 위해 Adobe 파트너와 협력합니다. URL에 포함된 쿼리 문자열은 선택 사항이며 파트너에 종속적입니다. 통합 모듈에는 브라우저 캐싱을 방지하기 위해 무작위 숫자가 포함된 쿼리 문자열이 자동으로 포함됩니다.
