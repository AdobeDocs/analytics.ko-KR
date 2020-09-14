---
description: '개별 지표에 대한 세그먼트화는 동일한 보고서 내에서 지표 비교를 수행할 수 있도록 해줍니다. '
title: 세그먼트화된 지표
uuid: 88f9829b-76e4-4598-9494-084a91602bc1
translation-type: tm+mt
source-git-commit: 234a2eadfe02322daa886d2edbea042f8ad99e1e
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 59%

---


# 세그먼트화된 지표

계산된 지표 빌더에서 지표 정의 내에 세그먼트를 적용할 수 있습니다. 분석에 사용할 새 지표를 추출하려는 경우 유용합니다. 세그먼트 정의는 세그먼트 빌더를 통해 업데이트할 수 있습니다. 변경 사항이 있는 경우, 세그먼트는 계산된 지표 정의에 속하는지 등 세그먼트가 적용된 모든 곳에서 자동으로 업데이트됩니다.

![](assets/german-visitors.png)

## 세그먼트화된 지표 만들기 {#create}

&quot;독일 방문자&quot; 세그먼트의 여러 측면을 &quot;해외 방문자&quot; 세그먼트의 여러 측면과 비교하려고 한다고 가정해 보겠습니다. 다음과 같이 통찰력을 제공하는 지표를 만들 수 있습니다.

* 두 그룹 간 컨텐츠 탐색 행동은 어떻게 비교합니까? (다른 예: 두 세그먼트 간 전환 비율은 어떻게 비교합니까?)
* 총 방문자 수의 백분율로, 특정 페이지를 탐색하는 독일 방문자 수와 해외 방문자의 수는 어떻게 됩니까?
* 이렇게 다른 세그먼트에서 액세스한 컨텐츠의 측면에서 볼 때 차가 가장 큰 곳은 어디입니까?

1. 비교 가능한 세그먼트가 없는 경우 &quot;국가&quot;가 &quot;독일&quot;과 같은 계산된 지표 빌더에서 바로 애드혹 세그먼트를 만듭니다. 국가 차원을 정의 캔버스로 드래그하고 독일을 값으로 선택하면 됩니다.

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >[세그먼트 빌더](/help/components/segmentation/segmentation-workflow/seg-build.md)에서도 이 작업을 수행할 수 있지만 계산된 지표 빌더에서 차원을 사용 가능하도록 설정하여 워크플로우를 간소화했습니다. &quot;Adhoc&quot; means that the segment is not visible in the **[!UICONTROL Segments]** list in the left rail. 그러나 그 옆에 있는 &quot;i&quot; 아이콘 위에 마우스를 올려놓고 **[!UICONTROL 공개하기]**&#x200B;를 클릭하여 공개할 수 있습니다.

1. 비교 가능한 세그먼트가 없을 경우에는 &quot;해외 방문자&quot;라는 세그먼트를 만드십시오. 여기서 &quot;국가&quot;는 &quot;독일&quot;과 같지 않습니다.
1. 독일 방문자 세그먼트를 [정의] 캔버스로 드래그하고 고유 방문자 수 지표를 그 안에 드래그하여 &quot;미국 방문자&quot;라는 지표를 만들고 저장하십시오.

   ![](assets/german-visitors.png)

1. 해외 방문자 세그먼트와 고유 방문자 수 지표를 사용하여 3단계를 반복하여 해외 방문자 지표를 만듭니다.
1. Analysis Workspace에서 **[!UICONTROL Page]** 차원을 자유 형식 테이블로 드래그하고 서로 옆에 있는 계산된 두 개의 지표를 위쪽으로 끕니다.

   ![](assets/workspace-pages.png)

## 총 지표 비율 {#percent-total}

세그먼트를 총 모집단과 비교하여 위 예제를 한 단계 더 가져올 수 있습니다. 이렇게 하려면 두 개의 새 지표 &quot;총 독일 방문자의 %&quot;와 &quot;총 해외 방문자의 %&quot;를 만드십시오.

1. 독일(또는 해외) 방문자 세그먼트를 캔버스에 넣으십시오.
1. 아래에 다른 독일(또는 해외) 방문자 세그먼트를 넣으십시오. 하지만, 이때, 그 구성(톱니바퀴) 아이콘을 클릭하여 지표 유형 &quot;합계&quot;를 선택합니다. 형식은 &quot;퍼센트&quot;여야 합니다. 연산자는 &quot;나누기&quot;여야 합니다. 다음 지표 정의로 종료합니다.

   ![](assets/cm_metric_total.png)

1. 이 지표를 프로젝트에 적용합니다.

   ![](assets/cm_percent_total.png)

