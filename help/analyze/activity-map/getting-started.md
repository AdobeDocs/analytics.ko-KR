---
title: Activity Map 시작하기
description: Activity Map 오버레이 및 차원 사용을 시작합니다.
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: a7670fcda3e8e6af0c036c8b263746e142278255
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 100%

---

# Activity Map 시작하기

Adobe Analytics의 Activity Map은 네 가지 주요 요소로 구성됩니다.

* **보고서 세트 설정**: 보고서 세트 설정에서 Activity Map을 사용하도록 설정해야 합니다. 활성화되면 보고서 세트는 Activity Map 차원 및 지표에 대해 예약된 변수를 여러 개 만듭니다.
* **구현**: 웹 사이트 또는 속성에서 Activity Map 데이터를 수집합니다. 데이터 수집 방법을 사용자 정의하면 보고서의 품질과 경험을 향상시킬 수 있습니다.
* **Workspace 차원 및 지표**: 구현이 올바르게 구성되면 Analysis Workspace에서 Activity Map 차원 및 지표를 사용할 수 있습니다.
* **오버레이**: Adobe는 웹 사이트 컨텍스트에서 Activity Map 데이터를 볼 수 있는 브라우저 확장 기능을 제공합니다. 이 기능은 웹 SDK 구현에 사용할 수 없습니다.

## 보고서 세트 설정 활성화

데이터 수집을 시작하려면 보고서 세트에 Activity Map 보고를 활성화해야 합니다. 구현에서 Activity Map 보고 기능을 활성화하지 않은 상태에서 Activity Map 데이터를 보고서 세트로 전송하는 경우 Activity Map 데이터가 히트에 포함되지 않습니다.

**[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > 보고서 세트 선택 > **[!UICONTROL 설정 편집]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map 보고]** > **[!UICONTROL Activity Map 보고서 활성화]**

Activity Map 보고서를 활성화하면 몇 가지 백엔드 예약 변수가 만들어집니다. 자세한 내용은 [Activity Map 보고](/help/admin/tools/manage-rs/edit-settings/activity-map.md) Adobe Analytics 관리 안내서를 참조하십시오.

## 코드 설치

Adobe로 Activity Map 데이터를 보내도록 구현을 올바르게 구성해야 합니다. 웹 SDK을 사용하여 Adobe Analytics을 구현하는 경우 오버레이 브라우저 확장 기능을 사용할 수 없습니다.

+++웹 SDK 태그 확장 기능

Activity Map 데이터 수집을 사용하려면 **[!UICONTROL Adobe Experience Platform 웹 SDK]** 확장 기능 v2.23 이상이 필요합니다. v2.16까지의 확장 기능 버전은 지원이 제한되어 있습니다. 이전 확장 기능 버전은 Activity Map 데이터를 나머지 데이터와 별도의 이벤트로 보냅니다. 이 추가 이벤트는 Adobe Analytics 또는 Adobe Experience Platform으로 보내는 히트 수를 증가시킵니다.

**[!UICONTROL 데이터 수집 클릭]** 구성 설정은 Activity Map 데이터 수집을 처리하며 일반적으로 기본값은 활성화 상태입니다. 확장 기능의 구성 설정에서 활성화되어 있는지 확인할 수 있습니다.

