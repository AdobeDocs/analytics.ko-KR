---
description: 지도 시각화를 사용하여 지리 지도 시각화에 데이터를 플롯합니다.
title: 맵
uuid: 6038f336-62a3-4efa-8316-4d7792468db3
feature: Visualizations
role: User, Admin
exl-id: a60544b4-27b6-413a-96ce-ab9487594422
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 76%

---

# 맵 {#map}

<!-- markdownlint-disable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_button"
>title="맵"
>abstract="이 시각화는 지표를 맵 위에 중첩되도록 표현합니다. 이 시각화는 지리적으로 다른 지역들의 데이터를 식별하는 데 유용합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_bubbles"
>title="버블"
>abstract="버블을 사용하여 이벤트를 플롯합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_heatmap"
>title="열 지도"
>abstract="히트맵을 사용하여 이벤트를 플롯합니다."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_이 문서에서는_ ![Adobe Analytics](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**&#x200B;의 맵 시각화에 대해 설명합니다._<br/>_이 문서의 [CustomerJourneyAnalytics](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/visualizations/map)_ Customer Journey Analytics![&#x200B; 버전에 대한 &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg)맵&#x200B;_&#x200B;**을(를) 참조하십시오.**&#x200B;_

>[!ENDSHADEBOX]



Analysis Workspace의 ![세계](/help/assets/icons/Globe.svg) **[!UICONTROL 맵]** 시각화

* 모든 지표(계산된 지표 포함)의 시각적 맵을 작성할 수 있도록 해 줍니다.
* 지리적으로 다른 지역들의 지표 데이터를 식별하고 비교하는 데 유용합니다.
* 모바일 사용에 따른 위도/경도 또는 웹 사용을 위한 지리적 차원, 이렇게 2가지 데이터 소스를 지원할 수 있습니다.
* PDF 내보내기를 지원합니다.
* 그래픽 디스플레이를 위해 WebGL을 활용합니다. 그래픽 드라이버가 WebGL 렌더링을 지원하지 않으면 드라이버를 업데이트해야 할 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Analysis Workspace의 맵 시각화](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/visualizations/map-visualization){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]


## 사용

