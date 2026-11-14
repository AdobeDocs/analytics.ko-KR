---
title: 데이터 레이어 만들기
description: 데이터 레이어가 Analytics 구현을 지원하는 방법, Adobe에서 Adobe 클라이언트 데이터 레이어를 권장하는 이유 및 각 구현 방법으로 데이터 레이어 값을 읽는 방법에 대해 알아봅니다.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/JmxM3-AVA5--7Xt4kuES35KFtYbicdGO9JZXsygzuuE'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: df312454-73c4-43f6-a90e-18f5043f074c
    internal-label: Tags
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 7151dca7425bfb99271db71a3132485f85941a5e
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 7%
---
# 데이터 레이어 만들기

데이터 계층은 Analytics 구현에서 수집하는 데이터(예: 페이지 이름, 제품 세부 정보 및 주문 ID)를 표시하는 사이트의 JavaScript 구조입니다. 사이트 코드는 데이터 레이어에 쓰고 구현은 데이터 레이어에서 읽어서 Analytics 변수를 설정합니다. 구현이 페이지의 HTML에 따라 달라지지 않으므로 데이터 수집을 중단하지 않고 사이트를 다시 디자인할 수 있습니다.

## 사전 요구 사항

[솔루션 디자인 문서를 만듭니다](solution-design.md): 조직에서 추적 요구 사항을 충족시키는 것이 중요합니다. 조직의 개발 팀에 접촉하기 전에 솔루션 디자인 문서를 준비했는지 확인하십시오. 솔루션 디자인에 필요한 데이터는 데이터 계층에 포함된 데이터를 결정합니다.

## 데이터 레이어 사양 선택 {#specifications}

Adobe에서는 새 구현 또는 재구성된 구현을 위해 [ACDL(Adobe 클라이언트 데이터 레이어)](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/acdl/overview)을(를) 권장합니다. ACDL은 데이터와 이벤트를 전역 `adobeDataLayer` 배열로 푸시할 수 있는 표준 방법을 사이트에 제공하는 오픈 소스 JavaScript 라이브러리입니다. 태그, 웹 SDK 및 AppMeasurement을 모두 읽을 수 있으며 Adobe Experience Manager 핵심 구성 요소가 자동으로 태그를 채울 수 있습니다.

조직은 전역 `digitalData` 개체에 데이터를 저장하는 [CEDL(Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf)) 또는 사용자 지정 사양과 같은 다른 사양을 자유롭게 사용할 수 있습니다. 가장 중요한 것은 조직이 요구 사항을 충족하는 하나의 세부 항목에 맞추는 것입니다.

다음 표에서는 ACDL을 CEDL과 같은 객체 기반 데이터 레이어와 비교합니다.

| | Adobe 클라이언트 데이터 레이어(`adobeDataLayer`) | CEDL(`digitalData`)과 같은 개체 기반 데이터 계층 |
| --- | --- | --- |
| 사이트 코드가 데이터를 작성하는 방법 | 개체 밀어넣기: `adobeDataLayer.push({ page: { name: "Home" } })` | 속성을 설정합니다. `digitalData.page.pageInfo.pageName = "Home"` |
| 구현에서 값을 읽는 방법 | `adobeDataLayer.getState("page.name")` 또는 Adobe 클라이언트 데이터 레이어 태그 확장의 **데이터 레이어 계산 상태** 데이터 요소 | `digitalData.page.pageInfo.pageName` 또는 Core Tag Extension의 **JavaScript 변수** 데이터 요소 |
| 구현 시 데이터가 준비되었음을 아는 방법 | 사이트 코드는 `{ event: "page view" }`과(와) 같은 이벤트를 푸시하고 구현은 이벤트를 수신합니다. 리스너는 추가되기 전에 푸시된 이벤트에 대해서도 실행됩니다. | 구현은 예를 들어 직접 호출 규칙을 사용하여 사이트 코드의 채우기가 완료된 후 개체를 읽어야 합니다. |

## 예제 데이터 레이어 {#example}

ACDL에는 특정 데이터 구조가 필요하지 않습니다. 솔루션 디자인 문서 주위에 구조를 디자인하고 데이터 레이어에 쓰거나 이 문서에서 읽는 모든 사용자를 위해 구조를 문서화합니다. 이 안내서의 예제에서는 다음 구조를 사용합니다.

페이지가 로드되면 사이트 코드가 페이지의 데이터와 페이지 보기 이벤트를 푸시합니다.

```js
window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push({
  event: "page view",
  page: {
    name: "Home",
    section: "Products",
    url: "https://example.com/products",
    referrer: "https://example.com/"
  }
});
```

방문자가 구매를 완료하면 사이트 코드가 주문 세부 사항 및 구매 이벤트를 푸시합니다.

```js
window.adobeDataLayer.push({
  event: "purchase",
  transaction: { id: "ABC123" },
  products: [
    { name: "Example product", category: "Example category", quantity: 1, price: 25 }
  ]
});
```

ACDL은 모든 푸시를 구현에서 읽는 계산된 상태라는 단일 개체에 병합합니다. 이벤트 개체는 구현 시 이를 읽을 시기를 알려줍니다. [데이터 및 계산된 상태](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/concepts/computed-state) 및 [이벤트](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/concepts/events)를 참조하세요.

## 워크플로 {#workflow}

데이터 레이어를 사용하여 Adobe Analytics를 구현하는 절차는 일반적으로 다음과 같습니다.

