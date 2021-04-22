---
description: 모바일 서비스 처리 규칙을 Adobe Analytics로 마이그레이션하는 방법에 대해 알아봅니다.
title: 모바일 서비스 처리 규칙을 Adobe Analytics로 마이그레이션
exl-id: ea183c1a-a85e-4f4e-a7f6-f947b939e9d9
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '686'
ht-degree: 100%

---

# 모바일 서비스 처리 규칙을 Adobe Analytics로 마이그레이션

이 문서는 모바일 서비스 UI에서 생성한 추가 처리 규칙 (라이프사이클 지표 이외)을 Adobe Analytics로 마이그레이션하는 방법에 대한 지침을 제공합니다.

처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 prop 및 eVar로 이동합니다. 예를 들어 “검색어” 컨텍스트 데이터 변수의 값을 상거래 변수 eVar의 값에 배치하고 모든 히트에 해당 값을 덮어쓸 수 있습니다. 처리 규칙이 없으면 컨텍스트 데이터 변수는 의미가 없으며 Analytics에 보고서를 채우지 않습니다.

이 문서는 Analysis Workspace에서 모바일 사용 현황 보고를 수행하는 방법도 보여줍니다.

## 처리 규칙 마이그레이션

처리 규칙 및 사용 현황 보고 기능과 같은 무료 기능에 모바일 서비스를 활용하는 경우 분석 UI (처리 규칙 UI 또는 Analysis Workspace)로 원활하게 이동하여 이러한 기능을 수행할 수 있습니다. 라이프사이클 지표 또는 AA 처리 규칙 UI에서 설정된 규칙의 경우 마이그레이션을 수행할 필요가 없습니다. 라이프사이클 지표는 모바일 SDK가 앱에서 처음 구현될 때 자동으로 수집되는 “기본 제공” 지표입니다.

그러나 모바일 서비스 UI (라이프사이클 지표 이외)에서 추가 처리 규칙을 설정한 경우 모바일 서비스에 대한 액세스 권한을 잃은 후에 Analytics에서 편집/삭제할 수 있도록 이를 마이그레이션해야 합니다.

1. `experience.adobe.com`에 로그인하고 모바일 서비스로 이동합니다.
1. 컨텍스트 변수 매핑을 Adobe Analytics로 마이그레이션하려는 모바일 앱의 톱니 바퀴 아이콘을 클릭합니다.
1. **[!UICONTROL 변수 및 지표 관리]** 메뉴 항목을 클릭한 다음&#x200B;**[!UICONTROL 사용자 지정 변수]** 탭을 클릭합니다. 여기에서 구성에 추가된 컨텍스트 변수 매핑 (컨텍스트 데이터)을 확인할 수 있습니다. 이러한 구성을 기록해 두거나 스크린 샷을 찍으십시오. 예:

   ![컨텍스트 변수](assets/context-var.png)

1. Experience Cloud에서 Adobe Analytics로 전환하고 Mobile Services에서 보고 있었던 모바일 보고서 세트와 동일한 것에 있는지 확인합니다.
1. **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 처리 규칙]**&#x200B;으로 이동합니다.
1. **[!UICONTROL 규칙 추가]**&#x200B;를 클릭합니다.
1. 조건을 무시하고 계속해서 모바일 서비스에 존재하는 동일한 컨텍스트 변수를 추가합니다.

   ![처리 규칙](assets/proc-rule.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## Analysis Workspace의 모바일 사용 현황 보고

모바일 지표 및 차원 (보고서 세트가 모바일 서비스에 대해 활성화된 경우) 외에도 Analysis Workspace에는 분석을 용이하게 할 수 있는 여러 모바일 프로젝트 템플릿이 포함되어 있습니다.

* **[!UICONTROL 메시지]**: 인앱 및 푸시 메시징 성능에 중점을 둡니다.
* **[!UICONTROL 위치]**: 위치 데이터를 보여주는 지도를 포함합니다.
* **[!UICONTROL 주요 지표]**: 앱의 주요 지표에 대한 최신 정보를 지속적으로 확인합니다.
* **[!UICONTROL 앱 사용]**: 앱이 보유한 앱 사용자, 실행 횟수, 앱이 처음 실행된 횟수가 얼마나 되며 평균 세션 길이는 얼마입니까?
* **[!UICONTROL 확보]**: 모바일 확보 링크의 성능은 어떻습니까?
* **[!UICONTROL 성능]**: 앱 성능은 어떻고 사용자에게 문제가 발생하는 위치는 어디입니까?
* **[!UICONTROL 유지]**: 충성도 높은 사용자는 누구이며 그들이 무슨 작업을 수행합니까?
* **[!UICONTROL 여정]**: 내 앱의 두드러진 사용 패턴은 무엇입니까?

다음은 모바일 앱 사용 현황 템플릿의 일부입니다.

![모바일 앱 사용 현황](assets/mobile-app-usage.png)

템플릿에 액세스하려면 다음을 수행하십시오.

1. `experience.adobe.com`에 로그인하고 Analytics를 선택합니다.
1. 모바일 서비스에 대해 활성화된 보고서 세트에 있는지 확인합니다.
1. **[!UICONTROL Workspace]** 탭을 클릭합니다.
1. **[!UICONTROL 새 프로젝트 만들기]**&#x200B;를 클릭합니다.
1. 모바일 템플릿을 선택하고 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

## 다른 모바일 서비스 기능 마이그레이션

다음 모바일 서비스 기능도 Adobe Analytics와 연결되어 있지만 구입한 Adobe Analytics SKU가 필요합니다.

* 획득 링크
* 푸시 메시지
* In-App 메시징
* 위치 안내 표시 관리

유료 기능을 위해 모바일 서비스를 활용하면 다른 내부/외부 도구에 대한 실행 가능한 마이그레이션 경로가 없습니다.

* 확보 링크의 경우 Adobe 파트너로 안내하여 그러한 요구를 충족시킬 수 있습니다.
* 푸시 메시징 및 인앱 메시징은 Adobe Campaign Standard 및 Adobe Campaign Classic (푸시 전용)에서 사용할 수 있습니다. 그러나 타겟팅에 사용되는 기본 데이터 세트는 다릅니다. 메시징 데이터에 대한 마이그레이션 옵션을 결정하기 위해 Adobe 계정 팀과 협력하는 것이 좋습니다.
* 위치 기능의 경우 모든 AEP 고객에게 무료로 제공되는 새로운 [Adobe Experience Platform 위치 서비스](https://www.adobe.com/experience-platform/location-service.html)를 채택하는 것이 좋습니다.
