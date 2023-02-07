---
source-git-commit: 85d59d0a2b94953af457527a56d46faefb3ea94c
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 25%

---
# 스니펫

## Reports &amp; Analytics 서비스 종료 공지 {#ra-eol}

>[!IMPORTANT]
>
>Reports &amp; Analytics [서비스 종료 공지](https://express.adobe.com/page/6WnF8JK6IRDhf/)에 대해 자세히 알아보십시오.

## 데이터 사전 필터 기준 {#dd-filter-criteria}

1. (선택 사항) **필터** 아이콘 ![데이터 사전 필터 아이콘](/help/analyze/analysis-workspace/components/data-dictionary/assets/data-dictionary-filter-icon.png)을 선택한 다음, 다음 필터 옵션 중 하나를 선택하여 구성 요소 목록을 필터링합니다.

   | 옵션 | 함수 |
   |---------|----------|
   | [!UICONTROL **차원**] | Dimension인 구성 요소만 표시합니다. (이 옵션은 [!UICONTROL **빠른 필터**] 데이터 사전에 처음 액세스할 때 탭을 클릭합니다.) |
   | [!UICONTROL **지표**] | 지표인 구성 요소만 표시합니다. (이 옵션은 [!UICONTROL **빠른 필터**] 데이터 사전에 처음 액세스할 때 탭을 클릭합니다.) |
   | [!UICONTROL **세그먼트**] | 세그먼트인 구성 요소만 표시합니다. (이 옵션은 [!UICONTROL **빠른 필터**] 데이터 사전에 처음 액세스할 때 탭을 클릭합니다.) <!--this is Filters in CJA--> |
   | [!UICONTROL **날짜 범위**] | 날짜 범위인 구성 요소만 표시합니다. (이 옵션은 [!UICONTROL **빠른 필터**] 데이터 사전에 처음 액세스할 때 탭을 클릭합니다.) |
   | [!UICONTROL **설명이 없습니다.**] | 설명 필드에 아직 설명이 없는 구성 요소만 표시합니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | [!UICONTROL **중복 항목**] | 선택한 보고서 세트의 다른 구성 요소와 동일한 레이블 또는 설명이 있는 구성 요소만 표시합니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | [!UICONTROL **최근 데이터 없음**] | 지난 90일 동안 데이터를 수집하지 않은 구성 요소만 표시합니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | [!UICONTROL **Adobe 작성**] | Adobe에서 만든 구성 요소만 표시합니다. 관리자나 조직의 다른 사용자가 만든 구성 요소는 표시되지 않습니다. |
   | [!UICONTROL **승인됨**] | 관리자가 승인됨으로 표시한 구성 요소만 표시합니다. |
   | 승인되지 않음(관리자에게만 사용 가능) | <!--this is in the requirements doc, but I don't see this in the UI--> |

   {style=&quot;table-layout:auto&quot;}

## 데이터 사전 구성 요소 정보 {#dd-component-information}

| 옵션 | 함수 |
|---------|----------|
| [!UICONTROL **승인됨**] | 관리자가 구성 요소를 검토하고 승인했음을 나타냅니다. 관리자는 [!UICONTROL **승인 필요**] 승인되지 않은 구성 요소에 대한 옵션. 이 옵션을 선택하면 승인됨으로 표시됩니다. |
| [!UICONTROL **설명**] | 구성 요소의 의도된 기능을 설명합니다. (이 정보는 다음에 설명된 대로 Analytics 관리자가 추가합니다. [구성 요소 설명 추가](/help/analyze/analysis-workspace/components/add-component-descriptions.md)) |
| [!UICONTROL **다음과 함께 자주 사용됨**] | 5개의 기본 구성 요소 유형에서 보고 있는 구성 요소와 함께 가장 일반적으로 사용되는 5개의 구성 요소를 표시합니다. 지표, 계산된 지표, Dimension, 세그먼트 및 날짜 범위. 이 목록은 지난 90일의 데이터를 기반으로 합니다. 보기에 액세스할 수 있는 구성 요소만 표시됩니다. |
| [!UICONTROL **다음과 유사**] | 5개의 기본 구성 요소 유형에 대해 보고 있는 구성 요소와 유사한 레이블이 있는 최대 5개의 구성 요소를 표시합니다. 지표, 계산된 지표, Dimension, 세그먼트 및 날짜 범위. 보기에 액세스할 수 있는 구성 요소만 표시됩니다. |
| [!UICONTROL **태그**] | 구성 요소에 적용되는 모든 태그를 표시합니다. |
| [!UICONTROL **구성 요소 유형**] | 구성 요소의 유형, Dimension, 지표, 세그먼트 또는 날짜 범위 등을 나열합니다. |
| [!UICONTROL **작성자**] | 구성 요소를 만든 사용자의 이름을 표시합니다. |
| [!UICONTROL **미리보기**] | Analysis Workspace에서 구성 요소가 어떻게 보이는지에 대한 미리 보기를 표시합니다. |
| [!UICONTROL **마지막으로 수정한 날짜**] | 구성 요소를 마지막으로 수정한 날짜를 표시합니다. 이 섹션은 세그먼트, 계산된 지표 및 날짜 범위를 볼 때 표시됩니다. <!--for CJA, it is displayed for all components--> |

{style=&quot;table-layout:auto&quot;}

## 릴리스 단계 제한된 테스트 {#release-limited-testing}

>[!AVAILABILITY]
>
>이 문서에서 설명하는 기능은 릴리스의 제한된 테스트 단계에 있으며 사용자 환경에서 아직 사용하지 못할 수 있습니다. 기능이 일반적으로 제공되면 이 메모는 제거됩니다. Analytics 릴리스 프로세스에 대한 자세한 내용은 [Adobe Analytics 기능 릴리스](/help/release-notes/releases.md)를 참조하십시오.

## 릴리스 단계 제한된 테스트 섹션 {#release-limited-testing-section}

>[!AVAILABILITY]
>
>이 섹션에서 설명하는 기능은 릴리스의 제한된 테스트 단계에 있으며 사용자 환경에서 아직 사용하지 못할 수 있습니다. 기능이 일반적으로 제공되면 이 메모는 제거됩니다. Analytics 릴리스 프로세스에 대한 자세한 내용은 [Adobe Analytics 기능 릴리스](/help/release-notes/releases.md)를 참조하십시오.

