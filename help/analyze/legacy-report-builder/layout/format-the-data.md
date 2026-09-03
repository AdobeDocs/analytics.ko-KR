---
description: 표준 및 제한된 서식을 셀 범위에 적용하는 방법을 알아봅니다.
title: Report Builder에서 날짜 형식을 지정하는 방법
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
feature: Report Builder
role: User, Admin
exl-id: 9b251b09-9156-40b5-8e1f-fb6594a25c26
TQID: https://experienceleague.adobe.com/8FuosvmSvi-bRNaG5QbwUExuDffOIXbrkuiQLh0NZXM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 20%

---

# 날짜 포맷 지정

{{legacy-arb}}

Excel의 서식 > 셀(Ctrl+1) 기능을 통해 사용할 수 있는 표준 셀 서식 선택 항목 외에도 Report Builder을 사용하는 셀 범위에 제한된 서식을 적용할 수 있습니다. 이러한 서식 선택 사항은 선택한 지표에 따라 다릅니다.

Row Labels 그리드에 [차원을 추가](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md)한 후 **[!UICONTROL 서식]**&#x200B;을 클릭합니다.

**[!UICONTROL 서식]** 메뉴에서 **[!UICONTROL 사용자 지정 형식]**&#x200B;을 클릭하여 프리펜드 및 포스트펜드 기능과 유사한, 날짜에 대한 사용자 지정된 형식을 적용합니다. 예를 들어, 날짜 이후에 항상 발생하는 텍스트(예: A.D. B.C.E. A.H 등)를 입력할 수 있습니다. 날짜 이전에 [!UICONTROL 시작 날짜] 및 [!UICONTROL 시작 및 종료 날짜]와 같은 텍스트를 추가할 수 있습니다. 또한 일, 월, 년 약어로 사용자 정의 날짜 표현식을 만들고 날짜 부분 사이에 사용자 정의 구분 기호를 사용할 수 있습니다. 모든 날짜 형식은 대괄호로만 둘러싸인 세 개의 약어로 구성되어야 합니다.

다음 표에서는 [!UICONTROL 사용자 지정 형식] 필드에서 날짜 약어를 사용하는 방법을 설명합니다.

| 약어 | 의미 | 2012년 3월 14일 수요일 사용 예 |
|--- |--- |--- |
| MM/dd/yyy | 전체 숫자 날짜 | 03/14/2012 |
| M | 월 수 | 3 |
| MM | 개월 &lt; 10에 대해 0의 패딩이 있는 월 수 | 03 |
| MMM | 월의 약식 이름 | 3월 |
| MMMM | 월의 긴 이름 | 3월 |
| D | 날짜의 긴 이름 | 2012년 3월 14일 목요일 |
| d | 일 수 | 14 |
| dd | 일 &lt; 10에 대해 0개의 패딩이 있는 일 수 | 01 - 09 |
| ddd | 짧은 일 이름 | 수요일 |
| dddd | 오늘의 긴 이름 | 수요일 |
| yy | 자리 연도 | 10 |
| yyyy | 전체 4자리 연도 | 2012 |
