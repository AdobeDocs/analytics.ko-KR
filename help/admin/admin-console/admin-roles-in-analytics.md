---
title: Adobe Analytics의 관리자 역할
description: Adobe Analytics 시작, 일반 역할 유형, UI에 로그인하는 방법을 알아봅니다.
feature: Admin Tools
source-git-commit: 7cde90a15dc97468a70f8120bec46915eab7c1bb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 58%

---

# Adobe Analytics의 관리자 역할

Adobe Analytics에서는 다양한 유형의 관리자를 지원합니다. 전체 Adobe Analytics 관리자는 Adobe Analytics의 모든 기능에 액세스할 수 있는 반면, 다른 관리자와 사용자는 더 전문적인 작업을 수행할 수 있습니다.

>[!NOTE]
>
>Adobe Analytics에서 사용자에게 역할을 할당하려면 먼저 Experience Cloud에서 사용자를 첫 번째 관리자로 할당해야 합니다. 그런 다음 첫 번째 관리자는 이 문서에 설명된 대로 조직의 사용자에게 다른 주요 역할을 제공할 수 있습니다. 첫 번째 관리자에 대한 자세한 내용은 [Adobe Analytics 첫 번째 관리 안내서](/help/admin/admin-console/first-admin-guide.md).


## Experience Cloud 및 Adobe Analytics의 주요 역할

Adobe Analytics을 사용할 때 다음 주요 역할을 고려하십시오.

* **전체 Adobe Analytics 관리자:** 이러한 사용자는 보고서 세트 설정 및 사용자 권한을 포함하여 Adobe Analytics의 모든 항목에 액세스할 수 있습니다. 조직의 구성 방식에 따라 다른 사용자나 팀이 Analytics 관리의 여러 측면을 담당할 수 있습니다. 예를 들면 한 사람은 구현에서 사용할 변수를 지정합니다. 다른 사람은 모든 사람의 권한이 올바른지 확인하여 사용자가 보고서를 올바르게 가져올 수 있도록 담당합니다. Analytics 보고서 세트 설정 및 사용자 권한을 담당할 수 있는 사용자를 한 명 이상 식별하고, 이들이 여기서 다른 Analytics 관리자를 초대할 수 있습니다.
* **데이터 수집 관리자:** 이러한 사용자는 게시 권한, 컨테이너 만들기 및 사용자 권한 등 Adobe Experience Platform 데이터 컬렉션의 모든 항목에 액세스할 수 있습니다. 이러한 사용자가 반드시 프로그래머일 필요는 없지만 적어도 HTML, CSS 및 JavaScript에 대한 초보 지식이 있는 것이 유용합니다. 따라서 사이트에서 태그를 구현하기 위해 조직의 웹 사이트 소유자와 함께 작업하는 경우가 있습니다. 조직 구현을 담당할 최소한 한 명 이상의 사용자를 지정하십시오. 이 사용자가 다른 데이터 수집 관리자를 초대할 수 있습니다.
* **제품 프로필 관리자:** 이러한 사용자는 제품 프로필에 사용자를 추가하거나 제거하고, 제품 프로필의 권한 항목을 조정하고, 제품 프로필을 사용자 그룹에 지정하거나 제거할 수 있습니다. 제품 프로필 관리자는 Adobe Analytics에 대한 전체 액세스 권한이 없습니다. 하지만 팀을 위해 Adobe Analytics에 대한 액세스 권한을 부여하고 관리해야 하는 팀 리더 또는 관리자에게 이상적입니다. 제품 프로필에 대한 자세한 내용은 [Adobe Analytics용 제품 프로필](/help/admin/admin-console/permissions/product-profile.md).
* **지원 위임**: 지원되는 사용자라고도 하는 이 사용자는 Analytics 인터페이스에 추가적인 권한이 없습니다. 대신 Adobe 고객 지원 센터와 의사 소통할 때 추가적인 권한을 받습니다. 고객 지원 센터에서 문제를 해결하는 데 도움이 되므로 이러한 사용자는 거의 항상 Analytics 관리자도 됩니다. 최종 사용자와 Adobe 고객 지원 센터 간의 상호 작용을 용이하게 할 책임이 있는 Analytics 관리자를 한 명 이상 식별합니다.
* **웹 사이트 소유자:** 이 역할을 맡는 개인이나 팀은 웹 사이트의 코딩 및 개발을 담당합니다. 이 개인은 계정이 꼭 필요하지 않지만 데이터 수집 관리자와 협력하여 웹 사이트에 태그 코드를 확보하고 구현합니다.
* **최종 사용자:** 이 사용자는 일반적으로 보고서를 보고 비즈니스 질문에 대한 답변을 찾습니다. Analytics 관리자는 이러한 사용자에게 제품에서 작업할 수 있는 권한을 부여합니다.

## Analytics에 대한 전체 제품 관리자 액세스 권한 부여

시스템 수준 관리자는 제품에 직접 액세스할 수 없습니다. 그러나 제품 수준 관리자로 자신을 추가하여 자신에게 액세스 권한을 제공할 수 있습니다.

Adobe Analytics이 본인 또는 다른 사용자에게 액세스할 수 있도록 하려면 다음을 수행하십시오.

