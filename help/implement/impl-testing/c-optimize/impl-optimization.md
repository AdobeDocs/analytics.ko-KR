---
description: Analytics 배포는 세 가지 주요 단계로 구성됩니다.
keywords: Analytics 구현
seo-description: Analytics 배포는 세 가지 주요 단계로 구성됩니다.
seo-title: 최적화 개요
solution: Analytics
subtopic: 문제 해결
title: 최적화 개요
topic: 개발자 및 구현
uuid: 8 E 8 ECC 5 B-D 4 B 1-4 D 13-8525-39 E 4924 DF 247
translation-type: tm+mt
source-git-commit: 6250335d05c8e7799802fce26192896a7a6598fe

---


# 최적화 개요

Analytics 배포는 세 가지 주요 단계로 구성됩니다.

1. 여기에는 웹 사이트의 각 페이지(또는 페이지 템플릿)에 HTML 코드 조각을 붙여넣는 작업이 포함됩니다. HTML 코드 조각은 매우 작고(400-1,000바이트), 데이터 수집 프로세스를 용이하게 하는 JavaScript 변수와 다른 식별자를 포함합니다.
1. 이 코드 조각은 지표 모음 동안 사용된 Analytics 관련 JavaScript 함수가 들어 있는 JavaScript 라이브러리 파일을 호출합니다. Analytics 코드가 올바로 구현되면, 브라우저가 JavaScript 라이브러리 파일을 실행하는 데 필요한 시간은 보통 무시해도 될 정도입니다.

1. 라이브러리 파일은 Adobe 데이터 수집 서버에 이미지 요청을 수행합니다. 서버는 제출되는 데이터를 모으고, 1x1 투명 이미지를 방문자의 브라우저에 반환합니다. 이 세 번째 단계에서 총 페이지 다운로드 시간이 미미하게 증가합니다.

>[!NOTE]
>
>고객은 추가적인 단계를 수행하여 분석 오버헤드를 최소화할 수 있습니다.

