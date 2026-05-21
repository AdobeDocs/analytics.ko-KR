---
description: 책갈피가 지정된 모든 보고서 및 대시보드 보고서는 이제 요청 마법사 1단계에서 차원으로 표시되며 Report Builder 요청으로 가져올 수 있습니다.
title: 북마크가 지정된 보고서 및 대시보드 리포트릿 가져오기
feature: Report Builder
role: User, Admin
exl-id: 19813950-2495-4a75-aacb-587b59bf2484
TQID: https://experienceleague.adobe.com/dnOYs7eOvv15K73EPrfRegz1vH9-B5p8xI8d86vPYe4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 241
ht-degree: 18%

---

# 북마크가 지정된 보고서 및 대시보드 리포트릿 가져오기

{{legacy-arb}}

책갈피가 지정된 모든 보고서 및 대시보드 보고서는 이제 요청 마법사 1단계에서 차원으로 표시되며 Report Builder 요청으로 가져올 수 있습니다.

책갈피가 지정된 보고서를 선택하면 요청 마법사가 이 책갈피가 지정된 보고서를 정의하는 모든 차원과 지표를 채웁니다. 날짜 범위, 세부기간 및 선택한 세그먼트도 선택한 책갈피를 기반으로 업데이트됩니다.

다음은 요청 마법사 1단계에서 대시보드와 해당 reportlet을 표시하는 방법입니다.

![대시보드 검색 및 책갈피 검색을 강조 표시하는 요청 마법사 1단계/2를 보여 주는 스크린샷입니다.](assets/import_dashboard_reportlet.png)

**[!UICONTROL 대시보드 검색]** 또는 **[!UICONTROL 책갈피 검색]**&#x200B;을 클릭하면 기존 대시보드 및/또는 책갈피 데이터를 검색하여 워크시트에 붙여넣습니다.

>[!NOTE]
>
>데이터만 가져오므로 책갈피에 차트가 포함되어 있거나 대시보드 리포트릿이 차트로만 구성된 경우 차트를 채우는 데 사용되는 데이터만 가져옵니다.

대시보드 리포트릿(또는 책갈피)을 가져와서 요청을 만들면, 요청은 리포트릿(또는 책갈피)의 기본 차원에 연결됩니다. 따라서 요청을 편집하면 트리 보기에서 대시보드 리포트릿 트리 보기 노드(또는 책갈피 노드)가 더 이상 선택되지 않습니다. 대신 기본 차원이 선택됩니다.

