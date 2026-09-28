---
description: 분류는 값을 그룹으로 분류하고 그룹 수준에서 보고하는 데 사용됩니다. 예를 들어 모든 유료 검색 캠페인을 "팝 뮤직 용어" 같은 카테고리로 분류하고 인스턴스 (클릭스루라고도 함) 같은 지표와 관련한 해당 카테고리의 성공 및 성공 이벤트로의 전환을 보고합니다.
title: 전환 분류
feature: Classifications
role: Admin
exl-id: b4855000-adf3-4e3b-af36-f4803383126d
TQID: 'https://experienceleague.adobe.com/k8wtT-XfijkEOgPHw4j78mm8Da4BA4V3TVVfW6fpCp4'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: 00071d55-23eb-5795-a8d9-9d9b784f2791
    internal-label: Classifications
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 92%
---
# 전환 분류

분류는 값을 그룹으로 분류하고 그룹 수준에서 보고하는 데 사용됩니다. 예를 들어 모든 [!UICONTROL 유료 검색] 캠페인을 *팝 뮤직 용어*&#x200B;와 같은 범주로 분류하고 인스턴스(클릭스루)와 같은 지표와 관련한 해당 범주의 성공 및 성공 이벤트로의 전환에 대해 보고할 수 있습니다. 변수에 최대 255개의 분류를 추가할 수 있습니다.

**[!UICONTROL Analytics]** > **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 분류]**

전환 분류를 사용하면 전환 변수를 분류할 수 있습니다. 분류가 완료되면 키 데이터를 사용하여 생성할 수 있는 모든 보고서를 관련 데이터 속성을 사용해서도 생성할 수 있습니다.

>[!WARNING]
>
>분류 이름을 바꾸면 [분류 규칙 작성기](/help/components/classifications/crb/classification-rule-builder.md)에서 생성된 기존 규칙에 문제가 발생할 수 있습니다. 분류 규칙이 있는 분류의 이름을 바꾸는 경우 이름이 바뀐 분류를 가리키도록 각 규칙을 수정해야 합니다.

## 전환 분류 설명

| 요소 | 설명 |
| --- | --- |
| 이름 | 분류 이름입니다 |
| 활성화된 날짜 (텍스트만) | 텍스트 분류가 캠페인 변수의 날짜 범위인지 여부를 나타냅니다. |
| 옵션 (텍스트만) | 이 분류에 사용 가능한 분류 값 목록을 만듭니다. 캠페인 변수와 함께 옵션을 사용하여 캠페인 관리자에서 분류에 대해 지원되는 값 목록을 사용자에게 제공합니다. |
| 숫자 유형 (숫자만) | 숫자 분류에서 숫자 유형을 지정합니다. 옵션에는 숫자, 백분율 및 통화가 포함됩니다. |

## 전환 분류 추가

[관리]에 전환 분류를 추가하려면 다음 작업을 수행합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. 보고서 세트 선택.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 분류]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 분류 유형 선택]** 드롭다운 목록에서 분류를 추가하려는 변수를 선택합니다.

   ![단계 정보](/help/admin/tools/assets/sub_class_create.png)

1. **[!UICONTROL 분류 편집]** 아이콘으로 마우스를 가져간 다음 **[!UICONTROL 분류 추가]**&#x200B;를 선택합니다.
1. **[!UICONTROL 테스트 분류]** 대화 상자에서 원하는 대로 분류를 구성합니다.

1. 드롭다운 목록 대화 상자에서 옵션을 추가하거나 제거합니다.

   옵션을 추가하면 이 분류에 사용 가능한 분류 값 목록이 만들어집니다. 캠페인 변수와 함께 이 옵션을 사용하여 캠페인 관리자에서 분류에 대해 지원되는 값 목록을 사용자에게 제공할 수 있습니다. 거의 변경되지 않거나 절대 변경되지 않는 작은 수의 허용된 값이 있는 분류 차원에 대해 사용하십시오. 예를 들어 실버, 골드 및 플래티넘과 같이 다양한 수준의 고객 충성도를 대상으로 하는 다양한 캠페인을 실행할 수 있습니다. 그런 다음 드롭다운 목록을 사용하여 허용되는 값이 세 수준과 일치하는 값뿐이도록 할 수 있습니다. 다른 값을 사용하려는 사용자가 있으면 무시됩니다.

1. **[!UICONTROL 저장을]** 클릭합니다.

## 전환 분류 삭제

더 이상 필요하지 않은 전환 분류를 삭제합니다.

1. 세트 헤더에서 **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭하여 보고서 세트 관리자를 엽니다.
1. 보고서 세트 선택.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 분류]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 분류 유형 선택]** 드롭다운 목록에서 분류를 삭제하려는 변수를 선택합니다.
1. **[!UICONTROL 분류 편집]** 아이콘으로 마우스를 가져간 다음 **[!UICONTROL 분류 삭제]**&#x200B;를 선택합니다.
1. 분류 삭제 대화 상자에서 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.
