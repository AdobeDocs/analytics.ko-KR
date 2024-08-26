---
description: Analysis Workspace에서 차원 및 차원 항목을 분류합니다.
keywords: Analysis Workspace
title: 차원 분류
feature: Dimensions
role: User, Admin
exl-id: 0d26c920-d0d9-4650-9cf0-b67dbc4629e1
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 100%

---

# 차원 분류

Analysis Workspace에서 차원 및 차원 항목을 분류합니다.

구체적인 필요 사항들을 위해 원하는 방법으로 데이터를 분류할 수 있습니다. 적절한 지표, 차원, 세그먼트, 타임라인 및 기타 분석 분류 값을 사용하여 쿼리를 작성해 보십시오.

1. 데이터 테이블로 [프로젝트를 만듭니다](/help/analyze/analysis-workspace/home.md).
1. 데이터 테이블에서 라인 항목을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL 분류]** > *`<item>`*.

   ![단계 결과](assets/fa_data_table_actions.png)

   선택한 기간에 대해 차원 항목이나 대상자 세그먼트를 분류할 수 있습니다. 더 세부적인 수준으로 드릴다운할 수도 있습니다.

   >[!NOTE]
   >
   >테이블에 표시되는 분류의 수는 200개로 제한됩니다. 이 제한은 분류 내보내기에 대해서는 증가합니다.

## 분류에 속성 모델 적용

테이블 내의 모든 분류에는 모든 속성 모델이 적용될 수 있습니다. 이 속성 모델은 상위 열과 동일하거나 다를 수 있습니다. 예를 들어 마케팅 채널 차원에서 선형 주문을 분석하고 채널 내 특정 추적 코드에 U자형 주문을 적용할 수 있습니다. 분류에 적용되는 속성 모델을 편집하려면 다음과 같이 분류 모델 위로 마우스를 이동하고&#x200B;**[!UICONTROL 편집]**&#x200B;을 클릭합니다.

![분류 설정](assets/breakdown_settings.png)

이는 분류에 속성 모델을 적용하거나 편집할 때 예상되는 비헤이비어입니다.

* 다른 속성이 존재하지 않을 때 속성을 적용하는 경우 해당 속성이 전체 항목 트리에 적용됩니다.

* 속성이 적용된 후 분류를 추가하면 추가된 해당 분류에 대해 기본값이 사용됩니다(해당 차원에 기본값이 있는 경우). 그렇지 않은 경우 상위 열의 분류가 사용됩니다. 일부 차원에는 기본 할당이 있습니다. 예를 들어 [!UICONTROL 시간] 차원과 [!UICONTROL 레퍼러]는 [!UICONTROL 동일한 터치]를 사용합니다. [!UICONTROL 제품] 차원은 [!UICONTROL 마지막 터치]를 사용합니다. 다른 차원에는 기본값이 없으며 상위 열 할당을 사용합니다.

* 항목 트리에 속성이 이미 있는 경우 속성을 변경하면 편집 중인 속성만 변경됩니다.

## 비디오

Analysis Workspace에서 프로젝트에 치수 및 메트릭 추가하기

>[!VIDEO](https://video.tv.adobe.com/v/30606/?quality=12)

자유 양식 표에서 치수 작업하기

>[!VIDEO](https://video.tv.adobe.com/v/40179/?quality=12)

다음은 위치별 치수 분류에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/24033/?quality=12)
