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


# visitorID

방문자는 변수 또는 IP 주소/사용자 에이전트로 식별할 수 있습니다.

<!-- 

visitorID.xml

 -->

*`visitorID`*&#x200B;에는 영숫자를 최대 100자까지 사용할 수 있으며 하이픈은 사용할 수 없습니다.

사용자 지정 ID를 명시적으로 설정하는 경우, 다른 ID 방법 전에 항상 이 ID가 사용됩니다.

사용 순서는 s.visitorID &gt; s_vi &gt; s_fid &gt; IP/UA입니다.

| ** 최대 크기** | ** 디버거 매개 변수** | ** 채워진 보고서** | ** 기본값** |
|---|---|---|---|
| 100바이트 | vid | n/a | "" |

**구문 및 가능한 값** {#section_5F768C7AE6824557997E92B295C09280}

```js
s.visitorID="visitor_id"
```

> [!NOTE]*`visitorID`* 변수에는 하이픈을 사용할 수 없습니다.

**예** {#section_F7F07FEFAC3644A5A084D166ACE1315E}

```js
s.visitorID="abc123"
```

**구성 설정** {#section_582B376FE55C4BCA8F978E0F62B5DB54}

없음
