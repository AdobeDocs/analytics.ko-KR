---
description: 데이터 거버넌스에 대한 개인 정보 보호 레이블 지정 대화 상자는 보고서 세트의 개인 정보 레이블 및 네임스페이스에 대한 개요를 제공합니다. 여기에서 설정을 .csv 파일로 내보낼 수도 있습니다.
title: 데이터 거버넌스에 대한 개인 정보 레이블 보기/관리
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: 4bbed2efde0574bc9f5f6a78a022a22490e75549
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 44%

---

# 데이터 거버넌스에 대한 개인 정보 레이블 보기/관리

>[!NOTE]
>
>이 업데이트된 UI는 현재 제한된 테스트 중입니다.

다음 **[!UICONTROL 데이터 거버넌스에 대한 개인 정보 보호 레이블]** 대화 상자에서는 보고서 세트의 개인 정보 레이블 및 네임스페이스에 대한 개요를 제공합니다. 여기에서 설정을 .csv 파일로 내보낼 수도 있습니다.

## 개인 정보 레이블 보기 {#view-privacy}

1. Adobe Experience Cloud에 로그인합니다.
1. 다음으로 이동  **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 데이터 구성 및 수집]** > **[!UICONTROL 데이터 거버넌스]**.

   >[!NOTE]
   >
   >이 메뉴 항목이 표시되지 않으면 [Admin Console의 제품 프로필](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html)에 이 기능에 대한 사용 권한을 추가해야 합니다.

1. 오른쪽 상단에서 개인 정보 레이블을 보거나 관리할 보고서 세트를 선택합니다.

   ![](assets/privacy_labeling.png)

| 설정 | 설명 |
| --- | --- |
| **[!UICONTROL 구성 요소 이름]** | 이 열에는 이 보고서 세트의 일부인 모든 구성 요소(차원, 지표)가 나열됩니다. |
| **[!UICONTROL 신원]** | ID 데이터의 &quot;I&quot; 레이블은 특정 개인을 식별하거나 특정 개인에게 연락할 수 있는 데이터를 범주화하는 데 사용됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#identity-data-labels) |
| **[!UICONTROL 민감도]** | 중요 데이터 &quot;S&quot; 레이블은 지리 데이터와 같은 중요 데이터를 범주화하는 데 사용됩니다. 추가 민감한 데이터 레이블은 다른 유형의 민감한 정보를 식별하기 위해 나중에 도입됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#sensitive-data-labels) |
| **[!UICONTROL GDPR 액세스]** | 데이터 거버넌스 레이블은 규정 및 기업 정책을 준수하도록 개인정보 보호 관련 고려 사항 및 계약 조건을 반영하여 데이터를 분류하는 기능을 제공합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#data-privacy-access-labels) |
| **[!UICONTROL GDPR 삭제]** | 삭제 레이블은 히트를 데이터 주체(즉, 데이터 주체를 식별할 수 있는 주체)와 연결할 수 있는 값이 포함된 필드에만 필요합니다. 기타 개인 정보(즐겨찾기, 탐색/구입 내역, 건강 상태 등)는 데이터 주체와의 연결이 끊어지므로 삭제할 필요가 없습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#data-privacy-delete-labels) |
| **[!UICONTROL 네임스페이스]** | 변수에 ID-DEVICE 또는 ID-PERSON으로 레이블을 지정할 때 네임스페이스를 제공하라는 메시지가 표시됩니다. 이전에 정의된 네임스페이스를 사용하거나 새 네임스페이스를 정의할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-labels.html?lang=en#section_F0A47AF8DA384A26BD56032D0ABFD2D7) |
| **[!UICONTROL 카테고리]** | 표준 구성 요소, 전환 변수 등과 같은 구성 요소 유형을 나타냅니다. |

{style=&quot;table-layout:auto&quot;}

## 보고서 세트에 개인 정보 레이블 복사  {#copy-to-rs}

동일한 데이터 개인 정보 보호 설정을 둘 이상의 보고서 세트에 적용하려면 다음 단계를 수행합니다.

1. 복사할 변수를 선택합니다. 한 번에 하나의 변수에 대한 레이블만 복사할 수 있습니다.
1. 클릭 **[!UICONTROL 보고서 세트에 복사]** ( 데이터 거버넌스 대화 상자 하단에 있습니다.)

   ![보고서 세트에 복사](assets/copy_to_reportsuite.png)

1. 결과 화면에는 변수 이름, 현재 적용되어 복사하려는 레이블, 보고서 세트 및 해당 ID, 대상 보고서 세트의 설정이 일치하는지 여부가 표시됩니다.

   ![보고서 세트에 레이블 복사](assets/copy_to_rs.png)

   >[!IMPORTANT]
   >
   >선택한 모든 보고서 세트를 반드시 Experience Cloud 조직에 매핑해야 합니다.

   변수 또는 변수 세트에 대한 레이블을 다른 보고서 세트에 복사하면 복사본이 대상 보고서 세트의 해당 위치에 있는 변수로 이동합니다. 표준 구성 요소, 목록 변수 및 성공 이벤트의 경우, 레이블이 을 사용하여 변수에 복사됩니다. **동일한 이름** 를 반환합니다.

   하지만 전환 변수(eVar) 및 트래픽 Dimension(props)의 경우 복사본이 을 사용하여 변수에 전송됩니다 **동일한 숫자** 를 반환합니다. 예를 들어 eVar12는 모든 대상 보고서 세트의 eVar12에 복사됩니다. 이러한 변수의 이름은 복사본 대상을 판별할 때 무시됩니다. 해당 변수가 대상 보고서 세트에서 활성화되지 않은 경우 해당 변수에 대한 복사가 실패합니다.

   변수에 대해 정의된 분류에 대한 레이블을 복사할 때 복사 중인 분류와 동일한 이름을 갖는 대상 보고서 세트의 해당 변수(예: eVar7에서 eVar7으로)의 분류에 레이블을 복사합니다. 그렇지 않으면 해당 분류 레이블에 대한 복사가 실패합니다.

1. 설정이 일치하는 하나 이상의 보고서 세트 옆에 있는 상자를 선택합니다.
1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

   레이블이 적용된 후 상태 메시지가 표시됩니다. 상태 메시지에는 복사가 실패한 대상 변수 또는 분류와 해당 보고서 세트의 이름이 포함됩니다.

   >[!IMPORTANT]
   >
   >항상 대상 보고서 세트를 검사하여 레이블이 올바르게 복사되었는지 확인해야 합니다. 이는 ID 또는 DEL 레이블이 있는 변수에 특히 중요합니다.

## .csv 파일로 내보내기 {#export-csv}

선택한 보고서 세트의 모든 변수에 대한 현재 레이블 정의가 모두 포함된 CSV 파일을 다운로드할 수 있습니다. 법무팀에서는 레이블 지정 옵션을 검토하고 이 옵션을 통해 이 검토를 쉽게 수행할 것을 권장합니다. 데이터 거버넌스 UI에 로그인하는 동안 검토를 수행할 필요 없이 .CSV 파일을 공유할 수 있습니다.

1. 클릭 **[!UICONTROL CSV 내보내기]** 오른쪽 상단에서 이 대화 상자가 표시됩니다.

   ![](assets/export_csv.png)

1. 모든 데이터 거버넌스 설정을 내보낼 보고서 세트를 한 개 이상 선택합니다.

## 개인 정보 레이블 편집 {#edit}

을(를) 참조하십시오. [보고서 세트 개인 정보 레이블 지정 또는 편집](/help/admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md).