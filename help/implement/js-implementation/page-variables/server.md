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


# server

 변수는 웹 페이지의 도메인(방문자가 도착한 도메인 표시) 또는 페이지를 제공하는 서버(로드 밸런싱 빠른 참조용)를 보여주는 데 사용됩니다.

<!-- 

server.xml

 -->

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | server | 서버 | "" |

사이트에 동일한 컨텐츠를 제공하는 도메인이 두 개 이상 있을 경우, *`server`*&#x200B;변수를 사용하여 그 도메인들 중 방문자가 사용하고 있는 도메인을 추적할 수 있습니다. 다음 JavaScript는 페이지의 도메인을 server 변수에 채웁니다.

```js
s.server=window.location.hostname
```

server 변수를 사용하여 빠른 로드 밸런싱 지침을 제공하는 경우, 서버 이름이나 번호를 server 변수에 삽입하십시오. 다음 예를 참조하십시오.

```js
s.server="server 14"
```

[!UICONTROL 가장 방문 빈도가 높은 서버] 보고서를 빠른 로드 밸런싱 참조로 사용할 수는 있지만 이 보고서가 서버 로드에 대한 정확한 척도는 아닙니다. 예를 들어 [뒤로] 단추의 트래픽은 서버 로드를 증가시키지 않지만, 보고서에 표시됩니다. 이 보고서는 이미지나 큰 다운로드를 제공하는 서버를 보여주지 않습니다.

**구문 및 가능한 값** {#section_48E4B9BFEBFF4409A246D86EC0C0FB13}

```js
s.server="server_name"
```

*`server`* 변수에는 표준 변수 제한 외에는 제한이 없습니다.

**예** {#section_78B9EE3C27FB491384869E3D0BD503D6}

```js
s.server="server 18" 
s.server=window.location.hostname 
```

**구성 설정** {#section_969DB379D5BD469FBEE8D505D3000E49}

없음

**함정, 질문 및 팁** {#section_42A28F9B01574F38891D9D54B411D8FE}

*`server`* 변수를 사용하여 가장 사용 빈도가 높은 도메인이나 가장 많은 페이지를 제공하는 서버를 보여줄 수 있습니다.

