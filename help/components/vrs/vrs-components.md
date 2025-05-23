---
description: 가상 보고서 세트는 Analysis Workspace에 구성 요소를 포함하거나 제외하도록 큐레이션할 수 있습니다.
title: 가상 보고서 세트 구성 요소 큐레이션
feature: VRS
exl-id: 19163829-328a-4064-b1be-8c09d1d94a0d
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 92%

---

# 가상 보고서 세트 구성 요소 큐레이션

가상 보고서 세트는 Analysis Workspace에 구성 요소를 포함하거나 제외하도록 큐레이션할 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [구성 요소 큐레이션](https://video.tv.adobe.com/v/3425527?quality=12&learn=on&captions=kor){target="_blank"}을 참조하십시오.

>[!ENDSHADEBOX]


>[!NOTE]
>
>구성 요소 관리자 및 비관리자가 선별된 Workspace 프로젝트 및 선별된 가상 보고서 세트에서 볼 수 있도록 변경되었습니다. 이전에는 **[!UICONTROL 모든 구성 요소 표시]**&#x200B;를 클릭하면 누구나 조정되지 않은 구성 요소를 볼 수 있었습니다. [업데이트된 조정 환경](/help/analyze/analysis-workspace/curate-share/curate.md)에서는 표시되는 구성 요소를 보다 세밀하게 제어할 수 있습니다.

구성 요소 큐레이션을 사용하려면 다음을 수행하십시오.

1. **[!UICONTROL Analytics]** > **[!UICONTROL 구성 요소]** > **[!UICONTROL 가상 보고서 세트]** > **[!UICONTROL 새 가상 보고서 세트 만들기]**(으)로 이동합니다.
1. **[!UICONTROL 설정]**&#x200B;을 정의한 후 **[!UICONTROL 구성 요소]** 탭을 클릭합니다.

1. **[!UICONTROL 가상 보고서 세트 구성 요소의 사용자 지정 사용]** 확인란을 선택하십시오.

   ![](assets/vrs-enable.png)

   >[!NOTE]
   >
   >**&#x200B;** 구성 요소 사용자 지정을 활성화한 경우 가상 보고서 세트는 Analysis Workspace에서만 액세스할 수 있고, 다음에서는 액세스할 수 없습니다.
   >
   >* [!UICONTROL Data Warehouse]
   >* [!UICONTROL Report Builder]
   >* [!UICONTROL Activity Map]
   >* Analytics Reporting API

   이 옵션을 선택하면 &quot;제외된 구성 요소&quot; 열의 해당 구성 요소를 &quot;포함된 구성 요소&quot; 열로 드래그하여 가상 보고서 세트에 포함할 구성 요소를 추가할 수 있습니다. 포함하거나 제외할 수 있는 구성 요소는 다음과 같습니다.

   * 차원
   * 지표
   * 세그먼트
   * 데이터 범위

   >[!NOTE]
   >
   >조정된 구성 요소(세그먼트, 계산된 지표, 날짜 범위)를 더 이상 *공유*&#x200B;하지 않아도 됩니다. 이러한 구성 요소가 공유되지 않아도 가상 보고서 세트에 대해 조정된 경우 항상 Analysis Workspace에 표시됩니다.

1. 또한 **[!UICONTROL 모두 추가]**&#x200B;를 클릭하여 구성 요소를 필터링하거나 검색하고 필터링된 전체 선택을 포함된 열에 추가할 수 있습니다.

   ![](assets/vrs-add-all.png)

## 구성 요소 이름 바꾸기 {#section_0F7CD9F684FE4765BC00A2AFED56550E}

가상 보고서 세트와 관련된 포함된 구성 요소의 표시 이름을 변경할 수 있습니다. 예를 들어 페이지 이름을 가상 보고서 세트에 포함하되, 모바일 친화적인 이름으로 변경하려면 앱 화면으로 변경할 수 있습니다. 이 가상 보고서 세트를 사용할 때마다 Analysis Workspace에 새 이름이 표시됩니다.

![](assets/vrs-rename-component.png)

Analysis Workspace에서 포함된 구성 요소의 정보 아이콘을 클릭하여 이름이 바뀐 구성 요소의 원래 이름을 표시합니다.

![](assets/vrs-aw-renamed.png)

## 구성 요소 그룹 {#section_483BEC76F49E46ADAAA03F0A12E48426}

구성 요소 그룹을 사용하여 가상 보고서 세트에 대량 구성 요소를 추가하십시오. 예를 들어 모바일 앱 분석과 관련된 기본 구성 요소 세트를 가져오려면 모바일 앱 그룹을 선택하십시오. 해당 차원 및 지표 세트 (이미 이름이 변경됨)는 가상 보고서 세트의 포함된 목록에 자동으로 추가됩니다.

![](assets/vrs-comp-grp.png)

## Workspace 비헤이비어 {#section_6C32F8B642804C0097FCB14E21028D4A}

Analysis Workspace의 조정에 대한 자세한 내용은 [프로젝트 조정 및 공유](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=ko-KR)를 참조하십시오.
