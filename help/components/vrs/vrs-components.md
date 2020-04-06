---
description: 분석 작업 공간에 구성 요소를 포함 및 제외하도록 가상 보고서 세트를 조정할 수 있습니다.
title: 가상 보고서 세트 구성 요소 큐레이션
uuid: 6c6a4071-22ad-4e8c-b1ed-140b2aa04f76
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 가상 보고서 세트 구성 요소 큐레이션

분석 작업 공간에 구성 요소를 포함 및 제외하도록 가상 보고서 세트를 조정할 수 있습니다.

>[!NOTE]구성 요소 관리자 및 관리자가 아닌 사용자가 조정된 Workspace 프로젝트 및 조정된 VRS(가상 보고서 세트)에서 볼 수 있게 변경되었습니다. 이전에는, 누구나 아이콘을 클릭하여 조정되지 않은 구성 요소를 볼 수 **[!UICONTROL Show all Components]**&#x200B;있었습니다. The [updated curation experience](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/curate-projects-vrs.html) allows for more fine-grained control over which components are visible.

구성 요소 큐레이션을 사용하려면 다음을 수행하십시오.

1. Go to **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Virtual Report Suites]** > **[!UICONTROL Create new virtual report suite]**.
1. 을 정의한 **[!UICONTROL Settings]**&#x200B;후 **[!UICONTROL Components]** 탭을 클릭합니다.

1. 확인란을 **[!UICONTROL Enable Customization of Virtual Report Suite Components]**&#x200B;선택합니다.

   ![](assets/vrs-enable.png)

   >[!NOTE]
   >
   >**** 구성 요소 사용자 지정을 활성화한 경우 가상 보고서 세트는 Analysis Workspace에서만 액세스할 수 있고, 다음에서는 액세스할 수 없습니다.

   * [!UICONTROL Reports & Analytics]
   * [!UICONTROL Ad Hoc Analysis]
   * [!UICONTROL Data Warehouse]
   * [!UICONTROL Report Builder]
   * Analytics 보고 API
   이 확인란을 선택하면 해당 구성 요소를 &quot;제외된 구성 요소&quot; 열에서 &quot;포함된 구성 요소&quot; 열로 드래그하여 가상 보고서 세트에 포함할 구성 요소를 추가할 수 있습니다. 포함 및 제외할 수 있는 구성 요소는 다음과 같습니다.

   * 차원
   * 지표
   * 세그먼트
   * 데이터 범위
   >[!NOTE]
   >
   >조정된 구성 요소(세그먼트, 계산된 지표, 날짜 범위)를 더 이상 *공유*&#x200B;하지 않아도 됩니다. 이러한 구성 요소가 공유되지 않아도 가상 보고서 세트에 대해 조정된 경우 항상 Analysis Workspace에 표시됩니다.

1. Additionally, you can filter or search the components and add the entire filtered selection to the included column by clicking **[!UICONTROL Add All]**.

   ![](assets/vrs-add-all.png)

## 구성 요소 이름 바꾸기 {#section_0F7CD9F684FE4765BC00A2AFED56550E}

가상 보고서 세트와 관련된 포함된 구성 요소의 표시 이름을 변경할 수 있습니다. 예를 들어, 가상 보고서 세트에 페이지 이름을 포함하되 모바일 친화적인 컨텍스트로 이름을 바꾸려는 경우 앱 화면으로 변경할 수 있습니다. 이 가상 보고서 세트가 사용될 때마다 새 이름이 분석 작업 공간에 표시됩니다.

![](assets/vrs-rename-component.png)

분석 작업 공간에서 포함된 구성 요소에 대한 정보 아이콘을 클릭하여 이름이 변경된 구성 요소의 원래 이름을 표시합니다.

![](assets/vrs-aw-renamed.png)

## 구성 요소 그룹 {#section_483BEC76F49E46ADAAA03F0A12E48426}

구성 요소 그룹을 사용하여 가상 보고서 세트에 일괄 구성 요소를 추가합니다. 예를 들어 모바일 앱 분석과 관련된 기본 구성 요소 세트를 가져오려면 모바일 앱 그룹을 선택합니다. 해당 차원 및 지표 세트(이미 이름이 변경됨)가 가상 보고서 세트 포함 목록에 자동으로 추가됩니다.

![](assets/vrs-comp-grp.png)

## 작업 영역 동작 {#section_6C32F8B642804C0097FCB14E21028D4A}

Analysis Workspace에서 조정에 대한 자세한 내용은 [프로젝트 조정 및 공유](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/curate.html)를 참조하십시오.
