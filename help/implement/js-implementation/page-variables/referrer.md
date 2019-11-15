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


# referrer

 변수는 손실된 레퍼러 정보를 복원하는 데 사용할 수 있습니다.

<!-- 

referrer.xml

 -->

서버 측 및 JavaScript 리디렉션을 사용하여 방문자를 적절한 위치로 보내는 경우가 많습니다. 그러나 브라우저가 리디렉션되면 원래의 참조 URL이 손실됩니다. 

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 255바이트 | R | 트래픽 &gt; 검색 방법 전환 &gt; 검색 방법 | document.referrer |

많은 회사에서는 자신들의 웹 사이트 전체에서 리디렉션을 사용합니다. 예를 들어 방문자가 리디렉션을 통해 검색 엔진의 유료 검색 결과로 이동할 수도 있습니다. 브라우저가 리디렉션되면 레퍼러가 손실되는 경우가 많습니다. The *`referrer`* 변수는 리디렉션 후 첫 번째 페이지에서 원래 *`referrer`* 값을 복원하는 데 사용할 수 있습니다. *`referrer`*&#x200B;는 서버 측에서 채울 수도 있고 쿼리 문자열에서 JavaScript를 통해 채울 수도 있습니다.

Analytics가 레퍼러를 기록하려면 "형식을 제대로 지정"해야 하며, 이것은 프로토콜과 적절한 위치로 표준 URL 형식을 따라야 함을 의미합니다.

**구문 및 가능한 값** {#section_A0365D76789C4F4A959E81FE5A9D491D}

```js
s.referrer="URL"
```

 URL 호환 값만 *`referrer`*&#x200B;에 있어야 합니다. 문자열이 URL 인코딩되어 있는지(공백 없음) 확인하십시오.

**예** {#section_86FB1577670C4AA18BF3718F0832FCD4}

```js
s.referrer="https://www.google.com/search?q=search+string" 
s.referrer=<%=referrerVar%> // populated server-side  
if(s.getQueryParam('ref') 
s.referrer=s.getQueryParam('ref') 
```

**구성 설정** {#section_7AAEF28A7CBC446984F32C0659EFBF8D}

없음

**함정, 질문 및 팁** {#section_B42BF7FBA1094FF9805707FEA810CFE1}

*`referrer`*&#x200B;는 표준 URL의 모양이며 프로토콜을 포함해야 합니다.
