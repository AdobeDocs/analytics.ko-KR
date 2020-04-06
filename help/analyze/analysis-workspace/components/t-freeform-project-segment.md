---
description: 'null'
title: 세그먼트
uuid: 677f6030-5b3e-4dfa-bb79-9f27f3382fb1
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 세그먼트 {#topic_DC2917A2E8FD4B62816572F3F6EDA58A}

## 세그먼트 레일 {#section_3B07D458C43E42FDAF242BB3ACAF3E90}

구성 요소 메뉴 아래의 세그먼트 레일은 다음 아이콘으로 세그먼트 템플릿과 세그먼트를 표시합니다.

![](assets/segment_icons.png)

[Analysis Workspace에서 세그먼트 사용 - YouTube](https://www.youtube.com/watch?v=QlUCdQDnni4)(6:46)

## 세그먼트 만들기 {#section_693CFADA668B4542B982446C2B4CF0F5}

모든 구성 요소 유형(차원, 차원 항목, 이벤트, 지표, 세그먼트, 세그먼트 템플릿, 날짜 범위)을 패널 상단의 세그먼트 드롭 영역에 놓아 즉시 세그먼트를 만들 수 있습니다.

구성 요소 유형은 자동으로 세그먼트로 변환됩니다. 또는 세그먼트 추가 드롭박스에서 &quot;+&quot; 기호를 클릭할 수도 있습니다.

주의 사항:

* 다음 구성 요소 유형은 세그먼트 영역에 놓을 수 **없습니다** .세그먼트를 만들 수 없는 계산된 지표 및 차원/지표.
* 전체 차원 및 이벤트의 경우 분석 작업 공간에서 &quot;존재함&quot; 히트 세그먼트를 만듭니다. 예:&quot;eVar1이 있는 히트&quot; 또는 &quot;event1이 있는 히트&quot;입니다.
* 세그먼트를 놓는 영역에 &quot;지정되지 않음&quot; 또는 &quot;없음&quot;을 놓으면 세그멘테이션에서 올바로 처리되도록 자동으로 &quot;존재하지 않음&quot; 세그먼트로 변환됩니다.

![](assets/segment-dropzone.png)

>[!NOTE] 이러한 방식으로 생성된 세그먼트는 프로젝트 내부에서 사용됩니다.

다음 단계를 수행하여 이러한 세그먼트를 공개(글로벌)하도록 선택할 수 있습니다.

1. 놓기 영역의 세그먼트 위로 마우스를 가져간 다음 &quot;i&quot; 아이콘을 클릭합니다.
1. In the information panel that displays, click **[!UICONTROL Make public]**.

   ![](assets/segment-info.png)

## 세그먼트를 적용하는 다른 방법 {#section_10FF2E309BA84618990EA5B473015894}

자유 형식 프로젝트에 세그먼트를 적용하는 다른 몇 가지 방법이 있습니다.

| 작업 | 설명 |
|--- |--- |
| 선택 항목에서 세그먼트 만들기 | 인라인 세그먼트를 만듭니다. 행을 선택하고 선택 항목을 마우스 오른쪽 단추로 클릭한 다음 인라인 세그먼트를 만듭니다. 이 세그먼트는 열려 있는 프로젝트에만 적용되며, Analytics 세그먼트로 저장되지는 않습니다. 1. 행을 선택합니다. 2. 선택 항목을 마우스 오른쪽 단추로 클릭합니다. 3. *선택 항목으로 세그먼트 만들기*&#x200B;를 클릭합니다. |
| 구성 요소 > 새 세그먼트 | 세그먼트 빌더를 표시합니다. 세그멘테이션에 대한 자세한 내용은 [세그먼트 빌더](https://docs.adobe.com/content/help/ko-KR/analytics/components/segmentation/segmentation-workflow/seg-build.html)를 참조하십시오. |
| 공유 > 프로젝트 공유 또는 공유 > 프로젝트 데이터 조정 | [조정 및 공유](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6)에서, 수신자를 위한 공유 분석에서 프로젝트에 적용하는 세그먼트를 어떻게 사용할 수 있는지 알아봅니다. |
| 세그먼트를 차원으로 사용 | 비디오:분석 [작업 공간에서 세그먼트를 차원으로 사용](https://www.youtube.com/watch?v=WmSdReKTWto&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&amp;index=39) |
