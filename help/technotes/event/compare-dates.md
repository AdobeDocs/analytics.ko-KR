---
title: 이벤트의 영향을 받은 날짜와 이전 범위 비교
description: 이전 트렌드와 비교하여 구현 문제 또는 중단과 같은 이벤트의 영향에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---


# 이벤트의 영향을 받은 날짜와 이전 범위 비교

이벤트의 [영향을 받은 데이터가 있는](overview.md)경우 내역 트렌드를 확인하여 영향을 평가할 수 있습니다. 이러한 비교는 이벤트가 데이터에 미치는 영향을 파악하는 데 유용합니다. 따라서 데이터를 제외할지, 보고서에 메모를 추가할지 또는 무시할지를 결정할 수 있습니다.

## 이벤트를 포함하는 날짜 범위 만들기

해당 이벤트의 영향을 탐색하기 시작할 이벤트를 포함하는 날짜 범위를 만듭니다.

1. 구성 **[!UICONTROL 요소]** > **[!UICONTROL 날짜 범위로 이동합니다]**.
2. **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
3. 이벤트가 발생한 날짜 범위를 선택합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![날짜 범위 빌더](assets/date_range_builder.png)

## 이벤트 날짜 및 유사한 이전 범위 나란히 보기

자유 형식 테이블 시각화를 사용하여 이벤트의 날짜 범위와 비슷한 이전 날짜 범위 간의 지표를 비교할 수 있습니다.

1. 작업 공간 프로젝트를 열고 자유 형식 테이블에 &#39;일&#39; 차원을 추가합니다. &#39;발생&#39;과 같은 지표에 스택된 최근 만든 날짜 범위를 적용합니다.

   ![날짜 범위 지표](assets/date_range_metric.png)

2. 날짜 범위를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL 기간 추가 열]** > **[!UICONTROL 이 날짜 범위에 대한 사용자 지정 날짜 범위를 클릭합니다]**.
   * 일주일 간 비교를 위해 이벤트 범위를 빼기 7일을 선택합니다. 이벤트와 이 날짜 범위 사이의 요일이 정렬되었는지 확인하십시오.
   * 월정액 비교를 위해 지난 달 이벤트 범위를 선택합니다. 요일을 정렬하려는 경우 이벤트 범위를 빼기 28일을 선택할 수도 있습니다.
   * 1년 이상 비교의 경우 작년 이벤트 범위를 선택합니다.
3. 원하는 날짜 범위를 선택하면 자유 형식 테이블에 추가됩니다. 을 마우스 오른쪽 단추로 클릭하고 비교할 날짜 범위를 추가할 수 있습니다.

   ![날짜 정렬된 트렌드](assets/date_aligned_trends.png)

## 이벤트와 유사한 이전 범위 간의 백분율 차이 계산

자유 형식 테이블 시각화를 사용하여 이벤트의 날짜 범위와 비슷한 이전 날짜 범위 간의 차원 항목을 비교합니다. 다음 단계는 다음을 수행할 수 있는 주 단위 예를 보여 줍니다.

1. 작업 공간 프로젝트를 열고 자유 형식 테이블에 **비시간 차원을** 추가합니다. 예를 들어 &#39;모바일 장치 유형&#39; 차원을 사용할 수 있습니다. &#39;발생 횟수&#39;와 같이 지표에 스택된 최근 만든 날짜 범위를 적용합니다.

   ![영향을 받는 날짜 범위별 모바일 장치 유형](assets/mobile_device_type.png)

2. 날짜 범위를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL 기간 비교]** > **[!UICONTROL 사용자 지정 날짜 범위를 이 날짜 범위로 클릭합니다]**. 이벤트의 범위를 7일 이내로 선택합니다. 이벤트와 이 날짜 범위 사이의 요일이 정렬되었는지 확인하십시오.

   ![기간 비교 메뉴](assets/compare_time_custom.png)

3. 결과 &quot;변경 퍼센트&quot; 지표의 이름을 &quot;영향을 받는 범위&quot;와 같이 좀 더 구체적인 것으로 바꿉니다. 정보 아이콘을 클릭한 다음 연필 편집을 클릭하여 지표 이름을 편집합니다.

   ![주 단위](assets/wow_affected_range.png)

4. 월정액 및 연간 비교를 위해 3단계와 4단계를 반복합니다. 동일한 테이블에서 이 작업을 수행하거나 테이블을 분리할 수 있습니다.

## 비교 날짜 범위를 행으로 나란히 분석

위의 퍼센트 변경 사항을 더 자세히 분석하려면 행을 변환할 수 있습니다.

1. 자유 형식 테이블 시각화를 추가하고 테이블 빌더를 활성화합니다. 이 작업을 사용하면 백분율 변경 지표를 원하는 순서로 배치할 수 있습니다.
2. 3% 변경 지표 `Ctrl` (Windows) 또는 `Cmd` (Mac)를 한 번에 하나씩 표의 행으로 드래그합니다.

   ![테이블 빌더](assets/table_builder.png)

3. 테이블의 열 및 기타 원하는 세그먼트에 &#39;모든 방문&#39; 세그먼트를 추가합니다.

   ![테이블 빌더 세그먼트](assets/table_builder_segments.png)

4. **[!UICONTROL 작성을 클릭합니다]**. 결과 테이블에서 원하는 모든 세그먼트에서 영향을 받는 범위와 이전 주, 월 및 연도를 볼 수 있습니다.

   ![완성된 표](assets/table_builder_finished.png)
