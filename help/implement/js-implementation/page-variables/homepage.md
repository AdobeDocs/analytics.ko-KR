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



# homepage

 변수는 Internet Explorer에서 현재 페이지가 사용자의 홈 페이지로 설정되어 있는지 여부를 나타냅니다.

<!-- 

homepage.xml

 -->

이 변수는 페이지 코드의 뒤에, *`doPlugins`*&#x200B;가 실행되기 전에 채워집니다.

> [!NOTE] 이 변수는 읽기 전용이어야 하며 설정할 수 없습니다.

이 값을 읽고 props/eVars에 복사할 수는 있지만, 변경해서는 안 됩니다. 이 변수는 JavaScript 파일의 H.11 버전에서 도입되었습니다.

| 쿼리 매개 변수 | 값 | 예 | 영향을 받은 보고서 |
|---|---|---|---|
| hp | Y 또는 N | Y | 트래픽 &gt; 기술 &gt; 홈 페이지 |
