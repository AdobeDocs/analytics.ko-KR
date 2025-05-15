---
description: 계산된 지표 및 고급 계산된 지표는 기존의 지표에서 만들 수 있는 사용자 정의 지표입니다.
keywords: 계산된 지표;고급 계산된 지표
title: 계산된 지표 및 고급 계산된 지표
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: ht
source-wordcount: '552'
ht-degree: 100%

---

# 계산된 지표 및 고급 계산된 지표

계산된 지표 및 고급 계산된 지표는 기존의 지표에서 만들 수 있는 사용자 정의 지표입니다.

Adobe의 계산된 지표 도구에서는 지표를 작성하고, 관리하고, 조정하는 유연한 방법을 제공합니다. 이 도구를 사용하는 마케터, 제품 관리자 및 분석가는 [!DNL Analytics] 구현을 변경하지 않아도 데이터에 대해 질문할 수 있습니다. 각 [!DNL Analytics] 패키지에서 사용할 수 있는 사용자 정의 지표는 다음과 같습니다.

* Adobe [!DNL Analytics] Foundation: 계산된 지표
* [Adobe Analytics Select](https://www.adobe.com/kr/data-analytics-cloud/analytics/select.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Prime](https://www.adobe.com/kr/data-analytics-cloud/analytics/prime.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Ultimate](https://www.adobe.com/kr/data-analytics-cloud/analytics/ultimate.html): 계산된 + 고급 계산된 지표

다음은 계산된 지표와 고급 계산된 지표 기능을 비교한 것입니다.

| Builder 옵션 | 계산된 지표 | 고급 계산된 지표 |
|---|---|---|
| [형식 유형 (십진수, 시간, 퍼센트, 통화)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | 예 | 예 |
| [기여도 분석 변경 (기본값, 선형, 기여도 등)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | 예 | 예 |
| [지표 유형 (표준, 전체)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | 예 | 예 |
| 기본 연산자 (더하기, 빼기, 곱하기, 나누기) | 예 | 예 |
| [세그먼트 적용](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) | 아니요 | 예 |
| [기본 함수 (수, 절대값, 평균 등)](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | 아니요 | 예 |
| [고급 함수 (회귀, if/then, T 스코어 등)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | 아니요 | 예 |

## 기능 {#section_A0A5C275B68A4D628950BBB0B1EE631F}

다음과 같은 작업을 수행할 수 있습니다.

* [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL 예외 항목 탐지] 및 [!UICONTROL 기여도 분석]에서 지표를 만들 수 있습니다.
* 구현을 변경하지 않고도 보고서 실행 시 파생된 세그먼트화된 지표를 만들 수 있습니다. 이러한 지표는 세그먼트를 기반으로 하므로 기록에서 볼 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [계산된 지표](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

* 보고서 세트 간에 지표를 공유할 수 있습니다. 이것은 새로 만들어진 모든 지표가 동일한 로그인 회사에 있는 모든 보고서 세트에 적용됨을 의미합니다.
* (고급 계산된 지표만 해당) 지표의 세그먼트. 예를 들어 첫 번째 세션에 참여한 사람의 수로, “새 방문자 수”에 대한 지표를 만들 수 있습니다.

* (고급 계산된 지표만 해당) 통계 함수를 통합하여 데이터를 더욱 효율적으로 설명할 수 있습니다. 예를 들어 보고서에 있는 항목의 수를 계산하거나 각 항목에 대한 표준 편차의 수를 추가할 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트 내 세그먼트화된 계산된 지표](https://video.tv.adobe.com/v/25409?quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]


## 제한 사항 {#section_CB878B02451541D68A68B508D4DBD19A}

일부 [!DNL Analytics] 기능은 이벤트를 사용할 수 있지만 계산된 지표는 사용할 수 없습니다.

* Analysis Workspace의 폴아웃
* [!UICONTROL Analysis Workspace의 집단 분석]
* [!UICONTROL Data Warehouse]
* [!UICONTROL 세그먼트]
* [!DNL Analytics] for [!DNL Target]

## 도구 {#section_D65E9C067E9C45E1A50DD30F50561BB2}

다음은 [!UICONTROL 계산된 지표] 도구에 대한 간략한 개요입니다.

| 도구 | 기능 |
|--- |--- |
| 계산된 지표 빌더에서 계산된 지표를 작성합니다. | <ul><li>고급 할당 모델을 사용하여 계산된 지표 및 고급 계산된 지표를 생성합니다.</li><li>인라인 세그먼트를 지표 공식에 추가할 수 있습니다.</li><li>동일한 보고서에서 세그먼트들을 비교할 수 있습니다. 예를 들어 로컬 방문자와 해외 방문자를 비교할 수 있습니다.</li><li>통계 함수를 사용할 수 있습니다.</li><li>상세한 지표 설명을 제공할 수 있습니다(수행하는 작업, 사용할 곳, 사용하지 말아야 곳을 보여줌).</li><li>정의를 새 지표에 복사할 수 있습니다.</li><li>인라인 지표 미리보기를 제공할 수 있습니다.</li><li>주어진 사용자 정의 이벤트(지표)가 상승한다면 이것이 좋은 것인지 나쁜 것인지를 가리키는 지표 극성을 설정할 수 있습니다.</li><li>지표에 태그를 지정할 수 있습니다.</li></ul> |
| 계산된 지표 관리자 | <ul><li>지표를 다른 사람과 공유할 수 있습니다.<li>지표를 승인 및 조정할 수 있습니다.</li><li>사람들이 찾을 수 있도록 지표를 정리(태그 지정)할 수 있습니다.</li><li>지표를 삭제할 수 있습니다.</li><li>지표의 이름을 변경할 수 있습니다.</li></ul> |
| 지표 선택기 레일 | 지표를 검색하고 보고서에 추가/적용할 수 있도록 해 줍니다. 정렬 순서를 변경할 수도 있습니다(옵션: 알파벳, 권장, 자주 사용하는 항목, 최근에 사용한 항목). 또한 보고서 세트를 필터링하여 특정 보고서 세트에서 생성된 지표만 표시할 수도 있습니다.  지표 선택기에 액세스하려면 보고서 왼쪽에 있는 지표 아이콘을 클릭합니다. |
| 계산된 지표에 대한 API | Adobe Analytics 2.0 API 세트의 일부. |
