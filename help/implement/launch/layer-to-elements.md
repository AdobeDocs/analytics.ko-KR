---
title: 데이터 레이어 오브젝트를 데이터 요소에 매핑
description: 데이터 레이어에서 읽을 태그를 구성합니다.
feature: Tags
exl-id: b7594084-cb5f-408e-8a76-0a0815cc7553
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/MmwNCdmt9TwNojJEyzbfTukeh4sKITk06gY-EBzjZPw'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: df312454-73c4-43f6-a90e-18f5043f074c
    internal-label: Tags
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 7151dca7425bfb99271db71a3132485f85941a5e
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 46%
---
# 데이터 레이어 오브젝트를 데이터 요소에 매핑

조직이 사이트에서 데이터 레이어를 설정하고 구현하면 태그 내의 데이터 요소에 데이터 레이어 오브젝트를 매핑할 수 있습니다.

## 사전 요구 사항

[데이터 레이어 만들기](../prepare/data-layer.md): 사이트에 데이터 레이어가 있는지 확인합니다. 기술적으로 모든 JavaScript 오브젝트를 매핑하거나 페이지에서 직접 CSS 요소를 스크랩할 수 있지만 Adobe에서는 이 방법을 마지막 수단으로 권장합니다. 사이트 레이아웃이 변경되면 태그에 사용된 CSS 선택기가 더 이상 작동하지 않아 데이터가 손실됩니다.

## 태그를 사용하여 데이터 요소 만들기

[데이터 요소](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=ko-KR)는 Adobe Experience Platform 데이터 수집의 구성 요소로서 도구 전반에서 사용할 수 있습니다. 데이터 요소를 사용하여 Adobe Analytics 확장 기능에서 변수 값을 할당할 수 있습니다.

다음 단계에서는 태그 속성에 설치해야 하는 [Adobe 클라이언트 데이터 레이어 확장](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/client-data-layer/overview)을 사용합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 선택합니다.
1. **[!UICONTROL 데이터 요소]** 탭을 선택한 다음 **[!UICONTROL 데이터 요소 추가]**&#x200B;를 선택합니다.

   ![데이터 요소 만들기](assets/createelement.png)

1. 데이터 요소의 이름을 입력하십시오(예: `Page name`).
1. **[!UICONTROL 확장]** 드롭다운 목록에서 **[!UICONTROL Adobe 클라이언트 데이터 레이어]**&#x200B;를 선택합니다.
1. **[!UICONTROL 데이터 요소 유형]** 드롭다운 목록에서 **[!UICONTROL 데이터 계층 계산 상태]**&#x200B;를 선택합니다.
1. **[!UICONTROL 반환 값]**&#x200B;에서 **[!UICONTROL 특정 경로]**&#x200B;을(를) 선택한 다음 데이터 계층에 있는 값에 대한 경로를 입력합니다(예: `page.name`). 경로의 유효성을 검사하려면 브라우저의 콘솔에서 `adobeDataLayer.getState("page.name")`을(를) 실행하십시오.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

확장의 **[!UICONTROL 데이터 레이어 푸시]** 이벤트가 트리거되는 규칙에서 이러한 데이터 요소를 사용하여 데이터 레이어가 로드되고 푸시의 데이터를 포함합니다. [데이터 요소 형식](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/client-data-layer/data-element-types#computed-state)을 참조하세요.

### 개체 기반 데이터 레이어 {#object-based}

데이터 레이어가 CEDL `digitalData` 개체와 같은 JavaScript 개체인 경우 대신 **[!UICONTROL Core]** 확장의 **[!UICONTROL JavaScript 변수]** 데이터 요소 유형을 사용하십시오. 값의 경로를 입력하십시오(예: `digitalData.page.pageInfo.pageName`). 이 데이터 요소 유형은 개체 속성이 아닌 계산된 상태로 데이터를 저장하는 Adobe 클라이언트 데이터 레이어를 읽을 수 없습니다.

## 다음 단계

[데이터 요소를 Analytics 변수에 매핑](elements-to-variable.md): Analysis Workspace에서 차원으로 사용할 수 있도록 데이터 요소를 Analytics 변수에 할당합니다.
