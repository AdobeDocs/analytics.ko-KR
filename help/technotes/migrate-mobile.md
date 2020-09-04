---
description: Mobile Services 처리 규칙을 Adobe Analytics으로 마이그레이션하는 방법 살펴보기
title: Mobile Services 처리 규칙을 Adobe Analytics으로 마이그레이션
translation-type: tm+mt
source-git-commit: d6601640d06f65dd1ddd09cb9bde0267df20eec3
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 6%

---


# Mobile Services 처리 규칙을 Adobe Analytics으로 마이그레이션

이 문서에서는 라이프사이클 지표를 넘어 Mobile Services UI에서 만든 추가 처리 규칙을 Adobe Analytics으로 마이그레이션하는 방법에 대한 지침을 제공합니다.

처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 prop 및 eVar로 이동합니다. 예를 들어 &quot;search-term&quot; 컨텍스트 데이터 변수의 값을 상거래 변수 eVar의 값으로 가져와서 모든 히트에 해당 값을 덮어쓸 수 있습니다. 처리 규칙이 없으면 컨텍스트 데이터 변수는 의미가 없으며 Analytics에 보고서를 채우지 않습니다.

이 문서에서는 Analysis Workspace에서 모바일 사용량 보고를 하는 방법도 보여 줍니다.

## 처리 규칙 마이그레이션

처리 규칙 및 사용 보고 기능과 같은 무료 기능에 Mobile Services를 활용하는 경우 Analytics UI(처리 규칙 UI 또는 Analysis Workspace)으로 원활하게 이동하여 이러한 기능을 수행할 수 있습니다. 라이프사이클 지표 또는 AA 처리 규칙 UI에 설정된 규칙의 경우 마이그레이션을 수행할 필요가 없습니다. 라이프사이클 지표는 Mobile SDK가 앱에서 처음 구현되면 자동으로 수집되는 &quot;즉시 사용 가능한&quot; 지표입니다.

그러나 Mobile Services UI(라이프사이클 지표를 넘어)에서 추가 처리 규칙을 설정하는 경우, Mobile Services에 대한 액세스 권한이 없어진 후 Analytics에서 이러한 규칙을 편집/삭제할 수 있도록 마이그레이션해야 합니다.

1. Log in to `experience.adobe.com` and go to Mobile Services.
1. Adobe Analytics으로 마이그레이션하려는 컨텍스트 변수 매핑이 있는 모바일 앱의 톱니바퀴 아이콘을 클릭합니다.
1. 변수 **[!UICONTROL 및 지표]** 관리 메뉴 항목을 클릭한 다음 **[!UICONTROL 사용자 지정 변수]** 탭을 클릭합니다. 여기에서 구성에 추가된 컨텍스트 변수 매핑(컨텍스트 데이터)을 확인할 수 있습니다. 이러한 구성에 대해 메모하거나 스크린샷을 만듭니다. 예:

   ![컨텍스트 변수](assets/context-var.png)

1. Experience Cloud에서 Adobe Analytics으로 전환하여 Mobile Services에서 보고 있던 동일한 모바일 보고서 세트에 있는지 확인합니다.
1. 관리 > **[!UICONTROL 보고서]** 세트 **[!UICONTROL > 설정]** **[!UICONTROL 편집]** > 일반 **[!UICONTROL >처리 규칙]** ****&#x200B;으로 이동합니다.
1. Click **[!UICONTROL Add Rule]**.
1. 조건을 무시하고 Mobile Services에 있는 동일한 컨텍스트 변수를 추가합니다.

   ![처리 규칙](assets/proc-rule.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## Analysis Workspace의 모바일 사용량 보고

모바일 지표 및 차원(보고서 세트가 Mobile Services에 대해 활성화된 경우) 외에도, Analysis Workspace에는 분석을 용이하게 하는 여러 모바일 프로젝트 템플릿이 포함되어 있습니다.

* **[!UICONTROL 메시지]**:인앱 및 푸시 메시지 성능에 중점을 둡니다.
* **[!UICONTROL 위치]**:맵 표시 위치 데이터를 포함합니다.
* **[!UICONTROL 주요 지표]**:앱의 주요 지표에 대한 최신 정보를 확인하십시오.
* **[!UICONTROL 앱 사용]**:앱의 사용자 수, 실행 횟수 및 첫 번째 실행 횟수는 몇 명이며 평균 세션 길이는 얼마입니까?
* **[!UICONTROL 획득]**:모바일 획득 링크는 어떤 방식으로 수행됩니까?
* **[!UICONTROL 성능]**:앱의 성능과 사용자에게 문제가 있는 곳은 어디입니까?
* **[!UICONTROL 보존]**:충성도 높은 사용자는 누구이며 어떻게 해야 합니까?
* **[!UICONTROL 여정]**:내 앱에 대해 두드러진 사용 패턴은 무엇입니까?

다음은 모바일 앱 사용 템플릿의 일부입니다.

![모바일 앱 사용](assets/mobile-app-usage.png)

템플릿에 액세스하려면

1. Log in to `experience.adobe.com` and select Analytics.
1. Mobile Services에 대해 활성화된 보고서 세트에 있는지 확인합니다.
1. Click the **[!UICONTROL Workspace]** tab.
1. **[!UICONTROL 새 프로젝트 만들기]**&#x200B;를 클릭합니다.
1. 모바일 템플릿 중 하나를 선택하고 만들기를 **[!UICONTROL 클릭합니다]**.

## 다른 Mobile Services 기능 마이그레이션

다음 모바일 서비스 기능도 Adobe Analytics과 연계되어 있지만 구입한 Adobe Analytics SKU가 필요합니다.

* 획득 링크
* 푸시 메시지
* In-App 메시징
* 관심 영역 관리

유료 기능에 Mobile Services를 활용하는 경우 다른 내부/외부 도구에 실행 가능한 마이그레이션 경로가 없습니다.

* 획득 링크의 경우, Adobe는 고객의 요구를 충족하도록 Adobe 파트너에게 안내할 수 있습니다.
* 푸시 메시지 및 인앱 메시지는 Adobe Campaign Standard 및 Adobe Campaign Classic에서 사용할 수 있습니다(푸시 전용). 하지만 타깃팅에 사용되는 기본 데이터 세트는 다릅니다. 메시지 데이터에 대한 마이그레이션 옵션을 결정하려면 Adobe 계정 팀과 함께 작업하는 것이 좋습니다.
* 위치 기능의 경우 모든 AEP 고객에게 무료로 제공되는 새로운 [Adobe Experience Platform 위치 서비스](https://www.adobe.com/experience-platform/location-service.html)사용을 권장합니다.
