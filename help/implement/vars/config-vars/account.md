---
title: account
description: 계정 변수를 사용하여 데이터를 보낼 보고서 세트를 결정합니다.
translation-type: tm+mt
source-git-commit: 1f0fd2dcb0454ad9bc2e0c2141b5e17470c6a5de

---


# account

> [!IMPORTANT] 이 변수는 사용이 중단되었습니다. 구현에서 보고서 세트 대상을 수정해야 하는 경우 [`s.sa()`](../functions/sa.md) 함수를 사용합니다.

이전 버전의 Adobe Analytics에서 `account` 변수는 데이터를 보낼 보고서 세트를 결정합니다. Adobe Analytics로 데이터를 전송하려면 보고서 세트 ID가 필요합니다.

* Adobe Experience Platform Launch를 사용하는 경우 Adobe Analytics [!UICONTROL 확장 기능을 구성할 때 보고서] 세트가 라이브러리 관리 아코디언 아래에 있습니다.
* 이 `s_gi()` 함수를 사용하여 Analytics 추적 개체를 인스턴스화하는 경우 보고서 세트 ID가 함수에 필수 인수로 이미 존재합니다.
