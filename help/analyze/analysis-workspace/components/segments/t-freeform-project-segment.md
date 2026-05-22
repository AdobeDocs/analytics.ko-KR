---
description: Analysis Workspace 및 Adobe Analytics에서 세그먼트를 만들고 사용하는 방법에 대해 알아봅니다.
title: 세그먼트 개요
feature: Segmentation
role: User, Admin
exl-id: 67112e13-4d0a-4d77-be50-496c3d28779c
TQID: https://experienceleague.adobe.com/lvP1xaDFJOjAhwGNkLtTsSHhaNdOnMOnqRh7YgwaVNs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b0ca67c6-0a35-482c-ad91-baac1bcb26d6
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: a544b409-2610-410d-a842-474ac1d0d54e
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
  - id: e38cbddc-1633-4cd5-bed5-9f289f2a6029
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 355
ht-degree: 37%

---

# 세그먼트 개요

세그먼트의 복잡성과 해당 프로젝트의 적용 여부에 따라 Analysis Workspace 및 Customer Journey Analytics에서 세그먼트를 만들고 사용할 수 있습니다. 세그먼트 유형에 대한 요약은 다음과 같습니다.

| 세그먼트 유형 | 수행 | 적용 가능한 영역은? | 사용 시기 |
| --- | --- | --- | --- |
| 구성 요소 목록 세그먼트 | [세그먼트를 만드는 방법](/help/components/segmentation/segmentation-workflow/seg-create.md)을 참조하세요. | 모든 작업 영역 프로젝트 | 복잡한 세그먼트의 경우는 순차적 세그먼트 |
| 빠른 세그먼트 | [빠른 세그먼트 빌더](/help/analyze/analysis-workspace/components/segments/quick-segments.md) | 프로젝트만 저장하고 세그먼트 목록에 추가할 수 있습니다. | 임시 단일 규칙 세그먼트(끌어다 놓기 사용)에 사용하거나, 여러 규칙(세그먼트 아이콘 클릭)을 추가/편집하는 데 사용할 수 있습니다 |
| 계산된 지표 기반 세그먼트 | [계산된 지표 빌더](/help/components/calculated-metrics/workflow/c-build-metrics/metrics-with-segments.md) | 계산된 개별 지표에 | 지표 정의 내 세그먼트 적용 |
| 가상 보고서 세트 기반 세그먼트 | [가상 보고서 세트 빌더](/help/components/vrs/c-workflow-vrs/vrs-create.md) | 개별 가상 보고서 세트에 | 가상 보고서 세트 정의 내 세그먼트 적용 |

## 비디오

>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Analysis Workspace에서 세그먼트 사용](https://video.tv.adobe.com/v/31083?captions=kor&quality=12&learn=on){target="_blank"}을 참조하십시오.

>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트 찾기 및 만들기](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/components/segmentation/finding-and-creating-segments){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트의 롤링 기간](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/components/segmentation/rolling-date-ranges-in-segments){target="_blank"}을 참조하세요.

>[!ENDSHADEBOX]


## 세그먼트 만들기 {#section_693CFADA668B4542B982446C2B4CF0F5}

Analysis Workspace에서 다음과 같이 서로 다른 유형의 세그먼트를 만들 수 있습니다.

* [빠른 세그먼트](/help/analyze/analysis-workspace/components/segments/quick-segments.md)
* [세그먼트 빌더](/help/components/segmentation/segmentation-workflow/seg-build.md)에서 만들고 [세그먼트 관리자](/help/components/segmentation/segmentation-workflow/seg-manage.md)에 끝나는 [일반 세그먼트](/help/components/segmentation/segmentation-workflow/seg-create.md)


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트를 적용하는 다른 방법](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/applying-segments-to-your-analysis-workspace-project){target="_blank"}을 참조하십시오.

>[!ENDSHADEBOX]


## 세그먼트 비교

세그먼트 비교는 다음 기능으로 구성됩니다.

* [세그먼트 비교 패널:](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md) 두 세그먼트를 패널에 드래그하고 통계적으로 중요한 차이점과 두 대상자 간의 겹침을 보여 주는 포괄적인 보고서를 살펴보십시오.
* [폴아웃의 세그먼트 비교:](/help/analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.md) 폴아웃 시각화의 컨텍스트에서 서로 다른 대상자가 어떻게 서로 비교되는지 확인하십시오.




>[!MORELIKETHIS]
>
>세그먼테이션과 Adobe Analytics에서 세그먼트를 만들고, 빌드하고, 관리하는 방법에 대한 소개는 [세그먼테이션 개요](/help/components/segmentation/seg-overview.md)를 참조하십시오.
