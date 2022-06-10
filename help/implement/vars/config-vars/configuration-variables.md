---
title: 구성 변수
description: 구성 변수를 사용하여 데이터를 수집하는 방법을 결정합니다.
feature: Variables
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 66%

---

# 구성 변수 개요

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 이 변수는 일반적으로 차원 또는 지표 값을 포함하지 않습니다.

## 구성 변수 설정

웹 SDK 확장 또는 Analytics 확장을 사용하는 구현에서 구성 변수는 일반적으로 확장의 설정에 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 을(를) 클릭합니다. [!UICONTROL 확장] 탭을 클릭한 다음 [!UICONTROL 구성] 확장 아래의 를 참조하십시오.

`AppMeasurement.js`를 사용하는 JavaScript 구현에서 구성 변수는 일반적으로 JS 파일의 맨 위에 설정됩니다.

>[!IMPORTANT]
>
>추적 메서드 ([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))를 호출하기 전에 모든 구성 변수가 설정되었는지 확인하십시오. [`doPlugins()`](../functions/doplugins.md) 함수에서 구성 변수를 설정하지 마십시오.
