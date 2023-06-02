---
description: 작업 영역의 프로젝트 공유 및 프로젝트 역할
keywords: Analysis Workspace 공유
title: 프로젝트 공유
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 8aca2f068a455eddca904d0367bc4a282f464e56
workflow-type: tm+mt
source-wordcount: '1852'
ht-degree: 52%

---

# 프로젝트 공유

다음 유형의 사용자와 Analysis Workspace 프로젝트를 공유할 수 있습니다.

* Adobe Analytics에 액세스할 수 있는 조직의 사용자 및 그룹

   편집, 복제 또는 보기 액세스 권한을 공유할 수 있습니다.

* Adobe Analytics 액세스 권한이 없는 조직의 사용자 및 그룹

   수신자는 읽기 전용 액세스 권한을 가집니다.

* 조직 외부의 사용자

   수신자는 읽기 전용 액세스 권한을 가집니다.

임의 [큐레이션](curate.md) 수신자가 프로젝트를 열 때 공유하기 전에 적용합니다.

다음은 프로젝트 공유에 대한 비디오 개요입니다.

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## 조직의 Analysis Workspace 사용자 및 그룹과 공유 {#Add}

조직의 기존 Analysis Workspace 사용자 또는 그룹과 프로젝트를 공유할 수 있습니다. 이 섹션에 설명된 대로 프로젝트를 공유할 때 공유하는 사용자는 이미 Adobe Analytics에 액세스할 수 있어야 합니다.

사용자 또는 그룹과 특정 역할을 공유하거나 링크를 공유할 수 있습니다.

