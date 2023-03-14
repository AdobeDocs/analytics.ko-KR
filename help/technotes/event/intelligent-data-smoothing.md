---
title: 지능성 데이터 평활화
description: Intelligent Data Smoothing이 기간별 트렌드를 분석하여 영향을 받는 기간 내의 모든 지표의 값을 예측하는 방법을 알아봅니다.
feature: AI Tools
role: User, Admin
exl-id: b7a2e5d5-99d4-408d-84e6-67abff9e8727
source-git-commit: e0a4caec9bc58a0846cd46871aad3bed99d218a3
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 4%

---

# 지능성 데이터 평활화

드문 경우지만 일부 요소는 데이터 품질에 영향을 줄 수 있습니다. 보트 트래픽, 구현 변경 또는 서비스 중단은 모두 수집된 데이터의 무결성에 영향을 줄 수 있습니다. 또한 이벤트가 데이터 완전성에 어떤 영향을 미쳤을 수 있는지에 대한 분석도 복잡합니다.

Intelligent Data Smoothing은 의 프로토타입입니다 [Analytics Lab](/help/analyze/labs.md) 기간별 추세를 분석하여 영향을 받는 기간 내의 모든 지표 값을 예측하여 이 보기를 완료하는 데 도움이 될 수 있습니다. 프로토타입은 고급 머신 러닝 알고리즘을 적용하여 분석되는 기간 동안 지표에 대한 예상 값을 플롯합니다.

## 지능형 데이터 평활화 실행

1. Adobe Analytics Labs로 이동합니다.
   ![Labs](assets/labs.png)
1. Intelligent Data Smoothing 프로토타입을 시작합니다.
   ![프로토타입 실행](assets/intelligent-ds.png)
1. 분석해야 하는 지표를 자유 형식 테이블에 추가합니다. 프로토타입은 일별 세부기간에서만 작동하므로 테이블의 차원이 요일인지 확인합니다.
   ![지표 추가](assets/add-metric.png)
1. 이벤트의 창보다 넓은 날짜 범위를 선택하되 이벤트에 포함되어 있는지 확인하십시오.
   ![날짜 범위](assets/date-range.png)
1. 자유 형식 테이블에서 지표에 대한 톱니바퀴 아이콘을 클릭합니다.
   ![톱니바퀴 아이콘](assets/gear-icon.png)
1. 아래 [!UICONTROL 데이터 설정]를 선택하고 [!UICONTROL 데이터 매끄럽게 하기] 옵션을 선택합니다.
   ![데이터 매끄럽게 하기](assets/column-setting.png)
1. 이벤트에 해당하는 날짜/날짜 범위를 선택하고 [!UICONTROL 적용].
데이터 평활화에 대한 데이터 범위가 패널에 대해 선택한 날짜 범위의 하위 집합인지 확인합니다. 표 및 그래프의 지표는 예측된 값으로 대체됩니다.
   ![예측된 값](assets/predictive-values.png)
