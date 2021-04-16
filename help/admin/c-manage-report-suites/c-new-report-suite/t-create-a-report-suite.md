---
description: Adobe Analytics에서 데이터 수집을 위한 기본 컨테이너를 만듭니다
title: 보고서 세트 만들기
feature: 관리 도구
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 77%

---

# 보고서 세트 만들기

보고서 세트는 Adobe Analytics가 보고서를 가져오는 데 사용하는 데이터의 사일로입니다. 조직에는 여러 개의 보고서 세트가 있을 수 있으며, 각 보고서 세트에는 서로 다른 데이터 세트가 포함되어 있습니다. 이전에는 개별 보고서 세트가 중요했지만 단일 보고서 세트가 더 유용해졌습니다. [가상 보고서 세트](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=en#virtual-report-suites) 및 보고서 시간 처리를 도입하면 관리자가 고유한 데이터 하위 세트를 만들 수 있으므로 글로벌 및 사이트 특정 데이터를 모두 유연하게 얻을 수 있습니다.

이 문서는 시스템 수준 관리자 또는 분석 관리자가 데이터 수집을 준비할 수 있게 설계되었습니다.

## 전제 조건

[Adobe Analytics 첫 번째 관리 안내서](/help/admin/admin-console/first-admin-guide.md):시스템 수준 관리자가 Experience Cloud Admin Console을 통해 Adobe Analytics에 대한 액세스 권한을 부여했는지 확인합니다.

## 보고서 세트 만들기 {#create-report-suite}

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 새로 만들기]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. 보고서 세트의 설정을 복사하려면 템플릿 목록에서 미리 정의된 템플릿이나 [템플릿](/help/admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md)으로 사용할 기존 보고서 세트를 선택합니다.

   >[!NOTE]
   >
   >설정만 복사할 수 있고 데이터는 복사할 수 없습니다. 고객 지원에서 설정을 복사하는 경우 관련된 위험에 대해 고객 지원에서 제공하는 면책조항에 대한 서면 확인서를 제공해야 합니다. 자세한 내용은 [소스 보고서 세트에서 복사되지 않은 설정](/help/admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md)을 참조하십시오.

1. [새 보고서 세트](/help/admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md)에 설명된 필드를 채웁니다.
1. **[!UICONTROL 보고서 세트 만들기]**&#x200B;를 클릭합니다.

보고서 세트 ID의 길이는 최대 40바이트입니다. 보고서 세트의 친숙한 이름은 최대 길이 255바이트입니다.

## 문제 해결

**Experience Cloud에 로그인하면 Analytics 아이콘이 회색으로 표시됩니다.**

이는 계정에 Analytics에 대한 올바른 권한이 부여되지 않았음을 의미합니다. 조직의 시스템 수준 관리자와 함께 Adobe Analytics에 액세스할 수 있는 충분한 권한이 있는 프로필에 속해 있는지 확인합니다.

**Adobe Analytics에 로그인하면 &#39;Adobe Analytics에 오신 것을 환영합니다.&#39; 팝업과 드롭다운이 표시되지 않습니다.**

my.omniture.com을 통해서가 아니라 Experience Cloud를 통해 로그인했는지 확인합니다. my.omniture.com을 통해 로그인한 사용자는 보고서 세트 설정 마법사를 사용할 수 없습니다.

## 다음 단계

[Launch에서 Adobe Analytics에 대한 속성 만들기 및 구성](/help/implement/launch/create-analytics-property.md): Analytics 구현을 관리할 영역 만들기
