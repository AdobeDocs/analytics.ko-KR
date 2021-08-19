---
title: 지능성 데이터 평활화
description: 지능형 데이터 평활법 을 통해 내역 트렌드를 분석하여 영향을 받는 기간 내의 모든 지표의 값을 예측하는 방법을 알아봅니다.
feature: AI 도구
role: User, Admin
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 5%

---

# 지능성 데이터 평활화

드문 경우, 일부 요소는 데이터 품질에 영향을 줄 수 있습니다. 보트 트래픽, 구현 변경 또는 서비스 중단은 모두 수집된 데이터의 무결성에 영향을 줄 수 있습니다. 또한 이 이벤트가 데이터 완전성에 미치는 영향에 대한 분석을 복잡하게 만듭니다.

지능형 데이터 평활법은 영향을 받는 기간 내의 모든 지표의 값을 예측하기 위한 내역 트렌드를 분석하여 이 보기를 완료하는 데 도움이 되는 [Analytics Labs](/help/analyze/labs.md)의 프로토타입입니다. 프로토타입에서는 고급 기계 학습 알고리즘을 적용하여 분석 기간 동안 지표에 대한 예상 값을 그래프로 표시합니다.

## 지능형 데이터 평활 실행

1. Adobe Analytics Labs로 이동합니다.
   ![Labs](assets/labs.png)
1. 지능형 데이터 평활 프로토타입을 시작합니다.
   ![프로토타입 시작](assets/intelligent-ds.png)
1. 자유 형식 테이블에 분석해야 하는 지표를 추가합니다. 프로토타입은 일별 세부기간에서만 작동하므로 테이블의 차원이 일인지 확인합니다.
   ![지표 추가](assets/add-metric.png)
1. 이벤트 창보다 넓은 날짜 범위를 선택하되, 이벤트가 포함되어 있는지 확인하십시오.
   ![날짜 범위](assets/date-range.png)
1. 자유 형식 테이블에서 지표에 대한 톱니바퀴 아이콘을 클릭합니다.
   ![톱니바퀴 아이콘](assets/gear-icon.png)
1. [!UICONTROL 데이터 설정]데이터 평활] 옵션을 선택합니다.[!UICONTROL 
   ![데이터 평활](assets/column-setting.png)
1. 이벤트에 해당하는 날짜/날짜 범위를 선택하고 [!UICONTROL 적용]을 클릭합니다.
데이터 평활법 데이터 범위가 패널에 대해 선택한 날짜 범위의 하위 집합인지 확인합니다. 테이블 및 그래프의 지표는 예측된 값으로 대체됩니다.
   ![예측된 값](assets/predictive-values.png)
