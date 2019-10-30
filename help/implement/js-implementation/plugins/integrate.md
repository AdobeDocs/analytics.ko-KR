---
title: 모듈 통합
seo-title: Adobe Analytics용 모듈 통합
description: Adobe 파트너는 모듈 통합을 통해 데이터 수집 활동을 조직과 통합할 수 있습니다.
seo-description: Adobe 파트너는 모듈 통합을 통해 데이터 수집 활동을 조직과 통합할 수 있습니다.
translation-type: ht
source-git-commit: dae73042ace20eded9d0caf690a14203827f903a

---


# 모듈 통합

Adobe 파트너는 모듈 통합을 통해 데이터 수집 활동을 조직과 통합할 수 있습니다. 이 통합은 양방향 데이터 연결을 위한 기회를 제공합니다. 일반적으로 모듈 통합 사용은 Adobe 파트너에 의해 결정됩니다.

> [!NOTE] 구현에서 파트너 데이터를 요청하면 페이지 로드와 Adobe 데이터 수집 서버로 전송된 데이터 간의 지연이 늘어날 수 있습니다. 방문자가 데이터를 보내기 전에 새 페이지를 로드하면 해당 페이지가 기록되지 않습니다.

## 모듈 통합 워크플로우

1. 사이트 방문자는 파트너 데이터에 대한 `get` 요청을 시작하는 페이지를 로드합니다.
2. Adobe 파트너는 `get` 요청을 받고 JSON 개체에 적절한 변수를 패키지화합니다. JSON 개체가 반환됩니다.
3. 사이트에서는 JSON 개체를 수신하고 JSON 개체에 포함된 정보를 Adobe Analytics 변수에 할당하는 `setVars`를 호출합니다.
4. 이미지 요청이 Adobe 데이터 수집 서버로 전송됩니다.

## 모듈 통합 구현

Adobe 파트너와 협력하는 조직은 이러한 단계를 사용하여 모듈 통합을 성공적으로 사용할 수 있습니다.

### 모듈 통합 코드 얻기

모듈 코드를 얻으려면 사용자에게 제품 관리자 액세스 권한이 있거나 코드 관리자에 액세스할 수 있는 제품 프로필에 속해 있어야 합니다. 모듈 코드를 얻는 방법은 Adobe Experience Platform Launch를 비롯한 모든 구현 방법에 대해 동일합니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
1. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
1. 상단 탐색에서 [!UICONTROL 관리자] &gt; [!UICONTROL 코드 관리자]를 클릭합니다.
1. 최신 JavaScript AppMeasurement 라이브러리를 다운로드합니다.
1. 이 라이브러리가 다운로드되면 파일의 압축을 풀고 `AppMeasurement_Module_Integrate.js`를 찾습니다.

### 구현에 모듈 통합 배치

사이트에 모듈 통합을 구현하려면 Adobe Experience Platform Launch에 액세스해야 합니다. 기존 JavaScript 구현을 사용하는 경우 조직의 웹 사이트 소스 코드에 액세스해야 합니다.

1. Adobe ID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 편집할 Launch 속성을 클릭합니다.
3. 확장 탭을 클릭한 다음 Adobe Analytics 아래의 구성을 클릭합니다.
4. 먼저 '사용자 지정 코드를 사용하여 추적기 구성' 아코디언을 열고 '&lt;/&gt; 편집기 열기'를 클릭합니다.
5. 모듈 통합 코드를 코드 모달 창에 붙여넣습니다. 완료되면 저장을 클릭합니다.

## 모듈 통합 메서드

모듈 통합이 구현되었으면 원하는 다음 메서드를 사용하여 Adobe 파트너와 데이터를 주고 받을 수 있도록 구성합니다.

### add

`add` 메서드는 파트너 개체를 인스턴스화합니다. 이 개체는 파트너 시스템과 구현 사이에 데이터를 공유할 때 변수의 중간 저장소 역할을 합니다. 이 메서드는 모든 통합에 필요합니다. 여러 파트너가 단일 구현에 사용되는 경우 각각의 고유 파트너에 대해 별도의 파트너 개체를 사용해야 합니다.

```JavaScript
s.Integrate.add("<partner_name>");
```

일반적으로 조직은 Adobe 파트너와 함께 파트너 이름에 대한 값을 결정합니다.