1. **사이트 개발 팀과 협력하여 데이터 레이어를 구현하십시오**: 사이트 개발 팀은 데이터 레이어에 올바른 값이 포함되어 있는지 확인하는 작업을 주로 수행합니다. 사이트 개발 팀과 함께 이 페이지를 검토하여 팀 간의 기대 내용이 일치하는지 확인합니다. [Adobe 클라이언트 데이터 레이어 설치](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/acdl/install)를 참조하십시오.
1. **브라우저 콘솔을 사용하여 데이터 계층의 유효성 검사**: 브라우저의 개발자 콘솔을 엽니다. 이 작업은 `F12` 키로 대부분의 브라우저에서 수행할 수 있습니다. 계산된 상태를 보려면 `adobeDataLayer.getState()`을(를) 실행하고 단일 값을 보려면 `adobeDataLayer.getState("page.name")`을(를) 실행하십시오. [설치 확인](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/acdl/install#verify)을 참조하세요.
1. **데이터 레이어를 Adobe Analytics에 연결**: 이 단계는 조직의 구현 방법에 따라 다릅니다. [데이터 레이어를 Adobe Analytics에 연결](#connect)을 참조하십시오.

## 데이터 레이어를 Adobe Analytics에 연결 {#connect}

다음 표에서는 각 구현 방법이 Adobe 클라이언트 데이터 레이어에서 읽히는 방식을 보여 줍니다.

| 구현 방식 | 데이터 레이어를 읽는 방법 | 추가 정보 |
| --- | --- | --- |
| 웹 SDK 태그 확장 기능 | Adobe 클라이언트 데이터 레이어 확장에서 **데이터 레이어 푸시** 이벤트를 사용하여 규칙을 트리거합니다. 웹 SDK **변수 업데이트** 작업을 사용하여 데이터 레이어 값을 XDM 필드 또는 `data` 개체에 매핑한 다음 **이벤트 보내기** 작업을 사용하여 보냅니다. | [웹 SDK과 함께 Adobe 클라이언트 데이터 레이어 데이터 보내기](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/acdl/web-sdk), [XDM 개체 필드 매핑](../aep-edge/xdm-var-mapping.md) 및 [데이터 개체 필드 매핑](../aep-edge/data-var-mapping.md) |
| 웹 SDK JavaScript 라이브러리 | `addEventListener()`을(를) 사용하여 데이터 레이어 이벤트를 수신하고 `sendEvent`을(를) 호출할 때 데이터 레이어에서 XDM 또는 `data` 필드를 설정합니다. | [웹 SDK과 함께 Adobe 클라이언트 데이터 레이어 데이터 보내기](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/acdl/web-sdk), [XDM 개체 필드 매핑](../aep-edge/xdm-var-mapping.md) 및 [데이터 개체 필드 매핑](../aep-edge/data-var-mapping.md) |
| Analytics 확장 기능 | **데이터 레이어 푸시** 이벤트를 사용하여 규칙을 트리거하고 Adobe 클라이언트 데이터 레이어 확장에서 **데이터 레이어 계산 상태**&#x200B;를 만듭니다. **변수 설정** 작업에서 Analytics 변수에 데이터 요소를 할당한 다음 **비콘 보내기** 작업으로 데이터를 보냅니다. | [데이터 레이어 개체를 데이터 요소에 매핑](../launch/layer-to-elements.md) 및 [데이터 요소를 Analytics 변수에 매핑](../launch/elements-to-variable.md) |
| AppMeasurement | ACDL이 로드된 후 `getState()`을(를) 사용하여 값을 읽은 다음 `s.t()`을(를) 호출하십시오. | [AppMeasurement으로 데이터 레이어 읽기](#appmeasurement) |

### AppMeasurement으로 데이터 레이어 읽기 {#appmeasurement}

ACDL은 라이브러리가 로드될 때 `getState()` 메서드를 `adobeDataLayer` 배열에 추가합니다. 라이브러리가 로드되었는지, 계산된 상태가 최신 데이터를 포함하는지 확인하려면 이벤트 리스너 내에서 값을 읽습니다.

```js
window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function(dl) {
  dl.addEventListener("page view", function(event) {
    s.pageName = dl.getState("page.name");
    s.channel = dl.getState("page.section");
    s.t();
  });
});
```

리스너가 추가되기 전에 푸시된 이벤트를 포함하여 각 `page view` 이벤트에 대해 리스너가 한 번 실행됩니다. 이 안내서의 변수 페이지(예: [`pageName`](../vars/page-vars/pagename.md))는 `getState()`을(를) 사용하여 개별 값을 읽는 방법을 보여 줍니다. 이러한 예제를 이러한 수신기 내에서 사용하거나 **데이터 레이어 푸시** 이벤트가 트리거하는 Analytics 확장 규칙의 사용자 지정 코드 편집기에서 사용합니다.

구현이 단일 페이지 애플리케이션에서와 같이 페이지당 두 개 이상의 히트를 전송하는 경우 [`clearVars()`](../vars/functions/clearvars.md)을(를) 사용하여 한 히트의 값이 다음 히트로 지속되지 않도록 하십시오.

## 다음 단계

* [데이터 레이어 개체를 데이터 요소에 매핑](../launch/layer-to-elements.md): Adobe Experience Platform 태그에서 사이트의 데이터 레이어를 사용합니다.
* [Adobe 클라이언트 데이터 레이어 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/acdl/overview): 모든 ACDL 메서드, 이벤트 및 모범 사례에 대해 알아봅니다.
