---
title: 동적 및 정적 Dimension 항목
description: Analysis Workspace의 자유 형식 테이블에서 동적 차원 항목과 정적 차원 항목을 사용하는 방법에 대해 알아봅니다.
feature: Freeform Tables
role: User, Admin
exl-id: 4cdc93b5-67ed-46a4-ba9f-a96e640da9d9
source-git-commit: f258a1150a4bee11f5922d058930dc38b1ddfa14
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 94%

---

# 동적 및 정적 차원 항목

자유 형식 테이블에서 행과 열에는 다양한 구성 요소 값이 포함될 수 있습니다. 이러한 값은 빌드할 분석에 따라 동적(시간에 따라 변경) 또는 정적(시간에 따라 변경되지 않음)일 수 있습니다.

## 동적 차원 항목

동적 차원 항목은 시간에 따라 변경되며 자유 형식 테이블에서 정렬되는 지표에 따라 달라집니다. 지정된 기간 동안 상위 항목을 분석하려는 경우 동적 차원 항목을 사용하는 것이 좋습니다.

차원을 자유 형식 테이블에 놓으면 동적 행이 반환됩니다. 동적 행은 지정된 지표 및 기간에 대한 차원에 해당하는 상위 항목을 나타냅니다. 차원을 자유 형식 테이블 열에 놓을 수도 있으며 이 차원은 상위 5개 차원 항목으로 자동으로 확장됩니다.

예를 들어 브라우저 유형 차원을 테이블로 드래그하면 상위 브라우저 유형 차원 항목(예: Microsoft, Apple, Google 등)이 동적으로 테이블 행에 반환됩니다. 열에 놓으면 상위 5개의 브라우저 유형 차원 항목이 동적으로 반환됩니다.

동적 차원 항목에는 행 필터 옵션인 ![필터](/help/assets/icons/Filter.svg)와 ![닫기](/help/assets/icons/Close.svg)가 있으며, 잠금 ![LockClosed](/help/assets/icons/LockClosed.svg)이 **없습니다**. <!--do they have the lock icon? --> 동적 차원 항목 옆에 있는 ![닫기](/help/assets/icons/Close.svg)를 클릭하면 필터가 자동으로 적용됩니다. 테이블에 필터를 적용하는 방법에 대한 자세한 내용은 [테이블 필터링 및 정렬](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)을 참조하십시오.


![필터 아이콘을 강조 표시한 자유 형식 테이블.](assets/dynamic-items.png)

## 정적 차원 항목

정적 차원 항목은 시간에 따라 변경되지 않습니다. 자유 형식 테이블에서 항상 반환되는 고정 구성 요소입니다. 정적 차원 항목은 특정 캠페인이든 그 주의 특정 요일이든 항상 동일한 항목을 분석하려는 경우 선호됩니다.

특정 구성 요소 값(차원, 지표, 필터, 날짜 범위)을 수동으로 선택하여 테이블에 놓을 때마다 그 결과는 행 또는 열의 정적 목록입니다.

예를 들어 Microsoft나 Apple과 같은 특정 브라우저 유형 항목 위로 드래그하면 그 2개의 특정 항목이 항상 테이블에 표시되게 됩니다.

선택한 행의 컨텍스트 메뉴에서 **[!UICONTROL 선택한 행만 표시]**&#x200B;를 선택하면 정적 차원 항목도 만들 수 있습니다.

정적 차원 항목에는 행 필터 옵션이 **없습니다**. 대신 각 항목에는 ![LockClosed](/help/assets/icons/LockClosed.svg)와 ![닫기](/help/assets/icons/Close.svg)가 표시됩니다. ![닫기](/help/assets/icons/Close.svg)를 선택하여 테이블에서 해당 차원 항목을 제거합니다.

![잠금 아이콘이 있는 자유 형식 테이블의 브라우저 유형과 Microsoft 행(참고: 이 차원 항목은 정적이며 시간이 지나도 변경되지 않습니다.)](assets/static-items.png)

## 혼합 차원 항목

다른 차원의 차원 항목을 동일한 테이블에 추가할 수 있습니다. 이러한 경우 행 헤더에 **[!UICONTROL 혼합 차원]**&#x200B;이 표시됩니다. 이러한 차원 항목은 정적입니다. 예를 들어 브라우저 그룹 차원의 특정 차원 항목과 브라우저 이름 차원의 기타 차원 항목을 추가하는 경우가 있습니다.

![혼합 차원 열을 강조 표시한 자유 형식 테이블.](assets/mixed-dimensions.png)

## 자유 형식 합계 행

동적 및 정적 행은 자유 형식 합계 행에서 다르게 동작합니다. 기본적으로

* 동적 행은 세션이나 개인과 같이 합계로서 계산된 서버측 및 중복 제거 지표입니다.
* 정적 행은 클라이언트측에서 합해지며 지표에 대해 중복 제거를 수행하지 **않습니다**. 합계 행 서버측을 계산하려면 행 설정을 **총계 표시**&#x200B;로 변경하십시오. [자세히 알아보기](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md)


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [정적 행 순서 바꾸기](https://video.tv.adobe.com/v/33274?quality=12&learn=on&captions=kor){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]