1. ![맵](/help/assets/icons/Globe.svg) [!UICONTROL 맵] 시각화를 추가합니다. [패널 내에 시각화 추가](freeform-analysis-visualizations.md#add-visualizations-to-a-panel)를 참조하십시오. 자유 형식 테이블 위로만 맵 시각화를 끌 수 있습니다.

   ![맵 구성](assets/map-configuration.png){width="50%"}

1. 드롭다운 목록에서 지표를 선택합니다. 또는 지표(계산된 지표 포함) 목록에서 지표를 끌어옵니다.
1. 그리는 데 사용할 데이터 소스를 지정합니다. 이 대화 상자는 모바일 앱 데이터용으로 위치 추적이 활성화된 경우에만 표시됩니다.

   | 소스 | 설명 |
   | --- | --- |
   | **[!UICONTROL 모바일 위도/경도]** | 이 옵션은 모바일 앱 데이터를 나타냅니다. [!UICONTROL Analytics] > [!UICONTROL 관리] > [!UICONTROL 보고서 세트] > (보고서 세트 선택) > [!UICONTROL 설정 편집] > [!UICONTROL 모바일 관리]> [!UICONTROL 위치 추적 활성화]에서 보고서 세트에 대해 이 옵션을 활성화한 경우에만 이 옵션이 표시됩니다. 이 설정이 기본값입니다(위치 추적이 활성화된 경우). |
   | **[!UICONTROL 지역 차원]** | 이 옵션은 방문자의 IP 주소를 기반으로 방문자 위치에 대한 지리 특성 데이터를 나타냅니다. 이 데이터는 [!UICONTROL 국가], [!UICONTROL 지역] 및 [!UICONTROL 도시]로 변환됩니다. DMA나 우편 번호 수준으로는 이동하지 않습니다. 거의 모든 보고서 세트에 이 차원이 활성화되어 있습니다. 그렇지 않은 경우 Adobe 고객 지원 센터에 문의하여 지리적 보고서를 활성화하십시오. |

1. **[!UICONTROL 빌드]**&#x200B;를 선택합니다.

   버블이 포함된 세계 맵 시각화가 생성됩니다.

   ![](assets/bubble-world-view.png)

1. 이제 다음을 수행할 수 있습니다.

   * **확대/축소** - 맵을 더블 클릭하거나 스크롤 휠을 사용하여 특정 영역을 확대하도록 이 맵을 확대할 수 있습니다. 맵은 커서를 놓은 위치에 따라 확대됩니다. 확대/축소 상호 작용을 통해 확대/축소 수준에 따라 필요한 차원(국가 > 시/도 > 구/군/시)이 자동으로 업데이트됩니다.
   * **둘 이상의 맵 시각화를 나란히 배치하여 동일한 프로젝트에서**&#x200B;비교합니다.
   * **기간별(예: 연도별) 비교 표시**:

      * 음수를 표시합니다. 예를 들어 연도별 지표를 맵에 그리는 경우 뉴욕에 대해 -33%를 맵에 표시할 수 있습니다.
      * *퍼센트* 유형의 지표를 사용하면 클러스터링에서 백분율의 평균을 함께 계산합니다.
      * 녹색/빨간색 구성표: 양수/음수

   * **Ctrl** 키를 누른 채 맵을 이동하여 2D 또는 3D로 맵을 회전[!UICONTROL 합니다.]

   * **전환** - 아래 설명된 [설정](/help/analyze/analysis-workspace/visualizations/map-visualization.md#section_5F89C620A6AA42BC8E0955478B3A427E)을 사용하여 히트맵(열 지도)과 같은 다른 보기로 전환할 수 있습니다. 버블 보기가 기본 설정입니다.

1. 프로젝트를 **저장**&#x200B;하여 모든 맵 설정(좌표, 확대/축소, 회전)을 저장합니다.
1. 시각화 아래의 자유 형식 테이블은 왼쪽 레일에서 위치 차원과 지표를 드래그하여 채울 수 있습니다.



## 구성

맵 시각화를 재구성하려면 ![편집](/help/assets/icons/Edit.svg)을 선택합니다.


## 설정

시각화에 대한 설정을 정의하려면 ![설정](/help/assets/icons/Setting.svg)을 선택합니다.

| 설정 | 설명 |
|--- |--- |
| **[!UICONTROL 맵 유형]** | |
| **[!UICONTROL 버블] | 버블을 사용하여 이벤트를 플롯합니다. 거품형 차트는 산포도와 비례 영역 차트 간의 교차인 다중 변수 그래프입니다. 이 보기가 기본값입니다. |
| [!UICONTROL 히트맵] | 히트맵을 사용하여 이벤트를 플롯합니다. 히트맵은 매트릭스에 포함된 개별 값이 색상으로 표시되는 데이터를 그래픽으로 표시한 것입니다. |
| **[!UICONTROL 스타일]** | |
| [!UICONTROL 색상 테마] | 히트맵 및 버블의 색상 구성표를 보여 줍니다. 산호, 빨강, 녹색 또는 파랑 중에서 선택할 수 있습니다. 기본값은 코랄입니다. |
| [!UICONTROL 맵 스타일] | 기본, 도로, 더 밝게, 밝게, 어둡게, 위성 중에서 선택할 수 있습니다. |
| **[!UICONTROL 클러스터 반경]** | 지정된 픽셀 수 내에 있는 데이터 포인트를 그룹화합니다. 기본값은 50입니다. |
| **[!UICONTROL 사용자 정의 최대 값]** | 맵의 최대 값에 대한 임계값을 변경할 수 있도록 해 줍니다. 이 값을 조정하면 설정된 사용자 정의 최대 값에 비례하여 버블/히트맵 값(색상 및 크기)의 크기가 조정됩니다. |

<!--
## Build a time-parting heatmap

Here is a video on the topic:

>[!VIDEO](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/visualizations/build-a-time-parting-heatmap)

-->