### beacon

이 `beacon` 메서드는 이미지 요청을 만들고 지정된 URL을 가리킵니다. 이러한 이미지 요청은 표준 이미지 요청과 다릅니다. beacon 메서드는 일반적으로 Adobe 데이터 수집 서버 대신 Adobe 파트너에게 데이터를 전송합니다.

```JavaScript
p.beacon("<partner_url>/track?qs1=value1&qs2=value2");
```

일반적으로 조직은 Adobe 파트너와 함께 파트너 이름에 대한 값을 결정합니다. URL에 포함된 쿼리 문자열은 선택 사항이며, 파트너에 따라 다릅니다. 모듈 통합에는 브라우저 캐싱을 방지하기 위해 임의 숫자가 들어 있는 쿼리 문자열이 자동으로 포함됩니다.

### delay

Adobe는 이 메서드를 문서화하기 위해 내부적으로 팀과 협력하고 있습니다.

### get

이 `get` 메서드를 사용하면 클라이언트가 파트너 변수를 가져와 파트너 개체에 저장할 수 있습니다. 파트너 개체에 데이터가 있으면 Analytics 변수에 할당하고 이미지 요청에서 전송할 수 있습니다. 이 메서드는 원하는 데이터가 포함된 JSON 개체를 가리키는 URL을 호출합니다.

```JavaScript
s.Integrate.<partner_name>.get("<url_to_json_object>?pid=value1&pid2=value2");
```

* **파트너 이름:** 일반적으로 조직은 Adobe 파트너와 함께 파트너 이름에 대한 값을 결정합니다.
* **JSON 개체의 URL:** 이미지 요청에 통합할 파트너 변수가 들어 있는 JSON 개체의 URL입니다.
* **쿼리 문자열 매개 변수:** 파트너 시스템에서 조직을 식별하는 파트너 계정 정보입니다. Adobe 파트너는 이 정보를 사용하여 사용자의 데이터 세트를 식별합니다.

모듈 통합은 URL에 더 많은 쿼리 문자열을 자동으로 추가합니다. var 쿼리 문자열은 모듈이 파트너로부터 다시 기대하는 JSON 개체의 이름을 지정합니다. 브라우저 캐싱을 방지하기 위해 임의 번호도 추가됩니다.

### ready

Adobe는 이 메서드를 문서화하기 위해 내부적으로 팀과 협력하고 있습니다.

### useVars

이 `useVars` 메서드를 사용하면 클라이언트가 Adobe 파트너와 변수 값을 공유할 수 있습니다.

```JavaScript
s.Integrate.<partner_name>.useVars = function (s,p) {
    p.<partner_var1> = s.eVar1;
    p.<partner_var2> = s.eVar2;
}
```

일반적으로 조직은 Adobe 파트너와 함께 파트너가 사용하는 변수 및 파트너 이름에 대한 값을 결정합니다.

### setVars

이 `setVars` 메서드를 사용하면 클라이언트가 검색된 파트너 데이터를 사용하여 Analytics 변수를 채울 수 있습니다. 파트너 데이터는 `get` 메서드, 정적 할당 또는 데이터로 파트너 개체를 채우는 기타 메커니즘의 결과일 수 있습니다.

```JavaScript
s.Integrate.<partner_name>.setVars = function (s,p) {
    s.eVar1 = p.<partner_var1>;
    s.eVar2 = p.<partner_var2>;
}
```

일반적으로 조직은 Adobe 파트너와 함께 파트너가 사용하는 변수 및 파트너 이름에 대한 값을 결정합니다.

### 스크립트

이 `script` 메서드를 사용하면 Adobe 파트너가 특정 조건이 충족되는 경우(예: 캠페인 변수가 설정된 경우) 파트너 사이트에서 추가 JavaScript를 호출할 수 있습니다.

```JavaScript
p.script("<partner_url>/script?qs1=value1&qs2=value2");
```

일반적으로 조직은 Adobe 파트너와 함께 파트너 이름에 대한 값을 결정합니다. URL에 포함된 쿼리 문자열은 선택 사항이며, 파트너에 따라 다릅니다. 모듈 통합에는 브라우저 캐싱을 방지하기 위해 임의 숫자가 들어 있는 쿼리 문자열이 자동으로 포함됩니다.
