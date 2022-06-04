---
title: Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현
description: Adobe Experience Platform 데이터 수집의 웹 SDK 확장을 사용하여 데이터를 Adobe Analytics에 보냅니다.
source-git-commit: 6979736e1849d25af2141e0ab76a143605a90620
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 33%

---


# Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현

를 사용할 수 있습니다 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html) Adobe Analytics으로 데이터를 전송하는 중입니다. 이 구현 방법은 [XDM(경험 데이터 모델)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko) 형식에서 Analytics에 사용되는 형식으로 변환해야 합니다.

## 설정

XDM 데이터를 수신하도록 Analytics를 설정하려면 다음을 수행하십시오.

1. [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)를 설치하고 [구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=ko-KR)합니다.

1. 적용 가능한 보고서 세트가 원하는 데이터에 매핑되어 있는지 확인합니다. XDM 데이터는 Adobe Experience Edge에서 보고서 세트로 자동 전송됩니다.
