---
description: Analytics 관리자가 Activity Map 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 완료해야 하는 절차에 대해 설명합니다.
title: Activity Map 활성화
feature: Activity Map
role: Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
mini-toc-levels: 3
source-git-commit: 4c6df8bc08f326bfb54b27eb61f97b4be2320805
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 27%

---


# Activity Map 활성화 및 활성화

Analytics 관리자가 Activity Map 링크 컬렉션 및 사용자 다운로드를 활성화하기 위해 완료해야 하는 절차에 대해 설명합니다.

## 1단계. Activity Map 활성화 {#update_code}

Activity Map 모듈은 AppMeasurement.js, Adobe Experience Platform 태그 및 웹 SDK(alloy.js)의 일부입니다. 을(를) 업데이트하지 않으면 Activity Map 데이터를 수집할 수 없습니다. **Web SDK 버전 2.15.0** 또는 그 이상 **Adobe Analytics 태그 확장 v1.90** 또는 그 이상 **AppMeasurement 버전 1.6** 또는 그 이상

+++Web SDK (Adobe Experience Platform 태그 확장)

1. Adobe Experience Platform 태그에서 Analytics를 구현하는 속성으로 이동합니다. 아래 [!UICONTROL 확장] -> [!UICONTROL Adobe Experience Platform 웹 SDK], 선택 **[!UICONTROL 클릭 데이터 수집 활성화]** 아래에 강조 표시된 대로.
1. 변경 사항을 사용하여 라이브러리를 빌드합니다.
1. 라이브러리를 프로덕션에 게시합니다.

![](assets/web_sdk.png)

**유효성 검사**

Developer Console 네트워크 탭을 사용하여 호출 상호 작용:

1. 사이트에서 Development Launch 스크립트를 로드합니다.
1. 요소 클릭 시 네트워크 탭에서 &#39;/ee&#39;를 검색합니다.

   ![](assets/validation1.png)

Adobe Experience Platform Debugger:

1. 다운로드 및 설치 [Adobe Experience Platform 디버거](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpo).
1. 다음으로 이동 [!UICONTROL 로그] > [!UICONTROL Edge] > [!UICONTROL Edge에 연결].

   ![](assets/validation2.jpg)

**FAQ**

* **Interact 호출이 Network 탭에서 실행되지 않습니다.**
데이터 수집 호출 시 클릭 데이터 수집을 &quot;/ee&quot; 또는 &quot;collect?&quot;로 필터링해야 합니다.

* **수신자 호출에 대한 페이로드 표시가 없습니다.**
수집 호출은 추적이 다른 사이트로의 탐색에 영향을 주지 않는 방식으로 설계되었으므로, 수집 호출에 문서 언로드 기능을 적용할 수 있습니다. 데이터 수집에는 영향을 주지 않지만 페이지에서 유효성을 검사해야 하는 경우 target = &quot;_blank&quot;를 각 요소에 추가하십시오. 그런 다음 링크가 새 탭에서 열립니다.

* **PII 컬렉션을 어떻게 무시합니까?**
링크 클릭 전&lt;&lt; on 콜백>>에 해당 조건을 추가하고 false를 반환하여 해당 값을 무시합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)

  샘플 코드:

  ![](assets/sample-code.png)

+++

+++수동 웹 SDK 구현

다음을 참조하십시오 [링크 추적](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html) 링크 추적을 구현하는 방법 및 을 캡처하여 Activity Map을 활성화하는 방법에 대한 자세한 내용 `region` HTML 를 클릭합니다.

>[!NOTE]
>
>웹 SDK를 사용하여 링크 추적을 활성화하면 현재 고객이 한 페이지에서 다음 페이지로 이동할 때 링크 이벤트가 전송됩니다. 이는 AppMeasurement가 작동하는 방식과 다르며 잠재적으로 Adobe로 전송되는 추가 청구 가능 히트를 초래할 수 있습니다.

+++

+++Analytics 확장 프로그램 (Adobe Experience Platform 태그)

Adobe Experience Platform 태그에서 Analytics를 구현하는 속성으로 이동합니다. 다음에서 [!UICONTROL 확장 설치] 대화 상자, 선택 **[!UICONTROL Activity Map 사용]**.

![](assets/aa_extension.png)

+++

+++AppMeasurement

1. AppMeasurement을 위한 최신 Javascript 라이브러리를 다운로드합니다.
다음으로 이동 **[!UICONTROL 분석]** > **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 코드 관리자]**.
1. 다음을 통해 구현 [이 지침](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html).

+++

## 2단계. Activity Map 보고서 활성화 {#enable}

보고서 세트 수준에서 Activity Map 보고서를 활성화해야 합니다.

1. Adobe Analytics에 로그인하고 **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > 보고서 세트 선택 > **[!UICONTROL 설정 편집]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map 보고]**&#x200B;로 이동합니다.

1. Activity Map에서는 Activity Map 보고서에 있는 링크 데이터를 수집합니다. 활성화가 수행되도록 하려면 **[!UICONTROL Activity Map 보고서 활성화]**&#x200B;를 클릭하여 변수를 먼저 활성화합니다.

   이 단계에서는 데이터를 수집하는 데 필요한 모든 Analytics 차원이 추가됩니다.

   ![](assets/enable.png)

1. 약 1시간 후, 사용자가 링크를 클릭한 모든 페이지를 보여 주는 [Activity Map 페이지 보고서](/help/analyze/activity-map/activitymap-reporting-analytics.md)를 확인하십시오.

## 3단계. 에 사용자 추가 [!UICONTROL Activity Map 액세스] 제품 프로필 {#add_users}

1. **[!UICONTROL 그룹에 사용자 추가]**&#x200B;를 클릭합니다.

   이렇게 하면 의 제품 프로필 페이지로 이동합니다. [Adobe Admin Console](https://adminconsole.adobe.com/E2F05B3B52F54D2E0A490D44@AdobeOrg/overview).

1. 을(를) 만들지 않은 경우 [!UICONTROL Activity Map 액세스] 제품 프로필로 지금 바로 예약하십시오. 이 프로필에 필요한 권한 항목은 다음과 같습니다. [!UICONTROL Analytics 도구] > [!UICONTROL Activity Map] 및 [!UICONTROL Analytics 도구] > [!UICONTROL 세그먼트 게시].

1. 해당 제품 프로필에 사용자를 추가합니다. 이렇게 하면 사용자가에서 Activity Map을 다운로드할 수 있습니다.  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL 도구]** > **[!UICONTROL ActivityMap]** .

