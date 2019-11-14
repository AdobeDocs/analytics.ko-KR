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


# trackingServer

 변수는 자사 쿠키 구현에서 이미지 요청 및 쿠키를 쓰는 도메인을 지정하는 데 사용됩니다.

<!-- 

trackingServer.xml

 -->

비보안 페이지에 사용됩니다. 만약 *`trackingServer`* 가 정의된 경우는 아무것도 2o7.net으로 전송되지 않습니다. *`trackingServer`*&#x200B;가 정의되지 않은 경우(및 dc가 정의되지 않은 경우) 데이터가 112.2o7.net으로 이동합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | "" |

Adobe 데이터 센터 목록은 [여기](https://helpx.adobe.com/analytics/kb/determining-data-center.html)에 있습니다.
