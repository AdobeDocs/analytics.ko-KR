---
description: Analysis Workspace에서 임시 세그먼트를 사용합니다.
title: 애드혹 세그먼트
feature: Segmentation
role: User, Admin
exl-id: 1c189abc-ab9f-413c-9be6-0d2fc457230e
source-git-commit: 931e9b0bd71abd852c515cd2e7d99dc9ae423a63
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 77%

---

# 임시 프로젝트 세그먼트

Ad Hoc 프로젝트 세그먼트를 사용하면 구성 요소를 패널 드롭 영역으로 바로 드래그하여 놓아 세그먼트를 만들 수 있습니다. 작성된 세그먼트는 현재 프로젝트에만 적용되는 [프로젝트 수준의 세그먼트](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/quick-segments.html?lang=ko-KR?#what-are-project-only-segments%3F)가 됩니다.

다음은 임시 프로젝트 세그먼트 만들기에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)

1. 구성 요소 유형(차원, 차원 항목, 이벤트, 지표, 세그먼트, 세그먼트 템플릿, 날짜 범위)을 패널 상단의 세그먼트 드롭 영역으로 드래그합니다. 구성 요소 유형은 자동으로 임시 세그먼트로 변환되거나, [빠른 세그먼트](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/quick-segments.html?lang=ko-KR) 호환되는 경우
다음은 Twitter 참조 도메인을 위한 세그먼트를 만드는 방법의 예입니다.

   ![](assets/ad-hoc1.png)

   패널에 이 세그먼트를 자동으로 적용하여 결과를 즉시 조회할 수 있습니다.

1. 패널에 세그먼트를 무제한으로 추가할 수 있습니다.
1. 이 세그먼트를 저장하기로 결정되면 아래의 다음 섹션을 참조하십시오.

다음 사항에 주의하십시오.

* 다음 구성 요소 유형을 세그먼트 영역으로 끌어 놓을 수 **없음**: 세그먼트를 빌드할 수 없는 계산된 지표 및 차원/지표.
* 전체 차원 및 이벤트에 대해 Analysis Workspace는 &quot;존재함&quot; 히트 세그먼트를 만듭니다. 예: `Hit where eVar1 exists` 또는 `Hit where event1 exists`.
* 세그먼트 드롭 영역에 ”지정되지 않음” 또는 ”없음”을 놓으면 세그먼테이션에서 올바로 처리되도록 자동으로 “존재하지 않음” 세그먼트로 변환됩니다.

작성하여 프로젝트 내에 적용할 수 있는 서로 다른 세그먼트를 비교하려면 [여기](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md)로 이동하십시오.

## 임시 세그먼트 저장 {#ad-hoc-save}

임시 세그먼트는 저장하여 다른 프로젝트에서 사용할 수 있도록 만들 수 있습니다.

1. 드롭 영역의 세그먼트에 마우스를 가져다 대고 “i” 아이콘을 클릭합니다.
1. 연필 모양의 편집 아이콘을 클릭하여 세그먼트 빌더로 이동합니다.
1. **[!UICONTROL 모든 프로젝트에 사용할 수 있도록 설정 및 구성 요소 목록 추가]**&#x200B;를 선택합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

저장하면 세그먼트를 왼쪽 레일 구성 요소 목록에서 사용할 수 있으며 세그먼트 관리자의 다른 사용자와 공유할 수 있게 됩니다.
