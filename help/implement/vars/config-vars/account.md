---
title: account
description: 계정 변수를 사용하여 보낸 데이터를 받을 보고서 세트를 결정합니다.
feature: Variables
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 47%

---

# account

>[!IMPORTANT]
>
>이 변수는 사용이 중단되었습니다. 구현에서 보고서 세트 대상을 수정해야 하는 경우 [`s.sa()`](../functions/sa-method.md) 함수를 사용하십시오.

이전 버전의 Adobe Analytics에서 `account` 변수는 보낸 데이터를 받을 보고서 세트를 결정했습니다. 데이터를 Adobe Analytics에 전송하려면 보고서 세트 ID가 필요합니다.

* 웹 SDK를 사용하는 경우 보고서 세트는 Web SDK가 데이터를 보내는 데이터 스트림 내의 Adobe Analytics 서비스 설정에 있습니다.
* Adobe Analytics 확장을 사용하는 경우 보고서 세트는 [!UICONTROL 라이브러리 관리] 아코디언을 사용하여 Adobe Analytics 확장을 구성할 수 있습니다.
* 를 사용하는 경우 [`s_gi()`](../functions/s-gi.md) 분석 추적 개체를 인스턴스화하는 함수에서 보고서 세트 ID가 필수 인수로서 이미 존재합니다.
