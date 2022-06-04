---
title: Adobe Experience Platform Mobile SDK를 사용하여 Adobe Analytics 구현
description: Adobe Experience Platform 데이터 수집의 Mobile SDK 확장을 사용하여 데이터를 Adobe Analytics에 보냅니다.
source-git-commit: 6979736e1849d25af2141e0ab76a143605a90620
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Adobe Experience Platform Mobile SDK를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Mobile SDK는 모바일 앱에서 Adobe의 Experience Cloud 솔루션 및 서비스를 제공하는 데 도움이 됩니다. Android, iOS 및 다양한 교차 플랫폼 개발 프레임워크에서 사용할 수 있습니다. 구성은 Adobe Experience Platform 데이터 수집 UI를 통해 처리됩니다.

Mobile SDK를 사용하여 Adobe Experience Edge에 데이터를 전송하려면 다음을 수행하십시오.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection).
2. 목록에서 원하는 속성을 선택하거나 [모바일 속성 설정](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).
3. Extensions 탭으로 이동하여 를 설치합니다. [에지 네트워크의 ID](https://aep-sdks.gitbook.io/docs/foundation-extensions/identity-for-edge-network) 확장.
4. 설치 [Adobe Experience Platform Edge Network](https://aep-sdks.gitbook.io/docs/foundation-extensions/experience-platform-extension).
5. [데이터 스트림 구성](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams): 원하는 보고서 세트를 가리키는 서비스로 Adobe Analytics 추가.
6. [SDK 설치](https://aep-sdks.gitbook.io/docs/getting-started/get-the-sdk) 공유할 수 있습니다.

>[!IMPORTANT]
>
>Adobe Analytics 확장은 데이터 수집 UI에서도 사용할 수 있습니다. 이 확장을 설치하는 경우 XDM 또는 Edge 네트워크를 사용하지 않습니다.
