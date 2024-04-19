---
title: AppMeasurement에서 웹 SDK로 마이그레이션
description: AppMeasurement JavaScript 라이브러리에서 웹 SDK JavaScript 라이브러리로 Adobe Analytics 구현을 업데이트합니다.
exl-id: c90246e8-0f04-4655-9204-33c0ef611b13
source-git-commit: 7bd4a188e5a2171260f1f0696d8bebad854dba4a
workflow-type: tm+mt
source-wordcount: '1334'
ht-degree: 0%

---

# AppMeasurement에서 웹 SDK로 마이그레이션

이 구현 경로에는 AppMeasurement 구현에서 Web SDK JavaScript 라이브러리 구현으로 이동하는 메서드 마이그레이션 접근 방식이 포함됩니다. 다른 구현 경로는 별도의 페이지에서 다룹니다.

* [Analytics 확장을 웹 SDK 확장으로](analytics-extension-to-web-sdk.md): Adobe Analytics 태그 확장 기능에서 웹 SDK 태그 확장 기능으로 이동하려면 유연하고 방법적인 접근 방식을 사용하십시오. 이 접근 방법에서는 조직이 Customer Journey Analytics과 같은 Adobe Experience Platform 서비스를 사용할 준비가 될 때까지 XDM을 사용할 필요가 없습니다. 사용 `data` 개체 대신 `xdm` Adobe에 데이터를 보낼 개체입니다.
* [웹 SDK JavaScript 라이브러리](web-sdk-javascript-library.md): Web SDK JavaScript 라이브러리를 사용한 새로운 웹 SDK 설치(`alloy.js`). 태그 UI를 사용하는 대신 구현을 직접 관리합니다. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.
* [Web SDK 태그 확장](web-sdk-tag-extension.md): Adobe Experience Platform 데이터 수집의 태그를 사용하여 구현을 관리하는 새로운 웹 SDK 설치. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.

## 이 구현 경로의 장단점

이러한 마이그레이션 접근 방식을 사용하면 장점과 단점이 모두 있습니다. 각 옵션을 신중히 평가하여 조직에 가장 적합한 접근 방식을 결정하십시오.

| 장점 | 단점 |
| --- | --- |
| <ul><li>**기존 구현 사용**: 이 접근 방식에서는 몇 가지 구현 변경이 필요하지만 처음부터 완전히 새로운 구현이 필요한 것은 아닙니다. 구현 논리를 최소한으로 변경하여 기존 데이터 레이어 및 코드를 사용할 수 있습니다.</li><li>**스키마가 필요하지 않음**: Web SDK로 마이그레이션하는 이 단계에서는 XDM 스키마가 필요하지 않습니다. 대신 `data` 개체 - Adobe Analytics으로 데이터를 직접 전송합니다. 웹 SDK로의 마이그레이션이 완료되면 조직에 대한 스키마를 만들고 데이터스트림 매핑을 사용하여 적용 가능한 XDM 필드를 채울 수 있습니다. 마이그레이션 프로세스의 이 단계에서 스키마가 필요한 경우 조직에서 Adobe Analytics XDM 스키마를 사용해야 합니다. 이 스키마를 사용하면 향후 조직에서 자체 스키마를 사용하는 것이 더 어려워집니다.</li></ul> | <ul><li>**구현을 변경하려면 개발자의 개입이 필요합니다**: 웹 SDK 구현을 변경하려면 개발 팀과 함께 사이트에서 코드를 편집해야 합니다. 접근 방식 [웹 SDK 태그 확장으로 마이그레이션](analytics-extension-to-web-sdk.md) 이 단점을 방지합니다.</li><li>**구현 기술 부채**: 이 방법은 기존 구현의 수정된 형식을 사용하므로 구현 논리를 추적하고 필요한 경우 나중에 변경 사항을 수행하는 것이 더 어려울 수 있습니다.</li><li>**데이터를 플랫폼으로 전송하기 위한 매핑 필요**: 조직에서 Customer Journey Analytics을 사용할 준비가 되면 Adobe Experience Platform의 데이터 세트로 데이터를 보내야 합니다. 이 작업을 수행하려면 의 모든 필드가 `data` 객체는 XDM 스키마 필드에 할당하는 데이터 스트림 매핑 도구의 항목입니다. 매핑은 이 워크플로우에 대해 한 번만 수행하면 되며 구현 변경을 수반하지 않습니다. 그러나 XDM 개체에서 데이터를 전송할 때는 필요하지 않은 추가 단계입니다.</li></ul> |

