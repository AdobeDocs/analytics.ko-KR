---
description: Akamai 및 Speedera와 같은 컨텐츠 전달 서비스나 CDN(Content Distribution Network)은 요청을 자주 받는 문서들을 액세스되는 위치에 가깝게 보관하면서, 웹 컨텐츠는 네트워크의 가장자리에 더 가깝게 두게 됩니다.
keywords: Analytics 구현
seo-description: Akamai 및 Speedera와 같은 컨텐츠 전달 서비스나 CDN(Content Distribution Network)은 요청을 자주 받는 문서들을 액세스되는 위치에 가깝게 보관하면서, 웹 컨텐츠는 네트워크의 가장자리에 더 가깝게 두게 됩니다.
seo-title: 컨텐츠 전달 서비스/네트워크
solution: Analytics
subtopic: 문제 해결
title: 컨텐츠 전달 서비스/네트워크
topic: 개발자 및 구현
uuid: 6 cb 57 c 59-d 0 f 9-4 ca 5-9 f 15-0 e 74 e 585 a 4 a 1
translation-type: tm+mt
source-git-commit: 6250335d05c8e7799802fce26192896a7a6598fe

---


# 컨텐츠 전달 서비스/네트워크

Akamai 및 Speedera와 같은 컨텐츠 전달 서비스나 CDN(Content Distribution Network)은 요청을 자주 받는 문서들을 액세스되는 위치에 가깝게 보관하면서, 웹 컨텐츠는 네트워크의 가장자리에 더 가깝게 두게 됩니다.

이렇게 하면 대개 액세스 지연, 대역폭 사용 및 인프라 비용이 줄어듭니다.

JavaScript용 AppMeasurement 라이브러리 파일을 CDN을 통해 전달하면 사이트 방문자에 대한 파일의 성능 및 전달을 향상시킬 수 있습니다. Adobe 고객은 자신들이 CDN 서비스를 올바로 구성했는지 확인해야 합니다. CDN은 다운로드 시에 발생하는 불안정의 일반적인 원인이며, 다운로드 시 모든 변화에 대한 가장 가능성 있는 원인으로 간주해야 합니다.

태그 관리자는 모든 JavaScript를 CDN에 보관합니다.
