---
title: 구성 변수
description: 구성 변수를 사용하여 데이터를 수집하는 방법을 결정합니다.
feature: Appmeasurement Implementation
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
role: Admin, Developer
TQID: https://experienceleague.adobe.com/amtLWIgyADqWBOv38xdJ6AF4IjhJ0aGVrvYqXLckfkI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 19%

---

# 구성 변수 개요

구성 변수는 데이터가 보고에서 캡처 및 처리되는 방식을 제어합니다. 이 변수는 일반적으로 차원 또는 지표 값을 포함하지 않습니다.

## 구성 변수 설정

웹 SDK 확장 또는 Analytics 확장을 사용하는 구현에서 구성 변수는 일반적으로 확장 설정에서 찾을 수 있습니다.

1. Adobe ID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭을 클릭한 다음 확장 아래의 [!UICONTROL 구성]을 클릭합니다.

`AppMeasurement.js`를 사용하는 JavaScript 구현에서 구성 변수는 일반적으로 JS 파일의 맨 위에 설정됩니다.

>[!IMPORTANT]
>
>추적 메서드([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))를 호출하기 전에 모든 구성 변수가 설정되었는지 확인하십시오. [`doPlugins()`](../functions/doplugins.md) 함수에서 구성 변수를 설정하지 마십시오.

## 폐기된 구성 변수

다음 구성 변수가 사용되지 않습니다. 기존 구현에서 이러한 문제가 발생하는 경우 참조할 수 있도록 여기에 문서화되어 있습니다.

* **`account`**: 데이터가 전송되는 보고서 세트를 확인했습니다. 이제 추적 개체 인스턴스화([`s_gi()`](../functions/s-gi.md) 메서드)를 통해 보고서 세트가 처리됩니다. 추적 개체가 인스턴스화된 후 보고서 세트를 변경해야 하는 경우 [`s.sa()`](../functions/sa-method.md) 메서드를 사용하십시오.
* **`cookieDomain`**: AppMeasurement에서 쿠키를 설정한 도메인을 확인했습니다. 현재 버전의 AppMeasurement은 올바른 쿠키 도메인을 자동으로 검색하므로 이 변수는 더 이상 사용되지 않습니다.
* **`cookieDomainPeriods`**: 도메인에 여러 개의 마침표가 포함되어 있을 때 AppMeasurement에서 쿠키를 저장할 위치를 결정할 수 있도록 지원했습니다. 현재 버전의 AppMeasurement은 올바른 도메인을 자동으로 검색하므로 이 변수는 더 이상 사용되지 않습니다.
* **`fpCookieDomainPeriods`**: 자사 도메인의 접미사에 `example.co.uk` 등의 추가 기간이 포함된 경우 올바른 위치에 쿠키를 설정하는 데 사용되는 `cookieDomainPeriods`과(와) 동등한 자사. 현재 버전의 AppMeasurement은 올바른 도메인을 자동으로 검색하므로 이 변수는 더 이상 사용되지 않습니다.
* **`trackingServer`**: HTTP를 통해 Adobe으로 데이터를 보내는 데 사용되는 도메인을 지정했습니다. HTTPS보다 안전한 데이터 수집을 위해 더 이상 사용되지 않습니다. 대신 [`trackingServerSecure`](trackingserversecure.md)를 사용하십시오.
* **`trackInlineStats`**: 이전 버전의 [Activity Map](/help/analyze/activity-map/overview.md)을(를) 사용하거나 사용하지 않도록 설정했습니다.
* **`visitorMigrationKey`**: 방문자를 서드파티 쿠키에서 자사 쿠키로 마이그레이션하는 데 사용되는 키를 포함했습니다. 최신 라이브러리가 자사 대체 쿠키(`fid`)를 설정하고 ID를 방문자 ID 서비스에 의존하기 때문에 사용이 중단되었습니다.
* **`visitorMigrationServer`**: 서드파티에서 퍼스트 파티 쿠키로 마이그레이션하는 동안 사용되는 서버를 지정했습니다.
* **`visitorMigrationServerSecure`**: `visitorMigrationServer`에 해당하는 HTTPS입니다.
* **`visitorNameSpace`**: 타사 쿠키 도메인을 확인하는 데 도움이 되었습니다. 방문자 ID 서비스를 사용하지 않는 구현의 경우 [`trackingServerSecure`](trackingserversecure.md) 변수 사용을 위해 사용이 중단됩니다.