Adobe은 다음 시나리오에서 이 구현 경로를 따를 것을 권장합니다.

* Adobe Analytics AppMeasurement JavaScript 라이브러리를 사용하는 기존 구현이 있습니다. Adobe Analytics 태그 확장을 사용하는 구현이 있는 경우 다음을 따르십시오 [Adobe Analytics 태그 확장에서 웹 SDK 태그 확장으로 마이그레이션](analytics-extension-to-web-sdk.md) 대신,
* 나중에 Customer Journey Analytics을 사용할 계획이지만 Analytics 구현을 처음부터 웹 SDK 구현으로 바꾸지는 않을 것입니다. 웹 SDK에서 구현을 처음부터 교체하려면 가장 많은 노력이 필요하지만 가장 실행 가능한 장기 구현 아키텍처도 제공합니다. 조직에서 깔끔한 웹 SDK 구현을 수행하려는 경우 다음을 참조하십시오. [Adobe Experience Platform Web SDK를 통해 데이터 수집](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) Customer Journey Analytics 사용 안내서에서 확인할 수 있습니다.

## 웹 SDK로 마이그레이션하는 데 필요한 단계

다음 단계에는 구체적인 작업 목표가 포함되어 있습니다. 각 단계를 클릭하여 수행 방법에 대한 자세한 지침을 확인하십시오.

+++**1. 데이터 스트림 만들기 및 구성**

Adobe Experience Platform 데이터 수집에서 데이터 스트림을 만듭니다. 이 데이터 스트림으로 데이터를 전송하면 데이터가 Adobe Analytics으로 전달됩니다. 향후에 이와 동일한 데이터스트림이 데이터를 Customer Journey Analytics에 전달합니다.

