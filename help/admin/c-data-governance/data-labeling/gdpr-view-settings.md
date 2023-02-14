---
description: 데이터 거버넌스를 위한 개인정보 보호 레이블 지정 대화 상자는 보고서 세트의 개인정보 보호 레이블 및 네임스페이스에 대한 개요를 제공합니다. 여기에서 설정을 .csv 파일로 내보낼 수도 있습니다.
title: 데이터 거버넌스를 위한 개인정보 보호 레이블 지정 보기/관리
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: 7b5a2ef1f96de5dfa59f70c6e017a2caa3920378
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 77%

---

# 데이터 거버넌스를 위한 개인정보 보호 레이블 지정 보기/관리

**[!UICONTROL 데이터 거버넌스를 위한 개인정보 보호 레이블 지정]** 대화 상자는 보고서 세트의 개인정보 보호 레이블 및 네임스페이스에 대한 개요를 제공합니다. 여기에서 설정을 .csv 파일로 내보낼 수도 있습니다.

## 개인정보 보호 레이블 보기 {#view-privacy}

1. Adobe Experience Cloud에 로그인합니다.
2. **[!UICONTROL 분석]** > **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 데이터 구성 및 수집]** > **[!UICONTROL 데이터 거버넌스]**&#x200B;로 이동합니다.

   >[!NOTE]
   >
   >이 메뉴 항목이 표시되지 않으면 [Admin Console의 제품 프로필](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html?lang=ko-KR)에 이 기능에 대한 사용 권한을 추가해야 합니다.

3. 오른쪽 상단에서 보거나 관리할 개인정보 보호 레이블이 있는 보고서 세트를 선택합니다.

![](assets/privacy_labeling.png)

| 설정 | 설명 |
| --- | --- |
| **[!UICONTROL 구성 요소 이름]** | 이 열에는 이 보고서 세트의 일부인 모든 구성 요소(차원, 지표)가 나열됩니다. |
| **[!UICONTROL 신원]** | ID 데이터의 “I” 레이블은 특정 개인을 식별하거나 특정 개인에게 연락할 수 있는 데이터를 범주화하는 데 사용됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-identity-labels) |
| **[!UICONTROL 민감도]** | 중요 데이터 “S” 레이블은 지리 데이터와 같은 중요 데이터를 범주화하는 데 사용됩니다. 추가적인 중요 데이터 레이블은 다른 유형의 중요 정보를 식별하기 위해 나중에 도입됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#sensitive-data-labels) |
| **[!UICONTROL GDPR 액세스]** | 데이터 거버넌스 레이블은 규정 및 기업 정책을 준수하도록 개인정보 보호 관련 고려 사항 및 계약 조건을 반영하여 데이터를 분류하는 기능을 제공합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-access-labels) |
| **[!UICONTROL GDPR 삭제]** | 삭제 레이블은 히트가 데이터 주체와 연관될 수 있도록 하는 값(즉, 데이터 주체를 식별할 수 있는 값)이 포함된 필드에만 필요합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#data-privacy-delete-labels) |
| **[!UICONTROL 네임스페이스]** | 변수에 ID-DEVICE 또는 ID-PERSON으로 레이블을 지정할 때 네임스페이스를 제공하라는 메시지가 표시됩니다. 이전에 정의된 네임스페이스를 사용하거나 새 네임스페이스를 정의할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-labels.html?lang=en#provide-namespace) |
| **[!UICONTROL 범주]** | 표준 구성 요소, 전환 변수 등 구성 요소의 유형을 의미합니다. |

{style=&quot;table-layout:auto&quot;}

## 보고서 세트에 개인정보 보호 레이블 복사  {#copy-to-rs}

동일한 데이터 개인정보 보호 설정을 둘 이상의 보고서 세트에 적용하려는 경우 다음 단계를 따릅니다.

1. 복사하려는 변수를 선택합니다. 한 번에 하나의 변수에 대한 레이블만 복사할 수 있습니다.
1. 데이터 거버넌스 대화 상자 아래에 있는 **[!UICONTROL 보고서 세트로 복사]**&#x200B;를 클릭합니다.

   ![보고서 세트로 복사](assets/copy_to_reportsuite.png)

1. 결과 화면에는 변수 이름, 복사하려는 현재 적용된 레이블, 보고서 세트 및 해당 ID, 대상 보고서 세트의 설정이 일치하는지 여부가 표시됩니다.

   ![보고서 세트에 레이블 복사](assets/copy_to_rs.png)

   >[!IMPORTANT]
   >
   >선택하는 모든 보고서 세트는 Experience Cloud 조직에 매핑되어야 합니다.

   변수 또는 변수 세트에 대한 레이블을 다른 보고서 세트에 복사하면 복사본이 대상 보고서 세트의 해당 위치에 있는 변수로 이동합니다. 표준 구성 요소, 목록 변수, 성공 이벤트의 경우 레이블이 대상 보고서 세트에서 **동일한 이름**&#x200B;을 가진 변수에 복사됩니다.

   하지만 전환 변수(eVar) 및 트래픽 Dimension(props)의 경우 복사본이 과 함께 변수에 이동합니다 **동일한 숫자** 를 반환합니다. 예를 들어 eVar12는 모든 대상 보고서 세트의 eVar12에 복사됩니다. 이러한 변수의 이름은 복사본 대상을 판별할 때 무시됩니다. 해당 변수가 대상 보고서 세트에서 활성화되지 않은 경우 해당 변수에 대한 복사가 실패합니다.

   변수에 대해 정의된 분류 레이블을 복사할 때 대상 보고서 세트에서 복사하는 분류와 동일한 이름을 가진 해당 변수의 분류에 레이블이 복사됩니다. 그렇지 않으면 해당 분류 레이블에 대한 복사가 실패합니다.

1. 설정이 일치하는 하나 이상의 보고서 세트 옆에 있는 확인란을 선택합니다.
1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

   레이블이 적용된 후 상태 메시지가 표시됩니다. 상태 메시지에는 복사가 실패한 대상 변수 또는 분류와 해당 보고서 세트의 이름이 포함됩니다.

   >[!IMPORTANT]
   >
   >항상 대상 보고서 세트를 검사하여 레이블이 올바르게 복사되었는지 확인해야 합니다. 이는 ID 또는 DEL 레이블이 있는 변수에 특히 중요합니다.

## .csv 파일로 내보내기 {#export-csv}

선택한 보고서 세트의 모든 변수에 대한 모든 현재 레이블 정의가 포함된 CSV 파일을 다운로드할 수 있습니다. 법무팀에서는 레이블 지정 옵션을 검토하고 이 옵션을 통해 이 검토를 쉽게 수행할 것을 권장합니다. 데이터 거버넌스 UI에 로그인하는 동안 검토를 수행할 필요 없이 .CSV 파일을 공유할 수 있습니다.

1. 오른쪽 상단의 **[!UICONTROL CSV 내보내기]**&#x200B;를 클릭하면 이 대화 상자가 표시됩니다.

   ![](assets/export_csv.png)

1. 모든 데이터 거버넌스 설정을 내보내려는 보고서 세트를 하나 이상 선택합니다.

## 개인정보 보호 레이블 편집 {#edit}

[보고서 세트 개인정보 보호 레이블 지정 또는 편집](/help/admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md)을 참조하십시오.