* [특정 프로젝트 역할 공유](#share-a-specific-project-role)

* [프로젝트에 대한 링크 공유](#share-a-link-to-a-project)

## 특정 프로젝트 역할 공유

조직의 사용자 및 그룹과 특정 프로젝트 역할을 공유할 때는 다음을 고려해 보십시오.

* 프로젝트 역할(**[!UICONTROL 편집 가능]**, **[!UICONTROL 복제 가능]** 및 **[!UICONTROL 보기 가능]**)은 사용자 및 특정 프로젝트 ID에 연결되어 있습니다. 프로젝트 역할은 [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR)에서 관리하는 사용자 권한과 다릅니다.

* Adobe Analytics에서 그룹은 [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR)에서 제품 프로필로 정의됩니다. 관리자는 “모두”를 비롯한 모든 그룹과 공유할 수 있습니다. 관리자가 아닌 사용자는 “모두”를 제외하고 자신이 구성원으로 있는 그룹과 공유할 수 있습니다.

* 여러 역할에 배치된 사용자는 항상 가장 높은 경험을 받게 됩니다. 사용자가 개인과 그룹의 일부로 모두 추가되는 경우 여러 역할에 배치될 수 있습니다. 예를 들어 사용자에게 개인으로서 **[!UICONTROL 편집 가능]** 역할이 주어지고 및 그룹의 구성원으로 **[!UICONTROL 보기 가능]** 역할이 주어지면 해당 사용자에게는 **[!UICONTROL 편집 가능]** 프로젝트 경험이 제공됩니다.

* **[!UICONTROL 복제 가능]** 또는 **[!UICONTROL 보기 가능]** 역할에 배치된 관리자는 프로젝트를 열 때 제한된 경험을 받게 됩니다. 원하는 경우 관리자는 **[!UICONTROL 구성 요소] > [!UICONTROL 프로젝트]**&#x200B;를 통해 언제든지 자신의 역할을 **[!UICONTROL 편집 가능]**&#x200B;으로 확장할 수 있습니다.

조직의 사용자 또는 그룹과 특정 프로젝트 역할을 공유하려면 다음 작업을 수행합니다.

1. 공유할 프로젝트로 이동한 다음 **[!UICONTROL 공유]** > **[!UICONTROL 작업 공간 사용자와 공유]**.
저장하지 않은 변경 내용이 있는 경우 먼저 프로젝트를 저장하라는 메시지가 표시됩니다.

   ![](assets/share-proj-modal.png)

   여러 프로젝트를 동시에 공유하는 방법에 대한 자세한 내용은 [프로젝트 관리자에서 프로젝트 공유](#share-projects-in-the-project-manager)를 참조하십시오.

1. 제공된 역할 필드 중 하나에 수신자 또는 수신자 그룹을 추가합니다.

   **편집 가능:** 수신자는 프로젝트 및 기능에 대한 변경 내용을 공동 소유자로서 **[!UICONTROL 저장]**&#x200B;할 수 있습니다. 이 역할은 프로젝트를 다른 동료와 공동 관리하려는 경우 유용합니다. 여기에는 공유 프로젝트에 대한 수신자 목록 편집, 삭제 및 수정 등이 포함됩니다. <br>참고: Analysis Workspace는 현재 라이브 공동 작업을 지원하지 않으므로 주어진 시간에 한 명의 사용자만 프로젝트를 편집하는 것이 좋습니다. 프로젝트를 동시에 저장하는 경우 마지막 버전이 유지됩니다.

   **복제 가능:** 수신자는 **[!UICONTROL 다른 이름으로 저장]**&#x200B;하고 왼쪽 레일에 액세스할 수 있습니다. 이 역할에서는 프로젝트 상호 작용이 제한되지 않습니다. 이 역할은 조직의 데이터를 이해하고 Analysis Workspace 사용 방법을 알고 있지만 프로젝트를 변경하지 않으려는 사용자에게 프로젝트를 공유하려는 경우에 유용합니다.

   **보기 가능:** 수신자는 **[!UICONTROL 저장]** 또는 **[!UICONTROL 다른 이름으로 저장]**&#x200B;할 수 없으며 왼쪽 레일에 액세스할 수 없습니다. 상호 작용이 제한됩니다. 이 역할은 일반적으로 조직의 데이터 구조, Analysis Workspace 또는 Adobe Analytics에 익숙하지 않은 사용자에게 프로젝트를 공유하려는 경우에 유용합니다. 그럼에도 불구하고, 안전한 환경에서 데이터와 인사이트를 소비해야 합니다. [보기 가능 프로젝트 경험](/help/analyze/analysis-workspace/curate-share/view-only-projects.md)에 대해 자세히 알아보십시오.

1. 프로젝트를 공유할 때 다음 옵션을 활성화할지 여부를 선택합니다.

   * **임베드된 프로젝트 구성 요소 공유:** 모든 수신자와 세그먼트, 계산된 지표 및 날짜 범위를 공유합니다. 이러한 구성 요소가 공유되면 수신자 작업 영역의 [구성 요소] 드롭다운에 표시됩니다. 이 설정은 공유 시점에만 수행되는 일회성 작업으로, 유지되지 않습니다.

   * **수신자의 랜딩 페이지로 설정:** 이 페이지를 수신자의 랜딩 페이지로 설정합니다. 이 설정은 공유 시점에만 수행되는 일회성 작업으로, 유지되지 않습니다.

1. **[!UICONTROL 공유]**&#x200B;를 클릭합니다. (프로젝트가 이미 공유된 경우 [!UICONTROL **업데이트**].)

   또는

   클릭 **[!UICONTROL 선별 및 공유]** 프로젝트 조정을 자동으로 적용합니다. (프로젝트가 이미 공유된 경우 **[!UICONTROL 조정 및 업데이트]**.) [프로젝트 조정](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=ko-KR)에 대한 자세한 내용을 살펴보십시오.

## 프로젝트에 대한 링크 공유

이 섹션에 설명된 대로 링크를 공유할 때는 다음을 고려해 보십시오.

* 링크를 사용하는 수신자는 프로젝트에 대한 액세스 권한을 얻기 전에 Adobe Analytics에 로그인해야 합니다.

* 수신자에게 역할이 할당되지 않고 [링크](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=ko-KR) 이 사용자에게는 기본적으로 역할이 주어집니다. 관리자 받기 **[!UICONTROL 편집 가능]** 및 관리자가 아닌 사용자가 수신 **[!UICONTROL 복제 가능]**.

조직의 사용자와 프로젝트 링크를 공유하려면 다음 작업을 수행합니다.

1. 프로젝트를 저장합니다. 저장하지 않은 변경 사항이 있으면 링크를 공유하기 전에 프로젝트를 저장하라는 메시지가 표시됩니다.

1. 선택 **[!UICONTROL 공유]** > **[!UICONTROL 작업 공간 사용자와 공유]**&#x200B;을 선택한 다음 을 선택합니다. **[!UICONTROL 복사]** 다음 옆에 **[!UICONTROL 링크로 공유]** 필드.

   ![](assets/share-proj-modal.png)

1. 조직의 사용자와 링크를 공유합니다. 예를 들어 이메일이나 내부 웹 사이트 등에 붙여넣을 수 있습니다.

## 누구와도 프로젝트 공유(로그인 필요 없음) {#share-public-link}

{{release-limited-testing-section}}

다음을 부여할 수 있습니다 [읽기 전용 액세스](/help/analyze/analysis-workspace/curate-share/view-only-projects.md) to Analysis Workspace projects to people to access to Adobe Analytics . 여기에는 다음이 포함될 수 있습니다.

* 조직 외부의 사용자

* 조직 내에서 Adobe Analytics에 액세스할 수 없는 사람

>[!NOTE]
>
>Adobe Analytics에 액세스할 수 없는 사용자와 Analysis Workspace 프로젝트를 공유할 때는 다음 사항을 고려하십시오.
>
>* Analytics 관리자가에 설명된 대로 이러한 방식으로 프로젝트를 공유하는 기능은 비활성화할 수 있습니다 [환경 설정](/help/analyze/analysis-workspace/user-preferences.md). 이 섹션에 설명된 대로 프로젝트를 공유할 수 없는 경우 Analytics 관리자가 이 기능을 비활성화했습니다.
>
>* 확장된 시각화가 50개를 초과하는 프로젝트는 Adobe Analytics 액세스 권한이 없는 사용자와 공유할 수 없습니다.
>
>* 프로젝트를 공유하는 사용자는 다음 기간 동안 프로젝트에 적용된 모든 필터를 볼 수 있습니다 [큐레이션](curate.md).
> 
>* 공유하는 사용자는 프로젝트 날짜 범위를 변경할 수 있습니다. 프로젝트에 대해 설정한 날짜 범위는 기본적으로 표시됩니다.
>
>* 많은 사용자가 지정된 링크에 동시에 액세스하려고 하면 프로젝트에 액세스할 수 없게 될 수 있습니다. 기본적으로 190명 이상의 사용자가 5분마다 하나의 링크에 액세스할 수 있습니다. 조직이 이 제한에 도달하면 5분 정도 기다린 후 링크에 다시 액세스해 보십시오.


다음 비디오 데모 및 함께 제공되는 설명서에서는 모든 사용자와의 링크 공유와 관련된 옵션에 대해 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3420093/?learn=on)

Adobe Analytics에 대한 액세스 권한이 없는 사람과 Analysis Workspace 프로젝트를 공유하려면 다음을 수행하십시오.

1. 공유할 Analysis Workspace 프로젝트를 엽니다.

1. 클릭 **[!UICONTROL 공유]** > **[!UICONTROL 누구와도 공유]**.

   저장하지 않은 변경 사항이 있으면 프로젝트를 저장하라는 메시지가 표시됩니다.

   <!-- Add screen shot of new modal -->

1. 활성화 **[!UICONTROL 링크가 활성 상태입니다.]** 아직 활성화되지 않은 경우 옵션을 선택합니다.

   이 옵션을 선택하면 누구와도 공유할 수 있는 프로젝트 링크가 만들어집니다. 이 옵션을 비활성화하면 언제든지 프로젝트에 대한 액세스를 비활성화할 수 있습니다.

   프로젝트의 소유자도 이 링크의 소유자입니다. 에 설명된 대로 프로젝트 소유권이 이전되어야 링크 소유권을 다른 사용자에게 이전할 수 있습니다. [사용자 자산 전송 또는 계정 만료 설정](/help/admin/admin/user-management2/users-assets.md) ( Analytics 관리 안내서).

1. 다음 보안 옵션을 활성화할지 여부를 선택합니다(이 옵션은 Analytics 관리자가 제어할 수 있음).

   * **[!UICONTROL Experience Cloud 인증 필요]:**

      이 옵션이 활성화된 경우 프로젝트에 액세스할 수 있는 사용자는 공유 중인 프로젝트가 생성된 Adobe Experience Cloud 조직에 로그인할 수 있는 사용자만 됩니다. 그러나 와 공유하는 사용자는 Adobe Analytics에 액세스할 필요가 없습니다.

      Analytics 관리자는에 설명된 대로 회사에 대해 이 환경 설정을 구성할 수 있습니다. [환경 설정](/help/analyze/analysis-workspace/user-preferences.md). 관리자가 이 옵션을 구성한 방식에 따라 다음과 같은 시나리오가 발생할 수 있습니다.

      * 이 옵션이 표시되지 않으면 Analytics 관리자가 이 기능을 활성화하지 않은 것입니다.

      * 이 옵션이 활성화되고 흐리게 표시되는 경우 Analytics 관리자는 Analysis Workspace 프로젝트에 액세스하는 모든 사용자에 대해 Experience Cloud 인증을 요구합니다.

1. 다음 옆에 **[!UICONTROL 누구와도 공유(로그인 필요 없음)]** 필드를 클릭하고 **링크 복사** 아이콘 ![링크 복사 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Link_18_N.svg) 시스템 클립보드에 링크를 복사합니다.

1. 프로젝트에 액세스할 수 있는 사람과 링크를 공유합니다. 예를 들어 이메일에 링크를 붙여넣을 수 있습니다.

   링크를 공유하는 모든 사용자는 Analysis Workspace 프로젝트를 볼 수 있습니다.

1. (선택 사항) **새 링크 생성** 아이콘 ![링크 생성 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) 을 클릭하여 이전에 프로젝트에 대한 링크를 받은 사용자의 액세스 권한을 제거합니다. 프로젝트에 액세스하려는 사용자와 공유할 수 있는 새 링크가 생성됩니다.

1. 선택 **[!UICONTROL 닫기]** 공유 대화 상자를 닫습니다. 변경 사항이 자동으로 저장됩니다.

## 프로젝트 관리자에서 프로젝트 공유 {#Manager}

**[!UICONTROL 구성 요소] > [!UICONTROL 프로젝트]**&#x200B;에서 프로젝트를 공유할 수도 있습니다. 위의 동일한 단계에 따라 단일 프로젝트를 공유할 수 있습니다. 여러 프로젝트를 공유하도록 선택하면 수신자가 각 프로젝트에 대한 기존 수신자 목록에 추가됩니다.

예:

* 프로젝트 A는 수신자 1, 2, 3에게 공유됨
* 프로젝트 B는 수신자 4, 5, 6에게 공유됨

프로젝트 A와 B를 선택하면 수신자 4 및 7이 공유 목록에 추가됩니다. 이제 각 프로젝트에 대한 새 공유 목록이 표시됩니다.

* 프로젝트 A: 1, 2, 3, 4, 7
* 프로젝트 B: 4, 5, 6, 7

![](assets/mult-proj-sharing.png)

## 임베드된 구성 요소 공유

다음은 해당 주제에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/24713/?quality=12)

## FAQ {#FAQs}

| 질문 | 답변 |
| --- | --- |
| 두 명의 편집자가 동시에 프로젝트를 저장하면 어떻게 됩니까? | 변경 사항은 병합되지 않고 마지막으로 저장한 프로젝트 버전이 유지됩니다. Analysis Workspace는 현재 실시간 공동 작업을 지원하지 않습니다. |
| 관리자는 어떤 프로젝트 경험을 보게 됩니까? | **[!UICONTROL 복제 가능]** 또는 역할 **[!UICONTROL 볼 수 있음]**&#x200B;에 배치된 관리자는 프로젝트를 열 때 제한된 경험을 받게 됩니다. 원하는 경우 관리자는 **[!UICONTROL 구성 요소] > [!UICONTROL 프로젝트]**&#x200B;를 통해 언제든지 자신의 역할을 **[!UICONTROL 편집 가능]**&#x200B;으로 확장할 수 있습니다. |
| 수신자가 하나의 역할에서 개인 또는 그룹의 구성원으로서의 다른 역할에 배치되면 어떻게 됩니까? | 수신자가 여러 역할에 배치되면 항상 더 높은 경험을 받게 됩니다. 예를 들어 수신자에게 개인으로서 **[!UICONTROL 편집 가능]** 역할 및 그룹의 구성원으로 **[!UICONTROL 볼 수 있음]** 역할이 주어지면 해당 사용자에게는 프로젝트 **[!UICONTROL 편집 가능]** 환경이 제공됩니다. |
| 프로젝트 링크를 열면 수신자는 어떤 경험을 얻을 수 있습니까? | 수신자는 공유 모달에서 지정한 역할을 받습니다. 수신자에게 역할이 지정되지 않고 프로젝트에 대한 링크(**[!UICONTROL 공유]** > **[!UICONTROL 작업 공간 사용자와 공유]**&#x200B;을 선택한 다음 을 선택합니다. **[!UICONTROL 복사]** 다음 옆에 **[!UICONTROL 링크로 공유]** 필드)를 입력하면 기본적으로 역할에 배치됩니다. 관리자는 **[!UICONTROL 편집 가능]** 역할을, 관리자가 아닌 사용자는 **[!UICONTROL 복제 가능]** 역할을 받습니다. |