1. 다음으로 이동 [experience.adobe.com](https://experience.adobe.com) 자격 증명을 사용하여 로그인합니다.
1. 오른쪽 상단의 홈 페이지 또는 제품 선택기를 사용하여 다음 위치로 이동합니다. **[!UICONTROL 데이터 수집]**.
1. 왼쪽 탐색에서 을 선택합니다. **[!UICONTROL 데이터스트림]**.
1. **[!UICONTROL 새 데이터스트림]**&#x200B;을 선택합니다.
1. 원하는 이름을 입력한 다음 을 선택합니다 **[!UICONTROL 저장]**.
1. 데이터 스트림이 생성되면 다음을 선택합니다. **[!UICONTROL 서비스 추가]**.
1. 서비스 드롭다운 메뉴에서 다음을 선택합니다. **[!UICONTROL Adobe Analytics]**.
1. 현재 분석 데이터를 보내는 사이트와 동일한 보고서 세트 ID를 입력합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

![Adobe Analytics 서비스 추가](assets/datastream-rsid.png) {style="border:1px solid lightslategray"}

이제 데이터 스트림이 데이터를 받아서 Adobe Analytics에 전달할 준비가 되었습니다. 코드에서 웹 SDK를 구성할 때 이 ID가 필요하므로 데이터 스트림 ID를 참고하십시오.

+++

+++**2. 웹 SDK JavaScript 라이브러리 설치**

최신 버전 참조 `alloy.js` 따라서 이 메서드 호출을 사용할 수 있습니다. 다음을 참조하십시오 [JavaScript 라이브러리를 사용하여 웹 SDK 설치](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/library) 을 참조하십시오.

+++

+++**3. 웹 SDK 구성**

Web SDK를 사용하여 이전 단계에서 생성한 데이터 스트림을 가리키도록 구현을 설정하십시오 [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) 명령입니다. 다음 `configure` 라이브러리 설치 코드와 함께 포함할 수 있도록 모든 페이지에서 명령을 설정해야 합니다.

사용 [`edgeConfigId`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgeconfigid) 및 [`orgId`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/orgid) Web SDK 내의 속성 `configure` 명령:

* 설정 `edgeConfigId` 이전 단계에서 검색된 데이터 스트림 ID로.
* 설정 `orgId` 을 조직의 IMS 조직에 연결합니다.

```js
alloy("configure", {
    "edgeConfigId": "ebebf826-a01f-4458-8cec-ef61de241c93",
    "orgId": "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

에서 다른 속성을 선택적으로 설정할 수 있습니다 [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) 조직의 구현 요구 사항에 따라 명령을 실행합니다.

+++

+++**4. JSON 페이로드를 사용하도록 코드 논리 업데이트**

를 사용하지 않도록 Analytics 구현 변경 `AppMeasurement.js` 또는 `s` 개체. 대신 변수를 올바른 형식의 JavaScript 개체로 설정하십시오. 이 개체는 Adobe으로 전송될 때 JSON 개체로 변환됩니다. 다음 작업 수행 [데이터 레이어](../../prepare/data-layer.md) 사이트에서는 동일한 값을 계속 참조할 수 있으므로 값을 설정할 때 많은 도움이 됩니다.

Adobe Analytics으로 데이터를 전송하려면 웹 SDK 페이로드가 다음을 사용해야 합니다. `data.__adobe.analytics` 모든 analytics 변수가 이 오브젝트 내에 설정된 경우. 이 개체 내의 변수는 AppMeasurement 변수 상대가 공유하는 것과 동일한 이름과 형식을 공유합니다. 예를 들어, `products` 변수를 XDM에서처럼 개별 객체로 분할하지 마십시오. 대신 를 문자열로 포함하면 를 `s.products` 변수:

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "products": "Shoes,Men's sneakers,1,49.99"
      }
    }
  }
}
```

궁극적으로 이 페이로드에는 원하는 모든 값과 `s` 구현에서 개체가 제거됩니다. 개별 값을 설정하는 점 표기법을 포함하여 JavaScript가 제공하는 모든 리소스를 사용하여 이 페이로드 개체를 설정할 수 있습니다.

```js
// Define the payload and set objects within it
var dataObj = {data: {__adobe: {analytics: {}}}};
dataObj.data.__adobe.analytics.pageName = window.document.title;
dataObj.data.__adobe.analytics.eVar1 = "Example value";

// Alternatively, set values in an object and use a spread operator to achieve identical results
var a = new Object;
a.pageName = window.document.title;
a.eVar1 = "Example value";
var dataObj = {data:{__adobe:{analytics:{...a}}}};
```

+++

+++**5. 웹 SDK를 사용하도록 메서드 호출 업데이트**

를 호출하는 모든 인스턴스 업데이트 [`s.t()`](../../vars/functions/t-method.md) 및 [`s.tl()`](../../vars/functions/tl-method.md), 다음으로 바꾸기 [`sendEvent`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendevent/overview) 명령입니다. 고려해야 할 세 가지 시나리오가 있습니다.

* **페이지 보기 추적**: 페이지 보기 추적 호출을 웹 SDK로 바꿉니다 `sendEvent` 명령:

  ```js
  // If your current implementation has this line of code:
  s.t();
  
  // Replace it with this line of code. The dataObj object contains the variables to send.
  alloy("sendEvent", dataObj);
  ```

* **자동 링크 추적**: [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) 구성 속성은 기본적으로 활성화되어 있습니다. 데이터를 Adobe Analytics으로 전송할 올바른 링크 추적 변수를 자동으로 설정합니다. 자동 링크 추적을 비활성화하려면 이 속성을 다음으로 설정하십시오. `false` 다음 범위 내 [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) 명령입니다.

* **수동 링크 추적**: 웹 SDK에는 pageview와 pageview가 아닌 호출 사이에 별도의 명령이 없습니다. 페이로드 객체 내에 해당 구분을 제공합니다.

  ```js
  // If your current implementation has this line of code:
  s.tl(true,"o","Example custom link");
  
  // Replace it with these lines of code. Add the required fields to the dataObj object.
  dataObj.data.__adobe.analytics.linkName = "Example custom link";
  dataObj.data.__adobe.analytics.linkType = "o";
  dataObj.data.__adobe.analytics.linkURL = "https://example.com";
  alloy("sendEvent", dataObj);
  ```

+++

+++**6. 변경 내용의 유효성 검사 및 게시**

AppMeasurement 및 의 모든 참조를 제거했으면 `s` 개체에서 변경 사항을 개발 환경에 게시하여 새 구현이 작동하는지 확인합니다. 모든 것이 올바르게 작동하는지 확인했으면 프로덕션에 업데이트를 게시할 수 있습니다.

올바르게 마이그레이션된 경우 `AppMeasurement.js` 가 더 이상 사이트에 필요하지 않으며 이 스크립트에 대한 모든 참조를 제거할 수 있습니다.

+++

이 시점에서 Analytics 구현은 완전히 웹 SDK에 있으며 향후 Customer Journey Analytics으로 이동할 준비가 되어 있습니다.
