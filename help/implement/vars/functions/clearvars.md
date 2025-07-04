---
title: clearVars
description: 인스턴스 개체에서 값을 지웁니다.
feature: Appmeasurement Implementation
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 67%

---

# clearVars

단일 페이지 애플리케이션과 같은 일부 구현에서는 동일한 페이지 로드 시 전송된 여러 개의 히트가 필요합니다. 변수 값이 후속 히트에 지속되지 않도록 변수 값을 지우려면 `clearVars()` 메서드를 사용하십시오.

이 메서드는 인수를 사용하지 않으며 값을 반환하지 않습니다. 인스턴스 개체에서 변수 값을 지우는 것이 이 메서드의 유일한 목적입니다. 이 메서드는 다음 요소를 `undefined`로 설정합니다.

* `prop1` - `prop75`
* `eVar` - `eVar250`
* `hier1` - `hier5`
* `list1` - `list3`
* `events`
* `products`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

## 웹 SDK을 사용하여 변수 지우기

웹 SDK을 사용하여 Adobe으로 데이터를 보내면 모든 XDM 데이터가 자동으로 지워집니다.

## Adobe Analytics 확장을 사용하여 변수 지우기

규칙을 구성할 때 변수 지우기 작업을 설정하십시오.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업] 아래에서 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운 목록을 Adobe Analytics으로 설정하고 [!UICONTROL 작업 유형]을(를) [!UICONTROL 변수 지우기]&#x200B;(으)로 설정합니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.clearVars()

Analytics 개체 인스턴스를 인스턴스화한 후에는 구현의 어느 곳에서든 `s.clearVars()` 메서드를 호출할 수 있습니다.

```js
s.clearVars();
```
