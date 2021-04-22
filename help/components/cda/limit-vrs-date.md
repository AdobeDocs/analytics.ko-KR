---
title: VRS를 특정 날짜로 제한
description: 연결된 데이터에만 집중하도록 VRS 날짜 범위를 제한하는 방법을 이해합니다.
exl-id: 421d101d-8c64-47f7-b5a2-da039889f663
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '256'
ht-degree: 100%

---

# VRS를 특정 날짜로 제한

연결을 켜면 특정 날짜에 연결이 시작됩니다. 날짜가 6월 1일이라고 가정해 보겠습니다. CDA VRS에는 6월 1일 이전에 연결되지 않은 데이터가 포함됩니다. 연결이 시작된 후 분석이 날짜 범위에 집중할 수 있도록 6월 1일 이전 VRS의 데이터를 숨길 수 있습니다.

다음을 수행하여 VRS 데이터를 특정 날짜로 제한할 수 있습니다.

## 1단계: 일별 롤링 날짜 범위를 사용하여 VRS 만들기

VRS를 설정할 때 구성 요소에서 고정된 시작 날짜가 있는 날짜 범위와 일별 롤링 날짜 범위를 추가합니다. 고정된 시작 날짜는 연결이 시작된 날이어야 합니다.

![](assets/rolling-daily.png)

## 2단계: “exclude-exclude” 세그먼트 만들기

다음으로 다른 제외 컨테이너 내의 제외 컨테이너에 날짜 범위를 넣는 히트 세그먼트를 만듭니다. 이것이 “exclude-exclude”입니다.

“exclude-exclude”를 하는 이유는 날짜 범위가 보고서의 날짜 범위를 재정의하기 위한 것입니다. 따라서 6월 1일 이후만 포함하면 항상 보고서 날짜 범위가 6월 1일 이후로 설정됩니다. 이로 인해 원하지 않는 결과가 발생합니다. “exclude-exclude”는 이 동작을 무시하고 가져올 수 있는 데이터를 적절한 날짜 범위로 제한합니다.

![](assets/exclude-exclude.png)

## 3단계: 이 세그먼트를 CDA VRS에 적용

![](assets/apply-segment.png)

## 4단계: 보고에서 결과 확인

이제 보고가 원하는 날짜 (연결이 처음 구현된 당일)에 시작됩니다.

![](assets/report-limited-dates.png)
