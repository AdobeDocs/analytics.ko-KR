---
description: Analytics 관리자가 Activity Map 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 완료해야 하는 절차에 대해 설명합니다.
title: Activity Map 활성화
feature: Activity Map
role: Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
mini-toc-levels: 3
source-git-commit: 75d50a5b2cd31aa11df22fa6a271f7ab937a770c
workflow-type: ht
source-wordcount: '696'
ht-degree: 100%

---


# Activity Map 활성화

Analytics 관리자가 Activity Map 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 완료해야 하는 절차에 대해 설명합니다.

## 1단계. Activity Map 활성화 {#update_code}

Activity Map 모듈은 AppMeasurement.js, Adobe Experience Platform 태그 및 Web SDK(alloy.js)의 일부입니다. **Web SDK 버전 2.15.0** 이상, **Adobe Analytics 태그 확장 기능 v1.90** 이상 또는 **AppMeasurement 버전 1.6** 이상으로 업데이트해야만 Activity Map 데이터를 수집할 수 있습니다.

+++Web SDK(Adobe Experience Platform 태그 확장 기능)

참고: Web SDK는 현재 별도의 링크 클릭 이벤트를 기록하여 Activity Map 정보를 수집합니다. 이는 후속 페이지 로드에 해당 정보를 포함시켜 내부 링크에 대한 Activity Map 정보를 기록하는 AppMeasurement와는 다릅니다. 이로 인해 Web SDK 수집은 추가 서버 호출을 발생시킵니다. Web SDK의 향후 릴리스에서는 AppMeasurement의 비헤이비어와 본질적으로 일치하는 후속 히트에 대한 Activity Map 정보를 패키징하도록 Web SDK를 구성할 수 있게 될 예정입니다.

1. Adobe Experience Platform 태그에서 Analytics를 구현하는 속성으로 이동합니다.
1. [!UICONTROL 확장] > [!UICONTROL Adobe Experience Platform Web SDK] 아래에서 강조 표시된 **[!UICONTROL 데이터 수집 클릭 활성화]**&#x200B;를 선택합니다.
1. 변경 사항을 적용하여 라이브러리를 빌드합니다.
1. 라이브러리를 프로덕션에 게시합니다.

![](assets/web_sdk.png)

**유효성 검사**

Developer Console 네트워크 탭을 사용하여 호출 상호 작용:

1. 사이트의 Development Launch 스크립트를 로드합니다.
1. 요소 클릭의 네트워크 탭에서 “/ee” 검색

   ![](assets/validation1.png)

Adobe Experience Platform Debugger:

1. [Adobe Experience Platform Debugger](https://chromewebstore.google.com/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob)를 다운로드하여 설치합니다.
1. [!UICONTROL 로그] > [!UICONTROL Edge] > [!UICONTROL Edge에 연결]로 이동합니다.

   ![](assets/validation2.jpg)

**FAQ**

* **상호 작용 호출이 네트워크 탭에서 실행되지 않습니다.**
컬렉트 콜의 데이터 수집 클릭에서 “/ee” 또는 “collect?”로 필터링해야 합니다.

* **컬렉트 콜의 경우 페이로드 디스플레이가 없습니다.**
컬렉트 콜은 추적이 기타 사이트 탐색에 영향을 주지 않도록 디자인되어서 문서 언로드 기능을 컬렉트 콜에 적용할 수 있습니다. 이는 데이터 수집에 영향을 주지 않지만, 페이지에서 유효성을 확인해야 경우 target = “_blank”를 각 요소에 추가합니다. 그런 다음 링크가 새 탭에서 열립니다.

* **PII 수집을 어떻게 무시합니까?**
&lt;&lt; 링크 클릭 전 콜백 전송>>에 각 조건을 추가하고 해당 값을 무시하려면 false를 반환합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)

  코드 샘플:

  ![](assets/sample-code.png)

+++

+++수동 Web SDK 구현

클릭한 HTML 요소의 `region`를 캡처하여 링크 추적을 구현하는 방법과 Activity Map을 활성화하는 방법에 대한 자세한 내용은 [추적 링크](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html)를 참조하십시오.

>[!NOTE]
>
>Web SDK로 링크 추적을 활성화하면 현재 고객이 하나의 페이지에서 다음 페이지로 이동할 때 링크 이벤트를 전송합니다. 이는 AppMeasurement가 작동하는 방식과 다르며 잠재적으로 Adobe로 전송되는 추가 청구 가능 히트를 초래할 수 있습니다.

+++

+++Analytics 확장 기능(Adobe Experience Platform 태그)

Adobe Experience Platform 태그에서 Analytics를 구현하는 속성으로 이동합니다. [!UICONTROL 확장 기능 설치] 대화 상자에서 **[!UICONTROL Activity Map 사용]**&#x200B;을 선택합니다.

![](assets/aa_extension.png)

+++

+++AppMeasurement

1. AppMeasurement의 최신 JavaScript 라이브러리를 다운로드합니다.
**[!UICONTROL Analytics]** > **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 코드 관리자]**&#x200B;로 이동합니다.
1. [이 지침](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html)에 따라 구현합니다.

+++

## 2단계. Activity Map 보고서 활성화 {#enable}

보고서 세트 수준에서 Activity Map 보고서를 활성화해야 합니다.

1. Adobe Analytics에 로그인하고 **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > 보고서 세트 선택 > **[!UICONTROL 설정 편집]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map 보고]**&#x200B;로 이동합니다.

1. Activity Map에서는 Activity Map 보고서에 있는 링크 데이터를 수집합니다. 활성화가 수행되도록 하려면 **[!UICONTROL Activity Map 보고서 활성화]**&#x200B;를 클릭하여 변수를 먼저 활성화합니다.

   이 단계에서는 데이터를 수집하는 데 필요한 모든 Analytics 차원이 추가됩니다.

   ![](assets/enable.png)

1. 약 1시간 후 사용자가 링크를 클릭한 모든 페이지를 보여 주는 [Activity Map 페이지 보고서](/help/analyze/activity-map/activitymap-reporting-analytics.md)를 확인하십시오.

## 3단계. [!UICONTROL Activity Map Access] 제품 프로필에 사용자 추가 {#add_users}

1. **[!UICONTROL 그룹에 사용자 추가]**&#x200B;를 클릭합니다.

   이렇게 하면 [Adobe Admin Console](https://adminconsole.adobe.com/E2F05B3B52F54D2E0A490D44@AdobeOrg/overview)에 제품 프로필 페이지가 표시됩니다.

1. [!UICONTROL Activity Map 액세스]제품 프로필을 만들지 않았다면 지금 만듭니다. 이 프로필에 필요한 권한 항목은 [!UICONTROL Analytics 도구] > [!UICONTROL Activity Map] 및 [!UICONTROL Analytics 도구] > [!UICONTROL  세그먼트 게시]입니다.

1. 사용자를 해당 제품 프로필에 추가합니다. 이렇게 하면 사용자는 **[!UICONTROL Adobe Analytics]** > **[!UICONTROL 도구]** > **[!UICONTROL ActivityMap]**&#x200B;에서 Activity Map을 다운로드할 수 있습니다.

