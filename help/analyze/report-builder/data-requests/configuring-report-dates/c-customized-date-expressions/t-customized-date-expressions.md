---
description: 사용자 지정 표현식을 만들어 복합적인 날짜 범위를 지정할 수 있습니다.
title: 사용자 지정된 날짜 표현식 - 개요
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
feature: Report Builder
role: User, Admin
exl-id: b3bdc07e-5c2d-4be3-86c9-b4b7380be0f6
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 30%

---

# 사용자 지정된 날짜 표현식 - 개요

사용자 지정 표현식을 만들어 복합적인 날짜 범위를 지정할 수 있습니다.

주 및 일 수를 올바르게 지정하려면 표현식을 작성할 때 달력을 참조하는 것이 좋습니다. Excel에는 날짜 간의 일, 업무일, 월 및 년 수를 계산할 수 있도록 해주는 몇 가지 내장 함수들이 있습니다. 공식에 이 함수들을 사용하여 주 수 및 분기 수와 같은 다른 간격들을 계산할 수 있습니다.

**사용자 지정 표현식을 활성화하는 방법**

**[!UICONTROL 순환 날짜]**&#x200B;를 사용하는 예시입니다.

1. [!UICONTROL 요청 마법사에서: 1단계]사전 설정 날짜&#x200B;]**를 사용하는 대신**[!UICONTROL &#x200B;순환 날짜&#x200B;]**를 선택합니다.**[!UICONTROL 

   ![](assets/rolldates1.png)

1. 주별, 월별, 분기별 또는 연도별 롤링 모드로 전환합니다. 아래 옵션이 어떻게 변경되는지 확인하십시오.
1. 추가 사용자 지정 옵션을 보려면 **[!UICONTROL 고급 옵션 표시]**&#x200B;를 클릭하십시오.

   ![](assets/rolldates2.png)

1. 예를 들어, 위의 날짜를 3개월 전 첫 번째 날부터 이번 달의 첫 번째 날로 변경하면 고급 옵션 부분의 날짜가 해당 날짜를 반영하도록 자체 업데이트됩니다.

   ![](assets/rolldatesfor3.png)

1. **[!UICONTROL 사용자 지정 표현식]**&#x200B;을 활성화합니다. **[!UICONTROL 롤링 날짜]** 아래에서 옵션을 선택하면 사용자 지정 날짜 표현식에 대한 구문을 쉽게 볼 수 있습니다.

   ![](assets/rolldatesfor5.png)

   고급 옵션을 사용하여 사용자 지정 날짜 표현식을 혼합하고 일치시킬 수 있습니다. 예를 들어 해당 연도의 첫 번째부터 마지막 전체 달 말까지 데이터를 보려는 경우 다음을 입력할 수 있습니다. `From: cy` `To: cm-1d` 마법사에서 해당 날짜가 1/1/2020-1/31/2020으로 표시됩니다.
