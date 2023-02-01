---
description: 작업 영역의 프로젝트 공유 및 프로젝트 역할
keywords: Analysis Workspace 공유
title: 프로젝트 공유
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 4b11a7057177bec9d2e9d7c435ad0d5476a46602
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 35%

---

# 프로젝트 공유

다음 유형의 사람과 Analysis Workspace 프로젝트를 공유할 수 있습니다.

* Adobe Analytics에 액세스할 수 있는 조직의 사용자 및 그룹

* Adobe Analytics에 액세스할 수 없는 조직의 사용자 및 그룹

* 조직 외부의 사람

임의 [큐레이션](curate.md) 공유하기 전에 적용한 사항은 수신자가 프로젝트를 열 때 반영됩니다.

다음은 프로젝트 공유에 대한 비디오 개요입니다.

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## 조직의 Adobe Analytics 사용자 및 그룹과 공유 {#Add}

조직의 기존 Adobe Analytics 사용자 또는 그룹과 프로젝트를 공유할 수 있습니다. 이 섹션에 설명된 대로 프로젝트를 공유할 때 공유하는 사용자에게 이미 Adobe Analytics 계정이 있어야 합니다.

특정 역할을 사용자 또는 그룹과 공유하거나 링크를 공유할 수 있습니다.

* [특정 프로젝트 역할 공유](#share-a-specific-project-role)

* [프로젝트에 대한 링크 공유](#share-a-link-to-a-project)

### 특정 프로젝트 역할 공유

조직의 사용자 및 그룹과 특정 프로젝트 역할을 공유할 때는 다음 사항을 고려하십시오.

* 프로젝트 역할 (**[!UICONTROL 편집 가능]**, **[!UICONTROL 복제 가능]**, 및 **[!UICONTROL 보기 가능]**)가 사용자 및 특정 프로젝트 ID에 연결되어 있습니다. 프로젝트 역할은 [Adobe Experience Cloud 관리 콘솔](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR)에서 관리되는 사용자 권한과 독립적입니다.

* Adobe Analytics에서 그룹은 [Adobe Experience Cloud 관리 콘솔](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR)에서 제품 프로필로 정의됩니다. 관리자는 &quot;모두&quot;를 비롯한 모든 그룹과 공유할 수 있습니다. 관리자가 아닌 사용자는 &quot;모두&quot;를 제외하고 자신이 구성원으로 있는 모든 그룹과 공유할 수 있습니다.

* 여러 역할에 배치되는 사용자는 항상 가장 높은 경험을 받습니다. 이는 사용자가 개인과 그룹의 일부로 모두 추가되는 경우에 발생할 수 있습니다. 예를 들어, 사용자에게 **[!UICONTROL 편집 가능]** 개인으로서의 역할 및 **[!UICONTROL 보기 가능]** 그룹의 구성원으로서의 역할은 **[!UICONTROL 편집 가능]** 프로젝트 경험.

* 관리자가 **[!UICONTROL 복제 가능]** 또는 **[!UICONTROL 보기 가능]** 역할은 프로젝트를 열 때 제한된 경험을 받습니다. 원하는 경우 관리자는 **[!UICONTROL 구성 요소] > [!UICONTROL 프로젝트]**&#x200B;를 통해 언제든지 **[!UICONTROL 편집 가능]**&#x200B;한 역할을 늘릴 수 있습니다.

조직의 사용자 또는 그룹과 특정 프로젝트 역할을 공유하려면 다음을 수행하십시오.

1. 공유할 프로젝트로 이동한 다음 **[!UICONTROL 공유]** > **[!UICONTROL 프로젝트 공유]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
저장하지 않은 변경 사항이 있으면 먼저 프로젝트를 저장하라는 메시지가 표시됩니다.

   ![](assets/share-proj-modal.png)

   여러 프로젝트를 동시에 공유하는 방법에 대한 자세한 내용은 [프로젝트 관리자에서 프로젝트 공유](#share-projects-in-the-project-manager).

1. 제공된 역할 필드 중 하나에 수신자 또는 수신자 그룹을 추가합니다.

   **편집 가능:** 수신자는 다음을 수행할 수 있습니다 **[!UICONTROL 저장]** 공동 소유자로서 프로젝트 및 기능 변경. 이 역할은 프로젝트를 다른 동료와 공동 관리하려는 경우 유용합니다. 여기에는 공유 프로젝트에 대한 수신자 목록 편집, 삭제 및 수정 등이 포함됩니다. <br>참고: Analysis Workspace는 현재 라이브 공동 작업을 지원하지 않으므로 주어진 시간에 한 명의 사용자만 프로젝트를 편집하는 것이 좋습니다. 프로젝트를 동시에 저장하는 경우 마지막 버전이 유지됩니다.

   **복제 가능:** 수신자는 다음을 수행할 수 있습니다 **[!UICONTROL 다른 이름으로 저장]** 왼쪽 레일에 액세스할 수 있습니다. 이 역할에서는 프로젝트 상호 작용이 제한되지 않습니다. 이 역할은 조직의 데이터 및 Analysis Workspace 사용 방법을 이해하지만 프로젝트를 변경하지 않으려는 사용자에게 프로젝트를 공유하려는 경우에 유용합니다.

   **다음을 볼 수 있습니다.** 수신자는 다음을 수행할 수 없습니다. **[!UICONTROL 저장]** 또는 **[!UICONTROL 다른 이름으로 저장]** 왼쪽 레일에 액세스할 수 없습니다. 상호 작용이 제한됩니다. 이 역할은 일반적으로 조직의 데이터 구조, Analysis Workspace 또는 Adobe Analytics에 익숙하지 않은 사용자에게 프로젝트를 공유하려는 경우 유용합니다. 그러나 안전한 환경에서 데이터와 인사이트를 소비해야 합니다. 프로젝트 경험 볼 수 있음[에 대해 자세히 알아보십시오](/help/analyze/analysis-workspace/curate-share/view-only-projects.md).

1. 프로젝트를 공유할 때 다음 옵션을 활성화할지 여부를 선택합니다.

   * **포함된 프로젝트 구성 요소 공유:** 모든 수신자와 세그먼트, 계산된 지표 및 날짜 범위를 공유합니다. 이러한 구성 요소가 공유되면 수신자 작업 영역의 구성 요소 드롭다운에 표시됩니다. 이 설정은 유지되지 않습니다. 공유 시 한 번의 작업입니다.

   * **수신자용 랜딩 페이지로 설정:** 이 페이지를 수신자의 랜딩 페이지로 설정합니다. 이 설정은 유지되지 않습니다. 공유 시 한 번의 작업입니다.

1. **[!UICONTROL 공유]**를 클릭합니다.
또한 **[!UICONTROL 조정 및 공유]**&#x200B;를 클릭하여 프로젝트 조정을 자동으로 적용할 수도 있습니다. 프로젝트가 이미 공유된 경우 이 버튼에는 **[!UICONTROL 업데이트]** 및 **[!UICONTROL 조정 및 업데이트]**&#x200B;가 표시됩니다. [프로젝트 조정](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=ko-KR)에 대한 자세한 내용을 살펴보십시오.

### 프로젝트에 대한 링크 공유

이 섹션에 설명된 대로 링크를 공유할 때는 다음 사항을 고려하십시오.

* 링크를 사용하는 수신자는 프로젝트에 액세스할 수 있으려면 먼저 Adobe Analytics에 로그인해야 합니다.

* 수신자에게 역할이 할당되지 않고 [링크](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=ko-KR) 프로젝트(**[!UICONTROL 공유] > [!UICONTROL 프로젝트 링크 가져오기]**), 기본적으로 역할을 받습니다. 관리자는 **[!UICONTROL 편집 가능]**&#x200B;하고 관리자가 아닌 사용자는 **[!UICONTROL 복제 가능]**&#x200B;합니다.

조직의 사용자와 프로젝트 링크를 공유하려면 다음을 수행하십시오.

1. **[!UICONTROL 공유]** > **[!UICONTROL 프로젝트 공유]**&#x200B;를 클릭합니다. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
저장하지 않은 변경 사항이 있으면 먼저 프로젝트를 저장하라는 메시지가 표시됩니다.

   ![](assets/share-proj-modal.png)

1. 클릭 **[!UICONTROL 링크 복사]** 다음 **[!UICONTROL URL 공유 필드]**.

1. 조직의 사용자와 링크를 공유합니다. 예를 들어 이메일, 내부 웹 사이트 등에 붙여넣을 수 있습니다.

## 모든 사람과 공개 링크 공유(로그인 필요 없음) {#share-public-link}

{{release-limited-testing-section}}

Adobe Analytics에 액세스할 수 없는 사람과 Analysis Workspace 프로젝트를 공유할 수 있습니다. 여기에는 다음이 포함될 수 있습니다.

* 조직 외부의 사람

* 조직 내에서 Adobe Analytics이 제공되지 않는 사람

>[!NOTE]
>
>에 설명된 대로 Analytics 관리자가 이 옵션을 비활성화할 수 있습니다 [기본 설정](/help/analyze/analysis-workspace/user-preferences.md). 이 섹션에 설명된 대로 공개 링크를 공유할 수 없는 경우 Analytics 관리자가 이 기능을 비활성화했습니다.

Analysis Workspace 프로젝트에 대한 공개 링크를 공유하려면:

1. 공유할 Analysis Workspace 프로젝트를 엽니다.

1. 클릭 **[!UICONTROL 공유]** > **[!UICONTROL 공개 링크 공유]**.

   저장하지 않은 변경 사항이 있으면 프로젝트를 저장하라는 메시지가 표시됩니다.

   <!-- Add screen shot of new modal -->

1. 를 활성화합니다 **[!UICONTROL 링크 활성]** 아직 활성화되지 않은 경우 선택합니다.

1. 다음 보안 옵션을 활성화할지 여부를 선택합니다(이러한 옵션은 Analytics 관리자가 제어할 수 있음).

   * **[!UICONTROL SSO(Single Sign-On) 인증 필요]:**

      공유 프로젝트에 액세스할 수 있으려면 먼저 SSO를 통해 인증을 받을 수 있는 링크가 있는 사람이 요청해야 합니다. 조직 내의 사용자만 프로젝트에 액세스할 수 있도록 하려면 이 옵션을 선택합니다.

      Analytics 관리자는 [기본 설정](/help/analyze/analysis-workspace/user-preferences.md). 관리자가 이 옵션을 구성한 방법에 따라 다음 시나리오가 발생할 수 있습니다.

      * 이 옵션이 표시되지 않으면 조직에 대해 SSO가 활성화되지 않았거나 Analytics 관리자가 이 기능을 활성화하지 않았습니다.

      * 이 옵션이 활성화되고 흐리게 표시되면 Analytics 관리자가 모든 공개 링크에 액세스하려면 SSO 인증을 필요로 합니다.
   * **[!UICONTROL 암호 필요]:** Analysis Workspace 프로젝트에 액세스하기 전에 링크를 가진 사람이 암호를 지정해야 합니다. 프로젝트에 대한 추가 수준의 보안을 제공합니다.

      이 옵션을 선택하는 경우 암호를 지정하십시오. 이 암호를 다른 사용자와 공유할 때는 프로젝트 링크와 공유해야 합니다. <!--go through this workflow and see how it works.-->

      이 옵션이 활성화되고 흐리게 표시되면 Analytics 관리자가 모든 공개 링크를 암호로 보호해야 합니다. Analytics 관리자는 [기본 설정](/help/analyze/analysis-workspace/user-preferences.md).


1. 다음 **[!UICONTROL 다른 사람과 공유(로그인 필요 없음)]** 필드에서 **링크 복사** 아이콘을 사용하여 시스템 클립보드에 링크를 복사합니다.

1. 프로젝트에 액세스할 사람과 링크를 공유합니다. 예를 들어 링크를 전자 메일에 붙여넣을 수 있습니다.

   링크를 공유하는 모든 사용자는 Analysis Workspace 프로젝트를 볼 수 있습니다. 암호를 사용하도록 선택한 경우 해당 링크에 액세스하려는 모든 사용자와 암호를 공유해야 합니다.

1. 선택 **[!UICONTROL 닫기]** 공유 대화 상자를 닫습니다. 변경 사항이 자동으로 저장됩니다. <!-- True? -->


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
| 관리자는 어떤 프로젝트 경험을 보게 됩니까? | **[!UICONTROL 복제 가능]** 또는 역할 **[!UICONTROL 볼 수 있음]**&#x200B;에 배치된 관리자는 프로젝트를 열 때 제한된 경험을 받게 됩니다. 원하는 경우 관리자는 **[!UICONTROL 구성 요소] > [!UICONTROL 프로젝트]**&#x200B;를 통해 언제든지 **[!UICONTROL 편집 가능]**&#x200B;한 역할을 늘릴 수 있습니다. |
| 수신자가 하나의 역할에서 개인 또는 그룹의 구성원으로서의 다른 역할에 배치되면 어떻게 됩니까? | 수신자가 여러 역할에 배치되면 항상 더 높은 경험을 받게 됩니다. 예를 들어 수신자에게 개인으로서 **[!UICONTROL 편집 가능]** 역할 및 그룹의 구성원으로 **[!UICONTROL 볼 수 있음]** 역할이 주어지면, 해당 사용자에게는 프로젝트 **[!UICONTROL 편집 가능]** 환경이 제공됩니다. |
| 프로젝트 링크를 열면 수신자는 어떤 경험을 얻을 수 있습니까? | 수신자는 공유 모달에서 지정한 역할을 받습니다. 수신자에게 역할이 할당되지 않고 프로젝트에 대한 링크를 받은 경우 (**[!UICONTROL 공유]> [!UICONTROL 프로젝트 링크 가져오기]**) 기본적으로 역할을 받게 됩니다. 관리자는 **[!UICONTROL 편집 가능]**&#x200B;하고 관리자가 아닌 사용자는 **[!UICONTROL 복제 가능]**&#x200B;합니다. |
