---
title: 구성 변수
description: 구성 변수를 사용하여 데이터를 수집하는 방법을 결정합니다.
feature: Appmeasurement Implementation
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
role: Admin, Developer
TQID: https://experienceleague.adobe.com/amtLWIgyADqWBOv38xdJ6AF4IjhJ0aGVrvYqXLckfkI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c069c44e-5426-4c1a-accc-8028662f2fdeid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 65%

---

# 구성 변수 개요

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 이 변수는 일반적으로 차원 또는 지표 값을 포함하지 않습니다.

## 구성 변수 설정

웹 SDK 확장 또는 Analytics 확장을 사용하는 구현에서 구성 변수는 일반적으로 확장 설정에서 찾을 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭을 클릭한 다음 확장 아래의 [!UICONTROL 구성]을 클릭합니다.

`AppMeasurement.js`를 사용하는 JavaScript 구현에서 구성 변수는 일반적으로 JS 파일의 맨 위에 설정됩니다.

>[!IMPORTANT]
>
>추적 메서드([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))를 호출하기 전에 모든 구성 변수가 설정되었는지 확인하십시오. [`doPlugins()`](../functions/doplugins.md) 함수에서 구성 변수를 설정하지 마십시오.
