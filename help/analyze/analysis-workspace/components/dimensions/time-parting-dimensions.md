---
description: 시간 분할 차원이 수집된 이벤트의 타임스탬프를 가져오고 이러한 이벤트를 시간 또는 요일 과 같은 더 의미 있는 차원으로 분류하는 방법에 대해 알아봅니다.
title: 차원 시간 분할
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 20%

---

# 차원 시간 분할

시간 분할은 수집한 히트의 타임스탬프를 가져와서 **시간** 또는 **요일**&#x200B;과 같은 더 의미 있는 차원으로 분할합니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [시간 분할 차원](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/time-parting-dimensions-in-analysis-workspace){target="_blank"}을 참조하십시오.

>[!ENDSHADEBOX]


시간 분할 차원은 보고서 세트 또는 가상 보고서 세트의 시간대를 기반으로 합니다. 이러한 차원은 Analysis Workspace에서 사용할 수 있으며 다음 질문에 답변하는 데 도움이 될 수 있습니다.

* 큰 날짜 범위에서 방문자가 내 사이트 또는 앱에 액세스하는 데 가장 인기 있는 시간은 무엇입니까?
* 내 사이트 또는 앱에서 전환율이 더 높은 요일 또는 시간이 있습니까?
* 주말 매출액은 평일 매출액과 어떻게 비교됩니까?
* 특정 마케팅 캠페인이 오전 또는 오후에 더 높은 전환율을 생성합니까?

>[!NOTE]
>
>시간 분할 차원은 Analysis Workspace에서만 사용할 수 있습니다. 다른 Analytics 솔루션에서 시간 분할 차원을 사용하려면 [getTimeParting 플러그인](/help/implement/vars/plugins/gettimeparting.md)을 구현할 수 있습니다.

Analysis Workspace의 시간 분할 차원은 다음과 같습니다.

| 차원 | 값 예 |
| --- | --- |
| 시간 | 0-23 |
| 오전/오후 | 오전, 오후 |
| 요일 | 월요일, 화요일, 수요일, 목요일, 금요일, 토요일, 일요일 |
| 주말/평일 | 주말, 평일 |
| 날짜(월 기준) | 1-31 |
| 월 | 1월-12월 |
| 일(한 해 기준) | 1-366 |
| 사분기 | Q1, Q2, Q3, Q4 |
