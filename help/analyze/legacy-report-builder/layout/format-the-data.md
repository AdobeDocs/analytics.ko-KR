---
description: 표준 및 제한된 서식을 셀 범위에 적용하는 방법을 알아봅니다.
title: Report Builder에서 날짜 형식을 지정하는 방법
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
feature: Report Builder
role: User, Admin
exl-id: 9b251b09-9156-40b5-8e1f-fb6594a25c26
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 81%

---

# 날짜 형식 지정

{{legacy-arb}}

Excel의 서식 > 셀(Ctrl+1) 기능을 통해 사용할 수 있는 표준 셀 서식 선택 항목 외에도 Report Builder이 있는 셀 범위에 제한된 서식을 적용할 수 있습니다. 이러한 서식 지정 선택 사항은 선택한 지표에 따라 다릅니다.

Row Labels 그리드에 [차원을 추가](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md)한 후 **[!UICONTROL 서식]**&#x200B;을 클릭합니다.

**[!UICONTROL 서식]** 메뉴에서 **[!UICONTROL 사용자 지정 형식]**&#x200B;을 클릭하여 프리펜드 및 포스트펜드 기능과 유사한, 날짜에 대한 사용자 지정된 형식을 적용합니다. 예를 들어 날짜 다음에 항상 표시되는 텍스트(A.D. B.C.E. A.H. 등)를 입력할 수 있습니다. 날짜 앞에 [!UICONTROL 시작 날짜] 및 [!UICONTROL 시작 및 종료 날짜]와 같은 텍스트를 추가할 수도 있습니다. 이 이외에도 일, 월 및 연도 약자로 사용자 지정 날짜 표현식을 만들고 날짜의 부분들 사이에 사용자 지정 구분 문자를 사용할 수 있습니다. 모든 날짜 형식은 대괄호만으로 묶여 있는 세 개의 약자로 구성되어야 합니다.

다음 표에서는 [!UICONTROL 사용자 지정 형식] 필드에서 날짜 약자를 사용할 수 있는 방법에 대해 설명합니다.

| 약자 | 의미 | 예   2012년 3월 14일 수요일 사용 |
|--- |--- |--- |
| yyy/dd/MM | 전체 숫자 날짜 | 2012/03/14 |
| M | 월의 숫자 | 3 |
| MM | 10보다 작은 달에 대해 십의 자리에 0을 사용하는 월의 숫자 | 03 |
| MMM | 월의 짧은 이름 | 3월 |
| MMMM | 월의 긴 이름 | 3월 |
| D | 날짜의 긴 이름 | 2012년 3월 14일 목요일 |
| d | 일의 숫자 | 14 |
| dd | 10보다 작은 일에 대해 십의 자리에 0을 사용하는 일의 숫자 | 01 - 09 |
| ddd | 일의 짧은 이름 | 수 |
| dddd | 일의 긴 이름 | 수요일 |
| yy | 2자리 연도 | 10 |
| yyyy  | 4자리 전체 연도 | 2012 |
