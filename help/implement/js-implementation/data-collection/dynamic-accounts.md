---
description: 보고서 세트 ID를 자동으로 선택하도록 .js 파일을 구성할 수 있습니다.
keywords: Analytics Implementation
solution: Analytics
title: 보고서 세트 ID - 다이내믹 계정
topic: Developer and implementation
uuid: 763a9741-309d-4795-8819-6543866047d5
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 보고서 세트 ID - 다이내믹 계정

보고서 세트 ID를 자동으로 선택하도록 .js 파일을 구성할 수 있습니다. .js 파일은 URL을 기반으로 이미지 요청을 자동으로 보고서 세트에 보냅니다. 예를 들어 URL이 `www.mysite.com`인 경우 이미지 요청은 보고서 세트 A로 자동 전송됩니다. URL이 `www.mysite1.com`인 경우에는 세트 B로 이미지 요청이 자동 전송됩니다.

이러한 문자열은 다음 항목 내에서 찾을 수 있습니다.

* 호스트/도메인(기본 설정)
* 경로
* 쿼리 문자열
* 호스트/도메인 및 경로
* 경로 및 쿼리 문자열
* 전체 URL

[!DNL Analytics]보고서 세트 ID[!UICONTROL 를 자동으로 선택하도록 ]를 구성하는 방법에 대해서는 Adobe 라이브 지원에 문의하십시오.

## 일치하는 URL 세그먼트 정의 {#section_8099162F75F641CFBE46FD814450EF36}

다음 샘플 URL이 주어지는 경우, 설정해야 하는 `s.dynamicAccountMatch` 변수와 함께 URL의 부분들은 아래와 같습니다. (`s.dynamicAccountMatch`가 정의되지 않은 경우, 기본값은 호스트/도메인 이름만 검색하는 것입니다.)
샘플 URL: `https://www.client.com/directory1/directory2/filename.html?param1=1234&param2=4321`

| 부분 | 예(위에서) |
|---|---|
| 호스트/도메인 이름 | `www.client.com` |
| 경로 | `directory1/directory2/filename.html` |
| 쿼리 문자열 | `param1=1234&param2=4321` |
| 호스트/도메인 및 경로 | `www.client.com/directory1/directory2/filename.html` |
| 경로 및 쿼리 문자열 | `directory1/directory2/filename.html?param1=1234&param2=4321` |
| URL | `https://www.client.com/directory1/directory2/filename.html?param1=1234&param2=4321` |
| 부분 | `s.dynamicAccountmatch` |
| 호스트/도메인 이름 | 정의되지 않음 |
| 경로 | `window.location.pathname` |
| 쿼리 문자열 | `(window.location.search?window.location.search:"?")` |
| 호스트/도메인 및 경로 | `window.location.host+window.location.pathname` |
| 경로 및 쿼리 문자열 | `window.location.pathname+(window.location.search?window.location.search:"?")` |
| URL | `window.location.href` |

다음 예를 생각해 보십시오.

* `s.dynamicAccountSelection=true`
* `s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite2=clientdirectory;reportsuite1=client.com"`
* `s.dynamicAccountMatch=window.location.host+window.location.pathname`

## 여러 규칙 {#section_163FED1C1FA74C48BCB78B0D67EF36AE}

여러 규칙을 선택한 경우(위의 예 참조), 규칙은 왼쪽에서 오른쪽으로 실행됩니다. 규칙은 아래에서 보듯이 일치 항목을 찾자마자 중지됩니다(주어진 규칙 세트 사용 시).

* `s.dynamicAccountSelection=true`
* `s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com"`

코드는 먼저 `qa.client.com`이 호스트/도메인 이름 내에 있는지 확인하여 판단합니다. 있는 경우 보고서 세트 `devreportsuite1`이 선택되고 비교가 중단됩니다. 규칙이 여러 개면 세미콜론으로 구분하십시오.

## 기본 보고서 세트 {#section_0360D724929348B0B211708B5BA15647}

`s_account` 변수는 맨 먼저 설정할 수 있고, 지정된 문자열을 찾을 수 없는 경우 기본값으로 작동합니다. 아래는 한 예입니다.

```javascript
var s_account="defaultreportsuiteid" 
s.dynamicAccountSelection=true 
s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com" 
```

위의 경우 호스트/도메인 이름에 `qa.client.com`이나 `client.com`이 들어 있지 않았다면 보고서 세트 *defaultreportsuiteid*&#x200B;가 사용됩니다.
