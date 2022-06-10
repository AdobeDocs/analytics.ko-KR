---
title: Adobe Experience Platform Mobile SDK를 사용하여 Adobe Analytics 구현
description: Adobe Experience Platform 데이터 수집에서 Mobile SDK 확장 기능을 사용하여 Adobe Analytics로 데이터를 전송합니다.
exl-id: 516e9a1e-caa7-4f8a-ab8c-6404e9242ccb
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 89%

---

# Adobe Experience Platform Mobile SDK를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Mobile SDK는 모바일 앱에서 Adobe의 Experience Cloud 솔루션 및 서비스를 강화하는 데 도움이 됩니다. Android, iOS, 다양한 크로스 플랫폼 개발 프레임워크에서 사용할 수 있습니다. 구성은 Adobe Experience Platform 데이터 수집을 통해 처리됩니다.

Mobile SDK를 사용하여 Adobe Experience Edge로 데이터를 전송하려면:

1. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 목록에서 원하는 속성을 선택하거나 [모바일 속성을 설정합니다](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).
3. 확장 탭으로 이동하여 [Edge Network용 ID](https://aep-sdks.gitbook.io/docs/foundation-extensions/identity-for-edge-network) 확장 기능을 설치합니다.
4. [Adobe Experience Platform Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/experience-platform-extension)를 설치합니다.
5. 원하는 보고서 세트를 가리키는 서비스로 Adobe Analytics를 추가하여 [데이터스트림을 구성](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams)합니다.
6. 모바일 앱에서 [SDK를 설치](https://aep-sdks.gitbook.io/docs/getting-started/get-the-sdk)합니다.

>[!IMPORTANT]
>
>Adobe Analytics 확장은 Adobe Experience Platform 데이터 수집에서도 사용할 수 있습니다. 이 확장 기능을 설치하는 경우 XDM 또는 Edge Network를 사용하지 않습니다.
