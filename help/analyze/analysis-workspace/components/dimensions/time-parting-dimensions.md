---
description: 시간 분할 차원이 수집된 이벤트의 타임스탬프를 가져오고 이러한 이벤트를 시간 또는 요일 과 같은 더 의미 있는 차원으로 분류하는 방법에 대해 알아봅니다.
title: 시간 분할 차원
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
source-git-commit: bf8bc40e3ec325e8e70081955fb533eee66a1734
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 74%

---

# 차원 시간 분할

시간 분할은 수집한 히트의 타임스탬프를 가져와서 **시간** 또는 **요일**&#x200B;과 같은 더 의미 있는 차원으로 분할합니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [시간 분할 차원](https://video.tv.adobe.com/v/30906?quality=12&learn=on&captions=kor){target="_blank"}을 참조하십시오.

>[!ENDSHADEBOX]


시간 분할 차원은 보고서 세트 또는 가상 보고서 세트의 시간대를 기반으로 합니다. 이러한 차원은 Analysis Workspace에서 사용할 수 있으며, 다음 질문에 대한 답변을 제공하는 데 도움을 줄 수 있습니다.

* 넓은 날짜 범위에서 방문자가 내 사이트나 앱에 가장 많이 오는 시간은 언제입니까?
* 내 사이트 또는 앱에서 전환율이 더 높은 요일이나 시간대가 있습니까?
* 평일 판매와 주말 판매를 비교하면 어떻습니까?
* 아침 또는 오후에 특히 전환이 높게 생성되는 특정 마케팅 캠페인이 있습니까?

>[!NOTE]
>
>시간 분할 차원은 Analysis Workspace에서만 사용할 수 있습니다. 다른 분석 솔루션에서 시간 분할 차원을 사용하려면 [getTimeParting 플러그인](https://experienceleague.adobe.com/docs/analytics/implementation/vars/plugins/gettimeparting.html?lang=ko-KR)을 구현할 수 있습니다.

Analysis Workspace의 시간 분할 차원에는 다음 항목이 포함됩니다.

| 차원 | 예제 값 |
| --- | --- |
| 시간 | 0-23 |
| 오전/오후 | 오전, 오후 |
| 요일 | 월요일, 화요일, 수요일, 목요일, 금요일, 토요일, 일요일 |
| 주말/평일 | 주말, 평일 |
| 날짜(월 기준) | 1-31 |
| 월 | 1월~12월 |
| 일(한 해 기준) | 1-366 |
| 사분기 | Q1, Q2, Q3, Q4 |
