---
description: 페이지 상단에 JavaScript 라이브러리 파일에 대한 호출을 삽입하면 이미지가 제일 먼저 다운로드되는 요소가 됩니다.
keywords: Analytics 구현
seo-description: 페이지 상단에 JavaScript 라이브러리 파일에 대한 호출을 삽입하면 이미지가 제일 먼저 다운로드되는 요소가 됩니다.
seo-title: JavaScript 파일 위치 및 동의
solution: Analytics
subtopic: 문제 해결
title: JavaScript 파일 위치 및 동의
topic: 개발자 및 구현
uuid: ED 5118 A 8-B 142-4 FAB -8 AA 1-92 D 931 CC 1439
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# JavaScript 파일 위치 및 동의

페이지 상단에 JavaScript 라이브러리 파일에 대한 호출을 삽입하면 이미지가 제일 먼저 다운로드되는 요소가 됩니다.

대부분의 웹 브라우저는 이미지들을 동시에 다운로드하며, 일반적으로 3-4개의 이미지를 동시에 다운로드할 수 있습니다.

대부분의 웹 브라우저가 요소를 동시에 다운로드하므로, 많은 일반적인 브라우저들(Internet Explorer 포함)의 상태 표시줄은 브라우저가 로드하려고 하는 요소를 정확하게 반영하지 않습니다. 예를 들어 상태 표시줄은 브라우저가 이미지 1의 다운로드를 기다리고 있다고 보고하지만, 네트워크 패킷 테스트를 해보면 브라우저가 이미 이미지 1을 받았고 현재 이미지 2를 기다리고 있을 수 있습니다.

>[!NOTE]
>
>타사 인터넷 성능 감사 공급자 (Keynote Systems 등) 는 페이지 이미지 요소를 동시에 다운로드하는 것이 아니라 순차적으로 다운로드하므로 일반적인 사용자 환경을 모방하지 않습니다.