1. Adobe ID 자격 증명으로 [Admin Console](https://adminconsole.adobe.com/)에 로그인합니다.
1. 맨 위의 **[!UICONTROL 제품]** 탭을 클릭합니다. 조직에서 구입한 모든 제품은 왼쪽에 있습니다. 클릭 **[!UICONTROL Adobe Analytics]**&#x200B;를 클릭한 다음 **[!UICONTROL 새 프로필]** 버튼을 클릭합니다.
1. 이 프로필의 이름을 &#39;Analytics 전체 관리자 액세스 권한&#39;으로 지정한 다음 **[!UICONTROL 다음]** > **[!UICONTROL 저장]**.
1. 다시 제품 프로필 페이지로 돌아가서 새로 만든 프로필을 클릭한 뒤 **[!UICONTROL 권한]** 탭을 클릭합니다.
1. 권한 라인 항목 중 하나를 클릭합니다. **[!UICONTROL 자동 포함]**&#x200B;이 이용 가능해진 경우 이를 활성화합니다. If **[!UICONTROL 자동 포함]** 사용할 수 없습니다. **[!UICONTROL 모두 추가]**. 두 옵션 모두 모든 권한 항목을 오른쪽 열로 이동합니다.
1. **[!UICONTROL 저장]**을 클릭합니다.
모든 권한 카테고리에 대해 위의 단계를 반복합니다.
1. 프로필에 모든 권한 카테고리가 부여되면 을 클릭하여 제품 페이지로 돌아갑니다 **[!UICONTROL 제품]** 바로 위에요
1. Adobe Analytics 타일에서 를 클릭합니다. **[!UICONTROL 사용자 할당]**.
1. 전체 Analytics 액세스 권한을 부여할 이메일 주소를 입력하고 새로 만든 전체 관리자 액세스 프로필을 지정합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이제 사용자는 Adobe Analytics에 대한 전체 액세스 권한을 갖습니다.

## Experience Platform의 데이터 수집에 대한 제품 관리자 액세스 권한 부여

Experience Platform의 데이터 수집에 대한 제품 관리자 액세스 권한을 부여하는 것은 Analytics에 대한 제품 관리자 권한을 부여하는 것과 거의 동일합니다.

1. Adobe ID 자격 증명을 사용하여 [Adobe Admin Console](https://adminconsole.adobe.com)에 로그인합니다.
1. 맨 위의 **[!UICONTROL 제품]** 탭을 클릭합니다. 조직에서 구입한 모든 제품은 왼쪽에 있습니다. **[!UICONTROL Experience Platform Launch]**&#x200B;를 클릭한 뒤 **[!UICONTROL 새 프로필]**&#x200B;을 클릭합니다.
1. 이 프로필의 이름을 &#39;데이터 수집에 대한 완전한 관리 액세스 권한&#39;으로 지정한 뒤 **[!UICONTROL 완료]**&#x200B;를 클릭합니다.
1. 다시 **[!UICONTROL 제품 프로필]** 페이지로 돌아가서 새로 만든 프로필을 클릭한 뒤 **[!UICONTROL 권한]** 탭을 클릭합니다.
1. 권한 라인 항목 중 하나를 클릭합니다. **[!UICONTROL 자동 포함]**&#x200B;이 이용 가능해진 경우 이를 활성화합니다. 자동 포함을 이용할 수 없는 경우 **[!UICONTROL 모두 추가]**&#x200B;를 클릭합니다. 두 옵션 모두 모든 권한 항목을 오른쪽 열로 이동합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다. 모든 권한 카테고리에 대해 위의 단계를 반복합니다.
1. 모든 권한 카테고리가 이 프로필에 부여되고 나면 맨 위의 **[!UICONTROL 개요]**&#x200B;를 클릭해 개요 페이지로 돌아갑니다.
1. [!UICONTROL Experience Platform Launch] 타일 아래에서 **[!UICONTROL 사용자 할당]**&#x200B;을 클릭합니다.
1. 전체 Analytics 액세스 권한을 부여할 이메일 주소를 입력하고 새로 만든 전체 관리자 액세스 프로필을 지정합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 이제 사용자가 Experience Platform의 데이터 수집에 대해 완전한 액세스 권한을 보유합니다.

## 제품 프로필에 대한 제품 관리자 액세스 권한 부여

사용자를 제품 프로필 관리자로 지정하는 방법에 대한 자세한 내용은 문서의 &quot;제품 프로필 관리자 관리&quot; 섹션을 참조하십시오. [엔터프라이즈 사용자를 위한 제품 프로필 관리](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) ( Enterprise 사용 안내서).

## 다음 단계

[보고서 세트 만들기](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Analytics 관리자가 도구에 로그인하고 데이터 수집을 위한 보고서 세트를 만들 수 있습니다.

[Analytics 태그 속성 만들기](/help/implement/launch/create-analytics-property.md): 데이터 수집 관리자가 도구에 로그인하여 사이트에 구현할 속성을 만들 수 있습니다.

Adobe Analytics에서 사용자에게 역할을 할당하려면 먼저 Experience Cloud에서 사용자를 첫 번째 관리자로 할당해야 합니다. 그런 다음 첫 번째 관리자는 이 문서에 설명된 대로 조직의 사용자에게 다른 주요 역할을 제공할 수 있습니다.

첫 번째 관리자는 조직의 나머지 부분이 각 Experience Cloud 솔루션을 사용할 수 있도록 하는 시작점입니다.

계약이 체결되면

1. Adobe의 프로비저닝 팀이 계정을 만들 준비를 합니다.

1. 첫 번째 관리자는 계약 시작일 전에 로그인 자격 증명이 포함된 이메일을 받게 됩니다.

>[!IMPORTANT]
>
>   첫 번째 관리자의 연락처 정보가 Adobe에 제공되었고 정확한지 확인한 후에 계약서에 서명하는 것이 좋습니다.