1. [experience.adobe.com](https://experience.adobe.com)에 로그인합니다.
1. 바로 가기 메뉴 또는 오른쪽 상단의 제품 선택기에서 **[!UICONTROL 데이터 수집]**&#x200B;을 선택합니다.
1. 왼쪽 탐색 메뉴에서 **[!UICONTROL 태그]**&#x200B;를 선택합니다.
1. 편집하려면 원하는 태그를 선택합니다.
1. 왼쪽 탐색 메뉴에서 **[!UICONTROL 확장 기능]**&#x200B;을 선택합니다.
1. 설치된 확장 기능 목록에서 **[!UICONTROL Adobe Experience Platform 웹 SDK]**&#x200B;를 선택한 다음 오른쪽에 있는 **[!UICONTROL 구성]**&#x200B;을 선택합니다.
1. [!UICONTROL 데이터 수집] 섹션을 찾아 **[!UICONTROL 데이터 수집 클릭 활성화]** 확인란이 활성화되어 있는지 확인합니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 필요한 경우 라이브러리에 변경 사항을 작성하고 프로덕션에 대한 변경 사항을 게시합니다.

자세한 내용은 [웹 SDK 태그 확장 기능](https://experienceleague.adobe.com/kr/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#data-collection)을 참조하십시오.

+++

+++웹 SDK JavaScript 라이브러리 (`alloy.js`)

Activity Map 데이터 수집을 사용하려면 웹 SDK JavaScript 라이브러리 v2.20 이상이 필요합니다. v2.15까지의 라이브러리 버전은 지원이 제한되어 있습니다. 이전 라이브러리 버전은 Activity Map 데이터를 나머지 데이터와 별도의 이벤트로 보냅니다. 이 추가 이벤트는 Adobe Analytics 또는 Adobe Experience Platform으로 보내는 히트 수를 증가시킵니다.

웹 SDK 구성 변수 [`clickCollectionEnabled`](https://experienceleague.adobe.com/kr/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled)는 Activity Map 데이터의 자동 수집을 처리합니다. 명시적으로 비활성화되지 않는 한 기본값은 활성화되어 있습니다.

```js
alloy("configure", {
  datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg",
  clickCollectionEnabled: true
});
```

+++

+++Adobe Analytics 태그 확장 기능

**[!UICONTROL Activity Map 사용]** 구성 설정은 Activity Map 데이터 수집을 처리하며 일반적으로 기본값은 활성화 상태입니다. 모든 태그 확장 기능 v1.9.0 이상에서 사용할 수 있습니다. 확장 기능의 구성 설정에서 활성화되어 있는지 확인할 수 있습니다.

1. [experience.adobe.com](https://experience.adobe.com)에 로그인합니다.
1. 바로 가기 메뉴 또는 오른쪽 상단의 제품 선택기에서 **[!UICONTROL 데이터 수집]**&#x200B;을 선택합니다.
1. 왼쪽 탐색 메뉴에서 **[!UICONTROL 태그]**&#x200B;를 선택합니다.
1. 편집하려면 원하는 태그를 선택합니다.
1. 왼쪽 탐색 메뉴에서 **[!UICONTROL 확장 기능]**&#x200B;을 선택합니다.
1. 설치된 확장 기능 목록에서 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택한 다음 오른쪽의 **[!UICONTROL 구성]**&#x200B;을 선택합니다.
1. **[!UICONTROL Activity Map 사용]** 확인란이 활성화되어 있는지 확인합니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 필요한 경우 라이브러리에 변경 사항을 작성하고 프로덕션에 대한 변경 사항을 게시합니다.

자세한 정보는 [Adobe Analytics 확장 기능 개요](https://experienceleague.adobe.com/kr/docs/experience-platform/tags/extensions/client/analytics/overview)를 참조하십시오.

+++

+++Adobe Analytics JavaScript 라이브러리(`AppMeasurement.js`)

Activity Map 모듈은 Activity Map 데이터 수집을 처리하며 모든 AppMeasurement 라이브러리 v1.6 이상에 포함됩니다. `AppMeasurement.js` 파일이 포함되어 있는지 검사할 수 있습니다.

1. GitHub의 [최신 Adobe Analytics AppMeasurement 릴리스](https://github.com/adobe/appmeasurement/releases/latest)로 이동합니다.
1. 압축된 AppMeasurement 라이브러리 파일을 다운로드한 다음 안에 포함된 `AppMeasurement.js`를 엽니다.
1. Activity Map 모듈은 이 파일의 상단 근처에 포함됩니다. 이 모듈이 사이트에서 사용하는 AppMeasurement 라이브러리에 포함되어 있는지 확인합니다.

+++

## 사용 가능한 차원

Activity Map이 보고서 세트와 구현 모두에 대해 활성화되어 있으면 Analysis Workspace에서 다음 차원을 사용할 수 있습니다.

* [[!UICONTROL Activity Map 링크]](/help/components/dimensions/activity-map-link.md)
* [[!UICONTROL Activity Map 지역]](/help/components/dimensions/activity-map-region.md)
* [[!UICONTROL Activity Map 페이지]](/help/components/dimensions/activity-map-page.md)
* [[!UICONTROL 지역별 Activity Map 링크]](/help/components/dimensions/activity-map-link-by-region.md)

## 브라우저 확장 기능 또는 추가 기능 다운로드 및 설치

Analysis Workspace에서 사용할 수 있는 차원 외에도 웹 사이트에서 Activity Map 데이터를 오버레이로 볼 수 있습니다. 이 오버레이를 보려면 Activity Map 브라우저 확장 기능 또는 추가 기능을 다운로드하여 설치하십시오.

**[!UICONTROL 도구]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map 다운로드]**

이 링크를 통해 브라우저의 지원 확장 기능 또는 추가 기능 마켓플레이스로 이동하여 설치할 수 있습니다. 설치되면 브라우저 오른쪽 상단에 로그인하여 오버레이를 활성화할 수 있는 확장 기능 또는 추가 기능이 나타납니다.
