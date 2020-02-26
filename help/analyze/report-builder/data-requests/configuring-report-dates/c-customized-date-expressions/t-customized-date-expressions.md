---
description: 사용자 지정 표현식을 만들어 복합적인 날짜 범위를 지정할 수 있습니다.
title: 사용자 지정된 날짜 표현식 - 개요
topic: Report builder
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
translation-type: tm+mt
source-git-commit: fa1b0b7fb24d0cd2c205fbbb6a1e526f243531f8

---


# 사용자 지정된 날짜 표현식 - 개요

사용자 지정 표현식을 만들어 복합적인 날짜 범위를 지정할 수 있습니다.

주 및 일 수를 올바로 지정하려면 표현식을 작성할 때 달력을 참조하는 것이 좋습니다. Excel에는 날짜 간의 일, 업무일, 월 및 년 수를 계산할 수 있도록 해주는 몇 가지 내장 함수들이 있습니다. 공식에 이 함수들을 사용하여 주 수 및 분기 수와 같은 다른 간격들을 계산할 수 있습니다.

**사용자 지정 표현식을 활성화하는 방법**

이 예는 를 사용하는 **[!UICONTROL Rolling Dates]**&#x200B;예입니다.

1. 를 사용하는 [!UICONTROL Request Wizard: Step 1]대신 **[!UICONTROL Preset Dates]**&#x200B;에서 을 선택합니다 **[!UICONTROL Rolling Dates]**.

   ![](assets/rolldates1.png)

1. 주별, 월별, 분기별 또는 연간으로 전환할 수 있습니다. 아래 옵션이 어떻게 변경되는지 확인하십시오.
1. 추가 사용자 정의 옵션을 보려면 을 클릭합니다 **[!UICONTROL Show Advanced Options]**.

   ![](assets/rolldates2.png)

1. 예를 들어, 위의 날짜를 3개월 전 첫 번째 날부터 이번 달의 첫 번째 날로 변경하는 경우, 사전 옵션 부분에 있는 날짜는 이를 반영하도록 자체적으로 업데이트됩니다.

   ![](assets/rolldatesfor3.png)

1. 활성화 **[!UICONTROL Customize Expression]**. 아래에서 옵션을 선택하면 사용자 지정 날짜 표현식의 구문을 쉽게 볼 수 **[!UICONTROL Rolling Dates]**&#x200B;있습니다.

   ![](assets/rolldatesfor5.png)

   고급 옵션을 사용하여 사용자 지정 날짜 표현식을 혼합하고 일치시킬 수 있습니다. 예를 들어 연도의 첫 번째부터 마지막 전체 월의 끝까지 데이터를 보려면 다음을 입력할 수 있습니다. `From: cy``To: cm-1d`5. 마법사에서 이러한 날짜는 2020년 1월 1일/1/31/2020으로 표시됩니다.
