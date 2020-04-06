---
title: account
description: 계정 변수를 사용하여 보낸 데이터를 받을 보고서 세트를 결정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# account

>[!IMPORTANT] 이 변수는 사용이 중단되었습니다. 구현에서 보고서 세트 대상을 수정해야 하는 경우 [`s.sa()`](../functions/sa-method.md) 함수를 사용하십시오.

이전 버전의 Adobe Analytics에서 `account` 변수는 보낸 데이터를 받을 보고서 세트를 결정했습니다. 데이터를 Adobe Analytics에 전송하려면 보고서 세트 ID가 필요합니다.

* If you use Adobe Experience Platform Launch, report suites reside under the [!UICONTROL Library Management] accordion when configuring the Adobe Analytics extension.
* [`s_gi()`](../functions/s-gi.md) 함수를 사용하여 Analytics 추적 개체를 인스턴스화하는 경우 보고서 세트 ID가 함수에서 필수 인수로서 이미 존재합니다.
