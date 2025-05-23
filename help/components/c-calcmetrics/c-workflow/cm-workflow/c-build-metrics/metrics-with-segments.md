---
description: 개별 지표에 대한 세그먼트화는 동일한 보고서 내에서 지표 비교를 수행할 수 있도록 해 줍니다.
title: 세그먼트화된 지표
feature: Calculated Metrics
exl-id: 1e7e048b-9d90-49aa-adcc-15876c864e04
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 68%

---

# 세그먼트화된 지표

계산된 지표 빌더에서는 지표 정의 내에서 세그먼트를 적용할 수 있습니다. 분석에 사용할 새 지표를 도출하려는 경우 유용합니다. 세그먼트 정의는 세그먼트 작성 도구를 통해 업데이트할 수 있습니다. 변경된 경우 세그먼트는 계산된 지표 정의의 일부인 경우를 포함하여 적용되는 모든 위치에서 자동으로 업데이트됩니다.

![](assets/german-visitors.png)

## 세그먼트 지표 만들기 {#create}

“독일 방문자” 세그먼트의 다양한 측면을 “해외 방문자” 세그먼트의 다양한 측면과 비교하려고 한다고 가정해 보겠습니다. 다음과 같이 통찰력을 제공하는 지표를 만들 수 있습니다.

* 두 그룹 간 콘텐츠 탐색 행동은 어떻게 비교합니까? (다른 예: 두 세그먼트 간 전환 비율은 어떻게 비교합니까?)
* 해외 방문자 수 대비 특정 페이지를 탐색하는 독일인 방문자 수는 전체 방문자 수의 백분율로 얼마나 됩니까?
* 이렇게 다른 세그먼트에서 액세스한 콘텐츠의 측면에서 볼 때 차가 가장 큰 곳은 어디입니까?

&quot;독일 방문자&quot;라는 지표와 &quot;해외 방문자&quot;라는 지표를 작성하고 저장합니다.

1. 계산된 지표 빌더에서 &quot;국가&quot;가 &quot;독일&quot;인 &quot;독일 방문자&quot;라는 임시 세그먼트를 만듭니다.

   국가 차원을 정의 캔버스로 드래그하고 값으로 [!UICONTROL **독일**]&#x200B;을(를) 선택합니다.

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >[세그먼트 빌더](/help/components/segmentation/segmentation-workflow/seg-build.md)에서도 이 작업을 수행할 수 있지만 계산된 지표 빌더에서 차원을 사용 가능하도록 설정하여 워크플로를 간소화했습니다. “임시”는 세그먼트가 왼쪽 레일의 **[!UICONTROL 세그먼트]** 목록에 표시되지 않는다는 의미입니다. 그러나 그 옆에 있는 “i” 아이콘 위에 마우스를 올려놓고 **[!UICONTROL 공개하기]**&#x200B;를 클릭하여 공개할 수 있습니다.

1. 독일 세그먼트를 정의 캔버스로 드래그하고 고유 방문자 수 지표를 그 안으로 드래그합니다.

   ![](assets/german-visitors.png)

1. [!UICONTROL **저장**]&#x200B;을 선택하여 계산된 지표를 저장합니다.

1. 계산된 지표 빌더에서 &quot;국가&quot;가 &quot;독일&quot;과 같지 않은 &quot;해외 방문자&quot;라는 임시 세그먼트를 만듭니다.

   국가 차원을 정의 캔버스로 드래그하고 값으로 [!UICONTROL **독일**]&#x200B;을 선택한 다음 연산자로 [!UICONTROL **같지 않음**]&#x200B;을 선택합니다.

1. 그 안에 있는 고유 방문자 수 지표를 드래그합니다.

1. [!UICONTROL **저장**]&#x200B;을 선택하여 계산된 지표를 저장합니다.

1. Analysis Workspace에서 **[!UICONTROL Page]** 차원을 자유 형식 테이블로 드래그하고 서로 옆에 있는 계산된 두 개의 지표를 위쪽으로 끕니다.

   ![](assets/workspace-pages.png)


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트화된 지표](https://video.tv.adobe.com/v/32602?quality=12&learn=on&captions=kor){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]


## 총 지표의 백분율 {#percent-total}

세그먼트를 전체 모집단과 비교하여 위의 예를 한 단계 더 발전시킬 수 있습니다. 그러기 위해 두 가지 새 지표 “총 독일 방문자의 %”와 “총 해외 방문자의 %”를 만드십시오.

1. 독일 (또는 해외) 방문자 세그먼트를 캔버스에 넣으십시오.
1. 아래에 다른 독일 (또는 해외) 방문자 세그먼트를 넣으십시오. 하지만, 이때, 그 구성 (톱니바퀴) 아이콘을 클릭하여 지표 유형 &quot;합계&quot;를 선택합니다. 형식은 &quot;퍼센트&quot;여야 합니다. 연산자는 &quot;나누기&quot;여야 합니다. 다음 지표 정의로 종료합니다.

   ![](assets/cm_metric_total.png)

1. 이 지표를 프로젝트에 적용합니다.

   ![](assets/cm_percent_total.png)
