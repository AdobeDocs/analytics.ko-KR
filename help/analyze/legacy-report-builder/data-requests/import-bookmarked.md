---
description: 책갈피가 지정된 모든 보고서와 대시보드 보고서는 이제 요청 마법사 1단계에서 차원으로 표시되며, Report Builder 요청으로 가져올 수 있습니다.
title: 북마크가 지정된 보고서 및 대시보드 리포트릿 가져오기
feature: Report Builder
role: User, Admin
exl-id: 19813950-2495-4a75-aacb-587b59bf2484
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 65%

---

# 북마크가 지정된 보고서 및 대시보드 리포트릿 가져오기

{{legacy-arb}}

책갈피가 지정된 모든 보고서와 대시보드 보고서는 이제 요청 마법사 1단계에서 차원으로 표시되며, Report Builder 요청으로 가져올 수 있습니다.

책갈피가 지정된 보고서를 선택하면 요청 마법사는 책갈피가 지정된 보고서를 정의하는 모든 차원 및 지표를 채웁니다. 날짜 범위, 세부기간 및 선택한 세그먼트도 선택한 책갈피를 기반으로 업데이트됩니다.

요청 마법사 1단계에는 다음과 같이 대시보드 및 해당 Reportlet이 표시됩니다.

![대시보드 검색 및 책갈피 검색을 강조 표시하는 요청 마법사 1단계/2를 보여 주는 스크린샷입니다.](assets/import_dashboard_reportlet.png)

**[!UICONTROL [대시보드 검색]]**&#x200B;이나 **[!UICONTROL [책갈피 검색]]**&#x200B;을 클릭하면, 기존 대시보드 및/또는 책갈피 데이터가 검색되고 워크시트에 붙여넣어집니다.

>[!NOTE]
>
>데이터만 가져오므로 책갈피에 차트가 포함되어 있거나 대시보드 리포트릿이 차트로만 구성된 경우 차트를 채우는 데 사용되는 데이터만 가져옵니다.

대시보드 Reportlet(또는 책갈피)를 가져와 요청을 만들었으므로 요청은 Reportlet(또는 책갈피)의 기본 차원에 연결됩니다. 따라서 요청을 편집하는 경우 트리 보기는 더 이상 대시보드 Reportlet 트리 보기 노드(또는 책갈피 노드)를 선택하지 않으며 대신 기본 차원을 선택합니다.

